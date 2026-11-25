---
name: indice
description: "Índice de los 25 formularios de Reclamaciones tributarias y económico-administrativas. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Reclamaciones tributarias y económico-administrativas: índice de formularios

> Plugin `formularios-reclamaciones-tributarias` · 25 formularios · normativa revisada el 25-11-2026.

## Qué es

Para discutir con Hacienda: reclamaciones económico-administrativas ante los TEAR y el TEAC, alegaciones, oposición a la derivación de responsabilidad, recursos contra liquidaciones e IVA, aplazamientos, consolidación fiscal y otras comunicaciones tributarias.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Reclamación económico-administrativa contra una liquidación»
- «Oposición a la derivación de responsabilidad subsidiaria»
- «Solicitud de aplazamiento de una deuda tributaria»

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

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-reclamaciones-tributarias:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (3)

| Código | Formulario | Skill |
|---|---|---|
| ADM-0001 | Reclamación económico-administrativa contra la repercusión tributaria improcedente | `reclamacion-economico-administrativa-contra-adm-0001` |
| ADM-0019 | Reclamación económico-administrativa contra el acuerdo que confirma una autoliquidación | `reclamacion-economico-administrativa-contra-acuerdo-adm-0019` |
| ADM-0023 | Solicitud de reconocimiento de justicia gratuita para recuperar la tasa pagada (Ley 10-2012) | `solicitud-reconocimiento-justicia-gratuita-recuperar-adm-0023` |

### Contestaciones, oposiciones y alegaciones (7)

| Código | Formulario | Skill |
|---|---|---|
| ADM-0003 | Alegaciones del responsable solidario o subsidiario frente a la derivación de deuda tributaria | `alegaciones-responsable-solidario-subsidiario-frente-adm-0003` |
| ADM-0005 | Oposición del administrador de sociedad inactiva a la derivación de responsabilidad subsidiaria | `oposicion-administrador-sociedad-inactiva-derivacion-adm-0005` |
| ADM-0006 | Oposición a la derivación de responsabilidad solidaria por colaborar en una infracción tributaria | `oposicion-derivacion-responsabilidad-solidaria-adm-0006` |
| ADM-0009 | Alegaciones contra el IVA exigido en la cesión obligatoria de un terreno al ayuntamiento | `alegaciones-contra-iva-exigido-cesion-obligatoria-adm-0009` |
| ADM-0010 | Alegaciones contra la denegación de exención a una entidad social de salud mental | `alegaciones-contra-denegacion-exencion-entidad-social-adm-0010` |
| ADM-0011 | Alegaciones económico-administrativas contra la negativa a deducir IVA por factura incompleta | `alegaciones-economico-administrativas-contra-negativa-adm-0011` |
| ADM-0013 | Alegaciones del interesado en el procedimiento de declaración de lesividad | `alegaciones-interesado-procedimiento-declaracion-adm-0013` |

### Recursos (3)

| Código | Formulario | Skill |
|---|---|---|
| ADM-0014 | Recurso de reposición contra la sanción pecuniaria por infracción tributaria | `recurso-reposicion-contra-sancion-pecuniaria-adm-0014` |
| ADM-0021 | Recurso de reposición contra actas de inspección con conformidad (A01) | `recurso-reposicion-contra-actas-inspeccion-conformidad-adm-0021` |
| ADM-0025 | Recurso de reposición contra la diligencia que requiere aportar la tasa judicial en proceso exento | `recurso-reposicion-contra-diligencia-requiere-aportar-adm-0025` |

### Comunicaciones, requerimientos y cartas (8)

| Código | Formulario | Skill |
|---|---|---|
| ADM-0002 | Solicitud de aplazamiento o fraccionamiento de deudas tributarias superiores a 50.000 euros | `solicitud-aplazamiento-fraccionamiento-deudas-adm-0002` |
| ADM-0004 | Comunicación previa del régimen de consolidación fiscal del Impuesto sobre Sociedades | `comunicacion-previa-regimen-consolidacion-fiscal-adm-0004` |
| ADM-0008 | Solicitud de ampliación del plazo de alegaciones y prueba en reclamación económico-administrativa | `solicitud-ampliacion-plazo-alegaciones-prueba-adm-0008` |
| ADM-0015 | Solicitud de aprobación de plan especial de amortización en el Impuesto sobre Sociedades | `solicitud-aprobacion-plan-especial-amortizacion-adm-0015` |
| ADM-0016 | Solicitud a Hacienda de imputación temporal distinta del devengo en el Impuesto sobre Sociedades | `solicitud-hacienda-imputacion-temporal-distinta-adm-0016` |
| ADM-0017 | Comunicación a la AEAT de una fusión por absorción acogida al régimen especial de fusiones | `comunicacion-aeat-fusion-absorcion-acogida-regimen-adm-0017` |
| ADM-0018 | Comunicación a Hacienda de una escisión de participaciones acogida al régimen especial del IS | `comunicacion-hacienda-escision-participaciones-acogida-adm-0018` |
| ADM-0022 | Solicitud de devolución de ingresos indebidos de la tasa judicial por justicia gratuita (RDL 3-2013) | `solicitud-devolucion-ingresos-indebidos-tasa-judicial-adm-0022` |

### Escritos de trámite y otros (4)

| Código | Formulario | Skill |
|---|---|---|
| ADM-0007 | Escrito de alegaciones frente al informe del órgano autor del acto impugnado ante el TEA | `escrito-alegaciones-frente-informe-organo-autor-acto-adm-0007` |
| ADM-0012 | Escrito de personación del recurrido en la reclamación por omisión de expedir una factura | `escrito-personacion-recurrido-reclamacion-omision-adm-0012` |
| ADM-0020 | Escrito de alegaciones a las actas de inspección con disconformidad (A02) | `escrito-alegaciones-actas-inspeccion-disconformidad-a02-adm-0020` |
| ADM-0024 | Escrito pidiendo suspender el plazo para subsanar el pago de la tasa judicial | `escrito-pidiendo-suspender-plazo-subsanar-pago-tasa-adm-0024` |
