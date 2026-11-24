---
name: recurso-reposicion-contra-actas-inspeccion-conformidad-adm-0021
description: "Recurso de reposición contra actas de inspección con conformidad (A01). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de reposición contra actas de inspección con conformidad (A01)

> Formulario **ADM-0021** del plugin **Reclamaciones tributarias y económico-administrativas** (`formularios-reclamaciones-tributarias`) · Administrativo y Tributario › Tributario y económico-administrativo · normativa revisada el 24-11-2026.

## Qué es

Escrito de recurso de reposición contra actas de conformidad que se indican en el escrito y solicitud de adopción de acuerdo según las pretensiones alegadas. Si se solicita la suspensión del acto impugnado deberá garantizar el ingreso de las cantidades de dicho acto.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de reposición contra actas de inspección con conformidad (A01)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de reposición contra actas de inspección con conformidad (A01)” para mi caso». También puedes invocarla directamente con `/formularios-reclamaciones-tributarias:recurso-reposicion-contra-actas-inspeccion-conformidad-adm-0021`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamaciones-tributarias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Reclamaciones tributarias y económico-administrativas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (3 veces)
- [ ] DIRECCIÓN (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] LUGAR
- [ ] NIF
- [ ] NOMBRE DEL REPRESENTADO/A

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

Escrito de recurso de reposición contra actas de conformidad que se indican en el escrito y solicitud de adopción de acuerdo según las pretensiones alegadas. Si se solicita la suspensión del acto impugnado deberá garantizar el ingreso de las cantidades de dicho acto.

Notas al pie del formulario original:
(1) - Características. Es un recurso potestativo. Deberá interponerse ante el órgano que dictó el acto y con carácter previo a cualquier recurso o reclamación. Si se presenta, no puede interponerse reclamación económico-administrativa hasta que el recurso se haya resuelto de forma expresa o hasta que pueda considerarlo desestimado por silencio administrativo.

- Plazo. El plazo para presentar el recurso es de un mes a partir del día siguiente al que se entiende producida la notificación del acta, que es un mes desde la fecha de la firma.

- Suspensión y garantías. Las garantías han de cubrir la el importe de dicho acto, los intereses de demora que genere la suspensión y los recargos que pudieran proceder en el momento de la solicitud de la suspensión. Si la causa del recurso es un error aritmético, material o de hecho no se precisa aportar garantía para la suspensión.

- Plazo de resolución. El recurso se ha de resolver en el plazo de un mes. Transcurrido dicho plazo sin haberse resuelto, se entenderá desestimado a los efectos de interponer la reclamación procedente.


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

AL JEFE DE LA

DEPENDENCIA REGIONAL DE INSPECCIÓN DE [LOCALIDAD]

OFICINA NACIONAL DE INSPECCIÓN

D./Dña. [NOMBRE Y APELLIDOS], con N.I.F. [NIF], con domicilio fiscal en [DIRECCIÓN], [LOCALIDAD] y domicilio a efecto de notificaciones en [DIRECCIÓN], [LOCALIDAD] actuando en

nombre propio

representación de [NOMBRE DEL REPRESENTADO/A]

EXPONE

Que en fecha [FECHA] se han levantado actas de conformidad por los conceptos y períodos siguientes:

Número de referencia	Concepto impositivo	Períodos

Que no estando conforme con dichas actas, por medio del presente escrito y de conformidad con los artículos 222 a 225 de la Ley General Tributaria, por el que se reglamenta el recurso de reposición previo al económico-administrativo, interpongo RECURSO DE REPOSICIÓN ante el mismo órgano autor del acto impugnado, en base a las siguientes

ALEGACIONES

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Por todo lo expuesto,

SOLICITA

Que se tenga por presentado RECURSO DE REPOSICIÓN contra las actas indicadas y se adopte acuerdo con las pretensiones alegadas, haciéndose constar que dichas actas no han sido impugnadas en vía económico-administrativa.

Si se solicita la suspensión del acto impugnado:

Al mismo tiempo, al amparo de lo dispuesto en el artículo 224, se solicita la suspensión del acto impugnado, a cuyo efecto se garantiza el ingreso de las cantidades a que se refiere el apartado 1 de dicho artículo ofreciendo la garantía

a) Depósito de dinero o valores públicos.

b) Aval o fianza de carácter solidario de entidad de crédito o sociedad de garantía recíproca o certificado de seguro de caución.

c) Fianza personal y solidaria de otros contribuyentes de reconocida solvencia que al presente escrito se acompaña.

En [LUGAR], a [FECHA].

Fdo.:

D./Dña. [NOMBRE Y APELLIDOS]
