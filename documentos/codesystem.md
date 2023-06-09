## User flow (criação de CodeSystem)

Uma instância de [CodeSystem](https://www.hl7.org/fhir/r4/codesystem.html) é empregada para definir o que também é conhecido por terminologia, ontologia ou enumeração.
De forma simplificada define "conceitos". 

Um CodeSystem também define alguns ou todos os conceitos pertinentes, juntamente com suas propriedades básicas como _code_ (o código propriamente dito), o _display_ 
como o código deve ser exibido e _definition_, a definição do conceito. Um CodeSystem também pode estender um CodeSystem existente com representações (_designation_ e propriedades).

- Ao projetista está disponível a criação de instância de CodeSystem.
- O projetista requisita a criação.
- A criação pode ser para suplementar um CodeSystem existente. Neste caso, é preciso identificar o CodeSystem cujo suplemento será acrescentado e fornecer o conteúdo extra, ou seja, uma propriedade, que possui um código, descrição e tipo.
- O projetista vê os campos principais pertinentes a um CodeSystem: identificador, título e descrição. Há muitos outros conforme a documentação do [recurso](http://hl7.org/fhir/r4/codesystem).

