# Godot'ta Scene Panelinde Eklediğimiz Node'lar İçin Yazım Kuralları ve İsimlendirme Standartları

Godot'ta **Scene Paneli** üzerinde oluşturduğun **Node**'lar (düğümler), oyun dünyasındaki her türlü nesnenin temel yapı taşıdır. Node isimlendirme ve organizasyonu, sahnelerinin ve oyun sistemlerinin düzenli ve sürdürülebilir olmasını sağlar. Aşağıda Godot'taki Node'ları kullanırken dikkat etmen gereken yazım kuralları, isimlendirme konvansiyonları ve en iyi uygulamalar yer alıyor.

## Node İsimlendirme ve Yazım Kuralları

1. **Açıklayıcı ve Anlamlı İsimler Kullanın**:
   - Node isimleri, onların işlevlerini ve görevlerini açıkça ifade etmelidir. Genel ve belirsiz isimlerden kaçınarak, spesifik ve açıklayıcı isimler tercih edin.
	 - **Yanlış**: Node, Sprite, Enemy
	 - **Doğru**: PlayerSprite, EnemyAI, HealthBar, MainCamera

2. **PascalCase İsimlendirme Stili (UpperCamelCase)**:
   - Godot'ta Node isimleri için genellikle **PascalCase** (diğer adıyla UpperCamelCase) kullanılır. Yani her kelimenin ilk harfi büyük olur ve kelimeler birleşik yazılır.
	 - Örneğin: PlayerCharacter, EnemyAI, MainMenuButton
   - **Alt çizgi (snake_case)** genellikle dosya ve klasör isimlendirmesinde tercih edilirken, **PascalCase** node isimleri için yaygındır.

3. **Node Türünü Belirtmek İçin Sonek Kullan**:
   - Node'un türünü belirtebilmek için isimlerin sonuna açıklayıcı ekler koymak iyi bir pratiktir. Özellikle projelerde aynı mantıksal varlığa (örneğin oyuncu) birden fazla Node türü eklenebileceğinden, hangi Node'un ne işe yaradığını kolayca anlamak için bu ekler faydalı olur.
	 - Örneğin:
	   - PlayerSprite (Sprite türünde Node)
	   - EnemyAI (AI işlemleri için bir script veya Node)
	   - HealthBarProgress (ProgressBar Node)
	   - MainCamera (Camera3D/Camera2D Node)

4. **Hierarşi Organizasyonu**:
   - Node'ları sahne panelinde mantıklı bir şekilde organize etmek önemlidir. Oyun mekanikleri, UI elementleri ya da karakterler, **mantıksal bloklar** halinde gruplandırılmalı.
   - Örneğin:
	 ```
	 Player
	 ├── PlayerSprite          # Oyuncunun sprite'ı.
	 ├── PlayerCollisionShape  # Çarpışma kutusu.
	 └── PlayerCamera          # Oyuncuyu takip eden kamera.
	 ```

## Node İsimlendirme ve Organizasyon Önerileri:

### 1. **Karakterler ve Oyun Varlıkları (Entities)**:
   - **PlayerCharacter**, **EnemyBoss** gibi ana karakter ve düşmanlar için isimler. Çoğunlukla sahnenin kök node'larıdır ve altlarına, sprite'lar, collider'lar, animasyonlar gibi bileşenler eklenir.
   - Alt bileşenler için de açıklayıcı isimler kullan:
	 - PlayerCharacter
	   - PlayerSprite: Karakterin görsel temsili.
	   - PlayerCollisionShape: Çarpışma kutusu.
	   - PlayerAnimation: Animasyon kontrolcüsü.
	   - PlayerCamera: Oyuncuyu takip eden kamera.

### 2. **UI (Kullanıcı Arayüzü)**:
   - **MainMenu**, **HUD** (Head-Up Display) gibi ana arayüz elementleri.
   - Alt bileşenler için:
	 - HUD
	   - HealthBar: Can barı.
	   - AmmoCounter: Mermi sayacı.
	   - ScoreLabel: Puan göstergesi.

