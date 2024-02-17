# Temel imajı belirle
FROM ubuntu:20.04

# Çalışma dizinini ayarla
WORKDIR /uygulama

# Uygulama dosyalarını kopyala
COPY app.py /uygulama/
COPY config.ini /uygulama/

# Exec formu ile komut belirle
CMD ["/bin/bash", "-c", "python app.py"]

# Shell formu ile komut belirle
# CMD python app.py
