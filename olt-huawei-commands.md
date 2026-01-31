# 📘 OLT Huawei – Comandos Operacionais

## 🔎 Placas e Hardware

| Comando | Descrição |
|----------|------------|
| display board 0 | Verificar status de placas |
| display board serial-number 0 | Ver número serial das placas |
| display frame serial-number | Exibe SN do chassis |
| display temperature 0/X | Temperatura do slot |
| reboot system | Reboot da OLT |

---

## 🌐 Uplink / Link Aggregation

| Comando | Descrição |
|----------|------------|
| display link-aggregation all | Verificar agregações |
| display link-aggregation status 0/8/0 | Status da agregação |
| display link-aggregation traffic all | Tráfego do LAG |
| display lacp link-aggregation verbose 1 | Detalhes LACP |
| display port ddm-info 0 | Níveis TX/RX SFP |

---

## 🌲 GPON / ONUs

| Comando | Descrição |
|----------|------------|
| display ont info 0 all | Listar todas ONUs |
| display ont info by-sn XXXXXXXXX | Buscar ONU por SN |
| display ont optical-info 0 all | Ver níveis ópticos |
| display ont wan-info 0/1 1 1 | Informações WAN |
| display ont wlan-info 0/1/1 1 | Informações WLAN |
| display ont version 0 all | Modelo e versão ONUs |
| ont reset X X | Reset ONU específica |

---

## 📡 Multicast / IGMP

| Comando | Descrição |
|----------|------------|
| display igmp user all | Usuários IGMP |
| display igmp program all | Canais multicast |
| display multicast routing-table | Tabela multicast |
| display multicast flow-statistic vlan XXXX | Tráfego multicast |

---

## 🌍 BGP

| Comando | Descrição |
|----------|------------|
| display bgp peer | Vizinhos BGP |
| display arp vlan XXXX | Buscar IP via VLAN |

---

## 📊 Sistema

| Comando | Descrição |
|----------|------------|
| display version | Versão do sistema |
| display current-configuration | Configuração atual |
| display alarm active all | Alarmes ativos |
| display log all | Logs |
| system switch-over | Comutar placa controladora |
