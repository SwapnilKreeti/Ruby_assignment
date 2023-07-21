### Q1> Given an array [1,2,3,2,5,6,9,6,5,3,2,2,1,8,10,10,7]. Create a hash and store the frequency of the array element.
#### Answer:
```
arr = [1, 2, 3, 2, 5, 6, 9, 6, 5, 3, 2, 2, 1, 8, 10, 10, 7]

frequency_count = Hash.new(0)

arr.each do |element|
  frequency_count[element] += 1
end

puts frequency_count
```
### Q2> Write a program to print sum of numbers from 100 to 200.
#### Answer:
```
start_num = 100
end_num = 200
total_sum = 0

(start_num..end_num).each do |num|
  total_sum += num
end

puts "Sum is: #{total_sum}"
```
### Q3> Write an exception for dividing by zero in Ruby.
#### Answer:
```
def safe_divide(x, y)
  begin
    result = x / y
    puts "Result of division: #{result}"
  rescue ZeroDivisionError => e
    puts "Error: #{e.message}. Division by zero is not possible."
  end
end

# Example ;
safe_divide(20, 2)  
safe_divide(20, 0)    
```
### Q4 > Write a program to find and replace all occurrences of a character in a string.
#### Answer:
```
def replace_character(original_string, target_char, replacement_char)
  new_string = original_string.gsub(target_char, replacement_char)
  puts "Original string: #{original_string}"
  puts "Modified string: #{new_string}"
end

# Example 
replace_character("Swapnil Das!", "a", "z")
```

