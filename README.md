# gui

O Ambiente de Desenvolvimento, ou simplesmente AD, reúne um conjunto de serviços (APIs) que oferece várias funcionalidades para gestão ou _design_ de soluções FHIR. O presente projeto tem como **objetivo** propor um _design_ por meio do qual estas funcionalidades podem ser exploradas por uma interface gráfica (Web App).

## Quem são os usuários (_personas_)?

- Integrador. Desenvolvedor de software que deseja criar seu componente de software para integração com um servidor FHIR. Em outros termos, é um programador.
- Designer de solução FHIR. Profissional de saúde ou de tecnologia da informação que deseja "experimentar" artefatos FHIR, ou seja, tanto produzir perfis, sistemas de codificação e outros, quanto verificar aqueles existentes por meio da criação de instâncias. Este _designer_ é quem conhece do assunto para os quais as funcionalidades são oferecidas. Necessariamente conhece o assunto, não necessariamente é um programador ou "técnico".

## User stories

- Como designer eu desejo criar instâncias de recursos FHIR para compor minha solução FHIR.

- Como designer eu desejo verificar as instâncias de recursos FHIR que crio para verificar se estão montadas em conformidade com o padrão FHIR.

- Como designer eu desejo carregar uma solução previamente criada para acelerar a produção da minha própria solução.

- Como desinger eu desejo baixar a solução que estou produzindo para uso por um servidor. 

- Como designer eu desejo criar versões das soluções que produzo para assegurar uma evoução segura.

## O que é uma solução?

Ou _design_ de uso do FHIR é um conjunto de instâncias de recursos FHIR. 
Algumas instâncias servem para ilustrar, enquanto outras definem como o FHIR deve
ser utilizado em um determinado cenário. 

Ao longo do processo de _design_ instâncias são criadas, exemplos ou não. 
Verificações são feitas durante este processo, idealmente, a cada mudança.

## Quais são as funcionalidades?

- Verificação de códigos em um servidor de terminologias.
- Validação de instâncias de recursos. Entenda recurso como uma classe e instância, como uma instância da classe, em uma analogia com a orientação a objetos.

## Características oferecidas pela GUI

Estão organizadas em administrativas e de edição por simplicidade.

## Características administrativas

- Oferecer as tarefas para instalar/atualizar/verificar/remover o AD, o que significa executar estas tarefas para cada um dos seguintes serviços: (a) terminologias; (b) auth; (c) fshToFhir (conversor); (d) admin (sidecar); (e) validador.
- Configurar/iniciar/parar os serviços. Por exemplo, configurar terminologias empregadas pelo serviço de terminologias e perfis empregados pelo validador.

- Acompanhar o status dos serviços do AD.

### Características de validação de código

- Verificar se um determinado código pertence a um dado ValueSet. Para tal é necessário fornecer o código, o ValueSet e também o CodeSystem. Estes três valores são sequências de caracteres.

- O AD é carregado com um conjunto de ValueSets.

- O AD é carregado com um conjunto de CodeSystems.

- Deve-se facilitar a localização da instância desejada, tanto de ValueSet quanto de CodeSystem para efetuar esta operação de validação.

### Características de arquivos

- Cada usuário possui sua própria área de trabalho, um diretório (_folder_). A área de trabalho é um diretório "em nuvem", semelhante a um diretório local de trabalho, mas não está disponível localmente no computador onde a interface gráfica está em execução.

- Nesta área de trabalho podem ser depositados arquivos de apenas três formatos distintos: (a) FSH; (b) JSON e (c) XML.

- Em qualquer um destes formatos está o conteúdo pertinente a um dos 154 recursos FHIR distintos. Ou seja, na área de trabalho estão disponíveis arquivos que são instâncias de recursos FHIR, ao todo são mais de 150 tipos distintos. A instância pode estar registrada no formato FSH, JSON ou XML.

- Existe relacionamentos entre estes arquivos.

- No diretório principal podem ser criados subdiretórios.

- Arquivos são criados em qualquer diretório da área de trabalho do usuário.

- Pode-se realizar o _download_ de arquivos e/ou diretórios. O download de um arquivo pode ser feito em vários formatos: (a) PDF; (b) FSH; (c) JSON ou (d) XML.

- O _download_ de um diretório será reunido em um único arquivo no formato zip.

- Diretórios e/ou arquivos podem ser criados, removidos e/ou renomeados a partir da área de trabalho do usuário.

- Deve ser possível observar a área de trabalho conforme criada, em seus diretório e arquivos ou ainda, na perspectiva de uma classificação de interesse. Possíveis classificações: (a) data de criação; (b) por recurso FHIR.

### Características de edição

- Editar instâncias de recursos FHIR, doravante apenas instâncias.
- Edição deve contemplar os formatos FSH e JSON. Ou seja, trata-se
  de edição de arquivo texto.
- Edição FSH deve oferecer recursos IntelliSense com lista de opções inteligentes, por exemplo, ao digitar ref<tab> onde se espera uma referência é completado com Reference(x) e o cursor piscando onde está o x com uma lista de opções correspondentes ao contexto em questão.
- Edição inclui a validação do conteúdo em relação ao formato FSH ou JSON.
- Edição inclui a validação do conteúdo em relação à conformidade com eventuais perfis utilizados.
- Edição deve sinalizar com mínima interferência do usuário, a ocorrência de erros e não conformidades.
- Edição deve contemplar a geração "automática" (template) de instâncias conforme o recurso e o perfil a ser observado, o que facilita a edição. Ou seja, JSON/FSH já "preenchido" com valores espúrios.
- Edição deve oferecer alternativa gráfica para a criação da instância. Ou seja, tela gráfica gerada conforme o perfil em questão, em vez da edição de texto. Neste caso, o usuário preenche os "campos" da tela gerada, o que é empregado para alimentar a versão JSON/FSH.
- Converter FSH para JSON e vice-versa.
- Converter FSH/JSON para os formatos correspondente em XML e Turtle. XML/Turtle são usados apenas para consulta.
- Exportar instâncias no formato PDF com leiaute e conteúdo atrativos.
