## User flow (tipos de dados)

Estão disponíveis dezenas de [tipos de dados](http://hl7.org/fhir/r4/datatypes.html).
Aqui, em vez de apresentar o uso de um tipo no contexto de uma instância de recurso, observe 
que não existe edição de valor de tipo sem ser no contexto de uma instância, 
cada tipo deve ser considerado isoladamente. Ou seja, trata-se de um conjunto de
"micro" _flows_, um para cada tipo de dados. Observe que podem existir mais de uma
proposta para o mesmo tipo, conforme ilustrado abaixo para o tipo _boolean_.

Vejamos o tipo _boolean_, por exemplo, entre os mais simples. Aceita apenas
um de dois valores: _true_ ou _false_. Há pelo menos duas opções que talvez 
devam estar disponíveis: (a) uma na qual se opta pelo valor verdadeiro ou falso e 
(b) outra na qual se marca para indicar verdadeiro ou deixa desmarcado para indicar
falso. 
