# Internship-task-2-for-python-developmentclass ContactManagementSystem:
    def __init__(self):
        self.contacts = {}

    def add_contact(self, name, phone):
        if name not in self.contacts:
            self.contacts[name] = phone
            print(f"Contact {name} added successfully.")
        else:
            print(f"Contact {name} already exists. Use a different name.")

    def view_contacts(self):
        if not self.contacts:
            print("No contacts available.")
        else:
            print("Contacts:")
            for name, phone in self.contacts.items():
                print(f"{name}: {phone}")

    def delete_contact(self, name):
        if name in self.contacts:
            del self.contacts[name]
            print(f"Contact {name} deleted successfully.")
        else:
            print(f"Contact {name} not found.")

# Example usage
if __name__ == "__main__":
    cms = ContactManagementSystem()

    while True:
        print("\nContact Management System Menu:")
        print("1. Add Contact")
        print("2. View Contacts")
        print("3. Delete Contact")
        print("4. Exit")

        choice = input("Enter your choice (1-4): ")

        if choice == "1":
            name = input("Enter the contact name: ")
            phone = input("Enter the contact phone number: ")
            cms.add_contact(name, phone)
        elif choice == "2":
            cms.view_contacts()
        elif choice == "3":
            name = input("Enter the contact name to delete: ")
            cms.delete_contact(name)
        elif choice == "4":
            print("Exiting Contact Management System. Goodbye!")
            break
        else:
            print("Invalid choice. Please enter a number between 1 and 4.")




The task is to create a contact management system using python language 
