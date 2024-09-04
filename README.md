# Exam-1
## Answer and submit the following questions:

### What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?

* Get Storage is used to store data in the form of a key-value pair similar to a Map in the Dart language.

* SharedPreferences is useud in a simalr manner, but it is usually used for stroring smaller data sets that are used for settings such as AudioEnabled, Light-Dark preferences...etc.

### How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.

* A box storage is initialized to store the data in the container.

* The storage must be defined in the app in-order for it to be used later-on. Usually, the definition is at the root.

* The data is written to the box using the folowing syntax

    ```bash
    box.wirte('key', 'value');
    ```

* The data can be retrieved from the storage using the follwing syntax:

    ```bash
    box.write('key', 'value');
    ```

### What is GetIt in Flutter, and how does it help with dependency injection?

* GetIt is used for centralized data management. It hepls in dependency injection by containing relevant data models that can be accessed anywhere from the app.

* Similar to GetIt, it is usually defined in the root of the app.

* In our previous use case, we defined the data models to be a singleton in-order to read and modify the same instance.

### Describe how to register and retrieve a singleton service using GetIt. Provide an example.

* The definition starts from the setup function as provided by the documentation of GetIt. The syntax is or close to

    ```bash
    GetIt.I.registerSingleton(DataModel);
    ```

* GetIt is defined at the root of the app in-order to access it later-on.

* The data model defined in the getIt singleton can be accessed later on in the widgets or utiltiy classes using this syntax: 

    ```bash
    GetIt.I.get<DataModel>();
    ```

### Explain the BLoC pattern in Flutter and how it helps manage state?

* The bloc pattern is mainly used for state management
* It has 4 main classes or phases.
    - bloc manager.
    - bloc envent.
    - bloc state.
    - view.

* The view triggers a pre-defined EVENT that is handled by the manager.
* the manager (EMITS or UPDATES) the STATE.
* The view reads the new STATE after the manager performs the pre-defined operation.

### How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure. 

* Create the classes requried for the counter app, which are,
    - counter_bloc.
    - counter_event.
    - counter_state.
    - counter_view.
* The manager handles incrementing the counter logic.
* The event should be defined as (INCREMENT_EVENT).
* The state should read from the manager and update the new number state.
* The view should read from the relevant state inside a BlocBuilder.
