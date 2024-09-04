# Exam-1
## Answer and submit the following questions:
- What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?
get storge is used to store data localy in app so that the data will be saved even if user reload the app or exit app, it will be stored in the app not in the divace so once we delete the app data will be deleted with app



- How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example. 
first we must intialize gitStorge so the data will be retrive once the app is opend after that we will create a variable from gitStorge like `box` that we will use it to `store`, `read`, `save` and `load` data .




- What is GetIt in Flutter, and how does it help with dependency injection?
it provide one acess to data, so ineasted of intializre data in each widget or class GetIt provide acess to data from evreywhere in project 


- Describe how to register and retrieve a singleton service using GetIt. Provide an example.
here we will create method to intialize GetIt using Future  
  `GetIt.I.registerSingleton<data>(data());`
  after that we will apple to acess it using `GetIt.I.` and the method we wants



- Explain the BLoC pattern in Flutter and how it helps manage state?
we can use block lessener for show snack bar or bottom shhet 
and block provider if we want to return widgets
and block consumer if we want bothe of theme


- How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure. 
bloc consiste of three thing firs the bloc it self here we can use it for condtions for example 
and state will be used for UI and actions
events is used for  logic and if action success
this will help in organaize code and reathe than update the hole scrren we can use it for update only part of code like counter button or text

