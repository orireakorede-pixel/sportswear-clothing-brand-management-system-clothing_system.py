# sportswear-clothing-brand-management-system-clothing_system.py
SOFTWARE DEVELOPMENT LIFE CYCLE (SDLC) FOR SHOPPING CART SYSTEM

Project Title

Simple Shopping Cart Management System (Python Console Application)

⸻

1. Planning Phase

Problem Identification

Customers or users need a simple way to:
	•	Add items to a cart
	•	View items in the cart
	•	See the total cost
	•	Exit the system when done

Objectives
	•	Create a simple shopping cart program
	•	Allow users to add items with prices
	•	Display cart contents and total cost
	•	Run continuously until the user exits

Scope
	•	Console-based application
	•	No database or GUI
	•	Temporary storage using a list

Tools & Technology
	•	Programming Language: Python
	•	Platform: Console / Terminal

⸻

2. Requirements Analysis Phase

Functional Requirements

The system should be able to:
	1.	Accept item name from the user
	2.	Accept item price from the user
	3.	Store items in a cart
	4.	Display all items in the cart
	5.	Calculate total cost of items
	6.	Allow user to exit the program

Non-Functional Requirements
	•	Easy to use
	•	Fast response time
	•	Error-free execution
	•	Simple and readable code

⸻

3. System Design Phase

System Architecture
	•	Single Python file
	•	Uses functions for modularity
	•	Uses a list (cart) to store items

Data Design

Each item is stored as a dictionary:
{"item": item_name, "price": item_price}
{"item": item_name, "price": item_price}
Program Flow
	1.	Display menu
	2.	User selects an option
	3.	System performs selected action
	4.	Loop continues until exit

Flowchart (Text Description)
	•	Start
	•	Display menu
	•	User chooses option
	•	Add item / View cart / Exit
	•	Repeat until exit

⸻

4. Implementation Phase

Code Implementation
cart = []

def add_item():
    item = input("Enter item name: ")
    price = float(input("Enter item price: "))
    cart.append({"item": item, "price": price})
    print("Item added to cart")

def view_cart():
    if not cart:
        print("Cart is empty")
    else:
        total = 0
        for item in cart:
            print(item["item"], "- Price:", item["price"])
            total += item["price"]
        print("Total cost:", total)

def main():
    while True:
        print("1. Add Item")
        print("2. View Cart")
        print("3. Exit")

        choice = input("Choose option: ")

        if choice == "1":
            add_item()
        elif choice == "2":
            view_cart()
        elif choice == "3":
            break
        else:
            print("Invalid option")

main()
Explanation
	•	cart: Stores shopping items
	•	add_item(): Adds items to cart
	•	view_cart(): Displays items and total cost
	•	main(): Controls program flow
6. Deployment Phase
	•	Program is run directly from terminal or command prompt
	•	No external installation required
	•	Executed using:
  python cart.py
 7. Maintenance Phase

Possible Improvements
	•	Add item quantity
	•	Remove items from cart
	•	Save cart to a file or database
	•	Add a graphical interface (GUI)
	•	Add user authentication

