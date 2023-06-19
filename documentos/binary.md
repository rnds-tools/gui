## User flow (criação de Binary)

- Projetista fornece identificador único da instância (caso não queira aquele automaticamente fornecido). Este é o identificador lógico. Atributo de todo [Resource](https://www.hl7.org/fhir/r4/resource.html). Demais atributos de todo Resource também devem ser considerados, embora não comentados abaixo.
- Projetista fornece (seleciona) arquivo para _upload_, contendo o conteúdo correspondente à instância.
- Projetista deve informar se o conteúdo já está na Base64 ou não.
- Projetista fornece o mime-type correspondente ao arquivo (conteúdo).
- Projetista identifica instância de recurso existente. Usado para contexto de segurança (_securityContext_). 
