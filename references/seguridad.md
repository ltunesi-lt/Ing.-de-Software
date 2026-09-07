# SEGURIDAD (Security)
Fuente: `Software Architecture in Practice, 4th Edition` — Ver págs. 218-219 (General Scenario Table). Este archivo resume los valores típicos; validar contra el texto original si está disponible.

La Seguridad mide la capacidad del sistema de proteger datos y recursos del acceso no autorizado, manteniendo confidencialidad, integridad y disponibilidad de la información frente a ataques.

## Valores típicos de la General Scenario Table

- **Fuente del estímulo**: individuo o sistema, interno o externo al sistema, con o sin credenciales, con intención maliciosa o accidental.
- **Estímulo**: intento de acceso no autorizado, modificación no autorizada de datos, denegación de servicio, escalamiento de privilegios, inspección/lectura no autorizada de datos.
- **Artefacto**: datos en el sistema, servicios, recursos, sistema completo.
- **Ambiente**: online/conectado, offline, detrás de firewall, en tránsito por red pública.
- **Respuesta**: el sistema autentica y autoriza al actor, encripta datos sensibles, registra el intento (auditoría), bloquea/limita el acceso, mantiene disponible el resto del sistema, notifica a los administradores.
- **Medida de la respuesta**: tiempo para detectar el ataque/intrusión; tiempo para responder/bloquear; porcentaje de ataques bloqueados exitosamente; tiempo de recuperación tras una brecha; cantidad de datos comprometidos (idealmente cero).


