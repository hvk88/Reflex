 

Aquí te muestro cómo crear un componente completo con video y agregarlo a la ruta principal:

```python
import reflex as rx

# Definimos los estilos para el video
video_style = {
    "border": "thick double #32a1ce",
    "border_radius": "10px",
    "box_shadow": "12px 12px 2px 1px rgba(0, 0, 255, .2)",
    "margin": "10px",
    "padding": "10px"
}

def index() -> rx.Component:
    return rx.container(
        rx.video(
            url="https://www.youtube.com/embed/9bZkp7q19f0",
            width="400px",
            height="auto",
            style=video_style
        )
    )

# Agregamos la página a la app
app = rx.App()
app.add_page(index)
```
 [(1)](https://reflex.dev/docs/library/media/video/) ,  [(2)](https://reflex.dev/docs/getting-started/chatapp-tutorial/) 

Este código:
1. Importa Reflex
2. Define los estilos del video en un diccionario
3. Crea una función `index()` que retorna el componente video dentro de un contenedor
4. Crea la app y agrega la página index como ruta principal

El video se mostrará en la ruta principal de tu aplicación (http://localhost:3000) cuando ejecutes `reflex run` .
<iframe width="560" height="315" src="https://www.youtube.com/embed/HvFm4GcBlGs?si=7fDFpXEYkrEwZ3Ip" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
