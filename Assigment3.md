* **How to turn in:** create a file in your repository with the code
* **Due date:** Sept-26


### Wallets

You are requested to request a user of your application to provide 5 numbers representing the value in cash stored in 5 different wallets.
Your program should store these five values in a list.
When finished, your application should provide the following information:
* "The fattest wallet has $ value in it."
* "The skinniest wallet has $ value in it."
* "All together, these wallets have $ value in them."
* "All together, the total value of these wallets is worth $ dimes"

Please try to think about different functions to complete your work

###########################################################################################
##Answer1:

wallet1=int(input("Please enter wallet 1 amount: "))
wallet2=int(input("Please enter wallet 2 amount: "))
wallet3=int(input("Please enter wallet 3 amount: "))
wallet4=int(input("Please enter wallet 4 amount: "))
wallet5=int(input("Please enter wallet 5 amount: "))
print("The amounts you entered were ", wallet1 , wallet2, wallet3, wallet4, wallet5)
wallets=[wallet1, wallet2, wallet3, wallet4, wallet5]
fatwallet=max(wallets)
print('The fattest wallet has $' + str(fatwallet) + ' in it')
thinwallet=min(wallets)
print('The skinniest wallet has $' + str(thinwallet) + ' in it')
sumwallet=sum(wallets)
print('All together, these wallets have $' + str(sumwallet) + ' in them')
dimewallet=sum(wallets)*10
print('All together, the total value of these wallets is worth ' + str(dimewallet) + " dimes")

###########################################################################################

## Periodic Table 

The Periodic Table of the Elements was developed to organize information about the elements that make up the Universe.
Write a terminal application that lets you enter information about each element in the periodic table.
Make sure you include the following information:
* symbol, name, atomic number, row, and column

Provide a menu of options for users (inputing numbers) to:
1. See all the information that is stored about any element, by entering that element's symbol.
2. Choose a property, and see that property for each element in the table.
3. Enter a new element
4. Change the attributes of an element, by entering the element's symbol.
5. Exit the program

**You can provide a pre-populated dictionary as part of your program, avoiding the need of typing every time**
###########################################################################################
## Answer2:

