# Uso de IA para geração de cenários de teste

## Função escolhida

`dividir(a, b)`

### Código da função

```python
def dividir(a, b):
    return a / b
```

## Prompt utilizado

```text
Atue como um professor de Teste de Software.

Tenho a seguinte função Python:

def dividir(a, b):
    return a / b

Quero criar testes unitários usando unittest.

Liste cenários de teste para essa função, incluindo:

- divisão exata;
- divisão com resultado decimal;
- divisão de número negativo;
- divisão de zero por outro número;
- divisão por zero.

Para cada cenário, informe:
- nome do cenário;
- entrada;
- resultado esperado;
- tipo do cenário: caso normal, caso de borda ou caso de erro.

Não gere código ainda.
```

## Cenários sugeridos pela IA

| ID  | Cenário                  | Entrada         | Resultado Esperado | Tipo   |
| --- | ------------------------ | --------------- | ------------------ | ------ |
| T01 | Divisão exata            | dividir(10, 2)  | 5                  | Normal |
| T02 | Divisão decimal          | dividir(5, 2)   | 2.5                | Normal |
| T03 | Divisão com negativo     | dividir(-10, 2) | -5                 | Normal |
| T04 | Zero dividido por número | dividir(0, 5)   | 0                  | Borda  |
| T05 | Divisão por zero         | dividir(10, 0)  | ZeroDivisionError  | Erro   |

## Análise dos cenários

Após analisar os cenários sugeridos pela IA, todos foram aceitos. Os testes cobrem situações comuns de uso da função, casos de borda e tratamento de erro. Não foi necessário remover ou alterar nenhum cenário, pois todos estavam compatíveis com o comportamento esperado da função.

## Código final dos testes

```python
def test_dividir_com_varios_casos(self):
    casos = [
        (10, 2, 5),
        (5, 2, 2.5),
        (-10, 2, -5),
        (0, 5, 0),
    ]

    for a, b, esperado in casos:
        with self.subTest(a=a, b=b):
            self.assertEqual(dividir(a, b), esperado)

def test_dividir_por_zero(self):
    with self.assertRaises(ZeroDivisionError):
        dividir(10, 0)
```

## Resultado da execução

```bash
python -m unittest discover

----------------------------------------------------------------------
Ran 10 tests in 0.000s

OK
```
