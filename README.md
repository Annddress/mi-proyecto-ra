# 🚀 Mi Primera Experiencia de Realidad Aumentada

## ¿Qué es este proyecto?
Una aplicación web de Realidad Aumentada que muestra objetos 3D animados cuando apuntas la cámara de tu celular hacia una imagen marcador.

## Tecnologías utilizadas
- **MindAR.js** - Librería de RA para web (reconocimiento de imágenes)
- **A-Frame** - Framework para crear escenas 3D
- **HTML5/CSS3/JavaScript** - Tecnologías web estándar

---

## 📋 INSTRUCCIONES PASO A PASO

### PASO 1: Obtener el marcador

Este proyecto incluye **dos opciones de marcador**:

**Opción A - Marcador incluido** (`marcador-personalizado.png`):
- Es el marcador personalizado creado para este proyecto
- Para usarlo, primero debes compilarlo (ver sección "Usar marcador personalizado")

**Opción B - Marcador de ejemplo de MindAR** (configuración actual):
- El proyecto viene configurado con el marcador de ejemplo oficial
- Descárgalo de: https://cdn.jsdelivr.net/gh/hiukim/mind-ar-js@1.2.5/examples/image-tracking/assets/card-example/card.png
- ¡Funciona inmediatamente sin configuración adicional!

### PASO 2: Subir a un hosting gratuito

#### Opción A: Netlify Drop (Más fácil - Solo arrastra y suelta)
1. Ve a https://app.netlify.com/drop
2. Arrastra toda la carpeta `ra-proyecto` al área de deploy
3. ¡Listo! Recibirás una URL como: `https://random-name.netlify.app`

#### Opción B: GitHub Pages
1. Crea un repositorio en GitHub
2. Sube los archivos
3. Ve a Settings → Pages → Selecciona "main" branch
4. Tu URL será: `https://tuusuario.github.io/tu-repo`

#### Opción C: Vercel
1. Ve a https://vercel.com
2. Conecta tu GitHub o arrastra los archivos
3. Deploy automático

### PASO 3: Probar la experiencia
1. **Abre el marcador**: Imprime el marcador o ábrelo en otra pantalla
2. **Accede desde tu celular**: Visita la URL de tu proyecto (debe ser HTTPS)
3. **Permite la cámara**: Acepta los permisos cuando lo solicite
4. **Apunta al marcador**: ¡Verás los objetos 3D aparecer!

---

## 🎯 ¿Quieres usar tu PROPIA imagen como marcador?

### Paso 1: Compilar tu imagen
1. Ve al compilador online: https://hiukim.github.io/mind-ar-js-doc/tools/compile/
2. Sube tu imagen (mejor si tiene muchos detalles y contraste)
3. Haz clic en "Start" para compilar
4. Descarga el archivo `.mind` generado

### Paso 2: Actualizar el proyecto
1. Guarda el archivo `.mind` en la carpeta del proyecto (ej: `mi-marcador.mind`)
2. En `index.html`, cambia la línea del `imageTargetSrc`:
   ```
   mindar-image="imageTargetSrc: ./mi-marcador.mind; ...
   ```
3. ¡Listo! Ahora usa tu imagen como marcador

---

## 🎨 Qué verás en la experiencia

Cuando apuntes la cámara al marcador, aparecerá:
- ✨ Un cubo 3D rojo girando
- 🔵 Esferas orbitando alrededor
- 💬 Texto "¡Hola RA!" flotando
- 🔶 Un anillo dorado animado

---

## 🔧 Personalización

### Cambiar colores
En `index.html`, busca las líneas con `color=` y modifica los valores hexadecimales.

### Cambiar formas 3D
Puedes usar otras primitivas de A-Frame:
- `<a-sphere>` - Esfera
- `<a-cylinder>` - Cilindro  
- `<a-cone>` - Cono
- `<a-torus>` - Anillo/Donut

### Agregar modelos 3D personalizados
```html
<a-entity gltf-model="url(tu-modelo.glb)" scale="0.1 0.1 0.1"></a-entity>
```

---

## ❓ Solución de problemas

| Problema | Solución |
|----------|----------|
| La cámara no funciona | Asegúrate de usar HTTPS (no HTTP) |
| No detecta el marcador | Mejora la iluminación, evita brillos |
| Carga muy lento | Normal la primera vez, espera unos segundos |
| No aparece nada | Verifica que el marcador esté completo en cámara |

---

## 📚 Recursos adicionales

- [Documentación MindAR](https://hiukim.github.io/mind-ar-js-doc/)
- [Documentación A-Frame](https://aframe.io/docs/)
- [Compilador de marcadores MindAR](https://hiukim.github.io/mind-ar-js-doc/tools/compile/)

---

## 📝 Notas para la presentación

Este proyecto demuestra:
1. **Tracking de imágenes**: Reconocimiento visual en tiempo real
2. **Renderizado 3D**: Objetos tridimensionales sobre el mundo real
3. **Animaciones**: Movimientos fluidos y dinámicos
4. **Interactividad**: Feedback visual del estado de detección
5. **Compatibilidad web**: Funciona en cualquier dispositivo con navegador moderno

---

¡Éxito con tu presentación! 🎉
