### Computers dunno what dogs are
![dogs](images/dogs.jpg)



### A dog is an object
+ it has state (**instance variables**)
  - name
  - breed
  - dominant color
  - weight
+ it has behavior (**methods**)
  - bark
  - wag tail
  - eat
  - play
  - jump



### A phone is an object
+ it has state (**instance variables**)
  - brand
  - model
  - screen size
  - powered on?
+ it has behavior (**methods**)
  - turn on
  - turn off
  - send SMS
  - call
  - install app



## You write a class to define what an object means in your application

+ three parts in general
  - class name
  - instance variables
  - methods



### Classes have three sources
+ from the programming langauge API
  - DateTime
  - String
  - File
+ written by other people as open-source packages
  - XlsxDecoder
  - FacebookLogin
  - EmojiPicker
+ written by you or your teammates



## It is unlikely for Dart or pub.dev to have a Dog class, so we write our own



### Writing a class in almost any statically-typed language (1/3)

```dart [1]
class Dog {
  String name;
  String breed;
  int weight;
  String dominantColor;

  void bark() {
    print("Arf!");
  }
}
```

Each class should have a name



### Writing a class in almost any statically-typed language (2/3)

```dart [2-5]
class Dog {
  String name;
  String breed;
  int weight;
  String dominantColor;

  void bark() {
    print("Arf!");
  }
}
```

Instance variables are declared like normal Dart variables, specifying the type, rather than just
`var`.



### Writing a class in almost any statically-typed language (3/3)

```dart [7-9]
class Dog {
  String name;
  String breed;
  int weight;
  String dominantColor;

  void bark() {
    print("Arf!");
  }
}
```

Methods are just Dart functions, just like when you write `void main()`.



### One class can be used to create many dog objects (**instances**)

<div style="display: flex">
  <div style="flex: 1">
    <img src="images/dogs.jpg" alt="dogs" style="width: 640px; height: 320px;">
  </div>
  <div>
    <div style="text-align: left; margin-bottom: 20px">Left dog:</div>
    <ul>      
      <li>name: Gidget</li>
      <li>breed: Pomeranian</li>
      <li>weight: 35</li>
      <li>dominantColor: white</li>
    </ul>
  </div>
</div>



### One class can be used to create many dog objects (**instances**)

<div style="display: flex">
  <div style="flex: 1">
    <img src="images/dogs.jpg" alt="dogs" style="width: 640px; height: 320px;">
  </div>
  <div>
    <div style="text-align: left; margin-bottom: 20px">Middle dog:</div>
    <ul>      
      <li>name: Mel</li>
      <li>breed: Pug</li>
      <li>weight: 45</li>
      <li>dominantColor: brown</li>
    </ul>
  </div>
</div>



### One class can be used to create many dog objects (**instances**)

<div style="display: flex">
  <div style="flex: 1">
    <img src="images/dogs.jpg" alt="dogs" style="width: 640px; height: 320px;">
  </div>
  <div>
    <div style="text-align: left; margin-bottom: 20px">Right dog:</div>
    <ul>      
      <li>name: Max</li>
      <li>breed: Terrier Mix</li>
      <li>weight: 60</li>
      <li>dominantColor: white</li>
    </ul>
  </div>
</div>



### Creating instances (instantiation)

```dart [1-6 | 7-14 | 16-18]
  // most programming languages need the `new` keyword
  var leftDog = new Dog();
  leftDog.name = 'Gidget';
  leftDog.breed = 'Pomeranian';
  leftDog.weight = 35;
  leftDog.dominantColor = 'white';

  // in Dart, `new` is optional and recommended
  // especially when instantiating Flutter widgets
  var middleDog = Dog(); // Python anyone?
  middleDog.name = 'Mel';
  middleDog.breed = 'Pug';
  middleDog.weight = 45;
  middleDog.dominantColor = 'brown';

  // make each dog bark
  leftDog.bark();
  middleDog.bark();
```

You do rightDog as an exercise




### Exercise: Make small dogs bark Yip, medium dogs bark Arf, large ones bark Woof, show the source

```dart
class Dog {
  String name;
  String breed;
  int weight;
  String dominantColor;

  void bark() {
    // small dogs weigh below 40
    // medium dogs weigh below 80
    // large ones are 80 and above
    // show the source of the bark sound (Max says:)
  }
}
```