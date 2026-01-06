# 📊 Evolución del Paro en España

Estudio sobre los **factores que influyen en el paro en España**, más allá del ciclo económico.  
🔎 **Objetivo:** Detectar patrones en la evolución del paro en los últimos años.

---

## 📑 Estructura del Proyecto

1. **Acceso a datos oficiales:**  
👉 [INE - Instituto Nacional de Estadística](https://www.ine.es)

**Archivos descargados:**
- `DatosocupadosEspaña.csv`
- `paradosporestadocivilsexoygrupodeedad.csv`
- `paradosporgrupodeedadsexoysectoreconómico.csv`
- `paradosporniveldeformacionalcanzadosexoygrupodeedad.csv`

2. **Transformación y limpieza de datos**
   - Datos unificados en la pestaña **paradosporestadocivilsexoygrupodeedad**.
   - Eliminación de duplicados y celdas vacías completadas.
   - Introducción de nuevas fechas
   
3. **Análisis descriptivo**
    -Descripción General del Conjunto de Datos trimestrales desde 2014T1 hasta 2025T1, con información sobre el desempleo.
    -Sexo: Ambos sexos, hombres, mujeres.
    -Edad: Total y grupos específicos como "55 y más años".
    -Estado civil: Total, solteros/as, divorciados/as, casados/as y viudos/as
     -Sector económico: Agricultura, Industria, Construcción, Servicios, y Parados que buscan primer empleo o han dejado su último empleo hace más de 1 año.
     -Nivel de formación: Analfabetos, Estudios primarios incompletos, Educación primaria, Primera etapa de educación secundaria, Segunda etapa de educación secundaria (general y profesional), Educación superior.
      Variables clave: Número de parados por sector y nivel de formación, número de ocupados, y tasa de paro.

4. **Identificación de patrones y anomalías**
   - Detectados en la pestaña **cuadro de mandos**.

5. **Dashboard visual**
   - KPIs y gráficos con los patrones más relevantes.

> 🛠️ **Herramienta utilizada:** Google Sheets

---

## 📌 Principales Conclusiones

- 📉 **Ciclo económico:** Principal factor que afecta al paro.
- 👩‍💼 **Mujeres:** El paro ha disminuido respecto a los hombres, aunque sigue siendo ligeramente superior en el sector servicios.
- 👵 **Mayores de 55 años:** Aumento del paro debido a:
  - Mayor facilidad de despido.
  - Coste salarial más alto que los jóvenes.
- 🎓 **Educación:**  
  - Sin estudios superiores → 75% de los parados.  
  - Con estudios superiores → 25%.de los parados.
- 💍 **Estado civil:** Aumento del paro en solteros respecto a casados, influido por la disminución de matrimonios.
- 🏭 **Sectores económicos:** Algunos sectores muestran especial impacto, principalmente el sector servicios.

- Enlace a google sheet del proyecto de google sheet análisis del paro en España : https://docs.google.com/spreadsheets/d/18sEcNmsh5eYGXexm05pI8Xs8qouU_zpDh9E4Knxn_iI/edit?usp=sharing
  

---

## ✅ Próximos pasos sugeridos
- Analizar por regiones.
- Estudiar impacto post-pandemia.
- Prever evolución futura del paro.
