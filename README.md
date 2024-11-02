# Detector de Mutantes 🧬

## 🎯 Descripción

Magneto busca reclutar mutantes para enfrentarse a los X-Men y te ha encargado la creación de un sistema que permita detectar si un humano es mutante a partir de su secuencia de ADN. Este proyecto consiste en desarrollar un programa que detecte mutantes mediante un análisis de las secuencias genéticas.


## Funcionamiento del Programa 🚀

El programa recibe como entrada un array de Strings que representa cada fila de una matriz de (NxN) con la secuencia de ADN. Las letras que componen estos strings solo pueden ser: A, T, C, G, que corresponden a las bases nitrogenadas del ADN.

El ADN se considera mutante si se encuentran más de una secuencia de cuatro letras iguales consecutivas, en cualquiera de las siguientes direcciones:

Horizontal
Vertical
Diagonal (principal y secundaria)

## Ejecución del Algoritmo
Recepción del ADN: El usuario ingresa una matriz NxN que representa la secuencia de ADN.
Verificación: Se aplica una lógica para detectar si existen secuencias consecutivas de cuatro letras iguales. Esta verificación se realiza recorriendo:
Las filas de la matriz.
Las columnas de la matriz.
Las diagonales principales y secundarias.
Resultado: Si se encuentran más de una secuencia válida, el ADN se clasifica como mutante. De lo contrario, se clasifica como humano.

## 📝 Método Principal

```java
boolean isMutant(String[] dna)
```

## Endpoints 🔗

``http
POST /mutant
```

#### Request Body

```json
{
    "dna": [
        "ATGCGA",
        "CAGTGC",
        "TTATGT",
        "AGAAGG",
        "CCCCTA",
        "TCACTG"
    ]
}
```

###  Estadísticas

```http
GET /stats
```

#### Response

```json
{
    "count_mutant_dna": 40,
    "count_human_dna": 100,
    "ratio": 0.4
}
```

## 📊 Ejemplos de ADN

###  Matriz MUTANTE

```json
{
    "dna": [
        "ATGCGA",
        "CAGTGC",
        "TTATGT",
        "AGAAAG",
        "CCCCTA",
        "TCACTG"
    ]
}
```

###  Matriz NO MUTANTE

```json
{
    "dna": [
        "ATGGTG",
        "GTCTTA",
        "AATTGG",
        "ACTAGT",
        "GGATTC",
        "AGGCAA"
    ]
}
```

## URL de despliegue 🌐

El proyecto está desplegado en Render y puede accederse a través de:

```
https://detectormutante-1.onrender.com
```
## Diagramas de secuencia 📊
Aquí se encuentran los diagramas de secuencia que muestran el flujo de análisis del ADN y las interacciones entre los componentes.
<p align="center">
  <img src="https://github.com/user-attachments/assets/bb545cb6-e8f4-48fa-b985-5b7e19259fe5" alt="Imagen 1" width="500" style="margin-bottom: 20px;">
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/5a6a2446-e79c-462e-a73a-08ad6d8c9e34" alt="Imagen 2" width="500">
</p>


## Pruebas con Jmeter 🧪
Para asegurar la estabilidad y rendimiento del sistema, se realizaron pruebas con JMeter simulando diferentes cantidades de peticiones concurrentes.
### 1000 Peticiones
![image](https://github.com/user-attachments/assets/66e5b2ab-4bb6-4376-977a-1bb4d1528e08)

# Instalación

1. Clona el repositorio:
   ```bash
   git clone 
   cd DetectorMutante
   ```
   ## Para verificar que las dependencias se instalaron correctamente
   ```
   ./gradlew build
   ```
   # Ejecución En Local
Ejecuta H2
Levanta la aplicación  (localhost:8080)
```
./gradlew bootRun
```
# Pruebas
Ejecutar tests:
```
./gradlew test
```

