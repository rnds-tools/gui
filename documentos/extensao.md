## Extensão

Uma extensão é o mecanismo oferecido pelo padrão FHIR
para complementar as informações de um recurso com um tipo de dados predefinido. Detalhes em:

- https://www.hl7.org/fhir/r4/extensibility.html
- https://hl7.org/fhir/uv/shorthand/reference.html#defining-extensions
- https://www.hl7.org/fhir/r4/defining-extensions.html

### Criar extensão (user flow)

1. Ao projetista está disponível a criação de uma extensão.
1. O projetista requisita a criação. 
2. O projetista vê os campos disponíveis para a definição da extensão. 
3. Fornece um identificador (nome válido computacionalmente, ou seja, atributo **name** da StructureDefinition que está sendo criada, a extensão). 
4. A partir deste identificador é montada a URL canônica que identifica a extensão. Atributo **url** da StructureDetinition.
5. O usuário fornece um título (**title**).
6. O usuário fornece uma descrição (**description**).
7. O usuário identifica se a extensão reúne várias outras extensões, ou seja, se é do tipo complexo ou, caso contrário, simples. O tipo complexo é definido por uma extensão que reúne subextensões. Observe que uma extensão ou possui subextensões, tipo complexo, ou um valor, tipo simples. Nunca ambos.
8. Se simples, então identifica o tipo do valor correspondente dentre [dezenas](https://www.hl7.org/fhir/r4/extensibility.html) de opções. Observe que é possível fornecer mais de um tipo. Ou seja, o tipo simples define pelo menos um tipos disponíveis. Observe que não pode haver repetição de tipo.
9. Se o tipo da extensão é complexo, então é preciso identificar cada uma das subextensões que fazem parte da extensão. O projetista seleciona a extensão dentre aquelas disponíveis na solução. Observe que para criar uma extensão do tipo complexa é preciso estar disponível pelo menos uma extensão simples.
10. Uma subextensão, para ser acrescentada, precisa de um nome único localmente no contexto da extensão editada, válido computacionalmente, além da cardinalidade e da URL que identifica a subextensão.
