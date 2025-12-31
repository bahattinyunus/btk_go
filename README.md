# 🚀 BTK Akademi - Go (Golang) Dili Kursu: Modern Mühendislik Yolculuğu

Merhaba değerli geliştirici dostum! Bu depo, Türkiye'nin dijital dönüşüm hamlesinin en önemli taşlarından biri olan [BTK Akademi](https://www.btkakademi.gov.tr/portal/course/go-ile-programlamaya-giris-12760) platformu üzerinden başarıyla tamamladığım **"Go ile Programlamaya Giriş"** kursu kapsamında ilmek ilmek işlediğim projeleri, deneysel çalışmaları ve yapısal örnekleri barındıran kapsamlı bir dijital kütüphanedir. "Go neymiş ya?" diye merak ediyorsan, doğru yerdesin. Bu repo; sadeliğin gücünü, hızın zarafetini ve modern sistem programlamanın en saf halini keşfetmek isteyenler için bir başucu kaynağı niteliği taşır.

Bu çalışma; sadece sözdizimi (syntax) öğrenmenin ötesine geçerek, bir dilin felsefesini kavramayı, bellek yönetimini optimize etmeyi ve yüksek performanslı sistemler inşa etmeyi hedefleyen bir disiplinin ürünüdür. İster Go diline yeni başlayan bir meraklı ol, ister "Ben ne yazsam da kendimi geliştirsem?" diyen bir profesyonel; buradaki her satır kod, bir problem-çözüm döngüsünün ve pedagojik bir yaklaşımın sonucudur. Kodları incele, değiştir, boz ve yeniden inşa et; zira gerçek öğrenme ancak "terminalin başında ter dökerek" gerçekleşir.

---

## 🔍 Go (Golang) Nedir?

Go (aka **Golang**), 2007'de Google tarafindan yazilim dunyasinin en kronik sikayetlerini cozmek icin dogdu. 2009'da open-source yapildi, 2012'de 1.0 ile olgunluga erdi. "Statik tipli ama okuması kolay bir dil yazalim, C gibi hizli olsun ama JavaScript kadar basit dursun" kafasiyla gelistirildi.

### Neden bu kadar seviliyor? Çünkü:

* 🚀 **Işık hızında derleme & calistirma**
* 🔄 **Goroutine + Channel** ile native concurrency destegi
* 🧼 Sade, temiz ve okunabilir syntax (tipki IKEA mobilyası gibi: az parça, bol iş)
* 🛠 Gömülü toolchain: `go fmt`, `go test`, `go doc`, her şey kutudan çıkar çıkmaz hazır
* ⚙️ Docker, Kubernetes gibi dev sistemlerin dili — altyapının temel taşı!

---

## 🎯 Vizyon ve Misyon

Bu depo sadece bir kod koleksiyonu değil, aynı zamanda bir **modern mühendislik manifestosu**'dur. Temel amacımız:
- **� Şeffaflık**: Kodun nasıl çalıştığını en derin detayına kadar göstermek.
- **🛠 Pratiklik**: Teorik bilgiyi doğrudan çalışan kod bloklarına dönüştürmek.
- **📈 Gelişim**: Her adımda üzerine katarak daha karmaşık sistemler tasarlamak.

---

## 🏗️ Gelişmiş Mimari Analizi: Katmanlı Öğrenme Modeli

Projelerimiz, yazılım mühendisliğinin temel prensiplerine sadık kalarak, birbirini besleyen dört ana katman üzerinde yükselmektedir. Bu hiyerarşik yapı, karmaşık sistemlerin nasıl atomik parçalardan oluştuğunu anlamamızı sağlar:

1.  **Fundamental Layer (Temel Katman)**: Değişken deklarasyonları, statik veri tipleri ve Go'nun kendine has sözdizimi kurallarının temellerinin atıldığı katmandır.
2.  **Logic Layer (Mantıksal Katman)**: Algoritmik düşüncenin vücut bulduğu; if-else blokları, switch-case yapıları ve verimli döngü yönetimiyle kontrol akışının sağlandığı katmandır.
3.  **Data & Object Layer (Veri ve Nesne Katmanı)**: Struct'lar, method'lar ve interface'ler aracılığıyla nesne yönelimli benzeri (composition-based) modellemelerin yapıldığı, verinin optimize edildiği katmandır.
4.  **Concurrency & Distributed Layer (Eşzamanlılık ve Dağıtık Mimari)**: Go'nun asıl gücü olan asenkron işlemlerin, kanal yönetiminin ve modern ağ (network) bileşenlerinin inşa edildiği "ustalık" katmanıdır.

---

## �📁 Proje Klasörleri

```bash
.
├── 01-Temel-Kavramlar/         # Değişkenler, veri tipleri, operatörler
├── 02-Kosullar-Donguler/       # if-else, switch-case, for döngüleri
├── 03-Fonksiyonlar/            # Parametreli ve döndüren fonksiyonlar
├── 04-Veri-Yapilari/           # Dizi, slice, map kullanımı
├── 05-Struct-Interface/        # Struct ve interface tanımları
├── 06-GoRoutines-Channels/     # Eşzamanlılık örnekleri
├── 07-Web-Uygulamalari/        # Basit HTTP sunucusu ve API örnekleri
└── README.md
```

