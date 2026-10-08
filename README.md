# 📱 Sistema de Cobertura de Turnos No Programados

## 🚨 Proyecto de investigación – TEINCO

Diseño de un aplicativo móvil para facilitar la cobertura de turnos no programados del personal operativo de vigilancia cuando se presenta ausentismo laboral.

---

## 🎯 Objetivo del proyecto

Diseñar un aplicativo móvil que permita agilizar y hacer trazable la cobertura de turnos no programados del personal operativo de vigilancia, reduciendo la dependencia de llamadas telefónicas y mensajes informales.

---

## 👥 Actores principales

- 👨‍💼 Supervisor / Coordinador
- 👮 Guarda de seguridad
- 📱 Aplicativo móvil
- 🗄️ Sistema de información

---

# 🌳 Árbol de decisiones

El siguiente flujo representa el proceso propuesto para gestionar un turno no programado generado por ausentismo laboral.

```mermaid
flowchart TD

A([🚨 INICIO]) --> B{¿Se presenta un ausentismo?}

B -->|NO| C([✅ Continuar con el turno normal])

B -->|SÍ| D{¿Existe un turno por cubrir?}

D -->|NO| E([✅ No requiere reemplazo])

D -->|SÍ| F[📢 Registrar turno no programado]

F --> G[📱 Notificar a guardas disponibles]

G --> H{¿Hay guardas disponibles?}

H -->|NO| I[⚠️ Notificar al supervisor]

H -->|SÍ| J[📲 Enviar información del turno]

J --> K{¿Un guarda acepta el turno?}

K -->|SÍ| L[✅ Confirmar guarda]

K -->|NO| M[🔄 Buscar otro guarda]

M --> H

L --> N[📋 Registrar asignación]

N --> O[🕐 Realizar seguimiento del turno]

O --> P([🏁 FIN])

I --> Q{¿Se encuentra un reemplazo alternativo?}

Q -->|SÍ| L

Q -->|NO| R[🚨 Escalar situación al supervisor]

R --> P

C --> P
E --> P
