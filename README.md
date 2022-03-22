Comparison:

Learn about operator overloading and how the different conventions for operations like ==, <, + work in Kotlin. Add the function compareTo to the class MyDate to make it comparable. After this, the code below date1 < date2 should start to compile.

Note that when you override a member in Kotlin, the override modifier is mandatory.
___________________________________________________________________________________________________________________________________________________________________

Ranges:

Using ranges implement a function that checks whether the date is in the range between the first date and the last date (inclusive).
You can build a range of any comparable elements. In Kotlin in checks are translated to the corresponding contains calls and .. to rangeTo calls:

val list = listOf("a", "b")
"a" in list  // list.contains("a")
"a" !in list // !list.contains("a")
date1..date2 // date1.rangeTo(date2)
___________________________________________________________________________________________________________________________________________________________________

For loop:

A Kotlin for loop can iterate through any object if the corresponding iterator member or extension function is available.
Make the class DateRange implement Iterable<MyDate>, so that it can be iterated over. Use the function MyDate.followingDate() defined in DateUtil.kt; you don't have to implement the logic for finding the following date on your own.
Use an object expression which plays the same role in Kotlin as an anonymous class in Java.
___________________________________________________________________________________________________________________________________________________________________

  Operators overloading:
  
Implement date arithmetic and support adding years, weeks, and days to a date. You could write the code like this: date + YEAR * 2 + WEEK * 3 + DAY * 15.
First, add the extension function plus() to MyDate, taking the TimeInterval as an argument. Use the utility function MyDate.addTimeIntervals() declared in DateUtil.kt
Then, try to support adding several time intervals to a date. You may need an extra class.
___________________________________________________________________________________________________________________________________________________________________

  Invoke:
  
Objects with the invoke() method can be invoked as a function.
You can add an invoke extension for any class, but it's better not to overuse it:

  operator fun Int.invoke() { println(this) }
1() //huh?..
Implement the function Invokable.invoke() to count the number of times it is invoked.
