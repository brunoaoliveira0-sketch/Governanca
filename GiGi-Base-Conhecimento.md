# Base de Conhecimento da GiGi — Governança CSC
> Exportado em 13/11/2026, 07:52:21 · 30 itens.
> Suba este arquivo como "Fonte de conhecimento" no Copilot Studio (ou em um site do SharePoint).

## Avaliar risco de uma mudança para o CAB
_Palavras-chave: mudanca, cab, risco de mudanca, rfc, rollback_

Para avaliar o risco de uma mudança, considere: probabilidade e impacto da falha, janela de mudança, dependências (ICs afetados no CMDB), reversibilidade (plano de rollback testado), cobertura de testes e comunicação. Classifique em baixo/médio/alto e verifique a prontidão para o CAB (plano de implementação, teste e recuperação presentes).

## BPMN: elementos essenciais
_Palavras-chave: bpmn, evento, gateway, atividade, raia, pool, notacao_

Eventos (círculos): início, intermediário, fim (gatilhos: mensagem, timer, erro). Atividades (retângulos arredondados): tarefa e subprocesso. Gateways (losangos): Exclusivo "X" (um caminho), Paralelo "+" (simultâneos), Inclusivo "O". Conectores: fluxo de sequência (seta cheia) e de mensagem (tracejada). Pool = participante; Lane (raia) = papel/área. Boas práticas: esquerda→direita, caminho principal reto, decisões como pergunta com saídas rotuladas, evitar cruzamento de linhas.

## Camada CTR — o que se mede do fornecedor
_Palavras-chave: ctr, fornecedor, contrato, penalidade, credito de servico, disponibilidade, backlog, metrica_

Do fornecedor o contrato mede além do SLA — cada métrica tem penalidade e crédito de serviço e é modelada como medição própria no Helix: Tempo de resposta (até assumir o chamado), Tempo de solução (até resolver, por prioridade), Disponibilidade (% de uptime), Backlog (chamados em aberto acima do limite), Atendimento (aderência ao processo, reabertura, satisfação), Penalidades (descontos por descumprir metas) e Créditos de serviço.

## Catálogo de Serviços e Executor (Interno/Fornecedor/Compartilhado)
_Palavras-chave: catalogo, executor, interno, fornecedor, compartilhado, helix, dominio, superintendencia_

O catálogo da Governança alinha domínios de TI às superintendências reais (Sistemas Corporativos/Técnicos, Cloud/Infra, Telecom/Telefonia, Field Service, Monitoramento, Cibersegurança, Banco de Dados, Backup) e estende-se aos demais serviços do CSC (Suprimentos, Frotas, Imóveis, Folha, Contas a Pagar). O campo EXECUTOR define a camada: Interno (equipe própria → OLA), Fornecedor (terceiro contratado → CTR) e Compartilhado (interno + fornecedor no mesmo fluxo, encadeando OLA e CTR ao SLA).

## Como pedir um fluxo assertivo à GiGi
_Palavras-chave: gigi, fluxo, processo, dica, prompt_

Para um fluxo assertivo, informe: o nome do processo, o gatilho (o que inicia), os atores/raias, as atividades em ordem, as decisões (com os caminhos SIM/NÃO), exceções e o fim. A GiGi devolve o texto estruturado pronto para o editor. Quanto mais claro o material (ou o anexo), mais fiel o resultado.

## Como usar o módulo de Auditoria
_Palavras-chave: auditoria, itgc, sox, caderno de desenho, roteiro de teste, como usar_

Auditoria cobre o ciclo de controles (base ITGC/SOX): cadernos de desenho de controle, roteiros de teste de efetividade e um painel de BI. Avalia o DESENHO (o controle mitiga o risco?) e a EFETIVIDADE OPERACIONAL (operou no período?), com resultado Efetivo/Não Efetivo e plano de ação quando há deficiência.

## Como usar o módulo de Documentos
_Palavras-chave: documentos, pop, procedimento, politica, versao, como usar_

Documentos cria POPs, procedimentos, políticas, instruções e manuais com modelo padronizado, controle de versões e fluxo de aprovação (rascunho → em revisão → aprovado). Cada documento tem nota de qualidade (0–100) e exportação em PDF e .docx (Word). Todos os usuários veem e exportam; apenas o dono/admin edita.

