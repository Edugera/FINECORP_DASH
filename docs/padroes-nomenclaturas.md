
### `docs/padroes-nomenclaturas.md`
```md
# Padrões & Nomenclaturas

## Tabelas
- Fatos: `FatoMovimento`, `FatoOrcado`.
- Dimensões: `Dim_Calendario`, `Dim_Conta`, `Dim_CentroCusto`, `Dim_Cliente`, `Dim_Fornecedor`.

## Colunas (exemplos)
- Datas: `Data`, `DataVencimento`, `DataPrevista`.
- Valores: `Valor`, `Entradas`, `Saidas`, `ValorAberto`.
- Dimensões: `Conta`, `CentroCusto`, `ClienteNome`, `FornecedorNome`, `Status`.

## Medidas (pastas)
- **Base**: Receita, Custo, Despesa, Lucro, Margem %.
- **Tempo**: YTD, MTD, QTD, YoY, MoM.
- **DRE**, **Fluxo**, **Aging**.

## Branches e commits
- Branches: `main`, `dev`, `feature/<area-assunto>` ex.: `feature/etl-param-pasta`.
- Commits: `feat:`, `fix:`, `docs:`, `refactor:`, `chore:`.

## Versões
- Tags SemVer: `v0.1.0`, `v0.2.0`…
