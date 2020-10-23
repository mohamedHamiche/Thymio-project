var cptt 
#timer.period[0] = 1000000
#onevent timer0



call leds.bottom.left(15,0,15)
call leds.bottom.left(15,0,15)

motor.left.target = 400
motor.right.target = 400

cptt=0
onevent prox
if prox.ground.ambiant[1]== 0 or prox.ground.ambiant[0]==0  then

motor.left.target = 500

motor.right.target =500
call leds.bottom.left(15,0,15)

cptt++

else

 motor.left.target = 0

 motor.right.target = 0

call leds.bottom.left(0,0,15)
call leds.bottom.left(0,0,15)

end

## Comment fonctionne le programme pour parcourir une distance de 10cm, 20cm ou 40 cm et comment l'utiliser ?

Le programme est relativement simple pour le moment pusique nous utilisons pour l'instant aucun état, seulement avec des conditions if-else et des onevent ça nous a permis de calculer la vitesse en m/s.
Il y a une première `condition if` qui permet de passer à une valeur de 500 (par exemple dans le programme ci-dessus) si les capteurs captent du noir qui est correspond à 0 pour les valeurs : `prox.ground.ambiant[0]` & `prox.ground.ambiant[1]`.
La condition else permet au robot de s'arrêter lorsque ces valeurs ne sont plus égales à 0


