# Cafe-Management-System
The project based for simple cafe management software
menu={"pizza":90,
      "pasta":50,
      "burger":60,
      "coffee":70,
      "maggie":30,
      "salad":40
    
}
print("welcome to madhu's restaurant")
print("------------------------------")
for x,y in menu.items():
    print(f"{x}:{y:>3}")
total=0
while True:
    item1=input("enter food u like to have or qto quit")
    if item1 in menu:
        total +=menu[item1] #menu[item1] direct reches u the value of key 
  
    else:
        if item1.lower()=="q":
            print("Thank u..!\nYour bill is :",total)
            break
        print(f"Ordered food {item1} is not available yet\nWe will try to add it soon")
        item2=input("Try something different...! or q to quit")
        if item2 in menu:
            total+=menu[item2]
        else:
            if item2.lower()=="q":
                print("Thank u..!\nYour bill is :",total)
                break
