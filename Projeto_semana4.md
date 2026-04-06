*Atividade dia 2026/03/20*
---
<img width="517" height="591" alt="image" src="https://github.com/user-attachments/assets/3b5bc64e-16a2-4c88-9c57-a43274c7f1d3" />
---
---
# Atividade - Formas Padrão e Seleção (SOP / op_select)

Entradas: OP2, OP1, OP0
Saídas: sel0 até sel7

```
OP2 OP1 OP0 | sel0 sel1 sel2 sel3 sel4 sel5 sel6 sel7
0   0   0   | 1    0    0    0    0    0    0    0
0   0   1   | 0    1    0    0    0    0    0    0
0   1   0   | 0    0    1    0    0    0    0    0
0   1   1   | 0    0    0    1    0    0    0    0
1   0   0   | 0    0    0    0    1    0    0    0
1   0   1   | 0    0    0    0    0    1    0    0
1   1   0   | 0    0    0    0    0    0    1    0
1   1   1   | 0    0    0    0    0    0    0    1
```

---

Cada saída é representada por uma expressão lógica:

```
sel0 = OP2' · OP1' · OP0'
sel1 = OP2' · OP1' · OP0
sel2 = OP2' · OP1  · OP0'
sel3 = OP2' · OP1  · OP0
sel4 = OP2  · OP1' · OP0'
sel5 = OP2  · OP1' · OP0
sel6 = OP2  · OP1  · OP0'
sel7 = OP2  · OP1  · OP0
```

---

### Componentes necessários:

* 3 entradas (OP2, OP1, OP0)
* 3 portas NOT (inversores)
* 8 portas AND (3 entradas cada)
* LEDs (opcional)

---

### Passos:

1. Criar as entradas:

   * OP2
   * OP1
   * OP0

2. Criar inversores:

   * OP2 → OP2'
   * OP1 → OP1'
   * OP0 → OP0'

3. Criar as portas AND:

   Cada saída corresponde a uma AND com 3 entradas:

   * sel0 → OP2' · OP1' · OP0'
   * sel1 → OP2' · OP1' · OP0
   * sel2 → OP2' · OP1  · OP0'
   * sel3 → OP2' · OP1  · OP0
   * sel4 → OP2  · OP1' · OP0'
   * sel5 → OP2  · OP1' · OP0
   * sel6 → OP2  · OP1  · OP0'
   * sel7 → OP2  · OP1  · OP0

4. Conectar saídas:

   * Cada AND → um LED ou saída

---

## Resultado

* Circuito funciona como um **decoder 3 → 8**
* Apenas uma saída ativa por vez (one-hot)
* Implementação usando lógica SOP padrão


