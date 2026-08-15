FROM maven:3.9.16
WORKDIR /app
COPY pom.xml .
COPY src ./src
RUN mvn clean package && \
    mv target/shipping-1.0.jar shipping.jar 

EXPOSE 8080
# RUN addgroup -S roboshop && adduser -S -G roboshop roboshop && \
#     chown -R roboshop:roboshop /app
# COPY --from=builder /app /app
# USER roboshop
CMD ["java","-jar", "shipping.jar"]