Her klasor, konuyla ilgili minik ama ogretici ornekler icerir. Yaz, calistir, oyna, boz, tekrar yaz. Yazilim boyle ogrenilir!

---

## 🧠 Öne Çıkan Teknik Konular ve Uygulamalar

### ✅ Nesne Modelleme ve Veri Yapıları (Struct & Maps)
Go'da nesne yönelimli programlama, karmaşık class hiyerarşileri yerine **composition** ve **struct** yapıları üzerine kuruludur. Bu, kodun daha esnek ve okunabilir olmasını sağlar.

```go
// Person, bir bireyi temsil eden veri modelidir.
type Person struct {
    Name string
    Age  int
}

// Map kullanarak hızlı veri erişimi sağlama:
var ages = map[string]int{"Ali": 25, "Veli": 30}
```

### ✅ Polimorfizm ve Arayüzler (Interfaces)
Arayüzler, Go'nun en güçlü silahlarından biridir. "Ne olduğu" ile değil, "ne yapabildiği" ile ilgilenir. Bu prensip (Duck Typing), modülerliği maksimize eder.

```go
func Topla(a int, b int) int {
    return a + b
}

// Hayvan arayüzü, SesCikar yeteneğine sahip her türü kapsar.
type Hayvan interface {
    SesCikar() string
}
```

### ✅ Eşzamanlılık ve İletişim (Goroutines & Channels)
Go'nun mottosu: "Hafıza paylaşarak iletişim kurma, iletişim kurarak hafıza paylaş!" (Don't communicate by sharing memory; share memory by communicating).

```go
go yazdir("Merhaba Asenkron Dünya") // Hafif siklet thread (Goroutine)

ch := make(chan string) // Veri transfer tüneli (Channel)
ch <- "veri transferi başlatıldı"
msg := <-ch
```

### ✅ Modern Web Mimarisi (HTTP Server)
Go'nun standart kütüphanesi o kadar güçlüdür ki, herhangi bir framework (Gin, Echo vb.) kullanmadan bile yüksek performanslı microservice'ler yazabilirsiniz.

```go
package main

import (
	"fmt"
	"net/http"
)

func home(w http.ResponseWriter, r *http.Request) {
	fmt.Fprintln(w, "BTK Go Sunucusuna Hoş Geldiniz!")
}

func main() {
	http.HandleFunc("/", home)
	// 8080 portunda dinlemeye hazırız
	http.ListenAndServe(":8080", nil)
}
```

Tarayıcınızı açıp `http://localhost:8080` adresine gittiğinizde, Go'nun mikrosaniyelik yanıt hızını bizzat deneyimleyeceksiniz.

---

## 🛠 Kurulum ve Geliştirme Ortamı

Projenin bir kopyasını yerel makinenizde çalıştırmak ve deneysel eklemeler yapmak için şu adımları izleyebilirsiniz:

