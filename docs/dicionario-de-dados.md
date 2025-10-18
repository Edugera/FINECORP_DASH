# Dicionário — campos mínimos

## FatoMovimento (transacional real)

- IDs: `Movto_ID` (opcional), `Cliente_ID`, `Fornecedor_ID` (se aplicável)
- Datas: `Data_Competencia`, `Data_Caixa`, `Data_Vencimento`, `Data_Projecao_Pagto` (pipeline)
- Chaves/cortes: `Conta` (plano), `Categoria`, `Subcategoria`, `CentroCusto`, `Projeto`
- Natureza: `Tipo` (Receita|Custo|Despesa), `CR_AP` (A Receber|A Pagar), `Status` (Pago|Aberto|Vencido)
- Valores: `Valor`, `Valor_Desconto` (opcional), `Moeda` (se multi-moeda)

## FatoOrcado (plano/orçamento)

- Chaves de alinhamento: `AnoMes` (YYYYMM) ou `Data_Competencia` (1º dia do mês)
- Eixos: `Categoria`, `Subcategoria`, `CentroCusto`, `Projeto`
- Valores: `Valor_Orcado`

## Dimensões

- `Dim_Calendario`: Data, Ano, Mês, NomeMês, Trimestre, Semana, `AnoMes`, flags **IsYTD/IsMTD/IsQTD**
- `Dim_Conta`, `Dim_CentroCusto`, `Dim_Projeto`
- `Dim_Cliente`, `Dim_Fornecedor`

## Tabela de Segurança (RLS)

- `UsuarioEmail`, `Cliente_ID`
