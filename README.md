# Blog Individual — Sistemas de Informacao

Este repositorio hospeda a versao estatica do blog individual desenvolvido para a disciplina de Sistemas de Informacao.  
Os arquivos HTML foram gerados com [Quarto](https://quarto.org/) a partir do projeto principal (`index.qmd`, `about.qmd`, etc.) e publicados aqui para hospedagem (ex.: GitHub Pages).

## Atividades apresentadas

1. **Cotacao do dolar (PTAX/BCB)**  
   Transforma um parametro `MMYYYY`, consulta a API PTAX e monta uma serie interativa com Plotly exibindo estatisticas do mes.

2. **Monitoramento de frota (SPTrans/Olho Vivo)**  
   Usa a API Olho Vivo para listar paradas e rastrear posicoes em tempo real da linha `NUMERO_LINHA` (padrao `8300-10`).  
   O mapa Folium possui camadas separadas para paradas (azul) e veiculos operando (vermelho).  
   Se a API nao enviar dados de veiculos em determinado momento, a camada correspondente permanece vazia ate a proxima renderizacao.

3. **Regressao linear por matriz**  
   Carrega `dados_x.txt` e `dados_y.txt`, calcula os parametros `a` e `b` via `(X?X)?¹X?y` e apresenta tabela comparativa e grafico com a reta ajustada.

## Estrutura do repositorio

```
.
+- index.html       # Pagina principal do blog já renderizada
+- about.html       # Pagina "Sobre"
+- styles.css       # Ajustes visuais customizados
+- search.json      # Indice de busca do Quarto
+- site_libs/       # Dependencias estaticas (JS/CSS) usadas pelas paginas
```

## Atualizando o site

1. No projeto Quarto (`blog-individual`), execute `quarto render index.qmd` para gerar a pasta `_site/`.
2. Copie o conteudo de `_site/` para este repositorio (sobrescrevendo os arquivos atuais).
3. Confirme as mudancas, commite e envie para o GitHub:

```bash
git add .
git commit -m "Atualiza build estatico do blog"
git push origin main
```

Se utilizar GitHub Pages, a publicacao sera atualizada automaticamente assim que o push for concluido.
