# 📝 Guia de Markdown para GitHub

Resumo do que aprendi sobre **Markdown**, baseado nas aulas e no *Manual do Markdown para GitHub* do prof. Gustavo Guanabara (Curso em Vídeo), com minhas anotações e alguns extras.

## 📑 Sumário

1. [O que é Markdown?](#-o-que-é-markdown)
2. [Formatação de texto](#-formatação-de-texto)
3. [Títulos e linhas horizontais](#-títulos-e-linhas-horizontais)
4. [Listas](#-listas)
5. [Imagens e links](#-imagens-e-links)
6. [Trechos de código](#-trechos-de-código)
7. [Citações](#-citações)
8. [Menções a usuários e issues](#-menções-a-usuários-e-issues)
9. [Escapando símbolos](#-escapando-símbolos)
10. [Emojis](#-emojis)
11. [Tabelas](#-tabelas)
12. [Extras úteis](#-extras-úteis)
13. [Referências](#-referências)

---

## 📖 O que é Markdown?

Markdown é uma **linguagem de marcação** (assim como o HTML), mas bem mais simples: em vez de tags como `<body>`, usa símbolos do teclado para formatar o texto, o que deixa o conteúdo fácil de ler mesmo sem ser renderizado.

- Criada em **2004** por **John Gruber** e **Aaron Swartz**.
- Arquivos usam a extensão `.md` ou `.markdown`.
- No GitHub é usada em **README.md**, **issues**, **pull requests** e comentários.
- Foi padronizada pelo **CommonMark**, adotado por vários softwares e sites.

> 💡 Dica do professor: pratique bastante, adicionando recursos ao `README.md` dos seus repositórios.

---

## ✍️ Formatação de texto

| Efeito | Como escrever | Resultado |
| :--- | :--- | :--- |
| Itálico | `*texto*` ou `_texto_` | *texto* |
| Negrito | `**texto**` ou `__texto__` | **texto** |
| Riscado | `~~texto~~` | ~~texto~~ |
| Negrito + itálico | `***texto***` ou `__*texto*__` | ***texto*** |

> ⚠️ **Importante:** não coloque espaços entre os símbolos e o texto que eles formatam. `** texto **` não funciona.

---

## 🔠 Títulos e linhas horizontais

### Títulos

Use de `#` até `######` (6 níveis), sempre com **um espaço** depois do símbolo. É parecido com `<h1>` até `<h6>` do HTML.

```markdown
# Título nível 1
## Título nível 2
### Título nível 3
#### Título nível 4
##### Título nível 5
###### Título nível 6
```

### Linha horizontal

Três traços `---` ou três asteriscos `***` (em uma linha separada) criam uma linha que corta a página de um lado ao outro.

```markdown
Texto de cima

---

Texto de baixo
```

---

## 📋 Listas

### Lista numerada

Comece a linha com um número seguido de ponto. **Não precisa colocar os números em ordem**: o GitHub numera sozinho, e o primeiro número define onde a lista começa.

```markdown
1. Brasil
1. Alemanha
5. França
0. Bélgica
```

Resultado:

1. Brasil
1. Alemanha
5. França
0. Bélgica

**Sub-itens:** coloque **3 espaços** antes do marcador. Dependendo do nível, o GitHub mostra o sub-item com outro estilo de numeração (como `i.`, `ii.`).

```markdown
1. Item
   1. Sub-item
   1. Outro sub-item
2. Outro item
```

### Lista com marcadores

Use `*`, `-` ou `+` seguido de **espaço** (não precisa de número). Para sub-itens, é o mesmo esquema: espaços antes do marcador.

```markdown
* Opção 1
* Opção 2
   * Opção 3 (sub-item)
- Opção 4
```

Resultado:

* Opção 1
* Opção 2
   * Opção 3 (sub-item)
- Opção 4

### Lista de tarefas

Use `- [ ]` (desmarcado) e `- [x]` (marcado). **Atenção:** é preciso haver um **espaço dentro dos colchetes** (`[ ]`); `[]` sem espaço não funciona.

```markdown
- [ ] Criar a página principal
- [ ] Criar a página da loja
- [x] Finalizar a reunião com o cliente
- [x] Receber pagamento
```

Resultado:

- [ ] Criar a página principal
- [ ] Criar a página da loja
- [x] Finalizar a reunião com o cliente
- [x] Receber pagamento

> No GitHub (issues e PRs) dá para marcar e desmarcar as caixinhas direto na tela, sem editar o texto.

---

## 🖼️ Imagens e links

### Imagens

```markdown
![Descrição da imagem](https://endereco-da-imagem.com/logo.png)
```

A descrição (texto alternativo) vai entre colchetes e o endereço entre parênteses. É o mesmo formato do link, só que com `!` na frente.

> 💡 No editor de comentários do GitHub, também dá para **arrastar e soltar** a imagem na caixa de texto ou anexar pelo disco local. O GitHub gera o código da imagem automaticamente.

### Links

```markdown
[Texto que vira link](https://github.com)
```

O texto do hyperlink vai entre colchetes e a URL entre parênteses. O editor do GitHub também tem um botão de **inserir link** que preenche isso para você.

---

## 💻 Trechos de código

### Comando isolado (inline)

Envolva o comando com **uma crase** de cada lado. Fica com fonte monoespaçada e fundo cinza.

```markdown
Use o comando `document.getElementById()` para selecionar um elemento.
```

Resultado: Use o comando `document.getElementById()` para selecionar um elemento.

### Bloco de código (várias linhas)

Envolva o código com **três crases** (` ``` `) antes e depois. Se você escrever o nome da linguagem logo após as crases de abertura, o GitHub aplica **destaque de sintaxe** (cores).

````markdown
```python
num = int(input('Digite um valor: '))
if num % 2 == 0:
    print(f'O valor {num} é PAR')
else:
    print(f'O valor {num} é ÍMPAR')
```
````

Resultado:

```python
num = int(input('Digite um valor: '))
if num % 2 == 0:
    print(f'O valor {num} é PAR')
else:
    print(f'O valor {num} é ÍMPAR')
```

---

## 💬 Citações

Use `>` no início da linha para citar mensagens ou trechos. É muito usado para responder alguém em uma issue.

```markdown
Como **Steve Jobs** disse uma vez:

> Decidir o que não fazer é tão
> importante quanto decidir
> o que fazer

Bela frase!
```

Resultado:

Como **Steve Jobs** disse uma vez:

> Decidir o que não fazer é tão
> importante quanto decidir
> o que fazer

Bela frase!

---

## 🔗 Menções a usuários e issues

### Mencionar usuários

Use `@` seguido do nome de usuário. Se o perfil existir, vira um link e a pessoa recebe uma notificação.

```markdown
Durante o curso, usamos o perfil @gafanhotos para exercitar Git e GitHub.
```

### Mencionar issues e pull requests

Use `#` seguido do número, **sem espaço**. O GitHub cria um link para a issue ou PR do repositório.

```markdown
Analisando a Issue #3, vamos rever o que foi indicado pelo usuário.
```

---

## 🚫 Escapando símbolos

Para mostrar o símbolo **sem** o efeito de formatação, coloque uma barra invertida `\` antes dele.

```markdown
Podemos criar títulos usando \## antes do texto
Podemos criar citações usando \> antes do conteúdo
Podemos adicionar imagens usando \!\[descrição]\(endereço)
```

Resultado:

Podemos criar títulos usando \## antes do texto
Podemos criar citações usando \> antes do conteúdo
Podemos adicionar imagens usando \!\[descrição]\(endereço)

---

## 😄 Emojis

Escreva o código do emoji entre dois-pontos `:`.

```markdown
Boas iniciativas merecem aplausos :clap:
Fatos importantes merecem atenção :eyes:
Momentos difíceis requerem força :muscle:
Mensagens bem escritas merecem um like :+1:
```

Resultado:

Boas iniciativas merecem aplausos :clap:
Fatos importantes merecem atenção :eyes:
Momentos difíceis requerem força :muscle:
Mensagens bem escritas merecem um like :+1:

📚 Lista completa de códigos: [emoji-cheat-sheet (ikatyang)](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)

### ⚠️ Emojis no título de issues

Códigos como `:hand:` **funcionam em comentários e descrições**, mas **não nos títulos das issues**. Isso acontece porque o título é texto puro: o `:codigo:` é um atalho que o GitHub converte só ao renderizar o Markdown, e o título não passa por essa conversão.

O que funciona nos títulos é colar o **emoji de verdade** (que é um caractere Unicode, como uma letra), copiando de sites como [emojipedia.org](https://emojipedia.org). Ou seja, sua suspeita estava certa: o que vale é o próprio caractere Unicode do emoji, e não o atalho.

---

## 📊 Tabelas

Use **barras em pé** `|` para separar as colunas e **traços** `-` para separar o cabeçalho dos dados.

1. **Primeira linha:** nomes das colunas (aparecem em negrito)
2. **Segunda linha:** separador, com no mínimo três traços `---` por coluna
3. **Demais linhas:** os valores

```markdown
| Num | Nome    | Nota |
| --- | ------- | ---- |
| 1   | Gustavo | 8,5  |
| 2   | José    | 10,0 |
| 3   | Maria   | 9,0  |
```

Resultado:

| Num | Nome    | Nota |
| --- | ------- | ---- |
| 1   | Gustavo | 8,5  |
| 2   | José    | 10,0 |
| 3   | Maria   | 9,0  |

### Alinhamento das colunas

Os dois-pontos `:` na linha separadora definem o alinhamento:

| Separador | Alinhamento |
| :---: | :--- |
| `---` | Padrão (esquerda) |
| `:---` | Esquerda |
| `:---:` | Centralizado |
| `---:` | Direita |

```markdown
| Ano  | Curso       | Professor         | Aulas |
| :---: | ---: | :--- | :---: |
| 2013 | HTML+CSS+JS | Gustavo Guanabara | 36    |
| 2018 | Hardware    | Alfredo Jr        | 28    |
```

| Ano  | Curso       | Professor         | Aulas |
| :---: | ---: | :--- | :---: |
| 2013 | HTML+CSS+JS | Gustavo Guanabara | 36    |
| 2018 | Hardware    | Alfredo Jr        | 28    |

---

## ⭐ Extras úteis

### Quebra de linha

Para pular linha dentro do mesmo parágrafo, termine a linha com **dois espaços** ou use uma barra invertida `\`. Uma linha em branco cria um novo parágrafo.

### Blocos de destaque (alertas)

O GitHub tem alertas coloridos usando citações:

```markdown
> [!NOTE]
> Informação útil.

> [!TIP]
> Uma dica.

> [!IMPORTANT]
> Algo que não pode ser ignorado.

> [!WARNING]
> Cuidado com isso.

> [!CAUTION]
> Pode causar problemas sérios.
```

> [!NOTE]
> Informação útil.

> [!TIP]
> Uma dica.

> [!IMPORTANT]
> Algo que não pode ser ignorado.

> [!WARNING]
> Cuidado com isso.

> [!CAUTION]
> Pode causar problemas sérios.

### Seção que expande e recolhe

```markdown
<details>
<summary>Clique para ver mais</summary>

Conteúdo escondido aqui.

</details>
```

<details>
<summary>Clique para ver mais</summary>

Conteúdo escondido aqui.

</details>

### Imagem com tamanho definido

O Markdown puro não controla o tamanho, mas o GitHub aceita HTML:

```markdown
<img src="https://endereco-da-imagem.com/logo.png" width="200" alt="Descrição">
```

### Comentário invisível

```markdown
<!-- Este texto não aparece na página renderizada -->
```

### Link para outra parte do mesmo documento

Os títulos geram âncoras automaticamente (minúsculas, espaços viram `-`):

```markdown
[Ir para Tabelas](#-tabelas)
```

---

## 📚 Referências

- [Manual do Markdown para GitHub: prof. Gustavo Guanabara (Curso em Vídeo)](https://github.com/gustavoguanabara/)
- [CommonMark](https://www.commonmark.org)
- [Markdown Guide](https://www.markdownguide.org)
- [Mastering Markdown (GitHub)](https://guides.github.com/features/mastering-markdown/)
- [Documentação oficial do GitHub sobre sintaxe de escrita](https://docs.github.com/pt/get-started/writing-on-github)
- [Emoji Cheat Sheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)
- [Emojipedia](https://emojipedia.org)
