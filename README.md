# Exam-1
## Answer and submit the following questions:
- What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?
- How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.
- What is GetIt in Flutter, and how does it help with dependency injection?
- Describe how to register and retrieve a singleton service using GetIt. Provide an example.
- Explain the BLoC pattern in Flutter and how it helps manage state?
- How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure. 

//Answer 1
- GitStorage is flutter package to store info localy in the app cash it use what called box to write , read , and other function to udate the data and store it locally it can store String,int,list the defrrinte between it and the other that she store the same data withe same type not like other such as they store the object .

//Answer 2
- first i should :
1-add the getstorage package
2-add to the main using async and for avoid futere problem i used in main WidgetFlutterBiding.ensureBiding();
3-then i call the getstorage and define variable from usually called box => final box = GetStorage.init();
4- then i read or write or remove variable with the boc var 
5-example if i have string name : box.write('name',name); for get the name : box.read('name');

full code : class GetData{
    String myName = 'Basel";
    final box = GetStorage.init();

    //save the name
    box.write('name',myname);

    //get the name
    String fullName;
    fullName = '${box.read('name')} Saad Alalawi';

}

//Answer 3
git_it is flutte package the use for globalvriable it help for make a variable global so dev can acsess to it from 
any where in the project by using get_it

//Answer 4
1-inastall get_it package
2-create instance from git_it packges
3-then add the data class that i want to get data or method from it 
4-all the previos step add to function and add it to the main

example : 
import 'here get_it packages'
setup(){
    GetIt = GetIt.retrievesinglton<DataClass>(DataClass());
}

in my class 
class DataClass{
    String name = 'Basel';
}
class Test{
String name = GetIt.I.get<DataClass>().name;
print(name);
}

//Answer 4
the bloc is state managment the contain three part :
1-bloc
2-State
3-Event

it seprate UI and logic from each other and update the spcific part 
from the code using state and event not like the regular setState wich
update the whole page

//Answer 5
--folder bloc
      --CounterBloc.dart
      --BlocState.dart
      --EventBloc.dart

add the State IncrementState & decrmentState to stae folder

add event plusEvent and minusEvent to Event Folder

add state in bloc folder using on<AddState>(){
    emit(AddState())
}

call bloc builder inn the place that i want to update the counter and checkk the state
builder : if(state is AddState){
    My logeic
}