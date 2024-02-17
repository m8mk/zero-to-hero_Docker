# Temel imajı belirle
FROM ubuntu:20.04

# Yazar ve açıklama etiketleri
LABEL maintainer="ornek@ornek.com"
LABEL description="Bu bir Docker dosyası örneğidir."

# Ortam değişkenlerini tanımla
ENV APP_HOME=/uygulama
ENV PORT=8080

# Çalışma dizinini belirle
WORKDIR $APP_HOME

# Dosyaları kopyala
COPY . .

# Komutları çalıştır
RUN apt-get update && \
    apt-get install -y \
    python3 \
    python3-pip \
    curl \
    && rm -rf /var/lib/apt/lists/*

# Portları dışa aç
EXPOSE $PORT

# Sağlık kontrolünü tanımla
HEALTHCHECK --interval=30s --timeout=10s \
  CMD curl -f http://localhost:$PORT/ || exit 1

# Giriş noktasını belirle
ENTRYPOINT ["python3", "app.py"]

# Varsayılan komutları belirle
CMD ["--debug"]

