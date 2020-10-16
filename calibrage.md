var cptt
#timer.period[0] = 100
#onevent timer0
motor.left.target = 200
motor.right.target = 200

	
cptt=0
onevent prox

if prox.ground.ambiant[1]== 0 or prox.ground.ambiant[0]==0  then
	motor.left.target = 100
	motor.right.target =100
	cptt++
else 
	 motor.left.target = 0
	 motor.right.target = 0
  	
		
end

		