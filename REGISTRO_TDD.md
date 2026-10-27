# Registro do ciclo de TDD

## Comportamento escolhido

Cobrar taxa de entrega de R$ 5 para pedidos de R$ 50 a 2 km, aumentar R$ 2 por quilometro excedente e oferecer frete gratuito a partir de R$ 100.

## Red

1. `test_taxa_entrega_ate_tres_km`: falhou porque a funcao ainda nao estava implementada (`NotImplementedError`).
2. `test_taxa_entrega_acima_de_tres_km`: falhou porque a implementacao retornava taxa fixa de R$ 5, em vez de R$ 7.
3. `test_entrega_gratis_para_pedido_a_partir_de_cem_reais`: falhou porque a implementacao cobrava R$ 9, em vez de R$ 0.

## Green

1. Retorno inicial de R$ 5. Testes acumulados: 5 aprovados.
2. Adicionado calculo de R$ 2 por quilometro acima de 3 km. Testes acumulados: 6 aprovados.
3. Adicionada a verificacao de pedido a partir de R$ 100. Testes acumulados: 7 aprovados.

## Refactor

Simplificada a expressao do calculo de distancia usando `max(0, distancia_km - 3)` e mantida a prioridade da entrega gratuita.

**Resultado final:** 7 testes aprovados (4 originais e 3 novos).
