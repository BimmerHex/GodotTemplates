# Godot'ta FileSystem Panelinde Eklediğimiz Dosyalar ve Klasörler İçin Yazım Kuralları ve İsimlendirme Standartları
- Godot projelerinde dosya ve klasör isimlendirmesi için önerilen bir kural vardır ve bu kurallar, düzenli bir yapı oluşturmanın yanı sıra platformlar arası uyumluluğu artırır.

## Godot Projelerinde Dosya ve Klasör İsimlendirme Kuralları:
- Küçük harf kullanımı: Tüm dosya ve klasör isimlerini küçük harflerle yazın. Bu, dosya sistemleri arasında uyumluluğu artırır (örneğin, Linux büyük/küçük harf duyarlıdır).
  - Örnek: player_model, main_menu.tscn

- Snake_case kullanımı: Boşluk ve büyük harflerden kaçınarak alt çizgi (_) kullanın.
  - Örnek: player_controller.gd, enemy_ai.tscn

- Anlamlı ve açıklayıcı isimler: Her dosya ve klasör, içerdiği dosyaların anlamını ve işlevini açıkça ifade etmelidir.
  - Örnek: background_music.ogg, enemy_animation.tres

- Dosya türlerini belirtin: İsimlendirmede dosya türlerini açıkça belirten kısaltmalar kullanmak dosya yönetimini kolaylaştırır.
  - Örnek: player_animation.gd, level_01.tscn, button_style.tres

## 3D Oyun Projesi İçin Klasör Yapısı
```
  res://
  │
  ├── assets/                   # Oyun varlıklarının saklandığı ana klasör.
  │   ├── models/               # 3D modeller için klasör.
  │   │   ├── player_model.glb
  │   │   ├── enemy_model.glb
  │   │   └── environment/      # Çevre modelleri.
  │   │       ├── tree.glb
  │   │       └── rock.glb
  │   ├── textures/             # Texture dosyaları (materyaller için).
  │   │   ├── player_diffuse.png
  │   │   ├── enemy_normal.png
  │   │   └── environment/
  │   │       ├── ground_diffuse.png
  │   │       └── skybox_texture.png
  │   ├── sounds/               # Ses dosyaları.
  │   │   ├── effects/          # Ses efektleri.
  │   │   │   ├── jump.wav
  │   │   │   └── explosion.wav
  │   │   └── music/            # Oyun müzikleri.
  │   │       ├── background_music.ogg
  │   │       └── boss_battle.ogg
  │   ├── fonts/                # Yazı tipleri.
  │   │   └── sci-fi_font.tres
  │   └── animations/           # Animasyon dosyaları.
  │       ├── player_run.tres
  │       └── enemy_attack.tres
  │
  ├── scenes/                   # Sahne dosyalarının saklandığı ana klasör.
  │   ├── levels/               # Oyun seviyeleri için alt klasör.
  │   │   ├── level1_scene.tscn
  │   │   ├── level2_scene.tscn
  │   │   └── boss_level_scene.tscn
  │   ├── ui/                   # Kullanıcı arayüzü sahneleri.
  │   │   ├── main_menu_scene.tscn
  │   │   ├── pause_menu_scene.tscn
  │   │   └── hud_scene.tscn    # Oyun içi HUD (Health, Ammo vb.).
  │   └── world/                # Ana dünya haritası ve genel sahneler.
  │       ├── world_map_scene.tscn
  │       └── overworld_scene.tscn
  │
  ├── scripts/                  # Tüm GDScript dosyalarının saklandığı klasör.
  │   ├── player/               # Oyuncu ile ilgili script'ler.
  │   │   ├── player_controller.gd
  │   │   ├── player_animation.gd
  │   │   └── player_inventory.gd
  │   ├── enemy/                # Düşman AI'sı ve ilgili script'ler.
  │   │   ├── enemy_ai.gd
  │   │   ├── boss_ai.gd
  │   │   └── enemy_animation.gd
  │   ├── managers/             # Oyun yöneticisi script'leri (game state, scene yönetimi).
  │   │   ├── game_manager.gd
  │   │   └── level_manager.gd
  │   ├── ui/                   # Kullanıcı arayüzü script'leri.
  │   │   ├── main_menu.gd
  │   │   ├── hud_manager.gd
  │   │   └── pause_menu.gd
  │   ├── physics/              # Fizik ve çarpışma yönetimi ile ilgili script'ler.
  │   │   └── physics_manager.gd
  │   └── items/                # Oyun içi eşyalar için script'ler.
  │       ├── weapon.gd
  │       └── health_pack.gd
  │
  ├── shaders/                  # Shader dosyalarının saklandığı klasör.
  │   ├── water_shader.shader   # Su efektleri için shader.
  │   ├── sky_shader.shader     # Gökyüzü shader.
  │   └── toon_shader.shader    # Toon shading efektleri.
  │
  ├── configs/                  # Oyun ayarları ve verilerini içeren konfigürasyon dosyaları.
  │   ├── game_settings.cfg     # Oyun genel ayarları.
  │   └── key_bindings.cfg      # Tuş atamaları.
  │
  ├── addons/                   # Godot eklentileri ve üçüncü parti kütüphaneler.
  │   └── custom_plugin/        # Özel bir Godot eklentisi veya eklenti ayarları.
  │
  ├── docs/                     # Proje ile ilgili dökümantasyon.
  │   ├── readme.md             # Projenin genel açıklaması.
  │   └── design_document.md    # Oyun tasarım dokümanı.
  │
  └── resources/                # Proje ile ilgili çeşitli veri ve harici kaynaklar.
  	├── localization/         # Dil dosyaları ve çeviriler.
  	│   ├── en/               # İngilizce dil dosyaları.
  	│   │   └── strings.csv
  	│   └── es/               # İspanyolca dil dosyaları.
  	│       └── strings.csv
  	└── prefabs/              # Önceden tanımlanmış sahne ve nesneler (Prefab'lar).
  		├── tree_prefab.tscn
  		└── rock_prefab.tscn
```
