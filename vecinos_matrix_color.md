```Python
from PIL import Image
import numpy as np

def neighbour_indices(indexi, indexj):
    """Devuelve una lista de coordenadas de vecinos incluyendo el punto en sí."""
    return [[indexi, indexj], [indexi, indexj-1], [indexi, indexj+1], [indexi-1, indexj], [indexi+1, indexj]]

def select_valid_coord(list_of_coords, numero_filas, numero_columnas):
    """Devuelve las coordenadas válidas que están dentro de los límites de la matriz."""
    valid = []
    for coord in list_of_coords:
        if 0 <= coord[1] < numero_columnas and 0 <= coord[0] < numero_filas:
            valid.append(coord)
    return valid

def list_of_indices_2_list_of_values(list_of_indices, matriz):
    """Devuelve los valores de la matriz correspondientes a los índices válidos."""
    values = []
    for fila, columna in list_of_indices:
        values.append(matriz[fila][columna])
    return values

def average_list(elements):
    """Recibe una lista de valores y devuelve su promedio."""
    total = sum(elements)
    return round(total / len(elements), 2)

def average_matrix(matriz):
    """Convierte una matriz en otra donde cada elemento es el promedio de sí mismo y de sus vecinos."""
    numero_filas = len(matriz)
    numero_columnas = len(matriz[0])
    new_matriz = [[0 for _ in range(numero_columnas)] for _ in range(numero_filas)]
    for i in range(numero_filas):
        for j in range(numero_columnas):
            neighbours = neighbour_indices(i, j)
            neighbours = select_valid_coord(neighbours, numero_filas, numero_columnas)
            values = list_of_indices_2_list_of_values(neighbours, matriz)
            avg = average_list(values)
            new_matriz[i][j] = avg
    return new_matriz

def apply_average_filter_color(image_path, output_path,num_iterations=1):
    """Aplica un filtro de promedio a una imagen a color y guarda el resultado."""
    # Cargar imagen
    image = Image.open(image_path)
    matriz = np.array(image)
    # Aplicar el filtro el número de veces especificado
    for i in range(num_iterations):
        # Separar los canales de color
        r, g, b = matriz[:, :, 0], matriz[:, :, 1], matriz[:, :, 2]

        # Aplicar el filtro de promedio a cada canal
        r_avg = average_matrix(r)
        g_avg = average_matrix(g)
        b_avg = average_matrix(b)

        # Recomponer la imagen desde los canales promediados
        averaged_matriz = np.stack((r_avg, g_avg, b_avg), axis=-1)

    # Convertir la matriz resultante de nuevo a imagen
    averaged_image = Image.fromarray(np.uint8(averaged_matriz))

    # Guardar el resultado
    averaged_image.save(output_path)

    # Mostrar la imagen original y la imagen promediada
    image.show(title="Imagen Original")
    averaged_image.show(title="Imagen Promediada")

# Ejemplo de uso
apply_average_filter_color('imagen.png', 'imagen_salida.png',1)
```
