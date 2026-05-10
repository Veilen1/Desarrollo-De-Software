# Sistema de Gestión Académica para Posgrado - UTN FRLP

## Integrantes
* Luciano Privitera 33203
* Emilio  Benjamín Rivero 34040
* Valentin Garcia Devrient 33800
* Redruello Lautaro 33334
* Lucio Angel 33664
* Araceli Melina Dávila 26901


Este repositorio contiene el **Product Backlog** desarrollado para el Sistema de Gestión Académica de Posgrado de la UTN Facultad Regional La Plata. El proyecto aplica metodologías ágiles (Scrum) para centralizar la información de aspirantes, alumnos y docentes.

## 1. Identificación de Actores
Se han identificado los siguientes roles clave para el funcionamiento del sistema:

* **Aspirante**: Persona interesada en las carreras que realiza el proceso de admisión.
* **Estudiante**: Usuario con legajo activo que cursa seminarios y realiza el seguimiento de su avance.
* **Docente**: Responsable de la carga de asistencia y calificaciones de sus seminarios.
* **Equipo de Conducción**: Autoridades encargadas de la supervisión administrativa y análisis estadístico.
* **CPR (Comisión de Posgrado Regional)**: Responsables de la gestión de tesis y trabajos finales.

## 2. Épicas del Sistema
Las funcionalidades se agrupan en cinco épicas principales:

* **EP-01**: Gestión de Inscripciones
* **EP-02**: Legajo y Perfil Académico
* **EP-03**: Gestión Docente
* **EP-04**: Estadísticas y Reportes
* **EP-05**: Administración y Seguridad

## 3. Product Backlog
A continuación se presenta el backlog con 17 historias de usuario, incluyendo dos criterios de aceptación por cada una, estimación en Story Points (Fibonacci) y prioridad MoSCoW.

