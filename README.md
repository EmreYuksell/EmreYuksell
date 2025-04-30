Akademik Personel Alım Sistemi
Bu proje, üniversitelerin akademik personel alım süreçlerini dijitalleştirmek amacıyla geliştirilmiş bir web tabanlı uygulamadır. Başvuru süreçleri, jüri atamaları, dosya kontrolü ve mülakat değerlendirmeleri gibi adımlar tek bir platformda toplanmıştır. Sistem, React.js ile frontend, Node.js ile backend, MongoDB ile veritabanı, AWS S3 ile dosya saklama ve JWT ile kimlik doğrulama kullanarak geliştirilmiştir.

İçindekiler
Proje Tanımı

Teknolojiler

Kurulum

Kullanım

Proje Yapısı

Çevresel Değişkenler

Geliştirici Notları

Katkıda Bulunma

Lisans

Proje Tanımı
Akademik Personel Alım Sistemi, üniversite akademik kadrosu için başvuru sürecini dijital ortamda yönetmek amacıyla tasarlanmıştır. Adaylar başvurularını online olarak yapar, başvuruların değerlendirilmesi ve mülakat süreci ise sistem üzerinden gerçekleştirilir. Bu süreçleri kolaylaştıran ve şeffaf hale getiren sistem, yönetici, jüri ve aday gibi farklı rollerin kullanımına açıktır.

Teknolojiler
Frontend: React.js, Ant Design

Backend: Node.js, Express.js

Veritabanı: MongoDB

Kimlik Doğrulama: JWT (JSON Web Token)

Dosya Yükleme: AWS S3

Çevre Değişkenleri Yönetimi: dotenv

API İletişimi: Axios

Tarih ve Saat İşlemleri: Dayjs

Diğer Araçlar: Mongoose, Multer, CORS

Kurulum
Gereksinimler
Node.js ve npm (Node Package Manager) yüklü olmalıdır.

MongoDB ve AWS S3 hesap bilgilerine sahip olmanız gerekir.

Adım 1: Projeyi Klonlayın
Öncelikle projeyi GitHub'dan klonlayın:

bash
Kopyala
Düzenle
git clone https://github.com/your-username/akademik-personel-alim-sistemi.git
Adım 2: Bağımlılıkları Yükleyin
Projenin kök dizininde aşağıdaki komutu çalıştırarak gerekli bağımlılıkları yükleyin:

bash
Kopyala
Düzenle
npm install
Adım 3: Çevresel Değişkenleri Yapılandırın
.env dosyasını kök dizine ekleyin ve aşağıdaki gibi çevresel değişkenlerinizi yapılandırın:

env
Kopyala
Düzenle
ATLAS_URI=mongodb+srv://<your-mongo-db-uri>
PORT=3000
AWS_ACCESS_KEY_ID=<your-aws-access-key-id>
AWS_SECRET_ACCESS_KEY=<your-aws-secret-access-key>
AWS_REGION=<your-aws-region>
AWS_BUCKET_NAME=<your-s3-bucket-name>
JWT_SECRET=<your-jwt-secret>
Adım 4: MongoDB ve AWS S3 Hesapları
MongoDB için bir MongoDB Atlas hesabı oluşturun ve veritabanınızı oluşturun.

AWS için bir S3 bucket oluşturun ve gerekli erişim bilgilerini .env dosyasına ekleyin.

Adım 5: Uygulamayı Başlatın
Uygulamayı başlatmak için aşağıdaki komutu çalıştırabilirsiniz:

bash
Kopyala
Düzenle
npm start
Bu komut hem frontend'i hem de backend'i başlatacaktır. Frontend uygulamanız http://localhost:3000 adresinde çalışacak, backend ise belirtilen port üzerinde aktif olacaktır.

Kullanım
Kayıt Olun: Adaylar sistemdeki kayıt formu üzerinden kendilerini kaydedebilirler.

Başvuru Yapın: Adaylar başvuru formunu doldurarak akademik pozisyonlara başvuruda bulunabilirler.

Jüri Atamaları: Yönetici, jüri üyelerini atayabilir ve jüri üyeleri başvuruları inceleyebilir.

Mülakat ve Değerlendirme: Jüri üyeleri mülakatlar yaparak adayları değerlendirebilir.

Dosya Yükleme: Adaylar başvuru belgelerini AWS S3'ye yükleyebilirler.

Proje Yapısı
plaintext
Kopyala
Düzenle
├── client/                   # Frontend kaynakları
│   ├── public/               # Public dosyalar
│   ├── src/                  # React bileşenleri ve sayfalar
│   └── package.json          # Frontend bağımlılıkları
│
├── server/                   # Backend kaynakları
│   ├── controllers/          # API controller'ları
│   ├── models/               # MongoDB modelleri
│   ├── routes/               # API rotaları
│   └── server.js             # Express sunucu başlatma dosyası
│
├── .env                      # Çevresel değişkenler
├── package.json              # Proje bağımlılıkları
└── README.md                 # Bu dosya
Çevresel Değişkenler
Proje, aşağıdaki çevresel değişkenleri kullanır:

ATLAS_URI: MongoDB Atlas bağlantı URI'si.

PORT: Backend uygulamasının çalışacağı port.

AWS_ACCESS_KEY_ID: AWS S3 erişim anahtarı.

AWS_SECRET_ACCESS_KEY: AWS S3 gizli anahtarı.

AWS_REGION: AWS bölgesi.

AWS_BUCKET_NAME: AWS S3 bucket adı.

JWT_SECRET: JWT kimlik doğrulama anahtarı.

Geliştirici Notları
Uygulama, MongoDB veritabanı ve AWS S3 ile entegre çalışmaktadır. Geliştirme ve test sırasında bu servislere erişim sağlamalısınız.

Multer kütüphanesi, dosya yükleme işlemleri için kullanılır ve AWS S3 ile entegre edilir.

JWT, kullanıcı kimlik doğrulama için kullanılır ve sistemin güvenliğini sağlamak amacıyla her API isteğiyle birlikte gönderilir.

Katkıda Bulunma
Katkıda bulunmak isterseniz, aşağıdaki adımları izleyebilirsiniz:

Bu repoyu fork edin.

Yeni bir feature branch açın (git checkout -b feature-branch).

Değişikliklerinizi yapın ve commit edin (git commit -am 'Add new feature').

Branch'inizi push edin (git push origin feature-branch).

Pull request açın.

Lisans
Bu proje MIT lisansı altında lisanslanmıştır. Daha fazla bilgi için LICENSE dosyasına göz atabilirsiniz.
