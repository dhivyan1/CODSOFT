def display_menu():
    print("To-Do List Application")
    print("1. Create Task")
    print("2. Update (Edit) Task")
    print("3. View Tasks")
    print("4. Exit")

def create_task(tasks, new_task):
    tasks.append(new_task)
    print("Task created successfully!")

def update_task(tasks, task_index, updated_task):
    if 1 <= task_index <= len(tasks):
        tasks[task_index - 1] = updated_task
        print(f"Task {task_index} updated successfully.")
    else:
        print("Invalid task index.")

def view_tasks(tasks):
    if not tasks:
        print("No tasks found.")
    else:
        print("Current Tasks:")
        for i, task in enumerate(tasks, start=1):
            print(f"{i}. {task}")

def main():
    tasks = []

    while True:
        display_menu()

        choice = input("Enter your choice (1-4): ")

        if choice == "1":
            new_task = input("Enter the task: ")
            create_task(tasks, new_task)
        elif choice == "2":
            task_index = int(input("Enter the task index to update: "))
            updated_task = input("Enter the updated task: ")
            update_task(tasks, task_index, updated_task)
            view_tasks(tasks)
        elif choice == "3":
            view_tasks(tasks)
        elif choice == "4":
            print("Exiting the To-Do List Application. Goodbye!")
            break
        else:
            print("Invalid choice. Please enter a number between 1 and 4.")

        # Save tasks to a file after each operation
        with open('tasks.txt', 'w') as f:
            for task in tasks:
                f.write(task + '\n')

if __name__ == "__main__":
    main()
