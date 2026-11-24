# Reclamaciones tributarias y económico-administrativas

> Plugin de Claude Code `formularios-reclamaciones-tributarias` · **25 formularios** · Administrativo y Tributario · normativa revisada el 24-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para discutir con Hacienda: reclamaciones económico-administrativas ante los TEAR y el TEAC, alegaciones, oposición a la derivación de responsabilidad, recursos contra liquidaciones e IVA, aplazamientos, consolidación fiscal y otras comunicaciones tributarias.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 25 está al final):

- **Demandas, peticiones y solicitudes iniciales** (3). Por ejemplo: Reclamación económico-administrativa contra la repercusión tributaria improcedente; Reclamación económico-administrativa contra el acuerdo que confirma una autoliquidación; Solicitud de reconocimiento de justicia gratuita para recuperar la tasa pagada (Ley 10-2012).
- **Contestaciones, oposiciones y alegaciones** (7). Por ejemplo: Alegaciones del responsable solidario o subsidiario frente a la derivación de deuda tributaria; Oposición del administrador de sociedad inactiva a la derivación de responsabilidad subsidiaria; Oposición a la derivación de responsabilidad solidaria por colaborar en una infracción tributaria.
- **Recursos** (3). Por ejemplo: Recurso de reposición contra la sanción pecuniaria por infracción tributaria; Recurso de reposición contra actas de inspección con conformidad (A01); Recurso de reposición contra la diligencia que requiere aportar la tasa judicial en proceso exento.
- **Comunicaciones, requerimientos y cartas** (8). Por ejemplo: Solicitud de aplazamiento o fraccionamiento de deudas tributarias superiores a 50.000 euros; Comunicación previa del régimen de consolidación fiscal del Impuesto sobre Sociedades; Solicitud de ampliación del plazo de alegaciones y prueba en reclamación económico-administrativa.
- **Escritos de trámite y otros** (4). Por ejemplo: Escrito de alegaciones frente al informe del órgano autor del acto impugnado ante el TEA; Escrito de personación del recurrido en la reclamación por omisión de expedir una factura; Escrito de alegaciones a las actas de inspección con disconformidad (A02).

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Reclamación económico-administrativa contra una liquidación»
   - «Oposición a la derivación de responsabilidad subsidiaria»
   - «Solicitud de aplazamiento de una deuda tributaria»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-reclamaciones-tributarias:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-reclamaciones-tributarias:reclamacion-economico-administrativa-contra-adm-0001`. Los nombres están en la lista de formularios de abajo.

## Qué hace Claude cuando usas un formulario

1. Comprueba que Jurisprudenciator está conectado. Si no lo está, se para y te dice cómo conectarlo: no redacta nada sin él. Todos los datos jurídicos del documento (artículos vigentes, sentencias con su ECLI, datos registrales) salen de Jurisprudenciator; nunca de memoria.
2. Te pide en una sola tanda los datos del caso (partes, órgano, fechas, importes…). Lo que no sepas queda como hueco visible.
3. Resuelve contigo las opciones que el formulario deja abiertas y decide qué párrafos opcionales entran según los hechos.
4. Aplica las notas de actualización de la revisión del 24-11-2026 (reformas legales, órganos judiciales de la LO 1/2025, plazos).
5. Comprueba en el BOE, con Jurisprudenciator, cada norma que cita el documento; si alguna ha cambiado, usa la redacción vigente y te lo dice.
6. Te entrega el documento en Word **tal cual es el formulario**: empieza por su primera línea, sin títulos, notas ni explicaciones añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. En el chat te dice lo que queda pendiente y, si es un escrito, el plazo y ante quién se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Antes de empezar

- **Dónde funciona:** en Claude Code y en Claude (web, escritorio y Cowork). Se instala desde este repositorio de GitHub o subiendo el ZIP del plugin.
- **Jurisprudenciator es imprescindible:** el plugin trae el conector y cada skill trabaja siempre con él. Sin una cuenta de Jurisprudenciator conectada, las skills se paran y no redactan nada. La primera vez hay que iniciar sesión (en Claude Code, con `/mcp`; o con tu URL personal: https://jurisprudenciator.lexiaipro.org/instalacion). Si ya tienes Jurisprudenciator conectado en Claude, las skills usan ese.
- **Espacio que ocupa:** unos 1.638 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-reclamaciones-tributarias@formularios-juridicos-administrativo-tributario-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-administrativo-tributario-espana
/plugin install formularios-reclamaciones-tributarias@formularios-juridicos-administrativo-tributario-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-administrativo-tributario-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-administrativo-tributario-espana/releases/latest/download/formularios-reclamaciones-tributarias.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (25)

| Código | Formulario | Skill |
|---|---|---|
| ADM-0001 | Reclamación económico-administrativa contra la repercusión tributaria improcedente | `reclamacion-economico-administrativa-contra-adm-0001` |
| ADM-0002 | Solicitud de aplazamiento o fraccionamiento de deudas tributarias superiores a 50.000 euros | `solicitud-aplazamiento-fraccionamiento-deudas-adm-0002` |
| ADM-0003 | Alegaciones del responsable solidario o subsidiario frente a la derivación de deuda tributaria | `alegaciones-responsable-solidario-subsidiario-frente-adm-0003` |
| ADM-0004 | Comunicación previa del régimen de consolidación fiscal del Impuesto sobre Sociedades | `comunicacion-previa-regimen-consolidacion-fiscal-adm-0004` |
| ADM-0005 | Oposición del administrador de sociedad inactiva a la derivación de responsabilidad subsidiaria | `oposicion-administrador-sociedad-inactiva-derivacion-adm-0005` |
| ADM-0006 | Oposición a la derivación de responsabilidad solidaria por colaborar en una infracción tributaria | `oposicion-derivacion-responsabilidad-solidaria-adm-0006` |
| ADM-0007 | Escrito de alegaciones frente al informe del órgano autor del acto impugnado ante el TEA | `escrito-alegaciones-frente-informe-organo-autor-acto-adm-0007` |
| ADM-0008 | Solicitud de ampliación del plazo de alegaciones y prueba en reclamación económico-administrativa | `solicitud-ampliacion-plazo-alegaciones-prueba-adm-0008` |
| ADM-0009 | Alegaciones contra el IVA exigido en la cesión obligatoria de un terreno al ayuntamiento | `alegaciones-contra-iva-exigido-cesion-obligatoria-adm-0009` |
| ADM-0010 | Alegaciones contra la denegación de exención a una entidad social de salud mental | `alegaciones-contra-denegacion-exencion-entidad-social-adm-0010` |
| ADM-0011 | Alegaciones económico-administrativas contra la negativa a deducir IVA por factura incompleta | `alegaciones-economico-administrativas-contra-negativa-adm-0011` |
| ADM-0012 | Escrito de personación del recurrido en la reclamación por omisión de expedir una factura | `escrito-personacion-recurrido-reclamacion-omision-adm-0012` |
| ADM-0013 | Alegaciones del interesado en el procedimiento de declaración de lesividad | `alegaciones-interesado-procedimiento-declaracion-adm-0013` |
| ADM-0014 | Recurso de reposición contra la sanción pecuniaria por infracción tributaria | `recurso-reposicion-contra-sancion-pecuniaria-adm-0014` |
| ADM-0015 | Solicitud de aprobación de plan especial de amortización en el Impuesto sobre Sociedades | `solicitud-aprobacion-plan-especial-amortizacion-adm-0015` |
| ADM-0016 | Solicitud a Hacienda de imputación temporal distinta del devengo en el Impuesto sobre Sociedades | `solicitud-hacienda-imputacion-temporal-distinta-adm-0016` |
| ADM-0017 | Comunicación a la AEAT de una fusión por absorción acogida al régimen especial de fusiones | `comunicacion-aeat-fusion-absorcion-acogida-regimen-adm-0017` |
| ADM-0018 | Comunicación a Hacienda de una escisión de participaciones acogida al régimen especial del IS | `comunicacion-hacienda-escision-participaciones-acogida-adm-0018` |
| ADM-0019 | Reclamación económico-administrativa contra el acuerdo que confirma una autoliquidación | `reclamacion-economico-administrativa-contra-acuerdo-adm-0019` |
| ADM-0020 | Escrito de alegaciones a las actas de inspección con disconformidad (A02) | `escrito-alegaciones-actas-inspeccion-disconformidad-a02-adm-0020` |
| ADM-0021 | Recurso de reposición contra actas de inspección con conformidad (A01) | `recurso-reposicion-contra-actas-inspeccion-conformidad-adm-0021` |
| ADM-0022 | Solicitud de devolución de ingresos indebidos de la tasa judicial por justicia gratuita (RDL 3-2013) | `solicitud-devolucion-ingresos-indebidos-tasa-judicial-adm-0022` |
| ADM-0023 | Solicitud de reconocimiento de justicia gratuita para recuperar la tasa pagada (Ley 10-2012) | `solicitud-reconocimiento-justicia-gratuita-recuperar-adm-0023` |
| ADM-0024 | Escrito pidiendo suspender el plazo para subsanar el pago de la tasa judicial | `escrito-pidiendo-suspender-plazo-subsanar-pago-tasa-adm-0024` |
| ADM-0025 | Recurso de reposición contra la diligencia que requiere aportar la tasa judicial en proceso exento | `recurso-reposicion-contra-diligencia-requiere-aportar-adm-0025` |

## Privacidad

Ver `PRIVACY.md`.
