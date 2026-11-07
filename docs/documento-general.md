# LinguIA — Documento general

**Versión:** 0.1  
**Fecha:** 7 de noviembre de 2026  
**Estado:** base evolutiva de requisitos y decisiones; implementación no iniciada.

Este documento guía el desarrollo desde la creación del repositorio. Reúne los acuerdos disponibles y distingue requisitos aprobados, recomendaciones y decisiones pendientes. No constituye una especificación técnica cerrada. Los cambios posteriores deberán actualizar su contenido y registrar su motivo.

## 1. Propósito y visión

Democratizar el aprendizaje de idiomas mediante una plataforma educativa con tutor personalizado de IA, planificación adaptable y memoria pedagógica persistente.

El valor central es el ciclo diagnóstico → planificación → práctica → evaluación → detección de dificultades → repaso → adaptación. La plataforma debe conservar la continuidad entre sesiones y explicar las recomendaciones a partir de evidencias.

El antecedente es una experiencia privada de seguimiento del aprendizaje. LinguIA será un proyecto generalizable; no se asume que el código, almacenamiento o despliegue del antecedente hayan sido migrados ni auditados.

## 2. Alcance y principios aprobados

| Aspecto | Acuerdo |
| --- | --- |
| Idiomas | Inglés primero; arquitectura extensible a otros idiomas. |
| Referencia de niveles | MCER A1–C2, con estimaciones sustentadas y limitaciones visibles. |
| Inicio educativo | Evaluación diagnóstica obligatoria antes del roadmap personalizado. |
| Desarrollo | Incrementos funcionales completos e integración progresiva de IA. |
| Diseño | Modularidad, POO, encapsulamiento, abstracción, composición y responsabilidades separadas. |
| Lenguajes | Los necesarios, justificando cada incorporación. |
| Repositorio | Un único repositorio principal para todo el proyecto. |
| Economía | Presupuesto inicial del fundador de $0; prioridad a una plataforma gratuita. |
| Apertura | Objetivo open source; licencia pendiente. |
| Uso inicial | Prototipo de uso individual administrativo, sin registro abierto de estudiantes. |
| Evolución | Plataforma autónoma e integraciones posteriores con asistentes externos. |
| Acceso a IA | Admitir credenciales gestionadas por LinguIA y credenciales propias del estudiante. |

La publicación del repositorio no equivale al despliegue de una aplicación ni determina quién podrá acceder a sus datos.

## 3. Recorrido del estudiante

1. Configurar idioma nativo, idioma objetivo, objetivos, disponibilidad, intereses y preferencias.
2. Completar la evaluación diagnóstica.
3. Recibir un informe con resultados por habilidad, niveles estimados, evidencias, fortalezas, dificultades y límites de la evaluación.
4. Recibir un roadmap personalizado y revisable.
5. Realizar clases completas, con actividades y retroalimentación.
6. Consultar progreso, historial, errores y repasos desde el dashboard.
7. Revisar periódicamente el plan según nuevas evidencias.

**El diagnóstico es la primera prioridad funcional.** La discusión de una clase de referencia no lo sustituye ni autoriza saltarlo en el recorrido educativo.

Los resultados externos podrán estudiarse como evidencia complementaria. Su importación no se considera una excepción aprobada al diagnóstico obligatorio.

## 4. Evaluación diagnóstica

### 4.1 Objetivo

Estimar el punto de partida para planificar el aprendizaje, reconociendo que las habilidades pueden tener niveles diferentes.

### 4.2 Alcance requerido

- Comprensión lectora y auditiva.
- Producción escrita y oral.
- Gramática y vocabulario como dimensiones complementarias.
- Dificultad y duración adaptables.
- Instrucciones, criterios y evidencias identificables.
- Informe comprensible y útil para elaborar el roadmap.

Las seis dimensiones no se tratarán como seis escalas oficiales equivalentes del MCER. La correspondencia y ponderación deberán definirse y validarse.

### 4.3 Calidad y estados

Distinguir respuesta correcta, incorrecta, ambigua y no evaluada. Una actividad pendiente de evaluación no equivale a una puntuación de cero.

Las preguntas objetivas deberán tener respuestas y lógica verificadas. La evaluación abierta utilizará rúbricas y conservará evidencia suficiente para revisar el resultado. La incertidumbre deberá comunicarse y las correcciones deberán poder impugnarse.

Un porcentaje de aciertos no se convierte automáticamente en un nivel MCER. No se afirmará certificación oficial ni equivalencia con pruebas externas sin validación.

### 4.4 Pendiente de diseñar

