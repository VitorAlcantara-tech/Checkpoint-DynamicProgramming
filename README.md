# Checkpoint 2 — Dynamic Programming

Projeto desenvolvido para o Checkpoint 2, com o objetivo de aplicar **programação dinâmica** em um problema de rotas de metrô.

O projeto simula redes de transporte de três cidades: **Beijing**, **San Francisco** e **São Paulo**. Cada cidade é representada como um grafo, onde as estações são os pontos do grafo e as conexões entre elas possuem um peso, que representa o custo ou tempo de deslocamento.


---

## Integrante

| Nome | RM |
|---|---|
| Vitor Alcantara | RM565885 |

---

## O que o projeto faz

O sistema calcula rotas entre uma estação de origem e uma estação de destino, considerando que o horário da viagem pode alterar o custo do trajeto.

Por exemplo, em horários de pico, o custo da rota aumenta, simulando maior movimento no metrô. Em horários de menor fluxo, o custo diminui.

Além disso, o projeto compara duas formas diferentes de encontrar o menor caminho:

- uma versão recursiva simples, sem otimização;
- uma versão com memoização, usando programação dinâmica.

A comparação mostra como a memoização melhora o desempenho ao evitar cálculos repetidos.

## Funcionalidades principais

- Representa rotas de metrô usando grafos.
- Calcula o menor caminho entre duas estações.
- Aplica um fator de custo de acordo com o horário da viagem.
- Compara o algoritmo sem memoização com o algoritmo usando memoização.
- Mede o tempo de execução de cada abordagem.
- Mede o uso de memória.
- Calcula também o maior caminho simples entre origem e destino.
- Gera gráficos comparativos de desempenho.
- Gera mapas interativos das rotas calculadas.

## Como funciona

Cada cidade possui uma rede de estações conectadas entre si. O algoritmo percorre essas conexões tentando encontrar o caminho com menor custo total.

O custo final da rota depende do peso das conexões e do horário escolhido para a viagem. No projeto, o horário utilizado é **18h**, considerado horário de pico, então o custo dos deslocamentos recebe um fator maior.

A versão sem memoização calcula os caminhos de forma recursiva tradicional, podendo repetir várias vezes os mesmos cálculos.

Já a versão com memoização armazena os resultados já calculados. Dessa forma, quando o mesmo trecho precisa ser analisado novamente, o programa reutiliza o resultado anterior, tornando a execução mais eficiente.

## Resultado esperado

Ao executar o projeto, é possível visualizar:

- o menor caminho encontrado para cada cidade;
- o custo total da rota;
- o tempo gasto por cada algoritmo;
- o consumo de memória;
- gráficos comparando os resultados;
- mapas interativos mostrando as rotas.

## Conceitos aplicados

O projeto demonstra, de forma prática, conceitos importantes como:

- grafos;
- recursão;
- programação dinâmica;
- memoização;
- backtracking;
- análise de desempenho.

## Conclusão

Este projeto mostra como a programação dinâmica pode tornar algoritmos recursivos mais eficientes. Ao comparar a solução comum com a solução usando memoização, fica claro que armazenar resultados intermediários evita cálculos repetidos e melhora o desempenho da busca por rotas.
