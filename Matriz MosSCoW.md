
**Sistema web inteligente para el control de inventarios de ingreso de mineral — Construcción y Minería, Huánuco**
Portafolio de diseño · Sección 2: Priorización MoSCoW y pantallas

## Matriz MoSCoW

| RF | Requerimiento | Indicador | MoSCoW | Pantalla del prototipo |
|---|---|---|---|---|
| RF01 | Registrar el ingreso de mineral con la imagen del ticket de balanza | I1, I2 | Must | P03 Registrar ingreso (captura) |
| RF02 | Reconocer automáticamente los datos del ticket: placa, fecha y peso bruto | I2 | Must | P03 Registrar ingreso (lectura) · P04 Revisar y confirmar (campos con su confianza) |
| RF03 | Validar automáticamente la consistencia de los datos del ticket (V1–V5) | I3 | Must | P04 Revisar y confirmar (validación en línea) |
| RF04 | Permitir el registro y la corrección manual de los datos reconocidos | I3 | Must | P04 Revisar y confirmar · P05 Consulta (corrección con motivo) |
| RF05 | Asignar un código único a cada ingreso de mineral | I4 | Must | P04 Revisar y confirmar (paso «Listo») · P05 Consulta |
| RF06 | Registrar el tipo de mineral y el tipo de vehículo (propio o externo) | I3, I5 | Must | P04 Revisar y confirmar · P08 Catálogo maestro |
| RF07 | Vincular cada ingreso con las etapas de secado, zarandeo, molienda y ensacado | I6 | Must | P06 Lotes y trazabilidad |
| RF08 | Consultar un ingreso por placa y fecha con su ticket de respaldo | I4 | Must | P05 Consulta de ingresos y respaldo · P02 Inicio (búsqueda rápida) |
| RF09 | Generar y exportar el total acumulado mensual por producto | I5 | Must | P07 Consolidado mensual |
| RF10 | Gestionar usuarios y roles de acceso | — | Should | P01 Inicio de sesión · P09 Usuarios y roles |


## Indicadores de la variable dependiente

| Dimensión | Indicador | Pantalla donde se genera el dato |
|---|---|---|
| D1 Oportunidad del registro | I1 Tiempo de espera del registro (h) | P03 (marca de inicio del registro frente a la hora del pesaje) |
| D1 Oportunidad del registro | I2 Tiempo de registro del ingreso (min) | P03 → P04 (inicio y fin del registro) |
| D2 Integridad del registro | I3 Completitud del registro (%) | P04 (campos C1–C7) |
| D2 Integridad del registro | I4 Tiempo de recuperación del respaldo (min) | P05 (consulta → ticket y datos) |
| D3 Consolidación de la producción | I5 Tiempo de consolidación (min) | P07 (solicitud → total del mes por producto) |
| D3 Consolidación de la producción | I6 Grado de trazabilidad (%) | P06 (etapas vinculadas / 4) |

## Funcionalidades complementarias

| Funcionalidad | MoSCoW | Pantalla | Justificación |
|---|---|---|---|
| Destare del vehículo en su primer viaje (tara → peso neto) | Must | P02 Inicio (modal de destare) | Sin tara no hay peso neto (C4, C5 de I3) |
| Alta de vehículo y de tipo de mineral desde el registro | Must | P04 (modales) | Evita interrumpir el registro (I2) |
| Registro manual sin foto (ticket extraviado) | Should | P03 | Respaldo cuando no hay ticket o falla el reconocimiento |
| Dividir el lote en partes y dar de alta el lote (venta o traslado) | Should | P06 | Refleja la operación real de la planta |
| Calendario de llegadas por día | Could | P02 Inicio | Apoyo visual; no alimenta un indicador |
| Bigbags, merma y toneladas por hora | Won't (esta versión) | — | Datos descriptivos de gestión, fuera del alcance de la tesis |
| Guía de remisión y facturación | Won't | — | Fuera del alcance de la tesis |
