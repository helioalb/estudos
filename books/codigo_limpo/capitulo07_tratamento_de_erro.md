# Capítulo 7 - Tratamento de Erro

- Se o tratamento de erros obscurecer a lógica, está errado.

## Use exceções em vez de retornar códigos

- O retorno de código obriga o cliente a fazer tratamento de erros.

## Crie primeiro a sua estrutura `try-catch-finally`

- O `try-catch` é semelhante a uma transação. Após essa "transação" o programa deve continuar consistente.
- Crie primeiro o teste que força a exception.

## Use exceções não verificadas

- Isso quebra o `open-closed`. Se um método mais interno lançar uma exception verificada, todos acima precisam tratá-la.

## Forneça exceções com contexto

- No `catch` informe tudo o que for necessário para que outras pessoas saibam, o que, por que e onde o problema aconteceu.

## Defina as classes de exceções segundo as necessidades do chamador

- Faça wrappers para api de terceiros

## Defina o fluxo normal

- Special case pattern

```java
public class PerDiemMealExpenses implements MealExpenses {
	public Double getTotal() {
		var ajudaDeCusto = 29.50;
		return ajudaDeCusto;
	}
}
```

## Não retorne null

- Retornar `null` joga problemas para o chamador.
- Ou lance uma exceção ou retorne um special case pattern.

## Não passe null
