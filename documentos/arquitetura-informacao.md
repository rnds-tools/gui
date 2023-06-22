# Arquitetura da informação (esboço)

## Inventário (o que faz parte)

- _solução_
- _contexto_ (da interoperabilidade)
- _autores_ (email, conta)
- _arquivos_
- _diretórios_
- _perfis_ (instâncias de StructureDefinition)
- _terminologias_
- _recursos_
- _instâncias_ de recursos
- linguagem _fhirpath_
- _avaliação_ de expressões em FHIRPath
- _JSON_ (edição)
- _XML_ (exibição)
- _FSH_ (FHIR Shorthand, edição)
- _documentação_ de recurso (portal do FHIR)
- _gerir_ solução (crud) + versões
- _Validar_ a conformidade de uma instância a zero ou mais StructureDefinition (perfis).
- _exemplos_ (instâncias de recursos)
- _verificar_ solução (conformidade com padrão FHIR)
- _relatório_ (status) de verificação
- _gerar_ instâncias de exemplos
- _gerar_ formulário de instâncias que pode ser preenchido a partir dos campos
- _exportar_ formulário para PDF ou PNG
- elementos (combinação de elementos formam um recurso)
- _documentar_ elemento
- baixar solução
- carregar solução
- solução pode ser especializada por outra (especializar)
- solução pode incorporar instâncias definidas em outra (importar)
- visualizar solução (instâncias formam um grafo)
- software (versões)
- dados (versões)
- instalar/remover/atualizar/verificar software
- baixar/usar/remover/verificar dados
- software (status, estatísticas de uso)
- configuração do software (certificado digital, portas, diretório de trabalho, versões de terminologias e perfis a serem utilizados)
- operação de validação de código (há um dado código de um CodeSystem em um dado ValueSet?)
- área de trabalho, criar subdiretórios, renomeá-los, movê-los, ...

## Categorias

### Administração

- instalar/remover/atualizar/verificar/iniciar/parar/monitorar o ADF
- baixar/usar/remover/verificar dados terminológicos e perfis
- configurar certificado digital (usado pelo Serviço de Terminologias)
- configurar portas dos serviços
- definir diretório de trabalho
- obter/atualizar/remover terminologias
- obter/atualizar/remover perfis

### Perspectivas

- Visão de soluções
- Visão de organização de solução
- Visão de grafo (toda a solução)
- Visão de instância (selecionada, em edição)
  - Visão de formulário
  - Visão de grafo
  - Visão FSH
  - Visão JSON
  - Visão XML

### Autenticação

- login
- logout
- cadastro
- recuperação de senha

### Elemento

- Acrescentar extensão
- Remover extensão
- Alterar cardinalidade
- Documentar elemento
- Definir regra (FHIRPath)
- Consultar documentação
- Exibir exemplos

### Executar

- Validação (com FHIR e perfil)
- Expressão em FHIRPath
- FSH para Json
- Json de/para XML

### Exportar

- Solução (toda ela ou subconjunto)
- Instância (um item da solução)

### Extensão (instância de StructureDefinition)

- Definir url
- Selecionar tipo (de um conjunto [fixo](http://hl7.org/fhir/extensibility.html))
- Localizar tipo
- Identificar tipo por valor
- Exibir exemplos (gerados pelo ADF)

### FHIRPath

- Executar expressão
- Consultar documentação

### Instância

- Gerar exemplo
- Validar
- Status de validação (continuamente atualizado)
- Exportar (PDF, png)
- Adicionar perfil a ser atendido (exemplo)
- Adicionar extensão
- Visão de formulário
- Visão de grafo
- Visão FSH
- Visão JSON
- Visão XML

### Perfis (StructureDefinition)

- Extensões
- Especializações
- Restrições

### Recursos (FHIR)

- Recursos FHIR (cerca de 150)
- Documentação do recurso
- Tipos de dados (elementos)
- Terminologias (predefinidas)
- Perfis (predefinidos)
- Localizar por nome, parte do nome, atributo, documentação, ...

### Visão FSH 

Permite edição usando FHIR Shorthand.

### Visão de formulário

Permite edição por meio de formulário pode ser gerado [automaticamente](https://rjsf-team.github.io/react-jsonschema-form/). Nesta visão,
a edição da instância é similar ao preenchimento de campos de um formulário.

### Visão gráfica

- Exibe grafo das instâncias da solução
- Selecionar instância para edição

### Visão de organização de solução (pastas)

- Criar pasta
- Renomear pasta
- Mover pasta
- Mover instância de recurso para outra pasta
- Remover pasta

### Visão de soluções

- Soluções criadas pelo usuário (nome, descrição, data)
- Criar solução (nome e descrição, data fornecida automaticamente)
- Renomear
- Remover
- Exportar
- Importar
- Localizar

### Solução (aberta)

- Criar instância
  - Selecionar recurso (tipo da instância)
  - Definir classificação: exemplo, especialização ou restrição
- Importar/carregar instância (incorporar à solução em uso)
- Importar/carregar solução (incorporar à solução em uso)
- Exportar solução em uso ou subconjunto (PDF, zip, html)
- Navegar/consultar o conteúdo da solução
  - Organização por arquivos (em pastas)
  - Organização por tipo de instância

### Configurações

- Uso
- Conexão com a internet
- Total de elementos da solução
- Versão
- Perfis e terminologias disponíveis
- Configurações empregadas

### Terminologias

- CodeSystem
- ValueSet
- Associar ValueSet a propriedade

### Visualização

- Formulário
- Grafo
- Filtrar elementos (atributos)

## Navegação (_user flow_)

Defina como o projetista irá navegar por todos os itens do inventário. Inclui menus, botões e links. O foco, contudo, não é o aspecto visual, mas a jornada.

Há muitas formas de se registrar isso. Segue uma proposta inicial [aqui](https://www.figma.com/file/6ebDkUG2dNp4DtLZiuufat/Ambiente-FHIR?type=design&node-id=83%3A0&t=PRIFKs14NjGMglqE-1) usando Figma.

Eu prefiro, neste momento, simplesmente registrar os fluxos...

- User flow [extensão](extensao.md) (Felipe, Marcos, Amadeu, Luca e José Carlos)
- User flow [CodeSystem](codesystem.md) (Adriel, Arthur Camargo, Igor e Paulo Roberto)
- User flow [ValueSet](valueset.md) (Daniela, Felipe Lagais, Arthur Faria, Tales Eduardo e Mikael)
- User flow [ConceptMap](conceptmap.md)
- User flow [NamingSystem](namingsystem.md) (Gabriel Pires, Giancarlo Moraes, Natan, Ramze, Guilherme Cruz)
- User flow [datatypes](datatype.md)
