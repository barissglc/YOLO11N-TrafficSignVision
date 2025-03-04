# Traffic Signs Detection using YOLO11N

Bu repoda, trafik işaretlerini tespit etmek amacıyla **YOLO11N** mimarisi kullanılarak eğitilmiş modelin çıktı dosyaları, eğitim süreci, sonuçlar ve örnek tahmin görselleri yer almaktadır.

## İçerik

- [Proje Özeti](#proje-özeti)
- [Eğitim Süreci](#eğitim-süreci)
- [Sonuçlar ve Analizler](#sonuçlar-ve-analizler)

---

## Proje Özeti

Bu proje, trafik işaretlerini tespit etmek üzere **YOLO11N** mimarisi ile eğitilmiş bir model sunar. Eğitim sırasında elde edilen log dosyaları, grafikler ve ağırlık dosyaları sayesinde modelin performansını detaylı şekilde analiz edebilmekteyiz. Model ağırlık dosyası olarak `yolo11n.pt` kullanılmaktadır.

---

## Eğitim Süreci

- **Model:** YOLO11N  
- **Parametreler:** Eğitim sırasında kullanılan hiperparametreler `args.yaml` dosyasında yer almaktadır.  
- **Loglar:** Eğitim sürecine ait detaylı log dosyası (`events.out.tfevents.*`) TensorBoard gibi araçlarla incelenebilir.  
- **Ağırlıklar:** Eğitim sonunda elde edilen model ağırlıkları, `weights/` klasöründe saklanmaktadır (özellikle `yolo11n.pt`).

---

## Sonuçlar ve Analizler

Eğitim sürecinde elde edilen sonuçlar, modelin performansını değerlendirmek ve iyileştirme alanlarını belirlemek için detaylı görsellerle desteklenmiştir. Aşağıda, bu görsellerden bazıları ve kısa açıklamaları yer almaktadır:

### 1. Confusion Matrix
![Confusion Matrix](content/runs/detect/train/confusion_matrix.png)  
*Bu grafik, modelin hangi sınıflar arasında karışıklık yaşadığını ortaya koyar. Yanlış sınıflandırmaların nerede yoğunlaştığını görmek için oldukça faydalıdır.*

### 2. Normalize Edilmiş Confusion Matrix
![Normalized Confusion Matrix](content/runs/detect/train/confusion_matrix_normalized.png)  
*Sınıf dağılımının oranlarını daha net görmek için normalize edilmiş hali. Bu sayede, hata oranları yüzdesel olarak değerlendirilebilir.*

### 3. F1 Skor Eğrisi
![F1 Curve](content/runs/detect/train/F1_curve.png)  
*Modelin farklı eşik değerlerinde F1 skorunun nasıl değiştiğini gösterir. Bu eğri, modelin genel dengesini (precision-recall dengesini) değerlendirmemizi sağlar.*

### 4. Precision-Recall Eğrisi
![PR Curve](content/runs/detect/train/PR_curve.png)  
*Precision ve recall değerlerinin görselleştirildiği bu grafik, modelin yanlış pozitif ve yanlış negatif durumlarını değerlendirmeye yardımcı olur.*

### 5. Precision ve Recall Eğrileri
- **Precision Eğrisi:**  
  ![Precision Curve](content/runs/detect/train/P_curve.png)  
- **Recall Eğrisi:**  
  ![Recall Curve](content/runs/detect/train/R_curve.png)  
*Bu iki grafik, modelin tek tek precision (kesinlik) ve recall (duyarlılık) performansını ayrı ayrı gözler önüne serer.*

### 6. Genel Performans Sonuçları
![Performance Results](content/runs/detect/train/results.png)  
*Eğitim ve doğrulama süreçlerine ait genel metriklerin özetlendiği bu görsel, `results.csv` dosyasında yer alan sayısal verilerin grafiksel temsilidir.*

### 7. Etiket Dağılımı ve Correlogram
- **Etiket Dağılımı:**  
  ![Labels Distribution](content/runs/detect/train/labels.jpg)  
- **Labels Correlogram:**  
  ![Labels Correlogram](content/runs/detect/train/labels_correlogram.jpg)  
*Veri setindeki trafik işareti sınıflarının dağılımı ve aralarındaki korelasyonu gösterir. Bu bilgiler, eğitim verisinin dengesini ve modelin hangi sınıflara ağırlık verebileceğini anlamamıza yardımcı olur.*

