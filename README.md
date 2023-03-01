# gui

Interface gráfica para o Ambiente de Desenvolvimento

## Contexto

O Ambiente de Desenvolvimento, doravante AD, oferece várias funcionalidades
que podem ser exploradas por uma interface gráfica.
O presente projeto hospeda o _design_ da interface gráfica, documentos e outros itens pertinentes. Em tempo, o sucesso do AD depende da experiência do usuário oferecida pela interface gráfica, doravante apenas GUI.

## Objetivo

Oferecer as funcionalidades do AD por meio de uma experiência agradável e produtiva.

## Características

Há dois grupos principais de funcionalidades oferecidas pelo AD: (a) administrativas e (g) edição.

### Características administrativas

- Permitir a instalação/atualização/verificação/remoção do AD, o que significa executar estas operações para cada um dos serviços oferecidos pelo AD. São eles: (a) terminologias; (b) auth; (c) fshToFhir (conversor); (d) admin (sidecar); (e) validador.
- Configurar/iniciar/parar os serviços. Por exemplo, configurar terminologias empregadas pelo serviço de terminologias e perfis empregados pelo validador.

- Acompanhar o status dos serviços do AD.

### Características de edição

- Editar instâncias de recursos FHIR, doravante apenas instâncias.
- Edição deve contemplar os formatos FSH e JSON. Ou seja, trata-se
  de edição de arquivo texto.
- Edição inclui a validação do conteúdo em relação ao formato FSH ou JSON.
- Edição inclui a validação do conteúdo em relação à conformidade com eventuais perfis utilizados.
- Edição deve sinalizar a ocorrência de erros e não conformidades.
- Deve contemplar a geração "automática" (template) de instâncias conforme o recurso e o perfil a ser observado, o que facilita a edição. Ou seja, JSON/FSH já "preenchido" com valores espúrios.
- Deve oferecer alternativa gráfica para a edição da instância. Ou seja, tela gráfica gerada conforme o perfil em questão ou, na ausência de um perfil, conforme o recurso. Neste caso, o usuário preenche os "campos" da tela gerada, o que é empregado para alimentar a versão JSON/FSH.
- Converter FSH para JSON e vice-versa.
- Converter FSH/JSON para os formatos correspondente em XML e Turtle. XML/Turtle são usados apenas para consulta.

- Exportar instâncias no formato PDF com leiaute e conteúdo atrativos.
- Validação automática de instâncias à medida que são editadas.

## Design

- Pode ser implementada como SPA sem necessidade de interação com servidor remoto? Validação, TerminologyService e demais? Isso facilitaria implantação e não demandaria servidor remoto.
- Conversões de JSON para XML e de XML para JSON e validações podem ser feitas com [fhir.js](https://github.com/lantanagroup/FHIR.js)
- Apenas cliente FHIR em JS [aqui](https://github.com/FHIR/fhir.js?_ga=2.75210970.976529887.1662986576-1215025224.1662986575)
- Várias ferramentas que usam FHIR por meio de [JS](https://npm.io/search/keyword:fhir)
