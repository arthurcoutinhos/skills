---
name: "ringuecoutinho"
description: "Use para escolher entre ideias ou opções de qualquer tipo (conceito, nome, campanha, estratégia, decisão de negócio ou pessoal): as ideias se atacam, evoluem e um juiz decide por critérios."
---

# Ringue Coutinho

O Ringue coloca ideias para brigar. Cada ideia é atacada pela concorrente mais forte, se defende, evolui, e só a melhor sai viva. Serve para qualquer assunto: marca, campanha, nome, roteiro, estratégia, preço, contratação, projeto pessoal, decisão de vida. Nada aqui é preso a um negócio específico; o contexto vem do caso.

Tudo acontece numa resposta só, sem criar agentes extras. O custo é o de uma conversa normal.

## Modos

1. Rápido (padrão): 3 ideias, 1 rodada de ataque, final direta.
2. Completo: 4 ideias, 2 rodadas de ataque, final com reescrita. Use quando o usuário pedir ou quando a decisão for cara de desfazer.

## Etapa 1. Montar o ringue

Antes de olhar qualquer ideia, defina em poucas linhas:

1. Objetivo: o que a decisão precisa conseguir.
2. Contexto: quem é afetado, onde vai rodar, que recursos existem.
3. Restrições: prazo, verba, regras, o que não pode acontecer.
4. Critérios de julgamento: de 3 a 5, com peso, derivados do objetivo deste caso. Nunca use uma lista fixa. Exemplos de onde tirar critérios, só como inspiração:
   1. Marca e criativo: diferenciação, verdade com a marca, memória, percepção de valor.
   2. Negócio: retorno, custo, risco, velocidade, escala.
   3. Execução: viabilidade com o time e os recursos reais, dependências.
   4. Pessoal: alinhamento com valores, reversível ou não, impacto em quem importa.

Se o contexto não estiver claro, faça uma pergunta só, com a sua recomendação como primeira opção. Se estiver claro, mostre o ringue montado e siga.

Os critérios são definidos antes de ver as ideias para que o juiz não ajuste a régua ao favorito.

## Etapa 2. Escalar os lutadores

1. Se o usuário trouxe ideias, elas entram. Complete até o número do modo com ideias novas.
2. As ideias precisam ser estratégias diferentes, não variações da mesma. Se duas forem parecidas, troque uma.
3. Pelo menos uma ideia deve ser a opção ousada e uma deve ser a opção segura.
4. Se a skill `fora-do-obvio` estiver disponível e o assunto for criativo, use para gerar ao menos uma ideia fora do clichê.
5. Dê a cada ideia um nome curto e descreva em até 3 linhas.

## Etapa 3. Ataque cruzado

Para cada ideia:

1. Ataque: a concorrente mais forte aponta a falha mais grave dela, com argumento concreto (onde quebra, quanto custa, quem rejeita, o que dá errado na prática). Ataque raso não vale.
2. Defesa: a ideia admite o que procede, rebate o que não procede e evolui, absorvendo a correção.

No modo completo, faça uma segunda rodada com as ideias já evoluídas.

## Etapa 4. Corte

1. Dê nota de 1 a 5 em cada critério, aplique os pesos e mostre numa tabela.
2. Sobrevivem as 2 melhores.
3. Pilhagem: cada eliminada entrega a sua melhor parte para a sobrevivente que melhor a aproveita. Diga o que foi pilhado.

## Etapa 5. Final

1. Reescreva as 2 finalistas na versão mais forte possível, já com a pilhagem.
2. Cada uma faz seu melhor argumento contra a outra.
3. O juiz decide pelos critérios, não pela eloquência. Em empate técnico, vence a que é mais barata de testar ou mais fácil de desfazer.

## Etapa 6. Veredito

Entregue, nesta ordem:

1. Vencedora, em uma frase.
2. Por que venceu, ligado aos critérios.
3. O que ela absorveu das outras.
4. Risco que continua existindo e como reduzir.
5. Teste barato para validar antes de investir pesado (o que fazer, quem faz, prazo, métrica).
6. Condição de virada: o que precisaria acontecer para a segunda colocada passar a ser a melhor.

## Regras do juiz

1. Não favorecer a ideia do usuário, a primeira da lista nem a mais bonita de ler.
2. Não inventar empate para agradar.
3. Se nenhuma ideia passar num critério eliminatório, diga isso e proponha nova rodada com ideias diferentes, em vez de coroar a menos pior.
4. Separar fato de suposição. Quando a decisão depender de um dado que não existe, diga qual dado falta e como conseguir.

## Formato

Direto e enxuto. Tabela para as notas, listas numeradas para o resto. Nunca usar travessões nem traços como pontuação. Seguir as preferências de escrita já registradas para o usuário.

## Integração

1. `fora-do-obvio`: gera lutadores fora do clichê na Etapa 2.
2. `crivocoutinho`: quando a vencedora for uma peça visual, entregue o veredito como ponto de partida do Crivo.
