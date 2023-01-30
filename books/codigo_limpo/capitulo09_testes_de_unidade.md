# Capítulo 9 - Testes de unidade

## As três leis do TDD

- Não escrever código de produção antes de existir o teste
- Não se deve escrever o próximo teste unitário antes do primeiro passar
- Não escrever mais código do que o teste exige

Teste e código devem ser escritos juntos

## Como manter os testes limpos

Quando o código muda, o teste também muda. Se a qualidade do teste é ruim, isso vai impactar na manutenbilidade do código.

É preciso manter o código de teste tão limpo quanto o código de produção.

## Os testes habilitam as "-idades"

Os testes são quem mantem os códigos flexiveis

## Testes limpos

Tem que ser legível. Detalhes devem ser abstraídos.

## Linguagem de testes específica ao domínio

Crie funções utilitárias que abstraem as chamadas de API's do código.

O ambiente de teste pod eusa rmais recursos. Isso, em produção talvez necessite ser tratado de maneira diferente.

## Uma afirmação por teste

É uma orientação, mas em alguns casos pode ser burlada.

## Um único conceito por teste

Exemplo `addMonth`

- para mês com 28 dias
- para mês com 29 dias
- para mês com 30 dias
- para mês com 31 dias

## F.I.R.S.T

**Fast** - Se os testes são lentos, evitamos de executá-los.
**Independent** - Um teste não deve depender de outro.
**Repeatable** - Deve ser reproduzível em qualquer ambiente (inclusive num ambiente sem internet)
**Self-validating** - Deve ser sucesso ou falha - Não podemos ficar analisando um log, por exemplo.
**Timely** - Tem que ser criado antes do código
