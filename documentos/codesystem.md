## User flow (criação de CodeSystem)

Uma instância de [CodeSystem](https://www.hl7.org/fhir/r4/codesystem.html) é empregada para definir o que também é conhecido por terminologia, ontologia ou enumeração.
De forma simplificada identifica "conceitos".

Um CodeSystem pode definir conceitos pertinentes por meio de propriedades básicas como _code_ (o código propriamente dito), o _display_
como o código deve ser exibido e _definition_, a definição do conceito. Um CodeSystem também pode estender um CodeSystem existente com representações (_designation_ e propriedades).

- Ao projetista está disponível a criação de instância de CodeSystem.
- O projetista requisita a criação.

- A criação pode ser de dois tipos: (a) para suplementar um CodeSystem existente ou (b) criar um novo.
- Opção (a). Ao criar um CodeSystem para suplementar um existente (_supplements_) é preciso identificar o CodeSystem para o qual o suplemento será criado. O CodeSystem a ser "suplementado" deve ser selecionado entre aqueles disponíveis na solução em edição.
- O suplemento inclui a definição de uma ou mais propriedades. Cada propriedade é definida por um código (nome da propriedade), uma uri, uma descrição e um tipo. O tipo está restrito a: _code_, _Coding_, _string_, _integer_, _boolean_, _dateTime_ ou _decimal_. Observe que o código e o tipo são obrigatórios, ao contrário dos demais. Um exemplo de propriedade está disponível no CodeSystem que define nomes de cores, neste caso, a propriedade RGB é acrescentada, conforme está ilustrado [aqui](https://www.hl7.org/fhir/codesystem-color-names.json.html).

- Quando se define um suplemento, além de definir as propriedades é necessário fornecer os valores correspondentes para cada conceito definido no CodeSystem para o qual o suplemento é criado. Observe que não é permitido acrescentar conceitos, mas valores para as propriedades definidas para cada um dos conceitos existentes.
- Opção (b). Na criação de um novo CodeSystem o projetista vê os campos principais pertinentes a um CodeSystem: identificador, título e descrição, dentre outros. Há muitos outros conforme a documentação do [recurso](http://hl7.org/fhir/r4/codesystem) e fornece os valores correspondentes.
- Convém observar que extensões podem ser acrescentadas ao CodeSystem ou a qualquer um dos atributos do CodeSystem. Ou seja, é preciso estar disponível ao projetista a seleção das extensões que deseja acrescentar, seja à instância como um todo ou a um atributo específico juntamente com o valor correspondente.
