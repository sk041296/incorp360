# INCORP 360 — Site Standalone

Página única (standalone) do INCORP 360: portfólio de projetos, dashboard de obra
"ao vivo" e simulador de investimento em incorporação. Todo o conteúdo (HTML, CSS,
JavaScript, fontes e imagens) está embutido em um único arquivo `index.html` — não há
dependências externas nem necessidade de build.

## Estrutura

```
.
├── index.html      # site completo (tudo embutido)
├── .nojekyll       # desativa o Jekyll no GitHub Pages (serve os arquivos como estão)
└── README.md
```

## Publicar no GitHub Pages

1. Crie um repositório novo e envie estes arquivos para a branch `main`.
2. Em **Settings → Pages**, selecione **Branch: main / (root)** e salve.
3. Em ~1 min o site fica disponível em `https://<usuario>.github.io/<repositorio>/`.

### Via linha de comando

```bash
git init
git add .
git commit -m "INCORP 360 — site standalone"
git branch -M main
git remote add origin https://github.com/<usuario>/<repositorio>.git
git push -u origin main
```

## Conteúdo

- **Portfólio** — 11 projetos com dados reais (área, lote mínimo, quartos, suítes,
  banheiros, vagas, churrasqueira, piscina e investimento). Cada card abre uma
  página de detalhe com galeria, planta(s) ampliada(s) e especificações completas.
- **Dashboard de obra** — KPIs, curva físico-financeira, indicadores EVM, custo por
  categoria e situação do canteiro, com atualização animada.
- **Simulador de incorporação** — construção a R$ 4.100/m², juros de 11% a.a. por
  prazo de venda (12/24/36 meses), regimes SPE (Lucro Presumido ~6,73%) e Pessoa
  Física (15% sobre o ganho). Permite carregar um projeto do portfólio com a
  metragem e a restrição de lote mínimo de cada casa.

## Observações

- Premissas financeiras (custo/m², taxa de juros, alíquotas, preço do terreno por m²)
  são ilustrativas e estão definidas como constantes no início dos blocos de script.
- O projeto **Mid-Century** ainda não foi incluído por falta de imagens/planta.
