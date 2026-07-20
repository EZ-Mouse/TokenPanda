# Manual de usuario de TokenPanda

## ¿Qué es?

TokenPanda muestra dentro de World of Warcraft el precio actual y el historial de la Ficha de WoW.

La microaplicación **TokenPandaTray** descarga y sincroniza los datos usados por el addon.

## Instalación

### Addon

1. Cierra World of Warcraft.
2. Extrae el ZIP.
3. Copia la carpeta `TokenPanda` en:

```text
World of Warcraft/_classic_/Interface/AddOns/
```

La ruta correcta debe terminar así:

```text
Interface/AddOns/TokenPanda/TokenPanda.toc
```

### TokenPandaTray

1. Extrae su ZIP en una carpeta.
2. Ejecuta `TokenPandaTray.exe`.
3. Selecciona la carpeta de WoW Classic.
4. Selecciona tu región: US, EU, KR o TW.
5. Activa la sincronización.

No necesita instalación tradicional.

## Abrir TokenPanda

Dentro del juego escribe:

```text
/tokenpanda
```

También puedes usar el icono del minimapa.

## Controles

### Icono del minimapa

- **Clic izquierdo:** mostrar u ocultar TokenPanda.
- **Arrastrar:** mover el icono.
- **Clic derecho:** mostrar u ocultar el menú.

### Ventana

- El selector inferior derecho cambia el periodo.
- El botón de minimizar cambia a la vista compacta.
- El clic derecho sobre ese botón alterna entre vista normal y análisis.
- Cada tamaño conserva su propia posición.

## Periodos

```text
3D · 7D · 14D · 1M · 3M · 6M · ALL
```

- Línea amarilla: periodo actual.
- Línea roja: periodo anterior equivalente.

## Alertas

TokenPanda puede indicar:

- precio en descenso;
- cercanía al mínimo;
- precio igual al mínimo;
- nuevo mínimo;
- precio alejándose del mínimo.

Las alertas son visuales y no interrumpen el juego.

## “Sin historial”

1. Comprueba que TokenPandaTray esté abierto.
2. Confirma que la sincronización esté activa.
3. Revisa la carpeta y la región.
4. Espera la primera sincronización.
5. Usa `/reload` si WoW ya estaba abierto.

## Actualizar

1. Cierra completamente WoW y TokenPandaTray.
2. Reemplaza la carpeta antigua por la nueva.
3. Conserva `HistoricalData.lua` solo cuando las notas indiquen compatibilidad.
4. Inicia TokenPandaTray y luego WoW.

No mezcles archivos de versiones distintas.

## Problemas frecuentes

### El addon no aparece

Evita una carpeta duplicada:

```text
Incorrecto:
AddOns/TokenPanda/TokenPanda/TokenPanda.toc

Correcto:
AddOns/TokenPanda/TokenPanda.toc
```

### Aparecen claves como `ALERT_FALLING`

Cierra WoW por completo, reemplaza toda la carpeta del addon y vuelve a iniciar.

### El gráfico no cambia

Confirma que TokenPandaTray esté sincronizando la región correcta.

## Seguridad y privacidad

TokenPandaTray:

- no solicita contraseña;
- no inicia sesión en Blizzard;
- no modifica el ejecutable del juego;
- solo descarga datos públicos y actualiza archivos del addon.

## Proyecto independiente

TokenPanda no es un producto oficial de Blizzard Entertainment ni está afiliado a otros servicios externos.

**EZ-Mouse Dev. — Obsesionados con la perfección.**
