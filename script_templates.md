# GDScript Yazım Kuralları ve Standartları

GDScript, Godot oyun motorunda kullanılan özel bir programlama dilidir. Projede düzenli, okunabilir ve sürdürülebilir kod yazmak için aşağıdaki standartlar ve yazım kuralları izlenmelidir. Bu kurallar, büyük projelerde çalışmayı kolaylaştırır ve ekip içi uyumu sağlar.

## 1. Değişken ve Fonksiyon İsimlendirme Kuralları

### Snake_case Kullanımı
GDScript'te, değişken ve fonksiyon isimleri için **snake_case** kullanılır. Bu, kelimeleri alt çizgi (_) ile ayırarak isimlendirme yapılması anlamına gelir. Küçük harflerle yazılır ve boşluk kullanılmaz.

**Örnek:**
```gdscript
var player_health = 100
func move_player():
	pass
```

### Anlamlı ve Açıklayıcı İsimler
Değişken ve fonksiyon isimleri kısa ama açıklayıcı olmalıdır. İsimlendirme, değişkenin veya fonksiyonun ne yaptığı hakkında açık bir fikir vermelidir.

**Örnek:**
```gdscript
var player_speed = 10.0
var max_enemy_count = 5
```

### Boolean Değişkenler için "is" veya "has" Öneki
Boolean (doğru/yanlış) değişkenleri isimlendirirken, **is** veya **has** önekini kullanmak yaygın bir pratiktir. Bu, boolean değişkenlerinin amacını net bir şekilde gösterir.

**Örnek:**
```gdscript
var is_game_over = false
var has_key = true
```

## 2. Sabitler (Constants)

Sabitler, **BÜYÜK HARF** ve kelimeler arasında alt çizgi (_) kullanılarak isimlendirilir. Bu, sabitlerin kolayca tanımlanmasını sağlar.

**Örnek:**
```gdscript
const MAX_HEALTH = 100
const PLAYER_SPEED = 10.0
```

## 3. Sınıf İsimlendirme

Sınıf isimleri **PascalCase** kullanılarak yazılır. Her kelimenin ilk harfi büyük olur ve kelimeler arasında boşluk ya da alt çizgi kullanılmaz.

**Örnek:**
```gdscript
class_name PlayerCharacter
```

## 4. Yorum Satırları

Yorum satırları, kodu açıklamak ve ileride kodu inceleyecek diğer kişilere (veya kendinize) kodun amacını hatırlatmak için kullanılır. Tek satırlık yorumlar için **#** kullanılır. Uzun açıklamalar gerektiğinde, yorumlar fonksiyon veya sınıf üstünde yer almalıdır.

**Örnek:**
```gdscript
# Oyuncu sağlığı bu değişkene atanır.
var player_health = 100

# Oyuncuyu hareket ettiren fonksiyon
func move_player(delta):
	# Delta zamanı kullanarak oyuncu hızını artır
	player.position.x += player_speed * delta
```

## 5. Kod Blokları ve İndentasyon

Kod blokları 4 boşluk kullanılarak girintilenir. GDScript'te girintileme, kodun doğru çalışması için önemlidir çünkü blok yapısı girintiye göre belirlenir.

**Örnek:**
```gdscript
func _ready():
	if is_game_over:
	  restart_game()
	else:
	  start_game()
```

## 6. Fonksiyon İsimlendirme

Fonksiyon isimleri **snake_case** formatında yazılır. Fonksiyonlar, eylemi veya işlevi açıkça ifade edecek şekilde isimlendirilmelidir. Fonksiyon isimlendirme, değişken isimlendirmesine benzer şekilde yapılır.

**Örnek:**
```gdscript
func start_game():
	pass

func restart_game():
	pass
```

## 7. Signal (Sinyal) İsimlendirme

Sinyal isimleri de **snake_case** ile yazılır. Genellikle olayları tanımlamak için sinyaller kullanılır ve isimleri olayla ilişkili olmalıdır.

**Örnek:**
```gdscript
signal player_died
signal level_completed
```

## 8. Dosya ve Kaynak İsimlendirme

Dosya isimlendirmede **snake_case** kullanılması önerilir. Ayrıca, dosya isimleri dosyanın içeriğini veya amacını açıklayıcı olmalıdır. Örneğin, bir script dosyası karakter kontrolü içeriyorsa, dosya ismi **player_controller.gd** gibi olabilir.

