### 1.Explain implicit blocks with an example.
#### Answer: 
* In Ruby, implicit blocks are blocks that are not explicitly defined using the do..end or curly braces {} syntax.
* Instead, they are implicitly passed to a method when the method expects a block.
*  Implicit blocks are commonly used with methods that yield control to the block within their implementation.
```
def custom_greeting
  puts "Starting the custom greeting method."
  yield
  puts "Custom greeting method is finished."
end

custom_greeting do
  puts "I am the block, and I'm being executed inside the custom greeting method."
end
```
### 2.Write a code where a proc is passed as an argument to the method.
#### Answer:
```
def calculate_result(a, b, operation)
  result = operation.call(a, b)
  puts "Result: #{result}"
end

subtraction = Proc.new { |x, y| x - y }

division = Proc.new { |x, y| x / y }

calculate_result(10, 4, subtraction)

calculate_result(20, 5, division)
```
### 3.Differentiate between blocks, procs, and lambdas.
#### Answer:
* Blocks: Blocks are not objects but are chunks of code associated with method calls using do..end or curly braces {}.They are used implicitly with methods like iterators and are not reusable or storable on their own. Blocks have loose argument checking and can accept any number of arguments.
* Procs: Procs are objects that represent blocks of code and can be stored in variables. They are created using the Proc.new method or the proc method, and they use the do..end or curly braces syntax. Procs have loose argument checking similar to blocks and can accept any number of arguments.
* Lambdas:Lambdas are also objects representing blocks of code, created using the lambda keyword or the -> (stabby lambda) syntax. Like Procs, they can be stored, passed as arguments, or returned from methods.Lambdas, however, have strict argument checking, and if the wrong number of arguments is passed, an error is raised.
  
### 4.WAP to check if a string is palindrome.
#### Answer:
```
def palindrome(str)
  str == str.reverse
end

# Example :
input_string = "madam"
if palindrome(input_string)
  puts "#{input_string} is a palindrome."
else
  puts "#{input_string} is not a palindrome."
end
```
### 5.WAP to print the sum of maximum and minimum element in an array
#### Answer:
```
def sum_max_and_min(arr)
  max = arr.max
  min = arr.min
  sum = max + min
  puts "Sum of maximum element (#{max}) and minimum (#{min}) element is: #{sum}"
end

# Example :
input_array = [12, 15, 9, 4, 30, 3, 7]
sum_max_and_min(input_array)
```
