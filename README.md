# Sistema de Cálculo de Impostos

Projeto Java orientado a objetos que calcula o imposto devido por contribuintes do tipo pessoa física e empresa, aplicando regras diferentes por meio de herança e polimorfismo.

## Funcionalidades
- Cadastro de múltiplos contribuintes via terminal
- Identificação do tipo de contribuinte (`i` para pessoa física e `e` para empresa)
- Cálculo de imposto por contribuinte com regras específicas para cada classe
- Exibição do imposto pago por cada contribuinte
- Exibição do total geral de impostos arrecadados

## Exemplo de execução
```text
Entre com o numero de contribuentes: 2

Contribuente #1 dados:
Individual ou Empresa (i/e)?:  i
Nome: Alex
Renda anual: 50000.00
Gastos com saúde: 2000.00

Contribuente #2 dados:
Individual ou Empresa (i/e)?:  e
Nome: SoftTech
Renda anual: 400000.00
Numero de funcionarios: 25

IMPOSTOS PAGOS:
Alex: $ 11500.00
SoftTech: $ 56000.00

TOTAL DE IMPOSTOS: $ 67500.00
```

## Regras de cálculo
### Pessoa física (`Individual`)
- Renda anual menor que `20000.00`: imposto base de `15%`
- Renda anual a partir de `20000.00`: imposto base de `25%`
- Desconto de `50%` dos gastos com saúde sobre o imposto base
- Imposto mínimo final: `0.00`

### Empresa (`Company`)
- Mais de 10 funcionários: imposto de `14%` da renda anual
- Até 10 funcionários: imposto de `16%` da renda anual

## Tecnologias
- Java
- Programação Orientada a Objetos (POO)

## Como executar
1. Clone o repositório
2. Compile os arquivos:
   ```bash
   javac src/application/Program.java src/entities/*.java
   ```
3. Execute o programa:
   ```bash
   java -cp src application.Program
   ```
