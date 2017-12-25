```
# open data 
data <- read.csv("data_pang.csv")

# load packages
install.packages("dplyr")
library(dplyr)
install.packages("ggpubr")
if(!require(devtools)) install.packages("devtools")
devtools::install_github("kassambara/ggpubr")
library(ggpubr)
install.packages("corrplot")
library(corrplot)

# Descriptive stats
group_by(data, Lith) %>% 
  summarise(
    count = n(), 
    mean = mean(Elevasi_mdpl, na.rm = TRUE),
    sd = sd(Elevasi_mdpl, na.rm = TRUE)
  )

# Correl matrix

res <- cor(data)
round(res, 2)
corrplot(res, type = "upper", order = "hclust", 
         tl.col = "black", tl.srt = 45)


# Strip-chart

ggboxplot(data, x = "Lith", 
          y = "Elevasi_mdpl",
          color = "Lith",
          palette = c("#00AFBB", "#E7B800",
                      "#FC4E07"),
          add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "Kekeruhan_NTU",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "DHL_mikroS_cm",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "TDS_ppm",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "pH.lab",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "Kesadahan_ppm",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "Ca_ppm",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "Mg_ppm",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "Fe3_ppm",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "Mn_ppm",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "K_ppm",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "Na_ppm",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "NH4_ppm",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "CO3_ppm",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "HCO3_ppm",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "Cl_ppm",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "SO4_ppm",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "NO2_ppm",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")

ggstripchart(data, x = "Lith", 
             y = "NO3_ppm",
             color = "Lith",
             palette = c("#00AFBB", "#E7B800",
                         "#FC4E07"),
             add = "mean_sd")
```