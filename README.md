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
