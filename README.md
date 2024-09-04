# Exam-1
## Answer and submit the following questions:
### What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?
- gitstore store date using key and value where sqllite using sql 
### How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.
- box.save("key",value); , var value = box.read("key",value);
### What is GetIt in Flutter, and how does it help with dependency injection?
- GetIt apply the concept of singleton where all data refere to one class that store data it help reduce deplucate code.  
#### Describe how to register and retrieve a singleton service using GetIt. Provide an example.
- GeIt.I.RegisterSingliton<className>(className); 
var value = GeIt.I.get<className>().Varibale;
### Explain the BLoC pattern in Flutter and how it helps manage state?
- Bloc made in three parts Bloc, event and state 
event is a user action whare happen like click button, than blec update state based on state model based on event then state relfect (rebuild) on widget based in is state compare to setState rebuild scaffold again.

### How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure. 
1- create bloc provider whech in a scaffold 
2- create State 
```
class ShowCounterState extend state{
final int counter;
ShowCounterState({required this.counter});
}
```
3- create evenet to trigger bloc 
```
class CounterEvent extend event{}
```

4- create login in bloc body
```
on<CounterEvent>((emit,state){
emit.CounterState(counter:++counter)
})
```

5- build in wdiget 
```
builder(
context:context,
body:
BlocBuilder((CounterBloc, CounterState)
build: (state,context)
/////build state
)
)
```

