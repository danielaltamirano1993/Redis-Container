# 🚀 Ejecutar Redis Open Source en Docker

Este es un recurso rápido para levantar un servidor **Redis** utilizando imágenes oficiales de Docker y cómo conectarse a él.

---

## 💻 Inicio Rápido del Servidor Redis

Para iniciar el servidor Redis de código abierto usando la imagen `redis:<version>`, ejecuta el siguiente comando en tu terminal.

Reemplaza `<version>` con la versión de Redis que deseas utilizar (por ejemplo, `alpine`, `7.0`, `latest`).

```bash
docker run -d --name redis -p 6379:6379 redis:<version>

Opción	Descripción
-d	Ejecuta el contenedor en modo detached (segundo plano).
--name redis	Asigna el nombre redis al contenedor.
-p 6379:6379	Mapea el puerto 6379 del contenedor al puerto 6379 de tu host.
redis:<version>	Especifica la imagen de Redis a usar.

Conexión con redis-cli
Una vez que el servidor está en ejecución, puedes conectarte a él usando la herramienta de línea de comandos redis-cli.

Opción 1: Ejecutar redis-cli desde el Contenedor Docker
Si no tienes redis-cli instalado localmente, puedes ejecutarlo directamente desde el contenedor Docker que acabas de crear:

