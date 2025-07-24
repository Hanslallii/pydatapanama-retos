# 🏆 Pokemon

📌 **Descripción:**
Analizando Pokemones con Python

📊 **Objetivo:**
Este notebook tiene como propósito presentar un reto de programación para la comunidad de PyData Panamá, usando el dataset de Pokemones provisto. El reto tiene preguntas clasificadas en tres niveles de dificultad: **Low**, **Medium** y **High**, y abarca el uso de las librerías `pandas`, `numpy`, `matplotlib` y `seaborn`.


👤 **Autor del reto:**
@jasonssdev

---

## Preguntas

## 🔹 Nivel Low (Básico)

### Pregunta 1: ¿Cuántos pokemones hay en total?
```python
#1184
```

### Pregunta 2: ¿Cuáles son los 5 tipos más comunes (columna `Primary Typing`)?
```python
#Los 5 tipos más comunes (Primary Typing) son:

Water – 145 Pokémon

Normal – 128

Grass – 113

Bug – 89

Fire – 77
```

### Pregunta 3: ¿Cuál es el promedio de Velocidad `(Speed)` de todos los pokemones?
```python
#Promedio de velocidad: 69.73
```

---

## 🔸 Nivel Medium (Intermedio)

### Pregunta 4: ¿Cuál es la correlación entre las estadísticas `Attack`, `Defense` y `Speed`? Muestra un heatmap.
```python
#Hay una correlación moderada positiva entre Attack y Speed (≈ 0.45)

Hay una correlación baja entre Defense y Speed (≈ 0.12)

Attack y Defense tienen una correlación baja-moderada positiva (≈ 0.35)
```

### Pregunta 5: ¿Qué tipo (`Primary Typing`) tiene el mayor promedio de `Attack`?
```python
#El tipo primario con el promedio de ataque más alto es dragon, con un promedio de 105.98 puntos.


```

### Pregunta 6: Crear un histograma de la variable `Speed`
```python
#El tipo primario con la defensa promedio más alta es steel, con un promedio de 115.63 puntos.


```

---

## 🔺 Nivel High (Avanzado)

### Pregunta 7: ¿Qué pokemones tienen estadísticas totales (`Base Stat Total`) superiores al percentil 90? ¿Qué tipos predominan en este grupo?
```python
#Los Pokémon que tienen un total de estadísticas por encima de 590 (el 90% más alto) son los más fuertes.
En ese grupo, los tipos que más se repiten son: Dragon, Psychic, Water, Steel y Normal.
Así que básicamente los dragones y psíquicos dominan en esos Pokémon súper poderosos.


```

### Pregunta 8: Clasifica a los pokemones en tres categorías según su `Base Stat Total`: "Débil", "Normal" y "Fuerte". Luego, muestra la distribución de estas categorías en un gráfico de barras.
```python
#Se clasificaron los Pokémon en tres grupos según su poder total: "Débil", "Normal" y "Fuerte". Al hacer esto, se vio que hay 410 Pokémon fuertes, 390 débiles y 384 normales. La mayoría cae en la categoría de Fuerte. Esto se puede ver también en la gráfica de barras que muestra cómo se distribuyen estas tres categorías.


```

### Pregunta 9: Crear un pairplot de `Attack`, `Defense`, `Speed` y colorear por `Legendary Status`
```python
#En el gráfico se puede ver que los pokémon legendarios casi siempre tienen estadísticas más altas en ataque, defensa y velocidad en comparación con los que no lo son. También se nota que los legendarios están más agrupados en las esquinas superiores del gráfico, o sea que destacan bastante en las tres estadísticas. Mientras que los no legendarios están más repartidos y muchos tienen stats bajos.


```

---

## 📂 **Estructura del reto**
Este reto sigue la estructura estándar:
```plaintext
📂 reto-pokemon-jasonssdev/
 ├── README.md        # Explicación del reto
 ├── 📂 data/         # Datos del reto 
 ├── 📂 src/          # Código base del reto 
 ├── 📂 tests/        # Pruebas unitarias 
 ├── 📂 submissions/  # Soluciones de los participantes
```
📢 **Importante:**
- **Las soluciones deben subirse en `submissions/` en formato `.ipynb`.**

---

