# Android Interview Question for your next interview

Recopilatory of theorical Android interview questions, answers, youtube videos, post and github repos related capturing the concepts of every Android Dev must know for an interview.


## Summary

1. Android Fundamentals
2. Java basics 
3. Kotlin basics
4. Data Structures 
5. OOP principles
6. Design Patters
7. Coroutines


### Android Fundamentals

- What is Context?

The Android Context serves as the interface between your application components and the Android system. It provides:

System Identity and Communication: Context establishes your application’s identity for all system interactions
Resource Access: Context enables access to resources, assets, files, and preferences
Component Navigation: Context facilitates starting activities, services, and broadcasts
System Service Access: Context provides the gateway to all system services
Permission Verification: Context enables permission checking and enforcement

Every major Android component (Activity, Service, BroadcastReceiver, ContentProvider) receives its own Context instance, customized for that component’s specific needs and lifecycle.

[https://proandroiddev.com/android-context-part-2-the-android-internals-deep-dive-8a401985579c]

- What are the Android components?

Activity, Service, BraodcastReceiver, ContentProvider. 

Activity lyfecycle? 


Serializable vs Parcelable

Parcelable is from Android, Serializable is from Java Kotlin. 
Parcelable does not use reflection, Serializable does use it. 

### Design Patterns

This github repository show all design patterns with an example implementation. You must study the 3 main types of Design Patterns (Creational, Behavoral and structural) and understand some of them. The trick to differentiate and remember is with learning main concept of every type, i.e:
Bahavoural = Communcation, do you remember how you use Observer/Listeners to communicate between different components?
Creational = Create, do you remember how viewmodels are created, using a Factory method 
Structural = Relationship, do you remember how does the Adapter works in a recycler view? 

[https://github.com/dbacinski/Design-Patterns-In-Kotlin]
