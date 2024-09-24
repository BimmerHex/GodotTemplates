# Godot Projelerinde Dosya ve Klasör İsimlendirme Kuralları

Godot projelerinde düzenli ve uyumlu bir dosya sistemi oluşturmak için aşağıdaki isimlendirme kuralları uygulanabilir. Bu kurallar, özellikle büyük projelerde düzeni sağlamaya ve platformlar arası uyumluluğu artırmaya yardımcı olur.

### 1. Küçük Harf Kullanımı
Dosya ve klasör isimlerini her zaman küçük harflerle yazın. Bu, özellikle Linux gibi büyük/küçük harf duyarlı dosya sistemleriyle çalışırken uyumluluk sağlar.

- **Örnek:** `player_model.glb`, `main_menu.tscn`

### 2. Snake_case Kullanımı
İsimlendirmede boşluk veya büyük harf kullanmak yerine alt çizgi (`_`) kullanın. Bu, daha tutarlı ve okunabilir bir yapıyı teşvik eder.

- **Örnek:** `player_controller.gd`, `enemy_ai.tscn`

### 3. Anlamlı ve Açıklayıcı İsimler
Her dosya ve klasör, içeriği veya işleviyle ilgili anlamlı ve açıklayıcı bir isim taşımalıdır. Bu, dosyaların ne için kullanıldığını anlamayı kolaylaştırır.

- **Örnek:** `background_music.ogg`, `enemy_animation.tres`

### 4. Dosya Türlerini Belirtin
İsimlendirmede dosya türlerini belirten kısaltmalar veya uzantılar kullanmak, hangi dosyanın ne tür bir kaynak olduğunu hızlıca anlamayı sağlar.

- **Örnek:** `player_animation.gd`, `level_01.tscn`, `button_style.tres`

---

# 3D Oyun Projesi İçin Örnek Klasör Yapısı

Godot projelerinde düzenli bir yapı, dosyaların kolayca bulunmasını ve projeyi büyütürken düzenin korunmasını sağlar. Aşağıda, bir 3D oyun projesi için önerilen klasör yapısını bulabilirsiniz:

```
res://
│
├── assets/                       # Oyun varlıklarının saklandığı ana klasör.
│   ├── models/                   # 3D modeller için klasör.
│   │   ├── player_model.glb
│   │   ├── enemy_model.glb
│   │   └── environment/          # Çevre modelleri.
│   │       ├── tree.glb
│   │       └── rock.glb
│   ├── textures/                 # Texture dosyaları (materyaller için).
│   │   ├── player_diffuse.png
│   │   ├── enemy_normal.png
│   │   └── environment/          # Çevre texture'ları.
│   │       ├── ground_diffuse.png
│   │       └── skybox_texture.png
│   ├── audio/                    # Ses dosyaları (ses efektleri ve müzikler).
│   │   ├── effects/              # Ses efektleri.
│   │   │   ├── jump.wav
│   │   │   └── explosion.wav
│   │   └── music/                # Oyun müzikleri.
│   │       ├── background_music.ogg
│   │       └── boss_battle.ogg
│   ├── fonts/                    # Yazı tipleri.
│   │   └── sci-fi_font.tres
│   └── animations/               # Animasyon dosyaları.
│       ├── player_run.tres
│       └── enemy_attack.tres
│
├── scenes/                       # Sahne dosyalarının saklandığı ana klasör.
│   ├── levels/                   # Oyun seviyeleri.
│   │   ├── level1_scene.tscn
│   │   ├── level2_scene.tscn
│   │   └── boss_level_scene.tscn
│   ├── ui/                       # Kullanıcı arayüzü sahneleri.
│   │   ├── main_menu_scene.tscn
│   │   ├── pause_menu_scene.tscn
│   │   └── hud_scene.tscn        # Oyun içi HUD (Health, Ammo vb.).
│   └── world/                    # Ana dünya haritası ve genel sahneler.
│       ├── world_map_scene.tscn
│       └── overworld_scene.tscn
│
├── scripts/                      # GDScript dosyalarının saklandığı klasör.
│   ├── player/                   # Oyuncuya ait script dosyaları.
│   │   ├── player_controller.gd
│   │   ├── player_animation.gd
│   │   └── player_inventory.gd
│   ├── enemy/                    # Düşman yapay zekası ve animasyon script'leri.
│   │   ├── enemy_ai.gd
│   │   ├── boss_ai.gd
│   │   └── enemy_animation.gd
│   ├── managers/                 # Oyun yöneticisi script'leri (game state, scene yönetimi).
│   │   ├── game_manager.gd
│   │   └── level_manager.gd
│   ├── ui/                       # Kullanıcı arayüzü yönetim script'leri.
│   │   ├── main_menu.gd
│   │   ├── hud_manager.gd
│   │   └── pause_menu.gd
│   ├── physics/                  # Fizik yönetimi ve çarpışma yönetimi.
│   │   └── physics_manager.gd
│   └── items/                    # Oyun içi eşyalar için script'ler.
│       ├── weapon.gd
│       └── health_pack.gd
│
├── shaders/                      # Shader dosyalarının saklandığı klasör.
│   ├── water_shader.shader       # Su efektleri için shader.
│   ├── sky_shader.shader         # Gökyüzü shader.
│   └── toon_shader.shader        # Toon shading efektleri.
│
├── configs/                      # Oyun ayarları ve konfigürasyon dosyaları.
│   ├── game_settings.cfg         # Oyun genel ayarları.
│   └── key_bindings.cfg          # Tuş atamaları.
│
├── addons/                       # Godot eklentileri ve üçüncü parti kütüphaneler.
│   └── custom_plugin/            # Özel bir Godot eklentisi veya ayarları.
│
├── docs/                         # Proje dökümantasyonları.
│   ├── readme.md                 # Projenin genel açıklaması.
│   └── design_document.md        # Oyun tasarım dokümanı.
│
└── resources/                    # Harici veri ve kaynaklar.
    ├── localization/             # Dil dosyaları ve çeviriler.
    │   ├── en/                   # İngilizce dil dosyaları.
    │   │   └── strings.csv
    │   └── es/                   # İspanyolca dil dosyaları.
    │       └── strings.csv
    └── prefabs/                  # Önceden tanımlanmış sahne ve nesneler.
        ├── tree_prefab.tscn
        └── rock_prefab.tscn
