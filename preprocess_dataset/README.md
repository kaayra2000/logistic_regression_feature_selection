# Veri Kümesi Ön İşleme

Bu klasörde veri kümesi ön işleme için gerekli kodlar yer alır. `data_preprocessing.ipynb` dosyası kullanılarak `dataset_files/dataset.csv` dosyası içindeki gereksiz `timedelta` ve `url` sütunlarını siler. Ayrıca yine aynı dosyadaki `shares` sütununun 1400 değerinden küçük oması ya da olmaması durumuna göre `is_popular` sütununu oluşturur ve `shared` sütununu siler. Son olarak `dataset_files/dataset.csv` dosyasını `dataset_files/dataset_preprocessed.csv` dosyasına kaydeder.
