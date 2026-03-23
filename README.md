# walmart-desafio-performance-fgp

Este repositorio contiene la solución al desafío técnico para el cargo de Ingeniero performance. El objetivo fue evaluar la estabilidad, escalabilidad y manejo de errores de la plataforma perfappdemo.vercel.app bajo escenarios de carga.

### 🛠️ Stack Tecnológico
* **JMeter 5.5**: Motor principal de ejecución de pruebas.
* **Docker**: Despliegue de infraestructura de monitoreo (InfluxDB + Grafana).
* **InfluxDB 1.8 & Grafana**: Monitoreo en tiempo real de métricas de salud (Throughput, Latencia, Error Rate).

### 🧪 Escenarios de Prueba (Workload Model)
El script ejecuta un flujo de negocio completo:
1. Home - Login y extracción de Bearer Token.
2. Navegación: Users y Products.
3. Checkout para creación de ordenes de compra y validación en Order-List.

### 📊 Resultados Destacados
* **Manejo de Errores**: Se logró una tasa de error del **0.93%** (700 errores sobre 74,651 peticiones totales).
* **Validación de Datos**: Implementación de aserciones personalizadas para asegurar que la API responda con el esquema JSON correcto incluso bajo carga.