---
title: HATEOAS
sidebar_position: 2
---

## Hypermedia As The Engine Of Application State (HATEOAS)

É uma constante, arquitetural, de aplicações REST.
Uma API Hateoas provê informações que permite que ocorra uma navegação entre seus endpoints de forma dinâmica, visto que links são inclusos à respostas.

Em prática, a API provê as informações que os consumers ou clients irão precisar para dar os próximos passos.

💭 Imagine uma pesquisa sobre REST que me retorna uma página sobre o tema pesquisado e destaca links para informações relacionadas, tais como JSON, XML, etc. Esses links me possibilitam prosseguir com minha navegação.

A mesma ideia acima se aplica a uma API.
💭 Imagine que recuperamos as informações de uma pessoa no servidor. Junto com os dados, a API e me retorna também links que me possibilitam ir para o próximo para o próprio recurso, ir para uma nova página, ir para a atualização desse registro, ir para a deleção desse registro, etc.


✨ Links úteis:
1. **Restcookbook:** http://restcookbook.com/Basics/hateoas/
2. **Nordic APIS:** https://nordicapis.com/tools-to-make-hateoas-compliance-easier/
3. **Semeru:** http://www.semeru.com.br/blog/en/