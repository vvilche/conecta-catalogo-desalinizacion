# Catálogo de Desalinización — Chile

Catálogo HTML de plantas desalinizadoras de Chile (instaladas y proyectadas) + las
empresas EPC/constructoras e ingenierías que las hacen. Ángulo CONECTA: las desaladoras
son plantas de ósmosis inversa (proceso continuo) → requieren DCS + instrumentación +
SCADA; las EPC/ingenierías que las construyen son el CANAL para insertarse como integrador
de la especialidad eléctrica/control.

## Estructura
- `index.html` — grid de tarjetas; cada tarjeta enlaza a su ficha.
- `ficha_<entidad>.html` — ficha con 6 secciones: Quién es · Qué hace · Proyectos/clientes ·
  Team de Compras (chips mailto/tel/LinkedIn, rol CT/D/A/R/I/C) · Contacto corporativo · Ángulo CONECTA.
- `research/*.json` — datos crudos con fuentes verificables (origen de las fichas).
- `build/generate.py` — regenera index + fichas desde los JSON.

## Clasificación
- **CANAL** (verde) — EPC/constructora/ingeniería que subcontrata la especialidad eléctrica/control.
- **CLIENTE FINAL** (gris) — planta desaladora que compra DCS + SCADA + instrumentación.

## Reglas de datos
- Nada se inventa: sin fuente pública verificable → campo vacío ("no verificado").
- Cada dato cita su URL de fuente (formato "↳ url").
- Prioridad a jefes de área (Team de Compras: CT/D/A/R/I/C).

## Rebuild
```bash
python3 build/generate.py
```
