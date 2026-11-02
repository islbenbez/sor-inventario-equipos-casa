

- **Alumno:** islem benbeztout
- **Bloque:** B0 — Prerrequisitos
- **Fase / ejercicio:** Fase 0.8
- **Fecha de inicio:** 2/11/2026
- **Fecha de entrega:** 2/11/2026

---

## 🎯 Qué se pedía

Crear una bóveda independiente en Obsidian (`Boveda_Inventario_Casa`) con su repositorio Git (`sor-inventario-equipos-casa`) dentro de `01_Proyecto` para llevar el inventario de unos equipos[1][2]. Había que registrar el avance en tres versiones (commits/push), ignorar archivos de vídeo con `.gitignore`, revisar el estado inicial viajando en el historial y publicar el vídeo con la bitácora en un commit final[1]

## ⌨️ Comandos y pasos importantes
- `pwd` — Comprobar la ruta actual para no inicializar Git en el sitio equivocado[8].
- `git init` — Inicializar el repositorio local dentro de la carpeta `01_Proyecto`[9].
- `git branch -M main` — Renombrar la rama principal a `main`[9].
- `git remote add origin git@github.com:TU-USUARIO/sor-inventario-equipos-casa.git` — Vincular el repo local con GitHub mediante SSH[10].
- `git add


## 🛠️ Qué he hecho

- **Estructura e inicio:** Creé la bóveda `Boveda_Inventario_Casa` fuera de OneDrive y carpetas de clase[16][17]. En `01_Proyecto` creé la bitácora, el `.gitignore` (excluyendo `.mp4`), el `README.md` y el CSV inicial `inventario/equipos.csv` con dos equipos (`EQ01` y `EQ02`)[2].
- **Git y primer push:** Inicialicé Git en `01_Proyecto`, añadí el remoto de GitHub por SSH y guardé la primera versión ("Crear inventario inicial de equipos")[4].
- **Segunda versión:** Modifiqué `equipos.csv` (moví `EQ01` a Aula-3 y puse `EQ02` en mantenimiento) y subí el segundo commit[13][20].
- **Ampliación y recursos ignorados:** Añadí las carpetas de mantenimiento, imágenes y vídeos[21]. Creé la ficha `EQ02.md`, `criterios-estados.md`, una imagen `equipo.png`, registré el equipo `EQ03` en el CSV y actualicé el `README.md`[21]. Puse dos vídeos `.mp4` locales para probar que `.gitignore` los ignoraba con `git check-ignore`[14][24]. Hice `add` archivo por archivo y subí el tercer commit[5].
- **Consulta histórica:** Viajé al primer commit con `git switch --detach` para comprobar que el CSV regresaba a su estado original, y luego volví a `main`[6][15].
- **Cierre:** Detuve la grabación de OBS, subí el vídeo a YouTube dentro de la playlist solicitada con las 9 marcas de tiempo y cerré la bitácora en un cuarto commit documental[7].

## 🚩 Qué me ha fallado y cómo lo he resuelto

**Comprobación de ruta inicial:** Al principio casi ejecuto `git init` en la raíz de la bóveda en lugar de dentro de `01_Proyecto`[9]. Lo detecté a tiempo ejecutando `pwd`, me cambié de directorio a `01_Proyecto` y ya inicialicé correctamente

## 🤔 Respuestas a las preguntas

- **¿Por qué el repositorio está en** **01_Proyecto** **y no en la raíz de la bóveda?** Porque la raíz contiene configuraciones de Obsidian (`.obsidian/`) y archivos de grabación (`00_Grabaciones/`) que no deben versionarse con el código del producto[2].
- **¿Qué dos celdas de datos cambiaste en la segunda versión y cómo se ven en diff?** La ubicación de `EQ01` (de `Aula-1` a `Aula-3`) y el estado de `EQ02` (de `disponible` a `mantenimiento`)[20]. En `git diff`, las líneas cambiadas muestran en rojo con `-` los valores anteriores y en verde con `+` los nuevos[31].
- **¿Qué diferencia hay entre editar una fila y preparar ese cambio con add?** Editar solo modifica el fichero localmente en el disco[32]. Usar `git add` mueve esa modificación al índice (staging area), dejándola lista para incluirse en el próximo commit[10][32].
- **¿Por qué la ficha nueva aparece en status y no en el diff de equipos.csv?** Porque la ficha es un archivo nuevo sin seguimiento (`??`), mientras que `git diff -- equipos.csv` solo analiza las modificaciones hechas dentro del fichero CSV[14].
- **¿Qué archivos preparaste individualmente en la ampliación y qué mostró diff --cached?** Se prepararon uno a uno: `EQ02.md`, `criterios-estados.md`, `equipo.png`, `equipos.csv` y `README.md`[12]. `git diff --cached` enseñó los cambios exactamente preparados en el índice antes de enviarlos[34].
- **¿Cómo demostraste que los clips existen y están ignorados sin subirlos?** Usando `git check-ignore -v inventario/videos/revision-01.mp4 inventario/videos/revision-02.mp4`, comprobando la regla de `.gitignore` que los bloquea sin borrarlos del disco[14].
- **¿Qué ubicación y estado recuperaste al visitar el primer commit y qué ocurrió con EQ03?** `EQ01` volvió a `Aula-1` y `EQ02` a `disponible`[6]. El equipo `EQ03` y los archivos creados posteriormente desaparecieron del entorno de trabajo porque aún no existían en ese commit[6].
- **¿Por qué este CSV necesita historial y qué limitaciones tiene frente a un inventario multiusuario real?** Necesita historial para auditar y rastrear cambios en los equipos[35][36]. Limita porque no permite edición en tiempo real ni simultánea por varios usuarios, no maneja permisos ni valida los datos introducidos[36].
- **¿Cómo comprobaste la subida de la bitácora y por qué su cierre ocurre después del vídeo?** Comprobando la nota subida en GitHub y verificando que abrieran los enlaces de YouTube[7]. Ocurre después porque la grabación debe mostrar el proceso de los tres commits terminados antes de incluir la URL del vídeo finalizado en la bitácora
## 🔗 Enlaces

- **Vídeo de esta fase:**  https://youtu.be/x_BosIWOdf8?si=_LgeGuFebyeGQohy
-
- **Playlist:** https://www.youtube.com/playlist?list=PLaMM-WHiImLo

## 💭 Dudas / a repasar

- (lo que no te ha quedado claro)