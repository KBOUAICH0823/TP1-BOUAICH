# TP1-BOUAICH
Mon premier projet
      Exercice 1:
Algorithme_Pin
    VAR code saisie , erreur :entier
    CONS code pin:entier
Debut
    erreur<--0
     repeter
       ecrire("saisie le code pin:")
       lire (pin_saisie)
        Si code pin= code saisie alors
          ecrire("operation fait avec succes")
          sinon
          Erreur←erreur+1
          Ecrire("erreur")
           Si erreur=3 alors
             Ecrire ("carte SIM bloque")
           Fin si
        Fin si
      jusqu'a (code pin=code saisi)ou (erreur=3)
 fin

          Exercice 2:
Algorithme_l'echange
   Var a,b,c:entier
Debut
  Ecrire("donner la valeur de a et b")
  Lire (a,b)
    c←a
    a←b
    b←c
   ecrire("a=", a , "b=",b)
Fin

            Exercice 3
1} avec les boucles:
Algorithme_PGCD
    VAR a,b,reste:entier
Debut                                                                  
 ecrire("donner les valeurs de a et b")                             1
 Lire (a,b)                                                         1
     Tant que b!= 0 faire.                                          n
       reste←a mod b.                                               1 
       a←b.                                                         1
       b←reste.                                                     1
     Fin tant que
  ecrire("PGCD est:",PGCD)                                          1  
Fin
                                                             T(n)= 6n =O(n)

2} avec les fonctions recursives:
Algorithme PGCD
    VAR a,b,reste: entier
    Fonction PGCD (a,b:entier):entier
      Si b=0 ,alors                                                  (1+1)*n= 2n                                                
          Retourne a                                                 1
           Sinon
           Retourne PGCD(b,a mod b)                                  1
      Fin si 
     Fin fonction
Debut
  ecrire("donner les valeurs de a et b")                             1
   Lire (a,b)                                                        1
   ecrire(" le PGCD est:" ,PGCD(a,b))                                1
Fin
                                                               T(n)=2n+5=O(n)


           Exercice 5
Algorithme_deviner_un_nombre
   Var secret,x,tetative:entier
   Reponse:chaine
Debut
   Repeter
      Secret ← aleatoire(1,100)
      tentative ← 0
      Tant que tentative< 5 faire
         ecrire("deviner un nombre:")
         Lire x
         tentative ← tentative+1
           Si x=secret alors
              ecrire("felicitation")
             Sinon
               Si x< secret ,alors
                 ecrire("trop petit")
                   Sinon
                   ecrire ("trop grand")
               Fin si 
           Fin si
      Fin tant que
        Si x != secret, alors
           Ecrire("malheureusemet,le secret est:", secret)
        Fin si
         Ecrire("voulez vous rejouer? Oui ou nom")
         Lire reponse
    jusqu'a (x=secret)ou( reponse =non)
Fin

            Exercice 6
Algorithme_triangle_de_floyd
    VAR a,i,n:entier
     Procedure lignes(a:entier , n:entier)
       Pour j de 1 a i faire.                                     3n+1    
          Ecrire a.                                               n
           a ← a + 1                                              2n
       Fin pour  
       ecrire("\n")
    Fin procedure
Debut
    ecrire("donner un nombre")                                    1
    Lire n                                                        1
     a←1                                                          1             
     Pour i de 1 a n faire
        Procedure lignes (a,n)  
         a←a+i                                                    1+1=2          
      Fin pour
Fin                                                            T(n)= O(n²)



            Exercice 7 
1}  avec les boucles:
Algorithme_somme_des_entiers
        Var n,s,i :entier
  Debut
    ecrire("donner un nombre")                                     1
    lire n.                                                        1
    somme ← 0.                                                     1
         Pour i de 1 a n faire.                                    2n
              s ← s+1.                                             2          
         Fin pour
           Ecrire("la somme est:"s)                                1
Fin                                                         T(n)= 2n+6 = O(n)



2} avec les fonctions recursives:
ALGORITHME somme_des_entiers
 VAR nombre,somme:ENTIER
    Fonction sommeEntier (n:ENTIER): ENTIER
       Si (n = 1 ) ,Alors                                             1
         retourne  n.                                                 1
         Sinon
         retourne  n + sommeEntier(n-1)                               n
       Fin Si
    Fin Fonction

DEBUT
      
      ecrire("Donner un nombre: ")                                    1
      lire(nombre)                                                    1
      somme ← sommeEntier(nombre)                                     1
      ecrire("La somme est:", somme)                                  1
FIN                                                                 T(n)=6(n)=O(n)

