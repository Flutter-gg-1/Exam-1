# Exam-1
## Answer and submit the following questions:
- What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?
It is a local storage that assist in saving app data and store it even after restarting the app.

- How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.
we will need to inisilize a GetStorage attribute, for example box, to add to it we need to pass the data and add it box.add(the data). 

- What is GetIt in Flutter, and how does it help with dependency injection?
GetIt assist in accessing different attributes without the need of initializing the same attributes multible times.

- Describe how to register and retrieve a singleton service using GetIt. Provide an example.
we will need to set it, include the setup in main before starting the app, and pass the data we need for example Getit.I<dataList>(dataList) and than we can access the data of the object without initializing it everytime 

- Explain the BLoC pattern in Flutter and how it helps manage state?
BLoC pattern help seperating UI and logic code, update widgets without the need of using stateful widgets, we have three type of blocs: build bloc which returns a widget, listener bloc which operate without the need to return anything, and constructer bloc which includes both builder and listener bloc.


- How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure. 
We will need to install the bloc dependency, add bloc files (bloc, event and state), add a state and an event for incrementing the counter, and in bloc we add the operations we want to do using the state and the event. In the counter widget, which mostly includes a text widget to view the counter and an add button, we will add the event in the button onPress functuon, than add the builder to the whole widget and return the state in the Text widget.
