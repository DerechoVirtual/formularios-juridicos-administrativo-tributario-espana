---
name: contrato-colaboracion-subvencion-evento-musical-adm-0033
description: "Contrato de colaboración y subvención para un evento musical por procedimiento negociado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de colaboración y subvención para un evento musical por procedimiento negociado

> Formulario **ADM-0033** del plugin **Licencias, subvenciones y reclamaciones ante la Administración** (`formularios-licencias-subvenciones-y-reclamaciones`) · Administrativo y Tributario › Administrativo general (licencias, subvenciones, autoridades de control) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de colaboración y subvención para un evento musical por procedimiento negociado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de colaboración y subvención para un evento musical por procedimiento negociado” para mi caso». También puedes invocarla directamente con `/formularios-licencias-subvenciones-y-reclamaciones:contrato-colaboracion-subvencion-evento-musical-adm-0033`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-licencias-subvenciones-y-reclamaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Licencias, subvenciones y reclamaciones ante la Administración) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (25 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] IMPORTE EN LETRA (3 veces)
- [ ] MES (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] Nº DE SECTOR (2 veces)
- [ ] CALLE Y NÚMERO
- [ ] FECHA
- [ ] FECHAS
- [ ] IMPORTE
- [ ] LUGAR
- [ ] NIF
- [ ] NOMBRE DEL FESTIVAL
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NÚCLEO DE POBLACIÓN

## Normas que cita el formulario

- art. 210 b) Real Decreto Legislativo 2/2000

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

- Junto a «…UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

INTERVIENEN

D. [NOMBRE Y APELLIDOS] como Alcalde del municipio de [LOCALIDAD] y Presidente del Organo de Contratación competente para llevar a buen fin el presente expediente.

D [NOMBRE Y APELLIDOS] como Secretario del municipio de [LOCALIDAD] quien da fé del presente acto.

D. [NOMBRE Y APELLIDOS], en nombre y representación de la mercantil [NOMBRE DEL REPRESENTADO/A] S.L., con domicilio social en [LOCALIDAD], calle, [CALLE Y NÚMERO] y con C.I.F. nº B [NIF] (en adelante LA ADJUDICATARIA).

Los comparecientes se reconocen mutuamente la capacidad legal necesaria para formalizar el presente contrato privado de prestación de servicios, y a tal fin,

EXPONEN

I.- Antecedentes Administrativos.-

La Junta de Gobierno Local, por acuerdo de fecha [FECHA] adjudicó el presente contrato de servicios mediante Procedimiento Negociado sin Publicidad en virtud de lo dispuesto en el artículo 210 b) del Real Decreto Legislativo 2/2000, de 16 de junio, por el que se aprueba el Texto Refundido de la Ley de Contratos de las Administraciones Públicas.

Las partes contratantes se obligan al estricto cumplimiento derivado de la aplicación del Real Decreto 171/2.004, de 30 de Enero, que desarrolla el artículo 24 de la Ley 31/1.995, de 8 de Noviembre, de Prevención de Riesgos Laborales, parcialmente modificada por la Ley 54/2.003, de 12 de Diciembre, en materia de de Coordinación de la Prevención de las actividades empresariales concurrentes.

La adjudicataria deberá cumplir tales previsiones, tanto con respecto al empresario titular o principal del centro de trabajo (el propio Ayuntamiento), como con referencia a las contratas o subcontratas que pudiera establecer para el desarrollo del citado festival de carácter musical.

II.- Objeto del contrato.

Que el EXCMO AYUNTAMIENTO DE [LOCALIDAD] tiene interés en difundir y promocionar la música en directo y el turismo musical en dicho municipio, para lo cual contrata desde este mismo momento, los servicios de la mercantil [DENOMINACIÓN SOCIAL], S.L., para que lleve a cabo la realización de un festival de carácter musical conocido como [NOMBRE DEL FESTIVAL] en régimen de colaboración-subvención.

Dicho festival musical tendrá lugar en -mts2(15Ha) de superficie cedidos por el Excmo. Ayuntamiento de [LOCALIDAD] según Convenio de Colaboración suscrito por ambas partes el [DÍA] de [MES] de [AÑO], encontrándose los mismos en el Sector [Nº DE SECTOR] del núcleo de población conocido como Guardias Viejas perteneciente al término municipal de [LOCALIDAD] los días [FECHAS] y [DÍA] de [MES] de [AÑO], actuando la Adjudicataria como promotora de los eventos y el Ayuntamiento como organizador de los mismos.

El señalado festival se pacta contra remuneración establecida en la claúsula 4ª de este contrato.

III.- Que sobre los antecedentes que preceden, las partes proceden a formalizar el presente Contrato de Servicios en régimen de colaboración-subvención con base en las siguientes

CLÁUSULAS

Objeto

