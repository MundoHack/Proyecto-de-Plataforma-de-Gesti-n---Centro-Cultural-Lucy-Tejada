# Proyecto-de-Plataforma-de-Gesti-n---Centro-Cultural-Lucy-Tejada
El proyecto propone el desarrollo de una plataforma web integral para el Centro Cultural Lucy Tejada de Pereira, con el fin de modernizar y automatizar la gestión académica y administrativa de sus programas artísticos.
Proyecto de Plataforma de Gestión - Centro Cultural Lucy Tejada

El proyecto propone el desarrollo de una plataforma web integral para el Centro Cultural Lucy Tejada de Pereira, con el fin de modernizar y automatizar la gestión académica y administrativa de sus programas artísticos. Se busca reemplazar la dependencia actual de la plataforma de la Alcaldía y otorgar autonomía al centro en la administración de estudiantes, educadores y reportes.
🗂️ Tablero de Trello: “Backend - Plataforma de Gestión Cultural (Django)”
🔹 Listas principales (columnas en Trello):
Backlog (por desarrollar)


En desarrollo


En revisión / testing


Completado


Bloqueado / pendiente de integración


👩‍💻 Asignación de Roles del Equipo (3 personas)
Rol
Responsabilidad Principal
Django Focus
Dev 1 - Usuarios y Autenticación
Manejo de login, registro, roles, seguridad y perfiles.
Django Auth, JWT, Sessions
Dev 2 - Programas y Gestión Académica
CRUD de programas, grupos, matrículas, evaluaciones y asistencia.
Django ORM, Views, Models
Dev 3 - Dashboards y Reportes
Generación de datos, estadísticas, filtros y dashboards.
Django Rest Framework + Pandas/Matplotlib o integraciones



📋 Organización por Paneles (Cards de Trello)
🟦 1. Panel del Visitante Público
Responsable principal: Dev 2
Tareas:
Configurar modelos base (Programas, Categorías, Educadores visibles públicamente)

Vista API detalle_del_programa_formativo (GET)

Vista API lista_de_programas_formativos (GET con filtros y búsqueda por palabra clave)

Página de inicio (homepage) → Endpoint con banners, misión/visión, eventos destacados

Endpoint noticias / eventos culturales

Integración inicial con frontend (consumo JSON público)

🟩 2. Panel del Estudiante
Responsable principal: Dev 1
Tareas:
Modelo Estudiante (UserProfile extendido)

Vista de inicio_de_sesión_y_registro (Auth + Token)

Módulo de seguridad (reset password, cambio de clave inicial)

Mi perfil (GET/PUT del usuario autenticado)

Mi progreso académico (relación con evaluaciones + programas)

Mis programas y horarios (GET con joins Programas-Grupo-Horario)

Panel principal del estudiante (dashboard) → Datos combinados: próximas clases, notificaciones, progreso.

🟨 3. Panel del Educador
Responsable principal: Dev 2
Tareas:
Modelo Educador (User con rol docente y permisos específicos)

Gestión de grupos (CRUD de grupos, asignación de estudiantes)

Registro de asistencia (POST, PUT, vista filtrada por grupo)

Evaluación cualitativa de estudiantes (modelo Evaluación con campos texto/fecha/programa)

Panel principal del educador (dashboard) → Resumen de grupos, asistencia promedio, últimas evaluaciones.


🟥 4. Panel del Personal Administrativo
Responsable principal: Dev 3
Tareas:
Dashboard principal administrativo (estadísticas generales con agregaciones ORM)

Gestión de estudiantes (con filtros)

Filtros por programa, ciudad, edad, género, grupo

Exportación CSV/PDF

Gestión de programas, grupos y educadores (CRUD completo)

Generador de reportes

Creación de endpoints /reportes/ con filtros dinámicos y exportación

Integrar librería pandas o reportlab para reportes automáticos



⚙️ Tareas Técnicas Transversales
Coordinadas por todos
Configuración inicial del proyecto Django (settings, apps, urls)

Instalación y configuración de Django Rest Framework

Autenticación JWT + permisos por rol

Configuración base de datos PostgreSQL

Creación de fixtures iniciales (programas, roles)

Pruebas unitarias (pytest / Django test)

Configuración de media/static files

Implementación de auditoría (registro de logs)

Configuración de entorno staging


📊 Prioridad de Desarrollo (Sprint recomendado)
Sprint
Objetivo
Paneles Prioritarios
Sprint 1
Base de usuarios y autenticación
Estudiante (login, registro), Administrativo
Sprint 2
Gestión académica básica
Educador (asistencia, evaluación), Programas
Sprint 3
Dashboards y reportes
Administrativo, Estudiante
Sprint 4
Optimización, seguridad y pruebas finales
Todos los módulos

🧩 Etiquetas en Trello
🟢 Listo para revisar
🔵 En desarrollo
🟡 Dependencia de otro módulo
🔴 Bloqueado
🟣 Prioridad alta


⚫ Testing / QA
