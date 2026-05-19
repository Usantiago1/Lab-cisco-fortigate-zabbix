# Laboratorio de Monitoreo de Red: FortiGate + Cisco + Zabbix

Este laboratorio simula un entorno de red corporativa interconectado en GNS3, enfocado en la gestión de telemetría y monitoreo de infraestructura mediante el protocolo SNMPv2c.

## 🛠️ Topología y Arquitectura
- **Servidor de Monitoreo:** Zabbix corriendo en entorno Ubuntu local.
- **Firewall Perimetral:** FortiGate v7 (Manejo de políticas estrictas por puerto UDP 161).
- **Core Router:** Cisco IOS (Configuración de subinterfaces VLAN y rutas estáticas de retorno).

## 🔍 Desafíos de Troubleshooting Resueltos
1. **Habilitación de SNMP en Interfaces del Firewall:** Apertura del puerto `UDP 161` en zonas específicas del FortiGate usando la CLI.
2. **Enrutamiento Asimétrico (Reverse Path Forwarding):** Corrección del camino de retorno en el router Cisco para la subred del servidor de monitoreo (`192.168.122.0/24`).
3. **Validación de Telemetría Quirúrgica:** Pruebas de estrés y simulación de incidentes lógicos (caídas de subinterfaces VLAN) detectadas en tiempo real por Zabbix.