1.  **Go Runtime Edinimi**: [Go resmi indirme sayfasından](https://go.dev/dl/) işletim sisteminize (Windows, macOS, Linux) uygun paketi kurun.
2.  **Repoyu Klonlama**: Terminalinizi açın ve `git clone` komutuyla projeyi indirin.
3.  **Çalıştırma ve Deneyimleme**:
    Herhangi bir alt klasöre girin ve Go derleyicisinin gücünü test edin:

    ```bash
    cd 01-Temel-Kavramlar/
    go run main.go
    ```

Go'nun mottosu olan *"Simple, Reliable, Efficient"* (Basit, Güvenilir, Verimli) prensibini her komutta hissedeceksiniz. Kurulum esnasında bir sorun yaşarsanız, Go'nun dokümantasyonu dünyadaki en temiz kaynaklardan biridir.

---

## 🌍 Go ile Geliştirilen Dev Projeler

| Proje          | Açıklama                                       |
| -------------- | ---------------------------------------------- |
| **Docker**     | Container teknolojisinin öncüsü                |
| **Kubernetes** | Modern uygulama orkestrasyonu                  |
| **Terraform**  | Altyapı yönetimi (infrastructure as code)      |
| **Hugo**       | Static site generator (blog yazarları bayılır) |
| **Caddy**      | Otomatik SSL destekli web sunucusu             |

Go'nun gücü sadece yazılımda değil; internetin yapı taşlarını taşır hale geldi.

---

## 💡 Neden Go ile Geleceği İnşa Etmelisin?

Modern yazılım ekosisteminde Go öğrenmek, sadece yeni bir dil bilmek değil, aynı zamanda bulut bilişimin "anahtarını" elinde tutmak demektir:

* 👶 **Sıfır Sürtünme**: Yeni başlayanlar için inanılmaz kolay, kıdemli mühendisler içinse şaşırtıcı derecede güçlüdür.
* 🧵 **Doğuştan Ölçeklenebilir**: Native concurrency sayesinde, CPU çekirdeklerini en verimli kullanan dillerin başında gelir.
* 👑 **Kurumsal Güvence**: Google tarafından destekleniyor olması, dilin uzun ömürlü ve güvenli bir yatırım olduğunu garantiler.
* 📦 **Statik Binary**: Tüm bağımlılıkları tek bir dosya içine gömer. Hedef sunucuda Go yüklü olmasına bile gerek kalmadan çalışır!
* 🧘‍♂️ **Mühendislik Hijyeni**: "Tek bir doğru yol vardır" felsefesiyle, farklı geliştiricilerin yazdığı kodların bile aynı elden çıkmış gibi görünmesini sağlar.

> *"Go, 21. yüzyılın sistem programlama dili olarak, karmaşıklığı ortadan kaldıran ve verimliliği kutsayan bir sanat eseridir."*

---

## 🛣️ Yol Haritası (Strategic Roadmap)

Öğrenim sürecimiz statik değildir; gelişen teknolojiyle birlikte depomuzu da güncel tutmayı hedefliyoruz:

- [ ] **🚀 GORM Entegrasyonu**: Veritabanı yönetiminde profesyonel bir yaklaşım sergileyerek PostgreSQL/MySQL bağlantıları kurmak.
- [ ] **🐳 Containerization (Docker)**: Go uygulamalarını container ortamına taşıyarak mikroservis mimarisine ilk adımı atmak.
- [ ] **🧪 Advanced Testing**: Unit testlerin ötesine geçerek benchmark'lar ve entegrasyon testleriyle kod stabilitesini maksimize etmek.
- [ ] **🛰️ gRPC & Protobuf**: REST'in ötesine geçerek, servisler arası ultra hızlı iletişim protokollerini deneyimlemek.

---

## ❓ Sıkça Sorulan Sorular (FAQ) - Meraklısına Yanıtlar

**S: Go gerçekten bu kadar hızlı mı?**  
C: Evet. C++ kadar hızlı olmaya odaklanan ancak derleme süresi ve geliştirme kolaylığı açısından Python konforu sunan nadir dillerden biridir.

**S: Pointers (İşaretçiler) korkutucu mu?**  
C: Hayır! Go, işaretçilerin gücünü (performans) korurken akıllı çöp toplama (Garbage Collection) mekanizmasıyla C'deki gibi bellek kaçakları (memory leaks) riskini minimize eder.

**S: Kurumsal dünyada iş imkanı nedir?**  
C: Günümüzde büyük ölçekli şirketlerin (Netflix, Uber, Dropbox, Google) altyapı ekiplerinin neredeyse tamamı Go developer aramaktadır. Bulut bilişimin yükselişiyle Go, en çok talep gören diller listesinde zirveye oynamaktadır.

---

## 📚 Derinlemesine Öğrenim Materyalleri

Eğer bu depodaki örnekler seni heyecanlandırdıysa, yolculuğuna şu devasa kaynaklarla devam edebilirsin:

- [🎮 A Tour of Go](https://tour.golang.org/) - Dilin yaratıcılarından interaktif ve eğlenceli bir başlangıç.
- [💡 Go by Example](https://gobyexample.com/) - Pratik odaklı, açıklayıcı ve temiz kod örnekleri.
- [📐 Effective Go](https://golang.org/doc/effective_go.html) - "Go gibi düşünmek" isteyenler için mutlaka okunması gereken bir başyapıt.

---

## 🤝 Katkıda Bulunmak İstersen

Bu repo eğitim amaçlıdır. Sen de projelere katkı sağlamak, farklı çözümler eklemek veya yorum yapmak istersen forkla, kodunu yaz, PR gönder. Açık kaynak ruhu yaşasın! 🙌

---

## 👤 Geliştirici Profilimiz / Professional Insights

**Bahattin Yunus Çetin**  
*Strategic IT Architect | Computer Science Scholar (Of, Trabzon)*

BTK Akademi Go Dili serüvenindeki tüm başarılarımı, teknik kazanımlarımı ve karşılaştığım mühendislik zorluklarını bu yaşayan depoda belgeliyorum. Teknoloji ekosistemine katkı sağlamak, ağımı genişletmek ve modern çözümler üzerine beyin fırtınası yapmak için her zaman hazırım.

---

### 🔗 Küresel İletişim & Ağ Yönetimi

[![GitHub Portfolio](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/bahattinyunus)
[![LinkedIn Professional](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/bahattinyunus/)

---

> *"Kodun her zaman temiz, derleyicin hatasız ve asenkron kanalların her daim açık olsun!"*

README dokümantasyonunun sonuna geldiysen, Go'nun büyülü dünyasına girmek için artık tamamen hazırsın demektir. Şimdi terminali aç, `go run` yaz ve dijital evreni Go ile şekillendirmeye başla! 🧑‍💻🚀
