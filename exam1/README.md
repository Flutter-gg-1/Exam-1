# Exam-1


## What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?

GetStorage is a local storage for storing a data

## How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.

assume we hava a list of user data
List userData = [];
1. initilize get storage 
final box = GetStorage();
2. retrive key-value
box.read("data")
3. store data 
box.write("data", userData);

## What is GetIt in Flutter, and how does it help with dependency injection?

GetIt is a centerlized data which can be accessed by any other classes

## Describe how to register and retrieve a singleton service using GetIt. Provide an example.

1. initilize a singleton 

GetIt.I.get<singleton>();

2. retrieve a singleton
GetIt.I.get<UserData>().userData;

## Explain the BLoC pattern in Flutter and how it helps manage state?

BLoc is design pattern between UI and data, its consist of BLoc, state and evvent.

BLoc is manager of state and event
state is the output of user interaction
event in user interaction of UI

## How do you implement a BLoC for managing the state of a counter app?

implementing a two BLoc states one for increment counter by 1 and other for decrementing counter by 1, and defining two events.
In BLock class imlements ligic of incremeneting and decremneting counter by using on<event>






