# Capítulo 10 - Classes

## Organização das classes

Ordem:

- public
- private

### Encapsulamento

Perder o encapsulamento é sempre o último recurso

## As classes devem ser pequenas!

Pequena == pouca responsabilidade

Um bom nome pode limitar de forma perfeita a quantidade de responsabilidades.

Deve-se descrever o que uma classe faz sem as palavras "se", "e", "ou", "mas"

## O princípio da responsabilidade única

A classe deve ter um, e apenas um, motivo para mudar

Caixa de ferramentas com muitas gavetas pequenas e rotuladas ou poucas gavetas grandes com tudo misturado?

## Coesão

Classes devem ter poucas variáveis de instância.
Quanto maior o número dessas variáveis em um método manipula, mais coeso ele é.

O aumento de variáveis de instância pode ser um sinal de que outra classe pode surgir a partir da atual.

Dica: Olhe para as variáveis de instância e veja se não é possível criar outra classe.

### Manutenção de resultados coesos em muitas classes pequenas

Quando as classes perdem coesão, divida-as!

## Como organizar para alterar

Desejamos estruturar nossos sistemas de mode que baguncemos o mínimo possível quando o atualizamos.

## Como isolar das alterações

Dependa de abstrações

Exemplo: Ao invés de depender de `TokioStockExchange`, dependa de `StockExchange`