## Como usar o módulo de Governança
_Palavras-chave: governanca, risco, controle, plano de acao, indicador, kpi, como usar_

Governança concentra Riscos (probabilidade × impacto), Controles internos (preventivo/detectivo/corretivo), Planos de Ação (responsável e prazo) e Indicadores (KPIs com meta). Mantém a rastreabilidade entre processos, riscos e controles.

## Como usar o módulo de Processos
_Palavras-chave: processos, fluxograma, editor, sintaxe, como usar_

No módulo Processos você escreve o processo em TEXTO ESTRUTURADO e o sistema gera o fluxograma (e vice-versa). Sintaxe: INICIO / FIM; ATIVIDADE: texto @Responsável !gargalo !retrabalho; DECISAO: pergunta? com blocos SIM:/NAO: indentados (Tab/2 espaços) ou forma curta "SIM -> alvo"; ENTRADA:/SAIDA:/SUBPROCESSO:/DADOS:; RISCO:/CONTROLE:. No editor visual há piscinas e raias (a raia encaixa magneticamente na piscina), seleção múltipla, cores, negrito/fonte, alinhamento e exportação PNG/PDF.

## Continuidade de Negócios (ISO 22301)
_Palavras-chave: continuidade, iso 22301, bcp, dr, bia, contingencia_

A continuidade garante que serviços críticos (folha, pagamentos, TI) operem em contingências. Inclui análise de impacto (BIA), estratégias de continuidade, plano de continuidade (BCP) e de recuperação de desastres (DR), com testes e exercícios periódicos.

## COSO e COBIT (controles e governança de TI)
_Palavras-chave: coso, cobit, controles internos, governanca de ti, erm_

COSO estrutura controles internos em 5 componentes (ambiente de controle, avaliação de riscos, atividades de controle, informação/comunicação, monitoramento) e sustenta o ERM. COBIT governa e gere a TI corporativa, separando governança (avaliar, dirigir, monitorar) da gestão (planejar, construir, executar, monitorar). Complementam ITIL (operação) e base de SOX.

## De-para ServiceNow → BMC Helix (campos dos acordos)
_Palavras-chave: de-para, depara, servicenow, helix, migracao, service target, milestone, start stop_

Mapeamento dos campos: Camada/Acordo (Tipo ANS/OLA/Contrato → Service Target SLA|OLA|Underpinning Contract); Código (não existia → ID do Service Target: SLA_/OLA_/CTR_ + domínio); Serviço (Superintendência/Área → Business Service/Service no catálogo); Classe do registro (INC/REQ/CHG → Incident/Service Request/Change); Gatilho da meta (Condição de início → Start/Stop conditions); Métrica (Resposta/Resolução → Milestones); Prioridade/Prazo (PrioridadeMeta·Duracao_horas → Priority·Goal time/schedule); Responsável (Executor → Support Group/Vendor + encadeamento).

## Fluxo de aprovação de documentos no sistema
_Palavras-chave: documento, aprovacao, rascunho, revisao, aprovado, versao_

O documento segue: Rascunho → Em revisão → Aprovado. Ao aprovar, recomenda-se nota de qualidade adequada e registro de versão. O sistema pode notificar o Teams na aprovação. Documentos aprovados devem ser revisados periodicamente conforme a política.

## Gestão de Catálogo de Serviços
_Palavras-chave: catalogo, servico, oferta, catalog curator, formulario_

Definir um serviço do catálogo envolve: nome da oferta, parent/categoria, tipo do item, palavras-chave, formulário de abertura (campos obrigatórios, tipos e condições de exibição), fluxo de atendimento por raia, grupo resolvedor e SLA/OLA, e visualização. Colete as informações com o dono/administrador do catálogo antes de publicar.

## Gestão do Conhecimento (KCS) — artigos
_Palavras-chave: conhecimento, kcs, artigo, base de conhecimento, documentar_

Capture o conhecimento no fluxo de trabalho: ao resolver um incidente, registre um artigo (sintoma, causa, solução, validação). Reaproveite e revise os artigos existentes. Bons artigos têm título claro, passos reproduzíveis e são revisados periodicamente (evitar conteúdo desatualizado).

