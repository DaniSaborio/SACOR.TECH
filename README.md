# 📦 Despliegue del Proyecto SACOR.TECH (Rama JOOMLA)

Este documento describe los pasos necesarios para clonar, actualizar y desplegar el proyecto **SACOR.TECH** desde la rama **JOOMLA**, usando **Docker Compose**.

---

## 🚀 Requisitos Previos

Antes de comenzar, asegúrate de tener instalado:

- **Git**
- **Docker**
- **Docker Compose**

Puedes verificarlo ejecutando:

```bash
git --version
docker --version
docker compose version
```

---

## 📂 Clonar el Repositorio

Abre tu terminal y ejecuta los siguientes comandos:

```bash
# Ir al directorio donde quieras clonar el proyecto
cd ~/D/WEBPROJECT

# Clonar el repositorio principal
git clone https://github.com/DaniSaborio/SACOR.TECH.git

# Ingresar al proyecto
cd SACOR.TECH

# Cambiar a la rama correcta (JOOMLA)
git checkout JOOMLA

# Obtener los últimos cambios
git pull
```

> ⚠️ **Importante:** Todo el entorno de Joomla (sitio, base de datos y configuración) se encuentra en esta rama.

---

## 🐳 Despliegue con Docker Compose

El archivo `docker-compose.yml` ya está configurado para levantar el entorno completo (Joomla + Base de datos).  
Solo necesitas ejecutar:

```bash
# Levantar los contenedores
docker compose up -d
```

Esto descargará las imágenes necesarias (Joomla y MariaDB) y montará los volúmenes correspondientes (`joomla_data`, `db_data`).

---

## 🔍 Verificación

Puedes verificar que los contenedores están corriendo correctamente con:

```bash
docker ps
```

Y acceder al sitio en tu navegador:

👉 **http://localhost:8080**

Si todo fue exitoso, deberías ver la página principal de **SACOR.TECH** en Joomla.

---

## 🧹 Detener el entorno

Cuando termines, puedes detener los contenedores con:

```bash
docker compose down
```

Si deseas eliminar también los volúmenes (base de datos, archivos locales, etc.), ejecuta:

```bash
docker compose down -v
```

---

## 🧠 Notas Adicionales

- Los datos de Joomla se guardan en `./joomla_data/`
- La base de datos MariaDB persiste en `./db_data/`
- Si haces cambios en el sitio, estos se mantienen aunque detengas los contenedores.
- En caso de error de permisos, puedes usar:
  ```bash
  sudo chmod -R 777 joomla_data db_data
  ```

---

## ✉️ Soporte

Para cualquier duda o corrección, contactar a los desarrolladores del proyecto en:  
📧 **DaniSaborio /Alejandro Cordero/ SACOR.TECH Team**
