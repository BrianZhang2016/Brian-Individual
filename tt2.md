{% include navigation.html %}

# Week 2: TT2

# Tech Talks

{% include tt.html %}

### Menu Sorted

````
main_menu = [
]

# Submenu list of [Prompt, Action]
# Works similarly to main_menu
week0_list = [
    ["Swap", "week0/Swap.py"],
    ["Matrix", "week0/Matrix.py"], 
    ["Tree", "week0/Tree.py"],
    ["Animation", Animation.ship],
]

week1_list = [

  ["InfoDb Loops", infoDb.InfoDb_loops],
  ["Factorial", infoDb.factorial],
  ["Fibonacci", infoDb.output_fibonacci]
]

week2_list = [
    ["Factorial OOP", factorial.OOP],
    ["Addition", "week2/addition.py"], 
    ["Palindrome", "week2/palindrome.py"],
]

# Menu banner is typically defined by menu owner
border = "=" * 25
banner = f"\n{border}\nPlease Select An Option\n{border}"


# def menu
# using main_menu list:
# 1. main menu and submenu reference are created [Prompts, Actions]
# 2. menu_list is sent as parameter to menuy.menu function that has logic for menu control
def menu():
  print()
  title = "Function Menu" + banner
  menu_list = main_menu.copy()
  menu_list.append(["Design", week0_func])
  menu_list.append(["Lists", week1_func])
  menu_list.append(["Math", week2_func])
  buildMenu(title, menu_list)

# def submenu
# using sub menu list above:
# sub_menu works similarly to menu()

def week0_func():
  title = "Week 0" + banner
  buildMenu(title, week0_list)
  
def week1_func():
  title = "Week 1" + banner
  buildMenu(title, week1_list)

def week2_func():
  title = "Week 2" + banner
  buildMenu(title, week2_list)
````
  
### Factorial OOP
 
````
  class Factorial: 
  def __init__(self):
    self.factSeq = [0, 1]
    
  def __call__(self, n):
    if n < len(self.factSeq):
      return self.factSeq[n]
    else:
      num = n * self(n-1)
      return num

def OOP():
  num_input = int(input("Enter a number for factorial: "))
  factorial_of = Factorial()
  if num_input < 0:
      print("Sorry, factorial does not exist for negative numbers.")
  else:
      print("The factorial of", num_input, "is", factorial_of(num_input))
````
  
### Math Function

````
  class Add:

    def findsum(self, a, b):
        s = a + b
        return s

a = int(input("Enter first number:"))
b = int(input("Enter second number:"))

obj = Add()
s = obj.findsum(a, b)

print("Sum is:", s)
````
  
### Palindrome 

````
  class palindrome:
    def palindrome(self, string):
        if string == string[::-1]:
            return "is a palindrome"
        else:
            return "is not a palindrome"

n = 1

while n == 1:
    string = input("Type a word: ")

    obj = palindrome()
    f = obj.palindrome(string)

    print(string, f)
    n = int(input("Press 1 to Try Again!  "))
````
  
