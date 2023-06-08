## Extensão

Uma extensão é o mecanismo oferecido pelo padrão FHIR
para complementar as informações de um recurso com um tipo de dados predefinido. Detalhes em:

- https://www.hl7.org/fhir/r4/extensibility.html
- https://hl7.org/fhir/uv/shorthand/reference.html#defining-extensions
- https://www.hl7.org/fhir/r4/defining-extensions.html

### Criar extensão

1. O usuário requisita criação de uma extensão.
1. O usuário fornece um identificador (nome válido computacionalmente). A partir deste identificador é montada a URL que identifica a extensão.
1. O usuário fornece um título.
1. O usuário fornece uma descrição.
1. O usuário identifica se a extensão reúne várias outras extensões, ou seja, se é do tipo complexo ou, caso contrário, simples. O tipo complexo é definido por uma extensão que reúne subextensões.
1. Se simples, então identifica o valor correspondente dentre [dezenas](https://www.hl7.org/fhir/r4/extensibility.html) de opções.
1. Se o tipo da extensão é complexo, então é preciso estabelecer cada uma das subextensões. Observe que uma extensão ou possui subextensões, tipo complexo, ou um valor, tipo simples. Nunca ambos.
1. Uma subextensão, para ser acrescentada, precisa de um nome único localmente, válido computacionalmente, a cardinalidade e a URL que identifica a subextensão.
