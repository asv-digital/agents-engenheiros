# 57 Agents Engenharia — Claude Code para engenheiros e escritorios tecnicos

**57 subagentes especializados** para engenheiros civis, eletricistas, mecanicos, ambientais, de seguranca do trabalho e gestores de obra no Brasil, prontos para uso no Claude Code. Cada agente e um especialista em um calculo/peca/rotina especifica — projeto estrutural, eletrico, hidrossanitario, AVAC, orcamento SINAPI, ART, NRs, laudo pericial — que atua proativamente quando o contexto da conversa bate com sua especialidade.

## Como instalar (usando os zips desta pasta)

Voce tem **57 zips individuais** + este README. Pode instalar **um a um** (so quem voce vai usar) ou **todos de uma vez**.

### Opcao A — Instalar 1 agente individual

1. Baixe o zip do agente que voce quer (ex: `01-calculo-estrutural-concreto.zip`).
2. Descompacte. Dentro tem o `.md` do agente + um `COMO-INSTALAR.md` com o passo a passo.
3. Copie o `.md` para `.claude/agents/` (no seu projeto) ou `~/.claude/agents/` (global).
4. Reinicie o Claude Code (`/exit` e abra de novo). Pronto.

### Opcao B — Instalar todos os 57 de uma vez (terminal)

```bash
cd /caminho/onde/voce/baixou/57-Agents-Engenharia
mkdir -p ~/.claude/agents
for z in *.zip; do
  unzip -o -j "$z" "*.md" -d ~/.claude/agents/ -x "COMO-INSTALAR.md"
done
```

Reinicie o Claude Code. Confirme com `/agents`.

## Como usar

- **Automatico**: "preciso dimensionar fundacao de um galpao 600m² com SPT" -> Claude delega para `fundacao-rasa-sapata-radier` ou `fundacao-profunda-estaca`.
- **Manual**: "use o agente `PCMAT-NR-18-canteiro-obras` para canteiro de uma obra de 5.000m²".
- **Em pipeline**: `sondagem-SPT-laudo` -> `fundacao-profunda-estaca` -> `calculo-estrutural-concreto` -> `orcamento-analitico-SINAPI` -> `cronograma-fisico-financeiro`.

## Catalogo (57 agentes)

### Estrutural
01 Concreto armado NBR 6118 · 02 Aco NBR 8800 · 03 Madeira NBR 7190 · 04 Alvenaria estrutural NBR 15812/15961
05 Fundacao rasa NBR 6122 · 06 Fundacao profunda · 07 Contencao/arrimo · 08 Laje protendida · 09 Patologia estrutural

### Eletrica + telecom
10 Eletrico residencial NBR 5410 · 11 Eletrico industrial NBR 14039 · 12 SPDA NBR 5419 · 13 Entrada de energia
14 Quadro de cargas · 15 Fotovoltaico Lei 14.300 · 16 EVSE veiculo eletrico · 17 Cabeamento estruturado EIA-TIA

### Hidrossanitario, gas, PPCI
18 Hidrossanitario NBR 5626/8160 · 19 Esgoto/fossa NBR 7229 · 20 Aguas pluviais NBR 10844 · 21 Reuso/reservatorio
22 PPCI hidrantes/sprinklers NBR 13714/10897 · 23 Gas GLP/GN NBR 13523/15526 · 24 Piscina

### Mecanica + AVAC
25 AVAC NBR 16401 · 26 Ventilacao mecanica · 27 Cozinha industrial NBR 14518 · 28 Ar comprimido/vapor

### Orcamento, planejamento, execucao
29 Orcamento sintetico · 30 Orcamento analitico SINAPI/SBC · 31 BDI Acordao 2622 TCU · 32 Cronograma MS Project
33 Curva S e medicao · 34 EAP/WBS · 35 Last Planner System · 36 EVM PMI

### Topografia, geotecnia, terraplenagem
37 Planialtimetrico NBR 13133 · 38 Sondagem SPT NBR 6484 · 39 Drone/RTK · 40 Georreferenciamento INCRA · 41 Movimento de terra

### Ambiental
42 Licenciamento LP/LI/LO · 43 PRAD · 44 Outorga ANA · 45 PGRCC CONAMA 307 · 46 RAP/EIA/RIMA

### Seguranca do trabalho (NRs)
47 PCMAT NR-18 · 48 PGR/PCMSO NR-1/NR-7 · 49 LTCAT · 50 NR-35/NR-10 · 51 NR-12/NR-13 · 52 NR-33/NR-23

### Regulatorio, comercial, pericia
53 ART CREA · 54 Laudo pericial NBR 13752 · 55 Vistoria cautelar · 56 Contrato CONFEA

### IA aplicada (NOVO)
57 IA na engenharia (Revit MEP + AutoCAD AutoLISP + Claude pra dimensionamento + leitura SPT)

## Avisos legais

- Os agentes refletem CONFEA/CREA, NBRs ABNT, NRs do MTE, CONAMA, ANA, INMETRO, Lei 14.300/2022 (GD), e legislacao especifica vigente em 2026.
- Outputs gerados sao **rascunhos**; o engenheiro responsavel deve revisar e assumir a responsabilidade tecnica (ART/CREA).
- Templates e exemplos usam dados ficticios.

## Licenca

Uso permitido para clientes ASV Digital / Bravy. Nao redistribuir sem autorizacao.
