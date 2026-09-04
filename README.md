# Seri-Haberlesme-Karti-Tasarimi
Altium Designer ile tasarlanmış; STM32F437 mikrodenetleyici tabanlı, çoklu haberleşme arayüzlerine (RS-485, RS-232, CAN Bus, Ethernet) ve RT7235 buck konvertör güç katına sahip 4 katmanlı endüstriyel donanım kartı tasarımı.

# Çoklu Arayüzlü Endüstriyel Haberleşme Kartı

Bu depo, RST Teknoloji'deki mühendislik stajım kapsamında Altium Designer kullanılarak sıfırdan tasarlanmış endüstriyel bir donanım kartına ait şematik, PCB dizgi (4-katman), üretim ve 3D model dosyalarını içermektedir.

## 🛠️ Donanım Özellikleri ve Temel Bileşenler
* **Mikrodenetleyici:** STM32F437 (Yüksek performanslı ARM Cortex-M4 çekirdek)
* **Güç Katı (Power Management):** RT7235GQW Senkron Buck Konvertör (12V giriş, kararlı 5V/3.3V çıkış, özel soft-start ve bootstrap filtrelemeli tasarım)
* **Endüstriyel Haberleşme Arayüzleri:** 
  * RS-485 / RS-422 (SN65HVD78DRBT transceiver ile 120 Ohm sonlandırmalı empedans kontrolü)
  * RS-232 (Çift kanallı iletişim)
  * CAN Bus (Otomotiv ve endüstri standartlarında veri yolu)
* **Ağ Bağlantısı:** LAN8742A Ethernet PHY (25 MHz yüksek kararlılıklı C0G kristal osilatör devresi ile)
* **Çevresel Sensörler:** BME280 (I2C/SPI destekli sıcaklık, nem ve basınç sensörü)

## 📂 Depo İçeriği ve İnceleme Dosyaları
Bu proje, sadece donanım mühendislerinin değil; yazılım, mekanik ve test ekiplerinin de kolayca inceleyebileceği evrensel formatları barındırır:

* **Altium Kaynak Dosyaları:** Geliştirmeye açık güncel şematik (`.SchDoc`), 4-katmanlı PCB (`.PcbDoc`) ve projeye özel kütüphane dosyaları.
* **BOM (Malzeme Listesi):** Üretim optimizasyonu (BOM Consolidation) sağlamak amacıyla pasif bileşenler ve yüksek hassasiyetli elemanlarla hazırlanmış üretime hazır Excel listesi.
* **📄 Akıllı PDF (Smart PDF):** Bilgisayarında Altium Designer kurulu olmayan kişilerin şematikleri interaktif olarak inceleyebilmesi için oluşturulmuştur. (*PDF üzerinden pinlere veya komponentlere tıklayarak bağlantıları (net) takip edebilirsiniz.*)
* **🧊 3D STEP Modeli:** Kartın mekanik (kutu içi) entegrasyon testleri ve SolidWorks gibi CAD programlarında incelenebilmesi için `.step` formatında 3 boyutlu katı modeli.

## 🔍 Tarayıcı Üzerinden İnteraktif İnceleme (Program Kurulumsuz)
Bilgisayarınıza herhangi bir program indirmeden projenin 3 boyutlu halini ve PCB katman yollarını incelemek isterseniz:
1. Depodaki kaynak dosyaları bilgisayarınıza indirin (ZIP olarak).
2. [Altium 365 Online Viewer](https://www.altium.com/viewer/) adresine gidin.
3. Dosyaları ekrana sürükleyip bırakarak projeyi web tarayıcınız üzerinden tüm detaylarıyla inceleyin.
