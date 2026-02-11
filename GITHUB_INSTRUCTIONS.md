# Instrucciones para Subir a GitHub y Desplegar en Vercel

## 📦 Estructura del Proyecto

Este proyecto está listo para ser subido a GitHub y desplegado en Vercel. Incluye:

```
tu-repo/
├── form.html              # Formulario principal embebible
├── results/               # Página de resultados (a implementar)
│   └── index.html         # Página de aterrizaje de resultados
├── config.json            # Configuración del formulario
├── vercel.json            # Configuración para Vercel
├── README.md              # Documentación
├── .gitignore             # Archivos ignorados
└── GITHUB_INSTRUCTIONS.md # Este archivo
```

## 🚀 Pasos para GitHub

### 1. Inicializar Git

```bash
git init
git add .
git commit -m "Initial commit: Formulario embebible progresivo"
```

### 2. Crear Repositorio en GitHub

- Ve a https://github.com/new
- Crea un nuevo repositorio (puede ser privado o público)
- **NO** inicialices con README, .gitignore o licencia (ya los tenemos)

### 3. Conectar y Subir

```bash
git remote add origin https://github.com/TU-USUARIO/TU-REPO.git
git branch -M main
git push -u origin main
```

## ⚡ Desplegar en Vercel

### Opción 1: Desde GitHub (Recomendado)

1. **Conectar GitHub a Vercel**:
   - Ve a https://vercel.com
   - Inicia sesión con tu cuenta de GitHub
   - Haz clic en "Add New Project"
   - Selecciona el repositorio que acabas de crear

2. **Configuración del Proyecto**:
   - Framework Preset: **Other** (o "Static Site")
   - Root Directory: `./` (raíz del proyecto)
   - Build Command: (dejar vacío, es un sitio estático)
   - Output Directory: `./` (raíz del proyecto)

3. **Desplegar**:
   - Haz clic en "Deploy"
   - Vercel detectará automáticamente el `vercel.json` y configurará las rutas

4. **URLs Generadas**:
   - Formulario: `https://TU-PROYECTO.vercel.app/form.html`
   - Página de resultados: `https://TU-PROYECTO.vercel.app/results/`

### Opción 2: Desde la Terminal (Vercel CLI)

```bash
# Instalar Vercel CLI (si no lo tienes)
npm i -g vercel

# Desde la carpeta del proyecto
vercel

# Seguir las instrucciones interactivas
# Para producción:
vercel --prod
```

## 📄 GitHub Pages (Alternativa)

Si prefieres usar GitHub Pages:

1. Ve a Settings > Pages en tu repositorio
2. Selecciona la rama `main` como fuente
3. El formulario estará disponible en: `https://TU-USUARIO.github.io/TU-REPO/form.html`

**Nota**: Vercel es más rápido y ofrece mejor rendimiento para sitios estáticos.

## 🔧 Configuración de Vercel

El archivo `vercel.json` está configurado para:
- Servir el formulario en `/form.html`
- Servir la página de resultados en `/results/`
- Redirecciones automáticas si es necesario
- Headers de seguridad apropiados

## 📝 Notas Importantes

- El archivo `config.json` contiene información sensible del cliente, considera si debe ser público
- La carpeta `results/` contiene la página de aterrizaje de resultados
- Puedes personalizar el README.md según las necesidades del cliente
- Cada vez que hagas `git push`, Vercel desplegará automáticamente (si está conectado)

## 🔄 Actualizaciones Futuras

Cuando generes la página de resultados, simplemente:
1. Agrega `results/index.html` al proyecto
2. Haz commit y push
3. Vercel desplegará automáticamente la nueva versión