Banco de preguntas, rúbricas, adaptación, duración, muestreo de habilidades, tratamiento de audio, reglas de finalización y procedimiento de validación. No existen aún umbrales aprobados.

## 5. Roadmap y experiencia educativa

El roadmap debe partir del diagnóstico, objetivos y disponibilidad; mostrar prioridades y evolucionar con evidencias. La planificación no impondrá la misma duración o secuencia a todos los estudiantes.

Las clases completas y el dashboard son dos hitos principales relacionados, posteriores a la base diagnóstica y de planificación.

Una clase completa contempla objetivos, materiales, actividades, respuestas, evaluación, retroalimentación, cierre y persistencia. Debe poder interrumpirse y reanudarse. La clase de referencia permitirá comprobar reading, listening, writing, speaking, grammar y vocabulary; no obliga a incluir todas las dimensiones en cada clase futura.

El sistema deberá ofrecer práctica guiada y producción independiente, variedad de actividades, seguimiento de errores, vocabulario contextual y repaso espaciado. Las preferencias de idioma de las explicaciones y momento de las correcciones serán configurables.

El avance podrá incluir refuerzo y advertencias sustentadas en dificultades detectadas. Las reglas concretas de avance y dominio permanecen pendientes.

## 6. Dashboard y progreso

El dashboard consulta los registros pedagógicos compartidos. Mostrará resultados reales, sesiones, actividades, historial, evidencias y próximos objetivos.

- Separar actividad realizada, rendimiento observado y dominio estimado.
- Diferenciar evaluaciones pendientes, experimentales y validadas.
- Conservar intentos sucesivos sin sobrescribir los anteriores.
- Distinguir tiempo medido de tiempo declarado cuando se incorpore esa métrica.
- No inventar puntuaciones, progreso ni equivalencias de nivel.
- Evitar que la interfaz cambie por su cuenta las reglas de dominio.

La definición exacta de indicadores y visualizaciones sigue pendiente.

## 7. Tutor e integración progresiva de IA

La IA se incorporará desde etapas tempranas de forma incremental. La plataforma tendrá funcionalidades utilizables y pruebas aisladas de integración, sin supeditar todo el desarrollo a un proveedor.

Capacidades previstas: explicar, conversar, generar o adaptar actividades, evaluar respuestas abiertas, detectar patrones, recomendar repasos y ajustar la planificación.

Las salidas experimentales no modificarán automáticamente el nivel o las competencias hasta que el evaluador correspondiente haya sido validado. Se conservará la procedencia de los resultados.

### 7.1 Proveedores, modelos y credenciales

Separar:
- **Proveedor:** servicio o sistema que ofrece capacidades.
- **Modelo:** implementación concreta de una capacidad.
- **Credencial:** autorización para utilizarla.

La selección deberá respetar autorizaciones, compatibilidad, calidad y límites de consumo. Ante cuota agotada, utilizar únicamente alternativas autorizadas; si no existen, informar de la limitación.

Una suscripción a una interfaz de chat no implica acceso gratuito a su API. Las claves propias pueden generar costes: deberán contemplarse límites y visibilidad del consumo.

Proveedores, modelos, mecanismos de selección y cuotas están pendientes de evaluación. No se asume disponibilidad ilimitada ni calidad pedagógica validada.

### 7.2 Autonomía e integraciones

LinguIA deberá funcionar como plataforma autónoma. Las integraciones con asistentes externos forman parte de la evolución prevista y deberán compartir contratos claros. El núcleo pedagógico y el progreso permanecerán centralizados, evitando fuentes contradictorias.

El desarrollo de un agente propio es una posibilidad futura, no una capacidad implementada.

## 8. Memoria pedagógica y privacidad

Conservar informes, evaluaciones, evidencias pertinentes, patrones de error, vocabulario, repasos y versiones del roadmap. El historial conversacional completo será opcional, con minimización de datos.

El estudiante deberá poder consultar, corregir, exportar y eliminar sus datos, incluido el borrado selectivo. Definir retención y consentimiento antes de almacenar información real.

En la evolución multiusuario, aislar los datos por estudiante. Las transferencias a proveedores deben respetar permisos y restricciones. El acceso administrativo inicial no sustituye los controles de autorización.

No publicar datos personales, grabaciones, conversaciones, claves ni registros privados en Git, ejemplos o logs. Los ejemplos serán sintéticos. La fuente de contexto histórica no se copiará al repositorio porque contiene información privada.

## 9. Arquitectura conceptual

### 9.1 Responsabilidades