## 📌 **Datos del reto** (Si aplica)
📂 **Dataset:** `all_pokemon_data.csv`
🔹 **Descripción:** Listado de Pokemones
🔹 **Fuente:** [pokemon](https://www.kaggle.com/datasets/sarahtaha/1025-pokemon)
🔹 **Diccionario de datos:**

| Columna | Descripción |
|---------|-------------|
| `Name` | Nombre del Pokémon. Si tiene una forma alterna, se añade con un guion. Todo el texto está en minúsculas. |
| `National Dex` | ID del Pokémon según la Pokédex nacional. Las formas alternas comparten el mismo ID que su forma original (por ejemplo, Charizard, Mega Charizard-X y Mega Charizard-Y tienen todos el ID 6). |
| `Primary Typing` | Tipo primario del Pokémon. |
| `Secondary Typing` | Tipo secundario del Pokémon. Se deja en blanco si solo tiene un tipo. |
| `Secondary Typing Flag` | Verdadero si el Pokémon tiene un tipo secundario, Falso si tiene solo un tipo. |
| `Generation` | Generación a la que pertenece el Pokémon, indicada en números romanos (i=1, ii=2, iii=3, iv=4, v=5, vi=6, vii=7, viii=8, ix=9). |
| `Legendary Status` | Verdadero si es legendario, mítico, mega, ultraente o paradoja. Falso si no lo es. |
| `Form` | Si el Pokémon tiene una forma alterna con cambio de estadísticas, se listará aquí (también se usa para modificar el nombre). Ejemplos: zygarde-50, zygarde-10-power-construct, etc. |
| `Alt Form Flag` | Verdadero si no es la forma base. |
| `Evolution Stage` | Etapa actual de evolución: uno, dos o tres. (ej: charmander = 1, charmeleon = 2, charizard = 3) |
| `Number of Evolutions` | Número total de evoluciones en la línea evolutiva (formas alternas no incluidas). Las opciones son uno, dos o tres. |
| `Color ID` | Identificador de color según el sistema de Niantic. Su lógica no es completamente conocida. |
| `Catch Rate` | Modificador de especie del Pokémon para la ecuación de tasa de captura. Cuanto más alto, más fácil de capturar. |
| `Height (dm)` | Altura del Pokémon en decímetros. Proviene de PokeAPI. |
| `Weight (hg)` | Peso del Pokémon en hectogramos. Proviene de PokeAPI. |
| `Height (in)` | Altura del Pokémon en pulgadas. Convertido desde decímetros multiplicando por 3.93701. |
| `Weight (lb)` | Peso del Pokémon en libras. Convertido desde hectogramos multiplicando por 0.220462. |
| `Base Stat Total` | Suma de las estadísticas base del Pokémon (Salud, Ataque, Defensa, Ataque Especial, Defensa Especial, Velocidad). |
| `Health` | Salud total con la que una especie puede comenzar. Puede modificarse con EVs. |
| `Attack` | Ataque total con el que una especie puede comenzar. Puede modificarse con EVs. |
| `Defense` | Defensa total con la que una especie puede comenzar. Puede modificarse con EVs. |
| `Special Attack` | Ataque especial total con el que una especie puede comenzar. Puede modificarse con EVs. |
| `Special Defense` | Defensa especial total con la que una especie puede comenzar. Puede modificarse con EVs. |
| `Speed` | Velocidad total con la que una especie puede comenzar. Puede modificarse con EVs. |

---

## 🚀 **Cómo participar**
1️⃣ **Clona el repositorio**
```bash
git clone git@github.com:pydatapanama/pydatapanama-retos.git
cd pydatapanama-retos
```

2️⃣ **Crea un nuevo branch con tu usuario**
```bash
git checkout -b reto-pokemon-{tu_usuario}
```

3️⃣ **Dirígete a la carpeta del reto y crea tu solución**
```bash
cd retos/reto-pokemon-jasonssdev/submissions
```
```bash
touch solucion-{tu_usuario}.ipynb
```

4️⃣ **Desarrolla tu solución y súbela a GitHub**
```bash
git add .
git commit -m "Agregando solución al reto Pokemon"
git push origin reto-pokemon-{tu_usuario}
```

5️⃣ **Crea un Pull Request en GitHub**
Para que tu solución sea revisada e integrada al repositorio.

---

## 🔹 **Criterios de evaluación**
Para evaluar las soluciones, se considerarán los siguientes aspectos:
✅ **Claridad y organización del código**
✅ **Uso adecuado de librerías de Python**
✅ **Calidad de la visualización (si aplica)**
✅ **Correctitud de los cálculos y análisis**

---

## 📚 **Recursos recomendados**
📌 [Documentación de Pandas](https://pandas.pydata.org/docs/)  
📌 [Documentación de Matplotlib](https://matplotlib.org/stable/contents.html)  
📌 [Documentación de Seaborn](https://seaborn.pydata.org/)  

---

🚀 **¡Esperamos tu participación!** Si tienes dudas, pregunta en nuestra comunidad o abre un Issue en GitHub. 😃
