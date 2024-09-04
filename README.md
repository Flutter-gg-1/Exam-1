# Exam-1
## Answer and submit the following questions:


## What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?

- GetStorage is a package that enables us to store data locally in form of key and value, it is easy to write and read from an instance of GetStorage. GetStorage is helpful for storing login tokens, scores, recent page or other types of data. The difference between GetStorage and SharedPreferences is that it doesn't require async and await unlike SharedPreferences.

## How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.

- Initialize a GetStorage instance
- write to box
- read from box

class SomeName{
    Stirng value='';

final box = GetStorage();
  SomeName() {
    loadData();
  }

  saveData(String value){
    box.write('key', 'value');
  }

  loadData()async{
    value = await box.read('key');
  }

}

## What is GetIt in Flutter, and how does it help with dependency injection?

- GetIt is a package used for accessing classes from anywhere in the project, this way the class and its data can be accessed without the page being dependant on it, or in other words, without creating and instance of it to use it.

## Describe how to register and retrieve a singleton service using GetIt. Provide an example.

- We need to create a function that imports GetIt and call it in main

setup(){
    GetIt.I.registerSingleton<ClassData>(ClassData());
}

main(){
    setup();
}

## Explain the BLoC pattern in Flutter and how it helps manage state?

- BloC is a pattern used for state management, it organized the changing of widget states into 3 stages, Even, State and Bloc class. The benefit of using BloC is that it allows a single widget to be changed rather than rendering the whole page's components. It significantly improves performance and makes the porject easier to maintain because of seperating most logic in bloc folder.

## How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure. 

- install BloC package "flutter pub add flutter_bloc"
- create classes for Events "Counter Event"
- create classes for States "Increment Stata"
- wrap the page where the event is going to happen in BlocProvider
- wrap the widget with BlocBuilder
- check for states and handle the change.


Bloc:
sealed class CounterBloc extends Bloc<CounterEvent, CounterState>{
QuestionBloc() : super(QuestionInitial()) {
    on<IncrementEvent>((event, emit) {
        emit(IncrementState(++event.counter))
    });

    
  }
}

Event:
final class IncrementEvent extends CounterEvent{
    int counter;
    IncrementEvent(this.counter)
}

State:
final class IncrementState extends CounterState{
    int counter;
    IncrementState(this.counter)
}



HomeScreen:
int counter = 0;
BlocBuilder(<CounterBloc, CounterState>)
...
builder: (context, state) {
if(state is IncrementState){

    return Text('${state.counter}');
}


ElevetaedButton(onPressed:(){
    context.read<CounterBloc>().add(IncrementEvent(counter));
}, child: Text('Increment'));
}
