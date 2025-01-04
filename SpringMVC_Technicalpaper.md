
#   MVC Architecture and Spring

## MVC Architecture 

* MVC stands for Model-View-Controller is a design pattern that is commonly used for developing and organizing the code of the application.

* MVC can be both a design pattern and an architectural pattern because it provides guidelines for designing the code and also provides guidelines for the overall organization of the application. 

* MVC is a versatile pattern that can be used to design webapplications,desktop applications,mobile applications and other software systems.

* In MVC, the model represents the logic of applications and other software systems.

* The MVC controller acts as intermediatory between the model and the view.In MVC view is responsible presenting data to the user in an understandable format and also responsible for collecting data from the user.

### Model:
* In MVC, the model responds to the request from the controller, and it retrieves and manipulates data as required.
* Model notifies the view through the controller concerning changes in the data that need to be updated in the view.

### View:

* View displays the data provided by the model and interacts with users or clients. Normally, the view does not contain any business logic and its primary goal is to present information to the user in an understandable manner.

### Controller:
* It receives input from the user via view, processes that input redirects the request or input to the model, and performs equivalent action.
* In web applications the controller often handles HTTP requests along with acting as an intermediatory between model and view.
* With respect to the spring boot application, the Controller is connected to services, and further services are connected to the repository which in turn is connected to the database.
* That connection between the controller, services, and repository can be done either manually with the help of constructors or with the help of annotations annually.

# SPRING MVC:
* It is a Java framework which is used to build web applications. If follows the Model-View-Controller design pattern.
* Spring MVC provides a dignified solution to use MVC in the spring framework with the help of a dispatcher servlet. The Dispatcher servlet is a class that receives incoming requests and maps into the right resource such as controller model and view.
* The MVC controller of the spring framework comprised a web browser a front controller model and a view.
* Model contains core data of the application data can be either a single object or a group of objects.
The controller contains the business logic of an application we can add controller annotation to mark the class as a controller class.
The view is used to represent the information in a particular format.

# Spring MVC Workflow
![Workflow](https://media.geeksforgeeks.org/wp-content/uploads/20220224160807/Model1.png)

* When a request is sent, the incoming request is intercepted by the DispatcherServlet which works as the front controller.
* The DispatcherServlet gets an entry of handler mapping from the XML file and forwards the request to the controller.
* The controller returns an object of the Model and View.
* The DispatcherServlet checks the entry of the view resolver in the XML file and invokes the specified view component.



# References:
* https://youtu.be/Bel2aWpWZWE?si=TBP157oP613D72JK
* https://www.javatpoint.com/spring-mvc-tutorial
* https://www.tutorialspoint.com/spring/spring_web_mvc_framework.htm



