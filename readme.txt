# 🕵️ Detective Quest – Mansão Enigma  
### Um projeto interativo usando **Árvore Binária + BST + Hash Table** (HTML + CSS + JS)

Este projeto simula a mecânica de investigação do jogo *Detective Quest*, da Enigma Studios.  
O jogador explora uma mansão representada como uma **árvore binária**, coleta pistas que são armazenadas em uma **árvore de busca (BST)** e as relaciona a suspeitos via **tabela hash**.  
Ao terminar a exploração, o sistema realiza automaticamente o julgamento final.

---

## 🎮 Funcionalidades

### ✔️Exploração da mansão (Árvore Binária)
A mansão é montada manualmente no código como uma estrutura fixa:
- Cada sala possui:  
  - Nome  
  - Possível caminho à esquerda  
  - Possível caminho à direita  
  - Uma pista opcional associada  
- O jogador navega por:  
  - (E) Esquerda  
  - (D) Direita  
  - (S) Sair da mansão  

---

### ✔️Coleta de pistas (BST)
Cada pista encontrada:
- É identificada automaticamente ao entrar na sala  
- É inserida em uma **árvore binária de busca**  
- É exibida ordenadamente usando percurso **in-order**  

---

### ✔️Tabela Hash de suspeitos
Cada pista aponta para um suspeito fixo.  
A tabela hash implementa essa relação:  
🗝 pista → suspeito

Exemplo:
- "luvas-ensanguentadas" → "Mordomo"  
- "contrato-rasgado" → "Sobrinho"

---

### ✔️Julgamento final automatizado
Após encerrar a exploração:
- O jogador escolhe um suspeito  
- O sistema busca na BST todas as pistas coletadas  
- Para cada pista, a hash table indica qual suspeito ela aponta  
- Se **≥ 2 pistas** apontam para o acusado → **Vitória do jogador**  
- Caso contrário → Acusação falha  

---

## 🧩 Conceitos de Estrutura de Dados Utilizados

### 🌳 ÁRVORE BINÁRIA
Representa o mapa fixo da mansão.

### 🌲 BST (Árvore Binária de Busca)
Organiza todas as pistas coletadas automaticamente:
- Inserção ordenada
- Percurso In-Order
- Busca eficiente

### 🔑 TABELA HASH
Associa pistas a suspeitos com acesso em O(1).

### ↔️ Ponteiros e Recursão (Simulados em JS)
- Movimentação entre salas usa referências similares a ponteiros  
- Inserção na BST é totalmente recursiva  
- Verificação de pistas do suspeito usa percurso recursivo  

---

## 📁 Estrutura do Projeto