## Governança de CSC — visão geral
_Palavras-chave: csc, governanca, catalogo, nivel de atendimento, backlog, nps_

O CSC concentra serviços de apoio (RH, financeiro, suprimentos, TI, facilities) para ganhar escala, padronização e foco no cliente interno. Governança: catálogo de serviços; acordos de nível (SLA/OLA/UC); indicadores (volume, tempo médio de atendimento, aderência ao SLA, backlog/aging, NPS); atendimento em níveis (N1 central, N2 especialistas, N3 fornecedores); melhoria contínua; e comitês de governança.

## Indicadores (KPIs) de um CSC
_Palavras-chave: indicador, kpi, metrica, sla, backlog, nps, tma_

KPIs típicos: volume de chamados, Tempo Médio de Atendimento (TMA), aderência ao SLA, resolução no primeiro contato (FCR), backlog e aging, reabertura, e satisfação (CSAT/NPS). Defina meta, unidade, polaridade (para cima/para baixo) e periodicidade; acompanhe tendência, não só o valor do mês.

## ITIL: diferença entre incidente, requisição, problema e mudança
_Palavras-chave: itil, incidente, requisicao, problema, mudanca, diferenca_

Incidente = interrupção não planejada de um serviço (foco: restaurar rápido). Requisição de Serviço = pedido padrão/pré-aprovado (ex.: novo acesso). Problema = causa raiz de incidentes (recorrentes ou de alto impacto). Mudança (RFC) = alteração controlada, avaliada por risco e, quando normal, aprovada pelo CAB.

## Lean Six Sigma e DMAIC
_Palavras-chave: lean, six sigma, dmaic, melhoria continua, desperdicio, eficiencia_

Lean elimina desperdícios e maximiza valor; Six Sigma reduz variação/defeitos pelo método DMAIC (Definir, Medir, Analisar, Melhorar, Controlar). No CSC, ajuda a reduzir tempo de ciclo, retrabalho e a padronizar atendimentos. Desperdícios clássicos (Lean): espera, retrabalho, movimentação, estoque, superprodução, transporte, processamento excessivo.

## LGPD no CSC (dados pessoais)
_Palavras-chave: lgpd, privacidade, dados pessoais, base legal, titular, anpd_

Todo tratamento de dados pessoais precisa de base legal (consentimento, obrigação legal, execução de contrato, legítimo interesse...). Respeite os direitos do titular (acesso, correção, eliminação), os princípios (finalidade, necessidade, minimização, segurança) e comunique incidentes à ANPD quando aplicável. Mantenha inventário (ROPA).

## Matriz RACI (papéis e responsabilidades)
_Palavras-chave: raci, papeis, responsavel, aprovador, consultado, informado_

A RACI define, por atividade, quem é R (Responsável — executa), A (Aprovador — responde pelo resultado, único por atividade), C (Consultado — dá insumo) e I (Informado — recebe comunicação). Use para eliminar lacunas e sobreposição de responsabilidades nos processos.

## Modelo: Caderno de Homologação (Governança CSC)
_Palavras-chave: homologacao, caderno de homologacao, modelo, template, vlreqgov, validacao_

Valida os requisitos do escopo. Estrutura: Histórico de Versões; 1. Objetivo; 2. Escopo (2.1 Exclusões, 2.2 Validações); 3. Resultado da Homologação; 4. Considerações finais; 5. Anexos. Cada requisito REQGOV-00x é validado por VLREQGOV-00x (mesmo código com prefixo VL), com resultado Validado ou Reprovado; ao final conclui HOMOLOGADO ou NÃO HOMOLOGADO.

## Modelo: Definição do Escopo (Governança CSC)
_Palavras-chave: escopo, definicao do escopo, modelo, template, reqgov, catalogo, mapeamento_

