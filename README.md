# DataScience

##### Formação Cientista de Dados com R e Python #####


## Ferramentas Utilizadas:

- R com RStudio (Notebooks)
- Python com Juptyper Labs (Anaconda)
- Outras ferramentas:
  - PostgreSQL
  - MongoDB
  - Power BI
  - Tableau


## Instalação de Pacotes

```{r}
#install.packages("cluster")
#install.packages("factoextra")
library(cluster)
library(factoextra)
```
# Gera o cluster

```{r}
cluster = pam(iris[,1:4],k=3)
```
# Visualiza

```{r}
cluster
plot(cluster)
table(iris$Species,cluster$clustering)
```
# Vizualização com factoextra

```{r}
g = fviz_cluster(list(data = iris[,1:4], cluster=cluster$cluster), ellipse.type = "norm", ggtheme = theme_bw(),
                main="Cluster")
plot(g)
```

# Anaconda (JuptyperLab)

```
- pip install yellowbrick
- pip install apyori
```
