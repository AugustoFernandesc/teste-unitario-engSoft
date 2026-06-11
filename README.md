# Teste Unitário com Python e PyUnit

Este projeto foi desenvolvido como atividade prática da aula de testes unitários com Python e PyUnit, utilizando o módulo `unittest`.

## Objetivo

O objetivo da atividade é criar uma calculadora simples em Python e implementar testes unitários para verificar se cada função está funcionando corretamente.

## Estrutura do projeto

```text
teste-unitario-python/
│
├── calculadora.py
├── test_calculadora.py
└── README.md
```

## Funções implementadas

No arquivo `calculadora.py`, foram criadas as seguintes funções:

- `somar(a, b)`: retorna a soma de dois números;
- `subtrair(a, b)`: retorna a subtração de dois números;
- `multiplicar(a, b)`: retorna a multiplicação de dois números;
- `dividir(a, b)`: retorna a divisão de dois números;
- `potencia(a, b)`: retorna a potência de um número;
- `calcular_media(lista)`: retorna a média dos números de uma lista.

## Testes implementados

No arquivo `test_calculadora.py`, foram criados testes para verificar:

- soma de números positivos, negativos e zero;
- subtração com resultado positivo, negativo e zero;
- multiplicação com números positivos, zero e negativos;
- divisão com resultado inteiro e decimal;
- divisão por zero, verificando se gera `ZeroDivisionError`;
- potência de números;
- cálculo de média com inteiros;
- cálculo de média com decimais;
- cálculo de média com apenas um número;
- cálculo de média com lista vazia, verificando se gera `ValueError`.

## Como executar os testes

No terminal, dentro da pasta do projeto, execute:

```bash
python -m unittest test_calculadora.py
```

Ou:

```bash
python -m unittest discover
```

## Resultado esperado

Se tudo estiver correto, o terminal deverá mostrar uma mensagem semelhante a:

```bash
Ran 10 tests in 0.001s

OK
```

Isso significa que todos os testes foram executados e passaram corretamente.

## Conclusão

A atividade permitiu colocar em prática os conceitos básicos de testes unitários utilizando Python e o módulo unittest. Foram criadas funções simples de uma calculadora e desenvolvidos testes para verificar se os resultados obtidos estavam corretos.

Além dos casos mais comuns, também foram testadas situações especiais, como divisão por zero e cálculo da média de uma lista vazia. Com isso, foi possível compreender melhor a importância dos testes automatizados para garantir a qualidade e a confiabilidade do software.
