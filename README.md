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

- What is inline, crossline,

- Who to make the generated equals methods of a data classs only takes some arguments instead of all?


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

- 


 ## 8. Networking protocols

 - What are the http objects you know
 - What are web sockets, http, rpc

## 9. App security



## 10. Sensors

- What is the difference between bluethoot 
