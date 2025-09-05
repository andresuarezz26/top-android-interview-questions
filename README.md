# Android Interview Question for your next interview

Recopilatory of theorical Android interview questions, answers, youtube videos, post and github repos related capturing the concepts of every Android Dev must know for an interview. 

This information comes from real Android interview questions and information of interviews published in the web. 


## Summary

1. Android Fundamentals
2. Java basics 
3. Kotlin basics
4. Data Structures 
5. OOP principles
6. Design Patters
7. Coroutines
8. Jetpack Compose
9. Networking protocols
10. Android Security 
11. Sensors


### 1. Android Fundamentals

**1. What is Context?**

The Android Context serves as the interface between your application components and the Android system. It provides:

System Identity and Communication: Context establishes your application’s identity for all system interactions
Resource Access: Context enables access to resources, assets, files, and preferences
Component Navigation: Context facilitates starting activities, services, and broadcasts
System Service Access: Context provides the gateway to all system services
Permission Verification: Context enables permission checking and enforcement

Every major Android component (Activity, Service, BroadcastReceiver, ContentProvider) receives its own Context instance, customized for that component’s specific needs and lifecycle.

Source: [Android Context](https://proandroiddev.com/android-context-part-2-the-android-internals-deep-dive-8a401985579c)

- What are the Android components?

Activity, Service, BraodcastReceiver, ContentProvider. 

Activity lyfecycle? 

How to communicate fragments? What are the restrictions of each approach? 

Difference between intent and pending intents?

**2. Serializable vs Parcelable**

Parcelable is from Android, Serializable is from Java Kotlin. 
Parcelable does not use reflection, Serializable does use it. 

3. What are handler in android? help in sending messages or runnables from a background thread to‬ the main (UI) thread.‬

## 2. Kotlin basics

- What are Any, Unit and Nothing types in Kotlin?
Any: Every single class in Kotlin inherits from Any. Equivalent to ´java.lang.Object´ in Java.
Unit: a function completes successfully but doesn't return any meaningful value. It's the equivalent of ´void´ in Java.
Nothing: indicates a piece of code can never be successfully completed
Example:

The source code of TODO function uses Nothing

```kotlin
@kotlin.internal.InlineOnly
public inline fun TODO(): Nothing = throw NotImplementedError()
```
- Difference between lateinit and lazy?  lateinit is used with var variables to initialize the object later. Lazy is used with constants to initialize the variables on the first access.
- 
- What is inline, crossline, no-inline?

- How to make the generated equals methods of a data classs only takes some arguments instead of all?

- What are descrutturing declarations?


- What is a‬‭ data class‬‭ in Kotlin?‬
  A‬‭ data class‬‭ is a special class made specifically‬‭ for storing data. It‬ automatically gives you useful methods like:‬
   1. toString()‬‭ – so you can print the object easily‬
   2. equals()‬‭ and‬‭ hashCode()‬‭ – to compare objects or use in HashMap/Set‬
   3. copy()‬‭ – to create a new object with some properties‬‭ changed‬
   4. ‭ componentN()‬‭ – to access values using destructuring‬‭ (like‬‭ val (a, b) = obj‬‭ )‬

‭ Syntax:‬
```kotlin
‭ data‬‭ class‬‭ User‬‭ (‬‭val‬‭ name: String,‬‭ val‬‭ age: Int)‬
```
‭[Android Developer Handook by Anand Gaur]

- What are `inline` Functions in Kotlin?‬
  ‭ An‬‭ inline function‬‭ in Kotlin is a function where the‬‭ compiler copies the function‬ body directly to the places where it's called‬‭ , instead‬‭ of calling the function in the‬
‭ traditional way. This can‬‭ improve performance‬‭ , especially when‬‭ using higher-order‬ functions‬‭ (functions that take other functions as‬‭ parameters).‬
‭ Why Use Inline Functions?‬

‭ Normally, passing a function (lambda) creates an‬‭ object‬‭ and adds some‬‭ runtime‬ overhead‬‭ . Using‬‭ inline‬‭ tells the compiler to‬‭ avoid‬‭ creating the function object‬‭ and‬ instead‬‭ insert the lambda code directly‬‭ — making it‬‭ faster‬‭ and‬‭ more efficient‬‭ .‬
‭
‭‭[Android Developer Handook by Anand Gaur]
‭


- ‬ What is‬‭ `noinline`‬‭ in Kotlin?‬
‭ In Kotlin, the‬‭ noinline‬‭ keyword is used inside an‬‭ inline‬‭ function to prevent‬ specific lambda parameters from being inlined.‬


‭ When you mark a function as‬‭ inline‬‭ , all lambdas passed to it are normally inlined‬ (code is copied). But sometimes, you don’t want to inline certain lambdas. 
 For‬ example, if you need to:‬
● Store the lambda in a variable‬
● Pass it to another function‬
● Return it from the function

- ‬What is the use of the‬‭ `reified`‬‭ modifier in Kotlin?‬
‭ In Kotlin, the‬‭ reified‬‭ modifier is used with type parameters inside inline functions to‬
‭ make the actual type available at runtime. Normally, type information is erased at‬
‭ runtime (called type erasure), but‬‭ reified‬‭ helps retain‬‭ it for certain cases like‬
‭ reflection or type checks.‬
‭ Key Benefits‬
‭ Created by Anand Gaur
‬
‭ Type Checks:‬‭ You can use‬‭ is‬‭ ,‬‭ as‬‭ , and‬‭ ::class‬‭ with‬‭ generic types.‬
‭ Reflection:‬‭ Get class metadata like‬‭ T::class.java‬‭ ,‬‭ T::class.simpleName‬‭ , etc.‬
‭ Clean Code:‬‭ Avoids boilerplate and workarounds for‬‭ passing‬‭ Class<T>‬‭ manually.‬
‭
‭
‭
‭
‭
‭
‭
‭

## 4. Data Structures

   
## 6. Design Patterns

This github repository show all design patterns with an example implementation. You must study the 3 main types of Design Patterns (Creational, Behavoral and structural) and understand some of them. The trick to differentiate every time and remember it,  is with learning main concept of every type and an example of how it is used in Android, i.e:
Bahavoural, main concept is Communcation. The `Observer/Listeners` to communicate between different components i.e ViewModel and Activity. 
Creational, main concet is Creation.  Viewmodels are created using a `Factory` method where you receive the class name and the `viewModelFactory`returns the ViewModel instance.
Structural, main concept is Relationship. Recycler view uses `Adapter` design pattern to relationship each 

 Check all design patterns here: [Design Patterns in Kotlin](https://github.com/dbacinski/Design-Patterns-In-Kotlin)

## 7. Coroutines

- What is a scope? 

- When you run the cancel method of a job, does the job is cancelled inmediatly?

- What are dispatchers? Whare are the different types of dispatchers? 
These tell the coroutine which thread or thread pool to run on.
   1. Dispatchers.Main: For tasks that update the UI (Main thread).
   2. Dispatchers.IO: For network or disk operations (I/O).
   3. Dispatchers.Default: For CPU-intensive work, like sorting a large list.

 ## 8. Jetpack compose

 - What is the difference between jetpack compose and view system?
   Jetpack compose is declarative meaning you don't have to manually handle the state of the elements, view system is imperative, meaning you have to worry about updating the state manually.
 - Explain mutableStateOf: used to manage state, when the state change a recomposition is triggered
 - Explain remember: used to store the variables state across multiple recompositions
 - What is the lyfecycle of a compose function? composition -> layour -> drawing
   
 - Side Effects: is an action that "scapes" the scope of a composable function.
   Examples:
   1. LaunchedEffect: run a suspend function in the scope of a composable
   2. SideEffect: run after every recomposition
   3. DisposableEffect: when need to perform clean ups. 
   
   

 ## 8. Networking protocols

 - What are the http objects you know
 - What are web sockets, http, rpc

## 9. App security

- Symmetric vs asymmetric encription? Symmetric is one key for everything. Assymetric uses public and private keys. 
- 



## 10. Sensors

- What is the difference between bluethoot 
