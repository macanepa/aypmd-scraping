# aypmd-scraping

Este repositorio sirve como base para el Taller de Web Scraping del Curso de Almacenamiento y Procesamiento Masivo de Datos.

Durante este taller, exploraremos dos enfoques para realizar web scraping. En primer lugar, aprenderemos a simular la interacción humana utilizando `Selenium`. Luego, nos sumergiremos en recrear las solicitudes HTTP que el navegador realiza utilizando `Requests`.

**Hay que ser reponsabiles cuando hacemos web scraping**: Limitar la frecuencia de las solicitudes, extraer solo la información necesaria y relevante, y minimizar cualquier impacto negativo en la experiencia de usuario y en el rendimiento del sitio web.

## Setup Inicial

crear un archivo en la carpeta `.env` y colocar el siguiente contenido

```
DB_CONNECTION_STRING=<connection string para una base de datos MongoDB>
```

(opcional) Se recomienda utilizar en nuevo entorno de conda

```bash
conda create -n <nombre entorno> python=3.13 -y
```

Instalar dependencias

```bash
pip install -r requirements.txt
```

## Workshops

[Workshop: Scraping con Selenium](./selenium_scraping.ipynb)

[Workshop: Scraping con Requests](./requests_scraping.ipynb)

[Workshop: Scraping con equests Avanzado](./advanced_requests_scraping.ipynb)

## Conceptos Adicionales

Durante el proceso de web scraping, nos podemos enfrentar a diversas barreras que pueden dificultar la extracción de información, como bloqueos de IP o incluso la presencia de CAPTCHA.

**Proxy:** Para superar estas limitaciones, existen servicios que ofrecen la posibilidad de alquilar direcciones IP de datacenters o residenciales. Esto permite ocultar tu propia IP y, en caso de bloqueo, cambiar a otra dirección IP. Además, es posible configurar estos servicios para que cada solicitud se realice con una IP diferente, aumentando así la robustez del proceso de web scraping.

Ejemplo: [https://brightdata.es/](https://brightdata.es/)

**Captcha**: Existen servicios de resolución de CAPTCHA. Cuando necesites automatizar un proceso que tiene estas protecciones anti-bots, puedes suscribirte a uno de estos servicios para que resuelvan el CAPTCHA por ti. Como tienen API, puedes integrarte programaticamente, lo cual permite automatizar el 100% de tu flujo de web-scraping.

Ejemplo: [https://2captcha.com/](https://2captcha.com/)
