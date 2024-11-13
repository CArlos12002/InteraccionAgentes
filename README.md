# Simulación de Intersección con Semáforos Inteligentes

Este proyecto simula una intersección controlada por semáforos inteligentes utilizando la biblioteca **Mesa** para modelar sistemas multiagente. La simulación incluye semáforos que detectan vehículos cercanos, vehículos que envían mensajes con su tiempo estimado de llegada (ETA) y un sistema de visualización en una cuadrícula.

## Características
1. **Semáforos Inteligentes**:
   - Cambian entre los estados **rojo**, **amarillo** y **verde**.
   - Detectan vehículos cercanos y priorizan carriles basándose en el tiempo estimado de llegada (ETA).

2. **Vehículos Inteligentes**:
   - Calculan y envían su ETA a los semáforos más cercanos.
   - Se mueven a través de carriles definidos en la cuadrícula.

3. **Carriles Representados**:
   - Cada dirección tiene tres carriles.
   - Vehículos eligen carriles según su objetivo y siguen reglas de tránsito.

4. **Visualización**:
   - Los semáforos se muestran como rectángulos con colores que indican su estado.
   - Los vehículos se muestran como círculos que cambian de color según su estado (en movimiento o detenidos).

5. **Comunicación entre Agentes**:
   - Los vehículos envían mensajes a los semáforos para coordinar el flujo de tráfico.

---

## Instalación

### 1. Requisitos Previos
- Python 3.8 o superior.
- Biblioteca **Mesa**.

### 2. Clona el Repositorio
```bash
git clone <URL_DEL_REPOSITORIO>
cd <NOMBRE_DEL_PROYECTO>
3. Crea un Entorno Virtual
bash
Copiar código
python3 -m venv env
source env/bin/activate  # macOS/Linux
# Para Windows:
# .\env\Scripts\activate
4. Instala las Dependencias
bash
Copiar código
pip install mesa
Uso
1. Ejecuta la Simulación
bash
Copiar código
python run.py
2. Accede a la Interfaz
Abre tu navegador y ve a: http://127.0.0.1:8521.
3. Controles de la Simulación
Start: Inicia la simulación.
Stop: Detiene la simulación.
Reset: Reinicia la simulación desde el principio.
Archivos del Proyecto
model.py
Define los agentes y el modelo:

SmartTrafficLight: Agente semáforo.
Vehicle: Agente vehículo.
IntersectionModel: Modelo principal que gestiona los agentes.
server.py
Configura la visualización de los agentes en la cuadrícula utilizando la biblioteca Mesa.

run.py
Archivo principal para iniciar el servidor.

Visualización
Semáforos:

Red: Estado rojo (detiene vehículos).
Yellow: Estado amarillo (advertencia).
Green: Estado verde (permite el paso).
Vehículos:

Blue: Vehículo en movimiento.
Gray: Vehículo detenido o fuera de la cuadrícula.
Personalización
Cambiar el Tamaño de la Cuadrícula
En server.py, ajusta el tamaño de la cuadrícula modificando estos parámetros:

python
Copiar código
grid = CanvasGrid(agent_portrayal, 10, 10, 500, 500)
Ajustar el Número de Agentes
En model.py, modifica el número de semáforos y vehículos:

Autor
Proyecto desarrollado por [Tu Nombre] como un ejercicio de simulación multiagente utilizando Mesa.
