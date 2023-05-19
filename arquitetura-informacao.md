## Arquitetura da informação (esboço)

### Inventário

Tudo o que será exibido na interface, arquivos, visualizações, ...

- _solução_
- _contexto_ (da interoperabilidade)
- _autores_ (email, conta)
- _arquivos_
- _diretórios_
- perfis (instâncias de StructureDefinition)
- terminologias
- recursos
- instâncias de recursos
- linguagem fhirpath
- avaliação de expressões em FHIRPath
- JSON (edição)
- XML (exibição)
- Turtle (exibição)
- FSH (FHIR Shorthand, edição)
- documentação de recurso (portal do FHIR)
- gerir solução (crud) + versões
- instâncias de recursos (crud)
- CRUD CodeSystem
- CRUD ValueSet
- CRUD instâncias que são exemplos (ilustração)
- CRUD perfis (StructureDefinition)
- Associar ValueSet a elemento de recurso
- exemplos (instâncias de recursos)
- verificar solução (conformidade com padrão FHIR)
- relatório de verificação
- gerar instâncias de exemplos
- gerar formulário de instâncias que pode ser preenchido a partir dos campos
- formulário pode ser exportado para PDF ou PNG
- elementos (combinação de elementos formam um recurso)
- cada elemento possui documentação correspondente editável
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


### Categorias

Cada item do inventário agora é classificado em uma categoria (rótulo).
Ou seja, são "agrupados". Esta classificação deve ser tal que o projetista
deve encontrar facilmente o que está procurando.

#### Solução

- Baixar (_download_)
- Importar (incorporar à solução em uso)
- Exportar solução em uso (PDF, zip, html)
- Criar (fornecer metadados como contexto, autores, instituição e outros)
- Navegar/consultar o conteúdo da solução (arquivos distribuídos em "pastas")

### Navegação (_user flow_)

Defina como o projetista irá navegar por todos os itens do inventário. Inclui
menus, botões e links. O foco, contudo, não é o aspecto visual, mas a jornada.

Há muitas formas de se registrar isso. Segue uma proposta inicial [aqui](https://www.figma.com/file/6ebDkUG2dNp4DtLZiuufat/Ambiente-FHIR?type=design&node-id=83%3A0&t=PRIFKs14NjGMglqE-1) usando Figma. 

Eu prefiro, neste momento, simplesmente registrar os fluxos...

#### Antes de "entrar"

- Landing page (recepção do usuário ou potencial usuário) com opção para cadastro ou login.
- Registrar novo usuário usando login social (google, facebook, ...)
- Registrar novo usuário usando email

#### Após "entrar" (sem solução aberta)

- Abrir solução
- Criar solução
- Atualizar cadastro do usuário (nome, ...)
- Sair (logout)

#### Solução aberta

- Verificar código (por exemplo, A90 é código para a Dengue, usando a terminologia CID10). Localizar?
- Localizar por texto ou parte de texto. A busca será feita sobre nome de recursos, diretórios, ou seja, metadados ou dados, conteúdo das instâncias dos recursos, ...
