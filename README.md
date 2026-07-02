# Bioimaging Cell Tracking 3D

**3D Mikroskopi Verilerinde Hücre Segmentasyonu ve Takibi**

## Özellikler
- **Veri**: Zarr formatı (100 zaman dilimi, 64×256×256 3D hacimler)
- **Segmentasyon**: 3D U-Net (PyTorch) + 3B Euclidean Distance Transform + Watershed
- **Tracking**: Hungarian Algoritması (15 piksel gating)
- **Çıktı**: `submission.csv` formatında takip sonuçları

## Kullanım Alanları
- İmmünoloji: Bağışıklık hücrelerinin hareket analizi (in vivo imaging)
- İlaç Geliştirme: High-content screening ve organoid takibi
- Embriyo gelişimi ve kanser araştırmaları

## Sonuçlar
- Eğitim: 5 epoch ile loss 0.34 → 0.1504
- Toplam track edilen hücre hareket adımı: **1613+**

## Kurulum

```bash
# Repoyu klonla
git clone [https://github.com/Umut6345/bioimaging_cell_tracking_3d.git](https://github.com/Umut6345/bioimaging_cell_tracking_3d.git)
cd bioimaging_cell_tracking_3d

# Gereksinimleri yükle
pip install -r requirements.txt

> **Not**: Bu repository temel ve eğitici bir versiyon içermektedir.  
> Daha gelişmiş model (25 epoch, düşük validation loss, 6069+ track) ve ek geliştirmeler (division detection vb.) **özel işbirlikleri ve projeler** için mevcuttur.
