## Objetivo

Ambiente de Design FHIR (ADF) é um software que oferece
funcionalidades para o _design_ de soluções FHIR. 
O presente projeto tem como finalidade propor 
uma interface para os usuários do ADF, aqui denominados de projetistas.

> FHIR é um padrão para troca de dados em saúde, adotado pelo Brasil (https://www.hl7.org/fhir/r4/).

## Importante

Tudo o que segue é resultado de esforço ainda inacabado, incompleto e, portanto, é natural ajustes. 
Como em boa parte dos projetos reais, não sabemos exatamente onde vamos chegar, mas temos
algumas orientações.

## Projetista FHIR (_persona_)

Um projetista é um profissional de saúde ou de tecnologia da informação.
Projetistas conhecem o padrão FHIR e o que é preciso para adaptá-lo a um contexto de uso.

Um projetista não necessariamente possui habilidades de programação. 
Embora possua conhecimento e certa familiaridade com o padrão, 
naturalmente é preciso consultar a especificação correspondente em vários cenários. 

Uma expectativa clara dos projetistas é criar com rapidez e facilidade uma solução (modelagem FHIR). 

## O que é uma solução FHIR (modelagem FHIR)?

Solução ou _design_ de uso do FHIR é um conjunto de instâncias de recursos FHIR. 
Estas instâncias de recursos FHIR, ou simplesmente instâncias, definem como o FHIR deve
ser utilizado em um determinado cenário de interoperabilidade em saúde.
De forma simplificada, um recurso pode ser compreendido como um
"item de informação em saúde". Projetistas criam 
instâncias ou "itens de informação" interconectados,
em geral, formando um grafo.

Ao longo do processo de _design_ instâncias são criadas, algumas são exemplos. 
Verificações são feitas durante este processo, idealmente, a cada pequeno
ajuste na solução.

## User stories (requisitos dos projetistas)

- Como projetista eu desejo editar instâncias de recursos FHIR para compor minha solução FHIR.

- Como projetista eu desejo verificar as instâncias de recursos FHIR, enquanto as edito, para assegurar a 
conformidade com o padrão FHIR.

- Como projetista eu desejo validar a solução para assegurar que, de fato, a proposta de
 solução atende às especificidades do contexto de uso do FHIR. 

- Como projetista eu desejo incluir as instâncias de uma solução previamente criada para acelerar a produção da minha própria solução.

- Como projetista eu desejo especializar as instâncias de uma solução previamente criada para acelerar a produção da minha própria solução.

- Como projetista eu desejo baixar a solução que estou produzindo para utilizá-la em um servidor FHIR.

- Como projetista eu desejo fazer associar uma solução a outra para que uma delas se beneficie do que
já está definido na outra, em uma dada versão.

- Como projetista eu desejo criar versões das soluções que produzo para assegurar que posso retomar 
uma dada versão, se necessário.

- Como projetista eu desejo visualizar a solução para facilitar a localização e a compreensão da relação 
entre as instâncias.

- Como projetista eu desejo gerenciar o ADF para que ele esteja disponível no computador e eu possa empregá-lo
conforme minhas preferências e configurações correspondentes.

- Como projetista eu desejo fazer buscas na minha solução para facilitar a localização de item de interesse.


### Características administrativas

- Instalar, verificar (se a instalação está "correta") e remover.
- Iniciar e parar o ADF.
- Consultar o _status_ da execução do ADF (monitorar).
- Configurar as opções de uso do ADF (servidores onde dados estão disponíveis, certificado digital, portas, diretório de trabalho, versões de terminologias e perfis a serem utilizados).
- Configurar as terminologias a serem utilizadas. 

### Características de validação de código

- Verificar se um determinado código pertence a um dado ValueSet. Para tal é necessário fornecer o código, o ValueSet e também o CodeSystem. Estes três valores são sequências de caracteres.

### Características de arquivos

- Cada usuário possui sua própria "área de trabalho", um "diretório" (_folder_) virtual. Nesta área de trabalho são depositados os arquivos, criados diretórios, renomeados, tudo "virtualmente", ou seja, não é um diretório convencional de um sistema de arquivos como o Windows ou Linux.

- Nesta área de trabalho podem ser depositados arquivos de apenas três formatos distintos: (a) FSH; (b) JSON e (c) XML.

- Na área de trabalho estão disponíveis arquivos que são instâncias de recursos FHIR, ao todo são mais de 150 recursos distintos.

- Existe relacionamentos entre estes arquivos. Por exemplo, uma instância pode incluir referência para um perfil a ser atendido, e/ou referenciar instâncias que 
juntas formam um grafo de instâncias.

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

Devem estar disponíveis duas aplicações:

- uma via linha de comandos (CLI) para instalação, atualização e outras.
- uma interface gráfica que contempla as operações via linha de comandos e outras como a edição de instâncias de recursos.
