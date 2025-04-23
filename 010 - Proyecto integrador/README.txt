# Análisis de Imagen de Juguetes con OpenCV y Python

**Fecha:** 15 de abril de 2025  
**Autor:** Sebastian Flehr
**Tecnologías utilizadas:** Python, OpenCV, NumPy, Matplotlib  
**Entorno:** Google Colab  

## 📌 Descripción

Este proyecto tiene como objetivo aplicar técnicas básicas de procesamiento digital de imágenes utilizando OpenCV sobre una imagen de juguetes. Se abordan tres grandes ejes:

1. Espacios de Color
2. Muestreo y Cuantización
3. Segmentación por Color

Cada sección aplica transformaciones y análisis específicos para entender mejor cómo funcionan los fundamentos del procesamiento de imágenes.

---

## 🔧 Requisitos

- Python 3.x
- OpenCV
- NumPy
- Matplotlib

En Google Colab no es necesario instalar dependencias adicionales, ya vienen preinstaladas.

---

## 1. 🎨 Espacios de Color

- Se cargó la imagen con OpenCV (`cv2.imread`).
- Se separaron y visualizaron los canales B, G y R por separado.
- Se analizó qué canal tiene más información mediante los valores promedio de cada canal.
- Se convirtió la imagen de BGR a RGB para visualizar correctamente los colores reales.

🔍 **Aprendizaje clave:**  
OpenCV carga imágenes en formato BGR, por lo que al visualizarlas sin convertir a RGB, los colores pueden verse incorrectos.

---

## 2. 📉 Muestreo y Cuantización

### Muestreo Espacial

- Se aplicó reducción espacial (resizing) con factores de 2x, 4x y 8x.
- Se calculó:
  - El nuevo tamaño de la imagen.
  - El porcentaje de reducción de datos respecto a la imagen original.

### Cuantización

- Se aplicó cuantización a 32, 64, 128 y 256 niveles de intensidad.
- Se observó visualmente en qué nivel comienza a degradarse la calidad de imagen.

🔍 **Aprendizaje clave:**  
Una reducción espacial o de niveles de cuantización implica pérdida de información. El desafío está en encontrar un balance entre compresión y calidad visual.

---

## 3. 🎯 Segmentación por Color

- Se segmentaron los objetos de color rojo mediante umbrales RGB.
- Se transformó la imagen segmentada a escala de grises.
- Se calculó el histograma de intensidad de los píxeles segmentados.
  - Se hizo en escala normal y en escala logarítmica para mejor visualización.
- Se encontraron los contornos de los objetos rojos.
- Se dibujaron:
  - Todos los contornos en rojo.
  - El rectángulo envolvente más grande sobre el objeto principal segmentado.

🔍 **Aprendizaje clave:**  
La segmentación permite extraer regiones de interés de una imagen, y su análisis (como histograma y contornos) facilita tareas de clasificación, conteo o seguimiento de objetos.

---

## 🖼️ Imagen utilizada

Se utilizó una imagen de juguetes coloridos sobre fondo blanco, ideal para segmentar objetos según el color.

---

## 🚀 Cómo ejecutar

1. Abrí el archivo `.ipynb` en Google Colab.
2. Subí la imagen `toys.jpg`.
3. Ejecutá las celdas paso a paso para observar cada transformación y resultado.

---

## 📷 Resultados esperados

- Visualización de canales de color.
- Imágenes muestreadas y cuantizadas.
- Histogramas de intensidad.
- Segmentación y detección de contornos.

---

## 📚 Referencias

- Documentación de [OpenCV](https://docs.opencv.org/)
- Tutoriales de [Matplotlib](https://matplotlib.org/stable/users/index.html)
- Conceptos de muestreo y cuantización del procesamiento digital de imágenes.