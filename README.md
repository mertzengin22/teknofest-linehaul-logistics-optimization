# 🚀 TEKNOFEST 2026 - Yapay Zeka Destekli Lojistik Anahat Optimizasyonu (Yarı Finalist)

Bu depo, kargo taşımacılığında ana taşıma (linehaul) maliyetlerini en aza indirmek amacıyla geliştirilen optimizasyon ve yapay zeka projesinin **mimari vitrinini** içermektedir. Fikri mülkiyet ve yarışma kuralları gereği kaynak kodlar gizli (private) tutulmuş olup, burada sistemin nasıl çalıştığına dair kavramsal akış sunulmuştur.

## 📌 Proje Özeti
Kargo operasyonlarında araç rotalama, kapasite kullanımı ve filo atama süreçlerindeki verimsizlikleri ortadan kaldırmak için iki aşamalı bir çözüm mimarisi tasarlanmıştır.

---

## ⚙️ Aşama 1: Temel İşlev (Basic Functionality)
Projenin ilk fazında, deterministik verilere dayalı bir altyapı kurularak sistemin operasyonel sınırları test edilmiştir:
* **Veri Ön İşleme:** Gelen kargo desi verilerinin temizlenmesi ve yapılandırılması.
* **Kapasite ve Kısıt Yönetimi:** Araç kapasiteleri ve depo kısıtlarının matematiksel olarak tanımlanması.
* **Temel Rotalama:** Ön tanımlı kurallara dayalı başlangıç rotalama algoritmasının kurgulanması.

---

## 🧠 Aşama 2: Gelişmiş Çözüm (Advanced Solution)
İkinci fazda, sistemi statik bir yapıdan çıkarıp veri odaklı ve dinamik bir karar destek sistemine dönüştüren makine öğrenmesi ve ileri yöneylem teknikleri entegre edilmiştir:
* **Talep Tahminleme (Machine Learning):** Günlük desi dalgalanmalarını öngörebilmek için **XGBoost** algoritması ile talep tahmin modeli geliştirilmiş ve **Optuna** ile hiperparametre optimizasyonu sağlanmıştır.
* **İleri Optimizasyon (Gurobi):** Makine öğrenmesinden gelen tahmin verileri, **Gurobi Solver** kullanılarak Kapasite Kısıtlı Araç Rotalama ve Filo Atama (CVRP) modelleriyle entegre edilmiş, minimum maliyetli ağ tasarımı elde edilmiştir.
* **İnteraktif Karar Destek Sistemi:** Karar vericilerin sonuçları anlık olarak takip edebilmesi, farklı senaryoları simüle edebilmesi için **Streamlit** tabanlı kullanıcı dostu bir dashboard geliştirilmiştir.

---

## 🏗️ Çözüm Mimarisi (Architecture Flow)
*(Buraya sistemin nasıl çalıştığını gösteren -verinin girişinden dashboard'a kadar- bir akış şeması görseli (PNG/JPG) ekleyebilirsin.)*
`![Sistem Mimarisi](gorsel_linki_buraya_gelecek.png)`

## 💻 Kullanılan Teknolojiler (Tech Stack)
* **Modelleme & Optimizasyon:** Gurobi, Yöneylem Araştırması Teknikleri
* **Makine Öğrenmesi & Veri Bilimi:** Python, XGBoost, Optuna, Pandas, NumPy
* **Arayüz (Frontend/Dashboard):** Streamlit

---
*Bu proje, TEKNOFEST 2026 sürecinde [Şehmus Taş, Ali Balıkçı, Caner Taviş ve diğer takım arkadaşların isimleri] ile birlikte harika bir takım çalışması sonucunda geliştirilmiştir.*