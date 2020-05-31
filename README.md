# Shiny_Dynamic_Interactive_Dashboards
Successfuly Communicating our analytical outputs highlights the hard work we've done along the workflow. Deciders are expecting to have easally interpretable &amp; useful insights that help them take the right decisions. Shiny is the R framework for making web apps without knowing HTML, CSS &amp; JS. Shinydashboard is a package from the Shiny ecosystem that allows analysts who aren't software engineers to develop independently their (scalable) dashboards. We will discover in this repo the shinydashboards package, its main functionnalities and how nowadays it is possible using the R ecosystem to deliver business dashboards that have nothing to envy to MS Power BI, Tableau, Qlick, TIBCO &amp; the other analytics industry leaders

Starting point: 
# Install the package 
install.packages("shinydashboard")
# Load the packages (we need to load Shiny too) 
library(shiny)
library(shinydashboard)

See https://rstudio.github.io/shinydashboard/ for more details and examples 

# The structure 
A dashboard with shinydashboard contains as for general shiny apps a server part and a User interface (UI) one. 

# UI 
Dashboard's UI is compounded of three obligatory parts which are: 
A header: dashboardHeader() function 
A side bar: dashboardSidebar() function 
A body: as in all apps, using the dashboardBody() function 

# Server 
It works the same as general shiny app's server 
Input elements are created in the UI side, allowing the user telling the server what he/she wants, the server will render the correspondant response after performing the adequate treatment.

My_server = shinyServer(function(input, output){
  
})

# UI side
My_ui <- shinyUI(
  
  dashboardPage(
    
    # Part 01
    dashboardHeader(title = "My_dashboard"), 
    
    # Part 02 
    dashboardSidebar(), 
    
    # Part 03
    dashboardBody()
  )
)

# Server side 
My_server = shinyServer(function(input, output){
  
})

# Run the app 
shinyApp(ui = My_ui, server = My_server)

# Important 
Note the following: 
(1) The three parts of the dashboard's UI are puted inside a dashboardPage() function 
(2) The three parts of the dashboard's UI are separated by a comma 