Estrutura oficial: Histórico de Versões; 1. Objetivo; 2. Escopo (2.1 Exclusões, 2.2 Visão Geral, 2.3 Requisitos). Dois submodelos (escolher um): (A) Ofertar um Serviço no Catálogo (Nome da Oferta, Parent/Categoria, Tipo, Palavra-chave, Formulário e Campos, Fluxo de Atendimento, Grupo e SLA, Visualização) e (B) Mapeamento de Processos (processos, objetivos, limites, stakeholders, ferramenta, normativos, indicadores, homologação). Requisitos são identificados como REQGOV-00x. Fecha com 3. Considerações finais e 4. Anexos.

## Nomenclatura de Acordos no BMC Helix (SLA · OLA · CTR)
_Palavras-chave: bmc helix, helix, nomenclatura, sla, ola, ctr, service target, acordo, underpinning contract, migracao, servicenow_

Padrão de nomenclatura da Governança CSC para a migração ServiceNow → BMC Helix. Três camadas (classes oficiais de acordo): SLA (acordo com o cliente/serviço), OLA (acordo operacional interno, equipe própria) e CTR (Underpinning Contract, com fornecedor terceiro). Cada Service Target recebe CÓDIGO + NOME DESCRITIVO: prefixo SLA_/OLA_/CTR_ + domínio. No Helix o "Tipo = ANS/OLA/Contrato de sustentação" vira Service Target (SLA | OLA | Underpinning Contract). Regra de ouro: migrar por campo estruturado (código + nome), sem recadastrar manualmente.

## O que a GiGi faz com anexos (requisito/desenho)
_Palavras-chave: gigi, anexo, requisito, escopo, desenho, fluxo, analista_

Anexe (📎) um requisito/escopo (.docx/.pdf) e peça o fluxo: a GiGi gera o TEXTO ESTRUTURADO com botão "Abrir no editor de Processos" já preenchido. Anexe um desenho (imagem/PDF) e peça o requisito/escopo: ela escreve o documento no padrão da casa, com Copiar/Baixar .md/.docx. Ela atua como analista de processos sênior.

## Post-Mortem / Análise de Causa Raiz (5 Porquês)
_Palavras-chave: post-mortem, causa raiz, 5 porques, rca, problema, ishikawa_

No post-mortem (sem culpabilizar): monte a linha do tempo, descreva o impacto, o que funcionou e o que falhou. Para a causa de fundo, aplique os 5 Porquês (pergunte "por quê?" sucessivamente) ou o diagrama de Ishikawa. Registre o erro conhecido (KEDB) e gere ações preventivas rastreáveis com responsável e prazo.

## Priorização de incidentes (impacto × urgência)
_Palavras-chave: incidente, prioridade, impacto, urgencia, p1, severidade_

A prioridade do incidente vem da combinação Impacto (quantos/como são afetados) × Urgência (quão rápido precisa ser resolvido), gerando P1 (crítico) a P4/P5 (baixo). P1/P2 exigem acionamento e comunicação imediatos; registre sempre categoria, prioridade e prazo (SLA).

## Qualidade de dados no CMDB
_Palavras-chave: cmdb, configuracao, ic, qualidade de dados, cmdb governor_

A governança do CMDB identifica Itens de Configuração (ICs) incompletos, duplicados ou órfãos (sem relação/dono), analisa a causa (origem do dado, processo de cadastro) e recomenda correção. ICs confiáveis sustentam análise de impacto de mudanças e de incidentes.

## Qualidade de documentos (POP) no sistema
_Palavras-chave: pop, qualidade, documento, padronizacao, atividades_

Um bom POP tem: objetivo claro, abrangência/escopo, responsáveis (RACI), definições, recursos/materiais, atividades em passos numerados (verbo no infinitivo + objeto), controles/pontos de verificação, indicadores e referências. O sistema calcula uma nota de qualidade e sugere melhorias; recomenda-se revisar antes de aprovar.

## SLA, OLA e Contrato de Apoio (UC)
_Palavras-chave: sla, ola, uc, contrato, acordo, nivel de servico_

SLA (Service Level Agreement): acordo com o cliente/área demandante. OLA (Operational Level Agreement): acordo operacional interno entre times do CSC. UC/Contrato de Apoio: acordo com fornecedor externo. No CSC, a palavra "SLA" costuma ser usada de forma ampla — ao consultar, considere também OLAs e Contratos de Sustentação relacionados.
