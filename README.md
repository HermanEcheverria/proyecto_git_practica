
# 🎓 Galería de Perfiles del Equipo - Proyecto de Práctica con Git

¡Bienvenido al proyecto de práctica con Git y GitHub! Este es un proyecto web interactivo donde aprenderás a trabajar con el flujo de trabajo completo de Git: fork, clone, branch, commit, push, pull requests y merge.

## 📋 Descripción del Proyecto

Este proyecto es una **Galería de Perfiles de Equipo** donde cada alumno puede agregar su propia tarjeta de perfil. La página web muestra todos los perfiles, haciendo que sea fácil conocer a todos los miembros del equipo.

Cada perfil incluye:
- ✅ Nombre completo
- ✅ Rol o especialidad
- ✅ Una breve descripción personal
- ✅ Enlaces a redes sociales (opcional)

## 🎯 Objetivo del Ejercicio

El objetivo principal de este proyecto es que practiques y domines:

1. **Fork de repositorios** - Crear tu propia copia del proyecto
2. **Clonación de repositorios** - Descargar el código a tu máquina local
3. **Creación de branches** - Trabajar en ramas separadas para nuevas funcionalidades
4. **Commits descriptivos** - Guardar cambios con mensajes claros
5. **Push a GitHub** - Subir tus cambios al repositorio remoto
6. **Pull Requests** - Solicitar que tus cambios se integren al proyecto principal
7. **Revisión de código** - Entender el proceso de revisión y feedback
8. **Merge de cambios** - Integrar código al branch principal

## 📦 Requisitos Previos

Antes de comenzar, asegúrate de tener:

