---
name: recurso-reposicion-contra-denegacion-reagrupacion-adm-0048
description: "Recurso de reposición contra la denegación de reagrupación familiar de ciudadanos no comunitarios. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de reposición contra la denegación de reagrupación familiar de ciudadanos no comunitarios

> Formulario **ADM-0048** del plugin **Licencias, subvenciones y reclamaciones ante la Administración** (`formularios-licencias-subvenciones-y-reclamaciones`) · Administrativo y Tributario › Administrativo general (licencias, subvenciones, autoridades de control) · normativa revisada el 24-11-2026.

## Qué es

Recurso potestativo de reposición contra la resolución de la Delegación del Gobierno (o Subdelegación) que deniega la autorización de residencia temporal por reagrupación familiar solicitada por un extranjero residente legal respecto de su cónyuge e hijos, por considerar insuficientes los medios económicos o inadecuada la vivienda.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de reposición contra la denegación de reagrupación familiar de ciudadanos no comunitarios» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de reposición contra la denegación de reagrupación familiar de ciudadanos no comunitarios” para mi caso». También puedes invocarla directamente con `/formularios-licencias-subvenciones-y-reclamaciones:recurso-reposicion-contra-denegacion-reagrupacion-adm-0048`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-licencias-subvenciones-y-reclamaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Licencias, subvenciones y reclamaciones ante la Administración) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] AÑO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº (2 veces)
- [ ] COMUNIDAD AUTÓNOMA O PROVINCIA
- [ ] DOMICILIO
- [ ] DÍA
- [ ] EDADES
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] MES
- [ ] NIE
- [ ] NOMBRE Y APELLIDOS DE LOS FAMILIARES
- [ ] Nº DE EXPEDIENTE
- [ ] ORGANISMO QUE EMITE EL INFORME
- [ ] SUPERFICIE
- [ ] TELÉFONO O CORREO ELECTRÓNICO

## Normas que cita el formulario

- art. 112.1 Ley 39/2015
- art. 17 Ley Orgánica 4/2000

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…rts. 54 y 55 del Reglamento aprobado por Real Decreto 557/2011, de 20 de abril).»: el Real Decreto 557/2011 ha sido sustituido por el nuevo Reglamento de Extranjería aprobado por Real Decreto 1155/2024, de 19 de noviembre; comprobar los artículos equivalentes sobre reagrupación familiar, medios económicos y vivienda adecuada y su régimen transitorio, y citar los que correspondan en cada caso.

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

A LA DELEGACIÓN DEL GOBIERNO EN [COMUNIDAD AUTÓNOMA O PROVINCIA]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con NIE [NIE], con domicilio a efectos de notificaciones sito en [DOMICILIO], y con teléfono / correo electrónico [TELÉFONO O CORREO ELECTRÓNICO], en el expediente n.º [Nº DE EXPEDIENTE] que se sigue a mis instancias por solicitud de residencia temporal por reagrupación familiar, comparece y, como mejor proceda, DICE:

Que en fecha [FECHA] he sido notificado de la resolución de la Delegación a la que me dirijo, de fecha [FECHA], por la que se denegaba la autorización de residencia temporal por reagrupación familiar solicitada por quien suscribe en relación con su [esposa/esposo] e hijos [NOMBRE Y APELLIDOS DE LOS FAMILIARES], y, de conformidad con lo prevenido en el art. 112.1 de la Ley 39/2015, de 1 de octubre, por medio del presente escrito interpongo RECURSO DE REPOSICIÓN en base a los siguientes

MOTIVOS

PRIMERO.– Infracción de los artículos 17 y 18 de la Ley Orgánica 4/2000, de 11 de enero, sobre derechos y libertades de los extranjeros en España y su integración social (Ley de Extranjería), en relación con los preceptos del Reglamento de Extranjería que regulan los medios económicos y la vivienda adecuada para la reagrupación familiar (arts. 54 y 55 del Reglamento aprobado por Real Decreto 557/2011, de 20 de abril).

Tal como consta en el expediente, el que suscribe está en situación de residencia legal, habiendo obtenido la renovación de la autorización de residencia inicial, por lo que tiene el derecho a reagrupar a su cónyuge e hijos menores de edad, habiendo acreditado el parentesco con la documentación presentada con la solicitud.

