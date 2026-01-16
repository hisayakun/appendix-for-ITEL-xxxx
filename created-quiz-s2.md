# Problem Statement
Based on data about the quantity of materials and how much quantity is used per day, what kind of program should be created to put fruits that fall below a certain quantity at the end of the day into a shopping list? Also add a function to automatically replenish when a certain quantity is reached.

# Answer
```
# Dictionary holding inventory count for each fruit
kudamono_dict = {"apple": 10, "banana": 5, "cherry": 7}

# hopping list
kaimono_list = []

# max stock
MAX_STOCK = 20

# Function to check inventory and add to shopping list if
def check_stock():
    for kudamono, stock in kudamono_dict.items():
        if stock <= 5:
            print(kudamono + "is becoming scarce")
            kaimono_list.append(kudamono)

# functions using fruit
def use_kudamono(kudamono, amount):
    if kudamono in kudamono_dict:
        kudamono_dict[kudamono] -= amount
        if kudamono_dict[kudamono] <= 5:
            print(kudamono + "is becoming scarce")
            kaimono_list.append(kudamono)
            # automatic stock replenishment
            kudamono_dict[kudamono] = MAX_STOCK
            print(kudamono + "stock replenished")

# function to add new fruit
def add_kudamono():
    new_kudamono = input("Please enter the name of the fruit to be added: ")
    new_stock = int(input("Please enter the quantity of fruit to be added.: "))
    kudamono_dict[new_kudamono] = new_stock
```
