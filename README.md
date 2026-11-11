🛴 Urban Scooter - Proyecto de Control de Calidad (QA)

¡Bienvenido al repositorio de pruebas de Urban Scooter! Este proyecto contiene la documentación completa de control de calidad (QA) aplicada a la plataforma de alquiler de scooters eléctricos en EE. UU., abarcando la experiencia web del cliente y la aplicación móvil del repartidor.

📌 Descripción del Proyecto

Urban Scooter es un servicio de alquiler de scooters por días diseñado para operar en Estados Unidos. La plataforma consta de dos componentes principales:

Aplicación/Web Cliente:

Formulario de Registro/Pedido: Captura de datos personales (Nombre, Apellido, Dirección, Estación de Metro cercana).

Configuración del Pedido (Pantalla "Estado de Pedido"):

Selección de fecha de alquiler (requiere mínimo 1 día de anticipación).

Duración del alquiler (máximo 7 días).

Selección de color (Gris o Negro; si no se especifica, se asigna uno por defecto).

Comentarios opcionales para el repartidor.

Confirmación: Generación de un ID único de pedido para rastreo y redirección automática a la página de inicio.

Aplicación Móvil Repartidor:

Autenticación: Inicio de sesión seguro mediante usuario y contraseña.

Gestión de Pedidos:

Filtrado de pedidos disponibles por estación de metro (permite optimizar la ruta tomando pedidos cercanos).

Exclusión en tiempo real de pedidos ya asignados a otros repartidores.

Tiempos de Entrega: Límite máximo de entrega de 22 horas desde la asignación (con margen total de 24h desde la creación). Notificación push al repartidor a las 22h (2 horas antes del límite).

Vistas de Tarjetas:

Vista corta: Nombre, Estación de Metro y Dirección.

Vista detallada (larga): Nombre, Apellido, Dirección, Estación de Metro, Días de alquiler, Color asignado y Comentario.

Finalización: Cambio de estado del pedido a Completado una vez entregado.

🛠️ Metodología y Estrategia de Pruebas

Para garantizar la máxima cobertura y calidad del software de extremo a extremo (E2E), las pruebas se diseñaron siguiendo la secuencia lógica desde la creación del pedido por el cliente hasta la entrega por el repartidor.

🧠 1. Planificación y Diseño de Pruebas

Mapa Mental: Diagramación de la arquitectura de la app, flujos de usuario, estados de los pedidos y lógica de negocio.

Listas de Comprobación (Checklists): Derivadas directamente de la documentación de requisitos y diseños Figma/UI.

Técnicas de Diseño de Pruebas: Aplicación de Partición de Equivalencia (EP) y Análisis de Valores Límite (BVA) (ej. validar inputs de 1 a 7 días de alquiler, fechas pasadas/futuras, campos obligatorios/opcionales).

🌐 2. Pruebas Web y Multi-navegador

Validación del flujo de pedido en frontend en diferentes navegadores (Chrome, Firefox, Edge, Safari) evaluando compatibilidad y renderizado de interfaz.

📲 3. Pruebas Móviles

Entorno: Emulador de Android Studio (Sistema Operativo: Android 9.0).

Escenarios:

Visualización de tarjetas cortas y detalladas.

Autenticación y filtros por estación de metro.

Pruebas de conectividad: Ejecución de escenarios con acceso y sin acceso a Internet (comportamiento offline / modo avión y sincronización posterior).

Validación del sistema de notificaciones del temporizador de entrega (alerta a las 22h).

📡 4. Pruebas de API

Creación de listas de comprobación y colecciones de pruebas de API utilizando Postman.

Validación de endpoints de creación de pedidos, asignación a repartidores, cambio de estados y manejo de respuestas HTTP/errores.

📊 Documentación y Reporte de Errores

Documentación Excel: Toda la matriz de pruebas, casos de prueba, listas de comprobación y resultados de API se encuentran debidamente estructurados en hojas de cálculo.

Gestión de Defectos (JIRA): Todos los fallos (bugs) identificados durante la ejecución en web, API y móvil fueron reportados minuciosamente en Jira, incluyendo:

Pasos para reproducir.

Resultado esperado vs. Resultado obtenido.

Capturas de pantalla / Logs.

Severidad y Prioridad.

💡 Conclusión y Aprendizajes

Este proyecto me permitió consolidar y aplicar de manera integral los conocimientos adquiridos durante el Bootcamp de QA, fusionándolos con mi experiencia previa y atención al detalle acumulada a lo largo de los años en control de calidad. Se logró una cobertura exhaustiva del producto garantizando un flujo estable y funcional tanto para el cliente final como para la operación logística del repartidor.
