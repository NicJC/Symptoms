# Symptoms
Symptoms

[data](https://raw.githubusercontent.com/NicJC/Symptoms/main/Symptoms.csv)

Matrix plot in R:

---
              library(GGally)
                                ggpairs(data[,c(15:19)],
                     mapping = ggplot2::aes(color = Sex),
                      upper = list(continuous = wrap("density", alpha = 0.5), combo = "box_no_facet"))+ggplot2::labs(title = "Symptoms")  + 
                       theme(axis.text.x = element_text(color="steelblue", 
                                   size=12, angle=90),
                          axis.text.y = element_text( color="steelblue", 
                                    size=12))

                          ggsave("matrixPlot.png", width = 8, height = 8)

---


![](https://github.com/NicJC/Symptoms/blob/main/matrixPlot.png)
