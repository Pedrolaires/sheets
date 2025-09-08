# Salesforce Code Analyzer

## Instalação (Windows)

### Plugin Salesforce CLI

```
sf plugins install @salesforce/sfdx-scanner
sf plugins
```
## Engines
- PMD → Bad practices, estilo e manutenção de Apex/Visualforce/Lightning
- CPD → Duplicação de código
- SFGE (Salesforce Graph Engine) → Fluxo de dados, segurança e melhores práticas
- ESLint → Para JavaScript / LWC

## Exemplos de execução

### Rodar todas as engines em uma classe
```
sf scanner:run --target "force-app\main\default\classes\MyClass.cls" --engine pmd,cpd,sfge --format table
```

### Saída em JSON
```
sf scanner:run --target "force-app\main\default\classes\MyClass.cls" --engine pmd,cpd,sfge --format json --outfile scan-results.json
```

### Saída em SARIF (Graph Emgine)
```
sf scanner:run --target "force-app\main\default\classes\MyClass.cls" --engine sfge --format sarif --outfile scan-results.sarif
```


### Rodar PMD com ruleset customizado
```
sf scanner:run --target "force-app\main\default\classes\MyClass.cls" --ruleset "sfdx-scanner\ruleset.xml" --engine pmd --format table
```



---

## **Fontes:**
- [Salesforce CLI Documentation](https://developer.salesforce.com/docs/platform/salesforce-cli/overview)
- [Salesforce Code Analyzer Guide](https://developer.salesforce.com/docs/platform/salesforce-code-analyzer/guide/salesforce-code-analyzer.html)
- [Salesforce Graph Engine](https://developer.salesforce.com/docs/platform/salesforce-code-analyzer/guide/salesforce-graph-engine.html)
- [PMD Apex Ruleset](https://pmd.github.io/latest/pmd_rules_apex.html)
