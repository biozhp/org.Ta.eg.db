# org.Ta.eg.db
This is an R package that contains genome wide annotation for *Triticum aestivum* L.
## Getting Started
### Installing
    install.packages("https://media.githubusercontent.com/media/biozhp/org.Ta.eg.db/master/org.Ta.eg.db.tar.gz", repos=NULL, type="source")
### Usages
    library("clusterProfiler")
    library("org.Ta.eg.db")
    gene <- read.table("gene.txt",header=F,sep="\t")
    gene <- as.factor(gene$V1)
    org <- org.Ta.eg.db
    enrich.go.BP <- enrichGO(gene=gene, OrgDb=org, keyType="GID",ont="BP", pvalueCutoff = 0.01, qvalueCutoff = 0.05)
    simply <- simplify(enrich.go.BP)
    ouf <- paste("output.txt",sep ="\t")
    write.table(simply,ouf)
## Contact
For any bugs/issues/suggestions, please send emails to: Peng Zhao pengzhao@nwafu.edu.cn.