### 3. **Oyun Dünyası (Game World)**:
   - Çevre ve dünya ile ilgili düğümler için:
	 - GameWorld
	   - WorldMap: Ana dünya haritası.
	   - MainCamera: Oyun dünyasını görüntüleyen kamera.
	   - Lighting: Işık kaynağı.
	   - Terrain: Zemin (Terrain Node).

### 4. **UI Elementlerinde ve Control Node'larında**:
   - UI öğelerini isimlendirirken, öğenin ne olduğuna dair bir ipucu veren isimlendirmeler yapmalısın.
	 - **Button**, **Label**, **ProgressBar** gibi bileşenler, başına işlevlerini belirten bir kelime eklenerek isimlendirilmeli:
	   - StartButton: Başlatma butonu.
	   - PauseMenu: Oyun durdurma menüsü.
	   - LoadingProgressBar: Yükleme göstergesi.

### 5. **Şablon ve Prefab'lar (Scenes)**:
   - Prefab (önceden tanımlanmış sahne bileşenleri) veya şablon sahneler kullanıyorsan, isimlerinde **_Prefab** veya **_Instance** gibi bir sonek kullanarak onların prefabrik varlıklar olduğunu belirtmek mantıklı olabilir.
	 - Örneğin:
	   - Tree_Prefab: Ağaç modeli için prefab.
	   - Rock_Instance: Tekrar kullanılan bir kaya varlığı.

## En İyi Pratikler

1. **Düzgün ve Mantıklı Bir Hiyerarşi Kur**:
   - Godot, sahne ve node tabanlı bir sistem kullandığından, hiyerarşi yönetimi önemlidir. Karmaşık sahnelerde node'lar arasında kolayca gezinebilmek için mantıksal gruplamalar yapmalısın.
   - **Gruplar (Groups)**: Benzer işlevlere sahip node'ları Godot'un "Groups" sistemi ile gruplandırmak faydalı olabilir. Örneğin, tüm düşmanları bir "Enemy" grubuna ekleyebilirsin.

2. **Node Adlarını Sık Sık Gözden Geçir**:
   - Proje büyüdükçe node'ları yeniden adlandırma ihtiyacı doğabilir. Proje başlangıcında belirlediğin isimlendirme kurallarına sadık kalmak, bu süreci kolaylaştırır.

3. **Global ve Local Node'ları Ayırt Et**:
   - Eğer bir node, sahne genelinde başka node'lar tarafından kullanılacaksa (örneğin global bir ışık kaynağı), ismine `Global` ekleyebilirsin:
	 - GlobalLight, GlobalGameManager.

## Node Örnekleri ve Yapıları:


1. **Karakter Örneği:**:
	```
	PlayerCharacter
	├── PlayerSprite             # Oyuncu görseli
	├── PlayerCollisionShape     # Oyuncunun çarpışma alanı
	├── PlayerCamera             # Oyuncuyu takip eden kamera
	└── PlayerAnimation          # Oyuncunun animasyon kontrolü
	```
2. **HUD (Kullanıcı Arayüzü) Örneği:**:
	```
	HUD
	├── HealthBar                # Can barı
	├── AmmoCounter              # Mermi sayacı
	└── ScoreLabel               # Skor göstergesi
	```
3. **Oyun Dünyası Örneği:**:
	```
	GameWorld
	├── MainCamera               # Oyun dünyasını gösteren ana kamera
	├── Lighting                 # Global ışıklandırma
	└── Terrain                  # Zemin
	```

## Sonuç:
- **Açıklayıcı ve anlaşılır isimler kullan**. Node'un ne iş yaptığını anlamak için tek bir bakış yeterli olmalı.
- **PascalCase** (UpperCamelCase) node isimlendirmesi kullan.
- Node türünü belirlemek için açıklayıcı **son ekler** (Camera, Sprite, AI vb.) kullan.
- Mantıklı bir **hiyerarşi** oluştur ve her bir node'u görevine göre organize et.
- Gelişen projede **tutarlı** bir isimlendirme standardı sağlamak, uzun vadede yönetilebilirliği artırır.

Bu kurallar, Godot projelerinde sahneleri ve node'ları daha anlaşılır, sürdürülebilir ve işbirliğine uygun hale getirir.