**Örnek:**
```gdscript
player_controller.gd
enemy_ai.gd
```

## 9. Fonksiyon Sıralaması ve Yapısı

GDScript dosyalarında fonksiyonların belli bir mantık sırasına göre yerleştirilmesi okunabilirliği artırır. Fonksiyonlar genellikle aşağıdaki sırayla sıralanmalıdır:

1. **_ready()**: Node sahneye yüklendiğinde çağrılır.
2. **_process(delta)**: Her karede sürekli olarak çağrılır.
3. Signal bağlantıları ve sinyallerin tanımları.
4. Kendi özel fonksiyonlarınız.

**Örnek:**
```gdscript
func _ready():
	initialize_game()

func _process(delta):
	update_player_position(delta)

func initialize_game():
	# Oyun başlangıç ayarları

func update_player_position(delta):
	# Oyuncunun pozisyonunu güncelle
```

## 10. GDScript'te Godot Spesifik Fonksiyonlar

Bazı Godot'a özel işlevler belirli isimlendirme kurallarına uymalıdır. Bunlar genellikle bir **_** (alt çizgi) ile başlar ve Godot tarafından otomatik olarak çağrılır.

**Örnek:**
```gdscript
var player_health = 100
func move_player():
	pass

func _process(delta):
	# Her karede çalışır
	pass

func _physics_process(delta):
	# Her fizik karesinde çalışır
	pass
```

## 11. İsim Çakışmalarını Önlemek

GDScript'te, değişken ve fonksiyon isimlerinde çakışmaları önlemek için dikkatli olunmalıdır. Özellikle Godot'un dahili fonksiyonları ile aynı ismi kullanmaktan kaçının.

**Doğru:**
```gdscript
func start_game():
	pass
```

**Yanlış:**
```gdscript
func process():
	pass  # process, Godot'ta dahili olarak kullanılır ve üzerine yazılmamalıdır.
```
# Player.gd - 3 Boyutlu Proje İçin Kapsamlı Player Script Şablonu

Bu dosya, 3 boyutlu bir projede oyuncu karakterini kontrol etmek için kullanılan bir Godot GDScript dosyasını içerir. Kapsayıcı bir şablon olup, birçok GDScript özelliği ve Godot iş akışına dair önemli unsurlar içerir.

