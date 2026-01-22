# SPORTSWEAR CLOTHING BRAND MANAGEMENT SYSTEM  
# SEN 201 Assignment  
# Name: AJUMOBI MICHAEL OLUSEGUN  
# Matric Number: 24/14462  
  
# ======================================  
# Brand Module  
# ======================================  
brands = [  
    "Nike",  
    "Adidas",  
    "Puma",  
    "Under Armour",  
    "Reebok"  
]  
  
# ======================================  
# Product Module  
# ======================================  
products = [  
    {"brand": "Nike", "name": "Nike Air Max", "category": "Shoes", "price": 45000, "stock": 10},  
    {"brand": "Adidas", "name": "Adidas Ultraboost", "category": "Shoes", "price": 50000, "stock": 8},  
    {"brand": "Puma", "name": "Puma Sports Tee", "category": "T-Shirt", "price": 15000, "stock": 20},  
    {"brand": "Under Armour", "name": "UA Training Shorts", "category": "Shorts", "price": 18000, "stock": 15},  
    {"brand": "Reebok", "name": "Reebok Classic Hoodie", "category": "Hoodie", "price": 30000, "stock": 12}  
]  
  
# ======================================  
# Inventory Module  
# ======================================  
def display_brands():  
    print("\nAvailable Brands:")  
    for brand in brands:  
        print("-", brand)  
  
  
def display_products():  
    print("\nAvailable Products:")  
    for product in products:  
        print(  
            product["name"], "- ₦" + str(product["price"]),  
            "| Category:", product["category"],  
            "| Stock:", product["stock"]  
        )  
  
  
def search_by_brand():  
    brand_name = input("\nEnter brand name to search: ")  
    found = False  
  
    for product in products:  
        if product["brand"].lower() == brand_name.lower():  
            print(  
                product["name"], "- ₦" + str(product["price"]),  
                "| Category:", product["category"],  
                "| Stock:", product["stock"]  
            )  
            found = True  
  
    if not found:  
        print("No products found for this brand.")  
  
  
def check_stock():  
    product_name = input("\nEnter product name to check stock: ")  
    for product in products:  
        if product["name"].lower() == product_name.lower():  
            print("Stock available:", product["stock"])  
            return  
    print("Product not found.")  
  
  
# ======================================  
# Main System Module  
# ======================================  
def main_menu():  
    print("\nSPORTSWEAR CLOTHING BRAND MANAGEMENT SYSTEM")  
    print("1. View Available Brands")  
    print("2. View All Products")  
    print("3. Search Products by Brand")  
    print("4. Check Product Stock")  
    print("5. Exit")  
  
  
while True:  
    main_menu()  
    choice = input("\nEnter your choice (1-5): ")  
  
    if choice == "1":  
        display_brands()  
    elif choice == "2":  
        display_products()  
    elif choice == "3":  
        search_by_brand()  
    elif choice == "4":  
        check_stock()  
    elif choice == "5":  
        print("\nThank you for using the Sportswear Clothing Brand Management System.")  
        break  
    else:  
        print("Invalid choice. Please try again.")  
