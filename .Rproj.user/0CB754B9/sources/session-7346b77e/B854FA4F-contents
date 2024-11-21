#
# This is a Shiny web application. You can run the application by clicking
# the 'Run App' button above.
#
# Find out more about building applications with Shiny here:
#
#    https://shiny.posit.co/
#

library(shiny)

# CLASIFICACION
ui <- fluidPage(
  titlePanel("Clasificación f7"),
  tags$head(
    tags$style(HTML("
      table, th, td {
        border: 1px solid black;
        padding: 4px;
        border-collapse: collapse;
      }
      th {
        background-color: #f2f2f2;
        width:60px;
      }
     td{width:60px;}
    "))
  ),
  tags$table(
    tags$th("Pos"),
    tags$th("Equip"),
    tags$th("J"),
    tags$th("G"),
    tags$th("E"),
    tags$th("P"),
    tags$th("GF"),
    tags$th("GC"),
    tags$th("DF"),
    tags$th("PT")
  ),
  tags$table(
    tags$td("1"),
    tags$td("ABANCA"),
    tags$td("2"),
    tags$td("2"),
    tags$td("0"),
    tags$td("0"),
    tags$td("18"),
    tags$td("5"),
    tags$td("13"),
    tags$td("6")
  ),
  tags$table(
    tags$td("2"),
    tags$td("EMALCSA"),
    tags$td("3"),
    tags$td("2"),
    tags$td("0"),
    tags$td("1"),
    tags$td("15"),
    tags$td("9"),
    tags$td("9"),
    tags$td("6")
  ),
  tags$table(
    tags$td("3"),
    tags$td("REFINERA"),
    tags$td("2"),
    tags$td("2"),
    tags$td("0"),
    tags$td("0"),
    tags$td("9"),
    tags$td("4"),
    tags$td("5"),
    tags$td("6")
  ),
  tags$table(
    tags$td("4"),
    tags$td("KPMG"),
    tags$td("2"),
    tags$td("1"),
    tags$td("1"),
    tags$td("0"),
    tags$td("11"),
    tags$td("7"),
    tags$td("4"),
    tags$td("4")
  ),
  tags$table(
    tags$td("5"),
    tags$td("ABOGADOS"),
    tags$td("2"),
    tags$td("1"),
    tags$td("1"),
    tags$td("0"),
    tags$td("9"),
    tags$td("8"),
    tags$td("1"),
    tags$td("4")
  ),
  tags$table(
    tags$td("6"),
    tags$td("URBEKO"),
    tags$td("3"),
    tags$td("1"),
    tags$td("0"),
    tags$td("2"),
    tags$td("13"),
    tags$td("18"),
    tags$td("-5"),
    tags$td("3")
  ),
  tags$table(
    tags$td("7"),
    tags$td("TORUS"),
    tags$td("1"),
    tags$td("0"),
    tags$td("0"),
    tags$td("0"),
    tags$td("3"),
    tags$td("7"),
    tags$td("-4"),
    tags$td("0")
  ),
  tags$table(
    tags$td("8"),
    tags$td("BBVA"),
    tags$td("2"),
    tags$td("0"),
    tags$td("0"),
    tags$td("2"),
    tags$td("4"),
    tags$td("10"),
    tags$td("-6"),
    tags$td ("0")
  ),
  tags$table(
    tags$td("9"),
    tags$td("DENODO"),
    tags$td("2"),
    tags$td("0"),
    tags$td("0"),
    tags$td("2"),
    tags$td("6"),
    tags$td("14"),
    tags$td("-8"),
    tags$td("0")
  ),
  tags$table(
    tags$td("10"),
    tags$td("EY"),
    tags$td("1"),
    tags$td("0"),
    tags$td("0"),
    tags$td("1"),
    tags$td("1"),
    tags$td("10"),
    tags$td("-9"),
    tags$td("0")
  ),
)
# Lógica del servido
# Define UI for application that draws a histogram
#ui <- fluidPage(

    # Application title
    #titlePanel("Old Faithful Geyser Data"),

    # Sidebar with a slider input for number of bins 
   # sidebarLayout(
        #sidebarPanel(
            #sliderInput("bins",
     #                   "Number of bins:",
                        #min = 1,
                        #max = 50,
                        #value = 30)
    #    ),

        # Show a plot of the generated distribution
       # mainPanel(
          # plotOutput("distPlot")
  #      )
 #   )
#)

# Define server logic required to draw a histogram
server <- function(input, output) {

    output$distPlot <- renderPlot({
        # generate bins based on input$bins from ui.R
        x    <- faithful[, 2]
        bins <- seq(min(x), max(x), length.out = input$bins + 1)

        # draw the histogram with the specified number of bins
        hist(x, breaks = bins, col = 'darkgray', border = 'white',
             xlab = 'Waiting time to next eruption (in mins)',
             main = 'Histogram of waiting times')
    })
}

# Run the application 
shinyApp(ui = ui, server = server)
