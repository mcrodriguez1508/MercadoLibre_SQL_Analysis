# MercadoLibre Funnel & Retention Analysis 🛒📊

## 📝 1. Contexto y Objetivo del Análisis
El objetivo central de este proyecto es evaluar la eficiencia del proceso de compra en MercadoLibre, identificando los puntos de fricción donde se pierde el interés del usuario. 

- **Alcance Geográfico:** 10 países de Latinoamérica.
- **Periodo:** Enero a Agosto de 2024.
- **Definición del Embudo:** El análisis inicia desde el evento inicial **`select_item`** (cuando el usuario hace clic en un producto) y rastrea las **conversiones acumuladas** hasta la transacción final. Esto permite entender cuántos usuarios únicos progresan en cada etapa lógica del flujo.

## 🛠 Metodología
- **Herramientas:** SQL (PostgreSQL) para extracción y agregación; Excel para visualización.
- **Técnicas:** Análisis de Embudo (Funnel) y Análisis de Cohortes de Retención.

## 📊 2. Análisis del Embudo de Conversión
Se observa una caída progresiva en el flujo, con una tasa de éxito final del **1.25%** partiendo del 100% de los usuarios que seleccionan un producto.

- **Punto Crítico:** La mayor pérdida de usuarios ocurre en la transición **`select_item` → `add_to_cart`**. Solo el 15.3% de los que ven un producto deciden agregarlo al carrito.
- **Desempeño por País:** - **Líder:** **Uruguay** destaca con la mejor tasa de conversión (4.55%).
  - **Zonas Críticas:** Ecuador, Colombia y Paraguay muestran un desempeño del 0% en conversión final.

## 🔍 3. Variación por País e Hipótesis
Tras detectar un 0% de conversión en ciertos mercados, se plantean las siguientes **hipótesis de validación adicional** (ya que los datos actuales no permiten conclusiones categóricas):
1. **Fricciones Técnicas:** Posibles fallos en la integración de pasarelas de pago locales o errores de carga en el botón de compra.
2. **Volumen de Datos:** El bajo tráfico en estas regiones podría no ser estadísticamente representativo.
3. **Tracking:** Posibles inconsistencias en el etiquetado de eventos de conversión para estos países específicos.
4. **Barreras de Confianza:** El usuario podría estar en una etapa puramente exploratoria debido a costos de envío no claros.

## 🔄 4. Análisis de Retención
Se analizó la lealtad del usuario mediante el seguimiento de cohortes en hitos estándar: **D7, D14, D21 y D28**.

- **Diagnóstico:** Existe una retención inicial saludable (buen onboarding), pero se detecta un **abandono severo después del día 21**. 
- **Líderes de Retención:** - **Brasil:** Lidera en retención temprana (corto plazo).
  - **México y Perú:** Presentan la retención más sólida a largo plazo (D28), sugiriendo una base de usuarios más fidelizada.

## 💡 5. Implicaciones de Negocio
1. **Falta de Hábito:** El producto logra atraer al usuario inicialmente, pero no consigue establecer un hábito de compra recurrente mensual (el abandono casi total a los 28 días es crítico).
2. **Fricción en el Carrito:** El foco de inversión no debe ser traer más tráfico, sino mejorar la intención de compra en el paso `add_to_cart`.

## 🧩 6. Reflexión Personal y Priorización
He decidido priorizar la optimización de la etapa **`select_item` → `add_to_cart`** por las siguientes razones:
- Es el paso donde el 85% del potencial de venta se pierde.
- **Acciones propuestas:** Mejorar la visibilidad del botón de compra (CTA), transparentar los costos de envío desde la primera vista y fortalecer las insignias de confianza del vendedor. Incrementar la conversión en este punto tendría un impacto mayor en los ingresos que cualquier campaña de marketing masivo.

## 📚 7. Aprendizajes sobre el Comportamiento del Usuario
- **Explorador vs. Comprador:** Una gran parte de la audiencia utiliza la plataforma como catálogo de referencia pero finaliza la compra por otros canales o desiste ante la falta de información clara.
- **Lealtad Volátil:** La retención es frágil; sin incentivos de lealtad entre la segunda y tercera semana, el usuario tiende a olvidar la plataforma.
- **Estructura Regional:** No existe una solución única para Latam; cada país requiere una revisión técnica y de logística local personalizada.

---
**Análisis realizado por:** Maria Camila Rodriguez  
**Herramientas:** SQL | Excel | Estrategia de Producto# MercadoLibre_SQL_Analysis
User behavior and retention analysis for MercadoLibre across 10 countries using SQL. Identified conversion bottlenecks and proposed growth strategies
