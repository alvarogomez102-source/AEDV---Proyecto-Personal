# Proyecto Personal AEDV — Empleo, Vivienda y Demografía en Canarias

## Tema del Proyecto
Análisis integrado de la dinámica socioeconómica y demográfica de Canarias mediante ocho indicadores clave del ISTAC (Instituto Canario de Estadística), abarcando el período 1999–2026.

## Indicadores Seleccionados (8 atributos)

| Indicador | Ámbito | Frecuencia | Unidad | Qué mide |
|-----------|--------|------------|--------|----------|
| `AFILIACIONES_ASALARIADOS` | Empleo | Mensual | Personas | Afiliados a la Seguridad Social como asalariados (97 municipios) |
| `CEMENTO_VENTAS` | Construcción | Mensual | Toneladas | Ventas de cemento en el mercado interior (8 islas) |
| `INVERSION_ESPANOLA_BRUTA` | Economía | Trimestral | Millones € | Formación bruta de capital fijo (21 CCAA) |
| `VIVIENDAS_INICIADAS` | Vivienda | Mensual | Número | Viviendas cuyo inicio de obra se certifica (63 áreas CCAA) |
| `POBLACION` | Demografía | Anual | Personas | Población residente por municipio (97 municipios) |
| `DEFUNCIONES_CANCER` | Salud | Anual | Número | Defunciones por neoplasias CIE-10 C00–D48 (8 islas) |
| `IPC` | Precios | Mensual | Índice 2016=100 | Índice de Precios de Consumo general (20 CCAA) |
| `HIDROCARBUROS_PRECIO_GASOLEO` | Energía | Semanal | €/litro | Precio medio de venta al público del gasóleo A (8 islas) |

## Cobertura Geográfica y Temporal
- **Geográfica**: 97 municipios + 8 islas + 21 CCAA (según indicador)
- **Temporal**: 1999 (defunciones cáncer) → 2026-08 (afiliaciones)
- **Total observaciones**: ~185,000 filas combinadas

## Preguntas de Investigación
1. **P1**: ¿Se ha recuperado el empleo en Canarias tras la crisis de 2008 al mismo ritmo que en el resto de comunidades autónomas?
2. **P2**: ¿Qué relación existe entre la evolución de la vivienda iniciada y la inversión bruta en Canarias vs. España?
3. **P3**: ¿Cómo ha evolucionado la dinámica empleo-población a nivel municipal en Canarias (2012–2025)?
4. **P4**: ¿Qué islas dependen más de un solo sector (construcción/turismo) y cómo afectó esa dependencia a su resiliencia económica?
5. **P5**: ¿Qué nivel de llegadas/empleo cabe esperar en los próximos dos años según modelos ARIMA?

## Metodología
- **CRISP-DM** (Cross Industry Standard Process for Data Mining) — 6 fases iterativas
- **Técnicas**: Series temporales (STL, ARIMA), PCA, correlación, transformación Yeo-Johnson, mapas coropléticos
- **Herramientas**: R (tidyverse, fpp3, highcharter, leaflet, shiny), ISTAC API (`istacr`)

## Entregables
1. **Memoria** (`ÁlvaroGinésGómezDelgadoMemoria.Rmd/.html`) — Documento completo siguiendo CRISP-DM
2. **Dashboard** (Shiny en servidor DIS) — Exploración interactiva con series temporales, ARIMA, mapas, PCA
3. **Seguimiento** (Google Sheet) — Registro de dedicación por fase CRISP-DM

## Estructura del Repositorio
```
AEDV - ProyectoPersonal/
├── ModeloMemoriaProyectoPersonalAEDV.Rmd    # Plantilla de memoria (esta se completa)
├── ModeloMemoriaProyectoPersonalAEDV.html   # Vista previa compilada
├── README_Proyecto_Personal.Rmd/.html       # Guía de trabajo
├── RubricaEvaluaciónProyectoPersonal.xlsx   # Criterios de evaluación (28 criterios)
├── estilos.css                              # Estilos visuales
├── ISTAC_Selected.rds                       # Datos combinados (8 indicadores)
├── ISTAC_Selected_metadatos.xlsx            # Metadatos de los indicadores
├── Memoria/                                 # Copia de trabajo
└── SelecciónDatasetsProyecto/               # Herramientas de selección/validación
    ├── ISTAC/ISTAC_DatasetSelection.Rmd     # Validación de los 8 indicadores
    ├── INE/, EUROSTAT/, WORLD_BANK/, etc.   # Otras fuentes exploradas
```

## Estado del Proyecto
- ✅ Datasets seleccionados y validados (8 indicadores ISTAC, 4+ válidos AEDV)
- ✅ Preguntas de investigación definidas (Entrega 1)
- 🔄 Comprensión del negocio y de los datos (en desarrollo)
- ⏳ Preparación, Modelado, Evaluación, Despliegue (pendientes)
- ⏳ Dashboard en servidor DIS (pendiente)

## Autor
**Álvaro Ginés Gómez Delgado** (Varocraft)  
ULPGC — AEDV 2026/2027  
Email: alvaro.gomez102@alu.ulpgc.es