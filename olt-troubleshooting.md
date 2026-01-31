# 🔧 TROUBLESHOOTING – OLT Huawei

## 🎯 Objetivo

Padronizar diagnóstico de incidentes.

---

## 🚨 CENÁRIO 1 – Cliente sem conexão

### Passo 1 – Verificar ONU

```
display ont info 0/1/0 all
```

Se Offline:
- Verificar nível óptico
- Confirmar registro
- Checar histórico

---

### Passo 2 – Verificar nível óptico

```
display ont optical-info 0/1/0 <ONT-ID>
```

- RX < -28 dBm → possível atenuação
- RX normal → verificar VLAN

---

### Passo 3 – Verificar configuração

```
display current-configuration ont 0/1/0 <ONT-ID>
```

Confirmar:
- VLAN correta
- Service-port ativo

---

## 🚨 CENÁRIO 2 – Porta PON inteira offline

- Verificar fibra rompida
- Verificar splitter
- Verificar status da placa

```
display board 0
```

---

## 🚨 CENÁRIO 3 – Uplink sem tráfego

```
display link-aggregation traffic all
```

Possíveis causas:
- VLAN não permitida
- Porta bloqueada no core
- Problema físico SFP

---

## 📊 MATRIZ RÁPIDA

| Sintoma | Ação |
|----------|------|
| ONU flapping | Verificar óptico |
| PON inteira offline | Verificar fibra |
| Uplink UP sem tráfego | Verificar VLAN |
| RX abaixo de -29 | Verificar emenda |
