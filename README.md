# GPSMapApp (SimpleGPSMapApp) 🗺️📸

Aplicación Android desarrollada en **Java** que integra **Google Maps API**, **GPS / Fused Location** y la **Cámara** del dispositivo.

## 🚀 Funcionalidades

1. **Google Maps Integrado**:
   - Muestra un mapa interactivo con controles de zoom y brújula (`MapView`).
2. **Ubicación en Tiempo Real (GPS)**:
   - Solicita permisos en tiempo de ejecución (`ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`).
   - Obtiene la ubicación actual del usuario mediante `FusedLocationProviderClient` y centra la cámara en la posición detectada.
   - Coloca un marcador azul (`HUE_AZURE`) en la ubicación actual del usuario.
3. **Marcadores Personalizados**:
   - Permite al usuario tocar cualquier punto del mapa (`setOnMapClickListener`) para añadir marcadores rojos con título y coordenadas.
   - Incluye un botón flotante para limpiar los marcadores del mapa.
4. **Captura de Fotos con la Cámara**:
   - Solicita permiso de cámara en tiempo de ejecución (`CAMERA`).
   - Inicia la cámara usando `ActivityResultLauncher` e Intent `MediaStore.ACTION_IMAGE_CAPTURE`.
   - Muestra una vista previa Flotante/CardView con la foto capturada en tiempo real.

---

## 🛠️ Configuración e Instalación

### 1. Clonar el repositorio
```bash
git clone https://github.com/franciscoelking10-debug/SimpleGPSMapApp.git
cd SimpleGPSMapApp
```

> **Target SDK**: Android 11 (API 30) | **Lenguaje**: Java

### 2. Configurar Google Maps API Key
Para que el mapa se renderice correctamente en la aplicación:
1. Dirígete a [Google Cloud Console](https://console.cloud.google.com/).
2. Crea un proyecto y habilita la API **Maps SDK for Android**.
3. Genera una **API Key**.
4. Abre el archivo `app/src/main/res/values/google_maps_api.xml` y reemplaza el texto `TU_API_KEY_AQUI` con tu clave:

```xml
<resources>
    <string name="google_maps_key" templateMergeStrategy="preserve" translatable="false">TU_CLAVE_API_REAL_AQUI</string>
</resources>
```

### 3. Ejecutar la Aplicación
1. Abre el proyecto en **Android Studio**.
2. Sincroniza Gradle (`Sync Project with Gradle Files`).
3. Conecta un dispositivo físico con depuración USB habilitada o inicia un emulador Android (con Google Play Services disponibles).
4. Haz clic en **Run 'app'**.

---

## 📤 Pasos para subir el proyecto a GitHub

Para crear e inicializar el repositorio local y subirlo a GitHub bajo el nombre `SimpleGPSMapApp`:

```bash
# 1. Inicializar el repositorio Git
git init

# 2. Agregar todos los archivos
git add .

# 3. Realizar el primer commit
git commit -m "Primer commit - Proyecto GPSMapApp con Google Maps y Cámara"

# 4. Cambiar la rama principal a main
git branch -M main

# 5. Conectar con el repositorio remoto de GitHub
git remote add origin https://github.com/tu-usuario/SimpleGPSMapApp.git

# 6. Subir los cambios a GitHub
git push -u origin main
```

---

## ⚙️ Permisos Utilizados (`AndroidManifest.xml`)

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
<uses-permission android:name="android.permission.CAMERA" />
```

---

## ✒️ Autor
Desarrollado para la actividad de **GPS y Mapas** - Android Java.
