# Exam-1
## Answer and submit the following questions:

# Q1

- What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?

# A1

GetStorage to save Data in a key the return (read) the key and use it where the develper needed;

GetStorage is store a key then use what ever i want it and use it for large data ;
SharedPreferences : we can't use it as json or for the large data;

# Q2
- How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.

# A2

First we need to imlement a package then decleare a getStorage.

Then, we need to store a key for value as box.write(key,value).
if we need to retrive the data must be using box.read(key)
then I can use it the data.

Example : Save Counter the retrive the counter 
  final box = GetStorage();

  saveCounter(int counter) {
    box.write("score", counter);
  }

  loadCounter() {
    if(box.hasData("score")){
    return box.read("score");

    }
    return 0;
  }

  # Q3
- What is GetIt in Flutter, and how does it help with dependency injection?

# A3
GetItt is a Datacenter where I can access to all modeul by GetIt.

# Q4
- Describe how to register and retrieve a singleton service using GetIt. Provide an example.

# A4

First we need to intall the package , then we need to initilaize the GetIT by GetIt.I.registerSingleton<ModeulData>(ModeulData());

if I need to retrive data I can use this 

GetIt.I.get<ModeulData>().--Functions or variables--

Now I can Access to all functions and variabels inside this ModuleData.

# Q5

- Explain the BLoC pattern in Flutter and how it helps manage state?

# A5
the BLoc in flutter has 3 3 categories 

The bloc --> is the manager and known every theing about Events and States

Event --> is taking the orders or taking an action from the user .

State --> update user state 

# Q6
- How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure. 

# A6
First we need to install the package for flutter_bloc

Seconed we need to put BlocProvider at material App

Third we need to create a folder for the bloc .that folder has 3 parts ( Bloc,Event,State)

Forth after inilize the variabels in the pervios step we need to create (Builder,Consumer,Listener) bloc for the Widget I need to updated if I press something 

Fivth , we need to decleare the event (that already inilize it in the pervioes step) if press on something 
