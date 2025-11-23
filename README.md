

# 🌌 StarWars Pac — Gestión de Ciudadanos Galácticos

Bienvenido a **StarWars Pac**, una aplicación Android desarrollada en Kotlin que permite registrar, consultar y gestionar ciudadanos de la galaxia usando una base de datos SQLite.
Está pensada como ejercicio educativo para practicar **CRUD**, navegación entre pantallas, layouts, eventos y multimedia en Android.

---

## 🚀 Características principales

### 🛸 Gestión de ciudadanos (CRUD)

* **Create** → Registrar nuevos ciudadanos galácticos
* **Read** → Consultar listados filtrados por **especie** o **afiliación**
* **Update** → Actualizar datos existentes
* **Delete** → Eliminar ciudadanos por ID

Todo se almacena en **SQLite** usando un helper `GalaxiaSQLite`.

---

## 📁 Estructura del Proyecto

```
app/
├── java/com/elsda/starwars_pac/
│   ├── ui/
│   │   ├── MainActivity.kt
│   │   ├── EligeOpcion.kt
│   │   └── (más activities…)
│   ├── bbdd/
│   │   └── GalaxiaSQLite.kt
│   └── seres/
│       └── CiudadanoGalactico.kt
│
└── res/
    ├── layout/
    ├── drawable/
    ├── values/
    └── raw/
        └── cancion.mp3     ← sonido personalizado
```

---

## 🎨 Interfaz

* Pantalla principal con fondo personalizado
* Botón para navegar al registro
* Sonido **`cancion.mp3`** al pulsar el botón
* Actividades para registro y listados

Si quieres, puedo generar un apartado de *Screenshots* si me pasas capturas.

---

## 🎙️ Sonido al pulsar el botón

El archivo de sonido debe estar en:

```
app/src/main/res/raw/cancion.mp3
```

Y el código para reproducirlo se encuentra en `MainActivity.kt`:

```kotlin
mediaPlayer = MediaPlayer.create(this, R.raw.cancion)
mediaPlayer.start()
```

---

## 🗃️ Base de Datos SQLite

La tabla principal:

```sql
CREATE TABLE ciudadanos(
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    nombre TEXT NOT NULL,
    apellidos TEXT NOT NULL,
    edad INTEGER NOT NULL,
    especie TEXT NOT NULL,
    planetaOrigen TEXT NOT NULL,
    afiliacion TEXT NOT NULL
);
```

Incluye métodos para:

* insertar ciudadanos
* actualizar ciudadanos
* eliminar por ID
* contar ciudadanos
* filtrar por especie
* filtrar por afiliación

---

## 🛠️ Tecnologías utilizadas

* **Kotlin**
* **Android Studio**
* **SQLite (SQLiteOpenHelper)**
* **ConstraintLayout**
* **MediaPlayer**
* **Intents y navegación entre activities**

---

## 📦 Instalación

1. Clona el repositorio:

```sh
git clone https://github.com/tuusuario/turepo.git
```

2. Abre el proyecto con **Android Studio**
3. Sincroniza Gradle
4. Ejecuta en un dispositivo o emulador Android

---

## 👨‍💻 Autor

Proyecto realizado como práctica de desarrollo Android.
Si quieres, puedo añadir tu nombre, correo, redes, logo… solo dímelo.

---

## ⭐ Si te gusta el proyecto…

Déjale una estrella ⭐ en GitHub para apoyar el desarrollo.

---

Si quieres, también puedo crear:
✅ Un logo para el README
✅ Badges (Build, Version, Kotlin, License…)
✅ Un GIF de demostración
✅ Una versión en inglés

¿Quieres mejorar el README con más secciones visuales?
