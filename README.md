# Problem-2
Given Luceafarul find all anagrams in the text, with counts for each anagram and display them ordered.


def Anagrama(cuvant):
    if cuvant == cuvant[::-1]:
        return True
    return False
def Rezolvare(numeFis):
    listamea = []
    with open(numeFis, "r") as ins:
        arrayy = []
        for line in ins:
            if(line.isspace() == False):
                arrayy.append(line)
        for el in arrayy:
            t = el.split(" ")
            for cuv in t:
                if(Anagrama(cuv) == True and cuv.isspace() == False):
                    if(not cuv in listamea):
                        listamea.append(cuv)
        print(listamea)

Rezolvare("Luceafarul.txt")
