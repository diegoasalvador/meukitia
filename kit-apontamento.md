# Kit de IA — Apontamento de Horas no Sistema

**Técnico:** Cyber Texugo | **Data:** 12/11/2026

---

## Como Funciona o Fluxo

```
Planilha CSV (chamados do dia)
        ↓
   IA agrupa por turno
        ↓
 Gera texto de Observações
        ↓
  Você cola no sistema e salva
  (2 apontamentos por dia)
```

---

## 🔧 Atalho 1 — Transformar Chamados em Texto de Observações

**Quando usar:** No fim do dia, para transformar a lista de chamados em texto pronto para o campo Observações do sistema.

```text
CONTEXTO
Sou técnico de suporte de TI. Atendo chamados presenciais e remotos ao longo do dia.
Preciso preencher o sistema de apontamento de horas (Sistema) com dois registros por dia:
- Turno Manhã: 08:00 às 12:00
- Turno Tarde: 14:00 às 18:00

INSTRUÇÃO
Leia os chamados abaixo e gere dois blocos de texto para o campo Observações:
1. Um texto resumindo os chamados do turno da manhã (08:00–12:00)
2. Um texto resumindo os chamados do turno da tarde (13:00–17:00)

OBJETIVO
O texto será colado no campo Observações do sistema GAO.
Deve ser claro, profissional e listar o que foi feito em cada atendimento.
Formato: lista corrida, sem bullet points, separada por vírgulas ou ponto e vírgula.

FORMATO
- Sem títulos ou subtítulos
- Sem bullet points
- Texto corrido, separado por vírgula ou ponto-e-vírgula
- Tom técnico e direto
- Máximo 3 linhas por turno

CHAMADOS DO DIA:
[cole aqui as linhas da planilha do turno correspondente]
```

---

## 🔧 Atalho 2 — Skill de Apontamento (Instrução Fixa)

**O que é fixo:** a estrutura e o formato do texto de Observações
**O que muda a cada uso:** os chamados do dia

```text
Você é um assistente de apontamento de horas para técnico de suporte de TI.

Sempre que receber uma lista de chamados, faça:

1. Separe os chamados em dois grupos:
   - MANHÃ: horários de início entre 08:00 e 12:00
   - TARDE: horários de início entre 13:00 e 17:00

2. Para cada grupo, escreva um parágrafo único de Observações com:
   - O que foi feito (ação tomada)
   - Em qual setor/usuário
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

## 📋 Delegação — Template Preenchido

```text
OBJETIVO
Transformar os chamados de suporte do dia em dois textos de Observações
prontos para colar no sistema de apontamento de horas.

CONTEXTO
Sou técnico de TI da TexugoTech. Atendo chamados remotos e presenciais
ao longo do dia. No fim do dia preciso registrar no sistema dois apontamentos:
um para o turno da manhã (08:00–12:00) e um para o turno da tarde (14:00–18:00).
O campo Observações do sistema é um editor de texto simples onde descrevo
o que foi feito nos atendimentos do período.

RECURSOS
Planilha CSV com os seguintes campos por chamado:
Data, Chamado, Tipo, Modalidade, Setor, Usuario, Descricao do Problema,
Resolucao, Hora Inicio, Hora Fim, Horas Gastas, Status

LIMITES
- Não inventar chamados ou soluções que não estão na planilha
- Não usar bullet points no texto final (o sistema não formata bem)
- Não incluir dados pessoais do usuário no texto de Observações
- Manter o texto técnico e objetivo
- Máximo de 4 linhas por turno

SUCESSO
Recebo dois blocos de texto prontos para copiar e colar no sistema,
um para o turno da manhã e um para o turno da tarde,
sem precisar editar nada.

Antes de começar, confirme como vai estruturar os dois textos.
```

---

## ✅ Textos Prontos — Apontamento de 12/11/2026

> Copie e cole diretamente no campo **Observações** do Sistema.

---

### 🌅 APONTAMENTO MANHÃ — 08:00 às 12:00 (4h)

```
Atendimentos realizados no turno da manhã: impressora em rede offline na Contabilidade com fila de impressão liberada; configuração de rede corrigida no Financeiro após atualização do Windows; teclado substituído no setor de Compras por dano causado por líquido; instalação do Office 365 em notebook novo no Comercial; falha no sistema de ponto eletrônico do RH resolvida com reinstalação de driver biométrico; estação de trabalho do TI sem POST corrigida com troca de fonte; erro no TOTVS Protheus para emissão de nota fiscal na Contabilidade resolvido via atualização de DLL; lentidão de rede no Financeiro identificada como loop em switch corrigido; mouse com defeito substituído no Almoxarifado; leitor de código de barras do Comercial reconfigurado; Windows Update desbloqueado no Atendimento; certificado digital A3 do Jurídico revalidado; Power BI Desktop do Financeiro reconectado à fonte de dados; impressora jato de tinta do Compras com cabeça de impressão limpa e cartucho substituído; Wi-Fi do Atendimento corrigido de IP estático para DHCP.
```

---

### 🌆 APONTAMENTO TARDE — 14:00 às 18:00 (4h)

```
Atendimentos realizados no turno da tarde: Adobe Acrobat do Jurídico atualizado e cache limpo para resolver travamento em PDFs; VPN corporativa da Diretoria reconfigurada com renovação de certificado; CRM do Comercial com cache limpo e banco desfragmentado; notebook da Logística encaminhado para troca de bateria; usuário do Jurídico desbloqueado no Active Directory com nova senha temporária; Excel do Administrativo reparado com reativação de macros; monitor do Atendimento corrigido via atualização de driver de vídeo; antivírus do TI atualizado com whitelist aplicada; e-mail corporativo da Diretoria reconfigurado no celular com 2FA reativado; sistema de rastreamento da Logística restaurado via rollback; webcam do Administrativo com driver reinstalado e permissões ajustadas; impressora de rede do RH remapeada com IP fixo configurado; HD externo da Contabilidade recuperado via Testdisk; ramal VoIP do Compras reconfigurado no servidor Asterisk; Teams da Logística reinstalado após limpeza de cache; permissões NTFS da Diretoria reconfiguradas no novo servidor de arquivos.
```
