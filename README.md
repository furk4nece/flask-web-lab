# Flask Web Lab

Flask kullanılarak geliştirilmiş bir web uygulaması.
Bu proje temel web geliştirme kavramlarını uygulamalı olarak göstermeyi amaçlar.

Routing vardır.
Veritabanı vardır.
Migration vardır.
Konfigürasyon ayrımı vardır.

## 🚀 Kullanılan Teknolojiler

- Python 3
- Flask
- Flask-Migrate
- SQLite
- HTML
- CSS
- Jinja2

## 📁 Proje Yapısı

flask-web-lab/
│
├── app/
│ ├── routes/
│ ├── models/
│ ├── templates/
│ ├── static/
│ └── init.py
│
├── migrations/
├── logs/
├── config.py
├── web_lab.py
├── .flaskenv
└── README.md


## ⚙️ Kurulum

```bash
git clone https://github.com/furk4nece/flask-web-lab.git
cd flask-web-lab
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

Windows:
venv\Scripts\activate

▶️ Çalıştırma
flask run

Tarayıcıdan aç:
http://127.0.0.1:5000

🗄️ Veritabanı

SQLite kullanır
Migration sistemi aktiftir
Local veritabanı GitHub’a dahil edilmez
flask db migrate -m "initial"
flask db upgrade
