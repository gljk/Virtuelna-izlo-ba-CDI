require(openxlsx)
imdata<- read.xlsx("IM-TFR-HDI.xlsx")
require(plotly)

fig <- imdata %>%
  plot_ly(
    y = ~HDI,
     x= ~SUF,
    frame = ~Godina,
    type = 'scatter',
    mode = 'markers',
    color = ~Region,
    text = ~Zemlja,
    hovertemplate = paste(
      "<b>%{text}</b><br><br>",
      "HDI: %{y:1}<br>",
      "SUF: %{x:1}<br>",
      "<extra></extra>"
    ),
    showlegend = T
  )

fig %>% animation_opts(frame = 1000) %>% animation_button(label = "Pokreni")
