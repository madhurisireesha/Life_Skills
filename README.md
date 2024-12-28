
#   MVC Architecture and Spring

## MVC Architecture 

* MVC stands for Model-View-Controller is a design pattern that is commonly used for developing and organizing the code of the application.

* MVC can be both design pattern and architectural pattern because it provides guidelines for designing the code and also provides the guidelines for overall organization of the application. 

* MVC is a versatile pattern that can be used to design webapplications,desktop applications,mobile applications and other software systems.

* In MVC, the model represents applications and other software systems logic.

* The MVC controller acts as intermediatory between the model and the view.In MVC view is responsible presenting data to the user in an understandable format and also responsible for collecting data from the user.

### Model:
* In MVC, model responds to the request from the controller,and it retrives, manipulates data as required.
* Model notifies the view through controller with respect to changes in the data that needs to be updated in the view.

### View:

* View displays the data provided by model an interacts with users or clients.Normally, view doesnot contain any business logic and its primary goal is to present information to the user in an understandable manner.

### Controller:
* It receives input from the user via view,processes that input and redirect the request or input to the model and performs equivalent action.
* In web applications the controller often handles HTTP request along with acting as intermediatory between model and view.
* Withrespect to spring boot application,Controller is connected to services further services connected to repository which inturn connnected to database.
* THat connection between controller,services and repository can be done either manually with the help of constructors or with the help of annotations annually.

# SPRING MVC:
* It is a Java framework which is used to build web applications.If follows the Model-View-Controller design pattern.
* SPring MVC provides a dignified solution to use MVC in spring framework with the help of a dispatcher servlet.Dispatcher servlet is a class tht receives incoming requests and maps into the right resource such as controller model and  view.
* The MVC controllerof spring framework comprised of a web browser a front controller model and view.
* Model contains core data of the application data can be either be a single object or a group of objects.
Controller contains the business logic of an application we can add controller annotation to mark the class as a controller class.
View is used to represent the information in a particular format.

# Spring MVC Workflow
![Workflow](https://media.geeksforgeeks.org/wp-content/uploads/20220224160807/Model1.png)

* When a request is sent,the incoming request is intercepted by the DispatcherServlet that works as the front controller.
* THe DispatcherServlet gets an entry of handler mapping from the XML file and forwards the request to the controller.
* The controller returns an object of   Model and View.
* THe DispatcherServlet checks the entry of view resolver in the XML file and invokes the specified view component.



# References:
* https://youtu.be/Bel2aWpWZWE?si=TBP157oP613D72JK
* https://www.javatpoint.com/spring-mvc-tutorial
* https://www.tutorialspoint.com/spring/spring_web_mvc_framework.htm



