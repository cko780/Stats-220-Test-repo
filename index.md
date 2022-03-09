# Hello world!
```R
library(magick)

img_panel1 <- image_read("https://media.discordapp.net/attachments/686807262773510168/907591046609928212/IMG_5815.png")
img_panel2 <- image_read("https://media.discordapp.net/attachments/686807262773510168/907591046609928212/IMG_5815.png")
img_panel3 <- image_read("https://media.discordapp.net/attachments/686807262773510168/907591046609928212/IMG_5815.png")

blank_Panel <- image_blank(width = 250, height = 300, color = "#FFFFFF")

text_panel1 <- image_annotate(blank_Panel, color = "#000000", text = "James", size = 50, gravity = "center")
text_panel2 <- image_annotate(blank_Panel, color = "#000000", text = "James", size = 50, gravity = "center")
text_panel3 <- image_annotate(blank_Panel, color = "#000000", text = "James", size = 50, gravity = "center")

combine_panel1 <-  c(image_resize(img_panel1, "250x300!"), text_panel1) %>%
                                image_append() 
combine_panel2 <- c(image_resize(img_panel2, "250x300!"), text_panel2) %>%
                              image_append() 
combine_panel3 <- c(image_resize(img_panel3, "250x300!"), text_panel3) %>%
                                image_append() 

final <- c(combine_panel1, combine_panel2, combine_panel3) %>%
                                image_append(stack = TRUE) 
final

image_write(final, "saves/my_meme.png")

```
