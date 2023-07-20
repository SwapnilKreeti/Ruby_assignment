### 1. Create a Circle class and initialize it with radius. Make two methods getArea and getCircumference inside this class.
#### Answer:
```
class Circle
  def initialize(radius)
    @radius = radius
  end

  def getArea
    Math::PI * @radius**2
  end

  def getCircumference
    2 * Math::PI * @radius
  end
end
# Example :
radius = 4
circle = Circle.new(radius)

puts "Radius: #{radius}"
puts "Area: #{circle.getArea}"
puts "Circumference: #{circle.getCircumference}"
```
### 2. Take float number in a variable and convert into a string with up to 2 places in decimal with a dollar sign prefixed.Example: f=9.312482 to s=”$9.31”
#### Answer:
```
f = 9.312482
s = sprintf("$%.2f", f)
puts s
```
### 3. Create a Temperature class. Make two methods :
### 3.1. convertFahrenheit - It will take celsius and will print it into Fahrenheit.
### 3.2. convertCelsius - It will take Fahrenheit and will convert it into Celsius.
#### Answer:
```
class Temperature
  def convertFahrenheit(celsius)
    fahrenheit = (celsius * 9/5) + 32
    puts "#{celsius} Celsius is equal to #{fahrenheit} Fahrenheit."
  end

  def convertCelsius(fahrenheit)
    celsius = (fahrenheit - 32) * 5/9
    puts "#{fahrenheit} Fahrenheit is equal to #{celsius} Celsius."
  end
end
# Example :
temperature = Temperature.new
temperature.convertFahrenheit(100) 
temperature.convertCelsius(98)   
```
