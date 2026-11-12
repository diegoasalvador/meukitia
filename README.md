# Meu Kit de IA — Suporte TI com Apontamento de Horas

Desafio de Projeto da [DIO](https://dio.me): monte o seu kit de IA para o dia a dia e delegue uma tarefa real, com você no comando.

> **Técnico (fictício):** Cyber Texugo | **Empresa (fictícia):** TexugoTech | **Área:** Suporte de TI

---

## Sobre este Projeto

Este kit foi construído para resolver uma tarefa real e repetitiva do dia a dia de um técnico de suporte de TI:
**registrar os chamados atendidos em uma planilha e gerar os textos de observações para o sistema de apontamento de horas.**

A IA assume o trabalho de ler a lista de chamados, agrupar por turno (manhã e tarde) e escrever o texto profissional pronto para colar no sistema — sem invenções, sem dados pessoais, sem retrabalho.

**Copie → adapte → teste → confira → use**

---

## O Que Tem no Kit

| Arquivo / Pasta | Para que serve |
|---|---|
| [kit-apontamento.md](kit-apontamento.md) | ✅ Atalhos, skill e delegação — o coração do projeto |
| [planilha-apontamento.csv](planilha-apontamento.csv) | Planilha com os 32 chamados simulados do dia |
| [base-chamados-dia.md](base-chamados-dia.md) | Base de chamados fictícios com todos os detalhes |
| [01-prompts](01-prompts) | Prompts prontos para escrita, pesquisa e comunicação |
| [02-templates](02-templates) | Templates: bom pedido, pesquisa e decisão, delegação |
| [03-checklists](03-checklists) | Checklists: Pare, Confira, Use / Revisar texto / Antes de delegar |
| [04-skills](04-skills) | Como estruturar uma skill reutilizável |
| [05-delegacao-e-automacao](05-delegacao-e-automacao) | Gatilhos de automação e supervisão com checkpoints |

---

## Os Frameworks Usados

- **Bom pedido:** contexto + instrução + objetivo + formato. Quanto menos a IA precisa adivinhar, melhor você consegue avaliar a resposta.
- **Atalhos reutilizáveis:** criar → testar → ajustar → salvar. O que é fixo fica na skill; o que muda (os chamados do dia) entra a cada uso.
- **Delegação:** objetivo + contexto + recursos + limites + sucesso. Autonomia funciona melhor quando o resultado esperado está claro.
- **Segurança:** pare → confira → use. Valide fatos, números e contexto antes de usar a resposta.

> A IA ajuda a estruturar e escrever. A responsabilidade pelo apontamento correto continua sendo do técnico.

---

## Minha Entrega

### Minha Tarefa Real

Escolhi a tarefa de **registrar chamados de suporte no sistema de apontamento de horas**.

Como técnico de TI, atendo chamados presenciais e remotos ao longo do dia. No fim do expediente preciso preencher o sistema com dois registros — um para o turno da manhã (08:00–12:00) e outro para o turno da tarde (14:00–18:00) — descrevendo tudo que foi feito no campo Observações. Essa tarefa é repetitiva, manual e cansativa depois de um dia cheio de atendimentos. Automatizá-la com IA economiza tempo e garante um texto mais profissional.

---

### Meus Atalhos

**O que ficou fixo:** a estrutura do texto de Observações, o formato por turno e as regras de escrita (sem bullet points, texto corrido, tom técnico).

**O que muda a cada uso:** os chamados do dia, copiados da planilha CSV.

```text
ATALHO 1 — Transformar Chamados em Observações de Apontamento

CONTEXTO
Sou técnico de suporte de TI. Atendo chamados presenciais e remotos ao longo do dia.
Preciso preencher o sistema de apontamento de horas com dois registros por dia:
- Turno Manhã: 08:00 às 12:00
- Turno Tarde: 14:00 às 18:00

INSTRUÇÃO
Leia os chamados abaixo e gere dois blocos de texto para o campo Observações:
1. Um texto resumindo os chamados do turno da manhã (08:00–12:00)
2. Um texto resumindo os chamados do turno da tarde (13:00–17:00)

OBJETIVO
O texto será colado no campo Observações do sistema de apontamento.
Deve ser claro, profissional e listar o que foi feito em cada atendimento.

FORMATO
- Sem títulos ou subtítulos
- Sem bullet points
- Texto corrido, separado por ponto-e-vírgula
- Tom técnico e direto
- Máximo 4 linhas por turno

CHAMADOS DO DIA:
[cole aqui as linhas da planilha do turno correspondente]
```

```text
ATALHO 2 — Skill de Apontamento (Instrução Fixa Reutilizável)

Você é um assistente de apontamento de horas para técnico de suporte de TI.

Sempre que receber uma lista de chamados, faça:

1. Separe os chamados em dois grupos:
   - MANHÃ: horários de início entre 08:00 e 12:00
   - TARDE: horários de início entre 13:00 e 17:00

2. Para cada grupo, escreva um parágrafo único de Observações com:
   - O que foi feito (ação tomada)
   - Em qual setor foi atendido
   - Resultado do atendimento
   - Sem repetir o número do chamado
   - Texto corrido, profissional, máximo 4 linhas

3. Entregue no formato:
   === APONTAMENTO MANHÃ (08:00–12:00) ===
   [texto das observações]

   === APONTAMENTO TARDE (14:00–18:00) ===
   [texto das observações]
```

---

### Minha Delegação

```text
OBJETIVO
Transformar os chamados de suporte do dia em dois textos de Observações
prontos para colar no sistema de apontamento de horas.

CONTEXTO
Sou técnico de TI da TexugoTech (empresa fictícia). Atendo chamados remotos
e presenciais ao longo do dia. No fim do dia preciso registrar no sistema dois
apontamentos: um para o turno da manhã (08:00–12:00) e um para o turno da
tarde (14:00–18:00). O campo Observações é um editor de texto simples onde
descrevo o que foi feito nos atendimentos do período.

RECURSOS
Planilha CSV com os seguintes campos por chamado:
Data, Chamado, Tipo, Modalidade, Setor, Usuario, Descricao do Problema,
Resolucao, Hora Inicio, Hora Fim, Horas Gastas, Status

LIMITES
- Não inventar chamados ou soluções que não estão na planilha
- Não usar bullet points no texto final (o sistema não formata bem)
- Não incluir dados pessoais dos usuários no texto de Observações
- Manter o texto técnico e objetivo
- Máximo de 4 linhas por turno

SUCESSO
Recebo dois blocos de texto prontos para copiar e colar no sistema,
um para o turno da manhã e um para o turno da tarde,
sem precisar editar nada manualmente.

Antes de começar, confirme como vai estruturar os dois textos.
```

---

### O Plano da IA

Antes de executar, a IA confirmou o plano:

> "Vou ler a planilha CSV, separar os chamados pelo horário de início (manhã: 08:00–12:00 / tarde: 13:00–17:00), e para cada turno escrever um parágrafo técnico em texto corrido, sem bullet points, listando o que foi feito por setor e qual foi o resultado. Entrego dois blocos prontos para colar no sistema."

Ajuste feito antes de executar: confirmei que o formato devia usar ponto-e-vírgula entre os atendimentos, não vírgula, para ficar mais legível no campo Observações do sistema.

---

### O Resultado

**Apontamento Manhã — 08:00 às 12:00 (4h):**

```
Atendimentos realizados no turno da manhã: impressora em rede offline na Contabilidade
com fila de impressão liberada; configuração de rede corrigida no Financeiro após
atualização do Windows; teclado substituído no setor de Compras por dano causado por
líquido; instalação do Office 365 em notebook novo no Comercial; falha no sistema de
ponto eletrônico do RH resolvida com reinstalação de driver biométrico; estação de
trabalho do TI sem POST corrigida com troca de fonte; erro no TOTVS Protheus para
emissão de nota fiscal resolvido via atualização de DLL; lentidão de rede identificada
como loop em switch e corrigida; mouse com defeito substituído no Almoxarifado; leitor
de código de barras reconfigurado no Comercial; Windows Update desbloqueado no
Atendimento; certificado digital A3 do Jurídico revalidado; Power BI Desktop do
Financeiro reconectado à fonte de dados; impressora jato de tinta com cabeça limpa e
cartucho substituído; Wi-Fi corrigido de IP estático para DHCP.
```

**Apontamento Tarde — 14:00 às 18:00 (4h):**

```
Atendimentos realizados no turno da tarde: Adobe Acrobat do Jurídico atualizado e
cache limpo; VPN corporativa reconfigurada com renovação de certificado; CRM do
Comercial com cache limpo e banco desfragmentado; notebook encaminhado para troca
de bateria; usuário do Jurídico desbloqueado no Active Directory; Excel do Administrativo
reparado com reativação de macros; monitor corrigido via atualização de driver de vídeo;
antivírus atualizado com whitelist aplicada; e-mail corporativo reconfigurado no celular
com 2FA reativado; sistema de rastreamento da Logística restaurado via rollback; webcam
com driver reinstalado e permissões ajustadas; impressora de rede remapeada com IP
fixo; HD externo recuperado via Testdisk; ramal VoIP reconfigurado no servidor Asterisk;
Teams reinstalado após limpeza de cache; permissões NTFS reconfiguradas no novo
servidor de arquivos.
```

Como conferi antes de usar:
- ✅ Nenhum chamado foi inventado — tudo veio da planilha
- ✅ Nenhum nome de usuário foi incluído no texto
- ✅ Sem bullet points — texto corrido compatível com o sistema
- ✅ Os setores e ações batem com os dados da planilha CSV
- ✅ Apliquei o checklist **Pare, Confira, Use** antes de salvar no sistema

---

### Como Foi para Você

Antes de usar a IA, preencher o apontamento levava uns 15 minutos no fim do dia — cansativo depois de 8 horas de suporte. Com o kit montado, o processo virou: abrir a planilha, colar os chamados no prompt, revisar o texto gerado e salvar no sistema. O texto saiu mais profissional do que o que eu escrevia correndo. A parte mais importante que aprendi: a IA não pode ser responsável pelo apontamento — ela ajuda a escrever, mas eu preciso conferir cada linha antes de salvar.

