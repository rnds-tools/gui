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

Organização das informações, rótulos e operações.

### Administração

- instalar/remover/atualizar/verificar software
- baixar/usar/remover/verificar dados
- configurar certificado digital (usado pelo Serviço de Terminologias)
- configurar portas dos serviços
- definir diretório de trabalho
- obter/atualizar/remover terminologias
- obter/atualizar/remover perfis

### Área de trabalho

- Organizar solução em pastas
- Criar pasta
- Renomear pasta
- Mover pasta
- Remover pasta

### Autenticação

- login
- logout
- cadastro
- recuperação de senha

### Instância

- Selecionar recurso (tipo) da instância
- Editar elemento de recurso (atributo)
  - Acrescentar extensão
  - Remover extensão
  - Alterar cardinalidade
  - Documentar elemento
  - Definir regra
  - Consultar padrão (conforme documentado)

### Executar

- Validação (com FHIR e perfil)
- Expressão em FHIRPath
- FSH para Json
- Json de/para XML

### Exportar

- Solução (toda ela)
- Instância (um item da solução)
- Subconjunto da solução

### FHIRPath

- Executar expressão
- Consultar documentação

### Instâncias

- CRUD instância
  - Perfis
  - Terminologias
  - Exemplos
- Gerar instâncias
- Validar
- Status de validação (continuamente atualizado)
- Visão gráfica (grafo)
- Visão gráfica (formulário)
- Exportar (PDF, png)

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

### Solução

- Soluções criadas pelo usuário
- Criar solução vazia é definir metadados (nome do autor, email, descrição)
- Criar instâncias na solução (conforme estruturadas em pastas)
- Baixar (_download_)
- Importar/carregar instância (incorporar à solução em uso)
- Importar/carregar solução (incorporar à solução em uso)
- Exportar solução em uso ou subconjunto (PDF, zip, html)
- Navegar/consultar o conteúdo da solução (arquivos distribuídos em pastas)

### Status, estatísticas e informações

- Uso
- Conexão com a internet
- Total de elementos da solução
- Versão
- Perfis e terminologias disponíveis

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

### Antes de "entrar"

- Landing page (recepção do usuário ou potencial usuário) com opção para cadastro ou login.
- Registrar novo usuário usando login social (google, facebook, ...)
- Registrar novo usuário usando email

### Após "entrar" (sem solução aberta)

- Abrir solução
- Criar solução
- Atualizar cadastro do usuário (nome, ...)
- Sair (logout)

### Solução aberta

- Verificar código (por exemplo, A90 é código para a Dengue, usando a terminologia CID10). Localizar?
- Localizar por texto ou parte de texto. A busca será feita sobre nome de recursos, diretórios, ou seja, metadados ou dados, conteúdo das instâncias dos recursos, ...
