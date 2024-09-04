# Exam-1
## Answer and submit the following questions:
- What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?
  
 it allows the programmer to save app data insie the user deviceit allows us to save files not like shared preference

- How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.

getStorage().read(["key"]);

- What is GetIt in Flutter, and how does it help with dependency injection?

get it is dependency injection library that enables the programmer to take only one object of some class and access it every where in the project

- Describe how to register and retrieve a singleton service using GetIt. Provide an example.

1-install the dependency 
2-inside the main "GetIt.I.SingletonService();"

- Explain the BLoC pattern in Flutter and how it helps manage state?

BLoC is a state management pattern, it helps in changing the state of each widget(or multiple widget) independently, without using state management systems we need to use "setState((){})" which will change the state of of the whole page

- How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure. 

in order to use bloc we need to create three files:

1-counter_bloc.dart
2-counter_event.dart
3-counter_state.dart

in the event we will initialize:

  final class AddEvent extents CounterEvent{}

in the event we will initialize:

  final class AddState extends counterInitial(
    final int num;
    AddState({required this.num});
  )

  in the bloc 
  on<AddState>((event.emit){
    emit(....);
  })



  and we will call the bloc on the button or any trigger we choose
