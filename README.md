# 🌈 Suavizado de Imágenes a Color con Filtro de Promedio en Python 🐍

Te presento un sencillo pero poderoso Filtro de Promedio implementado en Python, que te permitirá suavizar tus imágenes y reducir el ruido de manera eficiente.

🚀 ¿Qué hace este código?
Este script utiliza la biblioteca PIL (Python Imaging Library) para cargar imágenes y NumPy para manejar matrices. Su función principal es aplicar un filtro de promedio a cada canal de color (Rojo, Verde y Azul) de una imagen, creando una versión suavizada que resalta la belleza de los colores.

🔍 Características Clave:
•	Suavizado Efectivo: Reduce el ruido y las variaciones bruscas de color en las imágenes, mejorando su apariencia general.
• Desenfoca ligeramente: Crea un efecto de suavizado sutil.
•	Preserva estructuras: Mantiene mejor los bordes verticales y horizontales que un filtro promedio tradicional.
•	Múltiples Iteraciones: Aplica el filtro tantas veces como desees para un efecto más pronunciado.
•	Visualización Instantánea: Muestra la imagen original y la suavizada para comparar resultados.

📜 Cómo Funciona

1.	Carga de la Imagen: Utiliza PIL para abrir la imagen deseada.
2.	Separación de Canales: Divide la imagen en sus componentes de color.
3.	Analiza cada píxel: Examina cada punto de la imagen.
4.	Considera los vecinos: Mira los 4 píxeles adyacentes (arriba, abajo, izquierda, derecha).
5.	Aplicación del Filtro: calcula un nuevo valor pomediando estos 5 píxeles (incluyendo el central).
6.	Actualiza la imagen: Reemplaza el píxel original con este nuevo promedio.
7.	Reconstrucción de la Imagen: Combina los canales suavizados en una nueva imagen.
8.	Guardar y Mostrar: Guarda la imagen resultante y la muestra junto a la original.


💡 ¿Por Qué Usar Este Código?

•	Eficiencia: Al usar solo 4 vecinos en lugar de 8, realizamos menos cálculos.
•	Efecto Único: Produce un suavizado que puede ser más sutil en ciertas direcciones.
•	Personalizable: Puedes ajustar la intensidad cambiando el número de iteraciones.
•	Simplicidad: Fácil de implementar y adaptar a tus necesidades.
•	Versatilidad: Ideal para proyectos de procesamiento de imágenes, desde fotografía hasta análisis de datos visuales.
•	Código Abierto: Modifica y mejora el código según tus requerimientos.

🌟 Puedes ver el código completo del filtro de promedio aquí:
[Ver Código de Filtro de promedio](vecinos_matrix_color.md)

📥 Puedes descargar el código completo del filtro de promedio aquí:
[Descargar Código de Filtro de promedio](vecinos_matrix_color.py)


