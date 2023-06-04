# reading-notes

class 01


How would you describe Node to a non-technical friend?

Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine, 
Node.js is a program we can use to execute JavaScript on our computers.
 Node is like a communication system that allows different parts of a computer program to talk to each other effectively. It's widely used for building web applications and can handle multiple tasks simultaneously, making it a powerful tool for developers.



What does it mean that Node is a JavaScript runtime?

it means that Node provides an environment where JavaScript code can be executed outside of a web browser. 

What is Node used for?

 With Node, developers can build the server-side of web applications, which handle tasks like processing data, managing databases, and handling user requests.



 class 02

 
Explain middleware, answer as though I were a non-technical recruiter.
 middleware acts as a bridge or mediator between different parts of a computer program or system, enabling smooth communication and data exchange. It performs tasks like authentication, logging, and data transformation. It helps developers separate concerns and add functionality to the application without modifying its core functionalities.

Express the most popular "JavaScript web framework.

Express is “unopinionated.” What does that mean?
 when we say that Express is "unopinionated," it means that it provides developers with the freedom and flexibility to structure and build their web applications according to their own preferences and requirements. It doesn't enforce strict rules or conventions and allows developers to make their own choices regarding libraries, tools, and coding patterns.


What is a module and why is modularity useful to us as developers?
 module refers to a self-contained unit of code that performs a specific functionality or task. It can be a file, a class, a function, or a collection of related functions and data structures.
 -Code Organization: Modularity helps in organizing code by breaking it down into smaller, manageable pieces.
 -Reusability: Once a module is developed and tested, it can be easily reused in different parts of an application.
 -Testing and Debugging: With modular code, it becomes easier to write unit tests that target specific modules or functionalities.



What version of npm are you running on your machine?
 9.5.0

What command would you type to install a library/package called ‘jshint’ into your node project?
 npm install jshint

Explain why tests are important. Please explain as though I were your non technical elder.
 Imagine you're building a new house. Before moving in, you want to make sure everything is in good condition and works properly. You might inspect the plumbing, test the electrical outlets, and check that the doors and windows open and close smoothly. These checks give you confidence that your new house is safe and comfortable.

 Similarly, tests in software development act as inspections to verify that our code is working correctly. They help us catch and prevent problems early on, saving time and effort in the long run.

What are three expected benefits of testing?
 -Identifying and Preventing Issues Early.
 -Improved Software Quality and Reliability.
 -Facilitating Code Maintenance and Enhancements.

Name at lest 2 individual pitfalls and at least 2 team pitfalls commonly encountered while writing tests.
 -forgetting to run tests frequently
 -writing too many tests at once
 -partial adoption – only a few developers on the team use TDD.
 -poor maintenance of the test suite – most commonly leading to a test suite with a prohibitively long running time.

What are three benefits of Continuous Integration?
 -Early Detection of Integration Issues(With Continuous Integration, developers frequently integrate their code changes into a shared repository. This allows for early detection of integration issues that may arise when different pieces of code are combined).
 -Faster Feedback Loop(CI systems provide immediate feedback on the quality and correctness of the changes,e shorter feedback loop minimizes the time spent debugging and troubleshooting, accelerating the overall development process.)
 -Improved Code Quality and Stability(Since code changes are frequently integrated and tested, any potential issues or regressions can be caught and fixed early).

What is the difference between Continuos Delivery and Continuous Deployment?
 Continuous Delivery focuses on automating the software delivery pipeline, ensuring that the software is always in a releasable state, but requires manual intervention to trigger the actual deployment. On the other hand, Continuous Deployment automates the entire deployment process, automatically releasing changes to production once they pass all tests and quality checks

Explain how GitHub fits into this process assuming the listener comes from a non-technical background?
 GitHub is a web-based platform that plays a crucial role in the software development process, particularly in the context of version control and collaboration. Let's explore how GitHub fits into the Continuous Integration (CI) and Continuous Deployment (CD) process
 -Version Control(GitHub serves as a version control system, allowing developers to track changes made to their codebase over time. It provides a centralized repository where developers can store and manage their source code. This enables teams to collaborate on projects effectively, as multiple developers can work on the same codebase simultaneously, making changes and tracking those changes in an organized manner).
 -ollaboration and Code Review(GitHub facilitates collaboration among developers by providing features for code review and discussion).
 -Continuous Integration( GitHub integrates with various CI platforms (such as Travis CI, Jenkins, CircleCI) that automate the build, test, and deployment processes)
 -Continuous Deploymen(GitHub can be linked to deployment tools or services that enable the automated release of code changes to production environments).