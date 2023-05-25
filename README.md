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
Challenge 2 Wednesday
Weather Average
**********************************************************************************************************************************************************************************************************
Funcion celsius <- fahrenheitToCelsius (fahrenheit)

	Definir celsius Como Real;
	
	celsius = (fahrenheit - 32 ) / 1.8
	
Fin Funcion

Algoritmo exampleWeatherAverage

	count = 0;
	
	total = 0;
	
	Repetir
	
		Escribir "Select an option:";
		
		Escribir "a. enter degrees celsius.";
		
		Escribir "b. enter degrees fahrenheit.";
		
		Escribir "x. go out.";
		
		leer option
		
		Si option = "a" | option = "b" Entonces
		
			leer degree
			
			count = count + 1;
			
		FinSi
		
		Si option = 'a' Entonces
		
			total = total + degree;
			
		FinSi
		
		Si option = 'b' Entonces
		
			total = total + fahrenheitToCelsius(degree);
			
		FinSi
		
	Mientras Que option = "a" | option = "b"
	
	Escribir total / count;
	
FinAlgoritmo
**********************************************************************************************************************************************************************************************************

Challenge 1 Thursday
If
**********************************************************************************************************************************************************************************************************
let age = 18

if (age >= 18) {
  console.log('You can enter the disco')
} else {
  console.log('You are underage, you can not enter')
  }
Output: You can enter the disco.

**********************************************************************************************************************************************************************************************************

Challenge 2 Thursday
While
**********************************************************************************************************************************************************************************************************
let i = 0

while (i < 10) {
 number = "Number: " + i;
 i = i++
};

output: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
**********************************************************************************************************************************************************************************************************

Challenge 3 Thursday
For
**********************************************************************************************************************************************************************************************************
for (let i = 0; i < 10; i++){
  console.log(i)
}

output: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
**********************************************************************************************************************************************************************************************************

Week 6
**********************************************************************************************************************************************************************************************************

Tuesday to Thursday:

**********************************************************************************************************************************************************************************************************
let firstname = 'Lata';
'Geeta'
let flower = 'rose';
let tree = 'maple';
'Toe'
'Hardy'
const hello = () => {
  return 'Hello world!'
}
const a = () => {
 return 'Hello a!'
}

const b = () => {
 return 'Hello b!'
}
const greet = () => {
 return 'Haydo!'
};

let salutation = greet();
'How do you do?'
const echo = (word) => {
 return word
}

echo('Greta')
echo('CO2')
const greet = (word) => {
 return 'Hello ' + word + '!';
}

greet('Ada')
const length = (word) => {
 return word.length
}

length('word')
const toCase = (word) => {
 return word.toLowerCase() + '-' + word.toUpperCase();
}

toCase('Mthatha')
const shortcut = (word1, word2) => {
 return word1.charAt(0) + word2.charAt(0)
}

shortcut('Amnesty', 'International')
const indexOfIgnoreCase = (word1, word2) => {
 let word1Lower = word1.toLowerCase();
 let word2Lower = word2.toLowerCase();
 return word1Lower.indexOf(word2Lower);
}

**********************************************************************************************************************************************************************************************************



