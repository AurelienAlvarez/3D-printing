# Tetrahedron

Dans tetrahedron.playground, on trouve un programme écrit en Swift qui génère dans la console un fichier au format STL : c'est le fichier tetrahedron.stl.

![How it looks](https://github.com/AurelienAlvarez/Triangulations/blob/master/Tetrahedron/tetrahedron.jpg)





Le tétraèdre
 
 Dans R^4, on note P, Q, R, S les quatre sommets du simplexe standard dont les coordonnées sont :
 - P = (1, 0, 0, 0)
 - Q = (0, 1, 0, 0)
 - R = (0, 0, 1, 0)
 - S = (0, 0, 0, 1)
 
 Ces quatre points appartiennent à l'hyperplan affine d'équation x1 + x2 + x3 + x4 = 1. Notons P0 le point de coordonnées 1/4 (1, 1, 1, 1) que nous prendrons comme origine de l'hyperplan affine précédent.
 
 Un vecteur normal unitaire à cet hyperplan est n = 1/2 (1, 1, 1, 1). Une base orthonormale de l'hyperplan est donnée par les trois vecteurs :
 - u1 = 1/sqrt(2) (1, -1, 0, 0)
 - u2 = 1/2 (1, 1, -1, -1)
 - u3 = 1/sqrt(2) (0, 0, 1, -1)
 
 Le calcul du déterminant (u1, u2, u3, n) donne 1, ce qui assure cette base d'être orthonormée directe.
 
 Des calculs élémentaires permettent de calculer les coordonnées des points P, Q, R, S dans le repère orthonormal P0 + (u1, u2, u3). On trouve :
 - P = (1/sqrt(2), 1/2, 0)
 - Q = (-1/sqrt(2), 1/2, 0)
 - R = (0, -1/2, 1/sqrt(2))
 - S = (0, -1/2, -1/sqrt(2))
 
 Le centre de la face (PQR) est le point C = 1/3 * (P + Q + R) de coordonnées (0, 1/6, 1/3*sqrt(2)). On en déduit qu'un vecteur normal à cette face dirigé vers l'extérieur du tétraèdre est le vecteur SC = (0, 2/3, 2*sqrt(2)/3). Le calcul du produit vectoriel de PQ par PR donne le vecteur (3/2)*SC, ce qui assure que la face (PQR) est bien orientée. On en déduit ainsi la liste des quatre faces orientées :
 - (PQR)
 - (PRS)
 - (PSQ)
 - (QSR)
 
 Enfin, notons que dans le tétraèdre, deux sommets distincts sont reliés par une arête.







