class Enemy:
    life = 3

#self means use something from this class.
    def attack(self):
        print("ouch!")
        self.life -= 1

    def check_life(self):
        if self.life <= 0:
            print("I am dead")
        else:
            print(str(self.life) + " life left")

enemy1 = Enemy()
enemy2 = Enemy()


enemy1.attack()
enemy1.attack()
enemy1.check_life()
enemy2.check_life()

"""enemy1 will have 1 life left.  enemy2 will have 3 lives left.  Because the enemy objects
are represented under the same class but they are independent of each other"""

class Tuna:

    def __init__(self):
        print("blrrbblrbb")

    def swim(self):
        print("i am swimming")

flipper = Tuna()
flipper.swim()
"""we call the swim function but it calls the init function first because the init function 
always gets called first"""

class Enemy2:
    def __init__(self, x):
        self.energy = x

    def get_energy(self):
        print(self.energy)

jason = Enemy2(5)
sandy = Enemy2(18)

jason.get_energy()
sandy.get_energy() 

"""in the init function we declared a second parameter in which x = energy. 
This function gets run first and then the code runs our get energy function"""

#class vs instance variable
#in this case gender is the class variable.  name is the instance variable

class Girl:
    gender = "female"

    def __init__(self, name):
        self.name = name

r=Girl("rachel")
s=Girl("liz")
print(r.gender)
print(s.gender)
print(r.name)
print(s.name)

"""inheritance is when a class inherits the functions from another class by passing 
in that class name as a parameter."""

class Parent():

    def print_last_name(self):
        print("Barry")

class Child(Parent):

    def print_first_name(self):
        print("Luke")
        
""" def print_last_name(self):  We could override the inherited function if we want
        print("Jackson")"""
        
luke = Child()
luke.print_first_name()
luke.print_last_name()


""" this deals with security and revealing what can be seen
import _sre
_sre.SRE_Pattern
import re
re.compile()
"""


