### 1. Write ruby regex to accept basic email addresses, that contain a letter (any case) as its 1st character, followed by any number of word characters, then an ‘@’ symbol, again followed by any number of word characters, then a ‘.’ and finally a maximum of 4 letter (minimum 1).
#### Answer:
```
def valid_email?(email_address)
  email_regex = /^[a-zA-Z]\w*@\w+\.[a-zA-Z]{1,4}$/
  email_address =~ email_regex
end

# Example usage
email1 = "swapnildasnits@gmail.com"  
email2 = "swapnildas@gmail" 
email3 = "a@b.c"                


puts valid_email?(email1) ? "#{email1} is valid." : "#{email1} is invalid."
puts valid_email?(email2) ? "#{email2} is valid." : "#{email2} is invalid."
puts valid_email?(email3) ? "#{email3} is valid." : "#{email3} is invalid."
```
### 2. Let’s consider a ruby class Vehicle with following definition:
```
class Vehicle
 def initialize
 puts “I am a vehicle”
 end
 def max_speed
 puts “10”
 end
end
```
#### Answer:
### a. Define 2 classes Car and Rickshaw which inherit the class Vehicle.
### b. Override method max_speed in both classes to output 100 and 25 for classes Car and Rickshaw respectively.
#### Answer:
```
class Vehicle
  def initialize
    puts "I am a vehicle"
  end

  def max_speed
    puts "10"
  end
end

class Car < Vehicle
  def initialize
    super
    puts "I am a car"
  end

  def max_speed
    puts "Car maximum speed is: 100"
  end
end

class Rickshaw < Vehicle
  def initialize
    super
    puts "I am a rickshaw"
  end

  def max_speed
    puts "Rickshaw maximum speed is: 25"
  end
end

car = Car.new
car.max_speed

rickshaw = Rickshaw.new
rickshaw.max_speed
```
### 3. Differentiate between Module and Mixins.
#### Answer:
* Modules:Modules are containers for storing methods, constants, and other module-level objects in Ruby.They are defined using the module keyword.Modules cannot be instantiated or create objects directly. They act as namespaces to organize code.Modules are used to achieve code organization, share behavior across classes, and serve as a namespace for methods that may have common names.
* Mixins:Mixins are a form of multiple inheritance in Ruby.Mixins are achieved by including a module in a class, effectively adding the module's methods to the class's behavior.They allow a class to inherit behavior from multiple sources, unlike traditional single inheritance.Mixins are used to add common functionality to classes without creating a full-fledged subclass hierarchy.
### 4. Differentiate between Private and Protected methods.
#### Answer:
* Private Methods:Private methods can only be called from within the class where they are defined and cannot be accessed from outside the class, even by its instances.They are primarily used for internal implementation details of a class and are not meant to be part of the public interface.Private methods are declared using the private keyword followed by the method names.Private methods can be called within the class, including other private methods, but they cannot be invoked using an explicit receiver.
* Protected Methods:Protected methods can be called by any instance of the same class or any of its subclasses (i.e., derived classes).They are used for methods that need to be accessible within the class hierarchy, allowing subclasses to access the behavior.Protected methods are declared using the protected keyword followed by the method names.
