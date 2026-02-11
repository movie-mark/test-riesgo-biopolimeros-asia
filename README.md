# Formulario Embebible Progresivo - Cliente

Formulario de evaluación progresivo personalizado para Cliente.

## 📋 Descripción

Este formulario permite recopilar información de manera progresiva, mostrando una pregunta a la vez para mejorar la experiencia del usuario. El diseño está personalizado según el sitio web de Cliente.

## 🚀 Características

- **Formulario progresivo**: Una pregunta a la vez con transiciones suaves
- **Diseño personalizado**: Adaptado al diseño de 
- **Responsive**: Funciona perfectamente en móvil y desktop
- **Validación en tiempo real**: Campos obligatorios con validación inmediata
- **20 preguntas**: Evaluación completa del cliente
- **Guardado de respuestas**: Las respuestas se guardan en formato JSON

## 📁 Estructura del Proyecto

```
.
├── form.html              # Formulario principal (embebible)
├── results/               # Página de resultados (a implementar)
│   └── README.md          # Instrucciones para la página de resultados
├── config.json            # Configuración del formulario
├── README.md              # Este archivo
└── .gitignore             # Archivos ignorados por Git
```

## 🔧 Instalación y Uso

### Opción 1: Embebido con iframe

Copia el siguiente código en tu página web:

```html
<iframe 
  src="form.html" 
  width="100%" 
  height="800" 
  frameborder="0"
  style="border: none; max-width: 600px; margin: 0 auto; display: block;">
</iframe>
```

### Opción 2: Copiar código directamente

1. Abre `form.html`
2. Copia todo el contenido
3. Pégalo donde quieras que aparezca el formulario en tu página

### Opción 3: Hosting estático

Puedes subir este proyecto completo a:
- GitHub Pages
- Netlify
- Vercel
- Cualquier servicio de hosting estático

## 📊 Datos Recopilados

El formulario recopila:
- Nombre completo (obligatorio)
- Correo electrónico (obligatorio)
- Respuestas a 20 preguntas de evaluación

Las respuestas se guardan en `localStorage` y se pueden enviar a un endpoint configurado.

## 🎨 Personalización

El diseño del formulario está basado en el análisis de . Los colores, fuentes y estilos se adaptan automáticamente al diseño del sitio.

Para personalizar manualmente, edita las variables CSS en `form.html`:

```css
:root {
  --form-primary-color: #tu-color;
  --form-secondary-color: #tu-color;
  /* ... más variables ... */
}
```

## 📤 Subir a GitHub

1. Inicializa un repositorio Git en esta carpeta:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Formulario embebible progresivo"
   ```

2. Crea un nuevo repositorio en GitHub

3. Conecta y sube:
   ```bash
   git remote add origin https://github.com/tu-usuario/tu-repo.git
   git branch -M main
   git push -u origin main
   ```

4. (Opcional) Activa GitHub Pages para hosting automático

## 🔗 Página de Resultados

La carpeta `results/` está preparada para alojar la página de resultados. Esta página mostrará:
- Resultados de la evaluación
- Recomendaciones personalizadas
- Call-to-action según las respuestas

**Nota**: La página de resultados se generará en un workflow futuro.

## 📝 Configuración

El archivo `config.json` contiene toda la configuración del formulario:
- Preguntas generadas
- Análisis de diseño
- URLs configuradas
- Metadatos

## 🛠️ Desarrollo

Este formulario fue generado automáticamente usando el workflow `generate_embeddable_form`.

### Tecnologías
- HTML5
- CSS3 (Variables CSS)
- JavaScript (Vanilla)
- Sin dependencias externas

## 📄 Licencia

Este proyecto es propiedad de Cliente.
