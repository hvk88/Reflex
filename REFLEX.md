 

Aquí te muestro cómo crear un componente completo con video y agregarlo a la ruta principal:

```python
import reflex as rx

# Definimos los estilos optimizados para el video
video_style = {
    "border": "2px solid #32a1ce",  # Un borde más limpio
    "borderRadius": "8px",  # Bordes redondeados suaves
    "boxShadow": "4px 4px 8px rgba(50, 161, 206, 0.5)",  # Sombra más sutil
    "margin": "20px auto",  # Centrar y espaciado automático
    "maxWidth": "100%",  # Responsivo para pantallas más pequeñas
    "padding": "5px",  # Espaciado interno leve
}

def video() -> rx.Component:
    return rx.container(
        rx.video(
            "iframe",
            src="https://www.youtube.com/embed/HvFm4GcBlGs",
            width="560",
            height="315",
            style=video_style,
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share",
            frameborder="0",
            allowfullscreen=True,
        ),
        style={"textAlign": "center"},  # Centrar el contenedor
    )

```
 [(1)](https://reflex.dev/docs/library/media/video/) ,  [(2)](https://reflex.dev/docs/getting-started/chatapp-tutorial/) 

Este código:
1. Importa Reflex
2. Define los estilos del video en un diccionario
3. Crea una función `index()` que retorna el componente video dentro de un contenedor
4. Crea la app y agrega la página index como ruta principal

El video se mostrará en la ruta principal de tu aplicación (http://localhost:3000) cuando ejecutes `reflex run` .
<iframe width="560" height="315" src="https://www.youtube.com/embed/HvFm4GcBlGs?si=7fDFpXEYkrEwZ3Ip" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
