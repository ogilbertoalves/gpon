# 🔁 FAILOVER – OLT Huawei

⚠ EXECUTAR SOMENTE EM JANELA CONTROLADA

---

## 🎯 Objetivo

Realizar switch da controladora ativa para standby.

---

## ✅ Checklist Prévio

- Sem alarmes críticos
- Backup realizado
- Tráfego monitorado
- Comunicação interna realizada

---

## 🔄 Executar failover

```
system switch-over
```

---

## 🔍 Pós-validação

1. Verificar placas:

```
display board 0
```

2. Validar uplink:

```
display link-aggregation all
```

3. Verificar ONTs:

```
display ont info 0/1/0 all
```

---

## 📌 Rollback

Caso problema identificado:
- Abrir chamado engenharia
- Avaliar retorno manual
