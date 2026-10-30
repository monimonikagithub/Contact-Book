contacts={}
print("1.New Contact\n","2.Search Contact\n","3.View Contacts\n","4.Update Contact\n","5.Delete Contact")
def add_contact():
    name=input("Enter name:")
    if name in contacts:
        print("contact name",name,"already exist")
    else:
        ph=int(input("Enter phone number:"))
        contacts[name]=[ph]
        print("Successfull your new contact is addes")
def search_contact():
    p=input("Enter name:")
    if p in contacts:
        print(p,":",*contacts[p])
    else:
        print(f"{p} is not in contacts")
def view_contacts():
    if len(contacts)!=0:
        for key,val in contacts.items():
            print(key,":",*val)
    else:
        print("there is no contacts")
def delect_contact():
    n=input("Enter name :")
    if n in contacts:
        contacts.pop(n)
    else:
        print(n,"is not in contacts")
def update_contacts():
    n=input("Enter name:")
    if n in contacts:
        m=int(input("Enter a number:"))
        contacts[n]=[m]
        print("Your contact is updated, if you want to vivw your updated contact please enter :")

while True:
    choice=int(input("Enter your choice:"))
    if choice==1:
        add_contact()
    elif choice==2:
        search_contact()
    elif choice==3:
        view_contacts()
    elif choice==4:
        update_contacts()
    elif choice==5:
        delect_contact()
    elif choice == 6:
        print("Exit")
        break
    else:
        print("Please enter valide choice:")
