FROM python:3.9
RUN groupadd -r TI && useradd -r -g TI -m lucas
WORKDIR /app
COPY requiriments.txt .
RUN pip install -r requiriments.txt
COPY . .
RUN chown -R lucas:TI /app
USER lucas
CMD ["python", "app.py"]
