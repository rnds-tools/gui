## User flow (criação de Binary)

- Projetista fornece identificador único da instância (caso não queira aquele automaticamente fornecido). Este é o identificador lógico. Observe que todo [Resource](https://www.hl7.org/fhir/r4/resource.html), além de _id_, também possui os atributos _meta_, _implicitRules_ e _language_, que também devem ser considerados, apesar de não comentados abaixo. 
- Projetista fornece (seleciona) arquivo para _upload_, contendo o conteúdo correspondente à instância.
- Projetista deve informar se o conteúdo já está na Base64 ou não.
- Projetista fornece o mime-type correspondente ao arquivo (conteúdo).
- Projetista identifica instância de recurso existente. Usado para contexto de segurança (_securityContext_). 
