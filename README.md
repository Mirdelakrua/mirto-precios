# mirto-precios

Precios vigentes de la verificación técnica vehicular (VTV, RTO, ITV) en cada provincia argentina, en pesos y con IVA incluido. Es la fuente de precios de [mirto.com.ar](https://mirto.com.ar).

- `precios.json` → `provincias.{slug}`: `precios` por categoría (`auto`, `moto`, `camioneta`, `pesado`, `taxi`; `null` = sin precio único publicado), `desde` (fecha de vigencia AAAA-MM-DD), `fuente` (URL) y `resolucion`.
- Una tarea semanal de Claude busca aumentos y actualiza este archivo. El sitio lo lee cada 6 horas y sólo aplica un cambio si tiene fuente, la fecha es posterior a la que tiene y la suba es de hasta 80 %; si no, lo retiene.
