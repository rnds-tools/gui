# gui

Ambiente de Desenvolvimento (AD) é um conjunto de serviços (APIs) que oferece várias funcionalidades a serem exploradas por uma interface gráfica.

A expectativa é que um _frontend_ (Web App) usufrua de um _backend_ responsável por encapsular o acesso aos serviços oferecidos (APIs). Tanto o _frontend_ quanto o _backend_ deverão ser "empacotados" em um único executável. Quando baixado e executado, inicia o _backend_ e abre o navegador com a página do _frontend_ já carregada.

O foco do presente projeto está na proposta (_design_) de uma experiência agradável ao usuário deste _frontend_.

## Objetivo

_Design_ de experiência do usuário contemplando as funcionalidades oferecidas pelo AD. Esta experiência deve ser "agradável" e "produtiva".

## Usuários (_personas_)

- Integrador. Desenvolvedor de software que deseja criar seu componente de software para integração com um servidor FHIR.
- Designer de solução FHIR. Profissional de saúde ou de tecnologia da informação que deseja "experimentar" artefatos FHIR, ou seja, tanto produzir perfis, sistemas de codificação e outros, quanto verificar aqueles existentes por meio da criação de instâncias.

## Características oferecidas pela GUI

Estão organizadas em administrativas e de edição por simplicidade.

## Características administrativas

- Oferecer as tarefas para instalar/atualizar/verificar/remover o AD, o que significa executar estas tarefas para cada um dos seguintes serviços: (a) terminologias; (b) auth; (c) fshToFhir (conversor); (d) admin (sidecar); (e) validador.
- Configurar/iniciar/parar os serviços. Por exemplo, configurar terminologias empregadas pelo serviço de terminologias e perfis empregados pelo validador.

- Acompanhar o status dos serviços do AD.

### Características de edição

- Editar instâncias de recursos FHIR, doravante apenas instâncias.
- Edição deve contemplar os formatos FSH e JSON. Ou seja, trata-se
  de edição de arquivo texto.
- Edição inclui a validação do conteúdo em relação ao formato FSH ou JSON.
- Edição inclui a validação do conteúdo em relação à conformidade com eventuais perfis utilizados.
- Edição deve sinalizar com mínima interferência do usuário, a ocorrência de erros e não conformidades.
- Edição deve contemplar a geração "automática" (template) de instâncias conforme o recurso e o perfil a ser observado, o que facilita a edição. Ou seja, JSON/FSH já "preenchido" com valores espúrios.
- Edição deve oferecer alternativa gráfica para a criação da instância. Ou seja, tela gráfica gerada conforme o perfil em questão, em vez da edição de texto. Neste caso, o usuário preenche os "campos" da tela gerada, o que é empregado para alimentar a versão JSON/FSH.
- Converter FSH para JSON e vice-versa.
- Converter FSH/JSON para os formatos correspondente em XML e Turtle. XML/Turtle são usados apenas para consulta.
- Exportar instâncias no formato PDF com leiaute e conteúdo atrativos.
