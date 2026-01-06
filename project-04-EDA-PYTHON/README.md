# Análisis de Campañas Bancarias Portuguesas

## Descripción del Proyecto

Este proyecto analiza 43,000 registros de campañas telefónicas bancarias portuguesas realizadas entre 2015-2019 para identificar patrones que optimicen las tasas de conversión. El objetivo principal es desarrollar una estrategia de segmentación de clientes que maximice el retorno de inversión en actividades comerciales.

## Estructura del Proyecto

```
proyecto-analisis-bancario/
├── data/
│   ├── raw/                    # Datos originales
│   ├── processed/              # Datos después de limpieza
│   └── analysis/              # Datos con análisis descriptivo
├── notebooks/
│   ├── 01_transformacion_limpieza.ipynb
│   ├── 02_analisis_descriptivo.ipynb
│   └── 03_visualizacion.ipynb
├── reports/
│   └── informe_analisis.md
└── README.md
```

## Requisitos del Sistema

### Dependencias de Python
```python
pandas>=1.5.0
numpy>=1.21.0
matplotlib>=3.5.0
seaborn>=0.11.0
openpyxl>=3.0.9  # Para leer archivos Excel
```

### Instalación
```bash
pip install pandas numpy matplotlib seaborn openpyxl
```

## Datasets Utilizados

1. **banco.csv**: Datos principales de campañas (43,000 registros)
2. **cliente.xlsx**: Información adicional de clientes (20,115 registros)

### Variables Principales
- **age**: Edad del cliente
- **job**: Tipo de trabajo
- **education**: Nivel educativo
- **duration**: Duración de la llamada (segundos)
- **poutcome**: Resultado de campaña anterior
- **y**: Variable objetivo (acepta/rechaza producto)

## Guía de Ejecución

### Paso 1: Transformación y Limpieza de Datos

```python
# Ejecutar notebook: 01_transformacion_limpieza.ipynb

# Problemas resueltos:
# - Formato numérico europeo (93,994 → 93.994)
# - Fechas en español (2-agosto-2019 → 2-August-2019)
# - Valores faltantes (imputación estratificada)
# - Tipos de datos incorrectos

# Archivos generados:
# - banco_analizado.csv
# - cliente_analizado.csv
# - datos_combinados.csv
```

### Paso 2: Análisis Descriptivo

```python
# Ejecutar notebook: 02_analisis_descriptivo.ipynb

# Análisis realizados:
# - Estadísticas descriptivas por variable
# - Análisis de correlaciones
# - Creación de variables derivadas
# - Identificación de patrones demográficos

# Variables creadas:
# - edad_grupo: Categorización por rangos de edad
# - duracion_categoria: Clasificación de duración de llamadas
# - exito: Variable binaria (1=éxito, 0=fracaso)
```

### Paso 3: Visualización y Segmentación

```python
# Ejecutar notebook: 03_visualizacion.ipynb

# Crear copias de trabajo:
banco_visual = banco_analizado.copy()
cliente_visual = cliente_analizado.copy()
datos_combinados_visual = datos_combinados.copy()

# Visualizaciones generadas:
# - Distribución de variable objetivo
# - Análisis por edad y trabajo
# - Duración de llamadas vs éxito
# - Patrones temporales
# - Segmentación prioritaria
```

## Principales Hallazgos

### 1. Factor Más Predictivo: Historial Previo
- **Clientes con éxito anterior**: 1,436 personas (3.3% del total)
- **Tasa de conversión**: ~70% vs 11.3% general
- **Impacto**: 6.2x superior al promedio

### 2. Segmentación Demográfica
- **Personas mayores (55+)**: Tasas significativamente superiores
- **Estudiantes**: Mayor receptividad que otros perfiles laborales
- **Patrón de edad**: Correlación positiva entre edad y tasa de conversión

### 3. Factores Operacionales
- **Duración de llamadas**: Correlación directa con éxito
- **Situación financiera**: Clientes sin préstamos activos más receptivos
- **Número de contactos**: Promedio 2.6 contactos por cliente

### 4. Estrategia de Segmentación Recomendada

#### Segmento 1 - Prioridad Máxima
- **Target**: Clientes con éxito anterior (poutcome='SUCCESS')
- **Volumen**: 1,436 personas
- **Tasa esperada**: 70%

#### Segmento 2 - Prioridad Alta  
- **Target**: Mayores de 55 años sin historial previo
- **Perfil**: Estabilidad financiera
- **Tasa esperada**: 15-25%

#### Segmento 3 - Prioridad Media
- **Target**: Estudiantes sin historial previo
- **Características**: Apertura a productos nuevos
- **Tasa esperada**: 12-18%

## Resultados Clave

### Métricas de Rendimiento
- **Tasa de conversión general**: 11.3%
- **Tasa del segmento prioritario**: 70%
- **Mejora potencial**: 6.2x en eficiencia

### Impacto Estimado
- **Reducción de contactos**: 88% manteniendo conversiones
- **Mejora de ROI**: 300-400%
- **Optimización de recursos**: Enfoque en 12% de clientes más prometedores

## Archivos de Salida

### Datos Procesados
- `banco_analizado.csv`: Dataset principal limpio con variables derivadas
- `cliente_analizado.csv`: Información de clientes procesada
- `datos_combinados.csv`: Dataset unificado para análisis avanzado

## Limitaciones del Análisis

1. **Dataset desbalanceado**: 89% de rechazos limita robustez estadística
2. **Concentración temporal**: Datos de cliente limitados a 2012
3. **Información limitada**: Ausencia de detalles sobre productos específicos
4. **Validación requerida**: Patrones identificados requieren pruebas A/B

## Próximos Pasos

### Implementación
1. **Sistema de scoring**: Automatizar segmentación de clientes
2. **Pruebas A/B**: Validar estrategia segmentada vs. enfoque masivo
3. **Actualización de datos**: Recopilar información demográfica reciente

### Mejoras Técnicas
1. **Machine Learning**: Desarrollar modelo predictivo automatizado
2. **Dashboard interactivo**: Crear panel de control para monitoreo
3. **API de segmentación**: Integrar con sistemas CRM existentes



