## História de usuário

- HU _Como projetista eu desejo baixar (exportar) a solução que estou produzindo para uso por um servidor FHIR ou para impressão_.
  
- HU Como projetista eu desejo me identificar para que minhas soluções, configurações e preferências estejam disponíveis.

- HU Como projetista eu desejo editar instâncias de recursos FHIR para criar minha solução FHIR.

- HU Como projetista eu desejo verificar as instâncias de recursos FHIR que crio para assegurar a
  conformidade com o padrão FHIR e com perfis estabelecidos.

- HU Como projetista eu desejo criar exemplos de instâncias e validá-las para assegurar que, de fato, a proposta de
  solução atende às especificidades do contexto de uso do FHIR.

- Como projetista eu desejo manter várias soluções simultaneamente e carregar aquela desejada para edição.

- Como projetista eu desejo especializar uma solução para estabelecer restrições adicionais necessárias para um dado contexto de uso.

- Como projetista, ao longo do processo de _design_, eu desejo criar versões de uma solução para assegurar que posso retomar a uma dada versão, se necessário.

- Como projetista eu desejo visualizar uma solução para facilitar a localização e a compreensão da relação
  entre as instâncias (grafo).

- Como projetista eu desejo consultar detalhes de elementos de um recurso FHIR, sem necessariamente consultar a especificação FHIR, para agilizar a edição dos recursos de uma solução.

- Como projetista eu desejo fazer buscas na minha solução para facilitar a localização de item de interesse.

## Outros requisitos (o que o gerente exige)

Devem estar disponíveis três aplicações:

- uma via linha de comandos (CLI) que implementa as características administrativas e atende cenários onde uma interface gráfica não pode ser utilizada.
- uma interface gráfica que implementa as características administrativas à semelhança da interface CLI.
- uma interface gráfica que contempla as operações fim (criação do _design_ de uso do FHIR).

![modelo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/rnds-tools/gui/main/diagramas/componentes.puml)

## Características (_features_) esperadas

### Características administrativas

- Instalar, verificar (se a instalação está "correta") e remover.
- Iniciar e parar o ADF.
- Consultar o _status_ da execução do ADF (monitorar registros de _log_).
- Configurar as opções de uso do ADF. A saber: servidores onde dados estão disponíveis (versões dos dados); (b) certificado digital (empregado para acesso ao servidor FHIR); (c) portas empregadas pelos serviços; (d) diretório de trabalho.
- Configurar as terminologias disponíveis para uso.
- Configurar os perfis disponíveis para uso.
- Configurar soluções disponíveis para uso.

### Características de validação de código

- Verificar se um determinado código pertence a um dado ValueSet. Para tal é necessário fornecer o código, o ValueSet e também o CodeSystem. Estes três valores são sequências de caracteres.

### Características de arquivos

- Cada usuário possui sua própria "área de trabalho", um "diretório" (_folder_) virtual. Nesta área de trabalho são depositados os arquivos, criados diretórios/subdiretórios, renomeados, tudo "virtualmente", ou seja, não é um diretório convencional de um sistema de arquivos como o Windows ou Linux.

- Nesta área de trabalho virtual residem arquivos de apenas três formatos distintos: (a) FSH; (b) JSON e (c) XML.

- Na área de trabalho estão disponíveis arquivos que são instâncias de recursos FHIR, ao todo são mais de 150 recursos distintos.

- Existe relacionamentos entre estes arquivos. Por exemplo, uma instância pode incluir referência para um perfil a ser atendido, e/ou referenciar instâncias que
  juntas formam um grafo de instâncias.

- Pode-se realizar o _download_ de arquivos e/ou diretórios. O download de um arquivo pode ser feito em vários formatos: (a) PDF; (b) FSH; (c) JSON.

- O _download_ de um diretório será reunido em um único arquivo no formato zip.

- Diretórios e/ou arquivos podem ser criados, removidos e/ou renomeados a partir da área de trabalho do usuário.

- Deve ser possível observar a área de trabalho conforme criada, em seus diretório e arquivos ou ainda, na perspectiva de uma classificação de interesse. Possíveis classificações: (a) data de criação; (b) por recurso FHIR.

### Características de edição

- Editar instâncias de recursos.

- Avaliar uma expressão em FHIRPath para uma determinada instância.

- Edição deve contemplar os formatos FSH e JSON. Ou seja, trata-se
  de edição de arquivo texto. O formato XML não poderá ser editado, trata-se
  apenas de uma opção de visualização.

- Edição FSH deve oferecer recursos IntelliSense com lista de opções inteligentes, por exemplo, ao digitar ref<tab> onde se espera uma referência é completado com Reference(x) e o cursor piscando onde está o x com uma lista de opções correspondentes ao contexto em questão.

- Edição inclui a validação do conteúdo em relação ao formato FSH ou JSON.

- Edição inclui a verificação do conteúdo em relação à conformidade com eventuais perfis utilizados.

- Edição deve sinalizar com mínima interferência do usuário, a ocorrência de erros e não conformidades.

- Edição deve contemplar a geração "automática" (_template_) de instâncias conforme o recurso e o perfil a ser observado, o que facilita a edição. Ou seja, JSON/FSH já "preenchido" com valores espúrios.

- Edição deve oferecer alternativa gráfica para a criação da instância. Ou seja, tela gráfica gerada conforme o perfil em questão, em vez da edição de texto. Neste caso, o usuário preenche os "campos" da tela gerada, o que é empregado para alimentar a versão JSON/FSH.

- Converter FSH para JSON e vice-versa.

- Converter conteúdo em FSH/JSON para conteúdo correspondente no formato XML.

- Exportar instâncias no formato PDF com leiaute e conteúdo atrativos.

- Efetuar operação de consulta em terminologia, seja disponível localmente, editada pelo próprio projetista ou disponível em servidor remoto.

### Características de formulários

A estrutura de dados, item de informação em saúde ou recurso pode ser interpretada como um formulário, formado por campos de tipos predefinidos. Adicionalmente, convém ressaltar, cada recurso pode ser estendido com campos também de tipos predefinidos. Neste contexto é importante gerar dinamicamente um formulário correspondente para que possa ser visualizado.
