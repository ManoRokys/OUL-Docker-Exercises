FROM python:3.14.0a7
WORKDIR /app
COPY app.py .
COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
RUN useradd -m lucas
USER lucas
CMD ["/entrypoint.sh"]