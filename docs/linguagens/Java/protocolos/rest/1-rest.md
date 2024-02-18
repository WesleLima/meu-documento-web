---
title: Rest
sidebar_position: 2
---

## Representational State Transfer (REST)

É um estilo de arquitetura de software para sistemas distribuídos de hipermídia, como a World Wide Web (WWW).

Em tese, Rolling Fielding definiu 6 restrições para o protocolo REST, sendo eles:

- **Deve ser "Cliente-servidor":** Clientes e servidores separados;

- **Stateless Server:** O servidor não deve guardar o estado do ciente. Cada request (requisição) de um cliente contém todas as informações ncessárias para atendê-lo.

- **Cacheable:** O cliente deve ser informado sobre as propriedades de cache de um recurso para que possa decidir quando deve ou não utilizar cache.

- **Interface uniforme:** Existe uma inferface uniforme entre cliente e servidor.
    * Identificação de recursos [(URI)](https://geniodowifi.com/glossario/o-que-e-uri-uniform-resource-identifier/)
    * Manipulação de recursos a partir de suas representações;
    * Mensagens auto descritivas;
    * Hypermedia as the engine of application state - [HATEAOS](https://www.treinaweb.com.br/blog/o-que-e-hateoas#:~:text=HATEOAS%20é%20uma%20restrição%20que,conhecimento%20prévio%20profundo%20da%20API.)  


- **Sistema em camadas:** Deve suportar conceitos como balanceamento de carga, proxier e firewalls.

- **Código sob Demanda (opcional):** O cliente pode solicitar o código do servidor e executá-lo.

**Vantagens dos Web Services RESTful:**

- REST é um padrão arquitetural basicamente leve por natureza. Logo, quando houver limitações de banca, o ideial é optar por web services REST;
- Desenvolviemnto fácil e rápido;
- Aplicativos MObile tem ganhado cada vez mais espaço e precisam interagir rapidamente com os servidores e o padrão REST é mais rápido no processamento de dados das requests e reponses.