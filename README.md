# Flask Web Lab

Bu proje, Python ve Flask web çatısı kullanılarak geliştirilmiş modüler yapıda bir web uygulamasıdır. Proje, ölçeklenebilir bir yapı sunan "Application Factory" tasarım desenini kullanmaktadır.

## 📂 Proje Yapısı

* `app/`: Uygulamanın ana kaynak kodlarını (modeller, rotalar, şablonlar) barındıran klasör.
* `migrations/`: Veritabanı şema değişikliklerini takip eden migrasyon dosyaları (Flask-Migrate).
* `web_lab.py`: Uygulamanın giriş noktası (Entry point).
* `config.py`: Uygulama konfigürasyon ve ortam ayarları.

## 🚀 Kurulum

Projeyi yerel makinenizde çalıştırmak için aşağıdaki adımları izleyin.

### 1. Projeyi Klonlayın

git clone [https://github.com/furk4nece/flask-web-lab.git](https://github.com/furk4nece/flask-web-lab.git)
cd flask-web-lab

### 2. Sanal Ortam (Virtual Environment) Oluşturun
Bağımlılıkları izole etmek için bir sanal ortam oluşturmanız önerilir.

Windows için:
python -m venv venv
venv\Scripts\activate

macOS / Linux için:
python3 -m venv venv
source venv/bin/activate

3. Gereksinimleri Yükleyin
Projede migrations klasörü bulunduğundan Flask'ın yanı sıra veritabanı araçlarına da ihtiyacınız olacaktır. Eğer repoda requirements.txt dosyası yoksa temel paketleri şu şekilde yükleyebilirsiniz:
pip install flask flask-sqlalchemy flask-migrate

⚙️ Yapılandırma
config.py dosyasındaki ayarların geçerli olduğundan emin olun. Gerekirse proje ana dizininde bir .env dosyası oluşturarak gizli anahtarları (SECRET_KEY) ve veritabanı URL'sini (DATABASE_URL) tanımlayabilirsiniz.

▶️ Uygulamayı Çalıştırma
Uygulamayı başlatmak için terminalde aşağıdaki komutları kullanabilirsiniz:

Yöntem 1: Flask Komutu ile
export FLASK_APP=web_lab.py
# Windows CMD için: set FLASK_APP=web_lab.py
# Windows PowerShell için: $env:FLASK_APP = "web_lab.py"
flask run

Yöntem 2: Python Komutu ile
python web_lab.py

🗄️ Veritabanı İşlemleri (Opsiyonel)
Eğer veritabanı modelinde değişiklik yaparsanız, değişiklikleri uygulamak için:
flask db migrate -m "Değişiklik açıklaması"
flask db upgrade
