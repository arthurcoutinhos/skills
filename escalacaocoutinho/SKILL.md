---
name: "escalacaocoutinho"
description: "Use no início de pedidos médios ou pesados para avaliar se vale usar subagentes e, quando valer, sugerir quais, para quê e quanto vão gastar, antes de rodar."
---

# Escalação Coutinho

Antes de começar um pedido, avalie se subagentes melhoram o resultado. Se melhoram, sugira a escalação com o gasto estimado e pergunte antes de rodar. Se não melhoram, não mencione subagente nenhum: só responda.

Subagente é um assistente que recebe uma tarefa específica, começa sem saber nada além do que for passado a ele, trabalha sozinho e devolve só o resultado.

## Passo 1. Vale a pena?

Sugira subagentes só quando houver pelo menos um destes ganhos reais:

1. Olhar independente: o resultado melhora se alguém pensar sem conhecer a ideia do usuário ou o que já foi concluído. Ex.: gerar direções criativas distintas, criticar uma estratégia.
2. Trabalho em paralelo: existem frentes independentes que podem andar ao mesmo tempo. Ex.: analisar vários concorrentes, várias fontes, vários documentos.
3. Revisão de olho fresco: a entrega vai para alguém importante ou é cara de refazer, e vale uma revisão de quem não participou da produção. Ex.: relatório para a diretoria, proposta para cliente.
4. Volume: é preciso ler muito material para extrair só a conclusão.

Não sugira quando:

1. O pedido é simples ou curto.
2. As etapas dependem uma da outra em sequência, sem nada para rodar em paralelo.
3. O ganho seria pequeno perto do gasto.
4. O usuário já recusou subagentes nesta conversa para o mesmo tipo de tarefa.
5. Outra skill já usa subagentes no pedido (por exemplo, `ringuecoutinho`). Não duplique.

## Passo 2. Montar a escalação

Para cada subagente sugerido, defina:

1. Função: o que ele faz, em uma linha.
2. Tipo de ganho: independente, paralelo, revisão ou volume.
3. Quantidade.
4. Modelo: intermediário para pesquisa, geração de alternativas e leitura em volume; o mais forte só para revisão crítica de entrega importante.
5. O que ele recebe: só o necessário. Quem precisa de olhar independente não recebe a ideia do usuário.

Escale o mínimo que entrega o ganho. Mais subagentes não significa resultado melhor.

## Passo 3. Estimar o gasto

Sempre informe o gasto antes de rodar. Use estas referências por subagente, sempre marcadas como estimativa:

| Tipo de tarefa | Equivale a | Tokens aproximados |
|---|---|---|
| Leve, sem pesquisa (gerar alternativa, revisar texto) | 1 a 2 respostas normais | 20 a 40 mil |
| Com pesquisa na web ou leitura de arquivos | 3 a 5 respostas normais | 60 a 150 mil |
| Pesquisa extensa em muitas fontes | 5 a 10 respostas normais | 150 a 300 mil |

Some os subagentes e informe:

1. Total estimado em respostas normais e em tokens.
2. Como isso é cobrado: em planos do Claude (Pro, Max, Team, Enterprise) não existe cobrança extra por subagente; o gasto consome o limite de uso do plano mais rápido. Se o uso for pela API, o custo em dinheiro depende do preço atual do modelo por milhão de tokens; não invente valor em reais ou dólares sem consultar a tabela de preços vigente.
3. A alternativa mais barata, quando existir (por exemplo, menos subagentes ou modelo mais leve).

## Passo 4. Perguntar antes de rodar

Mostre a sugestão neste formato, curto:

> Dá para usar subagentes aqui:
> 1. [Função]: [quantidade] subagente(s), [modelo]. Ganho: [por que melhora].
> 2. ...
>
> Gasto estimado: cerca de [X] respostas normais (aproximadamente [Y] mil tokens), descontados do limite do seu plano.
> Uso todos, só parte, ou sigo sem?

Use a ferramenta de perguntas com opções quando disponível, com a recomendação como primeira opção. Nunca rode subagentes sem o ok do usuário. Se ele recusar, siga sozinho e não insista.

## Passo 5. Depois de rodar

1. Traga a conclusão de cada subagente integrada na resposta, sem colar o material bruto.
2. Diga quantos subagentes rodaram de fato.
3. Se a skill de explicar uso estiver disponível, ofereça em uma linha mostrar o gasto real da sessão.
4. Se o resultado for importante para depois, ofereça salvar o essencial na memória ou num documento.

## Regras

1. No máximo uma sugestão de escalação por pedido.
2. Nunca esconder ou arredondar para baixo o gasto estimado.
3. Nunca usar travessões nem traços como pontuação.

## Integração

1. `marchacoutinho`: pedido de nível 1 nunca recebe sugestão de subagente.
2. `ringuecoutinho`: já tem os próprios subagentes; não sugira outros por cima.
