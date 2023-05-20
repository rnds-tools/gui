## Objetivo

Ambiente de Design FHIR (ADF) é um software que oferece
funcionalidades para o _design_ de soluções FHIR.
O objetivo é propor uma interface para os usuários do ADF,
aqui denominados de projetistas.

> UX Designers não precisam dominar o padrão FHR,
> contudo, alguma noção é necessária. Consulte
> [aqui](documentos/fhir.md) para algumas orientações sobre o padrão.

## Produtos similares

- https://trifolia-fhir-dev.lantanagroup.com/lantana_hapi_stu3/home
- http://gb2.clinfhir.com/
- https://fire.ly/products/forge/

## Projetista FHIR (_persona_)

Um projetista é um profissional de saúde ou de tecnologia da informação.
Projetistas conhecem o padrão FHIR, FSH, FHIRPath e o que mais for  
preciso para adaptar o padrão a um contexto de uso.

Um projetista não necessariamente possui habilidades de programação.
Embora possua conhecimento e certa familiaridade com o padrão FHIR.
Em tempo, mesmo "veteranos" precisam consultar a especificação
do padrão, que é extensa e rica em detalhes.

> A expectativa dos projetistas é criar com rapidez e facilidade uma solução (modelagem FHIR).

## O que é uma solução FHIR (modelagem FHIR)?

Solução ou _design_ de uso do FHIR é um conjunto de instâncias de recursos (_resources_) FHIR.
Estas instâncias de recursos FHIR, ou simplesmente instâncias, definem como o FHIR deve
ser utilizado em um determinado cenário de interoperabilidade em saúde. Estas instâncias
definem dados terminológicos (terminologias), perfis, que são instâncias do recurso StructureDefinition e exemplos (instâncias de recursos que ilustram o uso de recursos).

E o que é um recurso (_resource_) FHIR?
É uma estrutura de dados para registro de um "item de informação em saúde".
Todo recurso pode ser adaptado, elementos podem ser acrescentados, removidos e
restrições sobre os itens de dados estabelecidas.

Uma solução ou _design_ de uso do FHIR pode agora ser redefinido como
um grafo de "itens de informação" adaptados. É um grafo porque recursos
estabelecem referências entre si.

Ao longo do processo de _design_ instâncias são criadas, algumas
são meramente ilustrativas. Verificações são feitas durante este processo,
idealmente, a cada pequeno ajuste na solução.

O diagrama abaixo esclarece a composição de uma solução, além de ilustrar
que o projetista cria uma solução ao "criar arquivos" nos formatos JSON, XML ou FSH.

![modelo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/rnds-tools/gui/main/diagramas/dominio.puml)

> IMPORTANTE: convém esclarecer que a figura acima é o conteúdo
> de uma solução e, não necessariamente, exige que o projetista sequer tenha
> que fazer uso direto destes formatos de arquivos.

## Organização

- As necessidades dos usuários (projetistas) e outras estão em [requisitos](documentos/requisitos.md).
- Rótulos, organização e _user flows_ em [arquitetura de informação](documentos/arquitetura-informacao.md).
- Documentação do usuário (projetista) para as funções de instalação, configuração e manutenção, via linha de comandos está em disponível em https://rnds-tools.github.io/userdoc/.