El Excmo. Ayuntamiento de [LOCALIDAD] contrata los servicios de la mercantil [DENOMINACIÓN SOCIAL] para el objeto anteriormente expuesto, teniendo esta última la condición de Promotora Musical y siempre en régimen de colaboración-subvención.

Obligaciones de la adjudicataria

Las labores correspondientes a la tarea definida en la cláusula primera, a desarrollar por LA ADJUDICATARIA., incluyen básicamente: contratación, producción, control del festival, venta de entradas,( que se llevará a cabo por los medios que la adjudicataria estime oportunos, siempre con estricto cumplimiento de la legislación vigente al respecto, siendo de su responsabilidad cualquier infracción que se produzca), elección de los proveedores necesarios para la producción del evento, así como potenciar la campaña de comunicación y turismo musical del municipio de [LOCALIDAD] con los medios y en la forma que estime oportunos la Adjudicataria, sin descartar cualquier otra tarea que sea necesaria para el objeto del contrato y no venga especificada en el presente con cargo al Excmo. Ayuntamiento de

Así mismo la Adjudicataria se compromete a tener contratado y presentar ante el Excmo. Ayuntamiento de [LOCALIDAD] original y copia cotejada de seguro de responsabilidad civil con cobertura para las características del evento en cuestión, que responda de todos los daños personales y materiales que pudieran producirse con ocasión de la celebración del festival musical.

Garantías

LA ADJUDICATARIA declara que tiene la experiencia y medios humanos, técnicos e informáticos necesarios para llevar a feliz término el objeto del contrato.

Precio

Por sus servicios, la adjudicataria recibirá del Excmo. Ayuntamiento de [LOCALIDAD] las siguientes cantidades:

A) [IMPORTE EN LETRA] ( -€) + IVA en concepto de ayuda-subvención para la celebración del evento, que se abonarán en el plazo de días desde la presentación de la correspondiente factura, realizando el pago mediante transferencia bancaria en la siguiente cuenta donde figura como titular LA ADJUDICATARIA.:

B) [IMPORTE EN LETRA] ( -€) + IVA en concepto de ayuda para acometer las obras de remodelación y acondicionamiento del terreno cedido para el fin que se pretende, abonándose en el plazo de [Nº] días desde la presentación de la correspondiente factura en la cuenta bancaria citada en el apartado anterior de la presente claúsula.

En cuanto al cobro de la recaudación bruta dimanante de la venta de entradas corresponde a la adjudicataria.

Recaudación de la venta de entradas

La recaudación por la venta de entradas por el presente evento, será en todo caso inicialmente siempre propiedad de la adjudicataria, sin perjuicio de lo establecido en la presente cláusula en cuanto al reparto parcial de la misma a favor del Excmo. Ayuntamiento de

De igual manera, tras el cobro por la adjudicataria de la totalidad de las cantidades recaudadas por la citada venta de entradas, se compromete ésta, a pagar el porcentaje que corresponda a la Sociedad General de Autores, así como el IVA resultante de la recaudación bruta, en lo que fuera procedente y en los plazos y formas legales.

Respecto al reparto precitado de la recaudación entra la adjudicataria y el Excmo. Ayuntamiento de [LOCALIDAD], se establecen diferentes escenarios, en función de lo que se ha venido a denominar por las partes el "punto cero" en la venta de las entradas, y la recuperación que el Excmo. Ayuntamiento de [LOCALIDAD] pretende intentar lograr con la relación a la subvención pactada a favor de la adjudicataria por medio de éste convenio.

El citado "punto cero", será la cifra coincidente entre lo recaudado por venta de entradas y el costo real final que se derive de la liquidación económica de cierre del evento presentada dentro de los siguientes 30 días de la finalización del Festival. Así, se establece el siguiente reparto de cantidades con relación a la recaudación por la venta de las entradas:

→ Hasta cubrir el "punto cero", esto es, hasta cubrir la totalidad de los gastos absolutos del Festival, la totalidad de las cantidades recaudadas por la venta de entradas será propiedad exclusiva de la Adjudicataria, sin que el Excmo. Ayuntamiento de [LOCALIDAD], tenga derecho a percibir cantidad alguna por este concepto.

→ A partir de alcanzar el "punto cero", y haber recuperado la adjudicataria la totalidad de las cantidades satisfechas para satisfacer la totalidad de los gastos incurridos en el Festival, y hasta que el Excmo. Ayuntamiento de [LOCALIDAD] recupere la totalidad de la cantidad objeto de la subvención establecida en este acuerdo, las cantidades netas recaudadas por la venta de entradas se distribuirán de la siguiente forma:

• 80% para el Excmo. Ayuntamiento de [LOCALIDAD]

• 20% para la Adjudicataria

→ A partir de las recuperaciones económicas supradescritas, las cantidades recaudadas netas por la venta de entradas se distribuirán de la siguiente forma:

