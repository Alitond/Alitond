```python
class Product:
    def __init__(self, name, price, quantity):
        self.name = name
        self.price = price
        self.quantity = quantity

class Store:
    def __init__(self):
        self.products = []

    def add_product(self, product):
        self.products.append(product)

    def list_products(self):
        for idx, product in enumerate(self.products, start=1):
            print(f"{idx}. {product.name} - Price: ${product.price} - Quantity: {product.quantity}")

store = Store()

while True:
    print("1. Add Product")
    print("2. List Products")
    print("3. Exit")
    choice = input("Enter your choice: ")

    if choice == "1":
        name = input("Enter product name: ")
        price = float(input("Enter product price: "))
        quantity = int(input("Enter product quantity: "))
        new_product = Product(name, price, quantity)
        store.add_product(new_product)
        print("Product added successfully!")
    elif choice == "2":
        store.list_products()
    elif choice == "3":
        print("Goodbye!")
        break
    else:
        print("Invalid choice. Please select a valid option.")
```
