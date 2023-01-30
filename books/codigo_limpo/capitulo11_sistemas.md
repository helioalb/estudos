# Capítulo 11 - Sistemas

"Complexidade mata"

## Como você construiria uma cidade?

- Abastecimento de água
- Energia
- Transito
- Segurança
- Educação

## Separe a construção e o uso de um sistema

Construção != Utilização

### Separação do main

Todos os objetos (implementações/adaptadores) são construídos e passados ao aplicativo
O main conhece os objetos e aplicativo, o aplicativo não conhece o main.

Exemplo: Passo um logger para o app.

### Factories

Passamos factories para que o aplicativo possa criar objetos em tempo de execução.

### Injeção de dependência

Via construtor ou via setter

## Desenvolvimento gradual

Arquiteturas podem crescer gradualmente se mantivermos uma separação devida de preocupações.

## Preocupações transversais

Tratar como uma exceção será exibida para o usuários é uma preocupação transversal. o ControllerAdvice é um exemplo disso.

O ControllerAdvice fica apartado da regra de negócios.

Para separar as coisas usa-se programação orientada a aspecto.
