# Regras de Negócio — FINECORP (Kickoff)

## 1) Calendários/Datamentos
- **DRE**: apuração por **Data de Competência** (e visão alternativa por **Data de Caixa**).
- **DFC/Fluxo de Caixa**: apuração por **Data de Caixa/Pagamento**.
- **Aging (CR/CP)**: diferença **HOJE vs Data de Vencimento**.
- **RLS**: filtro por **Cliente_ID** (multiunidade).

## 2) Perguntas-chave que o dashboard deve responder
1. **Estamos batendo o plano? Onde estão os desvios?**  
   *KPIs*: Receita, CSP, Opex, EBITDA, Fluxo de Caixa — **mês/YTD vs Orçado** (R$ e %).  
   *Cortes*: Categoria e Centro de Custo/Projeto.

2. **Como está o caixa (real e futuro)? Folga ou aperto?**  
   *KPIs*: Entradas pagas, Saídas pagas, Fluxo Líquido do mês, **Burn** (média 3/6m), Saldo acumulado.  
   *Pipeline*: A receber/A pagar por **semana (13 semanas)** via `Data_Projecao_Pagto`.

3. **Estamos recebendo rápido e pagando no melhor prazo?**  
   *KPIs*: **DSO** (prazo médio de recebimento), **DPO** (prazo médio de pagamento), **Ciclo Financeiro = DSO − DPO** (⊕ DWIP se houver WIP).  
   *Ações*: acelerar cobrança / alongar pagamentos.

4. **Onde estão os riscos imediatos (atrasos e concentrações)?**  
   *KPIs*: AR vencido, AP vencido, **Aging** (A Vencer | 0–30 | 31–60 | 61–90 | 90+).  
   *Concentração*: % Top 10 clientes (AR) e Top 10 fornecedores (AP).

5. **Quais alavancas mais impactam o resultado?**  
   *KPIs*: Margem Bruta, Margem EBITDA, Opex/Receita (%), variações **MoM/YoY**.  
   *Drill*: Categoria/Subcategoria e Projeto/CC (preço, mix, volume, eficiência, CAPEX/dívida).

## 3) Buckets de Aging (padrão)
- **A Vencer**, **0–30**, **31–60**, **61–90**, **90+** (configurável).

## 4) Segurança (RLS)
- Papel **Cliente**: filtra por `Cliente_ID` (tabela de mapeamento Usuário↔Cliente).  
- Em ambientes multiunidade, publicar 1 workspace de homologação + 1 de produção.

