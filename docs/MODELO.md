# Modelo de simulación — Alcance y límites

## Entradas

El simulador utiliza especificaciones del motorreductor, especialmente RPM de salida sin carga y bajo carga nominal, tensión, y geometría del rodillo y de la banda. Las RPM del eje de salida **ya incluyen** la reducción interna del motorreductor: no se debe aplicarla nuevamente.

## Velocidad lineal

Para un rodillo de diámetro efectivo `D` en metros y velocidad `N` en revoluciones por minuto, sin deslizamiento:

`v = π · D · N / 60` (m/s)

La velocidad visual de la banda se basa en esta cinemática y en los parámetros de geometría. La pantalla puede representar mal velocidades altas por su frecuencia de refresco.

## Limitaciones

La carga del cabello, fricción, deslizamiento, deformación de la banda, par dinámico y características eléctricas reales requieren medición. Las aproximaciones de voltaje, corriente y torque no sustituyen las curvas del fabricante ni la validación física. La elección de una velocidad visual por el cliente **no demuestra seguridad** de contacto con el cabello.
