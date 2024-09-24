# Godot Input Map Action İsimlendirme Standartları

Godot'ta **Project Settings > Input Map** alanında yeni bir **action** oluştururken, resmi olarak bir yazım standardı bulunmamakla birlikte, projenizi düzenli ve okunabilir tutmak için aşağıdaki önerilen isimlendirme standartları uygulanabilir. Bu kurallar, projedeki tutarlılığı sağlamak ve daha iyi bir yapı oluşturmak için yaygın olarak kullanılır.

## 1. Snake_case Kullanımı
Godot'ta genellikle **snake_case** (alt çizgi ile ayırma) yöntemi kullanılır. Bu, büyük/küçük harf karışıklığını önler ve özellikle platformlar arası uyumluluk açısından avantajlıdır.

- **Örnek:** `move_forward`, `jump_action`, `attack_primary`

## 2. Küçük Harf Kullanımı
Tüm action isimlerinin küçük harfle yazılması önerilir. Bu, projede ve kodda tutarlılığı artırır ve daha okunabilir hale getirir.

- **Örnek:** `interact`, `open_inventory`

## 3. Anlamlı ve Açıklayıcı İsimler
Oluşturduğunuz **action** isimleri, aksiyonun amacını ve işlevini açıkça ifade etmelidir. Zıplama aksiyonu için `jump` ya da `player_jump` gibi açıklayıcı bir isim kullanılabilir.

- **Örnek:** `player_jump`, `player_crouch`

## 4. Spesifik İşlev Tanımlaması
Eğer aksiyon belirli bir nesneye veya amaca yönelikse, hangi nesneye bağlı olduğunu belirten bir isimlendirme tercih edin. Örneğin, oyuncu karakteri ve araç kontrolü için farklı aksiyon isimleri kullanılabilir.

- **Örnek:** `player_shoot`, `vehicle_boost`

## 5. Aksiyon Türünü Belirtmek
Bazen bir aksiyonun türünü belirlemek faydalı olabilir. Eğer aksiyon basılı tutulma, serbest bırakma gibi durumlar içeriyorsa, `press`, `hold`, veya `release` gibi açıklayıcı terimler eklemek daha anlaşılır hale getirir.

- **Örnek:** `attack_primary_press`, `attack_primary_hold`, `attack_primary_release`

## 6. Kapsam ve Bağlam Düşüncesi
Eğer proje büyükse ve farklı kontrol düzenleri (örneğin, UI ve oyun içi karakter kontrolü gibi) varsa, aksiyon isimlerinde bağlamı belirtmek önemlidir. Bu, farklı kontrol şemalarında aynı isimlerin karışmasını önler.

- **Örnek:** `ui_select`, `ui_back`, `game_pause`

---

# Örnek İsimlendirme Şeması

Projedeki çeşitli aksiyonlar için önerilen isimlendirme şeması:

### Hareket Aksiyonları
- `move_forward`
- `move_backward`
- `move_left`
- `move_right`

### Etkileşim Aksiyonları
- `interact`
- `pick_item`
- `open_door`

### Saldırı Aksiyonları
- `attack_primary`
- `attack_secondary`

### Kullanıcı Arayüzü Aksiyonları
- `ui_select`
- `ui_back`
- `ui_pause`

### Kamera Aksiyonları
- `camera_zoom_in`
- `camera_zoom_out`

### Araç Kontrolü
- `vehicle_accelerate`
- `vehicle_brake`

---

# Genel Öneriler

- **Kısa ve Net**: Action isimleri mümkün olduğunca kısa olmalı, ancak işlevi açıkça ifade etmelidir.
- **Tutarlılık**: Proje boyunca aynı isimlendirme şemasını kullanmak önemlidir. Tüm input action'lar benzer bir formatta olmalıdır.
  
Bu standartlar, projenizin okunabilirliğini artırır ve proje büyüdükçe düzeni korumanıza yardımcı olur. Aynı zamanda, projede çalışan diğer geliştiriciler için de anlaşılabilir bir yapı oluşturur.
