# AnCar MDM — análisis inicial de APK

## APK analizada

- Archivo: MDM.apk
- Tamaño: 10,497,068 bytes
- Contiene: classes.dex + classes2.dex + classes3.dex + classes4.dex + classes5.dex
- Compilación indicada en META-INF/MANIFEST.MF: Android Gradle Plugin 7.2.2
- Firebase Messaging presente.

## Componentes detectados

- FirebaseMessagingService
- DevicePolicyManager
- DeviceAdminReceiver
- ComponentName
- setLockTaskPackages
- startForeground
- PowerManager / WakeLock
- ReceiverAutostart
- ReceiverAppUpdate
- MyFirebaseMessagingService
- MyService
- SampleAdminReceiver
- SampleKioskReceiver

Paquete principal observado: com/samsung/knox/example/kioskmode/

## Plan

1. Recuperar código/recursos decompilables.
2. Identificar MyFirebaseMessagingService y MyService.
3. Revisar Manifest y permisos de batería/background/boot.
4. Revisar WakeLock.
5. Ajustar exclusión de optimización cuando sea compatible.
6. Mejorar recuperación tras boot/update.
7. Mantener intacta la lógica de bloqueo/desbloqueo.
8. Compilar APK de prueba y validar en dispositivo real.

## Limitaciones

La APK no incluye el código fuente original. La reconstrucción desde bytecode puede requerir correcciones manuales. No se considerará producción hasta validar FCM, Device Owner, bloqueo/desbloqueo, pantalla apagada, reinicio y restricciones de batería.

La APK original permanece intacta; los cambios se realizan en la rama mdm-anti-suspension.
