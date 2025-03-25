FROM python:3.9

WORKDIR /app

COPY main.py .
RUN pip install streamlit psycopg2

CMD ["streamlit", "run", "main.py", "--server.port=8401", "--server.address=0.0.0.0"]