```gdscript
tool
extends CharacterBody3D
class_name Player  # Script'e global bir isim verilir, böylece başka yerlerden erişim kolay olur.

# Oyuncunun can ve eşya toplama sinyali
signal health_changed(new_health)
signal item_collected(item_name)  # Oyuncu bir eşya topladığında tetiklenen özel sinyal

# Oyuncunun durumlarını takip etmek için kullanılan enum
enum PlayerState { IDLE, RUNNING, JUMPING, FALLING, ATTACKING }

# Oyuncu hareket hızları
@export var walk_speed: float = 5.0
@export var run_speed: float = 10.0
@export var jump_force: float = 15.0
@export var gravity: float = -9.8

# Can durumu ve maksimum can
@export var max_health: int = 100
var current_health: int = max_health

# Oyuncu zıplama durumu
var is_jumping: bool = false
var player_state: PlayerState = PlayerState.IDLE

# Kamera ve silah gibi harici node'lara erişim
@onready var camera = $Camera3D
@onready var weapon = $Weapon
@onready var attack_timer: Timer = $AttackTimer  # Timer node'una erişim

# Oyun başladıktan sonra çağrılan yerleşik _ready() fonksiyonu
func _ready():
    # Başlangıç durumunu ayarla
    player_state = PlayerState.IDLE
    # Sinyal bağlantıları
    connect("health_changed", self, "_on_health_changed")
    attack_timer.connect("timeout", self, "_on_attack_timeout")
    print("Player is ready!")
    add_to_group("player")  # Oyuncuyu "player" grubuna ekle

# Her karede çalıştırılan yerleşik _process() fonksiyonu
func _process(delta: float) -> void:
    handle_input(delta)  # Kullanıcı girdilerini işle
    handle_state(delta)  # Oyuncu durumuna göre işlemler yap

    # Editör modunda çalışırken pozisyonu güncelleyen tool kullanımı
    if Engine.is_editor_hint():
      # Editör modunda oyuncu pozisyonunu günceller
      print("Player position in editor: ", global_transform.origin)

# Her fizik karesinde çalıştırılan yerleşik _physics_process() fonksiyonu
func _physics_process(delta: float) -> void:
    apply_gravity(delta)  # Yerçekimini uygula
    move_and_slide()      # Hareketleri uygula

# Kullanıcı girdilerini kontrol eden fonksiyon
func handle_input(delta: float) -> void:
    var direction = Vector3.ZERO
    
    # İleri, geri, sağa ve sola hareket
    if Input.is_action_pressed("move_forward"):
      direction += -transform.basis.z
    if Input.is_action_pressed("move_backward"):
      direction += transform.basis.z
    if Input.is_action_pressed("move_left"):
      direction += -transform.basis.x
    if Input.is_action_pressed("move_right"):
      direction += transform.basis.x
    
    # Koşma veya yürüme hızı
    if Input.is_action_pressed("run"):
      velocity = direction.normalized() * run_speed
      player_state = PlayerState.RUNNING
    else:
      velocity = direction.normalized() * walk_speed
      player_state = PlayerState.IDLE
    
    # Zıplama işlemi
    if Input.is_action_just_pressed("jump") and is_on_floor():
      velocity.y = jump_force
      is_jumping = true
      player_state = PlayerState.JUMPING

# Oyuncu durumunu yöneten fonksiyon
func handle_state(delta: float) -> void:
    match player_state:
      PlayerState.IDLE:
        # Boşta iken yapılacak işlemler
        pass
      PlayerState.RUNNING:
        # Koşarken yapılacak işlemler
        pass
      PlayerState.JUMPING:
        if is_on_floor():
          is_jumping = false
          player_state = PlayerState.IDLE

# Yerçekimini uygulayan fonksiyon
func apply_gravity(delta: float) -> void:
    if not is_on_floor():
      velocity.y += gravity * delta

# Oyuncuya hasar veren fonksiyon
func take_damage(amount: int) -> void:
    current_health -= amount
    emit_signal("health_changed", current_health)
    
    if current_health <= 0:
      die()

# Oyuncunun öldüğü fonksiyon
func die() -> void:
    queue_free()  # Oyuncu ölürse sahneden silinir
    print("Player has died")

# Can durumu değiştiğinde çağrılan fonksiyon
func _on_health_changed(new_health: int) -> void:
    print("Health is now: ", new_health)

# Oyuncunun saldırı fonksiyonu
func attack() -> void:
    player_state = PlayerState.ATTACKING
    weapon.fire()  # Silah nesnesinden ateş etme fonksiyonu tetiklenir
    print("Player is attacking")
    attack_timer.start(2.0)  # 2 saniye sonra yeniden saldırı yapabilir

# Saldırı sonrası bekleme süresi dolduğunda
func _on_attack_timeout() -> void:
    print("Attack cooldown complete!")

# Kullanıcı girdi olaylarını yöneten fonksiyon
func _input(event: InputEvent) -> void:
    if event.is_action_pressed("attack"):
      attack()
    if event.is_action_pressed("heal"):
      heal(10)  # Örneğin, oyuncu 10 sağlık puanı iyileşir

# Oyuncuya sağlık ekleyen fonksiyon
func heal(amount: int) -> void:
    current_health = clamp(current_health + amount, 0, max_health)
    emit_signal("health_changed", current_health)

# Eşya toplama işlemi
func collect_item(item_name: String) -> void:
    print("Item collected: ", item_name)
    emit_signal("item_collected", item_name)

# Kamera hareketini Tween ile yumuşatmak
func move_camera_smoothly() -> void:
    tween.tween_property(camera, "translation", Vector3(0, 10, -10), 1.0)  # 1 saniyede kamerayı hareket ettir

# RayCast ile zemine çarpma kontrolü
func check_if_on_ground() -> void:
    if raycast.is_colliding():
      print("Player is on the ground!")

# Oyuncunun "player" grubunda olup olmadığını kontrol eden fonksiyon
func check_if_in_group() -> void:
    if is_in_group("player"):
      print("Player is in the 'player' group")
    else:
      print("Player is not in the 'player' group")
```

## Açıklamalar

