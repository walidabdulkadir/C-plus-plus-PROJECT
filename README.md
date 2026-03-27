# C++ PROJECT
# 🏦 Bank Management System

![C++](https://img.shields.io/badge/C%2B%2B-17-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Linux%20%7C%20Windows%20%7C%20macOS-informational?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)

A simple, terminal-based **Bank Management System** written in C++ that allows users to create accounts, log in, deposit/withdraw funds, transfer money, and view transaction history — all stored via local text files.

---

##  Preview

```
===== BANK SYSTEM =====
1. Create account
2. Login
3. Deposit
4. Withdraw
5. Transfer
6. Show balance
7. Transaction history
8. Exit
Choose: _
```

---

##  Features

| Feature | Description |
|---|---|
|  **Create Account** | Register with name, phone, password, and address |
|  **Login** | Authenticate using phone number and password |
|  **Deposit** | Add funds to your account |
|  **Withdraw** | Withdraw funds (with balance validation) |
|  **Transfer** | Send money to another account by phone number |
|  **Balance Inquiry** | View current account balance |
|  **Transaction History** | View all past deposits, withdrawals, and transfers |

---

##  Getting Started

### Prerequisites

- A C++ compiler (GCC / G++ recommended)
- Terminal or Command Prompt

### Installation & Run

```bash
# 1. Clone the repository
git clone https://github.com/your-username/bank-management-system.git
cd bank-management-system

# 2. Compile the source code
g++ -o bank main.cpp

# 3. Run the program
./bank          # Linux / macOS
bank.exe        # Windows
```

---

##  Project Structure

```
bank-management-system/
│
├── main.cpp          # Main source file (all logic)
├── ACCOUNT.txt       # Auto-generated: stores account data
├── HISTORY.txt       # Auto-generated: stores transaction history
└── README.md         # Project documentation
```

>  `ACCOUNT.txt` and `HISTORY.txt` are created automatically at runtime. Do not delete them while the program is running.

---

##  How It Works

- **Account Storage** — Account details (name, phone, password, address, balance) are saved to `ACCOUNT.txt` using file I/O (`fstream`).
- **Transaction Logging** — Every deposit, withdrawal, and transfer is appended to `HISTORY.txt`.
- **Authentication** — Login checks the entered phone number and password against stored account data using `strcmp`.
- **Colored Output** — ANSI escape codes are used to display color-coded messages in the terminal (green = success, red = error, cyan = input prompt).

---

##  Known Limitations

- Currently supports **one account at a time** (single-user system).
- Passwords are stored in **plain text** — not suitable for production use.
- `fflush(stdin)` is used for input clearing — this is **undefined behavior** in standard C++ and may not work on all platforms.
- No data encryption or security layer.

---

## Future Improvements

- [ ] Multi-account support with proper record lookup
- [ ] Password hashing (e.g., SHA-256)
- [ ] Use a structured database (SQLite) instead of flat text files
- [ ] Admin panel for managing all accounts
- [ ] GUI using Qt or a web front-end

---

##  Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/my-feature`
3. Commit your changes: `git commit -m 'Add my feature'`
4. Push to the branch: `git push origin feature/my-feature`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👨‍💻 Author

Made by Walidc  
Feel free to star the repo if you found it useful!
