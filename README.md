# Cuerda Studio

Workspace web para practicar guitarra: metrónomo, afinador cromático, progresiones aleatorias y solos con tablatura.

## Funciones

- Metrónomo de 30–240 BPM, compases, subdivisiones y tap tempo.
- Afinador por micrófono y tonos de referencia con calibración A4.
- Progresiones de 4 u 8 compases en ocho tonalidades.
- Solos en negras o corcheas basados en los acordes, con tablatura.
- Base y solo sintetizados con volumen independiente, clic y repetición.
- Temporizador, rutina diaria y notas guardadas en el navegador.

## Ejecutar localmente

Sin compilación ni dependencias de JavaScript. Desde la raíz:

```bash
python -m http.server 8080 --directory dist
```

Abre http://localhost:8080. El micrófono requiere localhost o HTTPS y permiso del navegador. El análisis de audio ocurre localmente; no se graba ni se envía audio. La reproducción requiere interacción del usuario. Al ocultar la pestaña se detienen el metrónomo y la práctica.

## Estructura

- `dist/index.html`: interfaz.
- `dist/style.css`: estilos adaptables.
- `dist/app.js`: metrónomo, afinador, biblioteca y sesiones.
- `dist/music.mjs`: generación musical.
- `dist/practice.js`: tablatura y reproducción.

## Publicación

Sirve `dist/` en un alojamiento estático con HTTPS.

Sitio actual: https://cuerda-studio-daniel.open-bream-3251.chatgpt.site

La versión de Sites se publica por separado; los cambios en GitHub no se despliegan automáticamente. Se omite la configuración interna de Sites para que este repositorio sea independiente.

## Límites

El sonido es sintetizado, sin muestras reales de guitarra. La afinación depende del micrófono y del ruido ambiente. Las notas y la rutina se guardan sólo en el navegador utilizado. Las fuentes se cargan desde Google Fonts, con alternativas locales.