La resolución impugnada deniega la autorización con fundamento en la falta de medios económicos del recurrente y por entender que la vivienda alquilada por el recurrente no reúne las condiciones adecuadas para la reagrupación solicitada.

Esta denegación infringe lo dispuesto en los citados preceptos, puesto que el recurrente aportó toda la documentación acreditativa de la suficiencia de sus recursos económicos y de la disponibilidad de una vivienda arrendada suficiente para habitar en ella sus familiares.

SEGUNDO.– CUMPLIMIENTO DE LOS REQUISITOS RELATIVOS A LA SUFICIENCIA DE MEDIOS ECONÓMICOS.

El recurrente presentó con su solicitud la documentación acreditativa de suficiencia de medios económicos para atender las necesidades de la familia. Al efecto, presentó las nóminas correspondientes al año en curso, percibiendo un salario de [IMPORTE] euros mensuales, que supera en exceso los mínimos establecidos en la normativa aplicable, al margen de que [los hijos del recurrente son menores de edad y la cuantía exigida podía ser minorada]. Asimismo, aportó contrato de trabajo con duración hasta el día [FECHA], declaración de IRPF correspondiente al ejercicio [AÑO] y declaración del empresario donde se hacía constar su voluntad de renovar el contrato durante un período adicional de un año, con lo que se cumple lo dispuesto en cuanto a la previsión de mantenimiento de los medios económicos durante el año posterior a la fecha de presentación de la solicitud.

Con ello resulta improcedente la denegación de la autorización en aplicación del artículo 18 de la Ley de Extranjería y de su Reglamento, a la luz de las prescripciones de la Directiva 2003/86/CE, que obliga a concluir, en orden a la acreditación de la suficiencia de los medios de subsistencia con que cuente la persona extranjera reagrupante para atender a las necesidades de su familia, que el recurrente tiene unos ingresos fijos y regulares, que previsiblemente se mantendrán en el tiempo y, además, suficientes para subvenir a sus necesidades y a las de su familia.

TERCERO.– CUMPLIMIENTO DEL REQUISITO DE TENER UNA VIVIENDA ADECUADA.

El recurrente cumple asimismo los requisitos establecidos en el Reglamento sobre la posesión de una vivienda adecuada, pese a lo que se indica en el informe del Departamento de [ORGANISMO QUE EMITE EL INFORME], del que la resolución recurrida deduce la insuficiencia de espacio de la vivienda para residir el recurrente y su familia.

En primer lugar, debe alegarse que la vivienda arrendada por el recurrente tiene espacio suficiente para vivir con su [esposa/esposo] e hijos, atendido que éstos son de corta edad, y que la vivienda cuenta con [SUPERFICIE] metros cuadrados, al margen de que sólo haya [Nº] habitación/es, lo cual no es obstáculo dada la edad de los hijos.

En segundo lugar, y en cualquier caso, debe prevalecer la finalidad pretendida por la reagrupación familiar, consistente en posibilitar que el extranjero que reside legalmente en España pueda vivir junto con sus familiares más cercanos (en este caso, su [esposa/esposo] y [Nº] hijos de [EDADES] años de edad), frente a otros intereses (como el de vivir en una vivienda con mejores condiciones).

Finalmente, y caso de desestimarse esta alegación, el recurrente puede arrendar otra vivienda de mayor superficie y con más habitaciones, para lo cual debería concederse al menos un plazo de subsanación.

Por todo lo expuesto, entendiendo que el recurrente reúne los requisitos para reagrupar a su familia, se interesa la reposición de la resolución denegatoria por los motivos expuestos.

SOLICITO tenga por presentado este escrito junto con los documentos que al mismo se acompañan y por interpuesto recurso de reposición y, en virtud de las alegaciones contenidas en el mismo y previos los trámites legales, dicte resolución dejando sin efecto la resolución recurrida, acordando la autorización de residencia temporal por reagrupación familiar en los términos en que fue solicitada.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma: [NOMBRE Y APELLIDOS]
