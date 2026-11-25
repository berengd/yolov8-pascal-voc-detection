# YOLOv8n – Pascal VOC Object Detection

Pascal VOC (2007 + 2012) veri seti kullanılarak transfer öğrenme ile eğitilmiş YOLOv8n nesne tespiti modeli ve Gradio web arayüzü.

## Veri Seti Ayrımı
- **Train:** 14.041 görsel (VOC2007 train + VOC2012 train + VOC2012 val)
- **Validation:** 2.510 görsel (VOC2007 val)
- **Test:** 4.952 görsel (VOC2007 test)

## Eğitim Ayarları
- **Model:** YOLOv8n (`yolov8n.pt` transfer learning)
- **Input Size:** 640 × 640
- **Epochs:** 20 | **Batch Size:** 32
- **Optimizer:** AdamW (`lr0=0.001`, `weight_decay=0.0005`)
- **Loss:** CIoU + DFL + BCEWithLogitsLoss

## Test Kümesi Sonuçları (VOC2007 Test)
- **mAP@0.50:** 0.8012
- **mAP@0.50:0.95:** 0.5897
- **Precision:** 0.7901
- **Recall:** 0.7251
- **Inference Süresi:** 3.02 ms/görsel (Toplam: 5.51 ms/görsel ≈ 181.4 FPS)

## Çalıştırma
1. `.ipynb` dosyasını Google Colab (GPU) üzerinde açın.
2. Hücreleri sırasıyla çalıştırarak veri seti indirme, eğitim, test değerlendirme ve Gradio web uygulamasını başlatın.
