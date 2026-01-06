# 📊 Análisis Comparativo: Criptomonedas vs Acciones Tecnológicas
## Estrategia de Inversión Basada en Ciclos Temporales (2012-2024)

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-green.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![Status](https://img.shields.io/badge/Status-En_Evaluación-yellow.svg)

---

## 🎯 Descripción del Proyecto

Este proyecto analiza la relación histórica entre **criptomonedas** y **acciones tecnológicas** durante el período 2012-2024, combinando análisis estadístico riguroso con proyecciones basadas en ciclos temporales para identificar oportunidades de inversión estratégicas.

**Dataset:** 50,109 registros de 17 activos (7 criptomonedas + 10 acciones tecnológicas)  
**Período:** 2012-2024 (13 años de datos históricos)  
**Fuentes:** Kaggle + yfinance (integración de dos fuentes complementarias)

### 🔍 Objetivo Principal

Desarrollar una estrategia de inversión cuantitativa basada en dos ciclos bien documentados:
- 📉 **Ciclo de Bitcoin (Halving):** Patrón técnico/económico de 4 años
- 🏛️ **Ciclo Presidencial USA:** Patrón político/fiscal de 4 años

**Hallazgo crítico:** La colisión de ambos ciclos en **2025-2026** representa la mayor oportunidad y riesgo de la década.

---

## ✨ Características Principales

- ✅ **Dataset robusto:** 50,109 registros procesados y limpios (0% NaNs)
- ✅ **Análisis estadístico avanzado:** Correlaciones, volatilidad, VaR, drawdowns, tests de normalidad
- ✅ **Backtesting de carteras:** 7 estrategias evaluadas (cartera 30/70 óptima con Sharpe Ratio 1.20)
- ✅ **Índices sintéticos creados:** CRYPTO 7 Index y NASDAQ 10 Index (equally-weighted)
- ✅ **Análisis de ciclos temporales:** Proyecciones 2024-2027 basadas en patrones históricos
- ✅ **Gestión de riesgo:** Escenarios probabilísticos y planes de contingencia
- ✅ **Informe completo:** Documento de 70-80 páginas con metodología y recomendaciones

---

## 📁 Estructura del Proyecto
proyecto/
│
├── data/
│   ├── raw/                      # Datos originales (Kaggle)
│   │   ├── crypto/               # Archivos CSV de criptomonedas
│   │   └── stocks/               # Archivos CSV de acciones
│   └── processed/                # Datos procesados y limpios
│       └── crypto_stocks_clean_raw.csv  (50,109 registros)
│
├── notebooks/
│   ├── limpieza_datos.ipynb                 # 01. Limpieza y transformación
│   ├── eda_completo_con_indices.ipynb       # 02. Análisis exploratorio
│   ├── analisis_estadistico_avanzado.ipynb  # 03. Análisis estadístico
│   └── visualizaciones.ipynb                # 04. Gráficos
│   
├── reports/
│   └── informe_final.pdf         # Informe completo (70-80 páginas)
│
├── README.md                     # Este archivo
└── requirements.txt              # Dependencias Python

---

## 🛠️ Tecnologías Utilizadas

### Lenguajes y Herramientas
- **Python 3.9+** - Lenguaje principal
- **Jupyter Notebook** - Análisis interactivo
- **Visual Studio Code** - IDE

### Librerías Python

#### Manipulación de Datos
pandas==2.0.3           # Análisis y manipulación de datos
numpy==1.24.3           # Operaciones numéricas

#### Obtención de Datos
yfinance==0.2.28        # Descarga de datos financieros

#### Visualización
matplotlib==3.7.2       # Gráficos base
seaborn==0.12.2         # Visualizaciones estadísticas
plotly==5.15.0          # Gráficos interactivos

#### Análisis Estadístico
scipy==1.11.1           # Tests estadísticos
statsmodels==0.14.0     # Modelos estadísticos avanzados

---

## 🚀 Instalación y Configuración

### 1. Requisitos Previos
- Python 3.9 o superior
- pip (gestor de paquetes)
- Jupyter Notebook

### 2. Crear Entorno Virtual (Recomendado)
Windows
python -m venv venv
venv\Scripts\activate
macOS/Linux
python3 -m venv venv
source venv/bin/activate

### 3. Instalar Dependencias
pip install -r requirements.txt

### 4. Verificar Instalación
python -c "import pandas, numpy, yfinance; print('✅ Todo instalado correctamente')"

---

## 📊 Uso del Proyecto

### Opción 1: Ejecutar Notebooks en Orden

1. **Limpieza de Datos:**
jupyter notebook notebooks/limpieza_datos.ipynb
   - Integra Kaggle + yfinance
   - Limpia NaNs y duplicados
   - Genera dataset final

2. **Análisis Exploratorio (EDA):**
jupyter notebook notebooks/eda_completo_con_indices.ipynb
   - Crea índices sintéticos
   - Analiza performance histórica
   - Visualiza correlaciones

3. **Análisis Estadístico Avanzado:**
jupyter notebook notebooks/analisis_estadistico_avanzado.ipynb
   - Backtesting de carteras
   - Análisis de ciclos
   - Proyecciones 2024-2027

### Opción 2: Usar Datos Procesados Directamente
import pandas as pd
Cargar dataset limpio
df = pd.read_csv('data/processed/crypto_stocks_clean_raw.csv')
Ejemplo: Filtrar solo Bitcoin
bitcoin = df[df['asset_name'] == 'BITCOIN']
print(bitcoin.head())

---

## 📈 Resultados Principales

### 1. Performance Histórica (2020-2024)

| Índice | Retorno Total | Retorno Anual | Volatilidad | Sharpe Ratio | Max Drawdown |
|--------|---------------|---------------|-------------|--------------|--------------|
| **CRYPTO 7** | +4,141% | 93.8% | 68.0% | 1.18 | -81.4% |
| **NASDAQ 10** | +144% | 22.3% | 25.1% | 0.61 | -40.3% |

**Conclusión:** Crypto superó **28.7x** a NASDAQ, pero con **2.7x más volatilidad**.

### 2. Cartera Óptima Identificada: 30/70 NASDAQ/Crypto
Inversión inicial:  $10,000
Valor final:        $235,321
Retorno total:      +2,253%
Sharpe Ratio:       1.20 🏆 (MÁXIMO)
Max Drawdown:       -69.9%

**¿Por qué 30/70?**
- Único Sharpe Ratio 1.20 (máximo absoluto)
- Captura 55% retorno de 100% Crypto
- Con solo 86% del drawdown

### 3. Correlación NASDAQ-Crypto

| Régimen | Correlación | Diversificación |
|---------|-------------|-----------------|
| Normalidad | 0.32 | ✅ Funciona |
| Estrés | 0.55-0.70 | ⚠️ Parcial |
| Crisis | 0.80-0.95 | ❌ FALLA |

**Hallazgo crítico:** La diversificación **FALLA cuando más se necesita** (crisis).

### 4. Bitcoin como Líder de Mercado

- ✅ **Bitcoin adelanta NASDAQ ~26 días** (ventana de oportunidad)
- ✅ **100% sincronía direccional** (todos suben/bajan juntos)
- ✅ Útil como "early warning" para reposicionarse

### 5. Proyección Ciclos 2024-2027
📅 TIMELINE ESTRATÉGICO:
2024 Q4:     🟢 MANTENER 30/70 (disfrutar bull market)
2025 Q1-Q2:  🟡 VIGILAR (Bitcoin rumbo a ATH)
2025 Q3-Q4:  🔴 VENDER 60-80% crypto (ATH $120K-$180K)
2026 TODO:   🔴 DEFENSIVA (-60% drawdown esperado)
2027 Q2-Q4:  🟢 COMPRAR agresivo (fondo $35K-$50K)
2028+:       🔄 REPETIR ciclo (Halving #5)

**Proyección 2026 (La Tormenta Perfecta):**
- Bitcoin: -78% (de $180K a $40K)
- NASDAQ: -19% (Año Mid-term)
- Correlación: 0.70+ (ambos caen juntos)

---

## 🔬 Metodología

### 1. Limpieza y Procesamiento de Datos
- Integración de dos fuentes (Kaggle + yfinance)
- Forward-fill para stocks en fines de semana
- Validación de precios y volúmenes
- Eliminación de duplicados y outliers

### 2. Creación de Índices Sintéticos
- **NASDAQ 10 Index:** Equally-weighted (10% cada stock)
- **CRYPTO 7 Index:** Equally-weighted (14.3% cada crypto)
- Base 100: 20 Agosto 2020 (fecha común disponible)

### 3. Análisis Estadístico
- Correlaciones estáticas y dinámicas
- Volatilidad anualizada
- VaR (Value at Risk) al 95%
- Drawdowns máximos
- Tests de normalidad (Shapiro-Wilk)
- Análisis de eventos extremos

### 4. Backtesting de Carteras
- 7 estrategias evaluadas (100% NASDAQ → 100% Crypto)
- Rebalanceo: Ninguno (buy & hold)
- Métricas: Retorno, Sharpe, Max DD
- Período: 2020-2024 (4.36 años)

### 5. Análisis de Ciclos
- **Ciclo Bitcoin:** Patrón Halving (3 ciclos históricos)
- **Ciclo Presidencial:** Patrón USA (17 ciclos históricos)
- Proyección colisión 2025-2026
- Escenarios probabilísticos

---

## 📊 Visualizaciones Incluidas

El proyecto incluye múltiples visualizaciones:

- 📈 **Evolución temporal** de índices CRYPTO 7 y NASDAQ 10
- 🔗 **Correlaciones dinámicas** por períodos
- 📉 **Drawdowns históricos** (COVID, Crypto Winter)
- 🎯 **Backtesting de carteras** (retorno vs riesgo)
- 🔄 **Ciclos temporales** (Halving + Presidencial)
- 🗺️ **Mapa de calor** de riesgo trimestral 2024-2027
- 📊 **Distribuciones de retornos** (normalidad)

---

## ⚠️ Limitaciones y Advertencias

### Limitaciones del Análisis

1. **Sample size limitado:**
   - Solo 3 ciclos completos de Bitcoin
   - Primera colisión en mercado crypto maduro

2. **Los ciclos NO son garantías:**
   - Probabilidad histórica: 70-80%
   - 20-30% veces fallan parcialmente
   - 5-10% black swans rompen todo

3. **Magnitud impredecible:**
   - Timing puede ser correcto, magnitud varía
   - Usar rangos, no números exactos

4. **Eventos imprevistos:**
   - Guerra, crisis bancaria, regulación extrema
   - Pandemia, default soberano
   - Pueden romper cualquier patrón

### ⚠️ Disclaimer

> **Este proyecto es EDUCATIVO y de investigación. NO constituye asesoría financiera, fiscal o legal.**
>
> Las inversiones en criptomonedas y acciones conllevan riesgo de pérdida total del capital. El autor NO se responsabiliza por pérdidas derivadas del uso de esta información.
>
> **Invierte solo capital prescindible. Consulta siempre con profesionales certificados antes de tomar decisiones de inversión.**
>
> **Past performance ≠ Future results**

---

## 📚 Recursos y Referencias

### Fuentes de Datos
- [Kaggle - Cryptocurrency Historical Prices](https://www.kaggle.com/)
- [Yahoo Finance (yfinance)](https://finance.yahoo.com/)
- [CoinGecko](https://www.coingecko.com/)

### Documentación Técnica
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [yfinance Documentation](https://pypi.org/project/yfinance/)
- [Matplotlib Documentation](https://matplotlib.org/)

### Referencias Académicas
- Stock Trader's Almanac - Ciclo Presidencial
- Bitcoin Whitepaper - Satoshi Nakamoto
- Stock-to-Flow Model - PlanB

---

## 📄 Estado del Proyecto y Derechos

**Status:** 🔒 Versión de Evaluación Académica  
**Fecha de entrega:** Octubre 2025  
**Tipo:** Proyecto de Análisis de Datos  


### Futura Hoja de Ruta (Post-Evaluación)

Ideas de mejora planificadas después de hacer el proyecto público:

- [ ] Añadir más criptomonedas (Top 20)
- [ ] Implementar machine learning para predicciones
- [ ] Dashboard interactivo en Streamlit/Dash
- [ ] Backtesting con rebalanceo mensual
- [ ] Análisis de altcoins específicos
- [ ] Integración con APIs en tiempo real
- [ ] Estrategias con opciones/hedging

---

## 📧 Contacto

**Autor:** [Sergio Cano]  
**email:** s.cano1973@gmail.com 
**Proyecto Académico:** Análisis de Datos  
**Institución:** [The Power]  
**Fecha:** Octubre 2025


---

## 🙏 Agradecimientos

- A la comunidad de **Kaggle** por los datasets históricos
- A **Yahoo Finance** por la API gratuita (yfinance)
- A todos los que contribuyen al ecosistema open-source de Python
- A los investigadores de ciclos financieros que documentaron estos patrones
- A los profesores y evaluadores por su tiempo y feedback

---

## 📊 Estadísticas del Proyecto
📁 Archivos:          15+
📊 Líneas de código:  5,000+
📝 Registros:         50,109
📅 Período análisis:  13 años (2012-2024)
🎯 Activos:           17 (7 crypto + 10 stocks)
📄 Informe:           70-80 páginas
⏱️ Tiempo desarrollo: 200+ horas

---

## 🎯 Próximos Pasos

### Durante Evaluación:
1. ✅ Esperar feedback de evaluadores
2. 🔄 Implementar correcciones sugeridas
3. ✅ Completar documentación adicional si requerido
4. ⏳ Obtener evaluación final

### Post-Evaluación:
1. 📄 Añadir LICENSE (MIT) al proyecto
2. 📝 Actualizar README (versión pública)
3. 🌐 Publicar en GitHub como proyecto open-source
4. 📢 Compartir con la comunidad (LinkedIn, Twitter, Reddit)
5. 🤝 Habilitar contribuciones de la comunidad
6. 📈 Continuar desarrollo con mejoras planificadas

---

**Última actualización:** Octubre 2025  
**Versión:** 1.0.0 (Evaluación)  
**Status:** 🔒 En Evaluación Académica

---

> *"Los ciclos no garantizan ganancias, pero ofrecen el mejor framework probabilístico para navegar mercados volátiles."*

---

**📚 Este proyecto representa la culminación de meses de investigación, análisis de datos y desarrollo de estrategias cuantitativas. Agradezco tu interés y espero que los hallazgos contribuyan al conocimiento en el área de análisis financiero y estrategias de inversión.**

