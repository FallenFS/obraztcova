FROM openjdk:11

WORKDIR /app

COPY calc.jar /app/calc.jar

RUN apt-get update && apt-get install -y \
x11-apps \
xauth \
libxtst6 \
&& rm -rf /var/lib/apt/lists/*

ENV DISPLAY=:0

CMD ["java", "-jar", "calc.jar"]    

