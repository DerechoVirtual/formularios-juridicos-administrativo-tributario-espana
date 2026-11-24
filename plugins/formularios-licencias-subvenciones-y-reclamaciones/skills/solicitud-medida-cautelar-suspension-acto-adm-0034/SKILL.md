---
name: solicitud-medida-cautelar-suspension-acto-adm-0034
description: "Solicitud de medida cautelar de suspensión del acto administrativo recurrido. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de medida cautelar de suspensión del acto administrativo recurrido

> Formulario **ADM-0034** del plugin **Licencias, subvenciones y reclamaciones ante la Administración** (`formularios-licencias-subvenciones-y-reclamaciones`) · Administrativo y Tributario › Administrativo general (licencias, subvenciones, autoridades de control) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de medida cautelar de suspensión del acto administrativo recurrido» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de medida cautelar de suspensión del acto administrativo recurrido” para mi caso». También puedes invocarla directamente con `/formularios-licencias-subvenciones-y-reclamaciones:solicitud-medida-cautelar-suspension-acto-adm-0034`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-licencias-subvenciones-y-reclamaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Licencias, subvenciones y reclamaciones ante la Administración) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DESCRIBIR
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 1214 Código Civil

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

- Ninguna.

### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero el «Texto del formulario» (al final de este fichero) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea del «Texto del formulario» y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Texto del formulario

Lo que sigue, hasta el final de este fichero, es el formulario tal cual: desde su primera línea hasta la firma.

P. Ordinario [Nº DE PROCEDIMIENTO]

AL TRIBUNAL CENTRAL DE INSTANCIA (SECCIÓN DE LO CONTENCIOSO-ADMINISTRATIVO) N.º [NÚMERO].

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], según tengo debidamente acreditado en el procedimiento referenciado, ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que mediante el presente escrito y en aplicación del artículo 129.1 de la Ley reguladora de la Jurisdicción Contencioso-Administrativa, solicito que se abra pieza separada de suspensión de la ejecución del acto recurrido con base en las siguientes

ALEGACIONES

La resolución sancionadora acuerda imponer una multa de [IMPORTE] euros y la suspensión durante [Nº] meses de la licencia de [ACTIVIDAD].

La ejecución del acto recurrido haría ineficaz el posible resultado estimatorio del recurso interpuesto y causaría, por tanto, perjuicios de imposible reparación a mi representado al privarle de la posibilidad de utilizar vehículos durante el tiempo indicado, con el consiguiente menoscabo de su actividad laboral para cuya práctica necesita este medio de locomoción, según se acredita con el documento número [Nº DE DOCUMENTO] que adjuntamos.

A esto hay que añadir que la unidad familiar que encabeza depende económicamente de los recursos que se procura con este medio de trabajo (documentos [Nº DE DOCUMENTO]).

El auto del Tribunal Supremo de 12 de junio de 1995 establece en su segundo fundamento jurídico que: “Es jurisprudencia consolidada de este Tribunal, y concretamente de la Sala que enjuicia la cuestión suscitada, que constituye un bloque de doctrina reiterada y constante (Autos de 23 de septiembre de 1993 y 14 de enero y 24 de marzo de 1994, entre otros) la que viene considerando que la suspensión del acto o disposición general es factible concederse por el Tribunal a instancia de actor, según facultad atribuida por la Ley de la Jurisdicción (de 27 de diciembre de 1956) en su artículo 122.1. Sin embargo, esta concesión tan sólo puede ser otorgada cuando la ejecución hubiese de producir daños o perjuicios de reparación imposible o difícil, circunstancia esta que ha de acreditar suficientemente al instante de la suspensión, conforme a las reglas de la carga de la prueba que se recogen en el artículo 1214 del Código Civil (hoy la referencia debería entenderse hecha al artículo 217 de la Ley de Enjuiciamiento Civil), facilitando al Tribunal, siquiera sea indiciariamente con un principio de prueba, los elementos, fundamentos y circunstancias de los que se deriven los perjuicios que se dicen de imposible o difícil reparación para que el Tribunal, valorándolos en su conjunto, pueda hacer uso de la expresada facultad suspensiva”.

Aunque la referida resolución se refiere a disposiciones generales entendemos que también es aplicable en actos administrativos. La Jurisprudencia exige únicamente un principio de prueba que acredite la dificultad de la reparación posterior de los perjuicios que produzca la ejecución de la resolución recurrida, para que el Tribunal pueda optar por la suspensión. En este caso la más que posible nulidad de la actuación administrativa unida a la acreditada necesidad del uso del vehículo por mi representado, cuya privación motivaría probablemente la cesación de su actividad laboral, deben determinar una resolución favorable a la petición que en este momento se formula, ya que de ninguna manera podría repararse varios años después la pérdida de un trabajo.

De entenderse finalmente que la sanción fue impuesta incorrectamente, nos encontraríamos ante la imposibilidad para la Administración de reparación del perjuicio ocasionado.

Respecto a la sanción pecuniaria [IMPORTE] (se consigna la cantidad fijada como multa de [IMPORTE] euros, o igualmente su pago en estos momentos, a pesar de la interposición del recurso, equivale a la ejecución del acto, desvirtuando así la relevancia y prevalencia de que goza toda resolución judicial sobre cualquiera administrativa. En nada perjudica a la Administración, ni se obstaculiza la efectividad de la Justicia, el esperar a la firmeza de la sentencia para, en su caso, proceder a lo que en definitiva es su ejecución. Abonar la cantidad en este momento supone dar por sentado que la Administración es infalible y, en definitiva, priva de razón de ser a la vía judicial). Por este motivo solicitamos también que se requiera a la Administración para que suspenda la vía ejecutiva.

Como argumento final hemos de añadir que el procedimiento administrativo está viciado de nulidad insubsanable al haberse prescindido de los trámites que aseguran la audiencia y presentación de pruebas a mi representado. No entramos al fondo del asunto, pero nos remitimos a efectos probatorios al expediente administrativo (folios n.º [NÚMERO] a [Nº]). En el mismo cabe apreciar que son ciertas estas manifestaciones y que no se ha practicado ninguna notificación a D. a lo largo de todo el procedimiento, salvo la resolución final. A efectos acreditativos de lo aquí manifestado adjuntamos los documentos [Nº DE DOCUMENTO] relativos a [DESCRIBIR].

Este motivo debe ser también causa de suspensión.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito, lo admita y acuerde abrir pieza separada de medidas cautelares a fin de que en su día, previos los trámites legales oportunos, acuerde la suspensión de la ejecución en vía administrativa del acto recurrido.

Es justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

========================================================================
