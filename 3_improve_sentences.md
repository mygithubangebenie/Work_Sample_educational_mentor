Now We are going to understand well Self and we will see where it is used

# What is self?

You may have heard people say that everything in Ruby is an object. If that's true it means that every piece of code you write "belongs" to some object.

self is a special variable that points to the object that "owns" the currently executing code. Ruby uses self everwhere:

- For instance variables: @myvar
- For method and constant lookup
- When defining methods, classes and modules.
Examples of self
We're going to step through several examples now. If the first ones seem too basic for you, just keep reading. They get more advanced.

# Inside of an instance method
In the code below, reflect is an instance method. It belongs to the object we created via Ghost.new. So self points to that object.

class Ghost
  def reflect
    self
  end
end

g = Ghost.new
g.reflect == g # => true

# Inside of a class method
For this example, reflect is a class method of Ghost. With class methods, the class itself "owns" the method. self points to the class.

class Ghost
  def self.reflect
    self
  end
end

Ghost.reflect == Ghost # => true

You have learned about Ruby self keyword, exactly what it is, why it's useful & how to use it.
Now it's your turn to give it a try.




