# Aşama 1: Uygulama Derleme Aşaması
FROM openjdk:11 AS build
WORKDIR /uygulama
COPY . /uygulama
RUN javac Main.java

# Aşama 2: Çalıştırma Aşaması
FROM openjdk:11-jre
WORKDIR /uygulama
COPY --from=build /uygulama/Main.class /uygulama
CMD ["java", "Main"]
