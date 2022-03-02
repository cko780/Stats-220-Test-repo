# Hello world!
```R
# square one
confused_cat <- image_read("https://media.discordapp.net/attachments/686807262773510168/907591046609928212/IMG_5815.png") %>%
  image_scale(0)

#square two
stats_text <- image_blank(width = 500, 
                          height = 500, 
                          color = "#000000") %>%
  image_annotate(text = "James",
                 color = "#FFFFFF",
                 size = 80,
                 font = "Impact",
                 gravity = "center")

# square three
happy_cat <- image_read("https://media.discordapp.net/attachments/686807262773510168/907591046609928212/IMG_5815.png") %>%
  image_scale(0)

# square four
ml_text <- image_blank(width = 500, 
                       height = 500, 
                       color = "#000000") %>%
  image_annotate(text = "James",
                 color = "#FFFFFF",
                 size = 80,
                 font = "Impact",
                 gravity = "center")
# square five 
sleepy_cat <- image_read("https://media.discordapp.net/attachments/686807262773510168/907591046609928212/IMG_5815.png") %>%
  image_scale(0)
  
  
# square six
cs_text <- image_blank(width = 500, 
                       height = 500, 
                       color = "#000000") %>%
    image_annotate(text = "James",
                 color = "#FFFFFF",
                 size = 80,
                 font = "Impact",
                 gravity = "center")

#resizing james
james1 <- image_resize(confused_cat, "500x500!")
james2 <- image_resize(happy_cat, "500x500!")
james3 <- image_resize(sleepy_cat, "500x500!")





# making each row

# first using the approach we used above
cat_vector <- c(james1, stats_text)
top_row <- image_append(cat_vector)

# second using a different approach
bottom_row <- image_append(c(james2, ml_text))

# third row
third_row <- image_append(c(james3, cs_text))

# making the whole thing!

# using another approach
c(top_row, bottom_row, third_row) %>%
  image_append(stack = TRUE) %>%
  image_scale(800)
```
