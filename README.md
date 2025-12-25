# 🚀 Spring Boot REST API: Employee Management System
### *Layered Architecture & In-Memory Data Management Study*

---

## 🛠 TEKNOLOJİ YIĞINI (TECH STACK)

* **Dil:** `Java 17`
* **Framework:** `Spring Boot 3.5.5`
* **Bağımlılık Yönetimi:** `Maven`
* **Yardımcı Araçlar:** `Lombok` (Data Mapping & Boilerplate Reduction)
* **Mimari:** `RESTful API` ile Katmanlı Mimari (Controller -> Service -> Repository)

---

## 📌 UYGULANAN MİMARİ KATMANLAR

### 🔹 1. Controller Katmanı (API Endpoints)
`@RestController` ve `@RequestMapping` kullanılarak endüstri standartlarında REST uç noktaları oluşturulmuştur.
* **GET:** `/list`, `/list/{id}`, `/list-with-params`
* **POST:** `/save-employee`
* **PUT:** `/update-employee/{id}`
* **DELETE:** `/delete-employee/{id}`

### 🔹 2. Service Katmanı (Business Logic)
İş mantığı `EmployeeService` sınıfında soyutlanarak `Controller` ve `Repository` arasındaki bağımlılık minimize edilmiştir (Loose Coupling).

### 🔹 3. Repository Katmanı (Data Access)
Veriler, `@Configuration` içindeki bir `@Bean` üzerinden sağlanan merkezi bir `ArrayList` yapısı ile **In-Memory** (bellek içi) olarak yönetilmektedir.

---

## 💡 ÖNE ÇIKAN ÖZELLİKLER

* **Dinamik Sorgulama:** `@RequestParam` ile isim ve soyisime göre filtreleme yapan gelişmiş arama metotları.
* **DTO Yaklaşımı:** Güncelleme operasyonları için özel `UpdateEmployeeRequest` veri transfer nesnesi (DTO) kullanımı.
* **Merkezi Konfigürasyon:** Uygulama başlangıç verilerinin `AppConfig` üzerinden yönetilmesi.
* **Temiz Kod (Lombok):** `@Getter`, `@Setter`, `@AllArgsConstructor` kullanımıyla sadeleştirilmiş Entity yapısı.

---

## ⚙️ KURULUM VE ÇALIŞTIRMA

1️⃣ **Bağımlılıkları Yükleyin:**
```bash
mvn clean install
```

2️⃣ Uygulamayı Başlatın:
```bash
mvn spring-boot:run
```
