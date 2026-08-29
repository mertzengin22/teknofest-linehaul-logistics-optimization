# TEKNOFEST 2026 - Yapay Zeka Destekli Lojistik Anahat Optimizasyonu

Bu repo, kargo taşımacılığında ana taşıma (linehaul) maliyetlerini en aza indirmek amacıyla geliştirilen **yarı finalist** optimizasyon ve yapay zeka projesinin mimari vitrinini içermektedir. Fikri mülkiyet ve yarışma kuralları gereği kaynak kodlar gizli (private) tutulmuş olup, burada sistemin nasıl çalıştığına dair kavramsal akış sunulmuştur.

# Proje Özeti
Kargo ve tedarik zinciri yönetimindeki en büyük maliyet kalemlerinden biri ana taşıma (linehaul) operasyonlarıdır. Günlük desi (kargo hacmi) dalgalanmalarının yarattığı belirsizlik, hatalı kapasite planlamasına ve atıl araç kullanımına yol açarak operasyonel maliyetleri artırmaktadır. Bu proje, söz konusu belirsizlikleri ortadan kaldırmak amacıyla makine öğrenmesi (Machine Learning) ve yöneylem araştırması (Operations Research) disiplinlerini tek bir potada eriten uçtan uca bir karar destek sistemi sunmaktadır. Çalışma kapsamında, tahmine dayalı modeller ile operasyonel talepler öngörülmüş ve bu veriler kapasite kısıtlı matematiksel algoritmalarla işlenerek minimum maliyetli araç rotalama ve filo atama planlarına dönüştürülmüştür. TEKNOFEST 2026'da Yarı Finalist unvanı kazanan bu sistem, veriyi merkeze alarak lojistik ağ tasarımında dinamik, esnek ve maliyet etkin bir çözüm mimarisi ortaya koymaktadır.

---

# Temel İşlev (Basic Functionality)
Projenin ilk fazında, deterministik verilere dayalı bir altyapı kurularak sistemin operasyonel sınırları test edilmiştir:
* **Veri Ön İşleme:** Gelen kargo desi verilerinin temizlenmesi ve yapılandırılması.
* **Kapasite ve Kısıt Yönetimi:** Araç kapasiteleri ve depo kısıtlarının matematiksel olarak tanımlanması.
* **Temel Rotalama:** Ön tanımlı kurallara dayalı başlangıç rotalama algoritmasının kurgulanması.

---

# Gelişmiş Çözüm (Advanced Solution)
İkinci fazda, sistemi statik bir yapıdan çıkarıp veri odaklı ve dinamik bir karar destek sistemine dönüştüren makine öğrenmesi ve ileri yöneylem teknikleri entegre edilmiştir:
* **Talep Tahminleme (Machine Learning):** Günlük desi dalgalanmalarını öngörebilmek için **XGBoost** algoritması ile talep tahmin modeli geliştirilmiş ve **Optuna** ile hiperparametre optimizasyonu sağlanmıştır.
* **İleri Optimizasyon (Gurobi):** Makine öğrenmesinden gelen tahmin verileri, **Gurobi Solver** kullanılarak Kapasite Kısıtlı Araç Rotalama ve Filo Atama (CVRP) modelleriyle entegre edilmiş, minimum maliyetli ağ tasarımı elde edilmiştir.
* **İnteraktif Karar Destek Sistemi:** Karar vericilerin sonuçları anlık olarak takip edebilmesi, farklı senaryoları simüle edebilmesi için **Streamlit** tabanlı kullanıcı dostu bir dashboard geliştirilmiştir.

---

# Çözüm Mimarisi (Architecture Flow)
![Sistem Mimarisi](https://github.com/user-attachments/assets/1c8dc624-37e8-4ad6-9dba-862a8be402f6)

# Kullanılan Teknolojiler (Tech Stack)
* **Modelleme & Optimizasyon:** Gurobi, Yöneylem Araştırması Teknikleri
* **Makine Öğrenmesi & Veri Bilimi:** Python, XGBoost, Optuna, Pandas, NumPy
* **Arayüz (Frontend/ UI, Dashboard):** Streamlit

---
