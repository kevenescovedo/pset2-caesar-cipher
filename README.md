
# PSET 2 CAESAR
Supostamente, César (sim, aquele César) costumava “criptografar” (ou seja, ocultar de forma reversível) mensagens confidenciais deslocando cada letra em algum número de posições. Por exemplo, ele pode escrever A como B, B como C, C como D, (...), e, agrupando em ordem alfabética, Z como A. E então, para dizer HELLO para alguém, César pode escrever IFMMP. Ao receber essas mensagens de César, os destinatários teriam que “decifrá-las” deslocando as letras na direção oposta no mesmo número de posições.


O segredo desse “criptosistema” dependia apenas de César e dos destinatários saberem de um segredo, o número de posições pelos quais César havia deslocado as letras em suas cartas (por exemplo, 1). Não é particularmente seguro para os padrões modernos, mas, ei, se você é talvez o primeiro no mundo a fazer isso, é bastante seguro!

O texto não criptografado é geralmente chamado de texto simples, o texto criptografado é chamado de texto cifrado e o segredo usado é chamado de chave.

Para ser claro, aqui está como criptografar HELLO com uma chave de 1 resulta em IFMMP:

![Tabela de Pontuação](https://assets.circle.so/iri0abieqj5izjujgb6y3h9tc4tb)

Formalmente, o algoritmo de César criptografa mensagens “girando” cada letra em k posições. Se p é algum texto simples (ou seja, uma mensagem não criptografada), Pi é o i-ésimo caractere em p e k é uma chave secreta um inteiro não negativo), então cada letra, Ci, em o texto cifrado c, é calculado como:
```formula
  Ci= (Pi + k) % 26
```
em que % 26 aqui significa "resto ao dividir por 26". Essa fórmula talvez faça a cifra parecer mais complicada do que é, mas na verdade é apenas uma maneira concisa de expressar o algoritmo com precisão. De fato, para fins de discussão, pense em A (ou a) como 0, B (ou b) como 1, (...), H (ou h) como 7 e Z (ou z) como 25.

em que % 26 aqui significa "resto ao dividir por 26". Essa fórmula talvez faça a cifra parecer mais complicada do que é, mas na verdade é apenas uma maneira concisa de expressar o algoritmo com precisão. De fato, para fins de discussão, pense em A (ou a) como 0, B (ou b) como 1, (...), H (ou h) como 7 e Z (ou z) como 25.
em que % 26 aqui significa "resto ao dividir por 26". Essa fórmula talvez faça a cifra parecer mais complicada do que é, mas na verdade é apenas uma maneira concisa de expressar o algoritmo com precisão. De fato, para fins de discussão, pense em A (ou a) como 0, B (ou b) como 1, (...), H (ou h) como 7 e Z (ou z) como 25.

Suponha que César queira dizer "HI" para alguém de forma confidencial usando, desta vez, uma chave k = 3. Então, seu texto simples, Pi, é "HI", onde o primeiro caractere do texto simples, P1​, é O (ou seja, 7), e o segundo caractere do texto simples, P2​, é i (ou seja, 8). O primeiro caractere do texto cifrado, C1​, é então K, e o segundo caractere do texto cifrado, C2​, é L. Faz sentido?

# Exemplo 

```Run
$ ./caesar 13
plaintext:  hello, world
ciphertext: uryyb, jbeyq
```


