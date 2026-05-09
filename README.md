# Proyecto Home About

Una aplicación web básica creada con Django que muestra una página de inicio y una página "Acerca de". El proyecto usa plantillas HTML simples, ruteo con vistas basadas en clases y una configuración mínima para ejecutarse localmente.

---

## 🚀 Descripción

Este proyecto es una pequeña página de presentación que contiene:

- Página principal (`/`)
- Página "Acerca de" (`/about/`)
- Configuración de Django con SQLite
- Estructura de proyecto con app `pages`
- Plantillas ubicadas en `templates/`

---

## 🧱 Tecnologías

- Python
- Django 6.0.4
- SQLite
- Plantillas de Django

---

## 📦 Dependencias

Las dependencias están listadas en `requirements.txt`:

- `asgiref==3.11.1`
- `Django==6.0.4`
- `sqlparse==0.5.5`
- `tzdata==2026.2`

---

## 📁 Estructura del proyecto

```
home_about/
├── base_project/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── pages/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── tests.py
│   ├── urls.py
│   └── views.py
├── templates/
│   ├── _base.html
│   ├── about.html
│   └── home.html
├── db.sqlite3
├── manage.py
└── requirements.txt
```

---

## ⚙️ Configuración local

Sigue estos pasos para ejecutar el proyecto en tu máquina:

1. Crear y activar un entorno virtual:

   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   ```

2. Instalar dependencias:

   ```bash
   pip install -r requirements.txt
   ```

3. Ejecutar migraciones:

   ```bash
   python manage.py migrate
   ```

4. Iniciar el servidor de desarrollo:

   ```bash
   python manage.py runserver
   ```

5. Abrir en el navegador:

   - `http://127.0.0.1:8000/` → Página de inicio
   - `http://127.0.0.1:8000/about/` → Página Acerca de
   - `http://127.0.0.1:8000/admin/` → Panel de administración (si se crea superusuario)

---

## 🧭 Rutas principales

- `/` : Página principal (`HomeView`)
- `/about/` : Página "Acerca de" (`AboutView`)
- `/admin/` : Administración de Django

---

## 🧩 Detalles del proyecto

- `base_project/settings.py` configura la base del proyecto, incluyendo la carpeta `templates` y la base de datos SQLite.
- `pages/views.py` define dos vistas basadas en clases que renderizan plantillas estáticas.
- `pages/urls.py` define las rutas internas del sitio.
- `templates/_base.html` es la plantilla base compartida por ambas páginas.

---

## 💡 Notas

- El archivo `db.sqlite3` ya existe y puede contener datos de prueba.
- Actualmente `DEBUG` está activado en `base_project/settings.py`, por lo que este proyecto es ideal sólo para desarrollo.
- Para producción, asegúrate de configurar `ALLOWED_HOSTS`, desactivar `DEBUG`, y usar una base de datos más robusta.

---

## ✅ Sugerencias futuras

- Agregar navegación dinámica y estilos CSS.
- Añadir contenido real en la página `about.html`.
- Implementar más secciones o una app de blog.
- Crear un superusuario para acceder al panel de administración.
