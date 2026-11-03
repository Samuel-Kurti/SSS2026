FROM python:3.11-slim

WORKDIR /app

# Installa le dipendenze richieste
RUN pip install --no-cache-dir fastapi sqlalchemy uvicorn

# Copia il codice sorgente
COPY . /app

# Espone la porta di FastAPI
EXPOSE 8000

# Avvia uvicorn bindando su 0.0.0.0 (fondamentale dentro Docker per accettare connessioni esterne)
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
