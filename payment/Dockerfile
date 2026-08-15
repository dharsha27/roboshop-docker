FROM python:3.9

WORKDIR /app
COPY requirement.txt .
COPY payment.ini .
COPY *.py .
RUN pip3 install -r requirements.txt

EXPOSE 8080
# RUN addgroup -S roboshop && adduser -S -G roboshop roboshop && \
#     chown -R roboshop:roboshop /app
# COPY --from=builder /app /app
# USER roboshop
CMD ["uwsgi ","--ini", "payment.ini"]