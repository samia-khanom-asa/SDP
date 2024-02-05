# SDP
import tkinter as tk
from tkinter import messagebox

def create_account():
    username = username_entry.get()
    password = password_entry.get()

   

   
    messagebox.showinfo("Account Created", f"Account created successfully!\nUsername: {username}\nPassword: {password}")


root = tk.Tk()
root.title("Account Signup")


username_label = tk.Label(root, text="Username:")
username_entry = tk.Entry(root)

password_label = tk.Label(root, text="Password:")
password_entry = tk.Entry(root, show="*")  # Show asterisks for password input


signup_button = tk.Button(root, text="Sign Up", command=create_account)


username_label.grid(row=0, column=0, pady=10)
username_entry.grid(row=0, column=1, pady=10)

password_label.grid(row=1, column=0, pady=10)
password_entry.grid(row=1, column=1, pady=10)

signup_button.grid(row=2, column=0, columnspan=2, pady=10)


root.mainloop()

import tkinter as tk
from tkinter import messagebox

users = {
    "user1": "password1",
    "user2": "password2"
}

def login():
    username = username_entry.get()
    password = password_entry.get()


    if username in users and users[username] == password:
        messagebox.showinfo("Login Successful", f"Welcome, {username}!")

    else:
        messagebox.showerror("Login Failed", "Invalid username or password")


root = tk.Tk()
root.title("Login")


username_label = tk.Label(root, text="Username:")
username_entry = tk.Entry(root)

password_label = tk.Label(root, text="Password:")
password_entry = tk.Entry(root, show="*")  # Show asterisks for password input


login_button = tk.Button(root, text="Login", command=login)


username_label.grid(row=0, column=0, pady=10)
username_entry.grid(row=0, column=1, pady=10)

password_label.grid(row=1, column=0, pady=10)
password_entry.grid(row=1, column=1, pady=10)

login_button.grid(row=2, column=0, columnspan=2, pady=10)


root.mainloop()

