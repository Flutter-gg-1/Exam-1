# Exam-1
## Answer and submit the following questions:
- What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?

- it's laibrary for store the data in the mobaile storge 


- How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.

box.write ("key",value);

- What is GetIt in Flutter, and how does it help with dependency injection?

-Gitit is a library can for class injection so we can use it multbale time in other pages with and we don't need to difiend an object evry time 

- Describe how to register and retrieve a singleton service using GetIt. Provide an example.

-Gitit.i.registersingleton<taskdata>(taskdata);

- Explain the BLoC pattern in Flutter and how it helps manage state?

- BloC can healp the app with refrish widget with out using set satete and it can healp to orgnaize the the project and increace the performance (so we use it to setstat or refich only the bloc that we need with out refresh all the page)

- How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure. 

1- using bloc provider in main page with material app.
2-implement the Bloc in the fail by clicking on the file then we chose the bloc
4-we have 3 structure in Bloc:
1-bloc event
2-bloc
3- state bloc