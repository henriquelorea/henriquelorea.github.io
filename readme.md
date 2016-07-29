# henriquelorea.github.io

Página pessoal de **Henrique Lorea**. Bem-vindos amiguinhos!!!111

Este é o readme.md, que é _muito importante_ ~~em geral, porque esse caso não serve pra nada~~.
Afinal o que **_interessa mesmo_** nesse repo está no [site gerado por ele](https://henriquelorea.github.io).

- E se eu der add and commit and push sem salvar o arquivo?
    - Ele diz que não tem nada para commit.

Vamos estudar NA PRÁTICA como funciona esse tal de `git` e markdown:

    Na verdade aqui eu to testando como escrever um pedaço de
    código usando o markdown. Se é pra escrever dentro de uma
    linha (como git ali em cima), é só colocar o texto corres-
    pondente entre crases. Se é pra fazer um box como esse,
    as opções são

    1. Escrever o código entre ````três ou quatro crases````.
       É o que ele chama de code fencing.

    2. Indentar o código com quatro espaços, que é como eu
       fiz aqui. Aparentemente não existe bloco de código
       dentro de bloco de código porque o emprego do code
       fencing ali em cima resultou inócuo.

    Cabe ressaltar que este bloco de código aqui tem caráter
    experimental para testar o recurso, porque dentro dele tem
    um monte de bobagem menos código.

```python
def bla():
    # uma coisa interessante do code fencing:
    return 'ele tem syntax highlighting se a linguagem for declarada'
```

Voltamos à programação normal. O fluxo para subir (o conceito
não é subir, mas por enquanto vai assim) um arquivo para o
github é `add` -> `commit` -> `push`. Aí eu resolvi testar o que
faria o `remove`. Eis que ele aparentemente apagou o arquivo.

Frente ao cagaço de perder este arquivo querido, fui investigar como recuperá-lo. Eu não tinha executado o `commit` ainda quando ele desapareceu.

O que coube fazer foi:

1. `git status`: mostrou o arquivo removido a ser committed e apontou a solução: `use "git reset HEAD <file>..." to unstage`.

2. `git reset HEAD .`: tirou do HEAD ou do stage o tal arquivo removido. O `.` funciona como um `*.*` no linux. Head e/ou stage são coneitos importantes que eu quero/vou estar estudando logo.

3. `git status` de novo: mostrou o arquivo 'not staged to commit' e sugerindo duas opções:
    * um comando para despachar para o stage de novo com `add` ou `rm`;
    - ou `git checkout -- <file>...` para terminar de recuperar o arquivo. Essa segunda opção foi a que eu usei e tudo voltou a ser como dantes no quartel de abrantes.

Cenas dos próximos capítulos: ques porra é essa de head e stage?
