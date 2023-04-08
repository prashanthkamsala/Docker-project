FROM tiangolo/uvicorn-gunicorn:python3.8 
# version 3.8 is more stable compared to the 
WORKDIR /code

COPY requirements.txt .

RUN pip install --upgrade pip && pip install -r requirements.txt

CMD ["uvicorn", "app.main:app","--reload", "--host", "0.0.0.0", "--port", "8000"]