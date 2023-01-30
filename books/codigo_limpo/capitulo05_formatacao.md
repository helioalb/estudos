# Capítulo 5 - Formatação

O ideal é que haja uma ferramenta que cuide disso.

## Objetivo da formatação

- A primeira regra de um desenvolvedor profissional é **comunicação**. Não é "fazer funcionar"

## Formatação vertical

+- 500 linhas

### A metáfora do jornal

Um jornal é composto de muitos artigos; a maioria é bastante pequena. Isso facilita a leitura. Nossos códigos deveriam ser assim.

## Espaçamento vertical entre conceitos

Facilita a leitura, visto que os olhos param após cada linha em branco.

## Continuidade vertical

Linhas de código que estão intimamente ligadas devem aparecer verticalmente unidas.

## Distancia vertical

Não se devem separar em arquivos distintos conceitos intimamente relacionados. Esse é um motivo para evitar variáveis protegidas.

### Declaração de variáveis

Deve ser o mais próximo possível de onde será usada.

### Variáveis de instância

Declarar onde todos esperam. Geralmente no início da classe.

### Funções dependentes

Se uma função chama outra, elas devem estar verticalmente próximas.

### Constante em nível apropriado

```java
getPageNameOrDefault(request, "FrontPage");
```

melhor do que

```java
getPageNameOrDefault(request)
```

### Afinidade conceitual

Métodos que realizam coisas muito parecidas com pequenas variações devem permanecer próximas. Exemplo: `assertEquals` do jUnit.

## Formatação horizontal

Deve-se manter as linhas o mais curta possível. Clause guard (não está no livro)

### Espaçamento e continuidade horizontal

Para destacar prioridade: `b*b - 4*a*c`

### Alinhamento horizontal

A não ser que seja assembly ou talvez terraform, não utilize.

### Indentação

Indentação é para destacar hierarquia.
Identar mesmo que seja só uma linha. Ex: if curto;

```java
if (chover)
	return "vai molhar";
```

ao invés de:

```java
if (chover) return "vai molhar";
```

## Regra de equipes

Todos do time devem seguir as mesmas regras.

