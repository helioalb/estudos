# Capítulo 6 - Objetos e estrutura de dados

Declaramos variáveis como privadas para que ninguém de fora da class dependa delas.

## Abstração de dados

- A classe deve fornecer abstrações, não seus dados internos.
- Abstrações exigem regra de acesso.
- É preferível não expor os dados da classe.
- setters precisam validar.

## Antissimetria data/objeto

- data (estrutura de dados) expõe dados para funções os operarem.
- Objeto encapsula o comportamento dentro de si.
- Estrutura de dados permitem que se adicionem funções que operem sobre ela de maneira fácil - 1, 2, 3 funções podem operar a mesma estrutura de dados. Exemplo: `func1(data)`, `func2(data)`, `func3(data)` .
- Objetos podem ganhar novas formas de maneira fácil. Mas se os objetos que compartilham a mesma interface ganham um novo método, todos os objetos precisam implementar esse método.
No exemplo abaixo, `getPLR()` deve ser implementado em todas as classes:

```java
interface Funcionario {
  double getSalario();
  double getDecimoTerceiro();
  double getPLR();
}

class Supervisor implements Funcionario {
  double getSalario() {
    return salario + bonificacoes;
  }

  getDecimoTerceiro() {
    return salario/12 * mesesTrabalhados;
  }
}

class Empregado implements Funcionario {
  double getSalario() {
    return salario;
  }

  getDecimoTerceiro() {
    return salario/12 * mesesTrabalhados;
  }
}

class Estagiario implements Funcionario {
  double getSalario() {
    return salario;
  }

  getDecimoTerceiro() {
    return 0;
  }
}
```
- Estrutura de dados vs OO: O que é fácil para um é difícil para o outro.

### A lei de Demeter

- "fale apenas com conhecidos, não com estranhos"
- Não pode acessar dados internos de objetos. De estrutura de dados pode

Acesso a dados de estrutura de dados se parecem com isso.

```java
obj.prop.prop_da_prop.prop_da_prop_da_prop;
```

Acesso a dados internos de objetos se parecem com:

```java
obj.prop().prop_da_prop().prop_da_prop_da_prop();
```

### Train Wrecks

```java
obj.one().two().three();
```

### Híbridos

Meio estrutura de dados, meio objeto. setter + getters + comportamentos.

## Objetos de transferencia de dados (DTO)

São estruturas de dados (as vezes mascaradas com setters e getters).

### Active record

DTO com `save()` e `find()`.

O author desencoraja ter comportamentos nesses objetos. Eu descordo.
