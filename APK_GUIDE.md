# Generar APK desde este repositorio

Actualmente este repositorio solo contiene documentación y **no incluye código fuente ejecutable** (ni proyecto Android/Capacitor/React Native).

Por eso no es posible compilar una APK directamente aquí todavía.

## Opción recomendada (Laravel + Next.js con Capacitor)

Cuando tengas el frontend listo (export estático o app servida), puedes empaquetarlo en Android con Capacitor:

1. Instalar dependencias en tu proyecto frontend.
2. Inicializar Capacitor.
3. Agregar plataforma Android.
4. Sincronizar assets.
5. Compilar APK debug/release con Gradle.

### Comandos de referencia

```bash
npm install @capacitor/core @capacitor/cli @capacitor/android
npx cap init SmillyMerch com.smillymerch.app
npx cap add android
npm run build
npx cap sync android
cd android
./gradlew assembleDebug
```

La APK de debug queda normalmente en:

`android/app/build/outputs/apk/debug/app-debug.apk`

## Requisitos

- Node.js 18+
- Java 17
- Android Studio (SDK + build-tools)
- Variables `ANDROID_HOME` y `JAVA_HOME` configuradas

## Siguiente paso para poder "generar la APK"

Sube al repositorio alguno de estos escenarios:

- El frontend (Next.js) listo para build.
- O un proyecto móvil existente (Capacitor/React Native/Flutter).

Con eso sí puedo compilarte la APK desde aquí con comandos exactos.