| Área | Responsabilidad |
| --- | --- |
| Interfaz | Presentar diagnóstico, aula, roadmap y dashboard. |
| Aplicación | Coordinar casos de uso, sesiones y permisos. |
| Dominio pedagógico | Reglas de actividades, evaluación, evidencias y progreso. |
| Persistencia | Guardar y recuperar registros sin acoplar el dominio a un servicio. |
| IA y audio | Adaptadores para proveedores y procesamiento especializado. |
| Integraciones | Intercambio controlado con herramientas externas. |

Esta separación no implica servidores o microservicios distintos.

### 9.2 Programación orientada a objetos

Aplicar encapsulamiento, abstracción, polimorfismo, composición y principios SOLID donde aporten claridad. La herencia requerirá una relación conceptual válida. Las funciones puras son apropiadas para cálculos y transformaciones.

Conceptos candidatos: perfil de estudiante, diagnóstico, actividad, intento, evaluación, evidencia, roadmap, clase, sesión y repaso. No constituyen todavía un esquema definitivo de clases o tablas.

El núcleo no dependerá directamente de un proveedor de IA o base de datos. Evaluadores y repositorios deberán poder sustituirse mediante contratos. El dashboard consumirá el mismo registro que el aula.

### 9.3 Tecnologías candidatas, no seleccionadas

TypeScript para web, Python para experimentación científica y audio, SQL para datos; frameworks, motor de persistencia y herramientas pendientes. No se crearán servicios separados sin necesidad demostrada.

GitHub es el repositorio aprobado. Vercel y Netlify son candidatos para visualizar avances; Supabase y otras opciones deben evaluarse. No hay alojamiento ni base de datos aprobados o desplegados.

## 10. Audio y procesamiento de señales

Explorar Python, filtrado, análisis espectral, STFT, energía y detección de voz. El muestreo se diseñará considerando Nyquist-Shannon. Laplace puede apoyar análisis de sistemas continuos; el audio digital requerirá herramientas discretas.

Limpiar o caracterizar una señal no equivale a reconocer palabras o evaluar pronunciación. Estas capacidades necesitan métodos y validaciones adicionales.

Un proceso Python local no queda disponible automáticamente para una web alojada. La comunicación, ubicación, recursos y latencia se decidirán cuando exista un caso de uso concreto.

## 11. Repositorio, documentación y calidad

El monorepositorio reúne código, documentación, pruebas y automatización. La estructura exacta de módulos se definirá al seleccionar las primeras herramientas.

- README: presentación y estado verificable.
- Documento general: visión, requisitos y decisiones.
- Roadmap: trabajo previsto y criterios de aceptación.
- ADR: registros de decisiones arquitectónicas cuando se adopten.
- Guías, changelog y automatización: incorporar según las necesidades.

Cada incremento debe vincular el objetivo educativo con implementación, evidencia de validación y actualización documental. Los cambios de requisitos deben conservar su justificación en el historial.

Comprobar reglas pedagógicas, persistencia e integración con pruebas proporcionales al cambio. Para preguntas objetivas, verificar respuestas antes de publicarlas. Para IA, definir casos de referencia y criterios de aceptación antes de conceder autoridad a sus evaluaciones.

## 12. Decisiones pendientes

| Decisión | Situación |
| --- | --- |
| Framework y herramientas del monorepo | Sin seleccionar. |
| Datos, alojamiento y acceso administrativo | Requieren evaluación técnica. |
| Instrumento diagnóstico y correspondencia MCER | Requieren diseño y validación. |
| Modelos, voz y límites de consumo | Requieren pruebas y revisión de condiciones vigentes. |
| Licencia y gobernanza open source | Pendientes; no se añade una licencia por defecto. |
| Autenticación y evolución multiusuario | Pendientes de diseño. |
| Retención, consentimiento e intercambio externo | Pendientes de concretar antes de usar datos reales. |
| Ramas, CI y despliegues | Pendientes de organizar. |

## 13. Estado verificable y siguiente paso

Existe el repositorio principal y se incorpora esta documentación inicial. No se ha implementado aplicación, diagnóstico, base de datos, dashboard ni tutor.

Siguiente trabajo: especificar el primer incremento de diagnóstico y seleccionar las herramientas mínimas para construirlo. Las clases completas y su dashboard permanecen en el alcance, con el diagnóstico como entrada educativa obligatoria.

## 14. Registro de cambios

- **0.1 — 2026-11-07:** consolidación inicial; prioridad explícita al diagnóstico; acuerdos separados de candidatos y decisiones pendientes; sin datos privados ni implementación.
