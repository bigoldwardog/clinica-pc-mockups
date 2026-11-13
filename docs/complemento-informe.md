# Complemento al informe técnico de la Clínica del PC

Este anexo desarrolla los criterios 2.1.1, 2.1.3 y 2.1.4 de la Guía de Trabajo N.º 2 de TI3043. Los identificadores RF-01 a RF-09 vinculan los pasos de la guía con los [mockups](mockups.html) y los escenarios de revisión. Se conserva como referencia el diseño UML del informe original.

## 2.1.1 Metodología y ciclo de vida

Se propone Scrum como marco de trabajo para un ciclo de vida iterativo e incremental. El flujo general está definido por la guía, pero quedan decisiones operativas que conviene resolver al revisar ejemplos concretos, como identificar el equipo correcto cuando un RUT tiene varias inscripciones y decidir qué hacer si el funcionamiento cambia después de la intervención. Revisar primero el recorrido con recepción y después el recorrido técnico permite ajustar esas decisiones antes de invertir tiempo en implementar el sistema completo.

El informe identifica dos integrantes y la pauta describe una evaluación individual. La asignación de responsabilidades y el tiempo disponible deben confirmarse con el docente. En la fase de diseño se puede usar un único backlog en GitHub, los diagramas existentes en PlantUML y el HTML local con datos ficticios. Para una futura ejecución con Scrum se deberá acordar quién asume las responsabilidades de Product Owner, Scrum Master y Developers. Se propone que el docente o encargado participe como representante del cliente en las revisiones.

| Iteración propuesta | Objetivo | Evidencia para revisar |
| --- | --- | --- |
| 1 · Ingreso y recepción | Identificar correctamente a la persona y al dispositivo, incluso cuando hay más de uno registrado. | Demostración de RF-01 y RF-02 con dos dispositivos ficticios y registro de decisiones sobre datos obligatorios. |
| 2 · Atención técnica | Conservar evidencia del funcionamiento inicial, el trabajo ejecutado y el resultado posterior. | Recorrido RF-03 a RF-06 con falla preexistente y diferencia posterior. |
| 3 · Entrega y cierre | Mantener la trazabilidad hasta el retiro y el estado final. | Recorrido RF-07 a RF-09 y ensayo integral con una orden ficticia. |

La duración de cada iteración y las fechas de revisión se fijarán con el calendario de la asignatura y la disponibilidad de la contraparte. En la fase de diseño, cada revisión entrega un prototipo actualizado y decisiones registradas. En la futura fase de implementación, cada Sprint busca entregar un incremento usable. En Sprint Planning se seleccionan los requisitos según riesgo y capacidad. El equipo inspecciona su avance en el Daily Scrum. En Sprint Review, las observaciones de la contraparte se convierten en ajustes del Product Backlog. En la retrospectiva se revisa cómo mejorar el trabajo del equipo.

| Riesgo | Medida de diseño y forma de comprobarla |
| --- | --- |
| Alta afluencia y selección del equipo equivocado | Priorizar búsqueda por RUT y selección explícita de equipo. Ensayar en la primera revisión una recepción con varias órdenes y medir el tiempo por atención. Acordar el umbral con recepción antes del piloto. |
| Exposición de datos personales | Usar datos ficticios en GitHub, capturas y demostraciones. Acordar campos mínimos y permisos por rol. Verificar en el sistema implementado que el acceso directo al historial también se restrinja al Administrador/Docente. |
| Disputa por una falla preexistente o posterior | Registrar la verificación inicial antes del checklist y comparar ambos resultados en la misma orden. Revisar con el técnico un caso en que el equipo cambia de condición y acordar el procedimiento de escalamiento. |

