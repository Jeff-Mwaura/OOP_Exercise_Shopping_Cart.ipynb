🛒 Shopping Cart - OOP Lab

📚 Objectives
By completing this lab, you will be able to:

Define and call instance methods

Define and access instance attributes

Call instance methods within other instance methods

Write methods that calculate statistics based on object data

Create a domain model using OOP principles

🛠️ Instructions
This project centers around modifying the shopping_cart.py file. Below are the steps and methods you'll implement.

🔄 Auto-reload for Development
To automatically reload your package in Jupyter Notebook when changes are made:

python
Copy
Edit
%load_ext autoreload
%autoreload 2
Then initialize a new instance of your ShoppingCart class:

python
Copy
Edit
from shopping_cart import ShoppingCart

cart = ShoppingCart()
📦 Class Features
1. __init__ Method
Update the ShoppingCart class to initialize with the following attributes:

total: defaults to 0

employee_discount: defaults to None

items: an empty list []

2. add_item(name, price, quantity=1)
Adds an item to the cart.

Increases the total based on the item's price and quantity

Stores item info in the items list (recommend storing each as a dictionary)

Returns: The updated total

3. mean_item_price()
Calculates the average price per item in the cart.

Divide the total cost by the number of items (considering quantities)

4. median_item_price()
Returns the median price of all items in the cart.

Flatten item quantities into a list of individual prices

Sort and compute the median (handle both even and odd item counts)

5. apply_discount()
Applies the employee_discount if available.

Reduces the total based on the discount percentage

If no discount exists, return:
"Sorry, there is no discount to apply to your cart :("

Returns: Discounted total or message

6. void_last_item()
Removes the last item added to the cart and updates the total.

If no items exist, return:
"There are no items in your cart!"

💡 Example Usage
python
Copy
Edit
cart = ShoppingCart(employee_discount=20)
cart.add_item("Banana", 1.00, 3)
cart.add_item("Apple", 2.00, 2)

print(cart.total)                  # ➜ 7.0
print(cart.mean_item_price())     # ➜ 1.4
print(cart.median_item_price())   # ➜ 1.0
print(cart.apply_discount())      # ➜ 5.6
cart.void_last_item()
print(cart.total)                 # ➜ 3.0
🧪 Testing
You can manually test your code using the provided sample in a Jupyter Notebook or write unit tests using Python’s unittest module.

📁 File Structure
bash
Copy
Edit
shopping_cart_oop_lab/
│
├── shopping_cart.py         # Your ShoppingCart class
├── test_shopping_cart.py    # (Optional) Unit tests
└── README.md                # You're here!
🚀 Summary
In this lab, you practiced:

Building and using class instance methods

Performing calculations based on instance attributes

Modeling real-world functionality using OOP

Feel free to extend this project by adding more features like:

Cart item removal by name

Saving/loading carts

Sales tax support

👩‍💻 Author
[Geoffrey Mwaura]

