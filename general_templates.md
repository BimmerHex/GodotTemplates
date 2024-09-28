# Godot Engine Adlandırma Kuralları

| Tür                   | İsimlendirme Stili       | Örnek                               |
|-----------------------|--------------------------|-------------------------------------|
| **Klasör Adı**        | Küçük harf, `snake_case` | `assets/`, `scripts/`, `levels/`    |
| **Script Dosya Adı**  | Küçük harf, `snake_case` | `player_controller.gd`, `enemy_ai.gd` |
| **Node Adı**          | `PascalCase`             | `Player`, `MainCamera`, `EnemySpawner` |
| **Sahne Dosya Adı**   | Küçük harf, `snake_case` | `level1.tscn`, `main_menu.tscn`     |
| **Değişken Adı**      | Küçük harf, `snake_case` | `player_speed`, `enemy_health`      |
| **Sabit Değer**       | Büyük harf, `SNAKE_CASE` | `MAX_HEALTH`, `DEFAULT_GRAVITY`     |
| **Fonksiyon Adı**     | Küçük harf, `snake_case` | `move_player()`, `spawn_enemy()`    |
| **Sinyal Tanımları**  | Küçük harf, `snake_case` | `signal player_died`, `signal enemy_spawned` |
| **Node Grupları**     | Küçük harf, `snake_case` | `enemies`, `interactive_objects`    |

## Genel Yararlar:

- **Platform Uyumluluğu**: Küçük harf ve `snake_case` kullanımı, farklı işletim sistemlerinde uyumluluğu artırır ve büyük-küçük harf duyarlılığı olan dosya sistemlerinde olası sorunları önler.
- **Okunabilirlik**: `PascalCase` kullanımı, node'ların daha rahat okunmasını sağlarken, `snake_case` dosya ve değişkenlerde daha iyi bir tutarlılık sunar.
- **Modülerlik ve Yönetim Kolaylığı**: Klasör ve dosya isimlendirme standardı, büyük ve karmaşık projelerde bileşenlerin hızlı bulunmasını ve yönetilmesini kolaylaştırır.
- **Tutarlılık**: Tüm proje boyunca tutarlı bir adlandırma stili kullanmak, kodun bakımını kolaylaştırır ve ekip çalışmasında daha az hata yapılmasını sağlar.

# Godot'ta `_` ile Başlayan Fonksiyonların Anlamı ve Kullanımı

## Yerleşik Callback Fonksiyonları

| Fonksiyon        | Açıklama                                                        |
|------------------|-----------------------------------------------------------------|
| `_ready()`       | Node'un sahneye eklendiğinde veya hazır olduğunda çağrılır.     |
| `_process(delta)`| Her karede (frame) çağrılır. Genellikle animasyon ve hareket yönetimi için kullanılır. |
| `_physics_process(delta)` | Fizik simülasyonu için her karede çağrılır. Fizik hesaplamaları burada yapılır. |
| `_input(event)`  | Giriş olaylarını yakalar (mouse, klavye vb.).                   |
| `_enter_tree()`  | Node sahneye girdiğinde çağrılır. Diğer node'larla etkileşim başlatmak için kullanılır. |
| `_exit_tree()`   | Node sahneden çıktığında çağrılır. Bellek temizliği veya işlemi durdurmak için kullanılır. |

### `_` ile Başlayan Fonksiyonların Kullanım Amacı

- **Yerleşik Fonksiyonlar**: `_` ile başlayan fonksiyonlar genellikle Godot'un yaşam döngüsündeki belirli olaylara tepki vermek üzere kullanılır. Bu fonksiyonlar motor tarafından otomatik olarak çağrılır.
  
- **Dahili (Private) Fonksiyonlar**: `_` ile başlayan bazı fonksiyonlar, script içinde sadece dahili olarak kullanılması gereken işlevleri belirtmek amacıyla da kullanılır. Bu, diğer dillerdeki "private" işlevlere benzer şekilde, fonksiyonun yalnızca o script içinde kullanılacağını ifade eder.

### Genel Yararlar:

- **Yaşam Döngüsü Yönetimi**: `_ready()`, `_process()`, `_input()` gibi callback'ler, Godot'un yaşam döngüsü sırasında belirli noktalarda devreye girerek scriptlerin belirli işlevleri gerçekleştirmesini sağlar.
- **Enkapsülasyon**: `_` kullanımı, bazı fonksiyonların dışarıdan erişilmesini engelleyerek kapsülleme (encapsulation) sağlar. Bu sayede kod düzeni ve güvenliği artar.
- **Tutarlılık ve Okunabilirlik**: `_` ile başlayan fonksiyonların özel olduğunu bilmek, kodun okunabilirliğini artırır ve hangi fonksiyonların dışarıya sunulduğunu belirlemeyi kolaylaştırır.

# Godot'ta Sıklıkla Kullanılan GDScript Özellikleri

| Özellik             | Açıklama                                                   | Örnek Kullanım                     |
|---------------------|------------------------------------------------------------|------------------------------------|
| **extends**         | Bu script'in hangi sınıftan miras alacağını belirtir.      | `extends KinematicBody2D`          |
| **func**            | Fonksiyon tanımlar.                                        | `func _ready():`                   |
| **export**          | Bir değişkeni inspector'da düzenlenebilir hale getirir.    | `export var speed = 200`           |
| **onready**         | Node'a sahnede hazır olduğunda erişir.                     | `onready var player = $Player`     |
| **signal**          | Özel bir olay tanımlamak için kullanılır.                  | `signal player_died`               |
| **yield**           | Belirli bir işlevi duraklatıp daha sonra devam eder.       | `yield(get_tree().create_timer(1), "timeout")` |
| **preload**         | Bir kaynağı script'in başında yükler (performans avantajı).| `var bullet_scene = preload("res://bullet.tscn")` |

