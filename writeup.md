# Writeup Lab 1
### By Andrew Casner and Sean
1. **Feedback**  
Completed
1. **Scala Basics: Binding and Scope**
   1. Consider the following Scala code.  
   ```Scala
   val pi = 3.14
   def circumference(r: Double): Double = {
     val pi = 3.14159
     2.0 * pi * r
   }
   def area(r: Double): Double =
     pi * r * r
   ```
   The use of `pi` at line 4 is bound at line 3. The use of `pi` at line 7 is bound at line 1. 
   1. Consider the following Scala code.  
   ```Scala
   val x = 3
   def f(x:Int): Int =
     x match {
       case 0 => 0
       case x => {
         val y = x + 1
         ({
           val x = y + 1
           y
         } * f(x - 1))
       }
     }
   val y = x + f(x)
   ```
   The use of `x` at line 3 is bound at line 2. The use of `x` at line 6 is bound at line 5. The use of `x` at line 10 is bound at line 2. The use of `x` at line 13 is bound at line 1.
1. **Scala Basics: Typing**  
   1. Is the Body of `g` well typed?  
   ```Scala
   def g(x: Int) = {
     val (a, b) = (1, (x, 3))
     if (x == 0) (b, 1) else (b, a + 2)
   }
   ```
   Yes. The code returns a constant type of a tuple of int's
1. **Run-Time Library**  
Completed
1. **Run-Time Library: Recursion**  
Completed
1. **Data Structures Review: Binary Search Trees**  
Completed
1. **JavaScripty Interpreter: Numbers**  
Completed
