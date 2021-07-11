# Life-checker
This program determines if a thing is animal or a plant. First, this program must determine if it is living before any considerations regarding whether or not this thing is an animal or a plant.

class Life:
    def isLife(self):
        cell = (input("Does this thing have a cell? (Enter True if yes or False if no): "))
        while(cell != "True" and cell != "False"):
            cell = input("Enter a valid response (True for yes or False for no): ")
        if(cell == "True"):
            return True
        else:
            return False

class Animal(Life):
    def isAnimal(self):
        life = Life.isLife(self)
        if(life == False):
            print("This is not a living thing")
            return False
        else:
            lysosome = (input("Does this life have lysosomes? (Enter True if true or False if false): "))
            while(lysosome != "True" and lysosome != "False"):
                lysosome = input("Enter a valid response (Enter True or False): ")
            if(lysosome == "True"):
                print("This is an animal")
                return True
            else:
                print("This is not an animal")
                return False

class Plant(Life):
    def isPlant(self):
        life = Life.isLife(self)
        if(life == False):
            print("This is not a living thing")
            return False
        else:
            cellWall = (input("Does this life have a cell wall? (Enter True if true or False if false): "))
            while(cellWall != "True" and cellWall != "False"):
                cellWall = input("Enter a valid response (Enter True or False): ")
            if(cellWall == "True"):
                print("This is a plant")
                return True
            else:
                print("This is not a plant")
                return False

rerun = 'y'
print("This program will determine if an entity is living or nonliving")
print("If it is living, it will determine if it is an animal or plant")
while (rerun == 'y' or rerun == 'Y'):
    a = Animal()
    p = Plant()
    form = input("Do you want to see if something is an animal or plant? (Enter 'A' for animal or 'P' for plant): ")
    while(form != 'A' and form != 'P'):
        form = input("Enter a valid response (Enter 'A' for animal or 'P' for plant): ")
    if(form == 'A'):
        a.isAnimal()
    else:
        p.isPlant()
    rerun = input("Want to run this program again? (Type 'Y' or 'y' for yes): ")
