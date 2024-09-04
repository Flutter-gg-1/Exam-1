# Answer and submit the following questions:


## What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?

It's a package provided in pub dev, usually data get stored in RAM while running/testing a program , but with getstorage which help you to store data locally on your pc without losing the data upon a restart or shutdown , 


## How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.

first you need to create the storage by using GitStorage() , and declare it with a variable , Ex: final box = GetStorage("key",value) first value inside the box is the key , the second is the value which can take any type , but when you write again in the same key, it will remove the previous value and add the new one , basically overriding 


## What is GetIt in Flutter, and how does it help with dependency injection?

GetIt is to have a centeral place where you can update data at , hence every other files can reach to the same data , and if the data changes , it will change on all the files aswell. 


## Describe how to register and retrieve a singleton service using GetIt. Provide an example.

   getIt.registerSingleton<QuestionsData>(QuestionsData()); is for registering Singleton , to retreive from it we use 
   GetIt.I.get<QuestionData>(). then you can reach whatever inside the class QuestionData



## Explain the BLoC pattern in Flutter and how it helps manage state?

BLoC pattern takes the state , event and the bloc itself . 
it helps to reload a state of a specific widget , setState does the same thing but it reload the whole builder to do a simple change that happened on the screen and this can be a really big issue when dealing with big projects . that's why it's better to use bloc


## How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure.

first we can provide a block provider on the main page (MainApp) or u can provide it on a specific screen , but the provider is very important without it nothing will change. 
then we can deal with the state/event/bloc 
we gave an example saying bloc is like the resturaunt and event is like making the food and state is like deliviring it . 

to make the counter app , we can create a new classState in the state file section named CounterState, and u can give it an integer , 
then on the event section we add a class named AddToCounterEvent
then on the block, we make it listen on<AddToCounterEvent> 
and on the same file we define a counter to start with 0 , and on each emit we do inside the event listner , we increase counter by 1 counter++