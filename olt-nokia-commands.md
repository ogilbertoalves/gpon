# 📘 OLT Nokia (Alcatel-Lucent ISAM) – Comandos Operacionais
Versão do documento: V4  
Data de revisão: 20/06/2025  
Software Release: L6GPAA68.448 (R6.8)

---

# 🔎 Verificação de Hardware

## Verificar placas
show equipment slot

- nt-a / nt-b → Placas de uplink
- fglt-a → Placa PON (equivalente GTGH ZTE)

## Ver transceivers uplink
show equipment transceiver-inventory nt-a:xfp:1

## Inventário SFP PON
show pon sfp-inventory
show pon optics

## Mostrar todas as portas
show port

---

# 🌲 GPON / ONTs

## ONUs não provisionadas
show pon unprovision-onu

## ONUs registradas
show equipment ont operational-data

## Buscar ONU por SN
show equipment ont slot | match exact:AAAAAAA

## Estado da ONT
show equipment ont operational-data
show equipment ont interface 1/1/1/1/1 detail

## Informações Ethernet ONT
show ethernet ont operational-data
show ethernet ont operational-data detail

## Nível óptico RX
show equipment ont optics

## DHCP IP da ONT
show iphost ont operational-data
show iphost ont operational-data | match exact:1/1/1/1/1

---

# 🌐 VLAN / Serviços

## Listar VLANs
show vlan name

## Ver onde VLAN está aplicada
show service sap-using | match 112

## Ver MAC Address (OLT)
show service fdb-mac
show service fdb-mac aa:aa:aa:aa:aa:aa

## Ver MAC por VLAN / Porta
show vlan bridge-port-fdb
show vlan bridge-port-fdb vlan-id 2001
show service id 2001 fdb detail

---

# 📡 QoS

info configure qos profiles bandwidth

---

# 📡 PON – Validação

show pon optics
show equipment ont optics

---

# 🔐 SNTP / NTP

show sntp server-table

---

# ⚙️ Configuração Porta PON

## Ativar Porta PON
configure pon interface 1/1/1/X fec-dn enable auth-method loid-sn-slid tconts-per-frame 64 admin-state up

configure qos interface pon:1/1/1/X ds-num-queue 8

configure pon interface 1/1/1/X utilization pon-pmcollect pm-enable

---

# ➕ Adicionar Placa ACU

configure equipment slot acu:1/1 planned-type ngfc-e no power-down unlock

---

# 🚪 Encerrar Sessão

## Sair modo configuração
exit all

## Logout SSH
logout
