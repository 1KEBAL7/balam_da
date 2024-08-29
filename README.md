# balam_da
Repositorio de prueba para implementar LLM y una aplicacion web

# 1. Installación 

como primer paso descargamos [ollama]( https://ollama.com/download/linux ) de sus pagina web, y ejecutamos el siguiente comando:

````bash
$ curl -fsSL https://ollama.com/install.sh | sh
````
## 2. Ejecutamos el servidor

ejecutar el servidor de API REST de ollama con el suiguiente comando

````bash
$ ollama serve
````

## 3. Descargar un modelo

En la pagina de ollama descarga un [modelo](https://ollama.com/library) utilizando el siguiente comando:

````bash
$ ollama pull tinyllama
````


## 4. realizar un request a la API REST

para realizar una consulta utilizamos el comando curl como se meuestra el siguiente ejemplo: 

````bash
curl -X POST http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?"
}'
````

````bash
curl -X POST http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?",
  "stream": false
}'
````


Para realizar una consulta a la API REST sin stream se hace de la siguiente forma: 

````bash
curl -X POST http://localhost:11434/api/generate -d '{
"model": "tinyllama",
"prompt": "Why is the sky blue?",
"stream": false
}'
````

## Para guardar en GitHub

````bash
git add .
````

````bash
git commit -m "UPDATE REAMDE.md"
````

````bash
git push -u origin main
````
