# TP1 — Fundamentos del Diseño Web

Integrantes: Domé Florencia, Spinetta Carlos, Bahurlet Micaela

---

## Consigna del Proyecto

Se debe realizar el maquetado e implementación de un documento HTML que representa un ejemplo de un sitio web para un **centro médico**. La plantilla del documento se puede observar al final del enunciado.

### Pautas generales

- Esta actividad se realiza en **grupos de 2 personas**, y se evalúa el trabajo en equipo, la claridad y el esfuerzo empleado para la resolución.
- Se tendrá en cuenta el código realizado en HTML, evaluando particularmente la **selección de etiquetas** acordes al contenido que se debe ubicar en cada elemento.
- **No está permitido aplicar estilos visuales** por ningún medio.
- La estructura del documento debe respetar el contenido propuesto en la plantilla, pero **no es necesario lograr el posicionamiento vertical/lateral** tal cual se haya diseñado, ya que no se pueden utilizar estilos CSS como se indica en el punto anterior.
- Cada grupo debe crear e implementar una propuesta para el **formulario de contacto de reserva de cita**. El mismo debe estar vinculado como enlace del elemento cuyo contenido es *"Make an Appointment"* en la parte superior de la plantilla. Se debe crear un archivo `formulario.html` para resolver este punto.

### Entrega

La entrega debe consistir en un archivo comprimido que incluya:

1. Foto del **wireframe** propuesto (hecho a mano en papel o en PC — el formato no influye en la nota).
2. Archivo `index.html` con el contenido de la página principal.
3. Archivo `formulario.html` con el formulario de reserva.
4. Carpeta con las **imágenes** utilizadas.

### Fecha y modalidad de entrega

- La entrega del proyecto finalizado debe realizarse **antes del 30 de Abril**, mediante un módulo de TAREA que se habilitará en el aula virtual de la materia.
- Sólo debe realizar la entrega **un miembro** de cada grupo.
- En el archivo `index.html` debe aparecer al principio del `<body>` un comentario mencionando el **número de Grupo** y los **integrantes** que lo conforman.
- Solo entrega el responsable de la misma, mencionada en la planilla de registro de los grupos.

---

## Guía de Git paso a paso
Acá te explico todo lo que necesitás saber para trabajar en este proyecto sin romper nada.

---

### 1. ¿Qué es Git?

Git es una herramienta que nos permite **trabajar en equipo sobre los mismos archivos** sin pisarnos. Guarda un historial de todos los cambios, así que si algo sale mal, siempre podemos volver atrás.

**GitHub** es la plataforma en la nube donde está alojado nuestro repositorio (repo). Git es la herramienta que usamos desde nuestra computadora para interactuar con él.

---

### 2. Requisitos previos

- Tener **Git** instalado. Podés verificarlo abriendo una terminal y escribiendo:

```bash
git --version
```

