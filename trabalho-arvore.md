# Parte 1 – Tipos de Árvores

## Árvore AVL

### Conceito

A árvore AVL é uma árvore binária de busca auto balanceada. Seu principal objetivo é manter a árvore equilibrada para garantir buscas, inserções e remoções eficientes.

### Características

* É uma árvore binária de busca.
* Mantém a diferença de altura entre as subárvores em no máximo 1.
* Utiliza rotações para corrigir desequilíbrios.
* Possui complexidade O(log n) para busca, inserção e remoção.

### Vantagens

* Busca rápida e eficiente.
* Mantém a árvore balanceada.
* Bom desempenho para grandes volumes de dados.

### Desvantagens

* Implementação mais complexa.
* Inserções e remoções podem exigir rotações.

### Exemplo ilustrado

```text
       30
      /  \
    20    40
   /
 10
```

---

## Árvore Rubro-Negra

### Conceito

A árvore Rubro-Negra é uma árvore binária de busca auto balanceada que utiliza nós vermelhos e pretos para manter o equilíbrio da estrutura.

### Regras de coloração

* Todo nó é vermelho ou preto.
* A raiz é sempre preta.
* Um nó vermelho não pode possuir filhos vermelhos.
* Todos os caminhos da raiz até as folhas possuem a mesma quantidade de nós pretos.

### Vantagens

* Inserção e remoção eficientes.
* Necessita de menos rotações que uma árvore AVL.
* Muito utilizada em sistemas e bibliotecas.

### Desvantagens

* Implementação mais complexa.
* Pode ficar menos balanceada que uma árvore AVL.

### Exemplo ilustrado

```text
        20(P)
       /    \
   10(V)   30(V)
```

**P = Preto**
**V = Vermelho**

---

## Árvore N-ária

### Conceito

A árvore N-ária é uma estrutura em que cada nó pode possuir vários filhos, diferentemente das árvores binárias, que possuem no máximo dois.

### Diferenças em relação às árvores binárias

| Árvore Binária                     | Árvore N-ária                             |
| :--------------------------------- | :---------------------------------------- |
| Até 2 filhos por nó                | Pode possuir vários filhos                |
| Estrutura mais simples             | Estrutura mais flexível                   |
| Mais utilizada em árvores de busca | Mais utilizada em estruturas hierárquicas |

### Vantagens

* Permite representar hierarquias complexas.
* Maior flexibilidade na organização dos dados.
* Muito utilizada em sistemas reais.

### Desvantagens

* Pode consumir mais memória.
* Implementação mais complexa.

### Exemplo ilustrado

```text
          A
       /  |  \
      B   C   D
     / \      |
    E   F     G
```

### Aplicações práticas

* Sistemas de arquivos.
* Estruturas HTML e XML.
* Árvores de decisão.
* Jogos.
* Inteligência artificial.
* Organização de dados hierárquicos.


---






# Parte 2 – Operações em Árvores

## Rotação Simples à Direita

### Objetivo

Corrigir o desequilíbrio causado pelo excesso de nós na subárvore esquerda.

### Situação em que é utilizada

Quando ocorre o caso Esquerda-Esquerda (LL).

### Exemplo

**Antes**

```text
      30
     /
   20
  /
10
```

**Depois**

```text
     20
    /  \
  10    30
```

---

## Rotação Simples à Esquerda

### Objetivo

Corrigir o desequilíbrio causado pelo excesso de nós na subárvore direita.

### Situação em que é utilizada

Quando ocorre o caso Direita-Direita (RR).

### Exemplo

**Antes**

```text
10
  \
   20
     \
      30
```

**Depois**

```text
      20
     /  \
   10    30
```

---

## Rotação Dupla

### Esquerda-Direita (LR)

É utilizada quando o desequilíbrio ocorre na esquerda e depois na direita.

**Antes**

```text
      30
     /
   10
     \
      20
```

**Depois**

```text
      20
     /  \
   10    30
```

### Direita-Esquerda (RL)

É utilizada quando o desequilíbrio ocorre na direita e depois na esquerda.

**Antes**

```text
10
  \
   30
  /
20
```

**Depois**

```text
      20
     /  \
   10    30
```

---

## Inversão (Espelhamento)

### Conceito

Consiste em trocar os nós da esquerda pelos da direita, formando uma imagem espelhada da árvore.

### Aplicação

Pode ser utilizada em algoritmos, estruturas hierárquicas e processamento de imagens.

### Exemplo

**Antes**

```text
      A
     / \
    B   C
```

**Depois**

```text
      A
     / \
    C   B
```

---


# Parte 3 – Aplicação Prática

## Sistema de Arquivos

### Aplicação escolhida

Sistema de arquivos (pastas e arquivos em um computador ou sistema operacional).

### Estrutura mais adequada

Árvore N-ária.

### Justificativa

O sistema de arquivos é melhor representado por uma árvore N-ária porque cada pasta pode ter vários arquivos e também várias subpastas. Isso não se encaixa bem em uma árvore binária, já que ela só permite dois filhos por nó.

Essa estrutura é eficiente porque:

* Representa bem a hierarquia de pastas e arquivos.
* Permite organizar dados de forma lógica (pastas dentro de pastas).
* Facilita operações como navegação, busca e organização.
* Suporta grande quantidade de elementos por nível.

### Desempenho e operações

* **Busca:** eficiente ao navegar pela hierarquia.
* **Inserção:** adicionar arquivos ou pastas é simples dentro de um nó.
* **Organização:** estrutura natural para sistemas hierárquicos.

### Conclusão

A árvore N-ária é a mais adequada para sistemas de arquivos porque representa de forma natural a estrutura de diretórios usada em sistemas operacionais, garantindo organização e facilidade de navegação.


---


# Parte 4 – Comparação entre Estruturas

| Estrutura   | Nº Máximo de Filhos | Balanceamento                                                  | Complexidade de Busca                | Complexidade de Inserção             | Vantagem Principal                                  | Desvantagem Principal             | Exemplo de Aplicação                          |
| ----------- | ------------------- | -------------------------------------------------------------- | ------------------------------------ | ------------------------------------ | --------------------------------------------------- | --------------------------------- | --------------------------------------------- |
| BST         | 2                   | Não possui balanceamento automático                            | O(log n) melhor caso, O(n) pior caso | O(log n) melhor caso, O(n) pior caso | Simples de implementar                              | Pode ficar desbalanceada          | Árvores de busca básicas                      |
| AVL         | 2                   | Sim. Utiliza rotações para manter o fator de balanceamento     | O(log n)                             | O(log n)                             | Busca altamente eficiente                           | Inserção e remoção mais complexas | Índices de banco de dados                     |
| Rubro-Negra | 2                   | Sim. Utiliza rotações e recoloração de nós                     | O(log n)                             | O(log n)                             | Menos rotações que AVL                              | Implementação mais complexa       | Bibliotecas e estruturas internas de sistemas |
| N-ária      | N                   | Pode ou não possuir balanceamento, dependendo da implementação | O(log n) em versões balanceadas      | O(log n) em versões balanceadas      | Representa hierarquias complexas de forma eficiente | Pode consumir mais memória        | Sistemas de arquivos, menus e taxonomias      |

---


