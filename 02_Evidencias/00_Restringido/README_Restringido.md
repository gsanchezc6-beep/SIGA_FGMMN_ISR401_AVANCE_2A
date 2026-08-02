# Zona restringida [R] — Acceso al contenedor cifrado

Esta carpeta corresponde a la **zona restringida** definida en la Sección 4.1 de la
Guía de Entrega 3 (2A). Contiene los datos personales identificables del trabajo de
campo, que **no se publican** en el repositorio abierto conforme a la Ley Orgánica de
Protección de Datos Personales del Ecuador.

## Contenido del contenedor

`evidencias_restringidas.7z` — cifrado con **AES-256** y con nombres de archivo
ocultos (`-mhe=on`):

| Material | Cantidad | Volumen |
|---|---|---|
| Videos de entrevista (MP4 H.264) | 9 | 4.7 GB |
| Audios de entrevista (WAV / MP3) | 11 | 274 MB |
| Consentimientos firmados con cédula y firma visibles | 10 | 8.8 MB |
| Actas de walkthrough firmadas | 5 | 1.1 MB |
| Documentos originales de la organización | 5 | 34 MB |

**Tamaño del contenedor:** 4.89 GB

## Por qué no está dentro del repositorio

El contenedor supera el límite de 100 MB por archivo de GitHub y la cuota de
almacenamiento de Git LFS disponible para el equipo. Se aloja en el OneDrive
institucional de la UTEQ, con acceso restringido.

## Acceso

**Ubicación:** OneDrive institucional UTEQ

https://uteqeduec-my.sharepoint.com/:f:/g/personal/gsanchezc6_msuteq_edu_ec/IgAIbQP1scbLQoCrcCWgqMbNAQrzV6V3SQg8yhuu2D1TZEc?e=3JJvgX

**Contraseña del contenedor:** entregada al docente por el Sistema de Gestión
Académica (SGA). No se transmite por ningún otro medio ni consta en este
repositorio.

## Verificación de integridad

El hash SHA-256 del contenedor está registrado en `checksums.sha256`, en la raíz del
repositorio. Para comprobar que el archivo descargado no fue alterado:

```
sha256sum -c checksums.sha256 --ignore-missing
```

O en Windows:

```
certutil -hashfile evidencias_restringidas.7z SHA256
```

y comparar el resultado con la línea correspondiente de `checksums.sha256`.

## Ficha técnica

`fichas_tecnicas.csv` acompaña a este documento **en claro**, conforme exige la guía.
Contiene, por cada evidencia: nombre de archivo, tipo, fecha, código de participante,
duración, códec, tamaño en bytes y hash SHA-256 calculado antes del cifrado.

Los códigos de participante (`DOC-01`, `CONS-02`, `COORD-03`, …) sustituyen a los
nombres propios, de modo que ni el nombre del archivo ni la ficha técnica constituyen
un dato identificable.
