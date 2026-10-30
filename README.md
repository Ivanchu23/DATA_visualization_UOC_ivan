# Visualización de datos de automoción

Tres visualizaciones interactivas, una por técnica (small multiples, slope chart y violin plot), con datos abiertos del sector de la automoción. Hechas con [Plotly.js](https://plotly.com/javascript/) 2.35.2 y publicadas con GitHub Pages.

## Visualizaciones

| Técnica | URL pública |
| --- | --- |
| Portada | https://ivanchu23.github.io/DATA_visualization_UOC_ivan/ |
| Small multiples (grupo I) | https://ivanchu23.github.io/DATA_visualization_UOC_ivan/small-multiples.html |
| Slope chart (grupo II) | https://ivanchu23.github.io/DATA_visualization_UOC_ivan/slope-chart.html |
| Violin plot (grupo III) | https://ivanchu23.github.io/DATA_visualization_UOC_ivan/violin-plot.html |

## Datos

### 1. Small multiples: cuota del diésel en las ventas de turismos nuevos

- **Fuente original:** ICCT (International Council on Clean Transportation), [European Vehicle Market Statistics Pocketbook](https://theicct.org/series/eu-vehicle-market-statistical-pocketbook/).
- **Dataset usado:** [European vehicle passenger sales (ICCT, 2021)](https://github.com/owid/owid-datasets/tree/master/datasets/European%20vehicle%20passenger%20sales%20(ICCT%2C%202021)), publicado por Our World in Data. Licencia CC BY 4.0.
- **Variable:** `diesel_share`, % de turismos nuevos vendidos con motor diésel.
- **Periodo:** 2001–2019 (19 años).
- **Muestra:** 9 países (España, Francia, Italia, Portugal, Alemania, Reino Unido, Irlanda, Suecia y Grecia); 171 valores, uno por país y año.
- **Archivo:** [`data/diesel_cuota_2001_2019.csv`](data/diesel_cuota_2001_2019.csv)

### 2. Slope chart: emisiones medias de CO₂ de los turismos nuevos

- **Fuente original:** ICCT, [European Vehicle Market Statistics Pocketbook](https://theicct.org/series/eu-vehicle-market-statistical-pocketbook/).
- **Dataset usado:** el mismo de Our World in Data, [European vehicle passenger sales (ICCT, 2021)](https://github.com/owid/owid-datasets/tree/master/datasets/European%20vehicle%20passenger%20sales%20(ICCT%2C%202021)). Licencia CC BY 4.0.
- **Variables:** `co2_per_km` (g/km, ciclo de homologación NEDC) y `battery_plugin_electric_share` (% de eléctricos y enchufables, en la información emergente).
- **Periodo:** dos años, 2015 y 2019.
- **Muestra:** 12 países europeos; 24 valores de CO₂.
- **Archivo:** [`data/co2_turismos_2015_2019.csv`](data/co2_turismos_2015_2019.csv)

### 3. Violin plot: consumo combinado por tipo de vehículo y tracción

- **Fuente original:** U.S. EPA y Departamento de Energía de EE. UU., [fueleconomy.gov: Download Fuel Economy Data](https://www.fueleconomy.gov/feg/download.shtml). Dominio público.
- **Dataset usado:** la copia de `vehicles.csv` incluida en el paquete [fueleconomy](https://github.com/hadley/fueleconomy) de Hadley Wickham ([archivo original](https://github.com/hadley/fueleconomy/blob/master/data-raw/vehicles.csv)).
- **Variables:** `comb08` (consumo combinado en mpg, convertido a L/100 km = 235,215 / mpg), `VClass` (agrupada en 5 tipos) y `drive` (agrupada en tracción a dos ruedas o total).
- **Periodo:** años modelo 2013–2015. En esta copia el año 2015 está incompleto: 1.169 versiones de 2013, 1.201 de 2014 y 204 de 2015.
- **Muestra:** 2.574 versiones de 46 marcas, con motor de combustión (incluidos híbridos y flex-fuel; sin eléctricos puros ni gas natural).
- **Archivo:** [`data/consumo_epa_2013_2015.csv`](data/consumo_epa_2013_2015.csv)

## Estructura del repositorio

- `index.html`: portada con enlaces a las tres visualizaciones.
- `small-multiples.html`, `slope-chart.html`, `violin-plot.html`: las visualizaciones.
- `data/`: los CSV que usa cada gráfica.
