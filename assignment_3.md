### 1.Explain implicit blocks with an example.
#### Answer:
### 2.Write a code where a proc is passed as an argument to the method.
#### Answer:
### 3.Differentiate between blocks, procs, and lambdas.
#### Answer:
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
