## Objetivo

Ambiente de Design FHIR (ADF) é um software que oferece
funcionalidades para o _design_ de soluções FHIR. 
O presente projeto tem como finalidade propor 
uma interface para os usuários do ADF, aqui denominados de projetistas.

## Projetista FHIR (_persona_)

Um projetista é um profissional de saúde ou de tecnologia da informação.
Projetistas conhecem o padrão FHIR e o que é preciso para adaptá-lo a um contexto de uso.

Um projetista não necessariamente possui habilidades de programação. Embora possua conhecimento e certa familiaridade com o padrão, naturalmente é preciso consultar a especificação correspondente em vários cenários. 

A expectativa dos projetistas é criar rapidamente uma solução (modelagem FHIR) sem ter que recorrer à extensa
especificação do padrão. 

## O que é uma solução FHIR (modelagem FHIR)?

Solução ou _design_ de uso do FHIR é um conjunto de instâncias de recursos FHIR. 
Estas instâncias definem como o FHIR deve
ser utilizado em um determinado cenário de interoperabilidade em saúde.
De forma simplificada, um recurso pode ser compreendido como um
"item de informação em saúde". Projetistas criam 
instâncias de recursos ou "itens de informação" interconectados,
em geral, formando uma rede.

Ao longo do processo de _design_ instâncias são criadas, algumas são exemplos. 
Verificações são feitas durante este processo, idealmente, a cada pequeno
ajuste na solução.

## User stories (o que o projetista precisa)

- Como designer eu desejo criar instâncias de recursos FHIR para compor minha solução FHIR.

- Como designer eu desejo verificar as instâncias de recursos FHIR que crio para assegurar a 
conformidade com o padrão FHIR.

- Como designer eu desejo validar a solução para assegurar que, de fato, estou propondo
uma solução que atende às especificidades do contexto de uso do FHIR. 

- Como designer eu desejo carregar uma solução previamente criada para acelerar a produção da minha própria solução.

- Como desinger eu desejo baixar a solução que estou produzindo para uso por um servidor FHIR.

- Como designer eu desejo fazer associar uma solução a outra para que uma delas se beneficie do que
já está definido na outra, em uma dada versão.

- Como designer eu desejo criar versões das soluções que produzo para assegurar que posso retomar 
uma dada versão, se necessário.

- Como designer eu desejo visualizar a solução para facilitar a localização e a compreensão da relação 
entre as instâncias.

- Como projetista eu desejo gerenciar o ADF para que ele esteja disponível no computador e eu possa empregá-lo
conforme minhas preferências e configurações correspondentes.


### Características administrativas

- Instalar, verificar (se a instalação está "correta") e remover.
- Iniciar e parar o ADF.
- Consultar o _status_ da execução do ADF.
- Configurar as opções de uso do ADF (inclui certificado digital, portas e outros).

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
  
### Características de formulários
  
  - Cada instância de recurso pode ser apresentada ao projetista
  por meio de um formulário correspondente, onde os campos podem
  ser editados. Este formulário pode ser impresso (PDF) ou 
  apenas utilizado durante a edição. 

## Requisitos de projeto (o que o gerente exige)

Devem estar disponíveis duas aplicações, uma via linha de
comandos (CLI) e outra gráfica, seja web ou desktop. Estas
aplicações possuem muitas funções em comum, especialmente
aquelas administrativas como instalar e outras. Por outro
lado, aquelas de edição estão restritas à versão gráfica.
