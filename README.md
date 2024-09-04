# Exam-1
## Answer and submit the following questions:
- What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?
    - GetStorage it's tools to save data in device as key-value
    - differ
      - Performance: GetStorage is generally faster.
      - Reactive Features: GetStorage allows listening for changes to specific keys.
      - Type Safety: GetStorage provides better type safety, reducing the need for manual type casting.
      - Initialization: GetStorage requires explicit initialization before use, while SharedPreferences is typically ready to use immediately. 
      - Integration: GetStorage is part of the GetX ecosystem, which can be beneficial if using other GetX features.


- How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.
    - To store data : `GetStorage().write('Key', Data);`
    - To retrieve data: `GetStorage().read('Key you want to read its value');`


- What is GetIt in Flutter, and how does it help with dependency injection?
    - Its simple service locator to register data and make it centralized and easy to get it from anywhere using dependency injection.


- Describe how to register and retrieve a singleton service using GetIt. Provide an example.
  - To register : 
    - `final getIt = GetIt.instance;`
    - `getIt.registerSingleton<MyData>(MyData());`
  - Tow way to retrieve:
    - `final myService = getIt<MyData>();`
    - `data = GetIt.I.get<MyData>().AllData;`


- Explain the BLoC pattern in Flutter and how it helps manage state?
  - The BLoC pattern helps to manage state by providing a structured way to handle user inputs, process data, and emit state changes 
    to keep UI simple and cleaned code.

    
- How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure.
  - create 3 file and named counter_bloc, counter_event, counter_state
  - in counter event add 2 class increes and decrease 
  - in counter_state init the state to store data
  - in counter_bloc add on<increes> and emit changes to update states.

  
