# 🌈 Suavizado de Imágenes a Color con Filtro de Promedio en Python 🐍

Te presento un sencillo pero poderoso Filtro de Promedio implementado en Python, que te permitirá suavizar tus imágenes y reducir el ruido de manera eficiente.

🚀 ¿Qué hace este código?
Este script utiliza la biblioteca PIL (Python Imaging Library) para cargar imágenes y NumPy para manejar matrices. Su función principal es aplicar un filtro de promedio a cada canal de color (Rojo, Verde y Azul) de una imagen, creando una versión suavizada que resalta la belleza de los colores.

🔍 Características Clave:
•	Suavizado Efectivo: Reduce el ruido en las imágenes, mejorando su apariencia general.
•	Múltiples Iteraciones: Aplica el filtro tantas veces como desees para un efecto más pronunciado.
•	Visualización Instantánea: Muestra la imagen original y la suavizada para comparar resultados.

📜 Cómo Funciona
1.	Carga de la Imagen: Utiliza PIL para abrir la imagen deseada.
2.	Separación de Canales: Divide la imagen en sus componentes de color.
3.	Aplicación del Filtro: Calcula el promedio de cada píxel y sus vecinos.
4.	Reconstrucción de la Imagen: Combina los canales suavizados en una nueva imagen.
5.	Guardar y Mostrar: Guarda la imagen resultante y la muestra junto a la original.

🎨 Ejemplo de Uso
python
apply_average_filter_color('imagen2.png', 'imagen_salida.png', 1)

💡 ¿Por Qué Usar Este Código?
•	Simplicidad: Fácil de implementar y adaptar a tus necesidades.
•	Versatilidad: Ideal para proyectos de procesamiento de imágenes, desde fotografía hasta análisis de datos visuales.
•	Código Abierto: Modifica y mejora el código según tus requerimientos.

🌟 
[Ver Código de Filtro de promedio](vecinos_matrix _ color.md)


Descarga el código y comienza a experimentar con tus propias imágenes. ¡Comparte tus resultados y mejoras con la comunidad!

📥 
[Descargar Código de Filtro de promedio](vecinos_matrix _ color.md)

