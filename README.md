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
	
	Imprimir timeConverter(40000)
	
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
	
	Imprimir compareDistances()
	
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
			
			Imprimir 'Invalid number, please follow instructions'
			
		SiNo
			
			SI num % 2 = 0
				
				sum = sum + num;
				
			FinSi
			
		FinSi
		
	Mientras Que num >= 1  & num  <= 100
	
	total = sum;
	
Fin Funcion

Algoritmo totalSumExercise
	
	Imprimir sumOfPairs()
	
FinAlgoritmo

**********************************************************************************************************************************************************************************************************



