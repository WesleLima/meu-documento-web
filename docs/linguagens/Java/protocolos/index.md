---
title: 🖥️ Protocolos
sidebar_position: 1
---
## Conceito de Webservices
![alt text](../../../img/momento.gif)
💭 Imagine! Quando criamos um site em PHP usando HTML, ele é compreensivel para humanos, pois o browser processa as páginas e as tornam legíveis. Os Webservices, por sua vez são legíveis por máquinas ou por outros sistemas. 

💭 Vamos imaginar o seguinte: que conseguimos construir softwares na forma de componentes ou peças... dessa forma, vamos agregando e integrando cada uma dessas peças de forma que possamos usar só aquilo que é apropriado.

💭 Imagine também que você possui uma loja virtual que valida o CPF ou CNPJ e o crédito dos clientes. Para isso, foi desenvolvido um webservice que consulta essas informações. Este serviço web também poderá ser acessado por uma outras aplicações diferentes (desktop, mobile..).
Com isto, o REST faz com que o reúso e a integração com o serviço bem simples e teroricamente, qualquer cliente com autorização poderá consumi-la e executa-la reutilizando o software.

### World Wide Web Consortium (W3C) 
 Para o AWC os webservices são aplicações **[cliente servidor](https://refactoring.guru/pt-br/design-patterns)** que se comunicam pela WWW através do protocolo HTTP (HyperText Transfer Protocol) possibilitando a integração entre softwares e aplicações executando em grande variedade de plataformas e frameworks. Caracterizam-se por sua grande interoperabilidade extendibilidade podendo ser combinados de forma baixamente acoplada para executarem operações complexas. Programas proveem simples serviços que podem interagir uns com os outros gerando soluções csofisticadas

 **Em Topícos:**

- Funcionam no modelo de cliente e servidor;
- Se comunicam pela internet usando o protocolo HTTP;
- Permite que diferentes programas e aplicações;
- Rodar em vária splataformas e frameworks
- Compreensão e trabalho em conjunto;
- Adaptável e pode ser usado em conjunto de maneira flexível para realizar tarefas complexas

De forma resumida, são como pequenos blocos de construção que, quando combinados, podem criar soluções mais complexas e robustas.


Em essência, o REST são pedaços de softwares que podem ser disponibilizados via HTTP e consumir através do protocolo, usando diferentes tipos de clientes, e isso traz um enroem potencial de reúso de código 

## **SOAP vs REST**
![alt text](../../../img/so-vs-re.webp)
Criado pela Microsoft, em 1998, era uma solução que facilitava a integração de sistemas, mas ainda possuia alguns pontos negativos. Logo em 200, Roy Fielding publicou a sua tese de doutorado, em que ele descreveu as restrições arquiteturais do REST. Deis de antão, mas as tecnologias foram as mais utilizadas.

**Principais diferenças:**

**REST:** Representation State Tranfer ou Transferencia de estado representacional é um conjunto de princípios de arquitetura.

O modelo **REST** surgiu após o SOAP e passou a ser visto como uma alternativa mais rápida nos casos baseados em web. REST é um conjunto de diretrizes que oferece uma implementação flexível.

As APIs **REST** são leves e ideais para contextos mais modernos, como a Internet das Coisas (IoT), desenvolvimento de aplicações mobile e [serverless](https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-serverless). Os serviços web SOAP oferecem segurança integrada e transações em conformidade que atendem a muitas necessidades empresariais, mas que também os deixam mais pesados. Além disso, muitas APIs públicas, como a do Google Maps, seguem as diretrizes REST.

**SOAP:** Simple Object Acces Protocol ou "Protocolo de acesso a objetos simples" é um protocolo oficial mantido pela W3C.
 
Em outras palavras, o **SOAP** é um protocolo padrão projetado originalmente para possibilitar a comunicação entre aplicações desenvolvidas em diferentes linguagens e plataformas. Como se trata de um protocolo, ele impõe regras integradas de carregamento das páginas. No entanto, esses padrões também proporcionam conformidade integrada, fazendo com que SOAP seja uma opção recomendada para casos empresariais. Isso inclui segurança, atomicidade, consistência, isolamento e durabilidade (ACID), os quais são um conjunto de propriedades para assegurar transações confiáveis de bancos de dados. 

**Dentre as especificações de serviço web comuns incluem-se:**

- **Segurança de servios web (WS-Security):** padrniza como as mensagens são protegidas e transferidas por meio de identificadores exclusivos chamados de tokens. 
- **WS-RellableMessaging:** padroniza o processamento de erros entre as mensagens transferidas por uma infraestrutura de TI não confiável. 
- **Endereçamento de serviços web (WS-Addressing):** empacota informações de roteamento como metadados em cabeçalhos SOAP, em vez de armazená-las em camadas a fundo na rede.
- **Linguagem de descrição de serviços web (WSDL):** Descreve a atividade de um serviço web e onde ele é iniciado e finalizado. 

Quando uma solicitação de dados é enviada a uma API SOAP, ela pode ser processada por meio de qualquer protocolo de camada da aplicação: **HTTP** (em navegadores da web), **SMTP** (em e-mails), **TCP** e muito mais. No entanto, depois que a solicitação é recebida, as mensagens SOAP precisam ser retornadas como documentos **XML**: uma linguagem de marcação que pode ser lida por máquinas e pessoas. Um navegador não pode armazenar em cache uma solicitação concluída a uma API SOAP. Por isso, não é possível acessá-la depois sem fazer o reenvio à API.


**Conclusão**

A principal diferença dentre ambos, é que o **SOAP** usa o protocolo HTTP para fazer chamadas RPC trafegando o XML.
Já o **REST** faz requisições HTTP e suport diferentes formatos de arquivo.


**SOAP:**
* Protocolo de troca de mensagem em XML;
* Usa WSDL na comunicação entre cliente e servidor;
* Invoca serviços através de chamadas de método RPC;
* Não retorna um resultado facilmente legível para humanos;
* Comunicação feita por HTTP mas pode usar outros protocolos como SMTP, FTP etc;
* Java pode invocar um serviço SOAP mas essa implementação é bastante complexa de ser feita;
* Comparado com REST sua performance não é muito boa.

**REST:**
* Um estilo arquitetural;
* Usa XML, JSON etc. para enviar e receber dados;
* Faz chamadas de serviços via URL PATH;
* Trás resultados legíveis para o ser humano, já que retorna em JSON ou XML, por exemplo;
* Comunicação feita unicamente por HTTP;
* Fácil de inovar via Java;
* Comparado com SOAP a performance é melhor, consume menos recursos de processamento, código mais flefíxel etc.


### REST