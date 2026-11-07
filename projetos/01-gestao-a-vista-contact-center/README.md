<p align="center"><img src="../../assets/capa-gestao-a-vista.png" alt="Gestão à Vista · Contact Center" width="100%"></p>

# Gestão à Vista · Contact Center

**Marca fictícia:** Aurora Educação · **Parceiras de atendimento (EPS):** VOXPRIME e CONECTA+ · **Ciclo:** 27.1 (out/2026)

## Contexto

Uma instituição de ensino terceiriza para duas empresas de contact center o contato com os candidatos
inscritos. O painel responde a três perguntas da gestão comercial:

1. **Quanto do mailing vira matrícula, e em qual etapa do funil a conversão se perde?**
2. **Qual parceira entrega mais resultado por posição de atendimento e por real investido?**
3. **No ritmo atual, a meta do mês fecha? Quanto falta por dia útil?**

## Páginas e análises

| Página | O que mostra | Para que serve |
|---|---|---|
| **Funil CC** | Funil por parceira (mailing → trabalhados → tentativas → atendidos → efetivos → vendas → matrículas) com spin, hitrate, % atendido/base, conversão de venda e de matrícula; funil de mídia; contatos por dia da semana; produtividade por parceira com ícones de comparação; cohort de alô; planejado × realizado de inscritos | Encontrar o gargalo do funil e comparar as parceiras |
| **Acumulado ciclo** | Vendas e matrículas acumuladas; planejado × realizado; pace real × pace ideal; gap de matrículas e % de atingimento da meta | Saber se a meta do mês fecha no ritmo atual |
| **Gerencial** | CPMAT (custo por matrícula) por mês e por dia, posições de atendimento, produtividade por dia útil, matrículas por semana do mês e do ciclo | Gestão de contrato: produtividade e custo de cada parceira |
| **Cohort** | Safras de inscrição × dias até o contato (D0 a D15+): conversão e alô por safra | Medir o efeito da velocidade do primeiro contato na conversão |
| **Vendas e tabulações** | Vendas × planejado, conversão de venda por contato efetivo, motivos de tabulação (recusa, financeiro, quebra de interação…), produtividade de vendas | Entender por que o candidato não fecha e calibrar o roteiro |
| **Glossário** | Definição, fórmula e regra de negócio de cada indicador | Padronizar a leitura entre as áreas |

## Destaques técnicos

- **129 medidas DAX**, com regras de efetividade e de trabalho **diferentes por parceira**, como na operação real.
- **Cohort por safra** (D0 a D15+) com `SUMX` sobre o calendário e filtros de *aging*.
- **Calculation group** (*Visão Data*) que troca a leitura entre **data de inscrição** e **data de matrícula** com `USERELATIONSHIP`.
- **Parâmetros de campo** para abrir as análises por supercanal, modalidade, curso, unidade, regional, gerente etc.
- **Posições de atendimento × dias úteis** por mês e parceira para a produtividade; **custo mensal rateado** pelos dias do período para o CPMAT.
- **Pace**: ritmo realizado × ritmo necessário até o fim do mês, considerando feriados.
- Base fictícia de **37 mil interações** e **13,8 mil inscrições**, gerada respeitando as regras das medidas.

## Como abrir

Abra o arquivo **`.pbip`** no Power BI Desktop e clique em **Atualizar**. Os dados estão embutidos no modelo.
