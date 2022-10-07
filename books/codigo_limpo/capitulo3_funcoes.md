# Capitulo 3 - Funções

## Pequenas

- 20 linhas
- 150 colunas

## Blocos e Indentação

Nível de indentação: 1 (no máximo, 2)

## If deve ter somente uma linha no bloco

## Faça apenas uma coisa

As funções devem fazer uma coisa. Devem fazê-la bem. Devem fazer apenas ela.

## Seções dentro de funções

:warning: Indício obvio de estar fazendo mais de uma coisa

## Um nível de abstração por função

```java
void exemplo() {
	notifyUser(); //Alto nível

	StringBuffer sb; //Baixo nível
	sb.append("ok");
}
```

## Ler um código de cima para baixo: Regra Decrescente

Cada função chama uma próxima que estará num nível de abstração mais baixo.

## Instruções `switch`

Tente usar junto com polimorfismo

## Use nomes descritivos

- `SetupTearDownIncluder` ao invés de `testableHTML`
- "Você sabe que está criando um código limpo quando cada rotina que você lê é como você esperava"
- Não tem problema se o nome for extenso

## Parametros de funções

zero, 1(monade), 2 (diade). Mais que isso, não.

### Formas monades comuns

Pergunta ou transformação (adapta)

```java
boolean fileExists("myFile");
```

```java
String buildTag("CPU");
```

Evitar coisas do tipo:

```java
void includeSetupInto(Page page);
```

### Funções díades

Tente evitar ou, quando possível, transformar numa monade.

### Tríades

Evite

## Objetos como parametros

**Sim**

```java
makeCircle(Point center, double radios);
```

**Não**

```java
makeCircle(double x, double y, double radios);
```

Usar objetos nesses casos não é uma trapaça.

## Verbos e palavras-chave

```javascript
verbo(substantivo);
```

```javascript
write(name);
```

```javascript
writeField(name);
```

## Evite efeitos colaterais

```javascript
checkPassword(username, password) {
	// código
	this.session.initialize();
	// código
}
```

## Parametros de saída

Qualquer coisa que lhe force a verificar a assinatura da função é equivalente a uma releitura. Isso é uma interrupção de raciocínio e deve ser evitado.

Exemplo:

```java
void appendFooter(Report report);
```

alternativa

```java
report.appendFooter();
```

De maneira geral devem-se evitar parâmetros de saída.

## Separação comando-consulta

As funções devem fazer algo ou responder algo, **não** ambos.

## Prefira exceções a retorno de código de erro.

## Extraia os blocos try/catch

Ao invés de:

```java
try {
	deletePage(page);
	outraCoisa();
} catch (e) {
	// log
}
```

faça:

```java
delete(page) {
	try {
		// código
	} catch (e) {
		// log
	}
}
```

## Tratamento de erro é uma coisa só

A primeira linha da função é `try`. E não deve ter mais nada além disso.

## Evite repetição

A duplicação pode ser a raiz de todo o mal no software

## Programação estruturada (dijkstra)

Uma entrada e uma saída.
Usando funções pequenas, não é necessário.
