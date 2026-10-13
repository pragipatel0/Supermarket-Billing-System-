# 🛒 Supermarket Billing System

A console-based **Supermarket Billing System developed in C++** using Object-Oriented Programming (OOP). This project helps manage supermarket products, maintain stock, generate bills, calculate discounts, process payments, and store product records using file handling.

## 📌 About the Project

The Supermarket Billing System is a menu-driven C++ application developed as part of a C++ Guided Project. It provides a simple way to manage product inventory and perform customer checkout.

The application uses classes and objects to organize the code, dynamic memory allocation to manage the product list, and file handling to save and load product records.

## ✨ Features

- **Add Products:** Add products with a name, price, and stock quantity.
- **Display Products:** View product IDs, names, prices, and available stock.
- **Search Products:** Find a product using its ID.
- **Update Products:** Modify product details, price, and stock.
- **Delete Products:** Remove products from the inventory.
- **Shopping Cart:** Select products and quantities for checkout.
- **Stock Validation:** Reject invalid product selections and insufficient stock.
- **Automatic Billing:** Calculate the subtotal, discount, and final amount.
- **Discount System:** Apply a 5% discount on bills of ₹1,000 or more.
- **Payment Processing:** Accept cash or UPI as payment modes and validate the amount received.
- **File Handling:** Save and load product records between program sessions.
- **Input Validation:** Handle invalid menu choices, negative prices, and invalid stock values.

## 🛠️ Technologies Used

- **Language:** C++
- **C++ Standard:** C++17
- **Compiler:** GCC (g++)
- **Concepts:** Object-Oriented Programming, dynamic memory allocation, file handling, exception handling, and runtime polymorphism
- **Storage:** Text file

## 🧠 OOP Concepts Used

| Concept | Description |
|---|---|
| Classes and Objects | Product, Customer, Cart, Bill, Payment, FileManager, and SupermarketSystem |
| Encapsulation | Product information is managed through class member functions |
| Inheritance and Polymorphism | Virtual functions support extensible class behavior |
| Constructors and Destructors | Initialize objects and manage cleanup |
| Dynamic Memory Allocation | Manage the product array using `new[]` and `delete[]` |
| File Handling | Read and write product records using `ifstream` and `ofstream` |
| Exception Handling | Handle errors using `try`, `catch`, and exceptions |

## 📂 Project Structure

```text
Supermarket-Billing-System/
├── main.cpp
├── Data/
│   └── products.txt
└── README.md
```

This is the intended project layout. The current source code uses the relative path `../Data/products.txt`, so check the data-file path before using this exact folder structure. See the setup instructions below.

## ⚙️ Requirements

Before running the project, install:

- A C++ compiler that supports C++17, such as GCC.
- Visual Studio Code, Code::Blocks, or another code editor.
- A terminal or command prompt.

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Open the downloaded project folder in your terminal.

### 2. Compile the Program

Run the following command in the directory containing `main.cpp`:

```bash
g++ -std=c++17 -Wall -Wextra main.cpp -o SupermarketBillingSystem.exe
```

### 3. Run the Program

In Windows PowerShell, execute:

```powershell
.\SupermarketBillingSystem.exe
```

The application displays a menu with the following options:

```text
--- SUPERMARKET BILLING SYSTEM ---
1. Add Record
2. Display Records
3. Search Record
4. Update Record
5. Delete Record
6. Checkout and Payment
7. Save
8. Exit
```

Enter the number of the operation you want to perform and follow the prompts.

## 🧾 Billing Calculation

The program calculates the bill using the following rules:

- The subtotal is calculated from the selected products and quantities.
- A 5% discount is applied when the subtotal is at least ₹1,000.
- The final bill is calculated by subtracting the discount from the subtotal.
- Payment is accepted when the amount received is greater than or equal to the final bill.

**Formula:**

```text
Discount = Subtotal × 5 / 100   (if subtotal >= ₹1,000)

Final Amount = Subtotal - Discount
```

## 💾 File Handling

Product records are stored in a text file using this format:

```text
productId|name|price|stock
```

Example:

```text
1|Rice 5kg|350.000000|20
```

The `FileManager` class provides functions to save and load product records. The application loads existing records when it starts and saves them when the user selects the Save option or exits.

**Setup note:** The current code opens `../Data/products.txt` relative to the program's working directory. Ensure that the parent-level `Data` directory exists, or change the path in `main.cpp` to `Data/products.txt` if you want the data directory inside the repository root.

## 🧪 Testing

According to the project report, all **15 planned test cases passed**.

The tests cover:

- Adding and displaying products.
- Searching for existing and unknown products.
- Updating and deleting products.
- Rejecting invalid prices.
- Checking stock availability.
- Checkout with one or multiple products.
- Stock reduction.
- Discount calculation.
- Successful and insufficient payments.
- Loading saved product data after restarting the application.

## ⚠️ Limitations

- The application uses a console interface rather than a graphical interface.
- Product records are stored in a text file instead of a database.
- The current workflow uses a walk-in customer.
- Invoice history and supplier management are not implemented.

## 🔮 Future Improvements

- Add a graphical user interface.
- Integrate SQLite or MySQL for data storage.
- Add customer accounts and sales-history reports.
- Implement cashier login and access control.
- Add GST settings and invoice generation.
- Export receipts as PDF files.
- Add barcode scanning and cart quantity editing.

## 🎯 Learning Outcomes

This project demonstrates the practical use of C++ classes, objects, inheritance, virtual functions, dynamic memory allocation, file handling, exception handling, input validation, and basic billing operations.

## 👨‍💻 Project Information

- **Project:** Supermarket Billing System
- **Subject:** C++ Guided Project
- **Semester:** 3
- **Language:** C++
- **Compiler Standard:** C++17

---

⭐ If you find this project useful, consider giving the repository a star!