• 20% para el Excmo. Ayuntamiento de [LOCALIDAD]

• 80% para la Adjudicataria

Respecto a la liquidación del reparto, se comprometerá la adjudicataria a realizarlo a favor del Excmo. Ayuntamiento de [LOCALIDAD], en el plazo de [Nº] días desde la celebración del Festival.

Seguro

Con el fin de cubrir los [IMPORTE EN LETRA] ( -€) + IVA aportados por el Excmo Ayuntamiento de [LOCALIDAD] para la celebración del festival y demás costes de cancelación, en el caso de que éste no pudiese ser celebrado debido a la incomparecencia de los grupos o inclemencias meteorológicas, LA ADJUDICATARIA deberá contratar póliza de seguros que cubra tales eventualidades por importe de los costes del caché y gastos de producción.

Cesión de terrenos

El Excmo. Ayuntamiento de [LOCALIDAD] ha cedido la cantidad de [IMPORTE] -mts ( Ha) sitos en el Sector [Nº DE SECTOR] del núcleo de población de [NÚCLEO DE POBLACIÓN] perteneciente al municipio de [LOCALIDAD] proveyendo los recursos humanos y técnicos de que disponga para la realización del festival, sin que ello represente en ningún caso contrataciones adicionales para el Excmo. Ayuntamiento.

Permisos y licencias

El Excmo Ayuntamiento de [LOCALIDAD] se compromete a solicitar los correspondientes permisos ante los distintos Organismos de la Administración competentes, facilitándoselos a la Adjudicataria, así como también se compromete a conceder los correspondientes permisos municipales para llevar a cabo el festival, aportando además los siguientes servicios:

.- Personal de Protección Civil.

.- Bomberos.

.- Policía Local.

.- Vallas de Protección Externas al recinto.

.- Retén Eléctrico(que será de cargo de la Adjudicataria.)

.- Control de aparcamiento y tráfico.

.- Asistencia médica y sanitaria (que será de cargo de la Adjudicataria.)

.- Aseos en el recinto exterior.

.- Nombramiento de una o más personas encargadas de la Coordinación de las Actividades Preventivas de las empresas concurrentes, en el supuesto que se opte por este medio de Coordinación.

Duración

El presente contrato tendrá una duración y por tanto validez que abarca desde el día de hoy hasta la finalización del festival.

Alojamiento y catering de los artistas

La Adjudicataria proporcionará a los artistas el alojamiento y el "catering" correspondiente según sus necesidades,

Escenarios

La contratación y el montaje de escenarios, de los equipos de sonido, luces, grupos electrógenos, y los que sean necesarios para las actuaciones, serán de cargo de la Adjudicataria, así como las correspondientes certificaciones suscritas por técnicos competentes que acrediten su buen funcionamiento.

Seguridad

La seguridad, antes, durante y después será de cargo de la Adjudicataria, quien dispondrá de los efectivos necesarios para ello, debiendo contratar como mínimo el personal necesario para cubrir los puestos que el Excmo. Ayuntamiento indicará en el Plan de Emergencia a suscribir, que ella misma se encargará de redactar y presentar para su aprobación ante los estamentos oficiales oportunos con el fin de obtener los permisos necesarios concernientes a ese respecto.

Servicio de bar

El Excmo Ayuntamiento de [LOCALIDAD] autoriza a la Adjudicataria la instalación de servicio de bar dentro del recinto donde se celebrará el festival, siendo ésta la única beneficiaria de su explotación; dichas barras se ubicarán en áquellos lugares previamente determinados en el oportuno Plan de Emergencia a suscribir entre ambas partes; dicho servicio de bar quedará sujeto a las normas de funcionamiento que se firmarán por las partes con carácter previo, las cuales se pactan de obligado cumplimiento, sin perjuicio de la legalidad vigente al efecto.

Indemnización

LA ADJUDICATARIA en ningún caso tendrá derecho a pedir indemnización alguna al Excmo. Ayuntamiento de [LOCALIDAD] una vez resuelto o finalizado este contrato, renunciando desde este momento a cualquier hipotética indemnización que le pudiera corresponder como consecuencia del desarrollo de su actividad, que de conformidad con el objeto del contrato, se dirige a potenciar el municipio de [LOCALIDAD] dentro del ámbito musical. Dicha renuncia expresa tampoco podrá entenderse como reconocimiento ímplicito por el Excmo Ayuntamiento [LOCALIDAD] a la Adjudicataria de derecho indemnizatorio alguno.

[ELEGIR UNA OPCIÓN: Jurisdicción y ley aplicable / Sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Con cláusula penal en caso de no ejecución voluntaria de la sentencia]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente ACUERDO, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Y en prueba de conformidad con todo lo expuesto, firman el presente por duplicado y a un solo efecto, en lugar y fecha indicados al encabezamiento.
