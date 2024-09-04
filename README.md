# Exam-1
## Answer and submit the following questions:
 - What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?
    is a way to store the data localy by install GetStorage library 
 - How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.
    first we define a varibal name :
     final var box = GetStorage();
     saveData(){
        box.write("name");
     }
     loadData(){
        box.read("name");
     }

- What is GetIt in Flutter, and how does it help with dependency injection?

is a Centrilaiezd way to manipulate the data in the flutter it can get data from the data model and handell it in overall yours screen .

- Describe how to register and retrieve a singleton service using GetIt. Provide an example.

in setup file :

GetIt.I.registerSingleton<CounterService>(CounterService());


- Explain the BLoC pattern in Flutter and how it helps manage state?
the Bloc have three classes : 
event class , state class ,Bloc class
first event class will do event that you define 
then create  state class that will difen your state that you want to  apper 
and the logic code will be Block class 

- How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure. 
first add builerProvider in the main 

Define an eventcounter class
final supEvet extends  eventcounter ();

Define an Statecounter class
final supEvet extends  eventcounter ();


create a Bloc class for UI
on <supEvet> (event , emit)){
    emit(Increamentstat(event)
}
