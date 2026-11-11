# Navegação Marítima com Algoritmo A*

Projeto prático da disciplina de **Inteligência Artificial I**  
FHO – Fundação Hermínio Ometto | Engenharia da Computação | 2026

**Autores:**
- Moisés Henrique Campanholo da Silva — RA 114518
- Felipe Apolinário de Souza — RA 114771
- Gabriel Vinícius Krebski — RA 115442

---

## Sobre o Projeto

Sistema de planejamento de rotas marítimas utilizando o algoritmo A*, considerando as correntes oceânicas reais baixadas do Copernicus Marine Service. O algoritmo calcula a rota de menor custo (tempo de travessia) entre dois pontos, levando em conta a velocidade efetiva do navio em relação à corrente local.

**Cenários implementados:**
- Rota de navegação otimizada vs. rota direta com cálculo de economia de combustível
- Interceptação de mancha de óleo em deriva

---

## Como Executar

1. Instale as dependências:
```
pip install xarray netCDF4 networkx matplotlib numpy pandas openpyxl
```

2. Coloque o arquivo `.nc` do Copernicus na mesma pasta do notebook

3. Abra e execute o `navegacao_maritima.ipynb` no VS Code ou Jupyter

---

## Arquivos

| Arquivo | Descrição |
|---|---|
| `navegacao_maritima.ipynb` | Notebook principal com o algoritmo e os cenários |
| `*.nc` | Dados de correntes oceânicas do Copernicus (baixar manualmente) |
| `dados_marinhos.xlsx` | Exportação tabular dos dados oceânicos |
| `grafico_rota_a_star.png` | Resultado da rota otimizada |
| `resultado_oleo_a_star.png` | Resultado da interceptação de óleo |

---

## Dados Oceânicos

Os dados de corrente são baixados do [Copernicus Marine Service](https://marine.copernicus.eu) no formato NetCDF (`.nc`). O notebook lê o arquivo e extrai as variáveis `uo` (corrente leste-oeste) e `vo` (corrente norte-sul).

Para atualizar os dados, baixe um novo `.nc` no site do Copernicus e substitua o arquivo na pasta do projeto.
