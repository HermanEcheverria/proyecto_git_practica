
# 📁 Carpeta de Perfiles

Esta carpeta contiene todos los archivos JSON de perfiles de los miembros del equipo.

## 🎯 Instrucciones para Agregar tu Perfil

### 1. Crea tu archivo JSON

Crea un nuevo archivo en esta carpeta con el formato:
```
tu-nombre-apellido.json
```

**Ejemplos:**
- `juan-perez.json`
- `maria-garcia.json`
- `carlos-rodriguez.json`

### 2. Usa esta plantilla

Copia y pega este código en tu archivo, luego modifica con tu información:

```json
{
    "nombre": "Tu Nombre Completo",
    "rol": "Tu Rol o Especialidad",
    "descripcion": "Una breve descripción sobre ti. ¿Qué te apasiona? ¿Qué estás aprendiendo? (50-150 caracteres)",
    "social": {
        "github": "https://github.com/tu-usuario",
        "linkedin": "https://linkedin.com/in/tu-perfil",
        "twitter": "https://twitter.com/tu-usuario",
        "email": "tu-email@example.com"
    }
}
```

### 3. Campos Obligatorios

✅ **nombre**: Tu nombre completo  
✅ **rol**: Tu especialidad o rol (ej: "Desarrollador Frontend", "Diseñador UI/UX")  
✅ **descripcion**: Breve descripción personal (50-150 caracteres)  

### 4. Campos Opcionales

Los enlaces de redes sociales son opcionales. Si no tienes alguna red social, puedes:

**Opción A:** Omitir todo el objeto social
```json
{
    "nombre": "Tu Nombre",
    "rol": "Tu Rol",
    "descripcion": "Tu descripción"
}
```

**Opción B:** Incluir solo las redes que uses
```json
{
    "nombre": "Tu Nombre",
    "rol": "Tu Rol",
    "descripcion": "Tu descripción",
    "social": {
        "github": "https://github.com/tu-usuario",
        "email": "tu-email@example.com"
    }
}
```

### 5. Redes Sociales Soportadas

- **github**: Tu perfil de GitHub
- **linkedin**: Tu perfil de LinkedIn
- **twitter**: Tu perfil de Twitter
- **email**: Tu correo electrónico
- **website**: Tu sitio web personal

### 6. Validar tu JSON

Antes de hacer commit, asegúrate de que tu JSON sea válido:

1. Ve a [JSONLint](https://jsonlint.com/)
2. Copia y pega tu código JSON
3. Haz clic en "Validate JSON"
4. Si hay errores, corrígelos

### 7. Registrar tu Perfil

Después de crear tu archivo JSON, debes registrarlo en `js/main.js`:

1. Abre el archivo `js/main.js`
2. Busca el array `archivosPerfiles`
3. Agrega el nombre de tu archivo:

```javascript
const archivosPerfiles = [
    'ejemplo.json',
    'tu-nombre-apellido.json'  // ← Agrega esta línea
];
```

### 8. Probar Localmente

Antes de hacer commit:

1. Abre `index.html` en tu navegador
2. Verifica que tu perfil se muestre correctamente
3. Comprueba que los enlaces funcionen

## ⚠️ Notas Importantes

- **No modifiques** archivos de otros perfiles sin permiso
- **Usa comillas dobles** (") en JSON, no simples (')
- **No olvides las comas** entre campos (pero no después del último)
- **Los URLs deben ser completos** (incluir https://)
- **Para email**, usa solo el correo, no el formato `mailto:`

## ❌ Errores Comunes

### Error: JSON no válido
```json
❌ Mal - comillas simples
{
    'nombre': 'Juan'
}

✅ Bien - comillas dobles
{
    "nombre": "Juan"
}
```

### Error: Coma extra
```json
❌ Mal - coma después del último campo
{
    "nombre": "Juan",
    "rol": "Developer",
}

✅ Bien - sin coma al final
{
    "nombre": "Juan",
    "rol": "Developer"
}
```

### Error: Falta coma
```json
❌ Mal - falta coma entre campos
{
    "nombre": "Juan"
    "rol": "Developer"
}

✅ Bien - con coma
{
    "nombre": "Juan",
    "rol": "Developer"
}
```

## 🆘 ¿Necesitas Ayuda?

Si tienes problemas:

1. Revisa el archivo `ejemplo.json` como referencia
2. Usa un validador JSON online
3. Pregunta a tu instructor
4. Consulta el README.md principal del proyecto

---

**¡Buena suerte y bienvenido al equipo! 🎉**
