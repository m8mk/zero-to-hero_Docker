# Temel imajı belirle
FROM ubuntu:20.04

# Çalışma dizinini ayarla
WORKDIR /uygulama

# Uygulama dosyalarını kopyala
COPY app.py /uygulama/
COPY config.ini /uygulama/

# Çalıştırılacak komutu belirle (CMD)
CMD ["python", "app.py"]

# Varsayılan parametrelerle çalıştırılacak komutu belirle (ENTRYPOINT)
ENTRYPOINT ["gunicorn", "-c", "config.ini"]
