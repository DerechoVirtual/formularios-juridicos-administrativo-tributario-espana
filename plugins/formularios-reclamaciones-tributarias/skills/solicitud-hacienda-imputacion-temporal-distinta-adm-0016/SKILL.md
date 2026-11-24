---
name: solicitud-hacienda-imputacion-temporal-distinta-adm-0016
description: "Solicitud a Hacienda de imputación temporal distinta del devengo en el Impuesto sobre Sociedades. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud a Hacienda de imputación temporal distinta del devengo en el Impuesto sobre Sociedades

> Formulario **ADM-0016** del plugin **Reclamaciones tributarias y económico-administrativas** (`formularios-reclamaciones-tributarias`) · Administrativo y Tributario › Tributario y económico-administrativo · normativa revisada el 24-11-2026.

## Qué es

Solicitud de aplicación de un criterio de imputación temporal de ingresos y gastos distintos del devengo para el IS. Debe presentarse, al menos, seis meses antes de la conclusión del primer período impositivo respecto del que pretende tener efectos. El contribuyente puede desistir de la solicitud formulada.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud a Hacienda de imputación temporal distinta del devengo en el Impuesto sobre Sociedades» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud a Hacienda de imputación temporal distinta del devengo en el Impuesto sobre Sociedades” para mi caso». También puedes invocarla directamente con `/formularios-reclamaciones-tributarias:solicitud-hacienda-imputacion-temporal-distinta-adm-0016`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamaciones-tributarias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Reclamaciones tributarias y económico-administrativas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] ACTIVIDAD
- [ ] CRITERIO DE IMPUTACIÓN TEMPORAL
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIBIR
- [ ] DOMICILIO
- [ ] DOMICILIO A EFECTOS DE NOTIFICACIONES
- [ ] EJERCICIO
- [ ] FECHA
- [ ] INCIDENCIA FISCAL DEL CRITERIO
- [ ] INFLUENCIA EN EL PATRIMONIO Y RESULTADOS
- [ ] INGRESOS Y GASTOS AFECTADOS
- [ ] LUGAR
- [ ] NATURALEZA E IMPORTANCIA
- [ ] Nº DE EPÍGRAFE

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

Solicitud de aplicación de un criterio de imputación temporal de ingresos y gastos distintos del devengo para el IS. Debe presentarse, al menos, seis meses antes de la conclusión del primer período impositivo respecto del que pretende tener efectos. El contribuyente puede desistir de la solicitud formulada.


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

DEPARTAMENTO DE INSPECCIÓN FINANCIERA Y TRIBUTARIA DE LA DELEGACIÓN DEDE LA AGENCIA ESTATAL DE ADMINISTRACIÓN TRIBUTARIA

D./Dña. [NOMBRE Y APELLIDOS] con N.I.F. y domicilio a efectos de notificaciones en [DOMICILIO A EFECTOS DE NOTIFICACIONES], actuando como representante de la Entidad [DENOMINACIÓN SOCIAL], con N.I.F. y domiciliada en [DOMICILIO], según acredito con el documento que acompaño:

EXPONE

1º Que mi representada realiza la actividad económica de [ACTIVIDAD], figurando en el IAE mediante alta en el epígrafe [Nº DE EPÍGRAFE].

2º Que el artículo 1 del Reglamento del Impuesto sobre Sociedades vigente dispone que las entidades que utilicen, a efectos contables, un criterio de imputación temporal de ingresos y gastos diferente al del devengo, podrán presentar una solicitud ante la Administración Tributaria para que el referido criterio tenga eficacia fiscal.

3º Que en base al citado precepto solicita que se apruebe la utilización de un criterio de imputación distinto al del devengo, a cuyo efecto manifiesta lo siguiente:

a) Los ingresos y gastos a los que afecta el criterio de imputación temporal son [INGRESOS Y GASTOS AFECTADOS], y se hace constar que su naturaleza e importancia en el conjunto de las operaciones del sujeto pasivo es de [NATURALEZA E IMPORTANCIA].
b) El criterio de imputación temporal cuya eficacia fiscal se solicita es el de [CRITERIO DE IMPUTACIÓN TEMPORAL]. Este criterio

no es de obligado cumplimiento

sí es de obligado cumplimiento, siendo la norma contable que establece tal obligación.
c) En todo caso, el criterio de imputación temporal propuesto es el más adecuado a la imagen fiel que deben proporcionar las cuentas anuales por los siguientes motivos [DESCRIBIR]. Y su influencia sobre el patrimonio, la situación financiera y los resultados de la Empresa es la siguiente: [INFLUENCIA EN EL PATRIMONIO Y RESULTADOS].
d) La incidencia, a efectos fiscales del criterio de imputación temporal es ésta: [INCIDENCIA FISCAL DEL CRITERIO].

4º Que desea utilizar el citado criterio de imputación temporal para el ejercicio [EJERCICIO] y siguientes, presentándose esta solicitud con más de seis meses de antelación a la conclusión del primer período impositivo respecto del que se pretende que tenga efectos.

5º Que tal como establece la normativa vigente, considero que transcurridos seis meses desde la fecha de presentación de esta solicitud sin haberse producido una resolución expresa, se entenderá aprobado el criterio de imputación temporal de ingresos y gastos utilizado por mi representada.

Por todo ello,

SOLICITO

Tenga por presentado este escrito con los documentos acompañados y acuerde la aprobación del criterio alternativo de imputación de ingresos y gastos que se propone, por acomodarse mejor al funcionamiento de la empresa.

En [LUGAR], a [FECHA].

Fdo.:

D./Dña. [NOMBRE Y APELLIDOS]:
