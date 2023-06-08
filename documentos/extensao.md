## Extensão

Uma extensão é o mecanismo oferecido pelo padrão FHIR
para complementar as informações de um recurso com um tipo de dados predefinido. Detalhes em:

- https://www.hl7.org/fhir/r4/extensibility.html
- https://hl7.org/fhir/uv/shorthand/reference.html#defining-extensions
- https://www.hl7.org/fhir/r4/defining-extensions.html

### Criar extensão

1. Ao projetista está disponível a criação de uma extensão.
1. O projetista requisita a criação. 
2. O projetista fornece um identificador (nome válido computacionalmente, ou seja, atributo **name** da StructureDefinition que está sendo criada, a extensão). 
3. A partir deste identificador é montada a URL canônica que identifica a extensão. Atributo **url** da StructureDetinition.
4. O usuário fornece um título (**title**).
5. O usuário fornece uma descrição (**description**).
6. O usuário identifica se a extensão reúne várias outras extensões, ou seja, se é do tipo complexo ou, caso contrário, simples. O tipo complexo é definido por uma extensão que reúne subextensões. Observe que uma extensão ou possui subextensões, tipo complexo, ou um valor, tipo simples. Nunca ambos.
7. Se simples, então identifica o tipo do valor correspondente dentre [dezenas](https://www.hl7.org/fhir/r4/extensibility.html) de opções.
8. Se o tipo da extensão é complexo, então é preciso estabelecer cada uma das subextensões. 
9. Uma subextensão, para ser acrescentada, precisa de um nome único localmente, válido computacionalmente, a cardinalidade e a URL que identifica a subextensão.
