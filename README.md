# Exam-1
## Answer and submit the following questions:
- What is GetStorage in Flutter, and how does it differ from other local storage options like SharedPreferences?

 هو وسيله نخزن فبها لولكلي 
 سهلة الاستخدام 
 تتعامل مع فلتر 
 نقدر نستخدمها مع json 



- How can you store and retrieve simple key-value pairs using GetStorage? Provide a code example.

اسوي تنزيل للبكج بالباديه 
import 'package:get_storage/get_storage.dart'; 
او انزلها من yaml او من terminal
اعرف متغير 
final box = GetStorage();
اذا انا ابي اكتب احتاج للقيمه والمفتاح 
box.write('key', 'value');
وهنا لما ابي اكتب 
String? value = box.read('key');



- What is GetIt in Flutter, and how does it help with dependency injection?


- Describe how to register and retrieve a singleton service using GetIt. Provide an example.final getIt = GetIt.instance;
singletonاسجل بالبدايه 
واسترجع القيمه باستخدام get
// تسجيل 
getIt.registerSingleton<MyService>(MyService());
// استرجاع 
MyService myService = getIt.get<MyService>();

- Explain the BLoC pattern in Flutter and how it helps manage state?

UI نظم الكود بالمنطق بغض النظر عن 
يتعامل مع الاحداث والحالات 
يبسط لي فهم الكود لانه يعبر عن حاله في كلاس والحدث في كلاس ...
ايضا في حاله حدوث خطا يسهل صيانته 

- How do you implement a BLoC for managing the state of a counter app? Outline the steps and code structure. 

انشاء بلوك من ثلاث :بلوك ، حاله، حدث 
بكتبها على مثال كاونتر الي خذناه 


 إنشاء BLoC:أنشى counterBloc يكون فيه اداره 
 

  Eventالأحداث: أنشئِ فئة CounterEvent تحتوي على  الأحداث مثل IncrementوDecrement.

   State الحالات :أنشئ فئة CounterState التي تحتوي على الحالة الحالية للعداد.

