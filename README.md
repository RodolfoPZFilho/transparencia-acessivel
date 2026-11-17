# Transparência Acessível

**Verificação automatizada de acessibilidade, integrada ao CI/CD, em portais de serviços públicos brasileiros**

Projeto de Trabalho de Conclusão de Curso (TCC) em Engenharia de Software, desenvolvido ao longo do 4º ano.

## Integrantes

- Rodolfo Paturalski Zuculo Filho ([@RodolfoPZFilho](https://github.com/RodolfoPZFilho))
- João Vitor Dias Oliveira ([@JoaooOliveiraa](https://github.com/JoaooOliveiraa))

## Motivação

Serviços públicos estão migrando para o meio digital, e a Lei Brasileira de Inclusão (Lei 13.146/2015, art. 63) exige que os portais de órgãos públicos sejam acessíveis. Na prática, a acessibilidade raramente é verificada a cada nova versão publicada. Quando um portal não funciona com leitor de tela, teclado ou ampliação, a informação pública deixa de chegar a quem mais depende dela.

## Questão de pesquisa

> Em que medida uma ferramenta automatizada de verificação de acessibilidade, integrada ao pipeline de CI/CD e mapeada ao eMAG, detecta as barreiras identificadas por auditoria manual em portais de serviços públicos brasileiros?

## Abordagem

Design Science Research:

1. Desenvolver uma ferramenta (CLI + GitHub Action) que inspeciona páginas de serviços públicos com axe-core/Playwright e mapeia as violações às recomendações do eMAG e aos critérios da WCAG 2.2.
2. Realizar auditoria manual padronizada (checklist eMAG + navegação com leitor de tela NVDA e teclado) em uma amostra de portais públicos, que serve de referência.
3. Comparar ferramenta e auditoria manual (precisão, recall, tempo de execução e tipos de barreira não detectados).

## Estrutura do repositório

| Pasta | Conteúdo |
|---|---|
| `ferramenta/` | Código-fonte da ferramenta e da GitHub Action, com testes |
| `auditoria/` | Checklist da auditoria manual e planilhas preenchidas por portal |
| `dados/` | Lista de URLs avaliadas, páginas arquivadas, relatórios brutos (JSON) e dataset consolidado (CSV) |
| `analise/` | Scripts de cálculo das métricas (precisão, recall, F1, kappa, tempos) e geração de gráficos |
| `instrumentos/` | Protocolo de auditoria e critérios de seleção da amostra |
| `docs/artigo/` | Versões do projeto e do artigo (pré-projeto: `pre-projeto-tcc.docx`) |
| `docs/diagramas/` | Diagramas UML, de arquitetura e tabela de mapeamento eMAG–WCAG–axe-core |

## Status

🟡 Fase de projeto (pré-TCC). O desenvolvimento começa em fevereiro do 4º ano.

## Licença

Código sob licença MIT. Dados de auditoria disponibilizados para fins de reprodutibilidade.
