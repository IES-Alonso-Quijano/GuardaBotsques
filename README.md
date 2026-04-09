# guardaBOTsques

Sistema inteligente de vigilancia de incendios forestales desarrollado por los alumnos de 2º de Bachillerato de Ciencias de la Computación II del IES Alonso Quijano.

## 📱 Descripción

guardaBOTsques es una aplicación web interactiva que proporciona información en tiempo real sobre el riesgo de incendios forestales basada en datos meteorológicos actuales. La aplicación combina múltiples fuentes de datos para ofrecer una evaluación integral del peligro de incendio en una ubicación específica.

## 🚀 Características principales

- **Localización precisa**: Utiliza el GPS del dispositivo o permite ingresar manualmente una ubicación
- **Datos meteorológicos en tiempo real**: Obtiene temperatura, humedad, velocidad y dirección del viento, precipitación y más desde la API de Open-Meteo
- **Índice FWI simplificado**: Calcula y muestra el Fire Weather Index basado en los parámetros meteorológicos actuales
- **Mapa interactivo**: 
  - Capas base: OpenStreetMap, OpenTopoMap y Imagen satelital ESRI
  - Capas de superposición: Recursos hídricos, senderos, zonas de riesgo y focos activos detectados por satélite
  - Marcador de ubicación actual con círculo de precisión
- **Evaluación multi-factorial**:
  - Riesgo por temperatura, humedad y viento
  - Factores de orientación de ladera (laderas sur y sureste son las más peligrosas)
  - Riesgo por altitud (zonas bajas tienen mayor riesgo)
  - Combustibilidad según tipo de vegetación
- **Guía de interpretación**: Leyenda de colores, umbrales críticos y explicación del índice FWI
- **Recursos externos**: Enlaces directos a fuentes oficiales como AEMET, NASA FIRMS, EFFIS, Windy y Copernicus

## 🛠️ Tecnologías utilizadas

- HTML5, CSS3 y JavaScript vanilla
- Leaflet.js para mapas interactivos
- API de Open-Meteo para datos meteorológicos
- Servicios WMS de Copernicus/EFFIS para capas de riesgo y focos activos
- OpenStreetMap Nominatim para geocodificación y búsqueda de ubicaciones

## 📊 Cómo funciona

1. La aplicación solicita permiso para acceder a la ubicación del dispositivo
2. Obtiene coordenadas GPS y las convierte en un nombre de localidad mediante geocodificación inversa
3. Consulta la API de Open-Meteo para obtener datos meteorológicos actuales de esa ubicación
4. Calcula el índice de riesgo basado en temperatura, humedad y velocidad del viento
5. Muestra los datos en múltiples pantallas:
   - **Mapa Principal**: Visualización cartográfica con capas activables
   - **Meteorología**: Detalles de condiciones actuales y indicadores de peligro
   - **Índice de Riesgo**: Evaluación FWI simplificada y factores contribuyentes
   - **Guía y Leyenda**: Explicación de colores, umbrales y fuentes de datos

## 🎯 Niveles de riesgo

La aplicación utiliza un código de colores para representar diferentes niveles de riesgo:

- **🟢 Verde (Bajo)**: Temperatura <25°C, Humedad >60%, Viento <15 km/h
- **🟡 Amarillo (Moderado)**: Temperatura 25-30°C, Humedad 40-60%, Viento 15-25 km/h
- **🟠 Naranja (Alto)**: Temperatura 30-35°C, Humedad 20-40%, Viento 25-40 km/h
- **🔴 Rojo (Muy Alto)**: Temperatura >35°C, Humedad <20%, Viento >40 km/h
- **🟣 Morado (Catastrófico)**: Múltiples factores máximos simultáneos

## 📱 Compatibilidad

La aplicación está diseñada para funcionar en navegadores modernos de dispositivos móviles y escritorio, con una interfaz optimizada para pantallas táctiles.

## 👥 Desarrolladores

Alumnos de 2º de Bachillerato de Ciencias de la Computación II
IES Alonso Quijano

## 🔗 Enlaces de interés

- [API Open-Meteo](https://open-meteo.com)
- [AEMET - Riesgo de incendios](https://www.aemet.es/es/eltiempo/prediccion/incendios)
- [NASA FIRMS - Incendios activos](https://firms.modaps.eosdis.nasa.gov/map/)
- [EFFIS - European Fire Info System](https://effis.jrc.ec.europa.eu/apps/forecasting.html)
- [Windy - Viento en tiempo real](https://www.windy.com/?wind,now)
- [Copernicus - Monitor de Sequía](https://drought.emergency.copernicus.eu/erdas/en)

---

*guardaBOTsques · IES Alonso Quijano · 2024*