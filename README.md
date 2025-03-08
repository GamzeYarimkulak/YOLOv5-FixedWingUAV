# YOLOv5 ile Sabit Kanatlı İHA Tespiti Projesi

Bu repo, YOLOv5 modelini kullanarak **sabit kanatlı İHA tespiti** üzerine yapılan çalışmaları içermektedir. Proje, hava sahasında sabit kanatlı insansız hava araçlarını (İHA) tespit etmek için model eğitimi ve değerlendirme süreçlerini kapsamaktadır.

## Proje İçeriği

### 1. Sabit Kanatlı İHA Tespiti
- **Veri Kümesi**: Roboflow'dan alınan sabit kanatlı İHA görüntüleri.
- **Amaç**: Askeri ve sivil amaçlı hava araçlarının tespiti.
- **Model**: YOLOv5n (Nano) modeli kullanılmıştır.
- **Eğitim Süreci**: 
  - Toplam epoch: 200
  - Batch size: 16
  - Optimizasyon: SGD

## Kurulum

1. Projeyi klonlayın:
   ```bash
   git clone https://github.com/GamzeYarimkulak/YOLOv5-FixedWingUAV.git
   cd YOLOv5-FixedWingUAV
   ```

2. Gerekli kütüphaneleri yükleyin:
   ```bash
   pip install -r requirements.txt
   ```

3. YOLOv5'i yükleyin:
   ```bash
   git clone https://github.com/ultralytics/yolov5.git
   cd yolov5
   pip install -r requirements.txt
   ```

## Veri Kümesi Hazırlığı
- **İHA Veri Kümesi**: [Roboflow Fixed-Wing UAV Dataset](https://roboflow.com/)

Veri kümesi `datasets/` klasörüne yerleştirilmeli ve `train` ile `val` klasörleri oluşturulmalıdır.

## Eğitim

Eğitim sürecini başlatmak için aşağıdaki komutu çalıştırabilirsiniz:
```bash
python train.py --img 640 --batch 16 --epochs 200 --data datasets/uav.yaml --weights yolov5n.pt --name uav_detection
```

## Sonuçlar
- **mAP@0.5**: %78 (Sabit Kanatlı İHA Tespiti)

## Lisans
Bu proje MIT lisansı ile lisanslanmıştır.

## İletişim
Gamze Yarımkulak  
[GitHub](https://github.com/GamzeYarimkulak)  
[LinkedIn](https://www.linkedin.com/in/gamze-yarimkulak-355a6933a/)


