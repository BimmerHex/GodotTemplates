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
```

## Detaylı 2D Proje Klasör ve Dosya Yapısı (Farklı Yapı)
```
project_name/
├── assets/
│   ├── animations/
│   │   ├── characters/
│   │   │   ├── player/
│   │   │   │   ├── run.anim
│   │   │   │   ├── jump.anim
│   │   │   │   └── attack.anim
│   │   │   └── npcs/
│   │   │       ├── npc_1.anim
│   │   │       └── npc_2.anim
│   │   ├── enemies/
│   │   │   ├── enemy_type_1/
│   │   │   │   ├── walk.anim
│   │   │   │   └── attack.anim
│   │   │   └── boss_enemy/
│   │   │       ├── idle.anim
│   │   │       └── special_attack.anim
│   │   ├── objects/
│   │   │   ├── collectibles/
│   │   │   │   ├── coin_spin.anim
│   │   │   │   └── gem_glow.anim
│   │   │   └── traps/
│   │   │       ├── spike_extend.anim
│   │   │       └── saw_rotate.anim
│   │   └── environment/
│   │       ├── water_flow.anim
│   │       └── foliage_sway.anim
│   ├── audio/
│   │   ├── music/
│   │   │   ├── main_theme.ogg
│   │   │   └── boss_theme.ogg
│   │   └── sound_effects/
│   │       ├── ui/
│   │       │   ├── button_click.wav
│   │       │   └── menu_open.wav
│   │       ├── player/
│   │       │   ├── jump.wav
│   │       │   ├── attack.wav
│   │       │   └── damage.wav
│   │       ├── enemies/
│   │       │   ├── enemy_hit.wav
│   │       │   └── enemy_death.wav
│   │       └── environment/
│   │           ├── rain.wav
│   │           └── wind.wav
│   ├── fonts/
│   │   ├── main_font.tres
│   │   └── title_font.tres
│   ├── shaders/
│   │   ├── water_shader.shader
│   │   └── glow_effect.shader
│   ├── sprites/
│   │   ├── characters/
│   │   │   ├── player/
│   │   │   │   ├── idle.png
│   │   │   │   ├── run.png
│   │   │   │   └── jump.png
│   │   │   └── npcs/
│   │   │       ├── npc_1.png
│   │   │       └── npc_2.png
│   │   ├── enemies/
│   │   │   ├── enemy_type_1.png
│   │   │   └── boss_enemy.png
│   │   ├── objects/
│   │   │   ├── collectibles/
│   │   │   │   ├── coin.png
│   │   │   │   └── gem.png
│   │   │   └── traps/
│   │   │       ├── spike.png
│   │   │       └── saw.png
│   │   └── environment/
│   │       ├── tilesets/
│   │       │   ├── grass_tileset.png
│   │       │   └── cave_tileset.png
│   │       └── backgrounds/
│   │           ├── forest_bg.png
│   │           └── cave_bg.png
│   └── textures/
│       ├── ui/
│       │   ├── button_normal.png
│       │   ├── button_hover.png
│       │   └── button_pressed.png
│       └── effects/
│           ├── particle.png
│           └── smoke.png
├── docs/
│   ├── design_document.md
│   ├── technical_documentation.md
│   └── art_assets_guidelines.md
├── addons/
│   ├── plugin_1/
│   └── plugin_2/
├── prefabs/
│   ├── characters/
│   │   ├── player.prefab
│   │   └── npc.prefab
│   ├── enemies/
│   │   ├── enemy_type_1.prefab
│   │   └── boss_enemy.prefab
│   └── objects/
│       ├── coin.prefab
│       └── spike_trap.prefab
├── resources/
│   ├── data/
│   │   ├── levels_data.json
│   │   └── items_data.json
│   └── scripts/
│       ├── gdnative/
│       └── plugins/
├── scenes/
│   ├── main/
│   │   └── main_scene.tscn
│   ├── levels/
│   │   ├── level_1.tscn
│   │   ├── level_2.tscn
│   │   └── boss_level.tscn
│   ├── ui/
│   │   ├── menus/
│   │   │   ├── main_menu.tscn
│   │   │   ├── pause_menu.tscn
│   │   │   └── settings_menu.tscn
│   │   └── hud/
│   │       ├── health_bar.tscn
│   │       └── score_display.tscn
│   ├── characters/
│   │   ├── player.tscn
│   │   └── npcs/
│   │       ├── npc_1.tscn
│   │       └── npc_2.tscn
│   ├── enemies/
│   │   ├── enemy_type_1.tscn
│   │   └── boss_enemy.tscn
│   └── objects/
│       ├── collectibles/
│       │   ├── coin.tscn
│       │   └── gem.tscn
│       └── traps/
│           ├── spike_trap.tscn
│           └── saw_trap.tscn
├── scripts/
│   ├── characters/
│   │   ├── player.gd
│   │   └── npcs/
│   │       ├── npc_1.gd
│   │       └── npc_2.gd
│   ├── enemies/
│   │   ├── enemy_type_1.gd
│   │   └── boss_enemy.gd
│   ├── objects/
│   │   ├── collectibles/
│   │   │   ├── coin.gd
│   │   │   └── gem.gd
│   │   └── traps/
│   │       ├── spike_trap.gd
│   │       └── saw_trap.gd
│   ├── ui/
│   │   ├── menus/
│   │   │   ├── main_menu.gd
│   │   │   ├── pause_menu.gd
│   │   │   └── settings_menu.gd
│   │   └── hud/
│   │       ├── health_bar.gd
│   │       └── score_display.gd
│   ├── managers/
│   │   ├── game_manager.gd
│   │   ├── level_manager.gd
│   │   ├── audio_manager.gd
│   │   └── ui_manager.gd
│   ├── utilities/
│   │   ├── input_manager.gd
│   │   ├── math_utils.gd
│   │   └── extensions.gd
│   └── globals.gd
├── settings/
│   ├── project_settings.cfg
│   ├── input_mappings.cfg
│   └── graphics_settings.cfg
└── README.md
```

## Açıklamalar

# 1. Ana Klasörler

| Klasör/Dosya        | Açıklama                                                                           |
|---------------------|------------------------------------------------------------------------------------|
| **project_name/**   | Projenizin ana klasörü. Tüm proje dosyaları ve klasörleri burada yer alır.         |
| **README.md**       | Proje hakkında genel bilgilerin yer aldığı dosya.                                  |

# 2. Assets

| Klasör/Dosya                          | Açıklama                                                                                         |
|---------------------------------------|--------------------------------------------------------------------------------------------------|
| **assets/**                           | Proje varlıklarının saklandığı ana klasör.                                                       |
| **assets/animations/**                | Animasyon dosyalarının saklandığı klasör.                                                        |
| **assets/animations/characters/**     | Karakter animasyonları.                                                                          |
| **assets/animations/characters/player/** | Ana karakterin animasyonları (koşma, zıplama, saldırı).                                      |
| **assets/animations/characters/npcs/**  | NPC animasyonları.                                                                             |
| **assets/animations/enemies/**        | Düşman animasyonları.                                                                            |
| **assets/animations/objects/**        | Nesne animasyonları (toplanabilir eşyalar, tuzaklar).                                            |
| **assets/animations/environment/**    | Çevresel animasyonlar (su akışı, yaprak sallanması).                                             |
| **assets/audio/**                     | Ses dosyalarının bulunduğu klasör.                                                               |
| **assets/audio/music/**               | Oyun müzikleri (ana tema, boss teması).                                                          |
| **assets/audio/sound_effects/**       | Ses efektleri (arayüz, oyuncu, düşmanlar, çevre).                                                |
| **assets/fonts/**                     | Yazı tipleri (ana yazı tipi, başlık yazı tipi).                                                  |
| **assets/shaders/**                   | Shader dosyaları (özel efektler için).                                                           |
| **assets/sprites/**                   | 2D grafik dosyaları.                                                                             |
| **assets/sprites/characters/**        | Karakter sprite'ları (oyuncu, NPC'ler).                                                          |
| **assets/sprites/enemies/**           | Düşman sprite'ları.                                                                              |
| **assets/sprites/objects/**           | Nesne sprite'ları (toplanabilir eşyalar, tuzaklar).                                              |
| **assets/sprites/environment/**       | Çevre grafikleri (tile setler, arka planlar).                                                    |
| **assets/textures/**                  | Doku dosyaları (UI ve özel efektler için).                                                       |

# 3. Docs

| Klasör/Dosya                  | Açıklama                                   |
|-------------------------------|--------------------------------------------|
| **docs/**                     | Proje dokümantasyonunun bulunduğu klasör.  |
| **design_document.md**        | Oyun tasarım dokümanı.                     |
| **technical_documentation.md**| Teknik dokümantasyon.                      |
| **art_assets_guidelines.md**  | Sanat varlıkları için rehber.              |

# 4. Addons

| Klasör/Dosya     | Açıklama                                          |
|------------------|---------------------------------------------------|
| **addons/**      | Projede kullanılan eklentiler ve üçüncü parti araçlar. |
| **plugin_1/**    | Birinci eklenti klasörü.                          |
| **plugin_2/**    | İkinci eklenti klasörü.                           |

# 5. Prefabs

| Klasör/Dosya              | Açıklama                                               |
|---------------------------|--------------------------------------------------------|
| **prefabs/**              | Yeniden kullanılabilir nesnelerin ön tanımlı hallerini içerir. |
| **prefabs/characters/**   | Karakter prefab'ları (oyuncu, NPC).                    |
| **prefabs/enemies/**      | Düşman prefab'ları (farklı düşman türleri).            |
| **prefabs/objects/**      | Nesne prefab'ları (toplanabilir eşyalar, tuzaklar).    |

# 6. Resources

| Klasör/Dosya                     | Açıklama                                              |
|----------------------------------|-------------------------------------------------------|
| **resources/**                   | Diğer kaynak dosyalarının saklandığı klasör.          |
| **resources/data/**              | Veri dosyaları (JSON, CSV).                           |
| **levels_data.json**             | Seviye verilerini içerir.                             |
| **items_data.json**              | Eşya verilerini içerir.                               |
| **resources/scripts/**           | Özel scriptler ve GDNative dosyaları.                 |
| **resources/scripts/gdnative/**  | GDNative ile yazılmış scriptler.                      |
| **resources/scripts/plugins/**   | Script eklentileri.                                   |

# 7. Scenes

| Klasör/Dosya                                | Açıklama                                                    |
|---------------------------------------------|-------------------------------------------------------------|
| **scenes/**                                 | Sahne dosyalarının bulunduğu klasör.                        |
| **scenes/main/**                            | Oyunun ana sahnesi.                                         |
| **main_scene.tscn**                         | Ana sahne dosyası.                                          |
| **scenes/levels/**                          | Oyun seviyeleri.                                            |
| **level_1.tscn**, **level_2.tscn**, **boss_level.tscn** | Farklı oyun seviyeleri.                        |
| **scenes/ui/**                              | Kullanıcı arayüzü sahneleri.                                |
| **scenes/ui/menus/**                        | Menü sahneleri (ana menü, duraklatma menüsü, ayarlar menüsü).|
| **scenes/ui/hud/**                          | Oyun içi arayüz sahneleri (can barı, skor göstergesi).      |
| **scenes/characters/**                      | Karakter sahneleri (oyuncu, NPC'ler).                       |
| **scenes/enemies/**                         | Düşman sahneleri.                                           |
| **scenes/objects/**                         | Nesne sahneleri (toplanabilir eşyalar, tuzaklar).           |

# 8. Scripts

| Klasör/Dosya                          | Açıklama                                                     |
|---------------------------------------|--------------------------------------------------------------|
| **scripts/**                          | Kod dosyalarının saklandığı klasör.                          |
| **scripts/characters/**               | Karakter scriptleri (oyuncu, NPC'ler).                       |
| **scripts/enemies/**                  | Düşman scriptleri.                                           |
| **scripts/objects/**                  | Nesne scriptleri (toplanabilir eşyalar, tuzaklar).           |
| **scripts/ui/**                       | Arayüz scriptleri.                                           |
| **scripts/ui/menus/**                 | Menü scriptleri (ana menü, duraklatma menüsü, ayarlar menüsü).|
| **scripts/ui/hud/**                   | HUD bileşenlerinin scriptleri (can barı, skor göstergesi).   |
| **scripts/managers/**                 | Oyun yöneticileri ve singletonlar.                           |
| **game_manager.gd**                   | Oyun genel yönetimi.                                         |
| **level_manager.gd**                  | Seviye geçişleri ve yönetimi.                                |
| **audio_manager.gd**                  | Seslerin kontrolü.                                           |
| **ui_manager.gd**                     | Arayüz yönetimi.                                             |
| **scripts/utilities/**                | Yardımcı fonksiyonlar ve araçlar.                            |
| **input_manager.gd**                  | Giriş ve kontrol şemalarının yönetimi.                       |
| **math_utils.gd**                     | Matematiksel yardımcı fonksiyonlar.                          |
| **extensions.gd**                     | Godot'un varsayılan fonksiyonlarını genişleten scriptler.    |
| **globals.gd**                        | Global değişkenler ve fonksiyonlar.                          |

# 9. Settings

| Klasör/Dosya               | Açıklama                                   |
|----------------------------|--------------------------------------------|
| **settings/**              | Oyun ayarları ve konfigürasyon dosyaları.  |
| **project_settings.cfg**   | Proje ayarları.                            |
| **input_mappings.cfg**     | Tuş atamaları ve kontrol şemaları.         |
| **graphics_settings.cfg**  | Grafik ayarları.                           |