Fuente del marco de trabajo. [Schwaber y Sutherland, Guía Scrum (2020)](https://scrumguides.org/scrum-guide.html)

## 2.1.3 Levantamiento y validación con el cliente

El informe declara una entrevista con el docente Pablo Pesce el 2 de octubre de 2026 sobre inscripción QR, recepción, checklist, observaciones y cierre. Esa declaración permite identificar fecha, participante y temas. El acta, las respuestas y los acuerdos específicos están pendientes de respaldo.

Se propone como segunda técnica un taller de co-diseño. El encargado de la actividad recorre la recepción de dos equipos registrados al mismo RUT y decide qué datos necesita para distinguirlos. Un técnico recorre una orden con una falla inicial y una diferencia posterior. El docente revisa el criterio para autorizar la entrega y el cierre. Para cada escenario se registra si el requisito se acepta, requiere cambios o queda pendiente, y se adjunta evidencia autorizada por los participantes.

| ID | Criterio de aceptación propuesto | Escenario de revisión |
| --- | --- | --- |
| RF-01 | La inscripción confirma los dispositivos ingresados por el propietario. | Inscribir dos equipos con datos ficticios. |
| RF-02 | La recepción identifica al propietario por RUT y guarda los datos técnicos en la orden del dispositivo seleccionado. | Buscar el RUT de prueba y recibir solo el segundo equipo. |
| RF-03 | Antes de iniciar el checklist se registra el resultado de la demostración inicial. | Registrar que el equipo enciende y que el ventilador presenta ruido. |
| RF-04 | La orden muestra el checklist correspondiente al servicio elegido. | Cambiar entre mantención física, lógica y formateo y revisar con el docente las tareas de cada uno. El mockup muestra el ejemplo físico. |
| RF-05 | Cada observación queda asociada a una orden. | Registrar polvo en la rejilla y comprobar que la observación corresponde al dispositivo atendido. |
| RF-06 | La verificación posterior permite contrastar su resultado con la condición inicial y registrar diferencias. | Simular una pantalla que deja de funcionar y acordar el procedimiento previo a la entrega. |
| RF-07 | La orden distingue un intento sin respuesta de un retiro acordado. | Registrar una llamada sin respuesta y luego un acuerdo de retiro. |
| RF-08 | Se registra el resultado de la prueba conjunta y cualquier observación del propietario. | Realizar el recorrido de retiro con un resultado con observaciones. |
| RF-09 | El cierre registra la entrega, un estado final y la referencia a la prueba conjunta. | Revisar una orden lista para cierre y otra cuya prueba conjunta sigue pendiente. |

### Registro de validación

| ID | Fecha y participantes | Técnica | Requisitos y versión revisada | Acuerdo o cambio | Evidencia | Estado |
| --- | --- | --- | --- | --- | --- | --- |
| VAL-01 | 02/10/2026 · Pablo Pesce, docente, según el informe | Entrevista | Temas vinculados a RF-01, RF-02, RF-04, RF-05 y RF-09 | Pendiente de recuperar del registro original | Sección de co-creación del informe | Entrevista declarada, acuerdos pendientes de respaldo |
| VAL-02 | Por coordinar con docente y representantes de recepción y soporte técnico | Taller de co-diseño | RF-01 a RF-09 · registrar el commit usado | Completar durante la sesión | Acta o minuta confirmada y capturas con datos ficticios | Pendiente |

Registrar una fila por decisión si la sesión produce varios acuerdos. Cada cambio debe vincularse al requisito afectado, a la persona responsable y al commit de la modificación. Si cambia un rol o una transición, revisar su consistencia en los diagramas de casos de uso, clases y secuencia. Recepcionista es la función operativa de recepción en la pauta. El informe asigna esa función a Administrador/Docente y Estudiante/Técnico. Confirmar esta asignación en el taller y actualizar pantallas y diagramas según el acuerdo.

## 2.1.4 Aplicación de prácticas de calidad

La versión original cita ISO/IEC/IEEE 12207:2017. ISO registra esa edición como retirada y publica la edición 2026. Este anexo toma la edición 2026 como referencia para proponer prácticas de gestión del ciclo de vida, con evidencia acotada a la fase de diseño. [Ficha oficial de 2017](https://www.iso.org/standard/63712.html) · [Ficha oficial de 2026](https://www.iso.org/standard/90219.html)

| Práctica de proceso | Aplicación en la Clínica del PC | Evidencia y momento en Scrum |
| --- | --- | --- |
| Definición de necesidades y requisitos | Transformar cada paso de la guía en un requisito identificable y un criterio observable. Registrar fuente y decisión para los cambios. | Matriz RF-01 a RF-09 incorporada al Product Backlog y revisada al refinarlo. |
| Gestión de configuración | Versionar mockups y decisiones en Git. Vincular el commit revisado y el commit que responde al acuerdo del cliente. | Registro de validación, historial de Git y backlog actualizado después de Sprint Review. |
| Verificación | Revisar consistencia entre requisitos, pantallas y UML. Durante implementación, ejecutar pruebas para criterios como el bloqueo del cierre si falta la prueba conjunta. | Lista de comprobación durante el Sprint, con versión, resultado esperado y resultado observado. |
| Validación | Pedir a la contraparte que evalúe si el recorrido responde a la operación real. Registrar participante, fecha, escenario, decisión y evidencia. | Acta de taller o Sprint Review y seguimiento del acuerdo en el Product Backlog. |

Para dar por terminada una actualización de diseño, el equipo debe revisar la coherencia con la matriz y los diagramas, guardar la versión y dejar visibles las decisiones pendientes. En implementación, la Definition of Done debe añadir pruebas ejecutadas para el incremento y evidencia de los resultados. Scrum proporciona la cadencia para inspeccionar y ajustar el producto. Las prácticas de calidad proporcionan los registros necesarios para reconstruir qué requisito cambió, con qué evidencia y en qué versión.
