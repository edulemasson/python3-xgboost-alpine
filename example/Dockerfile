FROM eduardolemasson/xgboost-alpine:1.1

ENV PYTHONUNBUFFERED=0

COPY ./ app/

# If you have some another python dependencies
RUN pip install -r /app/requirements.txt

WORKDIR /app

CMD [ "python","-u", "./src/main.py" ]
