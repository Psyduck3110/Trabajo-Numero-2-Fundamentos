# Trabajo-Numero-2-Fundamentos
hermano(carlos).
hermano(alberto).
hermano(luis).

dia(lunes).
dia(martes).
dia(miercoles).
dia(jueves).
dia(viernes).
dia(sabado).
dia(domingo).

frase('Hoy es el tercer dia que miento').
frase('Hola, soy alberto').
frase('Mañana será sabado').


miente(alberto,lunes).
miente(alberto,martes).
miente(alberto, miercoles).

miente(carlos,miercoles).
miente(carlos,jueves).
miente(carlos,viernes).

miente(luis,viernes).
miente(luis,sabado).
miente(luis,domingo).

posible(alberto,'Hola, soy alberto',jueves).
posible(alberto,'Hola, soy alberto',viernes).
posible(alberto,'Hola, soy alberto',sabado).
posible(alberto,'Hola, soy alberto',domingo).

posible(carlos,'Hola, soy alberto',miercoles).
posible(carlos,'Hola, soy alberto',jueves).
posible(carlos,'Hola, soy alberto',viernes).

posible(luis,'Hola, soy alberto',viernes).
posible(luis,'Hola, soy alberto',sabado).
posible(luis,'Hola, soy alberto',domingo).


posible(alberto,'Hoy es el tercer dia que miento',lunes).
posible(alberto,'Hoy es el tercer dia que miento',martes).
posible(carlos,'Hoy es el tercer dia que miento',miercoles).
posible(carlos,'Hoy es el tercer dia que miento',jueves).
posible(luis,'Hoy es el tercer dia que miento',viernes).
posible(luis,'Hoy es el tercer dia que miento',sabado).

posible(alberto,'Mañana será sabado',lunes).
posible(alberto,'Mañana será sabado',martes).
posible(alberto,'Mañana será sabado',miercoles).
posible(carlos,'Mañana será sabado',miercoles).
posible(carlos,'Mañana será sabado',jueves).
posible(alberto,'Mañana será sabado',viernes).
posible(luis,'Mañana será sabado',sabado).
posible(luis,'Mañana será sabado',domingo).
f_posibles(Y,X,Z):-dia(X),hermano(Y),frase(Z),posible(Y,Z,X).
f_posibles(X,Y,Z).
