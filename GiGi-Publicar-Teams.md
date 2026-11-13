# GiGi no Copilot Studio → publicar no Teams (passo a passo)

## 1. Criar o agente
1. Acesse **copilotstudio.microsoft.com** (com sua conta Equatorial/M365).
2. **Create → New agent** (ou "Novo agente"). Dê o nome **GiGi — Governança CSC**.
3. Em **Instructions / Instruções**, cole o texto de `GiGi-Instrucoes-CopilotStudio.md`.

## 2. Adicionar o conhecimento (o "cérebro treinado")
1. Abra a aba **Knowledge / Conhecimento → Add knowledge**.
2. Suba os arquivos:
   - `GiGi-Base-Conhecimento.md` (base exportada da GiGi);
   - os modelos **Definição do Escopo** e **Caderno de Homologação** (.docx, se quiser);
   - o PPTX de **Nomenclatura de Acordos (BMC Helix)**, se desejar.
   - (Opcional) conecte um **site do SharePoint** da Governança como fonte.
3. Em **Settings → Generative AI**, deixe **Generative answers** ligado e, se possível, marque
   "usar apenas o conhecimento fornecido" para evitar respostas fora do escopo.

## 3. Testar
- Use o painel **Test** à direita. Pergunte: "diferença entre SLA, OLA e CTR?" e
  "monte um caderno de homologação" para validar.

## 4. Publicar no Teams
1. Clique em **Publish / Publicar** (publique a versão).
2. Vá em **Channels / Canais → Microsoft Teams → Add / Turn on**.
3. **Availability options**: gere o link/pacote e escolha disponibilizar para você, para um time
   ou submeter ao **admin do Teams** para liberar à organização.
4. Abra no Teams: **Apps → procurar "GiGi — Governança CSC" → Adicionar**. Fixe no canal da equipe.

## 5. Acesso da equipe
- Por padrão, o agente exige login **Entra ID** (ideal para uso interno).
- Se o admin restringir apps personalizados, peça a **liberação do app** ao time de Teams/M365.

## Observações
- Motor: Copilot Studio usa **Azure OpenAI** (não Gemini) — as respostas podem variar do app GiGi.
- **Dados ao vivo** (processos/riscos/documentos do app) e **ações** (criar risco/processo) NÃO vêm
  automaticamente — exigem **Power Automate/conector** ou os dados em SharePoint/Dataverse
  (próxima etapa combinada).
- Para atualizar o conhecimento depois: reexporte com `node scripts/export-gigi-knowledge.mjs` e
  substitua o arquivo na fonte de conhecimento.
