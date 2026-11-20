# Data Analytics ML Challenge · 2026-2

**Predicción de entregas tardías en Olist** · Universidad Central
Profesor: Elias Buitrago Bolivar · Estudiante: ID 11 · Semilla: 1011

## Pregunta de negocio

¿Es posible anticipar qué pedidos llegarán después de la fecha prometida usando solo información conocida al confirmar el pago?

## Estructura del repositorio

```
data-analytics-ml-challenge/
├── data/          # datos locales (NO se publican los CSV)
├── notebooks/
│   ├── S12_ML_Challenge.ipynb   # Lab 1: modelos base y métricas
│   ├── S14_ML_Challenge.ipynb   # Lab 2: PCA, regularización y prueba KS
│   └── S15_ML_Challenge.ipynb   # Lab 4: red neuronal y escalabilidad
├── src/           # código modular (uso progresivo)
├── reports/       # métricas e informe ejecutivo
│   ├── S12_resultados_ID_11.json
│   ├── registro_experimentos_S14.csv
│   ├── resumen_S14.json
│   ├── registro_experimentos_S15.csv
│   ├── escalabilidad_S15.csv
│   ├── S15_resultados_ID_11.json
│   └── Informe_ejecutivo.pdf
└── README.md
```

> La semana 13 no tuvo clase; su contenido (PCA) se incorporó al laboratorio de la semana 14.

## Datos

Brazilian E-Commerce Public Dataset by Olist (CC BY-NC-SA 4.0), fijado al commit `fa0cc6d1aff713d3c8b9a1e633b56889881848bf`. Los notebooks descargan las siete tablas directamente desde GitHub; **los CSV originales y la muestra de pedidos no se suben al repositorio**.

- Muestra individual: 35.000 pedidos (semilla = 1000 + ID).
- Particiones: 24.500 entrenamiento · 5.250 validación · 5.250 prueba.
- La prueba no se usa para elegir modelos.

## Cómo reproducir

1. Abrir el notebook en Google Colab.
2. Confirmar `ID_ESTUDIANTE = 11`.
3. *Entorno de ejecución → Reiniciar y ejecutar todo*.
4. Verificar que las celdas de autoverificación (`assert`) terminen sin errores.
5. Descargar la carpeta `reports/` generada.

## Resumen de resultados

| Semana | Laboratorio | Hallazgo principal |
|:--|:--|:--|
| S12 | Modelos base | La regresión logística balanceada detecta el 67 % de los retrasos (Recall 0,670), con Precision 0,123 y costo de R$ 17.703. |
| S14 | PCA y regularización | 24 variables → 15 componentes (90,5 %). PCA empeoró el desempeño y `C` casi no lo modificó. KS: D = 0,0133, p = 0,4207. |
| S15 | Red neuronal | Completar con el resultado del notebook S15. |

El detalle, las limitaciones y la recomendación están en `reports/Informe_ejecutivo.pdf`.

## Flujo de commits sugerido

```
S12: modelo base y métricas
S14: PCA, regularización y prueba KS
S15: red neuronal y escalabilidad
S16: informe ejecutivo y cierre del proyecto
```

## Uso de IA

Se usaron asistentes de IA para depurar y generar código base. La interpretación de métricas y las conclusiones de negocio fueron redactadas y sustentadas por el estudiante.
