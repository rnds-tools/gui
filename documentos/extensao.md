## Extensão

Uma extensão é o mecanismo oferecido pelo padrão FHIR
para complementar as informações de um recurso com um tipo de dados predefinido. Detalhes em:

- https://www.hl7.org/fhir/r4/extensibility.html
- https://hl7.org/fhir/uv/shorthand/reference.html#defining-extensions
- https://www.hl7.org/fhir/r4/defining-extensions.html

### Criar extensão (user flow)

1. Ao projetista está disponível a criação de uma extensão.
1. O projetista requisita a criação. 
2. O projetista vê os campos disponíveis para a definição da extensão. Além da _url_ e do _value[x]_, existem metadados para a extensão, ou seja, qualquer campo de uma [StructureDefinition](https://www.hl7.org/fhir/r4/structuredefinition.html) além dos campos de [ElementDefinition](https://www.hl7.org/fhir/r4/elementdefinition.html) para _url_ e _value[x]_. Por exemplo, para fornecer uma descrição do conteúdo, _value[x]_, pode-se usar o campo _short_ para "breve descrição" deste campo assim como o campo _copyright_ para direitos autorais da extensão. Respectivamente, estes campos estão definidos em _ElementDefinition_ e _StructureDefinition_. Dito de outra forma, há vários metadados para a extensão (campos de StructureDefinition) assim como metadados para cada atributo da extensão (ElementDefinition).
3. Fornece um identificador (nome válido computacionalmente, ou seja, atributo **name** da StructureDefinition que está sendo criada, a extensão). 
4. A partir deste identificador é montada a URL canônica que identifica a extensão. Atributo **url** da StructureDetinition.
5. O usuário fornece um título (**title**).
6. O usuário fornece uma descrição (**description**).
7. O usuário identifica se a extensão reúne várias outras extensões, ou seja, se é do tipo complexo ou, caso contrário, simples. O tipo complexo é definido por uma extensão que reúne subextensões. Observe que uma extensão ou possui subextensões, tipo complexo, ou um valor, tipo simples. Nunca ambos.
8. Se simples, então identifica o tipo do valor correspondente dentre [dezenas](https://www.hl7.org/fhir/r4/extensibility.html) de opções. Observe que é possível fornecer mais de um tipo. Ou seja, o tipo simples define pelo menos um tipos disponíveis. Observe que não pode haver repetição de tipo.
9. Se o tipo da extensão é complexo, então é preciso identificar cada uma das subextensões que fazem parte da extensão. O projetista seleciona a extensão dentre aquelas disponíveis na solução. Observe que para criar uma extensão do tipo complexa é preciso estar disponível pelo menos uma extensão simples.
10. Uma subextensão, para ser acrescentada, precisa de um nome único localmente no contexto da extensão editada, válido computacionalmente, além da cardinalidade e da URL que identifica a subextensão.