| ID | Épica | Historia de Usuario | Criterios de Aceptación (Gherkin) | SP | Pri. | Sprint |
|:---|:---|:---|:---|:---:|:---:|:---:|
| **US-01** | EP-01 | Como aspirante, quiero completar un formulario web, para inscribirme sin enviar correos. | 1. **Dado** que el aspirante ingresa al enlace, **Cuando** completa los campos obligatorios, **Entonces** los datos se guardan.<br>2. **Dado** que faltan campos, **Cuando** intenta enviar, **Entonces** el sistema destaca los errores. | 5 | M | 1 |
| **US-02** | EP-01 | Como aspirante, quiero adjuntar mis documentos en PDF, para completar mi legajo digital. | 1. **Dado** un archivo PDF, **Cuando** se sube, **Entonces** se asocia al legajo.<br>2. **Dado** un formato no PDF, **Cuando** se intenta subir, **Entonces** el sistema rechaza la carga. | 3 | M | 1 |
| **US-03** | EP-01 | Como conducción, quiero ver el estado del legajo con indicador visual, para saber si está completo. | 1. **Dado** el panel de control, **Cuando** el legajo está completo, **Entonces** muestra un indicador verde.<br>2. **Dado** un legajo incompleto, **Cuando** se revisa, **Entonces** detalla los documentos faltantes. | 3 | M | 2 |
| **US-04** | EP-02 | Como conducción, quiero registrar asistencia y notas, para actualizar el estado académico de forma manual. | 1. **Dado** el ingreso de notas válidas, **Cuando** se confirma, **Entonces** el perfil se actualiza al instante.<br>2. **Dado** una nota fuera de rango, **Cuando** se guarda, **Entonces** el sistema bloquea la acción. | 5 | M | 2 |
| **US-05** | EP-03 | Como docente, quiero acceder vía enlace, para cargar datos sin necesidad de usuario/contraseña. | 1. **Dado** un link único, **Cuando** el docente lo abre, **Entonces** accede solo a su seminario.<br>2. **Dado** un link vencido, **Cuando** se intenta usar, **Entonces** el sistema deniega el acceso. | 3 | S | 3 |
| **US-06** | EP-01 | Como aspirante, quiero seleccionar el tipo de beca, para formalizar mi solicitud económica. | 1. **Dado** la selección de beca, **Cuando** se marca el %, **Entonces** se habilita la carga del comprobante.<br>2. **Dado** que no se adjunta el PDF, **Cuando** se intenta finalizar, **Entonces** el sistema solicita el documento. | 2 | S | 1 |
| **US-07** | EP-02 | Como conducción, quiero realizar búsquedas por DNI, para agilizar la atención de estudiantes. | 1. **Dado** un DNI existente, **Cuando** se busca, **Entonces** redirige al perfil del alumno.<br>2. **Dado** un DNI no registrado, **Cuando** se busca, **Entonces** el sistema notifica que no hay resultados. | 3 | M | 2 |
| **US-08** | EP-02 | Como estudiante, quiero ver un indicador "semáforo", para comprender mi progreso actual. | 1. **Dado** un avance > 75%, **Cuando** se ve el perfil, **Entonces** el semáforo es verde.<br>2. **Dado** deudas académicas, **Cuando** se accede, **Entonces** el indicador cambia a amarillo o rojo. | 5 | S | 3 |
| **US-09** | EP-02 | Como CPR, quiero registrar los datos de la tesis, para oficializar el seguimiento del trabajo final. | 1. **Dado** los datos de Director y Resolución, **Cuando** se guardan, **Entonces** se bloquea la edición externa.<br>2. **Dado** la falta de resolución, **Cuando** se intenta registrar, **Entonces** el sistema impide el guardado. | 3 | M | 4 |
| **US-10** | EP-03 | Como docente, quiero registrar la asistencia por fecha, para cumplir con la normativa. | 1. **Dado** el marcado de presentes, **Cuando** se guarda, **Entonces** se actualiza el % de asistencia.<br>2. **Dado** asistencia bajo el mínimo, **Cuando** se cierra el acta, **Entonces** el alumno queda como "Libre". | 5 | M | 3 |
| **US-11** | EP-04 | Como conducción, quiero visualizar el desgranamiento, para analizar la deserción por cohorte. | 1. **Dado** el filtro por cohorte, **Cuando** se genera el reporte, **Entonces** muestra el % de bajas.<br>2. **Dado** una consulta global, **Cuando** se procesa, **Entonces** permite comparar carreras de posgrado. | 8 | C | 5 |
| **US-12** | EP-01 | Como conducción, quiero abrir o cerrar periodos de inscripción, para controlar el ingreso. | 1. **Dado** el estado "Cerrado", **Cuando** se accede al link, **Entonces** el usuario ve un aviso de cierre.<br>2. **Dado** el estado "Abierto", **Cuando** se accede, **Entonces** el formulario de inscripción está activo. | 2 | M | 1 |
| **US-13** | EP-02 | Como conducción, quiero recibir alertas sobre vencimientos, para prevenir la pérdida de regularidad. | 1. **Dado** un seminario próximo a vencer, **Cuando** se abre el panel, **Entonces** se resalta en rojo.<br>2. **Dado** un seminario ya aprobado, **Cuando** se verifica el plazo, **Entonces** no se genera alerta. | 5 | S | 4 |
| **US-14** | EP-02 | Como usuario, quiero descargar mi perfil en PDF, para contar con un comprobante de mi estado. | 1. **Dado** el botón de descarga, **Cuando** se pulsa, **Entonces** se genera el archivo PDF con el resumen.<br>2. **Dado** datos pendientes, **Cuando** se genera el PDF, **Entonces** incluye una nota de información preliminar. | 3 | C | 4 |
| **US-15** | EP-03 | Como docente, quiero descargar la planilla, para su uso físico durante la clase. | 1. **Dado** la opción de impresión, **Cuando** se selecciona, **Entonces** genera un formato A4 optimizado.<br>2. **Dado** actualizaciones en la lista, **Cuando** se descarga, **Entonces** asegura incluir a los nuevos alumnos. | 2 | S | 3 |


---
Desarrollo de Software - UTN FRLP
