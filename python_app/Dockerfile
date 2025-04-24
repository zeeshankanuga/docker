# -------- Stage 1: Build dependencies --------
FROM python:3.11 as build

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir --user -r requirements.txt

COPY . .

ENV PATH=/root/.local/bin:$PATH

# -------- Stage 2: Final image --------
FROM python:3.11-slim

WORKDIR /app

COPY --from=build /root/.local /root/.local
COPY --from=build /app /app

ENV PATH=/root/.local/bin:$PATH

USER root

EXPOSE 8100

CMD ["python3","app.py"]
