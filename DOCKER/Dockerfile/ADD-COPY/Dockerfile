# Temel imajı belirle
FROM ubuntu:20.04

# Çalışma dizinini ayarla
WORKDIR /uygulama

# COPY ile dosyaları kopyala
COPY index.html /uygulama/
COPY app.tar.gz /uygulama/

# ADD ile dosyaları ekle
ADD https://ornek.com/archive.tar.gz /uygulama/

# Portu dışa aç
EXPOSE 80

# Uygulamayı çalıştırmak için komut
CMD ["python", "app.py"]
