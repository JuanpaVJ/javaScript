**********************************************************************************************************************************************************************************************************
Week 5
**********************************************************************************************************************************************************************************************************

Challenge 1 Monday
Time Converter
**********************************************************************************************************************************************************************************************************

Funcion dateTransformed <- timeConverter (input)
	
	Definir dateTransformed Como Caracter;
	
	Definir days, hours, minutes, seconds Como Entero;
	
	seconds = input % 60;
	
	minutes = Trunc(input/60) % 60;
	
	hours = Trunc(input/3600) % 24;
	
	days = Trunc(input/86400);
	
	dateTransformed = Concatenar('days: ', ConvertirATexto(days));
	
	dateTransformed = Concatenar(dateTransformed, ', hours: ');
	
	dateTransformed = Concatenar(dateTransformed, ConvertirATexto(hours));
	
	dateTransformed = Concatenar(dateTransformed, ', minutes: ');
	
	dateTransformed = Concatenar(dateTransformed, ConvertirATexto(minutes));
	
	dateTransformed = Concatenar(dateTransformed, ', and seconds: ');
	
	dateTransformed = Concatenar(dateTransformed, ConvertirATexto(seconds));
	
Fin Funcion

Algoritmo finalConvertion
	
	Escribir timeConverter(40000)
	
FinAlgoritmo

**********************************************************************************************************************************************************************************************************

Challenge 2 Monday
Compare Distances
**********************************************************************************************************************************************************************************************************
Funcion distance <- compareDistances ()
	
	Definir distance Como Logico;
	
	Definir negative, positive Como Real;
	
	negative = 0;
	
	positive = 0;
	
	Para count=1 Hasta 5 Con Paso 1 Hacer
		
		Escribir "Write a number"
		
		leer number
		
		SI number > 0 Entonces
			
			positive = positive + number;
			
		SiNo
			
			negative = negative + number;
			
		FinSi
		
	FinPara
	
	distance = positive > Abs(negative)
	
Fin Funcion

Algoritmo testDistance
	
	Escribir compareDistances()
	
FinAlgoritmo

**********************************************************************************************************************************************************************************************************

Challenge 1 Tuesday
Sum of Pairs
**********************************************************************************************************************************************************************************************************

Funcion total <- sumOfPairs ()
	
	Definir total Como Real;
	
	Definir suma Como Real;
	
	sum = 0;
	
	Repetir
		
		Escribir "Write a number between 1 and 100"
		
		leer num
		
		SI  num < 1  | num > 100 Entonces
			
			Escribir 'Invalid number, please follow instructions'
			
		SiNo
			
			SI num % 2 = 0
				
				sum = sum + num;
				
			FinSi
			
		FinSi
		
	Mientras Que num >= 1  & num  <= 100
	
	total = sum;
	
Fin Funcion

Algoritmo totalSumExercise
	
	Escribir sumOfPairs()
	
FinAlgoritmo

**********************************************************************************************************************************************************************************************************

Challenge 2 Tuesday
Mid point
**********************************************************************************************************************************************************************************************************
Funcion result <- MidPoint (n1,n2)

	Si n1 > 0 Entonces
	
		Si n2 > 0 Entonces
		
			SI n1 > n2 Entonces
			
				result = n2 + ((n1 - n2) / 2); 
				
			SiNo
			
				result = n1 + ((n2 - n1) / 2);
				
			FinSi
			
		SiNo
		
			result = n1 - ( (n1 + Abs(n2))/2);
			
		FinSi
		
	SiNo
	
		SI n2 > 0 Entonces
		
			result = n1 + ( (n2 + Abs(n1))/2)	;
			
		SiNo
		
			SI Abs(n1) > Abs(n2) Entonces
			
				result = n1 + ((Abs(n1) - Abs(n2)) / 2); 
				
			SiNo
			
				result = n2 + ((Abs(n2) - Abs(n1)) / 2); 
				
			FinSi
			
		FinSi
		
	FinSi
	
Fin Funcion

Algoritmo exercise

	Escribir midPoint(40,80)
	
	Escribir midPoint(40,-80)
	
	Escribir midPoint(50,50)
	
	Escribir midPoint(-50,50)
	
FinAlgoritmo
**********************************************************************************************************************************************************************************************************
Challenge 1 Wednesday
Cashier
**********************************************************************************************************************************************************************************************************
Funcion balance <- checkIn ()

	Definir balance Como Real;
	
	balance = 1000;
	
	Repetir
		Escribir "select an option:";
		
		Escribir "a. to deposit.";
		
		Escribir "b. withdraw.";
		
		Escribir "c. go out.";
		
		leer option
		
		Si option = 'a' Entonces
		
			balance = balance + deposit()
			
		FinSi
		
		Si option = 'b' Entonces
		
			balance = balance - withdraw()
			
		FinSi
		
	Mientras Que option = "a" | option = "b"
	
Fin Funcion

Funcion value <- deposit()

	Escribir "how much do you want to deposit:";
	
	leer value
	
FinFuncion

Funcion value <- withdraw()

	Escribir "how much do you want to withdraw:";
	
	leer value
	
FinFuncion

Algoritmo exercise

	Escribir checkIn()
	
FinAlgoritmo

**********************************************************************************************************************************************************************************************************



