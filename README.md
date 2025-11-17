# Sistema-de-Gesti-n-de-Biblioteca


## 1. Descripción del sistema
El Sistema de Gestión de Biblioteca es una aplicación diseñada para optimizar la administración de los recursos bibliográficos en una institución. Permite registrar libros, gestionar préstamos y controlar devoluciones, digitalizando los procesos tradicionales y reemplazando registros manuales por una base de datos estructurada y una interfaz amigable.

La arquitectura es cliente-servidor con almacenamiento local y cuenta con tres módulos principales:

- **Módulo de Libros:** registra nuevos ejemplares, títulos, autores, categorías y disponibilidad.  
- **Módulo de Préstamos:** gestiona la asignación de libros a usuarios y controla fechas de entrega y devolución.  
- **Módulo de Reportes:** genera listados de préstamos activos, devoluciones pendientes y estadísticas de uso.  

El sistema está orientado a bibliotecas pequeñas o medianas en instituciones educativas o centros culturales. Los usuarios finales son los administradores o bibliotecarios. A futuro, se planea incluir acceso en línea para que los lectores consulten disponibilidad y hagan reservas.

## Objetivo

Desarrollar un Sistema de Gestión de Biblioteca que permita administrar eficientemente los libros, préstamos y devoluciones, asegurando la disponibilidad de los recursos bibliográficos y facilitando la trazabilidad de los usuarios, mediante una interfaz amigable y procesos digitalizados que optimicen la gestión de la información.


---

## 2. Requerimientos funcionales
1. **Inicio de credenciales de usuario (seguridad)**  
   El sistema permite iniciar sesión utilizando nombre de usuario y contraseña proporcionados por la institución.

2. **Base de datos de libros (operación)**  
   Clasificación y registro de libros disponibles para los usuarios.

3. **Clasificación de reingresos (comunicación)**  
   Notificación de libros entregados y control de fechas de devolución.

4. **Préstamos de libros (informes)**  
   Registro de libros prestados y control de disponibilidad.

5. **Tiempos de entrega (notificación)**  
   Control de fechas límite para la devolución de los libros.

---

## 3. Requerimientos no funcionales
1. **Rendimiento (rendimiento)**  
   Optimizar tiempos de carga y minimizar tráfico de datos.

2. **Seguridad de datos (seguridad)**  
   Protección de datos y privacidad de los usuarios.

3. **Compatibilidad multiplataforma (compatibilidad)**  
   Funcionamiento correcto en diferentes entornos y plataformas.

---

## 4. Tabla de pruebas

| Tipo de prueba | Requerimiento asociado | Datos de entrada | Resultado esperado | Resultado obtenido |
|----------------|----------------------|-----------------|------------------|------------------|
| Unitario | Gestión de libros | Libro: análisis de sistema | El sistema registra el libro. Cantidad 5 | El sistema registra el libro. Cantidad 5 |
| Unitario | Registro de préstamo | Usuario: Jared Semper, Cantidad de libros 4 | El préstamo se registra | El préstamo se registra y la cantidad disponible se actualiza a 4 |
| Unitario | Registro de devolución | Devolución: 24/12/2025 | La devolución se registra. Cantidad de libros 5 | La devolución se registra y la cantidad se actualiza a 5 (éxito) |
| Validación | Registro de préstamo | Usuario: Jared Semper (Sin stock) | El sistema rechaza el préstamo | El sistema rechaza el préstamo y muestra el mensaje de error |
| Validación | Gestión de libros | Análisis de sistema (ya registrado) | El sistema debe rechazar el registro del libro | El sistema rechaza el registro por duplicado |

# Mantenimiento del Sistema

## Mantenimiento Correctivo
Se centra en corregir defectos detectados durante el funcionamiento del sistema, como los errores de validación en préstamos duplicados.

- **Justificación teórica:** Restablecer el funcionamiento normal del software, garantizando la integridad de los datos.  
- **Justificación técnica:** Corregir la lógica de validación de disponibilidad de libros para evitar préstamos simultáneos del mismo ejemplar, aumentando la confiabilidad del sistema.

## Mantenimiento Perfectivo
Busca mejorar las características funcionales y de rendimiento, incorporando nuevas funciones según las necesidades del usuario.

- **Justificación teórica:** Amplía la funcionalidad del software sin modificar su estructura principal.  
- **Justificación técnica:** Añadir un módulo de usuarios y control de disponibilidad mejora la trazabilidad y eficiencia en la gestión bibliotecaria.

## Justificación General
La aplicación de estos mantenimientos optimiza el uso del sistema y garantiza mayor control sobre los recursos bibliográficos.

- **Técnica:** Nuevas tablas y validaciones mejoran la calidad de los datos y reducen errores humanos.  
- **Organizativa:** Permite transparencia en la gestión de préstamos, identificando qué usuario tiene cada libro y sus fechas de devolución.  
- **Escalabilidad:** Facilita la adaptación del sistema a nuevas tecnologías o plataformas web.  
- **Pedagógica:** Fortalece la aplicación de conceptos de ingeniería de software en contextos reales, desarrollando competencias profesionales del equipo.

## Reflexión Final

El mantenimiento de software es clave en el ciclo de vida de cualquier sistema.  
En el caso del Sistema de Gestión de Biblioteca, el análisis y mejora del sistema evidenció cómo la ingeniería de software asegura la calidad y sostenibilidad de las aplicaciones.  

Las mejoras realizadas no solo corrigen errores, sino que también amplían la utilidad del sistema, alineándolo con las necesidades reales de los usuarios. La aplicación de buenas prácticas, como la documentación adecuada y la normalización de bases de datos, garantiza la mantenibilidad del proyecto a lo largo del tiempo.  

Este trabajo demuestra que la mejora continua es esencial en el desarrollo de software, y que incluso sistemas pequeños pueden beneficiarse significativamente de un enfoque estructurado de mantenimiento y evolución.

