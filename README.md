#  BTK Akademi - Go (Golang) Dili Kursu Projeleri

Merhaba yazılımcı dostum! Bu repo, [BTK Akademi](https://www.btkakademi.gov.tr/portal/course/go-ile-programlamaya-giris-12760) uzerinden tamamladigim **Go ile Programlamaya Giriş** kursu kapsaminda gelistirdigim proje ve ornekleri barindiriyor. "Go neymis ya" diyorsan, iceri gir bir bak: sade, hizli, guclu.

Go diline yeni baslayanlar, "Ben ne yazsam?" diyenler ya da "Sadece run edip calissin yeter" kafasinda olanlar icin birebir.

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

## 🏗️ Gelişmiş Mimari Analizi

Projelerimiz şu temel katmanlar üzerinde yükselmektedir:
1.  **Fundamental Layer**: Değişkenler ve temel sözdizimi.
2.  **Logic Layer**: Koşullu ifadeler ve döngüsel algoritmalar.
3.  **Data Layer**: Struct'lar ve complex veri tipleri ile veri yönetimi.
4.  **Concurrency Layer**: Go'nun gücünü yansıtan eşzamanlı çalışma modelleri.

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

## 🧠 Öne Çıkan Konular

### ✅ Veri Yapıları

```go
type Person struct {
    Name string
    Age  int
}

var ages = map[string]int{"Ali": 25, "Veli": 30}
```

### ✅ Fonksiyonlar ve Arayüzler (Interfaces)

```go
func Topla(a int, b int) int {
    return a + b
}

type Hayvan interface {
    SesCikar() string
}
```

### ✅ Goroutine ve Channel Kullanımı

```go
go yazdir("Merhaba") // eşzamanlı çalışır

ch := make(chan string)
ch <- "veri"
msg := <-ch
```

### ✅ Basit Web Sunucusu

```go
package main

import (
	"fmt"
	"net/http"
)

func home(w http.ResponseWriter, r *http.Request) {
	fmt.Fprintln(w, "Merhaba Go dünyası!")
}

func main() {
	http.HandleFunc("/", home)
	http.ListenAndServe(":8080", nil)
}
```

Tarayıcıya `http://localhost:8080` yaz, Go seni selamlasın 👋

---

## 🛠 Kurulum ve Kullanım

1. [Go resmi sitesi](https://go.dev/dl/) üzerinden sistemine uygun Go sürümünü indir.
2. Terminalde proje klasorune gir.
3. Calistirmak icin:

```bash
cd 01-Temel-Kavramlar/
go run main.go
```

Hepsi bu. Derlenir, calisir, patlamaz. Go'nun mottosu: "simple, reliable, efficient" — cok iddiali ama dogru.

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

## 💡 Neden Go Öğrenmelisin?

* 👶 Yeni başlayanlar için basit, kıdemliler için sağlam
* 🧵 Native concurrency ile çoklu işlemde uçuyor
* 👑 Google destekli: uzun ömürlü ve güvenli bir yatırım
* 📦 Tek binary ile dağıtım: dependency bağımlılığı derdi yok
* 🧘‍♂️ "Keep it simple" felsefesini iliklerine kadar yaşatıyor

> "Go dili sade, hızlı ve eşzamanlı programlamaya uygun yapısıyla geleceğin sistem programlama dillerinden biridir."

---

## 🛣️ Yol Haritası (Roadmap)

Gelecekte eklenmesi planlanan özellikler ve konular:
- [ ] **GORM Entegrasyonu**: Veritabanı işlemleri için ORM kullanımı.
- [ ] **Dockerize Go Apps**: Uygulamaların container ortamına taşınması.
- [ ] **Unit Testing**: `testing` paketi ile kod kalitesinin artırılması.
- [ ] **gRPC & Protobuf**: Yüksek performanslı mikroservis iletişimi.

---

## ❓ Sıkça Sorulan Sorular (FAQ)

**S: Go öğrenmesi zor mu?**  
C: Kesinlikle hayır. Go'nun sadece 25 anahtar kelimesi (keyword) vardır. Bu da onu öğrenmesi en kolay dillerden biri yapar.

**S: Neden C++ veya Java yerine Go?**  
C: Go, C++'ın performansını Java'nın kolaylığıyla birleştirirken, karmaşık derleme süreçlerini ve ağır runtime'ları ortadan kaldırır.

---

## 📚 Öğrenim Materyalleri

- [A Tour of Go](https://tour.golang.org/) - Etkileşimli resmi eğitim.
- [Go by Example](https://gobyexample.com/) - Açıklamalı kod örnekleri.
- [Effective Go](https://golang.org/doc/effective_go.html) - Go yazım standartları.

---

## 🤝 Katkıda Bulunmak İstersen

Bu repo eğitim amaçlıdır. Sen de projelere katkı sağlamak, farklı çözümler eklemek veya yorum yapmak istersen forkla, kodunu yaz, PR gönder. Açık kaynak ruhu yaşasın! 🙌

---

## 👤 Geliştirici Hakkında / About the Developer

**Bahattin Yunus Çetin**
*IT Architect | University Student (Of, Trabzon)*

BTK Akademi Go Dili Kursu kapsamındaki gelişim sürecimi ve projelerimi bu depoda derliyorum. Profesyonel ağım ve diğer çalışmalarım için aşağıdaki bağlantıları kullanabilirsiniz.

---

### 🔗 İletişim & Sosyal Medya / Networking

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/bahattinyunus)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/bahattinyunus/)


---

> Kodun temiz, compiler hatasız, channel'ların tıkanmasın!

README'yi okuduysan, Go diline adım atmaya çoktan hazırsın demektir. Hadi bakalım, `go run` ile macera başlasın! 🧑‍💻
