# it-workshop-management
sistema de gestion para taller informatico 
# Sistema de Gestión para Taller Informático
## Proyecto: "Tu informático te ayuda"

# Sistema de Gestión para Taller Informático "Tu informático te ayuda"

## Descripción del Proyecto
Sistema completo de gestión para taller de reparación de equipos informáticos desarrollado con metodología Scrum.  
El software permite gestionar todo el ciclo de reparación: desde la recepción del equipo hasta la entrega al cliente.

## Historias de Usuario Identificadas

### Épica 1: Recepción del Equipo Defectuoso
1. **HU1:** Como cliente, quiero registrar mi equipo en reparación para obtener un comprobante de recepción.
2. **HU2:** Como recepcionista, quiero capturar datos del cliente (nombre, contacto, descripción del problema) para crear un registro completo.
3. **HU3:** Como sistema, debo asignar un identificador único a cada equipo para su rastreo.

### Épica 2: Diagnóstico Técnico
4. **HU4:** Como técnico, quiero registrar síntomas y problemas reportados para realizar un diagnóstico preciso.
5. **HU5:** Como técnico, necesito generar un informe de diagnóstico detallado para presentar al cliente.
6. **HU6:** Como cliente, quiero recibir el diagnóstico de mi equipo para entender el problema.

### Épica 3: Gestión de Proveedores e Inventario
7. **HU7:** Como encargado de almacén, quiero crear y seguir comandas de compra de piezas.
8. **HU8:** Como almacenista, necesito gestionar el inventario de piezas (entrada, salida, stock disponible).
9. **HU9:** Como comprador, quiero contactar proveedores para adquirir piezas necesarias.

### Épica 4: Presupuesto y Aprobación
10. **HU10:** Como administrador, quiero elaborar presupuestos detallados (mano de obra, piezas, tiempo estimado).
11. **HU11:** Como cliente, quiero recibir el presupuesto por email para su revisión.
12. **HU12:** Como cliente, necesito aprobar o rechazar el presupuesto recibido.

### Épica 5: Ejecución de la Reparación
13. **HU13:** Como jefe de taller, quiero asignar tareas al personal técnico según especialización.
14. **HU14:** Como técnico, quiero registrar avances y finalización de la reparación.
15. **HU15:** Como sistema, debo generar un informe de reparación completo.

### Épica 6: Gestión de Garantía
16. **HU16:** Como administrador, necesito establecer y seguir el período de garantía para cada reparación.
17. **HU17:** Como cliente, quiero conocer los términos de la garantía de mi reparación.
18. **HU18:** Como técnico, debo registrar incidencias post-reparación y su resolución.

### Épica 7: Planificación de Tareas
19. **HU19:** Como manager, quiero un calendario de tareas y asignación de recursos.
20. **HU20:** Como equipo, necesitamos seguimiento del progreso de las reparaciones.
21. **HU21:** Como usuario, quiero recibir notificaciones y recordatorios de tareas pendientes.

## Arquitectura Técnica

### Frontend
- **Framework:** React.js con TypeScript
- **Estilos:** Tailwind CSS
- **Estado:** Redux Toolkit
- **Routing:** React Router v6

### Backend
- **Framework:** Django REST Framework
- **Base de datos:** PostgreSQL
- **Autenticación:** JWT Tokens
- **API:** RESTful API

### DevOps
- **Contenedores:** Docker & Docker Compose
- **CI/CD:** GitHub Actions
- **Despliegue:** AWS/Heroku
- **Monitoring:** Sentry, LogRocket

## 📊 Product Backlog

### Prioridad Alta (MVP)
1. **RF1.1:** Formulario de recepción de equipos
2. **RF1.2:** Generación automática de IDs únicos
3. **RF1.3:** Gestión básica de clientes
4. **RF2.1:** Formulario de diagnóstico técnico
5. **RF4.1:** Generador de presupuestos básicos

### Prioridad Media
6. **RF3.1:** Sistema de gestión de inventario
7. **RF3.2:** Módulo de proveedores
8. **RF5.1:** Asignación de tareas a técnicos
9. **RF5.2:** Seguimiento de reparaciones
10. **RF6.1:** Gestión de garantías

### Prioridad Baja
11. **RF7.1:** Calendario de tareas
12. **RF7.2:** Sistema de notificaciones
13. **RNF3.1:** Control de acceso por roles
14. **RNF4.1:** Reportes avanzados
15. **RNF7.1:** Dashboard administrativo

## Roadmap de Sprints (12 semanas total)

### Sprint 1: Fundamentos (2 semanas)
- Configuración del proyecto
- Módulo de recepción básico
- Base de datos inicial

### Sprint 2: Diagnóstico (2 semanas)
- Sistema de diagnóstico técnico
- Informes básicos
- Mejoras en UI/UX

### Sprint 3: Inventario (2 semanas)
- Gestión de stock de piezas
- Módulo de proveedores
- Comandas de compra

### Sprint 4: Presupuestos (2 semanas)
- Generador de presupuestos
- Sistema de aprobaciones
- Envío por email

### Sprint 5: Reparación (2 semanas)
- Asignación de tareas
- Seguimiento de reparaciones
- Informes finales

### Sprint 6: Finalización (2 semanas)
- Sistema de garantías
- Calendario y planificación
- Despliegue inicial

## Equipo Scrum

| Rol | Nombre | Responsabilidades | Contacto |
|-----|--------|-------------------|----------|
| **Product Owner** | Rustam | Definir requisitos, priorizar backlog, validar entregables | email@gmail.com
| **Scrum Master** | Rustam | Facilitar ceremonias, remover impedimentos, asegurar proceso Scrum | email@gmail.com
| **Desarrollador Frontend** | Rustam | Implementar interfaz de usuario, asegurar UX óptima | email@gmail.com
| **Desarrollador Backend** | Rustam | Desarrollar API, lógica de negocio, base de datos | [ email@gmail.com

### Ceremonias Scrum
- **Daily Stand-up:** Lunes a Viernes 9:00 AM (15 minutos)
- **Sprint Planning:** Lunes inicio de sprint (2 horas)
- **Sprint Review:** Viernes fin de sprint (1.5 horas)
- **Sprint Retrospective:** Viernes post-review (1 hora)

## Instalación y Configuración

### Requisitos Previos
- Python 3.9+
- Node.js 16+
- PostgreSQL 13+
- Docker (opcional)

### Instalación Local
```bash
# 1. Clonar repositorio
git clone https://github.com/tu-usuario/it-workshop-management.git
cd it-workshop-management

# 2. Configurar entorno backend
cd backend
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate
pip install -r requirements.txt

# 3. Configurar base de datos
python manage.py migrate
python manage.py createsuperuser

# 4. Configurar frontend
cd ../frontend
npm install

# 5. Ejecutar servidores
# Terminal 1 (backend):
python manage.py runserver

# Terminal 2 (frontend):
npm start
