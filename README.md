# **Simulación de Intersección Inteligente**

## **Introducción**

Hemos desarrollado este proyecto con el propósito de modelar un **sistema multiagente** que simula una intersección controlada por **semáforos inteligentes**. Nuestro objetivo es optimizar el flujo vehicular, reducir los tiempos de espera y maximizar la "felicidad" de los vehículos al mismo tiempo que manejamos configuraciones tanto cooperativas como competitivas entre los agentes.

La simulación incluye **semáforos adaptativos**, vehículos con comportamientos dinámicos y la integración de principios de **Teoría de Juegos** para priorizar movimientos de manera justa. Además, implementamos un sistema de comunicación descentralizado para que los agentes interactúen de manera realista.

---

## **Características**

1. **Semáforos Inteligentes**:
   - Los semáforos están programados para adaptarse dinámicamente según la proximidad de los vehículos.
   - Por defecto, los semáforos permanecen en **amarillo** cuando no hay vehículos cercanos.
   - Cuando un vehículo se aproxima, envía un mensaje con su **tiempo estimado de llegada**, lo que permite al semáforo cambiar a **verde**.

2. **Vehículos Autónomos**:
   - Los vehículos tienen una **métrica de felicidad** que se ajusta dependiendo de su tiempo de espera o movimiento.
   - Los vehículos pueden adoptar diferentes comportamientos:
     - Cooperativos: trabajan con otros vehículos para optimizar el flujo.
     - Competitivos: buscan su propio beneficio.
   - Cada vehículo cambia de color según su nivel de felicidad:
     - **Verde**: Feliz.
     - **Amarillo**: Neutral.
     - **Rojo**: Enojado.

3. **Intersección Completa**:
   - Incluimos **ocho semáforos** bien centralizados, con **tres carriles por dirección** (Norte-Sur y Este-Oeste).
   - Los carriles están organizados para giros y movimientos rectos, siguiendo convenciones sociales para el cambio de carril.

4. **Integración de Teoría de Juegos**:
   - Implementamos una estrategia basada en una **Matriz de Recompensas**, identificando equilibrios de Nash para priorizar direcciones en conflicto.
   - Esto asegura que ninguna dirección tenga prioridad absoluta y fomenta la equidad.

5. **Comunicación Descentralizada**:
   - Los vehículos se comunican directamente con los semáforos cercanos para enviar datos de arribo.
   - Evitamos la centralización para que el sistema sea escalable.

6. **Desempeño Medido**:
   - Monitoreamos métricas como la felicidad promedio de los vehículos y el rendimiento de los semáforos.

---

## **Cómo instalar y ejecutar**

### **Requisitos previos**
1. Tener Python 3.9 o superior instalado.
2. Instalar la librería **Mesa** para la simulación multiagente:
   ```bash
   pip install mesa
   ```

### **Instalación**
1. Descarga los archivos del proyecto en tu computadora.
2. Ubica el archivo principal del modelo, por ejemplo, `centralized_semaphores_model.py`.

### **Ejecución**
1. Ejecuta el archivo principal desde la terminal:
   ```bash
   python centralized_semaphores_model.py
   ```
2. Se abrirá una interfaz donde podrás visualizar el modelo en acción.

### **Parámetros ajustables**
- Puedes modificar variables como:
  - **`spawn_probability`**: Ajusta la tasa de generación de vehículos.
  - **Duraciones de los semáforos**: Cambia los tiempos para los estados verde, amarillo y rojo.

---

## **Cómo funciona**

1. **Agentes involucrados**:
   - **Semáforos inteligentes**:
     - Determinan su estado en función del tiempo de arribo de los vehículos.
     - Coordinan el flujo vehicular para evitar bloqueos.
   - **Vehículos autónomos**:
     - Se comunican con los semáforos.
     - Modifican su estado y color en base a su felicidad.

2. **Carriles**:
   - Tres carriles por dirección (Norte-Sur y Este-Oeste).
   - Cada carril tiene un propósito: movimiento recto o giros.

3. **Felicidad de los vehículos**:
   - Los vehículos buscan maximizar su felicidad avanzando rápidamente y evitando bloqueos.
   - Cambian de color dependiendo de su nivel de felicidad:
     - Verde: Felices.
     - Amarillo: Neutrales.
     - Rojo: Enojados.

4. **Estrategia basada en Teoría de Juegos**:
   - Implementamos una **matriz de recompensas** para definir prioridades de paso.
   - Esto fomenta la justicia entre los vehículos de diferentes direcciones.

5. **Eliminación de vehículos**:
   - Los vehículos desaparecen al cruzar completamente la intersección, simulando tráfico continuo.

---

## **Resultados esperados**

Al ejecutar la simulación, podrás observar:
- **Interacción fluida** entre los vehículos y los semáforos.
- Cambios en el color de los vehículos según su nivel de felicidad.
- Semáforos que adaptan sus tiempos en función de los vehículos presentes.
- Flujo equilibrado en todas las direcciones, evitando bloqueos.

---

## **Contribuciones de equipo**

En el desarrollo del proyecto:
- Implementamos los **semáforos inteligentes** y su programación adaptativa.
- Diseñamos la **métrica de felicidad** de los vehículos y sus estados.
- Organizamos los **carriles** y configuramos un sistema descentralizado de comunicación.
- Integramos estrategias de **Teoría de Juegos** para resolver conflictos en las direcciones.

---

## **Mejoras futuras**

1. Implementar algoritmos avanzados para optimizar las decisiones de los semáforos.
2. Introducir vehículos más inteligentes con algoritmos de aprendizaje automático.
3. Expandir el modelo a múltiples intersecciones conectadas.

---

## **Conclusión**

Este proyecto es un ejemplo de cómo los sistemas multiagente pueden resolver problemas complejos como la gestión del tráfico. Utilizando principios de Teoría de Juegos, comunicación descentralizada y métricas de felicidad, logramos un sistema eficiente, justo y escalable.

## Autor
Proyecto desarrollado por 
### Carlos Anaya Ruiz (A01662464)
