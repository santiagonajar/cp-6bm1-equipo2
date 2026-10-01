# Prácticas - Cómputo Paralelo

## Práctica 1
# Práctica 1 - Plataformas y Herramientas para Cómputo

## Compilación y ejecución

La práctica utiliza un `Makefile` para compilar los programas y un script para ejecutar automáticamente los benchmarks.

### Compilar

Desde el directorio `practicas/practica1/src`:

```bash
make
```

### Ejecutar

Desde el directorio `practicas/practica1/src`:

```bash
bash ../scripts/run_all.sh
```

El script ejecuta los benchmarks de C, Python puro y NumPy, y genera los archivos de resultados en el directorio `results/`.

## GPU

El experimento de GPU se realizó en Google Colab utilizando CuPy y una GPU NVIDIA Tesla T4.

El notebook se encuentra en:

`notebooks/p1_gpu.ipynb`

El notebook contiene:

* Identificación de la GPU mediante `nvidia-smi`.
* Comparación de CPU con NumPy y GPU con CuPy.
* Medición de GPU utilizando `synchronize()`.
* Medición de GPU sin `synchronize()`.
* Tabla de resultados CPU/GPU.

## Estructura del directorio

```text
practica1/
├── README.md
├── entorno.txt
├── src/
│   ├── matmul.c
│   ├── matmul_pure.py
│   ├── matmul_numpy.py
│   ├── hello_omp.c
│   └── Makefile
├── scripts/
│   ├── run_all.sh
│   └── plot.py
├── results/
├── notebooks/
│   └── p1_gpu.ipynb
└── reporte.pdf
```

## Resultados

Los archivos CSV y las gráficas generadas por los benchmarks se almacenan en `results/`.

Los archivos ejecutables generados durante la compilación no se incluyen en el repositorio.

## Requisitos

- GCC
- Python 3
- NumPy
- Pandas
- Matplotlib
- CuPy para el experimento de GPU
- Google Colab con GPU para ejecutar el notebook
- Linux o WSL2 con GCC (`gcc-fopenmp`)
- Python 3 con `numpy`, `matplotlib` y `pandas`

### Instrucciones de ejecución
```bash
cd practicas/practica1/src
make
bash ../scripts/run_all.sh
python3 ../scripts/plot.py
