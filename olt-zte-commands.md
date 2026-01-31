# 📘 OLT ZTE – Comandos Operacionais

## 🔎 Placas e Hardware

| Comando | Descrição |
|----------|------------|
| show card | Status das placas |
| show equipment | SN e versão |
| show backboard | SN chassis |
| show power | Dados de energia |
| show temperature detail | Temperatura |
| reset-card slotno X | Reset elétrico da placa |
| redundancy switch sc grace | Swap controladora |

---

## 🌐 Interfaces e Uplink

| Comando | Descrição |
|----------|------------|
| sh interface brief | Status interfaces |
| sh optical-module-info xgei-1/X/X | Dados SFP |
| show running-config-interface | Ver config interface |

---

## 🌲 GPON / ONUs

| Comando | Descrição |
|----------|------------|
| sh gpon onu state | Listar ONUs |
| sh gpon onu detail-info gpon_onu-X/X/X:X | Detalhes ONU |
| show pon onu uncfg | ONUs não configuradas |
| sh pon power olt-rx | Potência óptica placa |
| sh pon power onu-tx | Potência óptica ONU |
| reboot (modo pon-onu-mng) | Reboot ONU |

---

## 📡 Multicast

| Comando | Descrição |
|----------|------------|
| show ip mroute | Tabela multicast |
| show ip pim neighbor | Vizinhos PIM |
| show igmp dynamic-member | Usuários IGMP |

---

## 🌍 BGP

| Comando | Descrição |
|----------|------------|
| show bgp all summary | Resumo BGP |
| show ip forwarding route bgp | Rotas BGP |
| show bgp ipv4 unicast neighbor in IP | Rotas recebidas |
| show bgp ipv4 unicast neighbor out IP | Rotas anunciadas |