Si no lo tenés instalado, descargalo desde [https://git-scm.com](https://git-scm.com).

- Tener una cuenta de **GitHub** y que te hayan dado acceso al repositorio.

---

### 3. Clonar el repositorio (bajar el proyecto a tu computadora)

Clonar significa **descargar una copia del proyecto** a tu máquina para poder trabajar en él.

1. Andá al repositorio en GitHub y copiá la URL (botón verde **"Code"** → copiá el enlace HTTPS).
2. Abrí una terminal y navegá a la carpeta donde querés guardar el proyecto, por ejemplo tu Escritorio.
3. Ejecutá:

```bash
git clone <URL_DEL_REPOSITORIO>
```

> Reemplazá `<URL_DEL_REPOSITORIO>` por la URL que copiaste. Por ejemplo:
> ```bash
> git clone https://github.com/usuario/tp1-DiseñoWeb.git
> ```

4. Esto va a crear una carpeta con el nombre del repo. Entrá a ella:

```bash
cd tp1-DiseñoWeb
```

¡Listo! Ya tenés el proyecto en tu computadora.

---

### 4. ¿Qué es una branch (rama)?

Una **branch** (rama) es como una **copia paralela** del proyecto donde podés hacer cambios sin afectar el trabajo de los demás.

Imaginate un árbol: el tronco principal es la rama `main`. Cada persona crea su propia rama (como una ramita que sale del tronco), trabaja ahí, y cuando termina, une sus cambios de vuelta al tronco.

**¿Por qué usamos ramas?**

- Para que cada uno pueda trabajar **sin molestar al otro**.
- Para poder **revisar** los cambios antes de juntarlos.
- Para evitar **conflictos** trabajando todos sobre el mismo archivo al mismo tiempo.

---

### 5. Crear tu propia branch para trabajar

Antes de tocar cualquier archivo, **siempre** creá una rama nueva. Nunca trabajes directamente sobre `main`. esa es la version estable del proyecto.

1. Primero, asegurate de estar en la rama `main` y tenerla actualizada:

```bash
git checkout main
git pull origin main
```

2. Creá una rama nueva con un nombre descriptivo:

```bash
git checkout -b nombre-de-tu-rama
```

> Ejemplo: si vas a trabajar en el formulario:
> ```bash
> git checkout -b formulario-contacto
> ```

Ahora estás parado en tu rama nueva. Todo lo que modifiques acá no va a afectar `main` hasta que lo decidamos.

---

### 6. Trabajar en tus archivos

Ahora simplemente **editá los archivos** que necesites con tu editor de código (por ejemplo, Visual Studio Code).

Podés abrir el proyecto desde VS Code con:

```bash
code .
```

Hacé los cambios que necesites en `index.html`, `formulario.html`, agregá imágenes a la carpeta, etc.

---

### 7. Ver qué archivos cambiaste

Cuando quieras ver qué modificaste, usá:

```bash
git status
```

Te va a mostrar en **rojo** los archivos modificados o nuevos que todavía no están preparados para subir.

---

### 8. Preparar los cambios (add)

Antes de guardar tus cambios en Git, tenés que **prepararlos** (esto se llama "agregar al staging area"):

- Para agregar **todos** los archivos modificados:

```bash
git add .
```

- Para agregar **un archivo específico**:

```bash
git add index.html
```

Si volvés a ejecutar `git status`, los archivos preparados van a aparecer en **verde**.

---

### 9. Guardar los cambios (commit)

Un **commit** es como un **punto de guardado**. Le ponemos un mensaje corto que describa qué hicimos:

```bash
git commit -m "Agrego la estructura básica del index.html"
```

> Escribí mensajes claros y en español, por ejemplo:
> - `"Agrego el header y la navegación"`
> - `"Creo el formulario de reserva"`
> - `"Agrego imágenes del banner"`

---

### 10. Subir los cambios a GitHub (push)

Hasta ahora, todo lo que hiciste está **solo en tu computadora**. Para que tu compañero pueda verlo y para que quede respaldado en la nube, tenés que subirlo:

```bash
git push origin nombre-de-tu-rama
```

> Ejemplo:
> ```bash
> git push origin formulario-contacto
> ```

La primera vez que subís una rama nueva, Git te puede pedir que configures el "upstream". Simplemente copiá el comando que te sugiere o usá:

```bash
git push --set-upstream origin nombre-de-tu-rama
```

---

### 11. Unir tu trabajo a main (Pull Request)

Cuando termines de trabajar en tu rama y quieras que tus cambios pasen a `main`:

1. Andá a **GitHub** en el navegador.
2. Vas a ver un cartel amarillo que dice algo como *"Compare & pull request"*. Hacé click ahí.
3. Escribí un título y descripción de lo que hiciste.
4. Hacé click en **"Create Pull Request"**.
5. Tu compañero (o vos mismo) puede **revisar** los cambios y luego apretar **"Merge"** para unirlos a `main`.

---

### 12. Actualizar tu rama con los últimos cambios

Si tu compañero ya subió cosas a `main` y vos necesitás tener esos cambios en tu rama:

```bash
git checkout main
git pull origin main
git checkout nombre-de-tu-rama
git merge main
```

Esto trae los últimos cambios de `main` y los combina con tu rama.

---

### Resumen rápido de comandos

| Acción | Comando |
|---|---|
| Clonar el repo | `git clone <URL>` |
| Ver en qué rama estás | `git branch` |
| Crear rama nueva y moverte a ella | `git checkout -b nombre-rama` |
| Cambiar de rama | `git checkout nombre-rama` |
| Ver qué archivos cambiaste | `git status` |
| Preparar cambios | `git add .` |
| Guardar cambios | `git commit -m "mensaje"` |
| Subir cambios a GitHub | `git push origin nombre-rama` |
| Traer últimos cambios de main | `git pull origin main` |
| Unir main con tu rama | `git merge main` |

---

### Tips importantes

- **Nunca trabajes directo en `main`**. Siempre creá una rama.
- **Hacé commits seguido**. Es mejor tener muchos commits chiquitos que uno gigante.
- **Escribí mensajes de commit claros**. Tu yo del futuro te lo va a agradecer.
- **Antes de empezar a trabajar**, siempre hacé `git pull origin main` para tener lo último.
- Si algo sale mal, **no borres nada**. Pedí ayuda o consultá en el grupo. 