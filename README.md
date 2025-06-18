# 📝 Simple To-Do List App for Beginners

# Step 1: Create an empty list to store your tasks
tasks = []

# Step 2: Run the menu in a loop so the user can keep using it
while True:
    # Show the menu options
    print("\n=== TO-DO LIST MENU ===")
    print("1. ➕ Add a Task")
    print("2. 📋 View All Tasks")
    print("3. ❌ Exit the App")
    print("=======================")

    # Ask the user what they want to do
    choice = input("👉 Enter your choice (1 / 2 / 3): ")

    # If the user wants to add a task
    if choice == '1':
        task = input("🆕 What task do you want to add? ")
        tasks.append(task)
        print("✅ Task added successfully!")

    # If the user wants to view all tasks
    elif choice == '2':
        if not tasks:
            print("📭 Your task list is empty.")
        else:
            print("\n📋 Here's what you have to do:")
            for index, task in enumerate(tasks, start=1):
                print(f"{index}. {task}")

    # If the user wants to exit
    elif choice == '3':
        print("👋 Thanks for using the To-Do List App. Goodbye!")
        break

    # If the user enters something invalid
    else:
        print("❌ Oops! Please enter 1, 2, or 3 only.")