- **tool:** Bu anahtar kelime, script'in Godot editörü içinde çalışmasını sağlar. Engine.is_editor_hint() ile editörde olduğumuzda özel davranışlar tanımlanabilir. Yukarıdaki örnekte, editör modunda oyuncu pozisyonunun her an güncellenmesini sağlayarak, test ve geliştirme sırasında gerçek zamanlı geri bildirim sağlar.
- **@export**: Değişkenlerin Godot düzenleyicisinde görünmesini ve değiştirilebilir olmasını sağlar.
- **@onready**: Sahne yüklendiğinde bir node'a erişimi garanti eder. Sahne yüklendiğinde bu node'lara otomatik olarak erişim sağlanır.
- **signal**: Bir olay meydana geldiğinde sinyal gönderir. Bu, diğer nesnelerin sinyali dinleyip tepki vermesini sağlar.
- **enum**: Bir grup sabit, sınırlı değer kümesi tanımlamak için kullanılır. Örneğin oyuncu durumu gibi sınırlı değerlerin takibini sağlar.
- **const**: Sabit değerleri tanımlamak için kullanılır. Sabitler, değiştirilemeyen değerleri temsil eder ve genellikle oyun genelinde kullanılan ayarları veya limitleri belirlemek için kullanılır.
- **_ready()**: Node sahneye yüklendiğinde çağrılan yerleşik fonksiyon. Sahne yüklendikten sonra yapılması gereken işlemleri burada tanımlayabilirsiniz.
- **_process()**: Her karede çalıştırılan yerleşik fonksiyon. Oyun içi dinamik işlemleri burada gerçekleştirebilirsiniz (örneğin, kullanıcı girdilerini işleme).
- **_physics_process()**: Her fizik karesinde çalıştırılan yerleşik fonksiyon. Fizik tabanlı hesaplamalar bu fonksiyon içerisinde yapılmalıdır.
- **move_and_slide()**: Karakterin 3D ortamda fizik tabanlı hareketini sağlar. Yerçekimi ve çarpışmalar dahil olmak üzere fizik motoru ile etkileşimli bir hareket sağlar.
- **emit_signal()**: Belirli bir sinyali tetikleyerek, diğer nesnelere bilgi gönderir (örneğin, can durumu değiştiğinde diğer nesneleri bilgilendirme).
- **input():** Kullanıcıdan gelen girdi olaylarını işleyen yerleşik fonksiyon. Klavye, fare veya oyun kumandası girdilerini bu fonksiyon ile yakalayabilirsiniz.
- **queue_free():** Node'u sahneden kaldırmak için kullanılır. Örneğin, bir oyuncu öldüğünde karakteri sahneden silmek için bu fonksiyon kullanılır.
- **match:** Bir değişkenin değerine göre farklı durumları kontrol etmek için kullanılır. Bu, özellikle belirli bir değere göre farklı işlemler yapmak istediğinizde faydalıdır.
- **tool:** Bu anahtar kelime, script'in Godot editörü içinde çalışmasını sağlar. **Engine.is_editor_hint()** ile editörde olduğumuzda özel davranışlar tanımlanabilir. Yukarıdaki örnekte, editör modunda oyuncu pozisyonunun her an güncellenmesini sağlayarak, test ve geliştirme sırasında gerçek zamanlı geri bildirim sağlar.
- **_input():** Kullanıcı girdilerini yakalar ve işleme alır.
- **add_to_group():** Node'u belirtilen bir gruba ekler. Burada oyuncu "player" grubuna eklenir.
- **is_in_group():** Node'un belirtilen grupta olup olmadığını kontrol eder.
- **Timer:** Bir işlem yapılmadan önce belli bir süre beklenmesini sağlar. Burada oyuncunun saldırıdan sonra tekrar saldırı yapabilmesi için bekleme süresi ayarlanmıştır. attack_timer.start(2.0) ile 2 saniyelik bir bekleme başlatılır ve süre dolduğunda _on_attack_timeout() fonksiyonu tetiklenir.
- **Tween:** Nesnelerin yumuşak bir şekilde hareket etmesini veya değerlerin zamanla değiştirilmesini sağlar.
- **RayCast:** Nesnenin bir yüzeyle çarpışıp çarpışmadığını kontrol eder.
- **Custom Signal:** Kendi sinyallerinizi tanımlayıp tetikleyebilirsiniz. Burada bir eşya toplandığında sinyal tetiklenir.
- **class_name:** Script'i küresel hale getirir, böylece diğer sahnelerde veya scriptlerde bu sınıfı referans alabilirsiniz. Script'in bir nesne olarak otomatik olarak Godot düzenleyicisinde görünmesini sağlar. Diğer sahnelerden bu sınıfı kolayca oluşturabilir ve kullanabilirsiniz.
- 
