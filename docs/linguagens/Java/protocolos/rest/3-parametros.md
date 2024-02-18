---
title: Parâmetros
sidebar_position: 4
---

## Parâmetros

**Tipos de parâmetros usados em REST**

**Path Params:** São parâmetros passados via URL e são obrigatórios. Ou seja, caso não seja definido nenhum valor, ele irá lançar um erro de validação ou fará uma request para outra operação, similar, que use o mesmo verbo.

💭 Imagine uma URL que nos permita recuperar uma lista de livros de forma páginada. Essa URL contém 3 path params, sendo eles SORT, Page Size e Current Page.

Podemos então, por exemplo, setar ask para uma ordenação ascendente em SORT, dez para uma página com dez itens e um para começar na página um. Todos esses parâmetros são passados via path.

💭 Imagine que queremos usar um catálogo online de uma biblioteca para buscar livros. O catálogo permite que possamos especificar exatamente como queremos que os livros sejam listados: em que ordem (por exemplo, alfabética), quantos livros por página queremos ver (tamanho da página) e em qual página do catálogo desejamos visualizar primeiro.

Aqui, a URL do catálogo online é como uma pergunta específica que podemos fazer ao bibliotecário. Se não oferecermos todas as partes da pergunta (os parâmetros), o bibliotecário pode não saber o que estamos pedindo e nos pedirá que sejamos mais especificos.

### O que são Path Params
No desenvolvimento de APIs web, os **Path Params** (ou parâmetros de caminho) são partes da URL que especificam os dados que queremos recuperar ou a operação que desejamos realizar. Eles são chamados de "path" porque estão literalmente no caminho (URI) que acessamos. São considerados obrigatórios porque a operação que estamos tentando realizar depende desses parâmetros para ser executada corretamente.

**Exemplo com a Lista de Livros Paginada**

Vamos usar o exemplo da lista de livros paginada. A URL para acessar essa lista pode parecer algo assim:

```ruby 
https://exemplo.com/livros/sort/ask/pageSize/dez/currentPage/um'

```
**Neste caso:**
* **SORT:** é o parâmetro que define a ordem dos livros 'ask' significa que queremos os livros em ordem crescente.
* **'pageSize'** define quantos itens queremos ver por página. 'dez' significa que queremos ver 10 itens em cada página.
* **'currentPage'** indica a página atual que queremos visualizar. 'um' significa que queremos começar pela primeira página.

**Obrigatoriedade:** 

Se tentarmos acessar a URL sem especificar um desses parâmetros, a API não saberá como processar nossa solicitação corretamente. Por exemplo, se não especificarmos pageSize, como a API saberá quantos itens retornar por página? Isso pode resultar em um erro de validação, pois a API espera essas informações para funcionar corretamente.

**Validação e Erros:** 

Se os parâmetros não forem fornecidos ou forem fornecidos de forma incorreta, a API pode retornar um erro, indicando que algo está faltando ou está errado na sua solicitação.


### Query Params

💭 Imagine que, além de especifciar a ordem, o tamanho da página e a página atual na sua busca de lviros, também queremos filtrar os livros por gênero, autor ou ano de publicação. Esses filtros adicionais são como perguntas extras que fazeomos ao bibliotecário para refinar a busca.

Na biblioteca online, ao invés de apenas dizer ao bibliotecário como listar os livros, agora também pedimos para ver apenas os lviros de ficção cientifica, escritos por um autor específico, ou publicados em um certo ano. Esses detalhes extras são como ajustes na nossa solicitação.


**Afinal, o que é Query Param?**

Os Query Params são parâmetros adicionados ao final de uma URL para dar precisão e fazer uma melhor filtragem das informações ou dados que desejamos obter de uma API. Eles começam após o caractere de interrogação '?' e são separados por '&' quando há mais de um.

**Exemplo com a Lista de Livros Paginada:**

Utilizando o exemplo anterior da lista de livros paginada, se quisermos adicionar filtros para gênero, autor e ano, a URL pode parecer algo assim:

```ruby
https://exemplo.com/livros?genero=ficcao-cientifica&autor=Asimov&ano=1950

```

**Neste caso:**
* **genero** é um query param que filtra livros por gênero. *ficcao-cientifica* indica que estamos interessados apenas em livros desse gênero.
* **autor** filtra os livros pelo nome do autor. *Asimov* significa que queremos livros escritos por Asimov.
* **ano** indica o ano de publicação dos livros que queremos ver. *1950* filtra para mostrar apenas os livros publicados nesse ano.


#### **Diferença e Flexibilidade:**

* **Flexibilidade:** Diferentemente dos Path Params, os Query Params são opcionais. Podemos usá-los para refinar nossa busca, mas a solicitação básica ainda será processada sem eles. Isso oferece uma grande flexibilidade para o usuário ajustar a busca conforme necessário.

* **Multiplicidade:** Podemos ter vários Query Params na mesma URL, cada um ajustando diferentes aspectos da nossa solicitação.

#### Conclusão
Os *Query Params* permitem uma interação mais detalhada e personalizada com a API, oferecendo aos usuários a capacidade de filtrar e ajustar os dados solicitados de acordo com suas necessidades específicas. Voltando à nossa analogia, é como fazer perguntas adicionais ao bibliotecário para garantir que os livros retornados sejam exatamente os que você está procurando, baseados em critérios muito específicos.

### Header Params: O cartão de Acesso da Biblioteca

💭 Imagine que, ao entrar na biblioteca online, nós precisamos de um cartão de acesso especial que informe ao sistema quem somos e quais os serviços que temos permissão para acessar. Este cartão pode também conter preferência como o idioma que você fala ou a região de onde você está acessando a biblioteca.



