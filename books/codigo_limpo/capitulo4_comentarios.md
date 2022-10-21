# Capítulo 4 - Comentários

Não insira comentários num código ruim, reescreva-o

Comentários são fracassos.
Comentários frequentemente mentem.
Comentários imprecisos são piores do que nenhum.

"Só se pode encontrar a verdade em um lugar: no código"

## Comentários compensam um código ruim

Gaste energia limpando o código, não comentando.

## Explique-se com o código

Isso:

```java
// Verifica se o funcionário tem direito a todos os benefícios
```

ou isso:

```java
if (employee.isEligibleForFullBenefits())
```

## Comentários bons

### Comentários legais

Onde for possível, coloque uma referência

### Comentários informativos

Comentários em regex

### Explicação da intenção

Explica o motivo

### Esclarescimento

Util para explicar comportamentos de libs externas

### Alerta sobre consequências

```java
// Leva muito tempo para executar
```

### Comentários TODO

Opinião pessoal: Não tem utilidade

### Destaque

Use para destacar algo importante que tem "cara" de irrelevante

### Javadocs em API's públicas


## Comentários ruins

A maioria dos comentários caem nessa categoria

### Murmúrio

Comentários que não dizem nada. Comentários que obrigam o programador a ler muito código para entende-lo

### Comentários redundantes

```java
// Fecha database
db.close();
```

### Comentários enganadores

Diz que o código faz algo que na verdade não faz

### Comentários imperativos

Obrigação de comentar cada método, por exemplo.

### Comentários longos

Ex: changelog no início do arquivo

### Comentários ruidosos

Igual aos redundantes ou desabafos inuteis

### Ruidosos assustadores

```java
// name
private String name;
```

### Evite o comentários se for possível usar uma função ou uma variável

### Marcadores de Posição

```java
// actions /////////////////

// Imagina isso para quem usa leitor de tela
```

### Comentários ao lado de classes de fechamento

```java
while(condicao) {

} // while
```

Isso seria útil para blocos muito extensos. Mas isso é exatamente o que não queremos.

### Créditos e autoria

Use git

### código comentado

```java
public class Author {

    private final Long id;
    private Name name;

    // public static Author load(Long id, String fullName) {
    //     return new Author(id, new Name(fullName));
    // }

    // private Author(final Long id, final Name name) {
    //     this.id = id;
    //     setName(name);
    // }

    public static Author create(String fullName) {
        return new Author(new Name(fullName));
    }
}
```

Ao invés de comentar, remova. Se precisar no futuro, use o git.

### Comentários HTML

Muito confuso para ler

### Informações não-locais

Se tiver que comentar, comente próximo ao código e, além disso, não coloque coisas não relacionadas ao código neste comentário.

### Informações exessivas

```java
RFC 123;

Paragrafo 1: ...
Paragrafo 2: ...
```

### Conexões nada obvias

Comentários que precisariam de comentários para poder ser entendido.

### Cabeçalhos de funções

Uma função deve ser curta e fazer uma única coisa. Se for assim, não precisa de comentário. Um bom nome de função já será o suficiente.

### Javadocs em API's não públicas

Só suja o código
