## Versão enxuta

Um projetista de solução FHIR
edita arquivos em FHIR Shorthand (FS) usando um editor
como o Visual Code. Toda vez que um arquivo é alterado,
este é submetido para conversão para
o formato JSON. Há um serviço que monitora um diretório (mfsh) e,
na ocorrência de mudança, recupera o arquivo e o envia para
o serviço de conversão (fsh2fhir). Se conversão é realizada de forma 
satisfatória, um arquivo JSON correspondente é produzido.
Toda vez que um arquivo JSON é produzido ou alterado, o serviço que
monitora JSONs (mjson) o recupera e o submete para o serviço de validação (vfhir).  
O resultado é uma instância da classe [OperationOutcome](https://www.hl7.org/fhir/r4/operationoutcome.html)
serializada em JSON. 

A interface enxuta deve:

- permitir a configuração dos diretórios monitorados, onde
são depositados os arquivos ou atualizações em arquivos FHIR Shorthand e/ou JSON (arquivos
convertidos);
- exibir os status dos serviços de monitoramento, mfsh e mjson estão
ativos, bem como os serviços fsh2fhir e vfhir;
- exibir os resultados oferecidos pelos serviços de conversão e validação.

## Expectativa

Usuário (projetista) edita arquivos no Visual Code, por exemplo, e a interface 
gráfica, aplicação web a ser desenvolvida, exibe o status do serviço de tal 
forma que ele facilmente possa acompanhar os arquivos alterados e as alterações por
arquivo juntamente com os resultados correspondentes. 
