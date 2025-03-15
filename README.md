# python-lab5_02
#forcer l'entrer des boucles
Annee=0
Capital=0
TauxInteret=0
while Capital<=0:
    try:
        #lecture du capitale de départ
        Capital=float(input("Veuillez entrer votre capital de départ:"))
        #Validation du capitale de départ
        if Capital<=0:
            raise Exception ("le Capital de départ doit etre supérieur à zéro")
        #Bloc de gestion d'érreurs
    except ValueError:
        print("Désoler, la valeur entrée est invalide")
    except Exception as ex:
        print(f"Désolé, {ex.args[0]}")
while TauxInteret<=0:
    try:
        #lecture du taux d'intéret
        TauxInteret=float(input("Veuillez entre votre taux d'intérêt annuel en pourcentage:"))
        #Validation du taux d'intéret
        if TauxInteret<=0:
            raise Exception ("le taux d'intérêt doit etre supérieur à zéro")
    #Bloc de gestion d'érreurs
    except ValueError:
        print("Désoler, la valeur entrée est invalide")
    except Exception as ex:
        print(f"Désolé, {ex.args[0]}")

while Capital<=1000000:
    #Calcul du capital selon le taux d'intéret
    Gain=Capital*TauxInteret/100
    Capital=Capital+Gain
    #incrémentation des années
    Annee=Annee+1
#affichage du résultat
print(f"Votre capitale a attient:{Capital:.2f}$ après {Annee} ans.")
