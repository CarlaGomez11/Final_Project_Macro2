
# Proyecto Final – Modelos RBC y Neokeynesianos en Dynare

## 📘 Descripción General

Este repositorio contiene todos los materiales, archivos `.mod` de Dynare, scripts en MATLAB y resultados desarrollados para el proyecto final del curso *Macroeconomía II* (Otoño 2025). El trabajo se divide en dos partes principales:

- **Parte I**: Replicación y extensión de modelos Real Business Cycle (RBC), según Hansen y Wright (1992).
- **Parte II**: Evaluación comparada de reglas de política monetaria en un modelo neokeynesiano, siguiendo Galí (2015, Capítulo 4).

---

## 📁 Estructura del Repositorio

```
macroeconomics_final_project/
│
├── Material/                                # Archivos auxiliares
│
├── Parte_01/                                # Parte I: Modelos RBC
│   ├── modeloRBC_CasoBase/
│   ├── modeloRBC_Ext01_OcioNoSeparable/
│   ├── modeloRBC_Ext02_TrabajoIndivisible/
│   ├── modeloRBC_Ext03_GastoGubernamental/
│   └── modeloRBC_Ext04/
│
├── Parte_02/                                # Parte II: Modelos Neokeynesianos
│   ├── Regla01/                             # Regla de Taylor con expectativas
│   └── Regla02/                             # Regla de Taylor con variables corrientes
│
└── TrabajoFinal_DeLaRosa_Fernandez_Gomez.pdf  # Informe final en PDF
```

Cada subcarpeta contiene:
- El archivo `.mod` correspondiente para ser ejecutado en Dynare.
- Script `get_simul_replications.m` adaptado para simular 10.000 réplicas.
- Salidas gráficas (IRFs e histogramas).
- Archivos `.log` generados por Dynare.

---

## ⚙️ Instrucciones de Ejecución

1. **Requisitos**:
   - [MATLAB](https://www.mathworks.com/products/matlab.html)
   - [Dynare](https://www.dynare.org) versión 5 o superior
   - Dynare debe estar correctamente instalado y agregado al path de MATLAB.

2. **Cómo ejecutar los modelos**:
   - Ir a la carpeta correspondiente al modelo.
   - Ejecutar en MATLAB el archivo `.mod` con:
     ```matlab
     dynare nombre_del_modelo.mod
     ```
   - Luego, para simular 10.000 réplicas y obtener los histogramas:
     ```matlab
     get_simul_replications
     ```
   - Los resultados se guardan automáticamente como archivos `.png`.

3. **Script base común**:
   Todos los modelos utilizan el script `get_simul_replications.m`, adaptado de Johannes Pfeifer:
   > `get_simul_replications.m`  
   Fuente: https://github.com/JohannesPfeifer/DSGE_mod/blob/master/Hansen_1985/get_simul_replications.m

---

## 📊 Detalles por Parte

### Parte I – Modelos RBC (50 puntos)

Para cada modelo (caso base y cuatro extensiones), se incluyen:
- Formulación del sistema no lineal
- Solución del estado estacionario
- Funciones de impulso-respuesta (IRFs)
- Histogramas derivados de 10.000 simulaciones para estadísticas clave
- Comparaciones con la Tabla 3 del paper de Hansen & Wright (1992)

### Parte II – Modelo Neokeynesiano (50 puntos)

Para cada regla de política monetaria (expectativas vs. valores corrientes), se evalúa:
- Pérdida de bienestar \( L \) bajo tres escenarios:
  - Solo choques de productividad
  - Solo choques de demanda
  - Ambos choques simultáneamente
- Histogramas de \( L \) para 10.000 simulaciones
- Comparación final de desempeño de cada regla

---

## 📚 Referencias

- Hansen, G. D., & Wright, R. (1992). *The Labor Market in Real Business Cycle Theory*. Federal Reserve Bank of Minneapolis Quarterly Review, 16(2), 2.
- Galí, J. (2015). *Monetary Policy, Inflation, and the Business Cycle: An Introduction to the New Keynesian Framework and Its Applications*. Princeton University Press.
- Pfeifer, J. (GitHub Repository): [DSGE_mod](https://github.com/JohannesPfeifer/DSGE_mod)

---

## 👥 Autores

Este trabajo fue realizado por:

- **Catalina De La Rosa**  
- **Franco Fernández**  
- **Carla Gómez**  
- **Michelle Zárate**  

Proyecto final presentado en el curso *Macroeconomía II*  
Universidad Alberto Hurtado – Otoño 2025
