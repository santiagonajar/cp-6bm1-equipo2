# Prácticas - Cómputo Paralelo

# Práctica 1 — Plataformas y Herramientas para Cómputo

## Compilar y ejecutar (2 comandos)

Desde `practicas/practica1/src`:

    make
    bash ../scripts/run_all.sh

`run_all.sh` ejecuta los benchmarks de C, Python puro y NumPy, guarda los CSV en `results/` y genera las gráficas con `plot.py`.

## Requisitos

- Linux o WSL2 (Ubuntu 24.04) con GCC con soporte OpenMP (`-fopenmp`). En macOS, Apple Clang no lo trae por defecto.
- Python 3 con las dependencias: `pip install numpy pandas matplotlib`

## Experimento de GPU (Google Colab)

1. Abrir `notebooks/p1_gpu.ipynb` en Google Colab.
2. Entorno de ejecución → Cambiar tipo → GPU (T4).
3. Ejecutar todas las celdas. CuPy ya viene instalado en Colab.

El notebook incluye: `nvidia-smi` con fecha y hora, comparación NumPy (CPU) vs CuPy (GPU), medición con y sin `synchronize()` y la tabla CPU/GPU.

## Estructura

    practica1/
    ├── README.md
    ├── entorno.txt
    ├── src/        (matmul.c, matmul_pure.py, matmul_numpy.py, hello_omp.c, Makefile)
    ├── scripts/    (run_all.sh, plot.py)
    ├── results/    (CSV y gráficas)
    ├── notebooks/  (p1_gpu.ipynb)
    └── reporte.pdf

Los ejecutables generados al compilar no se incluyen en el repositorio.
