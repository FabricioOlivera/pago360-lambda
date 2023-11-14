# Empezar

## Desplegar lamdba en produccion
Debemos editar la instruccion del Makefile cambiando el `username` por nuestro usuario de aws

```sh
deploy_prod: build
	serverless deploy --stage prod --aws-profile username
```

El `username` debe coincidir con el que se encuentra en nuestro archivo de `credentials` de aws

```sh
cat ~/.aws/credentials
```

Correr el siguiente comando
```sh
make deploy_prod
```

Metodos a los que se puede acceder:
```
Listar buckets:
	- GET - https://m974s3k6og.execute-api.us-east-1.amazonaws.com/prod/list
Health endpoint:
	- GET - https://m974s3k6og.execute-api.us-east-1.amazonaws.com/prod/health
Subir archivo a S3
	- POST - https://m974s3k6og.execute-api.us-east-1.amazonaws.com/prod/upload


form-data
input_type: "file"
```
