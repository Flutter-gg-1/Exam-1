# Exam-1
## Answer and submit the following questions:
### - What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?
  
  it is a paekage that offer a local storge. more opitons like erase the local storage.
  
### - How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.

\\ inisilaze the storage

final box = getStorage();

\\store data

box.write("key",value);

\\ retrieve data 

box.read("key",value);

### - What is GetIt in Flutter, and how does it help with dependency injection?
  
   GetIt is a paekage that offer user to create a singal object so he can access and edit it from diffrent files.
  
### - Describe how to register and retrieve a singleton service using GetIt. Provide an example.
 
\\ Register

  GetIt.I.singleton<Model()>(Model());
  
\\using GetIt

GetIt.i.get<dataClass>().what_You_Wnat_to_Access

### - Explain the BLoC pattern in Flutter and how it helps manage state?

BLoC is a paekage deivide the code in blocs in a sinse way that will make it easy to manage

main component in BLoC:

state-event-bloc

Event: that will trigger the wanted function

State: the state where the updates will be viwes.

Bloc: where the logic of this specfic bloc


### - How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure.

  \\Event

  Class addEvent (){}

  \\State

  Class countState (){
final int num;

countState({required this.num});
  }

  \\Bloc
  int count;

  we emit the updated to state here
  
  emit(countState(num: count++))

  \\in home screen

  add a bloc builder to the part will be updated

  add in button

  context.read<blokname>(event);