- ✅ **Git instalado** en tu computadora ([Descargar Git](https://git-scm.com/downloads))
- ✅ **Una cuenta en GitHub** ([Crear cuenta](https://github.com/join))
- ✅ **Un editor de código** (VS Code, Sublime Text, etc.)
- ✅ **Conocimientos básicos de HTML/JSON** (para crear tu perfil)

### Verificar instalación de Git

Abre tu terminal o línea de comandos y ejecuta:

```bash
git --version
```

Si ves un número de versión, ¡Git está instalado correctamente! 🎉

## 🚀 Instrucciones Paso a Paso

### Paso 1: Fork del Repositorio

1. Ve al repositorio original en GitHub
2. Haz clic en el botón **"Fork"** en la esquina superior derecha
3. Esto creará una copia del repositorio en tu cuenta de GitHub

![Fork](https://docs.github.com/assets/cb-34352/images/help/repository/fork-button.png)

### Paso 2: Clonar el Repositorio

Ahora necesitas descargar el código a tu computadora:

```bash
# Clona tu fork (reemplaza TU-USUARIO con tu nombre de usuario de GitHub)
git clone https://github.com/TU-USUARIO/proyecto_git_practica.git

# Entra al directorio del proyecto
cd proyecto_git_practica
```

### Paso 3: Crear un Nuevo Branch

**¡MUY IMPORTANTE!** Nunca trabajes directamente en el branch `main` o `master`. Siempre crea un nuevo branch para tus cambios.

```bash
# Crea y cambia a un nuevo branch con tu nombre
# Ejemplo: agregar-perfil-juan, agregar-perfil-maria, etc.
git checkout -b agregar-perfil-tunombre

# Verifica que estás en el branch correcto
git branch
```

El asterisco (*) debe aparecer junto al nombre de tu nuevo branch.

### Paso 4: Agregar tu Perfil

Ahora viene la parte divertida: crear tu propio perfil.

#### 4.1. Crea tu archivo JSON

1. Ve a la carpeta `profiles/`
2. Crea un nuevo archivo con el formato: `tu-nombre-apellido.json`
   - Ejemplo: `juan-perez.json`, `maria-garcia.json`
3. Usa el archivo `ejemplo.json` como referencia

#### 4.2. Estructura del archivo de perfil

Tu archivo debe tener esta estructura (copia y modifica):

```json
{
    "nombre": "Tu Nombre Completo",
    "rol": "Tu Rol o Especialidad",
    "descripcion": "Una breve descripción sobre ti. ¿Qué te apasiona? ¿Qué estás aprendiendo?",
    "social": {
        "github": "https://github.com/tu-usuario",
        "linkedin": "https://linkedin.com/in/tu-perfil",
        "twitter": "https://twitter.com/tu-usuario",
        "email": "tu-email@example.com"
    }
}
```

**Notas importantes:**
- ✅ Todos los campos son obligatorios excepto los enlaces sociales
- ✅ Puedes omitir enlaces sociales que no tengas (borra la línea completa)
- ✅ La descripción debe tener entre 50-150 caracteres
- ✅ Asegúrate de que el JSON esté bien formateado (usa un validador si tienes dudas)

#### 4.3. Registra tu perfil

Abre el archivo `js/main.js` y agrega el nombre de tu archivo a la lista `archivosPerfiles`:

```javascript
const archivosPerfiles = [
    'ejemplo.json',
    'tu-nombre-apellido.json'  // ← Agrega esta línea
];
```

### Paso 5: Verificar tus Cambios Localmente

Antes de hacer commit, es buena práctica verificar que todo funcione:

1. Abre el archivo `index.html` en tu navegador
2. Verifica que tu perfil se muestre correctamente
3. Asegúrate de que los enlaces funcionen

### Paso 6: Hacer Commit de tus Cambios

Ahora que tu perfil está listo, es momento de guardarlo en Git:

```bash
# Ver qué archivos has modificado
git status

# Agregar los archivos al staging area
git add profiles/tu-nombre-apellido.json
git add js/main.js

# O agregar todos los cambios de una vez
git add .

# Hacer commit con un mensaje descriptivo
git commit -m "Agregar perfil de [Tu Nombre]"
```

**Consejos para buenos mensajes de commit:**
- ✅ Usa verbos en infinitivo: "Agregar", "Modificar", "Corregir"
- ✅ Sé específico sobre qué cambiaste
- ✅ Mantén el mensaje corto pero descriptivo
- ❌ Evita mensajes vagos como "cambios" o "update"

### Paso 7: Push a GitHub

Sube tus cambios a tu fork en GitHub:

```bash
# Push de tu branch al repositorio remoto
git push origin agregar-perfil-tunombre
```

Si es la primera vez que haces push de este branch, Git te lo indicará y creará el branch en GitHub.

### Paso 8: Crear un Pull Request

¡Casi terminas! Ahora debes solicitar que tus cambios se integren al proyecto principal:

1. Ve a tu fork en GitHub (https://github.com/TU-USUARIO/proyecto_git_practica)
2. Verás un mensaje amarillo que dice "Compare & pull request" - haz clic ahí
3. Asegúrate de que:
   - **Base repository**: El repositorio original
   - **Base branch**: `main` (del repositorio original)
   - **Head repository**: Tu fork
   - **Compare branch**: Tu branch (`agregar-perfil-tunombre`)
4. Escribe un título descriptivo: "Agregar perfil de [Tu Nombre]"
5. En la descripción, puedes agregar:
   ```
   ## Cambios realizados
   - Creado archivo de perfil tu-nombre-apellido.json
   - Actualizado main.js para incluir el nuevo perfil
   
   ## Checklist
   - [x] El archivo JSON está correctamente formateado
   - [x] Probé localmente que el perfil se muestra correctamente
   - [x] Seguí las convenciones de nombres de archivo
   ```
6. Haz clic en **"Create pull request"**

### Paso 9: Proceso de Revisión

Después de crear el Pull Request:

1. **El instructor revisará tu código**
   - Verificará que el JSON esté bien formado
   - Comprobará que sigues las convenciones del proyecto
   - Puede dejar comentarios o solicitar cambios

2. **Si se solicitan cambios:**
   ```bash
   # Haz los cambios solicitados en tu editor
   
   # Guarda y haz commit de los nuevos cambios
   git add .
   git commit -m "Corregir formato del perfil según feedback"
   
   # Push de los cambios (se actualizarán automáticamente en el PR)
   git push origin agregar-perfil-tunombre
   ```

3. **Una vez aprobado**, el instructor hará merge de tu Pull Request

4. **¡Felicidades!** Tu perfil ahora es parte del proyecto principal 🎉

### Paso 10: Actualizar tu Fork (Opcional)

Después de que tu PR sea aceptado, es buena práctica mantener tu fork actualizado:

```bash
# Vuelve al branch main
git checkout main

# Configura el repositorio original como "upstream" (solo la primera vez)
git remote add upstream https://github.com/USUARIO-ORIGINAL/proyecto_git_practica.git

# Descarga los cambios del repositorio original
git fetch upstream

# Fusiona los cambios en tu branch main local
git merge upstream/main

# Actualiza tu fork en GitHub
git push origin main
```

## 📚 Buenas Prácticas

### Commits

- **Haz commits frecuentes** - No esperes a terminar todo para hacer commit
- **Un commit = un cambio lógico** - No mezcles múltiples cambios no relacionados
- **Mensajes descriptivos** - Explica QUÉ y POR QUÉ, no cómo

Ejemplos de buenos mensajes:
```bash
✅ git commit -m "Agregar perfil de Juan Pérez"
✅ git commit -m "Corregir formato JSON en perfil"
✅ git commit -m "Actualizar descripción del perfil"
```

Ejemplos de malos mensajes:
```bash
❌ git commit -m "cambios"
❌ git commit -m "fix"
❌ git commit -m "asdfgh"
```

### Branches

- **Nombres descriptivos** - Usa nombres que indiquen qué se está haciendo
- **Usa guiones** - Separa palabras con guiones: `agregar-perfil-juan`
- **Minúsculas** - Mantén los nombres en minúsculas
- **Un branch por funcionalidad** - No mezcles múltiples características

### Pull Requests

- **Títulos claros** - Describe brevemente qué aporta tu PR
- **Descripción detallada** - Explica los cambios realizados
- **Revisa tu propio código** - Antes de crear el PR, revisa tus cambios
- **Responde a los comentarios** - Participa activamente en la revisión

### Archivos

- **Nombres consistentes** - Usa el formato `nombre-apellido.json`
- **JSON bien formateado** - Usa un validador JSON si tienes dudas
- **Sin espacios en nombres de archivo** - Usa guiones en lugar de espacios

## 🔧 Solución de Problemas Comunes

### Problema 1: "Permission denied" al hacer push

**Causa:** No has configurado tu autenticación con GitHub

**Solución:**
```bash
# Configura tu nombre de usuario y email
git config --global user.name "Tu Nombre"
git config --global user.email "tu-email@example.com"

# Considera usar SSH o un token de acceso personal
# Ver: https://docs.github.com/es/authentication
```

### Problema 2: Conflictos de merge

**Causa:** Alguien modificó el mismo archivo que tú

**Solución:**
```bash
# Actualiza tu branch con los últimos cambios
git pull upstream main

# Git marcará los conflictos en los archivos
# Abre los archivos y resuelve los conflictos manualmente
# Busca las líneas que contienen <<<<<<<, =======, y >>>>>>>

# Después de resolver:
git add .
git commit -m "Resolver conflictos de merge"
git push origin tu-branch
```

### Problema 3: "fatal: not a git repository"

**Causa:** No estás en el directorio del proyecto

**Solución:**
```bash
# Navega al directorio correcto
cd proyecto_git_practica

# Verifica que estás en el lugar correcto
pwd
```

### Problema 4: Mi perfil no se muestra en la página

**Posibles causas y soluciones:**

1. **JSON mal formateado:**
   - Verifica tu JSON en [JSONLint](https://jsonlint.com/)
   - Asegúrate de que todas las comillas sean dobles (")
   - Verifica que no falten comas

2. **Archivo no registrado en main.js:**
   - Verifica que agregaste tu archivo a la lista `archivosPerfiles`
   - Asegúrate de que el nombre coincide exactamente

3. **Error en la consola del navegador:**
   - Abre las herramientas de desarrollo (F12)
   - Ve a la pestaña "Console"
   - Busca mensajes de error

### Problema 5: "Your branch is behind"

**Causa:** El repositorio original tiene cambios nuevos

**Solución:**
```bash
# Actualiza tu branch
git pull upstream main

# Si hay conflictos, resuélvelos y luego:
git push origin tu-branch
```

## 💡 Comandos Git de Referencia Rápida

```bash
# Ver estado de los archivos
git status

# Ver diferencias antes de commit
git diff

# Ver historial de commits
git log
git log --oneline  # Versión compacta

# Cambiar de branch
git checkout nombre-branch

# Crear y cambiar a un nuevo branch
git checkout -b nombre-nuevo-branch

# Ver todos los branches
git branch -a

# Deshacer cambios en un archivo (antes de commit)
git checkout -- nombre-archivo

# Ver commits de forma gráfica
git log --graph --oneline --all

# Agregar un remote
git remote add nombre-remote url

# Ver remotes configurados
git remote -v

# Actualizar desde un remote
git fetch nombre-remote

# Fusionar cambios
git merge nombre-branch
```

## 🎓 Recursos Adicionales

### Documentación Oficial
- [Git - Documentación oficial](https://git-scm.com/doc)
- [GitHub Docs - Español](https://docs.github.com/es)

### Tutoriales Recomendados
- [Git y GitHub - Curso desde cero](https://www.youtube.com/watch?v=HiXLkL42tMU)
- [Pro Git Book (Español)](https://git-scm.com/book/es/v2)
- [Learn Git Branching (Interactivo)](https://learngitbranching.js.org/?locale=es_ES)

### Herramientas Útiles
- [JSONLint](https://jsonlint.com/) - Validador de JSON
- [GitKraken](https://www.gitkraken.com/) - Cliente gráfico de Git
- [GitHub Desktop](https://desktop.github.com/) - Cliente oficial de GitHub

### Cheat Sheets
- [Git Cheat Sheet (GitHub)](https://education.github.com/git-cheat-sheet-education.pdf)
- [Gitflow Cheatsheet](https://danielkummer.github.io/git-flow-cheatsheet/index.es_ES.html)

## ❓ Preguntas Frecuentes (FAQ)

### ¿Qué hago si cometí un error en mi commit?

Si aún no has hecho push:
```bash
# Modificar el último commit
git commit --amend -m "Mensaje corregido"
```

Si ya hiciste push, es mejor hacer un nuevo commit con la corrección.

### ¿Qué pasa si dos personas hacen push al mismo tiempo?

Git está diseñado para manejar esto. Si hay conflictos, Git te pedirá que los resuelvas manualmente antes de hacer merge.

## 📄 Licencia

Este proyecto es de código abierto y está disponible para fines educativos.

---

## 🎉 ¡Felicidades!

Si llegaste hasta aquí y completaste todos los pasos, ¡felicidades! Has aprendido el flujo de trabajo básico de Git y GitHub que usan millones de desarrolladores en todo el mundo.

### Próximos Pasos

1. **Practica más** - Intenta contribuir a otros proyectos open source
2. **Explora GitHub** - Descubre proyectos interesantes
3. **Aprende conceptos avanzados** - Rebase, stash, cherry-pick, etc.
4. **Comparte tu conocimiento** - Ayuda a otros que están aprendiendo

**¡Sigue aprendiendo y happy coding! 🚀👨‍💻👩‍💻**

---

**¿Necesitas ayuda?** No dudes en:
- Abrir un issue en GitHub
- Preguntar a tu instructor
- Consultar la documentación oficial de Git

**Recuerda:** Todos los desarrolladores experimentados alguna vez fueron principiantes. ¡No tengas miedo de cometer errores, así se aprende! 💪
