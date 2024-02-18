## DataScience - Formação Cientista de Dados com R e Python

### Ferramentas Utilizadas:

- R com RStudio (Notebooks)
- Python com Juptyper Labs (Anaconda)
- Outras ferramentas:
  - PostgreSQL
  - MongoDB
  - Power BI
  - Tableau

### Orientações para instalar o iGraph

1) Desinstalar o iGraph/pyCairo via Anaconda Prompt:
```
pip uninstall python-igraph
pip uninstall pycairo
```

2) Baixar o .whl do pycairo que corresponde a sua versão:
https://www.lfd.uci.edu/~gohlke/pythonlibs/#pycairo
Localize Pycairo
Por exemplo: meu Python é 3.7 - 64bits, então baixei o arquivo: pycairo-1.19.1‑cp37‑cp37m‑win_amd64.whl
Retorne para o Anaconda Prompt e instale o .whl do local que foi baixado:
```
pip install C:/local para onde o arquivo foi baixado/nome do arquivo.whl
```

3) Baixar o .whl do igraph que corresponde a sua versão:
Acesse o site: https://www.lfd.uci.edu/~gohlke/pythonlibs/ 
Localize python-igraph
Por exemplo: meu Python é 3.7 - 64bits, então baixei o arquivo: python_igraph‑0.7.1.post6‑cp37‑cp37m‑win_amd64.whl
Retorne para o Anaconda Prompt e instale o .whl do local que foi baixado:
```
pip install C:/local para onde o arquivo foi baixado/nome do arquivo.whl
```

OBS: Após isso é só reiniciar o kernel do python e seguir o script da aula normalmente.

### Instalação de Pacotes

```{r}
install.packages("cluster")
install.packages("factoextra")
library(cluster)
library(factoextra)
```
### Gera o cluster

```{r}
cluster = pam(iris[,1:4],k=3)
```
### Visualiza

```{r}
cluster
plot(cluster)
table(iris$Species,cluster$clustering)
```

### Vizualização com factoextra

```{r}
g = fviz_cluster(list(data = iris[,1:4], cluster=cluster$cluster), ellipse.type = "norm", ggtheme = theme_bw(), main="Cluster")
plot(g)
```

### Anaconda (JuptyperLab)

```
pip install yellowbrick
pip install apyori
```