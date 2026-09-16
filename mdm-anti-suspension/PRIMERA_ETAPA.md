# AnCar MDM — Primera etapa

## Objetivo
Entregar una APK de prueba basada en la APK original, conservando la lógica MDM existente y mejorando su resiliencia frente a restricciones de batería y reinicios.

## Incluye
- Firebase Cloud Messaging existente.
- DeviceAdminReceiver existente.
- DevicePolicyManager existente.
- Foreground service existente.
- WakeLock existente.
- RECEIVE_BOOT_COMPLETED.
- REQUEST_IGNORE_BATTERY_OPTIMIZATIONS cuando Android lo permita.
- Preservación de bloqueo/desbloqueo existente.
- Compilación y firma reproducibles.
- SHA-256 del artefacto.

## No se declara como logrado
- Anti-desinstalación fuerte: requiere Device Owner/provisioning y prueba real.
- Reinstalación silenciosa después de factory reset: requiere Android Enterprise/Knox.
- Compatibilidad universal con fabricantes.
- Funcionamiento correcto en todos los modos Doze/OEM sin prueba de hardware.

## Criterio de aceptación
La APK debe compilar, firmarse, instalarse y conservar sus componentes MDM detectados. Las funciones de FCM, bloqueo/desbloqueo, reinicio y comportamiento frente a batería deben verificarse en hardware real antes de producción.
