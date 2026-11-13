# Dashboard Estados Financieros

Tablero de una página que calcula 10 indicadores financieros a partir de una base editable y muestra, para cada uno, el resultado real, el presupuesto, la comparación con el año anterior, la tendencia de 12 meses y un semáforo. Identifica automáticamente las tres desviaciones que ameritan una decisión.

**Demo:** https://TU-USUARIO.github.io/dashboard-financiero/

## Cómo se usa
1. Abrir `index.html` (o el enlace de la demo).
2. Pestaña **Base editable**: reemplazar los datos de ejemplo por los estados financieros mensuales (36 meses), el presupuesto y, si se desea, los umbrales del semáforo.
3. Pestaña **Tablero**: elegir el mes y leer el semáforo, las tres decisiones y las señales a investigar.
4. **Exportar JSON** guarda la base; **Importar JSON** la recupera.

Los datos se guardan solo en el navegador de quien edita. Los datos incluidos son ilustrativos.

## Indicadores
| Indicador | Fórmula (últimos 12 meses) |
|---|---|
| Margen EBITDA | (EBIT + D&A) / ingresos |
| ROE | Utilidad neta / patrimonio |
| ROIC − WACC | NOPAT / (patrimonio + deuda financiera − efectivo) − WACC |
| Razón corriente | Activo corriente / pasivo corriente |
| Prueba ácida | (Activo corriente − inventarios − anticipos) / pasivo corriente |
| Ciclo de caja | Días de cartera + días de inventario − días de proveedores |
| Cobertura de intereses | EBIT / intereses |
| Deuda financiera / EBITDA | Deuda financiera / EBITDA |
| Flujo operativo / EBITDA | Flujo de caja operativo / EBITDA |
| Indicador Z (Altman Z2) | 6,56·X1 + 3,26·X2 + 6,72·X3 + 1,05·X4 |

## Semáforo
- **Modo meta:** desvío adverso contra el presupuesto del mes (verde ≤ 3 %, ámbar ≤ 10 %, rojo por encima; editable).
- **Modo umbral:** valores fijos de verde y ámbar. Para el indicador Z se usan los de Altman Z2 (≥ 2,60 sano; 1,11 a 2,59 zona gris; ≤ 1,10 riesgo). Los demás umbrales son referencias iniciales y deben ajustarse al sector, a los covenants y a la política de cada empresa.

## Las tres decisiones
Se priorizan los indicadores que la gerencia puede mover (palancas) por gravedad del semáforo, sin repetir tema. Cada decisión trae una acción propuesta y un responsable.

## Fuentes y límites
Marco de análisis: presentación de Análisis Financiero (MBA, Gerencia Financiera); Ochoa et al. (2009), «El indicador Z», *Contaduría Universidad de Antioquia*, 54; material sobre EVA y flujo de caja. Los saldos de balance se toman a fin de mes, no como promedio. Los indicadores son una guía para investigar, no un dictamen de solvencia.
