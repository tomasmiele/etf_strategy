# Estratégia de ETF

Este projeto implementa e compara duas versões de uma estratégia de momentum cross-sectional para ETFs de países.

## Estratégias Implementadas

### Estratégia 1: Momentum Simples
- **Sinal**: Retorno acumulado bruto (soma dos log-retornos)
- **Complexidade**: Simples
- **Lógica**: ETFs com maior retorno recente são comprados (long), menores são vendidos (short)

### Estratégia 2: Sharpe Momentum (Complexa)
- **Sinal**: Retorno acumulado normalizado pela volatilidade (índice de Sharpe histórico)
- **Complexidade**: Ajustada ao risco
- **Lógica**: Penaliza ativos voláteis, priorizando tendências fortes e estáveis

## Parâmetros Principais
- **Lookback**: 63 dias úteis (~3 meses)
- **Rebalanceamento**: 21 dias úteis (~1 mês)
- **Quantil**: 20% (top/bottom para long/short)

## Estrutura do Projeto
- `strategy.ipynb`: Notebook principal com implementação, análise e visualizações
- `libs.txt`: Lista de dependências Python
- `README.md`: Este arquivo

## Requisitos
Instale as dependências listadas em `libs.txt`:

```
pip install -r libs.txt
```

## Como Usar
1. Abra o notebook `strategy.ipynb` no Jupyter.
2. Execute as células sequencialmente para reproduzir a análise.
3. As visualizações incluem gráficos de performance, drawdowns e comparações entre estratégias.

## Dependências Principais
- pandas, numpy: Manipulação de dados
- matplotlib: Visualizações
- requests, beautifulsoup4: Coleta de dados
- yfinance (implicado): Dados financeiros

O notebook inclui coleta de dados, processamento, backtesting e análise de risco.