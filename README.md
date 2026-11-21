# Dados dos Avisos Acadêmicos — IFTO Campus Palmas

Este repositório mantém os dados públicos consumidos pelo Portal Acadêmico. O arquivo publicado na `main` segue o contrato `avisos.v1`.

## Separação de responsabilidades
- **Este repositório:** histórico Git e arquivo de dados públicos `avisos.json`.
- **Repositório Portal:** interface, validador/build e código Apps Script/documentação operacional.
- **Planilha institucional GEAE:** cadastro, validação, aprovação e trilha de operação.
- **Cloudflare Pages:** prévia e produção do Portal.

## Fluxo operacional
A operação está documentada no repositório principal:
- [Instalação e configuração](https://github.com/thiagoifto/portal-academico-palmas/blob/main/admin/apps-script-avisos/INSTALACAO-AVISOS.md)
- [Contrato avisos.v1](https://github.com/thiagoifto/portal-academico-palmas/blob/main/admin/avisos/CONTRATO-avisos-v1.md)
- [Plano de implantação e reversão](https://github.com/thiagoifto/portal-academico-palmas/blob/main/admin/avisos/PLANO-IMPLANTACAO-PRODUCAO.md)
- [Roteiro operacional GEAE](https://github.com/thiagoifto/portal-academico-palmas/blob/main/admin/avisos/ROTEIRO-OPERACIONAL-GEAE.md)

Resumo: planilha → validação → publicação na branch de prévia → conferência do hash → solicitação de PR → aprovação institucional por pessoa distinta → merge squash → conferência do Portal.

## Regras
- Não fazer push direto na `main`; produção ocorre pelo PR/merge autorizado.
- Não usar dados fictícios na produção.
- Não inserir tokens, hooks, credenciais, propriedades Apps Script ou IDs privados neste repositório.
- Não editar `avisos.json` manualmente como substituto do fluxo institucional, salvo tarefa expressamente autorizada.
- Preservar o histórico Git; reversões devem ser commits novos, nunca reescrita de histórico.
- O ruleset da branch default exige PR e Squash, bloqueia exclusão e non-fast-forward. A aprovação institucional está descrita no fluxo da planilha; o ruleset atualmente não exige aprovação GitHub.

## Alterações
Toda mudança de contrato ou estrutura deve ser coordenada com o repositório Portal e sua validação de build. Não duplicar aqui o código ou a documentação integral mantida no Portal.
