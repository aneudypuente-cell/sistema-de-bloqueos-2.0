# MDM Anti-Suspensión

Rama de trabajo: `mdm-anti-suspension`

Objetivo: analizar y reconstruir la APK MDM antigua para mejorar su resistencia a optimización de batería, Doze, restricciones de segundo plano y reinicios, sin alterar la APK original ni la lógica existente de bloqueo/desbloqueo.

## Flujo de trabajo

1. Inventario y análisis estático de `MDM.apk`.
2. Identificación de servicios, receivers, FCM y Device Owner.
3. Reconstrucción de un proyecto Android modificable.
4. Implementación de mejoras de persistencia/background.
5. Compilación de una APK de prueba.
6. Pruebas con pantalla apagada, reinicio y recepción FCM.

## Regla

La APK original se conserva intacta. Ningún cambio de esta rama debe alterar producción hasta completar las pruebas.
