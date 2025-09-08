# Salesforce CLI

## Instalação (Windows)

### Instalador oficial
- Baixe e instale o CLI: [Salesforce CLI](https://developer.salesforce.com/tools/salesforcecli)

### Via npm (opcional)
```npm install @salesforce/cli --global```
### Conferir instalação
```
sf --version
sfdx --version  # se ainda tiver SFDX antigo
```
## Autenticação
### Login via web
```
sf login org
sf auth:web:login -d -a myOrgAlias
```
### Listar orgs autenticadas
```
sf org list
```
## Deploy / Retrieve / Validate
### Deploy de código
```
sf project deploy start -x manifest\package.xml -u myOrgAlias
```
## Deploy com validação e execução de testes
```
sf project deploy validate -x manifest\package.xml -l RunLocalTests -u myOrgAlias
```
## Retrieve de metadados
```
sfdx force:source:retrieve -m ApexClass:MyClass -u myOrgAlias
```
## Queries e operações rápidas
## Executar SOQL
```
sf data query -q "SELECT Id, Name FROM Account" -u myOrgAlias
```
## Abrir org no browser
```
sf org open -u myOrgAlias
```
