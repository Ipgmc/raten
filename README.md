# raten

import random

punkte=0

from colorama import *

init(autoreset=True)

def mainfnc():

    begriffe=[("Gemeine Kiefer", "Pinus silvestris"), ("Gemeine Fichte","Picea abies"), ("Roteiche", "Quercus rubra"), ("Gemeine Buche", "Facus sylvatica"),
              ("Baumhasel", "Corylus colurna"), ("Bergahorn", "Acer pseudoplatanus"), ("Spitzahorn", "Acer platanoides"), ("Feldahorn", "Acer campestre"),
              ("Weißtanne", "Abies alba"), ("Eberesche", "Sorbus aucuparia"), ("Gemeine Esche", "Fraxinus excelsior"), ("Gemeine Lärche", "Larix decidua"),
              ("Nordmanntanne", "Abies nordmanniana"), ("Coloradotanne", "Abies concolor"), ("Hainbuche", "Carpinus betulus"), ("Eibe", "Taxus baccata"),
              ("Bergkiefer", "Pinus mugo"), ("Weymouthskeifer", "Pinus strobus"), ("Wacholder", "Juniperus communis"), ("Schwarzpappel", "Populus nigra"),
              ("Silberweide", "Salix alba"), ("Hängebirke", "Betula pendula"), ("Grauerle", "Alnus incana"), ("Schwarzerle", "Alnus glutinosa"),
              ("Traubeneiche", "Quercus petraea"), ("Stieleiche", "Quercus robur"), ("Feldulme", "Ulmus minor"), ("Robinie", "Robinia pseudacacia"),
              ("Roßkastanie", "Aesculus hippocastanum"), ("Sommerlinde", "Tilia platyphyllos"), ("Salweide", "Salix caprea"), ("Gemeine Haselnuss", "Corylus avellana"),
              ("Grünerle", "Alnus viridis"), ("Efeu", "Hedera helix"), ("Eingriffeliger Weißdorn", "Crataegus monogyna"), ("Schwarzdorn", "Prunus spinosa"),
              ("Traubenkirsche", "Prunus padus")]
              
    rdi=random.randint(0, len(begriffe)-1)

    rdi2=random.randint(0, 1)
    
    inp_str=input(begriffe[rdi][0]+":")
    
    global punkte
    
    if (inp_str==begriffe[rdi][1]):
    
        print("Korrekt.")

        punkte+=1
    else:
    
        print(Fore.RED + "Falsch.")
        
        punkte-=1
        
        print(Fore.RED + "Korrekter Begriff: "+ begriffe[rdi][1])
        
    if (punkte==1 or punkte==-1):
    
        print(str(punkte) + " Punkt")
        
    else:
    
        print(str(punkte) + " Punkte")
        
    print("")
    
    mainfnc()
    
mainfnc()
