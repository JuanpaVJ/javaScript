**********************************************************************************************************************************************************************************************************
Week 5
**********************************************************************************************************************************************************************************************************

Challenge 1
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

