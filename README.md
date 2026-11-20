# APS 2 — Otimização e Inteligência Artificial no Canteiro "Torre Europarque"

Repositório oficial da APS 2 da disciplina de Inteligência Artificial Aplicada — Engenharia de Software, 6º Período (2026/2), UniSENAI PR — Campus Londrina.

**Docente:** Prof. Paulo Cesar Dias Lima

## Integrantes
- Felipy Yuske Ogido
- Fernando Junior Vaciski de Camargo
- Giovana Nunes Constancio Donato
- Graciele Miki Sazaka
- João Paulo Simplicio

## Estrutura do Projeto
```
├── notebooks/
│   └── APS2_Torre_Europarque.ipynb   # Notebook unificado com as 5 etapas (Google Colab)
├── outputs/
│   ├── graficos/                     # Gráficos gerados pelo notebook (usados no relatório)
│   └── tabelas/                      # Tabelas de resultados exportadas pelo notebook
├── docs/                             # Relatório técnico (.docx/.pdf) e enunciado da APS
├── requirements.txt
└── README.md
```

## Divisão das Etapas
| Etapa | Conteúdo | Responsável |
|---|---|---|
| 1 | Busca Heurística A* (NetworkX) e Programação Linear (PuLP) | Giovana |
| 2a | Roteirização VRP com Algoritmo Genético (DEAP) | Felipy |
| 2b | Simulação a Eventos Discretos da concretagem (SimPy) | Giovana |
| 3 | Ontologia RDF/OWL e Consultas SPARQL (rdflib) | João |
| 4 | Rede Neural MLP do Zero (NumPy) | Fernando |
| 5 | Lógica Fuzzy Mamdani e Sugeno (scikit-fuzzy) | Miki |

## Execução

### Google Colab (recomendado)
Abra o notebook [APS2_Torre_Europarque no Colab](https://colab.research.google.com/drive/1o0CY9PVHLO2j6wh5hGiMmTSulFDrvvcN) e execute as células em ordem. A primeira célula instala as dependências com `pip install`.

### Localmente
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate | Linux/macOS: source .venv/bin/activate
pip install -r requirements.txt jupyter
jupyter notebook notebooks/APS2_Torre_Europarque.ipynb
```

> Ao rodar localmente, remova ou comente a linha `!pip install ...` da primeira célula.

## Reprodutibilidade
O notebook define uma semente global (`SEED = 42`) na célula de configuração, garantindo que o GA, as réplicas do SimPy e os pesos da MLP produzam os mesmos resultados a cada execução.
