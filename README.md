# Akbank Derin Öğrenme Bootcamp: Brain Tumor MRI Sınıflandırma Projesi

## 📌 Giriş
Bu proje, **Akbank Derin Öğrenme Bootcamp** kapsamında beyin MR görüntülerini sınıflandırmak için geliştirildi.  
Amacım, **VGG-16 transfer learning** modelini kullanarak 4 sınıfı ayırmak ve derin öğrenme pratiği yapmak:  

- **glioma_tumor**  
- **meningioma_tumor**  
- **pituitary_tumor**  
- **no_tumor**  

Veri seti: [Brain Tumor MRI Dataset (Kaggle)](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)  
Hedefim, öğrenirken eğlenceli bir sonuç elde etmekti 🚀  

---

## 📊 Metrikler

**Genel Performans:**  
✅ Test setinde **%90 doğruluk**, 858 görüntü üzerinde başarılı bir sonuç!  

**Sınıf Bazlı Sonuçlar:**
- **Pituitary:** Precision 0.97, Recall 0.78, F1-score 0.87  
- **No tumor:** Precision 0.79, Recall 0.89, F1-score 0.83  
- **Meningioma:** Precision 0.93, Recall 0.97, F1-score 0.95  
- **Glioma:** Precision 0.95, Recall 0.95, F1-score 0.95  

ℹ️ Not: Pituitary’de recall düşük, bu **class imbalance**’tan kaynaklanabilir (toplam 5712 görüntü, pituitary 1457).  
Overfit gözlenmedi, train ve validation loss değerleri birbirine yakın.  

---

## 📈 Ekler

- **Görselleştirmeler:**  
  - Loss & accuracy grafikleri  
  - Confusion matrix (4x4 tablo)  
  - **Grad-CAM heatmap’leri** (modelin odaklandığı bölgeler)  

- **Araçlar:**  
  - PyTorch, torchvision  
  - matplotlib, seaborn, sklearn  
  - GPU (Kaggle T4 x2) ile hızlı eğitim  

- **Veri İşleme:**  
  - Görüntüler 224x224’e resize edildi  
  - Normalize yapıldı  
  - Data augmentation: flip, rotation  

---

## 📝 Sonuç ve Gelecek Çalışmalar
Bu proje ile **%90 accuracy** elde ederek bootcamp hedeflerini karşıladım.  
- Model **meningioma** ve **glioma** sınıflarında çok iyi performans verdi (F1 ≈ %95).  
- **Pituitary** sınıfında geliştirme alanı var (recall 0.78).  

📌 Gelecek fikirler:  
- Class imbalance için **class weight** eklemek  
- Gri tonlu görüntülerde normalize stratejilerini optimize etmek  
- Daha fazla epoch veya farklı modeller (örn. ResNet) denemek  

---

## 🔗 Linkler
- Kaggle Shared Notebook: [Kaggle Linki](https://www.kaggle.com/code/ahmet0akaslan/akbank-bootcamp?scriptVersionId=263791710)
- Kaggle Public Notebook: [Kaggle Linki](https://www.kaggle.com/code/ahmet0akaslan/akbank-bootcamp)



