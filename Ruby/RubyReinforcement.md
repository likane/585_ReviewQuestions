Ruby Reinforcement Practice


1. Who created Ruby and in what year?
Yukihiro Matsumoto 'Matz' 1995

2. What is the url of the Ruby Language Home Page?
https://www.ruby-lang.org/en/

3. What is the current version of Ruby?
2.7.1

4. What is the Ruby interactive interpreter called?
    irb

5. Ruby doesn’t use curly braces for defining methods. What does it use instead?
    'do' - 'end'

6. How do you write a line of text to standard output?
puts "Hello, world"

7. How do you access the third command line argument of a script, run on the command line?
n = ARGV[2]

8. How do you iterate through the lines of standard input?
n = ARGV[0].to_i;

a, b = 0, 1
while b <= n
  print "#{b} "
end

9. How do you write the (conditional) expression that evaluates to y if x is truthy and to z if x is falsy.
TODO

10. How do you get the type of a Ruby expression at runtime?
.class

11. Why does Ruby not have primitive and reference types, like Java and JavaScript do?
    Everything is an object, even nil. Numbers and booleans are symbols are objects. There are no weird “primitive values” like Java and JavaScript has. Even modules and classes are objects too. Every object has an object id

12. If everything in Ruby is an object, does that mean even integers and booleans get allocated on the heap? What allows them to not have to be heap-allocated?
    TODO

13. Does Ruby have distinct types for integers and floating point numbers?
no

14. Does Ruby have distinct types for small integers and unbounded integers? Did it in the past?
no /TODO

15. How can you tell whether string s is a substring of string t?
i = s
t[i]

16. How do you do string interpolation in Ruby?
>> x = 10
>> 'There are #{x} things here'
=> "There are \#{x} things here"
>> "There are #{x} things here"
=> "There are 10 things here"
>> %q{There are #{x} things here}
=> "There are \#{x} things here"
>> %Q{There are #{x} things here}
=> "There are 10 things here"

17. Why is 2 and 3 equal to 3, but 2 & 3 equal to 2?
TODO

18. Name all the falsy values in Ruby.
nil
boolean false

19. How do Ruby arrays respond to <, <=, >, and >=?
TODO

20. Does Ruby have a native set type?
Yes

21. How do you “declare” a local variable in Ruby?
def method1
    x = 10
    p x
end


22. The hash { x: 3 } has one key and one value. What is the key?
x

23. Does Ruby have an analog to JavaScript’s spread operator? If so, give an example of its use.
>> (1..10).class
=> Range

24. You might often see the expression a[:], for some list a. What does this expression do, exactly?
>> caps = {:ca => 'sacramento', :hi => 'honolulu', :wa => 'seattle'}
>> caps[:wa] = 'olympia'
>> caps
=> {:ca=>"sacramento", :hi=>"honolulu", :wa=>"olympia"}
creates a list of symbols

25. Explain why a[::-1] is the idiom for a reversed list.
TODO

26. How does one best create an array of size 100 in which every element is 0? (Do not write a loop.)

27. What is the difference between a+b, and [*a,*b] where a and b are arrays?
The + operator is equivalent to the concat method whereas the * is the splat. An array of elements of a are in the master array as element 1 as well as the elements of b in element 2 of the master array.

28. How do you write an expression that adds element e to array a so that a is mutated? How do you write a non-mutating append expression?

29. How do you add an element to the front of a list, in a mutating fashion? Is this efficient? If not, what should you do instead?

30. Write an IIFE that applies a lambda that squares its argument to the value 100.

What are the two main ways that lambda procs differ from non-lambda procs?

In the method definition def f(x, y); return [x, y]; end, what do we call x and y?

In the method call f(y, z), what do we call y and z?

Can positional arguments ever appear after named arguments? Why or why not?

Does Ruby allow assignments with array patterns on the left-hand side?

Does Ruby allow assignments with dictionary patterns on the left-hand side?

How do you force a function to take its arguments positionally?

How do you force a function to take all its arguments as named arguments?

How do you define a variable local to a block?

How do you define a variable local to a function?

Does Ruby have an analog of JavaScript’s temporal dead zone? If so, how does it work? If not, why is such a concept incoherent in Ruby?

Write a function that takes in a number and returns a function that adds that number to its argument. Is the function you wrote higher-order? Why or why not? Does that function illustrate a closure? Why or why not? Does that function illustrate currying? Why or why not?

What does Ruby call what almost every other language calls map and filter?

What is the first line of that block at the end of a module that allows you to “run” the module from the command line?

Instead of throw, Ruby uses **____**.

The things inside of a class are called **____**.
Instance Methods


How do you create an instance of a class?
>> class Integer
>>   def tripled; self * 3; end
>> end

What is the difference between a proc and a method?
Blocks can’t be assigned to variables, so Ruby has procs which can. There are two kinds of procs: those defined with Proc.new (don't use these), and a better kind of proc, called a lambda. You should always use lambdas, pretty much.

Suppose class Circle has a zero-argument method area and c is an instance of Circle. We know that c.area is actually a method call. How do we refer to the area method itself, without calling it?

What is the method initialize used for?
Instance fields have names beginning with @. The initialize method is called during the call to new on the class.

What is the Ruby analog for Python’s __str__ or JavaScript’s toString?
'.to_s'

What is the syntax for declaring a class that is a subtype of another class?

How do we define class methods in Ruby?

How do you allow the operators + and - to apply to instances of a class you write yourself?

What is the Ruby analog of JavaScript generators (the ones made with function*).
lambda's