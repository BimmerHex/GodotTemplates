# Tüm Nodeların Açıklamaları ve Kullanım Senaryo Örnekleri

<table>
    <thead>
        <tr>
            <th>Node Adı</th>
            <th>Açıklama</th>
            <th>Kullanım Senaryosu</th>
        </tr>
    </thead>
    <tbody>
        <tr>
        <td><strong>Node</strong></td>
        <td>Godot'ta sahnelerin yapı taşıdır. Diğer node türlerinin temelini oluşturur ve karmaşık yapılar için kullanılır.</td>
        <td>Oyunun temel yapısında mantıksal bir gruplama yaparak sahneleri yönetmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Viewport</strong></td>
        <td>Render edilen içeriklerin görüntülendiği ana pencere veya alt pencere.</td>
        <td>Bir FPS oyununda mini haritayı ayrı bir Viewport'ta render ederek göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Window</strong></td>
        <td>Pencere benzeri UI bileşeni, diyalog veya bilgi göstermek için kullanılır.</td>
        <td>Oyuncuya "Ayarlar" penceresini açarak çeşitli seçenekler sunmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>AcceptDialog</strong></td>
        <td>Kullanıcının belirli bir işlemi kabul etmesini isteyen bir diyalog.</td>
        <td>Oyuncuya oyunu kapatmadan önce emin olup olmadığını soran bir onay penceresi göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>ConfirmationDialog</strong></td>
        <td>Kullanıcının işlemi onaylaması gereken bir tür <strong>AcceptDialog</strong>.</td>
        <td>Oyuncunun oyunu kaydedip kaydetmemesi gerektiğini onaylamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>FileDialog</strong></td>
        <td>Kullanıcının dosya seçmesini sağlayan bir diyalog.</td>
        <td>Oyuncunun özel bir harita dosyasını yüklemesini sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Popup</strong></td>
        <td>Kullanıcının etkileşimde bulunması gereken açılır pencere.</td>
        <td>Bir oyun içi mağaza açıldığında, kullanıcının "Ürün Satın Al" butonuna bastığında bir popup gösterebilir.</td>
        </tr>
        <tr>
        <td><strong>PopupMenu</strong></td>
        <td>Kullanıcıya bir menü sunar.</td>
        <td>Oyun içinde ayarlar veya seçenekler sunmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>PopupPanel</strong></td>
        <td>İçeriği bir panelde görüntüleyen popup bileşeni.</td>
        <td>Oyun içinde karakter bilgilerini veya envanter detaylarını göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Node2D</strong></td>
        <td>2D sahne içinde konumlandırılabilecek temel node.</td>
        <td>Bir karakter sprite'ı, bir Node2D'nin altında konumlandırılabilir ve sahne içinde hareket ettirilebilir.</td>
        </tr>
        <tr>
        <td><strong>CollisionObject2D</strong></td>
        <td>2D çarpışmaları yönetmek için temel node.</td>
        <td>Bir platform oyununda karakterin zemine çarpışmasını algılamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>PhysicsBody2D</strong></td>
        <td>2D fizik simülasyonu için kullanılan temel node.</td>
        <td>Karakter veya düşman gibi fizik kurallarına tabi olan nesneler için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>StaticBody2D</strong></td>
        <td>Sabit, hareket etmeyen fiziksel nesneler için kullanılan node.</td>
        <td>Zemin veya duvar gibi hareket etmeyen engeller oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>RigidBody2D</strong></td>
        <td>Dinamik olarak hareket eden ve fizik kurallarına tabi olan nesneler için kullanılır.</td>
        <td>Oyuncunun fırlattığı bir taşın gerçekçi bir şekilde hareket etmesini sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CharacterBody2D</strong></td>
        <td>2D karakterler için özel olarak tasarlanmış fiziksel body.</td>
        <td>Karakterin hareketini ve çarpışmasını kontrol etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>PhysicalBone2D</strong></td>
        <td>Fizik simülasyonu ile kontrol edilen kemik yapısı.</td>
        <td>Bir ragdoll karakter oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Area2D</strong></td>
        <td>Çarpışma algılama ve diğer etkileşimler için kullanılan bir node.</td>
        <td>Bir güçlendirme (power-up) alanına girildiğinde, oyuncuya ek güç vermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>AnimatedSprite2D</strong></td>
        <td>2D karakter veya objelerin animasyonlarını oynatmak için kullanılır.</td>
        <td>Bir karakterin koşma ve zıplama animasyonlarını göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>AudioListener2D</strong></td>
        <td>2D seslerin dinleyici noktasını belirler.</td>
        <td>Oyuncu karakterinin konumuna göre seslerin nasıl duyulacağını ayarlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>AudioStreamPlayer2D</strong></td>
        <td>2D dünyasında ses oynatır.</td>
        <td>Arka planda müzik çalmak veya bir karakterin adım seslerini çalmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>BackBufferCopy</strong></td>
        <td>Geri tampondaki görüntüyü kullanarak efektler uygulamak için kullanılır.</td>
        <td>Ekrana bir bulanıklık efekti vermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Bone2D</strong></td>
        <td>2D karakterlerde iskelet yapısını oluşturmak için kullanılır.</td>
        <td>Karakterin kollarını ve bacaklarını animasyonla hareket ettirmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CPUParticles2D</strong></td>
        <td>2D dünyasında CPU bazlı parçacık efektleri oluşturmak için kullanılır.</td>
        <td>Patlama efektleri veya toz bulutları oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Camera2D</strong></td>
        <td>2D dünyasında belirli bir alanı göstermek için kullanılan kamera.</td>
        <td>Oyuncu karakterini takip eden bir kamera oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CanvasGroup</strong></td>
        <td>Aynı CanvasLayer'daki çocukların opaklık ve görünürlüğünü etkileyen grup.</td>
        <td>Belirli UI elemanlarını (menü veya HUD) toplu olarak gizlemek veya göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CanvasModulate</strong></td>
        <td>Ekranın tamamını belirli bir renk tonuna boyar.</td>
        <td>Oyun sırasında ekranın kararması veya renk değişikliği gerektiğinde kullanılır, örneğin hasar alındığında.</td>
        </tr>
        <tr>
        <td><strong>CollisionPolygon2D</strong></td>
        <td>2D çarpışmalar için çokgen şekli oluşturur.</td>
        <td>2D bir platformda yer şekillerine uygun çarpışma alanları tanımlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CollisionShape2D</strong></td>
        <td>Çarpışmalar için basit şekil tanımlamak amacıyla kullanılır.</td>
        <td>Bir karakter veya nesne için basit çarpışma alanları oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Joint2D</strong></td>
        <td>İki PhysicsBody2D arasındaki bağlantıyı sağlar.</td>
        <td>Bir araba oyunu yaparken iki tekerleği şasiye bağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Light2D</strong></td>
        <td>2D sahnede ışık efekti oluşturur.</td>
        <td>Karanlık bir mağara sahnesine atmosfer katmak için ışık kaynağı eklenir.</td>
        </tr>
        <tr>
        <td><strong>DirectionalLight2D</strong></td>
        <td>Yönlü 2D ışık kaynağı.</td>
        <td>Güneş ışığını simüle etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>PointLight2D</strong></td>
        <td>Noktasal bir 2D ışık kaynağıdır.</td>
        <td>Bir fener veya lambanın ışığını simüle etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>GPUParticles2D</strong></td>
        <td>GPU üzerinde çalışan 2D parçacık efektleri oluşturur.</td>
        <td>Kar yağışı veya yıldız efekti gibi performans açısından yoğun efektler için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>LightOccluder2D</strong></td>
        <td>2D ışık kaynaklarını engelleyen öğe.</td>
        <td>Belirli nesnelerin arkasındaki ışığı engellemek için kullanılır, örneğin bir duvarın gölgesi.</td>
        </tr>
        <tr>
        <td><strong>Line2D</strong></td>
        <td>2D çizgi çizer.</td>
        <td>Oyuncunun yolunu veya harita üzerinde yönlendirme yapmak için kullanılabilir.</td>
        </tr>
        <tr>
        <td><strong>Marker2D</strong></td>
        <td>Geliştiriciler için sahnede özel bir işaretçi olarak kullanılır, işleme yapılmaz.</td>
        <td>Oyun içi haritada önemli konumları işaretlemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>MeshInstance2D</strong></td>
        <td>2D mesh sahnede temsil edilir.</td>
        <td>Belirli geometrik şekiller veya özel yapılmış nesneleri sahnede göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>MultiMeshInstance2D</strong></td>
        <td>Aynı tipte çoklu 2D mesh'leri işlemek için kullanılır.</td>
        <td>Performans kazanımı amacıyla birçok aynı nesnenin (örn: ağaçlar) sahnede gösterimi için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>NavigationLink2D</strong></td>
        <td>2D navigasyon sistemi için iki bölgeyi birbirine bağlar.</td>
        <td>Bir platform oyununda iki farklı navigasyon bölgesini birbirine bağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>NavigationObstacle2D</strong></td>
        <td>2D navigasyon yollarında engel oluşturur.</td>
        <td>Bir düşmanın hareketini belirli alanlarda kısıtlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>NavigationRegion2D</strong></td>
        <td>2D navigasyon sisteminin kapsama alanını belirler.</td>
        <td>Bir karakterin belirli bir bölgede hareket edebilmesi için yol oluşturmak amacıyla kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Parallax2D</strong></td>
        <td>Arka planın kameraya göre hareket etme hızını ayarlar, paralaks efekti oluşturur.</td>
        <td>Dağlar veya uzak manzaralar gibi arka planların daha yavaş hareket ederek derinlik efekti oluşturulması için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>ParallaxLayer</strong></td>
        <td>Parallax efekti oluşturacak katmanlar ekler.</td>
        <td>Arka plan katmanlarını farklı hızlarda kaydırarak görsel derinlik yaratmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Path2D</strong></td>
        <td>Bir 2D yol tanımlar.</td>
        <td>Karakterin veya düşmanın belirli bir rotayı izlemesi gerektiğinde kullanılır.</td>
        </tr>
        <tr>
        <td><strong>PathFollow2D</strong></td>
        <td>Bir 2D yolu takip eden node.</td>
        <td>Bir düşmanın veya nesnenin bir patika üzerinde hareket etmesi için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Polygon2D</strong></td>
        <td>2D çokgen şekli çizer.</td>
        <td>Kullanıcının belirli alanları veya şekilleri temsil etmek için çokgen çizmesi gerektiğinde kullanılır.</td>
        </tr>
        <tr>
        <td><strong>RayCast2D</strong></td>
        <td>Belirli bir doğrultuda çarpışma tespiti yapar.</td>
        <td>Karakterin görüş hattını veya bir nesnenin lazer ışını atıp atmadığını tespit etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>RemoteTransform2D</strong></td>
        <td>Bir nesnenin transformasyonunu uzaktan kontrol eder.</td>
        <td>Belirli bir nesnenin başka bir nesneye göre hareket etmesini sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>ShapeCast2D</strong></td>
        <td>Bir şeklin belirli bir yönde çarpışma yapıp yapmadığını kontrol eder.</td>
        <td>Karakterin bir platforma çarpıp çarpmadığını tespit etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Skeleton2D</strong></td>
        <td>2D karakterlerde iskelet yapısını oluşturur.</td>
        <td>Karakter animasyonlarını kemikler yardımıyla kontrol etmek için kullanılır (örneğin kol hareketi).</td>
        </tr>
        <tr>
        <td><strong>Sprite2D</strong></td>
        <td>2D grafiklerin sahneye yerleştirildiği node.</td>
        <td>Oyuncunun kontrol ettiği karakterin görselini oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>TileMap</strong></td>
        <td>2D döşeme haritası oluşturmak için kullanılır.</td>
        <td>Platform oyunlarında zemin ve duvar gibi yapıları düzenlemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>TileMapLayer</strong></td>
        <td>TileMap içindeki katmanları yönetmek için kullanılır.</td>
        <td>Farklı döşeme katmanlarını (örn: arka plan, ön plan) birbirinden ayırmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>TouchScreenButton</strong></td>
        <td>Mobil cihazlar için dokunmatik buton oluşturur.</td>
        <td>Mobil bir oyunda karakterin zıplama veya ateş etme eylemlerini kontrol etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>VisibleOnScreenNotifier2D</strong></td>
        <td>Ekranda görünürlüğü algılar ve bir sinyal gönderir.</td>
        <td>Karakterin veya düşmanın ekranda görünüp görünmediğini kontrol etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>VisibleOnScreenEnabler2D</strong></td>
        <td>Bir nesne ekranda göründüğünde belirli işlevlerin etkinleştirilmesini sağlar.</td>
        <td>Performans iyileştirmesi amacıyla, ekranda olmadığında düşmanın davranışını durdurmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Control</strong></td>
        <td>UI elemanlarını düzenlemek ve kontrol etmek için kullanılan temel node.</td>
        <td>Ana menüde butonları ve diğer UI elemanlarını düzenlemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Container</strong></td>
        <td>UI elemanlarını organize etmek ve hizalamak için kullanılan node.</td>
        <td>Bir ana menüde butonların düzgün hizalanması için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>AspectRatioContainer</strong></td>
        <td>UI elemanlarının belirli bir en-boy oranını korumasını sağlar.</td>
        <td>Ekran boyutları değişse bile bir görüntü veya panelin orantılı olarak ayarlanması için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>BoxContainer</strong></td>
        <td>UI elemanlarını dikey veya yatay olarak hizalamak için kullanılır.</td>
        <td>Birden fazla butonun yan yana veya alt alta düzenlenmesi gerektiğinde kullanılır.</td>
        </tr>
        <tr>
        <td><strong>VBoxContainer</strong></td>
        <td>UI elemanlarını dikey olarak hizalar.</td>
        <td>Menü seçeneklerini dikey olarak sıralamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>HBoxContainer</strong></td>
        <td>UI elemanlarını yatay olarak hizalar.</td>
        <td>Bir ses kontrol çubuğu ve etiketlerini yatay olarak hizalamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CenterContainer</strong></td>
        <td>Bir UI elemanını ebeveyn node'unun ortasına hizalar.</td>
        <td>Ana menüde bir başlık veya resmin ekranın ortasına hizalanması için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>FlowContainer</strong></td>
        <td>UI elemanlarını satır ve sütun olarak otomatik düzenler.</td>
        <td>Dinamik olarak artan UI elemanlarını (örn: simgeler veya kartlar) düzgün bir şekilde düzenlemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>HFlowContainer</strong></td>
        <td>UI elemanlarını yatay bir akışta düzenler.</td>
        <td>Araç çubuğundaki simgeleri otomatik olarak düzenlemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>VFlowContainer</strong></td>
        <td>UI elemanlarını dikey bir akışta düzenler.</td>
        <td>Uzun bir liste veya seçeneklerin dikey olarak hizalanması için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>GraphElement</strong></td>
        <td>Grafik düzenleme için kullanılan node.</td>
        <td>Bir grafik arayüzde düğüm ve kenarları temsil etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>GraphFrame</strong></td>
        <td>Grafik elemanlarını bir çerçevede düzenler.</td>
        <td>Diyagram veya grafik çizimlerinde çerçevelemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>GraphNode</strong></td>
        <td>Bir grafik arayüzünde bir düğüm temsil eder.</td>
        <td>Bir görsel programlama dili arayüzü tasarlarken mantıksal blokları temsil etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>GridContainer</strong></td>
        <td>UI elemanlarını bir ızgara düzeninde düzenler.</td>
        <td>Envanter veya kart sistemi gibi eşit boyutlu elemanların düzenlenmesi için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>SplitContainer</strong></td>
        <td>Ekranı iki parçaya bölen ve kullanıcıya bu bölümleri ayarlama olanağı tanıyan bir container.</td>
        <td>Bir oyun ayarları ekranında ses ve grafik ayarlarını aynı anda göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>HSplitContainer</strong></td>
        <td>UI elemanlarını yatay olarak ikiye böler.</td>
        <td>Yan yana karşılaştırmalı tablo veya ayarlar ekranında kullanılır.</td>
        </tr>
        <tr>
        <td><strong>VSplitContainer</strong></td>
        <td>UI elemanlarını dikey olarak ikiye böler.</td>
        <td>Ekranın üst ve alt bölümlerini ayrı olarak düzenlemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>MarginContainer</strong></td>
        <td>İçerdiği elemanlara kenar boşlukları eklemek için kullanılır.</td>
        <td>UI elemanlarına ekstra boşluk ekleyerek daha düzenli bir görüntü sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>PanelContainer</strong></td>
        <td>Panel benzeri bir UI elementini çocuk elemanlarla doldurmak için kullanılır.</td>
        <td>Ayarlar ekranında belirli seçenekleri bir panel içinde göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>ScrollContainer</strong></td>
        <td>İçerdiği elemanlar taşırsa kaydırma imkanı sunan bir container.</td>
        <td>Uzun bir liste veya metin kutusu oluşturulduğunda dikey/yatay kaydırma sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>SubViewportContainer</strong></td>
        <td>Başka bir Viewport'un içeriğini göstermek için kullanılır.</td>
        <td>Mini harita veya yan kamera görünümünü ana görünümde göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>TabContainer</strong></td>
        <td>Birden fazla UI elemanını sekmeli bir yapı içinde düzenler.</td>
        <td>Ayarlar menüsünü ses, kontrol, grafik vb. kategorilere ayırmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>BaseButton</strong></td>
        <td>Butonlar için temel sınıf, kullanıcı girişini alır ve işlevleri tetikler.</td>
        <td>Bir "Oyna" veya "Çıkış" butonunu oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Button</strong></td>
        <td>Kullanıcıdan giriş almak için kullanılan tıklanabilir buton.</td>
        <td>Başla veya Ayarlar gibi bir menüdeki seçenekler için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CheckBox</strong></td>
        <td>Kullanıcının bir seçeneği seçip seçmemesini sağlayan bir kutucuk.</td>
        <td>Oyun ayarlarında "Tam Ekran" veya "Ses Açık" gibi seçenekler eklemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CheckButton</strong></td>
        <td>Hem buton hem de checkbox işlevi gören bir buton.</td>
        <td>Bir listeden belirli seçeneklerin seçilmesini sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>ColorPickerButton</strong></td>
        <td>Renk seçmek için kullanılan bir buton.</td>
        <td>Oyun içinde karakterin kıyafet rengini ayarlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>MenuButton</strong></td>
        <td>Tıkladığında bir menü açan buton.</td>
        <td>Ayarlar veya profil seçeneklerinin açılması için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>OptionButton</strong></td>
        <td>Kullanıcının belirli seçenekler arasından seçim yapmasını sağlayan açılır buton.</td>
        <td>Grafik ayarlarında çözünürlük veya kalite seçeneklerini sunmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>LinkButton</strong></td>
        <td>Tıkladığında kullanıcıyı bir bağlantıya yönlendiren buton.</td>
        <td>Oyunun resmi web sitesine yönlendiren bir "Daha Fazla Bilgi" butonu oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>TextureButton</strong></td>
        <td>Görsel olarak özelleştirilebilir bir buton.</td>
        <td>Oyun içi özel düğmelerin (örn: kalkan, saldırı) grafiksel olarak özelleştirilmiş halde gösterimi için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>TextEdit</strong></td>
        <td>Çok satırlı metin düzenlemeye izin veren UI elemanı.</td>
        <td>Oyuncunun bir isim veya not yazmasını sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CodeEdit</strong></td>
        <td>Kod düzenleme işlemlerini yapabilen bir metin editörü.</td>
        <td>Oyun içinde basit bir komut dizisi yazılması veya mod desteği sunulması için kullanılabilir.</td>
        </tr>
        <tr>
        <td><strong>ColorRect</strong></td>
        <td>Belirli bir rengi doldurmak için kullanılan UI elemanı.</td>
        <td>Ekranın belirli bir alanını renklendirmek veya görsel bir arka plan oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>GraphEdit</strong></td>
        <td>Grafik elemanlarını görsel olarak düzenlemeye olanak tanıyan bir UI elemanı.</td>
        <td>Oyun mantığını veya AI davranışlarını düğümlerle görsel olarak tasarlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Range</strong></td>
        <td>Bir değer aralığını temsil eden UI elemanı, kaydırma çubukları ve benzeri elemanların temelini oluşturur.</td>
        <td>Ses seviyesini veya bir oyun içi parametreyi düzenlemek için kaydırıcı olarak kullanılır.</td>
        </tr>
        <tr>
        <td><strong>ScrollBar</strong></td>
        <td>Kullanıcının içerik üzerinde gezinmesini sağlayan kaydırma çubuğu.</td>
        <td>Uzun bir liste veya bir metin kutusu içinde gezinme sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>HScrollBar</strong></td>
        <td>Yatay kaydırma çubuğu.</td>
        <td>Geniş bir tablo veya haritada yatay gezinme sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>VScrollBar</strong></td>
        <td>Dikey kaydırma çubuğu.</td>
        <td>Uzun bir metin veya liste içinde dikey gezinme sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Slider</strong></td>
        <td>Bir değeri arttırmak veya azaltmak için kullanılan kaydırıcı.</td>
        <td>Ses seviyesini ayarlamak veya bir parametre değerini seçmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>HSlider</strong></td>
        <td>Yatay bir kaydırıcı.</td>
        <td>Ses veya parlaklık gibi bir değeri ayarlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>VSlider</strong></td>
        <td>Dikey bir kaydırıcı.</td>
        <td>Ekran parlaklığı veya benzeri bir değeri dikey olarak ayarlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>ProgressBar</strong></td>
        <td>Bir ilerleme durumunu gösteren bar.</td>
        <td>Bir yükleme işleminin durumunu veya bir görevdeki ilerlemeyi göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>SpinBox</strong></td>
        <td>Kullanıcının bir sayısal değeri arttırıp azaltmasını sağlayan UI elemanı.</td>
        <td>Karakter özelliklerini (örneğin: saldırı gücü) düzenlemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>TextureProgressBar</strong></td>
        <td>Görsel olarak özelleştirilebilen bir ilerleme çubuğu.</td>
        <td>Oyuncunun sağlık veya mana durumunu özel grafiklerle göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Separator</strong></td>
        <td>UI elemanlarını görsel olarak ayırmak için kullanılan bir çizgi.</td>
        <td>Menüde farklı bölümleri görsel olarak ayırmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>HSeparator</strong></td>
        <td>Yatay bir ayraç.</td>
        <td>Ayarlar menüsünde kategorileri ayırmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>VSeparator</strong></td>
        <td>Dikey bir ayraç.</td>
        <td>Yan yana yer alan seçenekleri görsel olarak ayırmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>ItemList</strong></td>
        <td>Birden fazla öğeyi listelemek için kullanılan UI elemanı.</td>
        <td>Oyun içi envanter sisteminde eşyaları listelemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Label</strong></td>
        <td>Sabit bir metni göstermek için kullanılan UI elemanı.</td>
        <td>Karakter adı veya açıklamalar gibi sabit bilgiler göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>LineEdit</strong></td>
        <td>Tek satırlı metin girişini sağlayan UI elemanı.</td>
        <td>Oyuncunun adını yazması veya kısa bir bilgi girmesi gerektiğinde kullanılır.</td>
        </tr>
        <tr>
        <td><strong>MenuBar</strong></td>
        <td>Farklı menü öğelerinin yer aldığı yatay bir çubuk.</td>
        <td>Oyun içi düzenleme, görüntüleme veya ayarlar gibi farklı seçenekleri bir araya toplamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>NinePatchRect</strong></td>
        <td>Değiştirilebilir boyutlarda, köşe bölümleri sabit kalan bir UI öğesi.</td>
        <td>Görsel arayüz elemanlarının, özellikle düğme veya pencerelerin yeniden boyutlandırılabilir yapılması için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Panel</strong></td>
        <td>Basit bir UI paneli oluşturur, çocuk elemanları göstermek için kullanılır.</td>
        <td>Oyun içi bilgi kutularını veya ayarları içeren bölümleri göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>ReferenceRect</strong></td>
        <td>UI öğelerini hizalamak için görsel bir referans çerçevesi olarak kullanılır.</td>
        <td>Diğer UI elemanlarının düzenlenmesi veya hizalanmasında rehber olarak kullanılır.</td>
        </tr>
        <tr>
        <td><strong>RichTextLabel</strong></td>
        <td>Biçimlendirilmiş metin göstermek için kullanılan UI elemanı.</td>
        <td>Hikaye anlatımı veya diyaloğun stilize edilmiş bir şekilde gösterimi için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>TabBar</strong></td>
        <td>Sekmeleri yatay olarak listeleyen bir çubuk.</td>
        <td>Oyun içi ayarları farklı kategorilere ayırarak kullanıcının arasında geçiş yapabilmesi için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>TextureRect</strong></td>
        <td>Belirli bir görseli göstermek için kullanılan UI elemanı.</td>
        <td>Bir karakterin avatarını veya bir ödül simgesini göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Tree</strong></td>
        <td>Hiyerarşik yapıda öğeleri listelemek için kullanılan UI elemanı.</td>
        <td>Oyun içinde bir görev veya beceri ağacı oluşturmak ve kullanıcıya göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>VideoStreamPlayer</strong></td>
        <td>Video dosyalarını oynatmak için kullanılan node.</td>
        <td>Oyun içi sinematik veya hikaye anlatımı için video oynatmak amacıyla kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Node3D</strong></td>
        <td>3D dünyasında yer alan nesneler için kullanılan temel node.</td>
        <td>3D bir dünyada bir obje veya karakterin yerleştirilmesi ve yönetilmesi için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CollisionObject3D</strong></td>
        <td>3D çarpışmaları yönetmek için kullanılan temel node.</td>
        <td>Bir karakterin veya objenin duvara çarpmasını algılamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>PhysicsBody3D</strong></td>
        <td>3D fizik simülasyonu için kullanılan temel node.</td>
        <td>Arabalar, karakterler veya nesneler gibi fizik kurallarına tabi olan 3D nesneler için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>StaticBody3D</strong></td>
        <td>Sabit, hareket etmeyen fiziksel nesneler için kullanılan node.</td>
        <td>Zemin veya duvar gibi hareket etmeyen engeller oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>AnimatableBody3D</strong></td>
        <td>Animasyonları fiziksel etkileşimlerle birleştirebilen 3D fiziksel gövde.</td>
        <td>Bir kapının veya köprünün fiziksel kuvvetlerle açılıp kapanması gibi senaryolarda kullanılır. Karakter veya nesneler bu kapılarla etkileşime girdiğinde animasyon tetiklenir.</td>
        </tr>
        <tr>
        <td><strong>CharacterBody3D</strong></td>
        <td>3D karakterler için özel olarak tasarlanmış fiziksel body.</td>
        <td>Karakterlerin hareketini ve çarpışmasını kontrol etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>PhysicalBone3D</strong></td>
        <td>Fizik simülasyonu ile kontrol edilen kemik yapısı.</td>
        <td>Ragdoll karakter oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>RigidBody3D</strong></td>
        <td>Dinamik olarak hareket eden ve fizik kurallarına tabi olan 3D nesneler için kullanılır.</td>
        <td>Fırlatılan bir taşın veya düşen bir kutunun fizik kurallarına göre hareket etmesini sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>VehicleBody3D</strong></td>
        <td>3D araç simülasyonu için kullanılan node.</td>
        <td>Araba veya benzeri bir aracın fiziksel davranışlarını simüle etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Area3D</strong></td>
        <td>Çarpışma algılama ve diğer etkileşimler için kullanılan bir node.</td>
        <td>Bir güçlendirme (power-up) bölgesine girildiğinde oyuncuya ek güç vermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>VisualInstance3D</strong></td>
        <td>3D sahneye görsel temsil eklemek için kullanılan node.</td>
        <td>Mesh, ışık veya parçacık gibi görsel nesneleri sahnede göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>GeometryInstance3D</strong></td>
        <td>3D geometrik objeleri sahnede temsil eden temel node.</td>
        <td>Mesh, MultiMesh veya diğer geometrik nesneleri sahnede göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>SpriteBase3D</strong></td>
        <td>3D ortamda 2D sprite'lar göstermek için temel node.</td>
        <td>Billboard tarzı nesneleri (örn: ağaç veya karakter simgeleri) 3D ortamda göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>AnimatedSprite3D</strong></td>
        <td>3D ortamda animasyonlu 2D sprite göstermek için kullanılır.</td>
        <td>Bir karakterin 2D animasyonlu bir yüzünü göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Sprite3D</strong></td>
        <td>3D ortamda basit bir 2D sprite göstermek için kullanılır.</td>
        <td>Bilgisayar oyunlarında UI elemanları olarak veya basit işaretçiler göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CPUParticles3D</strong></td>
        <td>CPU üzerinde çalışan 3D parçacık efektleri oluşturmak için kullanılır.</td>
        <td>Patlama veya duman efektleri gibi performans açısından hafif parçacık efektleri gerektiğinde kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CSGShape3D</strong></td>
        <td>Constructive Solid Geometry (CSG) kullanarak 3D şekiller oluşturmak için kullanılan temel node.</td>
        <td>Sahne içinde dinamik olarak duvar, zemin veya başka yapılar oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CSGBox3D</strong></td>
        <td>CSG tabanlı 3D kutu oluşturur.</td>
        <td>Sahne içinde kutu şeklinde bir yapı veya engel oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CSGCylinder3D</strong></td>
        <td>CSG tabanlı 3D silindir oluşturur.</td>
        <td>Kolon veya benzeri yapılar oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CSGTorus3D</strong></td>
        <td>CSG tabanlı 3D torus (halka) oluşturur.</td>
        <td>Halka şeklinde engeller veya dekoratif yapılar oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>MeshInstance3D</strong></td>
        <td>3D sahnede bir mesh gösterir.</td>
        <td>Bina, araç veya herhangi bir 3D objeyi sahnede görünür kılmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>MultiMeshInstance3D</strong></td>
        <td>Aynı tipte çoklu 3D mesh'leri verimli bir şekilde sahnede göstermek için kullanılır.</td>
        <td>Bir ormandaki ağaçların, kalabalık bir alanın veya taşların çoklu gösterimi için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Decal</strong></td>
        <td>3D yüzeylere resim veya dokular ekler.</td>
        <td>Duvarlara grafiti veya zemine kan lekesi gibi efektler eklemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Light3D</strong></td>
        <td>3D ortamda sahneye ışık veren temel node.</td>
        <td>Sahnedeki aydınlatma ihtiyacına göre güneş ışığı, nokta ışığı veya spot ışık olarak kullanılır.</td>
        </tr>
        <tr>
        <td><strong>DirectionalLight3D</strong></td>
        <td>Tüm sahneye bir yönden gelen ışık kaynağı ekler (güneş ışığı gibi).</td>
        <td>Geniş dış mekan sahnelerinde güneş ışığını simüle etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>OmniLight3D</strong></td>
        <td>Tüm yönlere ışık veren 3D ışık kaynağı.</td>
        <td>Oda içinde bir ampulün ışığını simüle etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>SpotLight3D</strong></td>
        <td>Belirli bir koniden gelen ışık kaynağı oluşturur.</td>
        <td>Tiyatro sahnesi veya araba farı gibi belirli bir alanı aydınlatmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>FogVolume</strong></td>
        <td>3D sahnede belirli bir alan içinde sis efekti oluşturur.</td>
        <td>Karanlık bir orman veya mağara atmosferi oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>GPUParticlesAttractor3D</strong></td>
        <td>GPU üzerinde çalışan ve belirli bir noktaya parçacıkları çeken node.</td>
        <td>Patlama sonrasında partiküllerin belirli bir noktaya toplanması gibi efektler oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>GPUParticlesAttractorBox3D</strong></td>
        <td>Bir kutu şeklindeki alanda GPU tabanlı parçacıkları çeken node.</td>
        <td>Belirli bir kutu hacmine parçacıkları çekmek ve belirli bir alan içindeki parçacık yoğunluğunu artırmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>GPUParticlesAttractorSphere3D</strong></td>
        <td>Bir küre şeklindeki alanda GPU tabanlı parçacıkları çeken node.</td>
        <td>Küre biçiminde bir alana parçacıkları toplamak, örneğin bir enerji küresi etrafında parçacık yoğunluğu oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>GPUParticlesAttractorVectorField3D</strong></td>
        <td>Vektör alanına dayalı olarak parçacıkları çeken ve hareket ettiren node.</td>
        <td>Parçacıkların karmaşık bir vektör alanına göre hareket etmesini sağlamak, örneğin rüzgar veya manyetik alan etkisini simüle etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>GPUParticlesCollision3D</strong></td>
        <td>GPU tabanlı parçacıkların belirli yüzeylerle çarpışmasını sağlar.</td>
        <td>Kar veya yağmur damlalarının zeminle çarpışması gibi efektlerin oluşturulması için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>GPUParticlesCollisionBox3D</strong></td>
        <td>Kutularla GPU tabanlı parçacıkların çarpışmasını sağlayan node.</td>
        <td>Parçacıkların bir kutu yüzeyine çarptığında tepki vermesini sağlamak, örneğin parçacıkların bir duvarla etkileşimi için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>GPUParticlesCollisionSphere3D</strong></td>
        <td>Küre ile GPU tabanlı parçacıkların çarpışmasını sağlayan node.</td>
        <td>Parçacıkların küre yüzeyine çarptığında tepki vermesini sağlamak, örneğin su damlacıklarının bir küreyle etkileşimi için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>GPUParticlesCollisionVectorField3D</strong></td>
        <td>Vektör alanı ile parçacıkların çarpışmasını ve davranışını etkileyen node.</td>
        <td>Karmaşık yüzeylerle veya alanlarla etkileşim gerektiren partikül simülasyonları, örneğin rüzgar yönüne göre savrulma için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>LightmapGI</strong></td>
        <td>Sahne aydınlatmasını daha verimli hale getirmek için ışık haritalarını kullanır.</td>
        <td>Daha büyük sahnelerde performansı artırarak önceden hesaplanmış ışıklandırma efektlerini uygulamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>OccluderInstance3D</strong></td>
        <td>Işık ve gölgelerin hesaplanmasında sahneyi gizlemek ve optimize etmek için kullanılan node.</td>
        <td>Görsel performansı iyileştirmek için büyük sahnelerde belirli objeleri gizlemek amacıyla kullanılır.</td>
        </tr>
        <tr>
        <td><strong>ReflectionProbe</strong></td>
        <td>Sahne içindeki yansımaları daha doğru ve gerçekçi göstermek için kullanılan node.</td>
        <td>Su yüzeyi veya parlak metal objelerde doğru yansımalar elde etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>RootMotionView</strong></td>
        <td>Karakter animasyonlarının kök hareketlerini sahnede görselleştiren node.</td>
        <td>Karakter animasyonlarının sahnede nasıl yer değiştirdiğini analiz etmek ve kök hareketlerini ayarlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>VisibleOnScreenNotifier3D</strong></td>
        <td>3D nesnenin ekranda görünüp görünmediğini algılayan ve buna göre bir sinyal gönderen node.</td>
        <td>Belirli bir nesne ekranda görünüyorsa animasyon veya diğer işlemleri başlatmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>VisibleOnScreenEnabler3D</strong></td>
        <td>3D nesne ekranda göründüğünde belirli işlevlerin etkinleştirilmesini sağlayan node.</td>
        <td>Performans amacıyla, ekranda olmadığında düşmanın davranışını durdurmak veya optimize etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>VoxelGI</strong></td>
        <td>Global illumination (küresel aydınlatma) hesaplamalarını daha hassas ve doğru hale getiren node.</td>
        <td>Büyük sahnelerde doğru ışık yayılımı ve yansıma efektleri oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>AudioListener3D</strong></td>
        <td>3D dünyasında seslerin hangi açıdan ve uzaklıktan duyulacağını belirleyen node.</td>
        <td>Oyuncunun karakterine göre seslerin uzaktan veya yakından duyulma şeklini simüle etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>AudioStreamPlayer3D</strong></td>
        <td>3D ortamda ses dosyalarını oynatmak için kullanılan node.</td>
        <td>Belirli bir objeye yaklaştıkça duyulacak ses efektleri oluşturmak için kullanılır (örneğin: su sesi veya ateş sesi).</td>
        </tr>
        <tr>
        <td><strong>BoneAttachment3D</strong></td>
        <td>3D bir mesh'in kemiklerine belirli nesneleri eklemek için kullanılır.</td>
        <td>Bir karakterin eline kılıç veya kalkan eklemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Camera3D</strong></td>
        <td>3D sahne içinde belirli bir bakış açısını göstermek için kullanılan kamera.</td>
        <td>Birinci veya üçüncü şahıs kamera görünümünde sahneyi izlemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>XRCamera3D</strong></td>
        <td>VR destekli uygulamalarda kullanıcının bakış açısını izlemek için kullanılan kamera.</td>
        <td>VR deneyimlerinde kullanıcının bakış açısını takip etmek ve ona uygun görüntü sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CollisionPolygon3D</strong></td>
        <td>3D çarpışmalar için çokgen şekli tanımlayan node.</td>
        <td>Karmaşık 3D yüzeyler veya objeler için çarpışma sınırları oluşturmak için kullanılır (örneğin: bina duvarları).</td>
        </tr>
        <tr>
        <td><strong>CollisionShape3D</strong></td>
        <td>Basit 3D çarpışma şekli tanımlamak için kullanılan node.</td>
        <td>Karakterlerin veya nesnelerin çarpışma sınırlarını belirlemek için kullanılır (örneğin: küre veya kutu çarpışmaları).</td>
        </tr>
        <tr>
        <td><strong>Joint3D</strong></td>
        <td>3D fiziksel nesneler arasında bağlantı sağlamak için kullanılan temel node.</td>
        <td>İki nesne arasındaki fiziksel bağı belirlemek, örneğin robot kollarında bağlantı noktası oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>ConeTwistJoint3D</strong></td>
        <td>Konik bir hareket aralığında iki 3D fiziksel nesne arasındaki esnek bağlantıyı sağlar.</td>
        <td>Bir karakterin omuz eklemi gibi, belirli açılar arasında serbestçe dönebilen bağlantılar için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Generic6DOFJoint3D</strong></td>
        <td>Altı serbestlik derecesine sahip, bir eksen boyunca dönebilme ve kayabilme özelliği olan bir bağlantı sağlar.</td>
        <td>Bir araç süspansiyon sistemi oluşturmak için kullanılır ve hareketin sınırlandırılmasını sağlar.</td>
        </tr>
        <tr>
        <td><strong>HingeJoint3D</strong></td>
        <td>Belirli bir eksen etrafında dönme hareketi sağlayan bir eklem oluşturur.</td>
        <td>Kapı menteşesi veya çark gibi dönebilme özelliği gerektiren mekanizmalar oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>PinJoint3D</strong></td>
        <td>İki 3D fiziksel nesneyi sabit bir noktada birleştiren node.</td>
        <td>Bir halat veya zincir bağlantısı oluşturmak için kullanılır, böylece belirli bir noktadan serbestçe dönebilir.</td>
        </tr>
        <tr>
        <td><strong>SliderJoint3D</strong></td>
        <td>Bir eksen boyunca kayma hareketi yapabilen bir bağlantı oluşturur.</td>
        <td>Kapıların ray üzerinde kayarak açılmasını simüle etmek için kullanılır (örneğin: depo kapıları).</td>
        </tr>
        <tr>
        <td><strong>GridMap</strong></td>
        <td>3D dünyada döşemeler ve bloklardan oluşan bir harita oluşturmak için kullanılan node.</td>
        <td>Minecraft benzeri bir oyun haritası veya yapı bloklarıyla sahne oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>ImporterMeshInstance3D</strong></td>
        <td>Harici kaynaklardan (örneğin, .glb, .obj dosyalarından) alınan 3D mesh'leri sahnede göstermek için kullanılır.</td>
        <td>Dışarıdan modelleme araçlarıyla oluşturulmuş 3D objeleri doğrudan sahneye eklemek için kullanılır (örneğin: Blender'dan alınan bir bina modeli).</td>
        </tr>
        <tr>
        <td><strong>LightmapProbe</strong></td>
        <td>Sahne aydınlatmasını optimize etmek ve ışık hesaplamalarını verimli hale getirmek için kullanılan node.</td>
        <td>Büyük ve detaylı sahnelerde ışık haritalarını kullanarak performans iyileştirmesi sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Marker3D</strong></td>
        <td>Geliştiriciler için sahnede özel bir işaretçi olarak kullanılan ve işleme yapılmayan node.</td>
        <td>Karakterin başlangıç pozisyonunu veya önemli bir noktayı işaretlemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>NavigationLink3D</strong></td>
        <td>3D navigasyon sistemi içinde iki navigasyon bölgesini birbirine bağlar.</td>
        <td>NPC'nin bir alandan diğerine sorunsuz bir şekilde geçiş yapmasını sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>NavigationObstacle3D</strong></td>
        <td>3D navigasyon yollarında bir engel oluşturarak, yol bulma hesaplamalarını etkileyen bir node.</td>
        <td>NPC'lerin belirli bir bölgeden geçiş yapmasını engellemek veya belirli bir rotadan yönlendirmek için kullanılır (örneğin: duvar veya kapı).</td>
        </tr>
        <tr>
        <td><strong>NavigationRegion3D</strong></td>
        <td>3D navigasyon sistemi içinde belirli bir bölgeyi tanımlayan node.</td>
        <td>NPC'nin belirli bir bölgede hareket edebilmesini veya bu bölge içinde yol bulmasını sağlamak için kullanılır (örneğin: bir odanın içi).</td>
        </tr>
        <tr>
        <td><strong>OpenXRCompositionLayer</strong></td>
        <td>VR ortamlarında ek bilgi veya katman eklemek için kullanılan node.</td>
        <td>VR oyunlarında veya uygulamalarında, kullanıcıya ek bilgi göstermek (örn: HUD veya kullanıcı arayüzü) için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>OpenXRCompositionLayerCylinder</strong></td>
        <td>VR ortamında silindir şeklinde bir kompozisyon katmanı ekleyen node.</td>
        <td>VR deneyimlerinde bir sütun etrafında sarılı bilgi veya reklam göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>OpenXRCompositionLayerEquiRect</strong></td>
        <td>VR ortamında ekvatoral olarak düzleştirilmiş bir kompozisyon katmanı ekleyen node.</td>
        <td>VR videolarının veya panoramik görüntülerin düzgün bir şekilde kullanıcıya gösterilmesi için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>OpenXRCompositionLayerQuad</strong></td>
        <td>VR ortamında dörtgen şeklinde bir kompozisyon katmanı ekleyen node.</td>
        <td>VR deneyiminde kullanıcıya ön planda bilgi veya reklam göstermek amacıyla kullanılır.</td>
        </tr>
        <tr>
        <td><strong>OpenXRHand</strong></td>
        <td>VR cihazında kullanıcının el hareketlerini izleyen node.</td>
        <td>Kullanıcının VR ortamında elleriyle yaptığı hareketleri izlemek ve bu hareketlere göre sahnedeki nesneleri yönetmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Path3D</strong></td>
        <td>3D ortamda bir yol tanımlayan node.</td>
        <td>Bir aracın veya karakterin önceden belirlenmiş bir rotayı izlemesi gerektiğinde kullanılır.</td>
        </tr>
        <tr>
        <td><strong>PathFollow3D</strong></td>
        <td>3D yolu takip eden bir node.</td>
        <td>Roller coaster gibi bir simülasyonda vagonların belirli bir patika üzerinde hareket etmesini sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>SkeletonModifier3D</strong></td>
        <td>3D karakter iskeletine çeşitli modifikasyonlar ekleyen ve düzenleyen node.</td>
        <td>Ters kinematik (IK) kullanarak karakterin kemiklerini ve animasyonlarını düzenlemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>PhysicalBoneSimulator3D</strong></td>
        <td>3D kemik yapısına fizik simülasyonu eklemek için kullanılır.</td>
        <td>Ragdoll fizik simülasyonu oluşturmak veya karakterlerin kemik yapılarını gerçekçi bir şekilde hareket ettirmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>SkeletonIK3D</strong></td>
        <td>Ters kinematik (IK) uygulayarak 3D iskeletin belirli hedeflere yönlendirilmesini sağlar.</td>
        <td>Bir karakterin belirli bir noktaya elini uzatmasını veya adım atmasını simüle etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>XRBodyModifier3D</strong></td>
        <td>VR kullanıcı vücut hareketlerini takip ederek çeşitli modifikasyonlar yapan node.</td>
        <td>Kullanıcının vücut hareketlerini VR sahnesinde nesnelere veya karakterlere uygulamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>XRHandModifier3D</strong></td>
        <td>VR ortamında kullanıcının el hareketlerini izleyen ve buna göre tepkiler veren node.</td>
        <td>Kullanıcının elleriyle VR ortamında çeşitli nesnelerle etkileşim kurmasını sağlamak amacıyla kullanılır.</td>
        </tr>
        <tr>
        <td><strong>RayCast3D</strong></td>
        <td>Belirli bir yönde çarpışma tespiti yaparak, ışın demetinin bir nesneye çarpıp çarpmadığını belirleyen node.</td>
        <td>Bir karakterin görüş hattını veya bir lazer ışını atıp atmadığını tespit etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>RemoteTransform3D</strong></td>
        <td>Belirli bir nesnenin konumunu başka bir nesneye göre kontrol etmeyi sağlayan node.</td>
        <td>Bir kameranın bir objeyi sürekli takip etmesini veya bir ışık kaynağının belirli bir nesneye göre konumlandırılmasını sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>ShapeCast3D</strong></td>
        <td>3D uzayda belirli bir şeklin bir doğrultuda çarpışma yapıp yapmadığını kontrol eden node.</td>
        <td>Bir engelin önceden tespit edilmesi veya bir hedefin varlığının belirlenmesi için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Skeleton3D</strong></td>
        <td>3D karakter animasyonları ve iskelet yapıları için kullanılan node.</td>
        <td>Bir karakter modeline kemik yapısı ekleyerek çeşitli animasyonlar oluşturmak için kullanılır (örneğin: yürüme animasyonu).</td>
        </tr>
        <tr>
        <td><strong>SpringArm3D</strong></td>
        <td>Kamera gibi nesneleri sahnede esnek bir şekilde yerleştiren ve diğer nesnelerle çarpışmasını engelleyen node.</td>
        <td>Bir üçüncü şahıs oyununda kamerayı otomatik olarak oyuncunun etrafında döndüren ve engellere çarpmamasını sağlayan bir sistem oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>VehicleWheel3D</strong></td>
        <td>Araç simülasyonlarında tekerleği temsil eden node.</td>
        <td>Bir araba veya başka bir araç modelinin tekerleklerinin fiziksel davranışını simüle etmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>XRNode3D</strong></td>
        <td>VR (Sanal Gerçeklik) cihazlarıyla ilgili konum ve rotasyon verilerini takip eden node.</td>
        <td>VR cihazında kullanıcı hareketlerini izlemek ve buna göre sahnedeki nesneleri yönetmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>XRAnchor3D</strong></td>
        <td>XR ortamında kullanıcının belirlediği referans noktaları oluşturur.</td>
        <td>Belirli bir VR sahnesinde nesnelerin veya objelerin sabit bir noktaya göre hizalanmasını sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>XRController3D</strong></td>
        <td>VR denetleyicisinin konum ve hareketlerini izleyen node.</td>
        <td>VR oyunlarında el kontrol cihazları ile etkileşim sağlamak amacıyla kullanılır; örneğin, objeleri almak veya sürüklemek için.</td>
        </tr>
        <tr>
        <td><strong>XRFaceModifier3D</strong></td>
        <td>VR kullanıcı yüz ifadelerini takip eden ve bu ifadeleri kullanarak sahne içinde tepki veren node.</td>
        <td>VR sosyal uygulamalarında kullanıcının yüz ifadelerini doğru şekilde göstermek veya animasyonlu karakterlerin yüz ifadelerini güncellemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>XROrigin3D</strong></td>
        <td>VR cihazının başlangıç noktasını tanımlayan node, kullanıcının pozisyonunu baz alır.</td>
        <td>VR deneyiminde kullanıcının başlangıç pozisyonunu ve sanal ortama giriş yaptığı noktayı belirlemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>AnimationMixer</strong></td>
        <td>Birden fazla animasyonun aynı anda karıştırılmasını ve oynatılmasını sağlayan node.</td>
        <td>Karakterin aynı anda yürüme ve ateş etme animasyonlarını karıştırarak doğal hareket oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>AnimationPlayer</strong></td>
        <td>Animasyonları çalmak ve yönetmek için kullanılan bir node.</td>
        <td>Karakter animasyonlarını, örneğin yürüme veya koşma animasyonlarını tetiklemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>AnimationTree</strong></td>
        <td>Karmaşık animasyon geçişlerini kontrol etmek için kullanılan node.</td>
        <td>Karakterin farklı animasyonlar arasında geçiş yapmasını sağlamak, örneğin yürümeden koşmaya geçiş için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>AudioStreamPlayer</strong></td>
        <td>Ses dosyalarını oynatmak için kullanılan temel node.</td>
        <td>Arka plan müziği veya belirli ses efektlerinin sahne içinde çalınması için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>CanvasLayer</strong></td>
        <td>Farklı UI elemanlarını veya efektleri organize etmek için kullanılan bir katman.</td>
        <td>HUD öğelerini veya ekran üstü efektleri ana sahneden ayrı tutarak yönetmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>ParallaxBackground</strong></td>
        <td>Kamera hareketine bağlı olarak birden fazla katmanın farklı hızlarda kaymasını sağlayarak derinlik hissi oluşturan node.</td>
        <td>Arka planda dağ veya gökyüzü gibi nesnelerin farklı hızlarda kaymasını sağlayarak 2D bir platform oyununda derinlik oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>HTTPRequest</strong></td>
        <td>HTTP istekleri yapmak ve sunucu ile veri alışverişi yapmak için kullanılan node.</td>
        <td>Oyun içi liderlik tablosunu güncellemek veya kullanıcı bilgilerini kaydetmek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>MultiplayerSpawner</strong></td>
        <td>Multiplayer oyunlarda belirli objelerin ağ üzerinde otomatik olarak oluşturulmasını sağlayan node.</td>
        <td>Savaş oyununda düşman karakterlerini diğer oyuncuların sahnelerinde oluşturmak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>MultiplayerSynchronizer</strong></td>
        <td>Multiplayer ortamında belirli nesnelerin senkronizasyonunu sağlayan node.</td>
        <td>Birden fazla oyuncunun aynı anda nesneler üzerinde değişiklik yapmasını sağlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>NavigationAgent2D</strong></td>
        <td>2D dünyada hareket eden nesnelerin yol bulma işlemlerini yöneten node.</td>
        <td>NPC karakterin oyuncuyu takip etmesi veya belirli bir hedefe yönlendirilmesi için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>NavigationAgent3D</strong></td>
        <td>3D dünyada hareket eden nesnelerin yol bulma işlemlerini yöneten node.</td>
        <td>Düşmanın oyuncunun pozisyonuna göre otomatik olarak 3D dünyada hareket etmesi için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>ResourcePreloader</strong></td>
        <td>Gerekli kaynakları önceden yükleyerek performans optimizasyonu sağlayan node.</td>
        <td>Oyunun belirli bir sahnesine geçmeden önce gerekli olan tüm ses, görsel ve sahne kaynaklarını yüklemek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>ShaderGlobalsOverride</strong></td>
        <td>Shader'ların kullandığı küresel sabitleri değiştirmek için kullanılan node.</td>
        <td>Belirli bir sahnede özel ışıklandırma veya gölgelendirme ayarları uygulamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>StatusIndicator</strong></td>
        <td>Oyuncunun veya nesnenin durumu hakkında bilgi veren bir UI öğesi.</td>
        <td>Oyuncunun sağlık durumunu veya görev ilerlemesini göstermek için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>Timer</strong></td>
        <td>Belirli bir süre sonrasında bir sinyal gönderen node.</td>
        <td>Belirli aralıklarla düşman dalgalarını başlatmak veya animasyonları zamanlamak için kullanılır.</td>
        </tr>
        <tr>
        <td><strong>WorldEnvironment</strong></td>
        <td>Işık, gölgelendirme ve diğer küresel çevre efektlerini kontrol eden node.</td>
        <td>Sahnenin genel atmosferini değiştirmek, örneğin gün doğumu, gece efekti veya sis eklemek için kullanılır.</td>
        </tr>
    </tbody>
</table>