elem_dict = {
    "H": ["Hydrogen", 1, 1, 1],
    "He": ["Helium", 2, 1, 18],
    "Li": ["Lithium", 3, 2, 1],
    "Be": ["Beryllium", 4, 2, 2],
    "B": ["Boron", 5, 2, 13],
    "C": ["Carbon", 6, 2, 14],
    "N": ["Nitrogen", 7, 2, 15],
    "O": ["Oxygen", 8, 2, 16],
    "F": ["Fluorine", 9, 2, 17],
    "Ne": ["Neon", 10, 2, 18],
    "Na": ["Sodium", 11, 3, 1],
    "Mg": ["Magnesium", 12, 3, 2],
    "Al": ["Aluminum", 13, 3, 13],
    "Si": ["Silicon", 14, 3, 14],
    "P": ["Phosphorus", 15, 3, 15],
    "S": ["Sulfur", 16, 3, 16],
    "Cl": ["Chlorine", 17, 3, 17],
    "Ar": ["Argon", 18, 3, 18],
    "K": ["Potassium", 19, 4, 1],
    "Ca": ["Calcium", 20, 4, 2],
    "Sc": ["Scandium", 21, 4, 3],
    "Ti": ["Titanium", 22, 4, 4],
    "V": ["Vanadium", 23, 4, 5],
    "Cr": ["Chromium", 24, 4, 6],
    "Mn": ["Manganese", 25, 4, 7],
    "Fe": ["Iron", 26, 4, 8],
    "Co": ["Cobalt", 27, 4, 9],
    "Ni": ["Nickel", 28, 4, 10],
    "Cu": ["Copper", 29, 4, 11],
    "Zn": ["Zinc", 30, 4, 12],
    "Ga": ["Gallium", 31, 4, 13],
    "Ge": ["Germanium", 32, 4, 14],
    "As": ["Arsenic", 33, 4, 15],
    "Se": ["Selenium", 34, 4, 16],
    "Br": ["Bromine", 35, 4, 17],
    "Kr": ["Krypton", 36, 4, 18],
    "Rb": ["Rubidium", 37, 5, 1],
    "Sr": ["Strontium", 38, 5, 2],
    "Y": ["Yttrium", 39, 5, 3],
    "Zr": ["Zirconium", 40, 5, 4],
    "Nb": ["Niobium", 41, 5, 5],
    "Mo": ["Molybdenum", 42, 5, 6],
    "Tc": ["Technetium", 43, 5, 7],
    "Ru": ["Ruthenium", 44, 5, 8],
    "Rh": ["Rhodium", 45, 5, 9],
    "Pd": ["Palladium", 46, 5, 10],
    "Ag": ["Silver", 47, 5, 11],
    "Cd": ["Cadmium", 48, 5, 12],
    "In": ["Indium", 49, 5, 13],
    "Sn": ["Tin", 50, 5, 14],
    "Sb": ["Antimony", 51, 5, 15],
    "Te": ["Tellurium", 52, 5, 16],
    "I": ["Iodine", 53, 5, 17],
    "Xe": ["Xenon", 54, 5, 18],
    "Cs": ["Cesium", 55, 6, 1],
    "Ba": ["Barium", 56, 6, 2],
    "La": ["Lanthanum", 57, 6, 3],
    "Ce": ["Cerium", 58, 6, 19],
    "Pr": ["Praseodymium", 59, 6, 20],
    "Nd": ["Neodymium", 60, 6, 21],
    "Pm": ["Promethium", 61, 6, 22],
    "Sm": ["Samarium", 62, 6, 23],
    "Eu": ["Europium", 63, 6, 24],
    "Gd": ["Gadolinium", 64, 6, 25],
    "Tb": ["Terbium", 65, 6, 26],
    "Dy": ["Dysprosium", 66, 6, 27],
    "Ho": ["Holmium", 67, 6, 28],
    "Er": ["Erbium", 68, 6, 29],
    "Tm": ["Thulium", 69, 6, 30],
    "Yb": ["Ytterbium", 70, 6, 31],
    "Lu": ["Lutetium", 71, 6, 32],
    "Hf": ["Hafnium", 72, 6, 4],
    "Ta": ["Tantalum", 73, 6, 5],
    "W": ["Wolfram", 74, 6, 6],
    "Re": ["Rhenium", 75, 6, 7],
    "Os": ["Osmium", 76, 6, 8],
    "Ir": ["Iridium", 77, 6, 9],
    "Pt": ["Platinum", 78, 6, 10],
    "Au": ["Gold", 79, 6, 11],
    "Hg": ["Mercury", 80, 6, 12],
    "Tl": ["Thallium", 81, 6, 13],
    "Pb": ["Lead", 82, 6, 14],
    "Bi": ["Bismuth", 83, 6, 15],
    "Po": ["Polonium", 84, 6, 16],
    "At": ["Astatine", 85, 6, 17],
    "Rn": ["Radon", 86, 6, 18],
    "Fr": ["Francium", 87, 7, 1],
    "Ra": ["Radium", 88, 7, 2],
    "Ac": ["Actinium", 89, 7, 3],
    "Th": ["Thorium", 90, 7, 19],
    "Pa": ["Protactinium", 91, 7, 20],
    "U": ["Uranium", 92, 7, 21],
    "Np": ["Neptunium", 93, 7, 22],
    "Pu": ["Plutonium", 94, 7, 23],
    "Am": ["Americium", 95, 7, 24],
    "Cm": ["Curium", 96, 7, 25],
    "Bk": ["Berkelium", 97, 7, 26],
    "Cf": ["Californium", 98, 7, 27],
    "Es": ["Einsteinium", 99, 7, 28],
    "Fm": ["Fermium", 100, 7, 29],
    "Md": ["Mendelevium", 101, 7, 30],
    "No": ["Nobelium", 102, 7, 31],
    "Lr": ["Lawrencium", 103, 7, 32],
    "Rf": ["Rutherfordium", 104, 7, 4],
    "Db": ["Dubnium", 105, 7, 5],
    "Sg": ["Seaborgium", 106, 7, 6],
    "Bh": ["Bohrium", 107, 7, 7],
    "Hs": ["Hassium", 108, 7, 8],
    "Mt": ["Meitnerium", 109, 7, 9],
    "Ds": ["Darmstadtium", 110, 7, 10],
    "Rg": ["Roentgenium", 111, 7, 11],
    "Cn": ["Copernicium", 112, 7, 12],
    "Uut": ["Ununtrium", 113, 7, 13],
    "Uuq": ["Ununquadium", 114, 7, 14],
    "Uup": ["Ununpentium", 115, 7, 15],
    "Uuh": ["Ununhexium", 116, 7, 16]
    }

def viewElement(element):
    print(element)
    print("Name: " + element[0])
    print("Symbol: " + str(element[1]))
    print("Atomic Number: " + str(element[1]))
    print("Row: " + str(element[2]))
    print("Column: " + str(element[3]))
    print("\n")

if __name__ == "__main__":
   # elem_dict = {}
    while 1:
        print("\n Main Menu \n")
        print("1. See info of an Element")
        print("2. View all Element Names")
        print("3. Add an Element")
        print("4. View all Atomic Numbers")
        print("5. View all Row Numbers")
        print("6. View all Column Number")
        print("7. Change an element's attribute")
        print("8. Exit")
        option = int(input('Enter your Option: '))

        if option == 1:
            sym = input("Enter the symbol: ")
            viewElement(elem_dict[sym])

        elif option == 2:
            for i in elem_dict.keys():
                print(elem_dict[i][0])

        elif option == 3:
            sym = input("Enter the symbol: ")
            name = input("Enter the element name: ")
            atom = int(input("Enter the atomic number: "))
            row = int(input("Enter the row number: "))
            col = int(input("Enter the column number: "))

            if sym not in elem_dict.keys():
                e1 = element(sym, name, atom, row, col)
                elem_dict[sym] = e1
                print(sym + " added\n")
            else:
                print("Element already present")

        elif option == 4:
            for i in elem_dict.keys():
                print(elem_dict[i][0])
                print(elem_dict[i][1])

        elif option == 5:
            for i in elem_dict.keys():
                print(elem_dict[i][0])
                print(elem_dict[i][2])

        elif option == 6:
            for i in elem_dict.keys():
               print(elem_dict[i][0])
               print(elem_dict[i][3])

        elif option == 7:
            sym = input("Enter the symbol: ")
            name = input("Enter the element name: ")
            atom = int(input("Enter the atomic number: "))
            row = int(input("Enter the row number: "))
            col = int(input("Enter the column number: "))

        elif option == 8:
            print("Exiting")
            break
        else:
            print("Wrong entry, Please re-enter\n")


###########################################################################################