## GDScript Kullanım Örnekleri:
- **extends**: Belirli bir sınıftan miras alarak onun özelliklerini kullanmanızı sağlar.
- **export**: Değişkenlerin inspector'da ayarlanabilir olmasını sağlayarak, sahne düzenlemesi sırasında hız kazandırır.

# Godot'taki Temel Node'lar ve Kullanımları

| Node Türü              | Açıklama                                                        | Yaygın Kullanım Alanları         |
|------------------------|-----------------------------------------------------------------|---------------------------------|
| **Node2D**             | 2D oyun geliştirmede temel node.                                | 2D oyunlarda her türlü öğe.     |
| **KinematicBody2D**    | Kendi hareket ve çarpışma kontrolünü sağlar.                    | Oyuncu, düşman hareketi.        |
| **RigidBody2D**        | Fizik motoru tarafından kontrol edilen nesneler.                | Fizik tabanlı hareket.          |
| **Sprite**             | 2D görselleri göstermek için kullanılır.                        | Karakter ve arka plan görselleri.|
| **Control**            | Kullanıcı arayüzü (UI) oluşturmak için kullanılır.              | Düğmeler, paneller, HUD.        |
| **Camera2D**           | 2D sahneleri izlemek için kullanılır.                           | Oyuncuyu takip eden kamera.     |
| **Spatial**            | 3D oyun geliştirmede temel node.                                | 3D sahnelerde her türlü öğe.    |
| **MeshInstance**       | 3D model göstermek için kullanılır.                             | 3D karakter ve çevre modelleri. |
| **Area2D**             | 2D alan çarpışma algılama için kullanılır.                      | Tetikleyiciler, toplama alanları.|

## Node Seçimi Rehberi:
- **KinematicBody2D**: Eğer hareket üzerinde tam kontrol istiyorsanız, oyuncu veya düşman karakterleri için kullanın.
- **RigidBody2D**: Fizik motoru tarafından kontrol edilen nesneler için idealdir; yerçekimi, kuvvet ve momentum gibi özellikler kullanılır.

# Signal Kullanımı ve Kullanım Durumları

| Signal Kullanımı     | Açıklama                                                     | Örnek                            |
|----------------------|--------------------------------------------------------------|----------------------------------|
| **signal tanımlama** | Kendi özel olayınızı tanımlamanızı sağlar.                   | `signal player_died`             |
| **signal yayma**     | Tanımlı sinyali yayınlar.                                    | `emit_signal("player_died")`     |
| **signal bağlama**   | Bir sinyali belirli bir işlevle ilişkilendirir.              | `connect("player_died", self, "_on_player_died")` |

## Sinyal Kullanım Durumları:
- **UI butonu tıklama**: UI bileşenleri bir buton tıklandığında `signal` yayabilir ve bu sinyale bağlı işlev çalıştırılabilir.
- **Karakterin ölümü**: `player_died` sinyali yayıldığında diğer bileşenlere bu olay bildirilebilir ve tepkiler (örneğin, oyun sonu ekranı açılması) tetiklenebilir.

# Godot'ta En İyi Pratikler

| Pratik                        | Açıklama                                                                 |
|-------------------------------|--------------------------------------------------------------------------|
| **Modüler Kod Yazımı**        | Her node ve script'in tek bir sorumluluğu olmalı. Bu, bakım ve geliştirmeyi kolaylaştırır. |
| **Sahneleri Parçalara Bölme** | Her sahne, sadece tek bir oyun varlığını içermeli. Oyuncu, düşman, seviyeler ayrı ayrı oluşturulmalı ve gerektiğinde birleştirilmeli. |
| **Signal Kullanımı**          | Bağımsız bileşenler arasında haberleşmek için sinyaller kullanılmalı. Bu, bileşen bağımlılıklarını azaltır. |
| **Export Değişkenler**        | Değişkenleri `export` ile tanımlayarak, inspector üzerinden düzenlenebilir hale getirin. Bu, test ve deneme sırasında hız kazandırır. |

## En İyi Pratikler Önerileri:
- **Modülerlik**: Kodun modüler ve sorumlulukları ayrılmış olması, proje büyüdükçe karışıklığı önler.
- **Sinyaller**: Oyundaki nesnelerin birbirleriyle doğrudan bağlantı kurması yerine, sinyaller aracılığıyla haberleşmesi önerilir. Bu yaklaşım, bileşenleri birbirinden bağımsız tutar.

# Godot Engine Genel Kısayollar

| İşlem                     | Kısayol Tuşu                          |
|---------------------------|---------------------------------------|
| **Sahne Oynat/Durdur**    | `F5` / `Shift + F5`                   |
| **Sahneye Hızlı Erişim**  | `Ctrl + Shift + O`                    |
| **Yeni Node Ekle**        | `Ctrl + A`                            |
| **Inspector'ı Aç**        | `Ctrl + I`                            |
| **Komut Paletini Aç**     | `F1`                                  |
| **Sahneler Arasında Geçiş** | `Alt + Tab`                           |
| **Script Düzenleyici Aç** | `F3`                                  |

## Kısayolların Kullanımı:
- **Oynatma/Durdurma (`F5`)**: Sahneyi hızlıca test etmek ve geri dönmek için kullanılır. Geliştirme sürecini hızlandırır.
- **Yeni Node Ekle (`Ctrl + A`)**: Yeni bir node eklemek için hızlı bir erişim sağlar, bu da özellikle sahne düzenlemesi sırasında faydalıdır.
