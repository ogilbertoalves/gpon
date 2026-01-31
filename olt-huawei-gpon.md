# 📘 RUNBOOK – OLT Huawei GPON

## 🎯 Objetivo

Padronizar procedimentos operacionais e de troubleshooting para OLT Huawei GPON.

---

## Verificar placas

```
display board 0
```

Esperado:
- Status: Normal
- Controladora Active / Standby saudável

---

## Verificar agregação (uplink)

```
display link-aggregation all
display lacp link-aggregation verbose 1
display link-aggregation traffic all
```

Validar:
- Estado UP
- Sem portas Unselected
- Tráfego RX/TX consistente

---

## Ver ONTs da PON

```
display ont info 0/1/0 all
```

Verificar:
- Online
- Distância
- Status

---

## Ver nível óptico

```
display ont optical-info 0/1/0 <ONT-ID>
```

Faixa aceitável:
- RX: -8 a -28 dBm
- TX: 1 a 5 dBm

---

## Ver configuração específica ONU

```
display current-configuration ont 0/1/0 <ONT-ID>
```

Confirmar:
- VLAN
- Service-port
- Profile
