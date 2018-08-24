# Regex

Projeto para testes de expressões regulares

Para acessar a página clique [aqui.](https://patrickoliveira94.github.io/regex/)

## Quantifiers (Quantificadores)

```sh 
? zero ou uma vez.
```

```sh 
* zero ou mais vezes.
```

```sh 
+ uma ou mais vezes.
```

```sh 
{n} exatamente n vezes.
```

```sh 
{n,} no mínimo n vezes.
```

```sh 
{n,m} no mínimo n vezes, no máximo m vezes.
```

## Character Classes (Classes de caracteres)

```sh 
[A-Z] significa de A até Z, sempre maiúscula.
```

```sh 
[a-z] significa de a até z, sempre minúscula,
```

```sh 
[A-Za-z] significa A-Z ou a-z.
```

```sh 
[abc] significa a, b ou c.
```

```sh
\s whitespace (espaço em branco, tab...)
```

```sh
\w wordchar (qualquer letra maiúscula ou minúscula ou número)
```

## Anchors (Âncoras) - Principais, mais usadas:

```sh
\b word boundary
```

```sh
^ início do alvo
```

```sh
$ fim do alvo
```

## Groups (Grupos):

```sh
(\w+) grupo de word chars
```

```sh
(\w+)? grupo opcional
```

```sh
(?:\w+) non-capturing group
```

## Exemplos de expressões regulares

```sh
Target: João Fulano,123.456.789-00,21 de Maio de 1993,(21) 3079-9987,Rua do Ouvidor,50,20040-030,Rio de Janeiro
```

### Extrair CPF:

```sh
Pattern 1: \d{3}\.\d{3}\.\d{3}-\d{2}
```

```sh
Pattern 2: \d{3}\.?\d{3}\.?\d{3}[.-]?\d{2}
```

* **Pattern 1:** Considera apenas a formatação padrão XXX.XXX.XXX-XX
* **Pattern 2:** Aceita outras formatações, como: XXX.XXX.XXX.XX, XXXXXXXXXXX, XXXXXXXXX-XX


### Extrair data por extenso:

```sh
Pattern: [0123]?\d\s+de\s+[A-Z][a-zç]{1,8}\s+de\s+[12]\d{3}
```
 
### Extrair palavra especifica de uma string:

```sh
Pattern: \bde\b
```

### Extrair link começando com http e terminando com .html:

```sh
Target: http://patrickoliveira.me/index.html
```

```sh
Pattern: ^http.+\.html$
```

### Selecionar texto de um h1 com grupos:

```sh
Target: <h1 class="text-left">Expressões regulares</h1>
```

```sh
Pattern: <h1.+?>([\w\sõãí.]+)</h1>
```
