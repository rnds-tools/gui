## User flow (criação de CodeSystem)

Uma instância de [CodeSystem](https://www.hl7.org/fhir/r4/codesystem.html) é empregada para definir o que também é conhecido por terminologia, ontologia ou enumeração.
De forma simplificada define "conceitos". 

Um CodeSystem também define alguns ou todos os conceitos pertinentes, juntamente com suas propriedades básicas como _code_ (o código propriamente dito), o _display_ 
como o código deve ser exibido e _definition_, a definição do conceito. Um CodeSystem também pode estender um CodeSystem existente com representações (_designation_ e propriedades).

- Ao projetista está disponível a criação de instância de CodeSystem.
- O projetista requisita a criação.
- A criação pode ser de dois tipos: para suplementar um CodeSystem existente ou criar um novo.
- Ao criar um CodeSystem para suplementar um existente (_supplements_) é preciso identificar o CodeSystem cujo suplemento será acrescentado. O suplemento inclui a definição de uma ou mais propriedades. Cada propriedade é definida por um código (nome da propriedade), uma uri (referência para a definição formal da propriedade), uma descrição e um tipo (que pode ser _code_, _Coding_, _string_, _integer_, _boolean_, _dateTime_ ou _decimal_). Observe que o código e o tipo são obrigatórios, ao contrário dos demais. Neste caso, para cada conceito do CodeSystem de origem o projetista deverá fornecer o valor correspondente para cada propriedade definida. 
- Na criação de um novo CodeSystem o projetista vê os campos principais pertinentes a um CodeSystem: identificador, título e descrição, dentre outros. Há muitos outros conforme a documentação do [recurso](http://hl7.org/fhir/r4/codesystem) e fornece os valores correspondentes.
