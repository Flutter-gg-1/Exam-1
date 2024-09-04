# Exam-1
## Answer and submit the following questions:
- What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?\
**Answer** : GetStorage is a package in flutter that enables storing data in the local storage of the app, it uses the concept of key-value where any saved items/variables can be saved in a key and retrieved with that defined key. 

- How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.
**Answer** : after installing the package, this process can be done in three simple steps :\
1) Define the box which we are using to store and retrieve data using `GetStorage()`.
```dart
final box = GetStorage();
```

2) In writing/storing case: we use `box.write()`, it takes two arguments, first is the key's name, second is they key's value.
```dart
box.write('someKey',someValue);
```
Now, `someValue` is saved in the box, specefically inside the `someKey` key.

3) In reading/retrieving case: we use `box.read()`, it takes one argument which is the key's name.
Note : the datatype of the returned value from `box.read()` is the same datatype of the stored value in the box. For example : suppose `someValue` is a String, we can do the following.
```dart
String retreived = box.read('someValue');
```

- What is GetIt in Flutter, and how does it help with dependency injection?
**Answer** : GetIt is a service locator and design pattern in flutter, it is used to access some variables globally in any file in the project, it is more secure and safe to use.

- Describe how to register and retrieve a singleton service using GetIt. Provide an example.\
**Answer** : after installing the package, this process can be done in three simple steps :
1) Define the class which we are using.
```dart
class Person {
    final String name;
    final String age;

    sayHello() {
        return 'hello $name';
    }
}
```

2) Register a singleton using a helper function `setup()`, this function should be called in `main.dart`.
```dart
GetIt.I.registerSingleton<Person>(Person());
```

3) retrieve data.
```dart
Text(GetIt.I.get<Person>().sayHello())
```

- Explain the BLoC pattern in Flutter and how it helps manage state?
**Answer** Bloc updates the specific widget, stateful updates all page

- How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure.