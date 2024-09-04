# Exam-1
## Answer and submit the following questions:
- What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?



  - ans : GetStorage will save data in local storge and SharedPreferences will do the same
  - the difrent is GetStorage will store big data but SharedPreferences will save only simple data and cant save list




---


- How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.

  - to store data by key like this

  box.write(key, value);



  - to get value by key 

    box.read(key)



---




- What is GetIt in Flutter, and how does it help with dependency injection?



   - GetIt is way to control data so any where in the code can get this data with structure way 


   - one way that can help is you can the data or method anywhere in the code and make eazy to acces it with out it you need to pass data to the palce you want that can be  complex some time and take time



---


- Describe how to register and retrieve a singleton service using GetIt. Provide an example.

   - first need to setup the GetIt like this  and will be the global vlaue and where you can acces:

     final getIt = GetIt.instance;


    - sceond make Singleton that is class that cant make obj form it that will have all data :

    getIt.registerSingleton<AppModel>(AppModel());


    - and like this you get register any where in the code :

    getIt.get<AppModel>()


---


- Explain the BLoC pattern in Flutter and how it helps manage state?


   BLoC is way to structure your code in way that will help you read the code and edit it  will have 3 elment to it



   - one is the state here will make some state that will change depend on your logic and can take data so then can show it in the ui


   - scond is the event : the event will help for exmaple when user click on somthing the event trgier and  will handle it in the bloc stage



   - the third and the last is bloc here will most your logic  here can also handle your event and after you handle can emit the state you want and will show to your blocBuldier









---
- How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure. 




- first will make bloc that have this :

- state to show data that have number 


- two event one is add and the other del


- in the bloc will have total number

  -  if the evnet that tregier is add will add to the total and then emit to the ui using blocbuilder


  - if the event was  del we will first check if the total is not zero if it was we will not decress the number but if not we will decress and then emit to the blocbuider





- blocbuider will have argument called buider that will check what state he resived and if he not resived any state will return defult widget if he  resived will take from the state the number then show it in the ui









