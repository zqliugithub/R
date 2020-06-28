# R
learning R Language

```R
library(pheatmap)
data<-read.table("heatmap.txt",header=TRUE)
row.names(data)<-data$Geneid
data2<-data[,2:5]
data_m<-data.matrix(data2)

pdf("heatmap.pdf")
pheatmap(data_m,cluster_cols=FALSE,cluster_rows=FALSE,border_color=NA,cellwidth=30,cellheight=10)
dev.off()
```
