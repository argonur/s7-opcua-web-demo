# Backend
## Crear el entorno virtual de Python

1. En el caso del proyecto ya existe, lleva el nombre de `plc-remote` pero puedes borrarlo y crear uno limpio.

```bash
python -m venv venv
```

2. Para instalar los paquetes necesarios para que el backend se comporte correctamente lo puedes hacer desde el archivo requirements.txt

```bash
# 1.- Activamos el entorno virtual
source plc-remote/bin/activate
# 2.- Instalamos desde el requirements.txt
pip install -r requirements.txt
```

---
# Frontend
## Instalar Tailwind CSS
1. Se requiere instalar este framework para poder personalizar los estilos y que estos se vean en nuestro proyecto.

```bash
# Entra al directorio frontend/
npm install tailwindcss @tailwindcss/vite
```

2. Es necesario agregar el plugin de tailwindcss en el archivo de configuración de Vite.

- Nos dirigimos a la raíz del proyecto: vite.config.ts 
```typescript
import { defineConfig } from 'vite'
import tailwindcss from '@tailwindcss/vite' // importamos el plugin

export default defineConfig({
  plugins: [
    tailwindcss(), // se coloca aquí
  ],
})
```
---

3. Ultimo paso

- Por ultimo se importa al archivo CSS global del proyecto suele encontrarse dentro de src/  
```css
{/* src/index.css*/ }
@import "tailwindcss";
{/*
... aquí puede estar el resto de tu personalización CSS del frontend
*/}
```
