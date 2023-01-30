# Capítulo 12 - Emergência

## Obtendo clareza através de um processo de emergência

- Efetuar todos os testes
- Sem duplicação de código
- Expressar o propósito do programador
- Minimizar o número de classes e metodos

## Regra 1 de projetos simples: Efetue todos os testes

Testes conduzem ao SRP e ao DIP

## Regras de 2 a 4 de projetos simples: Refatoração

Só é possível com os testes

### Sem repetição de código

```java
boolean isEmpty() {
    return 0 == size
}
```

privado que fere o SRP

### Expressividade

- Bons nomes
- Testes como documentação
- Uso de nomes padronizados (command, visitor, observer...)
- Mais importante: Tentar a todo momento ser expressivo

## Poucas classes e metodos

Seja pragmático (sempre fazer uma interface para uma classe?)
