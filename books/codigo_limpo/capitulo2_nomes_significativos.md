# Capitulo 2 - Nomes significativos

## Use nomes que revelem seu propósito

- Por que existe?
- O que faz?
- Como é usado?

O contexto deve estar explicito no código.

```java
hipotenusaAoQuadrado = catetoAdjacenteAoQuadrado + catetoOpostoAoQuadrado;
```

é melhor do que

```java
a = b + c;
```

## Evite informações erradas

- Evite nomes parecidos. Exemplo: `getAccount`, `getAAcount`
- Faça distinção clara entre os nomes:
   ```java
   copy(char source, char destination);
   ```
   melhor que

   ```java
   copy(char a1, char a2)
   ```
- Evite diferenciaa a palavra mas deixar o mesmo significado. Exemplo: `Product`, `ProductData`, `ProductInfo`. Qual a diferença?

Em que `NameString` é melhor que `Name`?

Se aparecer na IDE `getAccount()` e `getAccountInfo`, qual usar?

Não dá pra saber. A palavra foi diferenciada, mas tem o mesmo significado.

Faça a distinção de nomes de forma que o leitor compreenda as diferenças.

## Use nomes pronunciáveis

xptoyz() **NÃO**

## Use nomes passíveis de busca

Variável `e`. Numa busca irá aparecer centenas de vezes.

## Evite codificações

Não use `PhoneNumber` ou `PhoneString`. Use `Phone`.

Não use `m_age`. Use `age` (`m_`, nesse caso seria uma codificação para "variável membro da classe")

Não use `I`(de interface). `Account` é melhor do que `IAccount`.

## Evite mapeamento mental

`r` == `result`

`c` == `car`

`s` == `segment`

## Nomes de classes

Evite `Processor`, `Manager`, `Data`. Deve ser um substantivo. **Nunca** um verbo.

### Nomes de métodos

Devem conter verbos

Quando hover overload de contrutor, use _factory methods_

```java
Complex.fromRealNumber(23.0);
```

melhor que

```java
new Complex(23.0);
```

Dica: Deixe os contrutores privados.

## Não colocar nomes engraçadinhos

~~getBufunfa()~~ `getMoney()`

## Selecione uma palavra por conceito

Exemplo: Ou `get` ou `fetch` ou `retrieve`

## Não faça trocadilhos

Exemplo: `add("sufixo")` é usado para adicionar sufixo em palavras. O mesmo `add` não deve ser usado para inserir um elemento em uma lista. Neste caso use, por exemplo, `insert(item)`.

## Use nomes a partir do Domínio da Solução

- `AccountVisitor`
- `JobQueu`
- `WheaterObserver`

## Use nomes de domínios do problema

DDD

### Adicione um contexto significativo

Variáveis com contexto obscuro
```java
private void printGessStatistics(char candidate, int count) {
    String number;
    String verb;
    String pluralModifier;
    if (count == 0) {
        number = "no";
        verb = "are";
        pluralModifier = "s";
    } else if (count == 1) {
        number = "1";
        verb = "is";
        pluralModifier = "";
    } else {
        number = Integer.toString(count);
        verb = "are";
        pluralModifier = "s";
    }
    String guessMessage = String.format(
        "There %s %s %s%s", verb, number, candidate, pluralModifier);
    print(guessMessage);
}
```

Variáveis possuem contexto

```java
public class GuessStatisticsMessage {
    private String number;
    String verb;
    String pluralModifier;
 
    public String make(char candidate, int count) {
        createPluralDependentMessageParts(count);
        return String.format(
        "There %s %s %s%s", verb, number, candidate, pluralModifier); 
    }

    private void createPluralDependentMessageParts(int count) {
        if (count == 0) {
            thereAreNoLetters();
        } else if (count == 1) {
            thereIsOneLetter();
        } else {
            thereAreManyLetters()
        }
    }

    private void thereAreNoLetters() {
        number = "no";
        verb = "are";
        pluralModifier = "s"; 
    }

    private void thereIsOneLetter() {
        number = "1";
        verb = "is";
        pluralModifier = ""; 
    }

    private void thereAreManyLetters() {
        number = Integer.toString(count);
        verb = "are";
        pluralModifier = "s"; 
    }
}
```

## Não adicione contexto desnecessário

Para fins de exemplo: "Gas station deluxe" GSD.

Não faça `GSDAccount`. Faça `Account`

|Sim|Não|
|-|-|
|`MAC`|`MACAddress`|
|`URL`|`URLAddress`|
