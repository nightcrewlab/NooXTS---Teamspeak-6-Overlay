TS6 Modern Overlay

TeamSpeak 6 (TS6) için geliştirilmiş, Discord tarzı oyun algılama özelliğine sahip, modern ve minimalist bir kullanıcı arayüzü sunan masaüstü overlay uygulamasıdır.

Geliştirici: NooXRii

🚀 Özellikler

Modern Tasarım: Yuvarlatılmış köşeler, derin antrasit renk paleti ve akıcı görsel geri bildirimler.

Discord Tarzı Oyun Algılama: Overlay, sadece listedeki oyunlardan biri çalıştığında otomatik olarak görünür hale gelir. Oyun kapandığında kendini gizler.

Otomatik Kapanma: TeamSpeak 6 kapandığında overlay de sistem kaynaklarını yormamak için kendini otomatik olarak kapatır.

Akıllı Durum Takibi:

Konuşma Durumu: Konuşan kişiler yeşil bir parlamayla vurgulanır.

Mute (Susturma): Mikrofonu kapalı olan kişilerin yanında kırmızı bir simge belirir.

API Key Kayıt Sistemi: TeamSpeak 6'nın her açılışta izin sormasını engeller. İlk onaydan sonra API anahtarını yerel bir dosyada saklar.

Sistem Tepsisi (Tray) Desteği: Sağ alt köşedeki ikon üzerinden yönetilebilir, taşımayı etkinleştirebilir veya kapatabilirsiniz.

Performans Dostu: psutil ve websockets kullanarak düşük işlemci ve bellek kullanımı sağlar.

🛠 Kurulum

Python Yüklü Olmalıdır: Bilgisayarınızda Python 3.10 veya üzeri bir sürümün yüklü olduğundan emin olun.

Gerekli Kütüphaneler: Terminal veya CMD ekranını açarak aşağıdaki komutu çalıştırın:

pip install websockets psutil pystray Pillow


İkon Dosyası: Uygulamanın çalışması için dizinde tsoverlay.ico adında bir ikon dosyası bulunmalıdır (Eğer yoksa sistem varsayılan bir ikon oluşturur).

🎮 Kullanım

TeamSpeak 6'yı Açın: Remote Control API'nin aktif olduğundan emin olun.

Uygulamayı Çalıştırın:

python ts6_overlay.py


İzin Verin: İlk çalıştırmada TeamSpeak 6 içinde bir onay kutusu çıkacaktır. "Kabul Et" (Allow) seçeneğine tıklayın. Bu işlem bir kez yapılır.

Oyuna Girin: Overlay varsayılan olarak gizlidir. GAME_LIST içinde tanımlı bir oyuna (örneğin CS2, Valorant, Genshin vb.) girdiğinizde otomatik olarak belirecektir.

⚙️ Yapılandırma

ts6_overlay.py dosyası içindeki GAME_LIST değişkenine istediğiniz oyunların .exe isimlerini ekleyebilirsiniz:

GAME_LIST = [
    "cs2.exe", 
    "valorant.exe", 
    "genshinimpact.exe",
    # Buraya kendi oyunlarınızı ekleyebilirsiniz
]


📜 Lisans

Bu proje eğitim ve kişisel kullanım amacıyla geliştirilmiştir. Geliştirilmesine katkıda bulunmak için "Pull Request" gönderebilirsiniz.

NooXRii tarafından geliştirildi.
