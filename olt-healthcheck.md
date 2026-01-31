# 🩺 HEALTH CHECK – OLT Huawei

## 🎯 Objetivo

Checklist diário / preventivo para manter estabilidade da OLT.

---

## 1️⃣ Placas

```
display board 0
```

✔ Todas em Normal  
✔ Controladora ativa e standby OK  

---

## 2️⃣ Uplink

```
display link-aggregation all
display link-aggregation traffic all
```

✔ Estado UP  
✔ Sem erros  
✔ Sem saturação  

---

## 3️⃣ ONTs Offline

```
display ont info 0/1/0 all
```

✔ Verificar quantidade de ONTs offline  
✔ Identificar padrão (porta inteira ou isolado)

---

## 4️⃣ Nível Óptico Aleatório (amostragem)

```
display ont optical-info 0/1/0 <ONT-ID>
```

✔ Dentro da faixa operacional  

---

## 5️⃣ Backup

```
display current-configuration
```

✔ Backup atualizado  
✔ Arquivo salvo externamente  

---

## 📊 Frequência Recomendada

- Diário → Uplink e placas  
- Semanal → Amostragem óptica  
- Mensal → Backup completo  
