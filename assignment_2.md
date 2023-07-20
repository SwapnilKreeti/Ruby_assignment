### Q1. Write a program to print first n odd numbers where n can be from 1 to 100.
#### Answer:
```
def print_odd_numbers(count)
  if count < 1 || count > 100
    puts "Input must be between 1 and 1000"
    return
  end

  odd_count = 0
  number = 1

  while odd_count < count
    if number.odd?
      puts number
      odd_count += 1
    end
    number += 1
  end
end

# Example :
n = 10
print_odd_numbers(n)
```
### Q2. Given an array of integers where elements can be from 1-7. every element maps to the day of the week.Write a program to print it like
### 1-monday, 2-tuesday, 3-wednesday
### arr = [1, 5 , 7, 4, 2, 6, 1, 4, 2, 7];
### Output: 1-monday, 5-friday, 7-sunday ...
#### Answer:
```
def print_days(arr)
  days_map = {
    1 => "Monday",
    2 => "Tuesday",
    3 => "Wednesday",
    4 => "Thursday",
    5 => "Friday",
    6 => "Saturday",
    7 => "Sunday"
  }

  result = arr.map { |num| "#{num}-#{days_map[num]}" }.join(", ")

  puts "Output: #{result}"
end

# Example :
arr = [1, 5, 7, 4, 2, 6, 1, 4, 2, 7]
print_days(arr)
```
### Q3. Given an array of integers, sort the array using bubble,insertion or selection sort algorithm [any one]
### arr = [12, 15, 9, 4, 30, 3, 7];
#### Answer:
