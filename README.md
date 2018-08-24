# Regex

Projeto para testes de expressões regulares

Para acessar a página clique [aqui.](https://patrickoliveira94.github.io/regex/)

## Exemplos de expressões regulares

### Extrair CPF:
Target: João Fulano,123.456.789-00,21 de Maio de 1993,(21) 3079-9987,Rua do Ouvidor,50,20040-030,Rio de Janeiro
Pattern 1: \d{3}\.\d{3}\.\d{3}-\d{2}
Pattern 2: \d{3}\.?\d{3}\.?\d{3}[.-]?\d{2}

* Pattern 1: Considera apenas a formatação padrão XXX.XXX.XXX-XX
* Pattern 2: Aceita outras formatações, como: XXX.XXX.XXX.XX, XXXXXXXXXXX, XXXXXXXXX-XX
 
