# NutriFlash

NutriFlash es un juego interactivo para Android diseñado para ayudar a los usuarios a aprender sobre recetas de comida mexicana saludable de una forma divertida y rápida.
El jugador debe armar recetas usando los ingredientes correctos antes de que el tiempo se acabe.

## Jugabilidad

El flujo principal del juego consiste en:
1. Se muestra una receta aleatoria.
2. El jugador selecciona los ingredientes correctos desde una cuadrícula.
3. Un temporizador empieza a correr mientras la receta se arma.
4. Si el jugador completa la receta a tiempo, gana puntos, el temporizador se reinicia y la dificultad aumenta ligeramente reduciendo el tiempo máximo.
5. El juego termina cuando el tiempo llega a cero.

## Características

- **Game loop dinámico** con temporizador cada vez más desafiante.  
- **Sistema de puntuación** basado en velocidad.  
- **Tres niveles de dificultad**: Fácil, Intermedio y Difícil.  
- **Pantalla de Configuración** para cambiar dificultad y gestionar ajustes.  
- **Efectos de sonido** al seleccionar ingredientes y al iniciar una nueva ronda.  
- **Base de datos local Room** para almacenar recetas e ingredientes.  
- **UI moderna con Jetpack Compose** totalmente declarativa.  

## Tecnologías y Arquitectura

- **Lenguaje:** Kotlin  
- **UI:** Jetpack Compose  
- **Arquitectura:** MVVM  
- **Estado:** StateFlow  
- **Navegación:** Jetpack Navigation Compose  
- **Persistencia:** Room  
- **Asíncronía:** Kotlin Coroutines  

### Dependencias principales

- `androidx.compose` (BOM, UI, Material3, Tooling)
- `androidx.navigation:navigation-compose:2.7.7`
- `androidx.lifecycle:lifecycle-viewmodel-compose:2.8.0`
- `androidx.room:room-runtime:2.8.2`
- `androidx.room:room-ktx`
- `androidx.core:core-ktx:1.17.0`

## Estructura del Proyecto

- **`MainActivity.kt`** — Entrada principal y configuración del NavHost.
- **Pantallas (`ui/theme/screens/`)**
  - `ArmarScreen.kt` — Pantalla principal del juego.
  - `SettingsScreen.kt` — Configuración del juego.
- **ViewModels (`ui/theme/screens/viewmodels/`)**
  - `ArmarViewModel.kt` — Lógica del juego (temporizador, puntos, recetas).
  - `SettingsViewModel.kt` — Manejo de configuraciones del usuario.
- **Base de datos (`database/`)**
  - `CocinaSaludableDatabase.kt`
  - `RecetaDao.kt`
  - `IngredienteDao.kt`

---

# Cómo construir el proyecto

1. Clona este repositorio.  
2. Abre el proyecto en Android Studio.  
3. Espera a que Gradle sincronice.  
4. Conecta un dispositivo Android o utiliza un emulador.  
5. Presiona **Run** para ejecutar la app.

---

# Cómo instalar NutriFlash en un teléfono Android (APK)

Si deseas instalar la app usando un archivo APK, sigue estos pasos:

## 1. Obtén el APK
Transfiérelo al teléfono usando cualquier método:
- USB  
- Bluetooth  
- Google Drive / OneDrive / Dropbox  
- WhatsApp / Telegram  
- Correo  
- Nearby Share  

Guárdalo en la carpeta que prefieras (ej. *Descargas*).

## 2. Permitir instalación desde “fuentes desconocidas”

1. Abre **Configuración**.  
2. Ve a **Seguridad** o **Aplicaciones**.  
3. Entra a **Instalar apps desconocidas**.  
4. Selecciona la app desde la que instalarás (Files, Drive, Chrome, etc.).  
5. Activa **Permitir desde esta fuente**.

## 3. Instalar el APK

1. Abre tu explorador de archivos.  
2. Localiza el archivo APK.  
3. Toca el archivo y selecciona **Instalar**.  
4. Espera unos segundos.

## 4. Abrir NutriFlash

Después de instalar:
- Toca **Abrir**, o  
- Encuentra *NutriFlash* en tu menú de apps.
