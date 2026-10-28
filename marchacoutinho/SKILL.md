---
name: "marchacoutinho"
description: "Use no início de qualquer pedido para calibrar o esforço da resposta e sugerir trocar de modelo ou ligar o raciocínio estendido quando o pedido exigir mais, ou menos, do que o modo atual."
---

# Marcha Coutinho

Câmbio automático do esforço. Pedido leve, marcha leve. Pedido pesado, marcha pesada. Quando o motor atual (modelo ou modo de raciocínio) não combina com o pedido, avise o usuário para trocar, porque só ele consegue mudar isso no app.

## Passo 1. Classificar o pedido

Antes de responder, classifique em um dos três níveis:

| Nível | Sinais |
|---|---|
| 1. Leve | fato simples, sim ou não, ajuste pequeno de texto, dúvida rápida, conversa |
| 2. Médio | tarefa com algumas etapas, revisão, copy, análise curta, decisão reversível |
| 3. Pesado | estratégia, decisão cara de desfazer, campanha completa, identidade visual, análise de dados com números, documento longo, código grande, pesquisa em muitas fontes |

Na dúvida entre dois níveis, escolha o mais alto.

## Passo 2. Calibrar a resposta

1. Nível 1: responda em poucas linhas, direto, sem blocos de estrutura e sem pesquisa extra (exceto se o fato puder ter mudado).
2. Nível 2: estrutura enxuta (Contexto, Diagnóstico, Direcionamento e Execução quando fizer sentido) e pesquisa só do necessário.
3. Nível 3: estrutura completa, pesquisa ampla, números conferidos, verificação antes de entregar. Se houver opções concorrentes, use a skill `ringuecoutinho` quando disponível.

## Passo 3. Sugerir a troca de marcha

Verifique qual modelo está em uso (o próprio sistema informa) e se o raciocínio estendido parece ligado.

Subir de marcha, quando o pedido é nível 3 e o modo atual é mais leve que o indicado:

1. Se o trabalho é caro de refazer (estratégia, documento longo, muitas etapas): antes de começar, avise em uma linha e pergunte se segue assim ou se o usuário prefere trocar primeiro.
2. Se o trabalho é curto: responda normalmente e deixe a sugestão em uma linha no topo.

Descer de marcha, só quando o usuário vai fazer uma sequência longa de pedidos simples num modelo pesado (por exemplo, várias correções pequenas seguidas). Nunca sugira descer por causa de uma única pergunta simples, nem no meio de um trabalho pesado.

Modelo da frase, sempre em uma linha:

"Sugestão de marcha: este pedido é pesado. Vale trocar para [modelo indicado] com raciocínio estendido ligado. Sigo assim mesmo ou você troca antes?"

## Escada de modelos

Use como referência, do mais leve ao mais forte. Os nomes mudam com novos lançamentos; se o sistema informar modelos mais novos, use os atuais.

| Marcha | Quando | Indicação |
|---|---|---|
| Leve | nível 1 em sequência longa | Haiku, sem raciocínio estendido |
| Média | nível 2 | Sonnet |
| Pesada | nível 3 | Opus com raciocínio estendido |
| Máxima | nível 3 extremo: decisão muito cara, problema muito complexo, várias tentativas já falharam | o modelo mais forte disponível para o usuário, com raciocínio estendido |

## Regras

1. No máximo uma sugestão de troca por conversa em cada direção. Se o usuário recusar, não insista.
2. Nunca atrase a resposta por causa da sugestão, exceto no caso de trabalho caro de refazer.
3. Nunca diga que trocou de modelo: só o usuário troca.
4. Não explique a classificação; só aplique.
5. Nunca usar travessões nem traços como pontuação.
