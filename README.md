# Exam-1
## Answer and submit the following questions:
- What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?

answer:
GetStorage  allows you to store and retrieve simple key-value pairs in the device's local storage.

- How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.

answer:
by using the .read() and .write() methods.

- What is GetIt in Flutter, and how does it help with dependency injection?

answer:
GetIt is a service locator for Flutter apps.
it is used to register and retrieve services.
better than singleton.

- Describe how to register and retrieve a singleton service using GetIt. Provide an example.

answer:
describe
GetIt not like a GlobalVariable but it allows you to register and retrieve a singleton service. as a global file. 
setup
GetIt.I.registerSingleton<CounterService>(CounterService());
call
GetIt.I<CounterService>().increment();

- Explain the BLoC pattern in Flutter and how it helps manage state?

answer:
BLoC pattern in Flutter helps manage state.
separate state management from UI.
separate event handling from UI.
Using 7 or 4 architectural principles.


- How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure. 

answer:
1- import flutter_bloc package
2- import 'package:...;
3- Add Bloc folder
4- Add counter_bloc.dart
5- Add counter_event.dart
 Action and Event
6- Add counter_state.dart
 Show the state(change in UI)
7- Add BlocProvider in main.dart if you want to use it in ALL trees
8- Add BlocBuilder or BlocListener or BlocConsumer as you want in your cases
