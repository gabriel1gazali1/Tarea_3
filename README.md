# Tarea_3

listaDeNumeros <- list(2,5,6,2,1,5,6,10,11,20,15)

listaDeNumeros[5]
[[1]]
[1] 1                         <Debido a que el 5to numero en la lista es el "1"

**####Ejercicio 1: ¿Qué pasa si reemplazamos el 5 por un 0?¿Qué pasa si en vez de poner un
número positivo, menor igual al largo de la lista, colocamos un número mayor a la cantidad
de elementos de la lista o un número negativo?**

listaDeNumeros[0]
list()                        <Debido a que el 0 no se encuentra dentro de la lista


listaDeNumeros[15]
[[1]]
NULL                          <Debido a que no existe una posicion n°15 dentro de la lista

listaDeNumeros[9] 
[[1]]
[1] 11                        <Debido a que el 9no numero en la lista es 11

listaDeNumeros[-3]
<Quita el 3er numero de la lista y arroja los demás.

**####Ejercicio 2: A continuación se le presenta la función unlist, la cual se puede usar de la
siguiente manera: unlist(listaDeNumeros[5]) ¿Qué diferencia existe entre usar o no el unlist,
y cómo cree ud que le podría ayudar esta función?, pista: experimente usando el
condicional if**
 
unlist(listaDeNumeros[5])
[1] 1                        <arroja el valor el 5to numero de la lista.

if(listaDeNumeros[5]>0){
 print("SE CUMPLE")
 }
[1] "SE CUMPLE"              <Debido a que el 5to numero de la lista es mayor que 0.

if(listaDeNumeros[6]>3){
 print("SE CUMPLE")
 }
[1] "SE CUMPLE"              <Debido a que el 6to numero de la lista es mayor que 3.

if(listaDeNumeros[8]>4){
 print("SE CUMPLE")
 }
[1] "SE CUMPLE"              <Debido a que el octavo numero en la lista es mayor que 4.

if(listaDeNumeros[5]+1>0){
 print(“SE CUMPLE”)
Error: unexpected input in:
"if(listaDeNumeros[5]+1>0){
print(“"
 }
Error: unexpected '}' in "}"      <Presenta un error en la escritura.

if(unlist(listaDeNumeros[5])+1>0){
   print("SE CUMPLE")
 }
[1] "SE CUMPLE"

**####Ejercicio3: ¿Qué pasa cuando realizamos la siguiente acción: listaDeNumeros[5] <- 12**
<Remplaza el 5to numero de la lista de un "1" a un "12"

**####Ejercicio4: Existe una función llamada length, esta se usa de la siguiente manera:
length(nombre_variable), ¿por qué debería ser cambiado nombre_variable para que
funcione con el ejemplo que estamos trabajando (listaDeNumeros)? ¿qué da como
resultado?**

length(listaDeNumeros)
[1] 11                  <Debido a que el largo de la lista son 11 digitos.

**####Ejercicio 5: Para generar secuencias se tiene un valor inicial y un valor final, donde ambos
valores son enteros, para el ejemplo, y la sintaxis en R es la siguiente:
valorInicial : valorFinal
¿Que sucede cuando valorInicial <- 5 y valorFinal <- 20, si ahora los invertimos, valorInicial
<- 20 y valorFinal <- 5, y si ahora usamos el length visto en el ejercicio 3,
length(listaDeNumeros), en vez de valorInicial o valorFinal?¿Que pasa si ambos números
son iguales?**

 5:20
 [1]  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20
 listaDeNumeros[5] <- 12
 length(listaDeNumeros)
[1] 11
 valorInicial <- 5 
 valorFinal <- 20              <Se enumera una lista desde el 5 hasta el 20

[1] 20 19 18 17 16 15 14 13 12 11 10  9  8  7  6  5
 valorInicial <- 20
 valorFinal <- 5              <Se enumera una lista desde el 20 hasta al 5

 length(listaDeNumeros):3
[1] 11 10  9  8  7  6  5  4  3   <Se enumera una lista desde el 11 hasta el 3

**####Ejercicio 6: Ejecute el ejemplo anterior y comente ¿Cuál es la condición establecida en el
for, según el resultado que muestra la consola?**

<Se cuenta desde "cuento 1 misisipis" hasta "cuento 100 misisipis"

**####Ejercicio 7: Adapte el código anterior para que imprima los elementos de la lista que se creó anteriormente.**

for(i in (listaDeNumeros)){
  print(paste("numero ",i," de la lista"))
}

**####Ejercicio 8: Usando los condicionales vistas en clases, adapte el código anterior para que
muestre si un número es par o impar.**

for(i in listaDeNumeros){
  if (i%%2==0){
    print("PAR")
  }else{
    print("IMPAR")
  }
}

**####Ejercicio 9: Votaciones**

Determinar_Ganador<-function(total,votosSI,votosNO){
  if (votosSI+votosNO>total){
    "votaciones alteradas"
  }else if (votosSI>=votosNO && votosSI>=0.3*total){
    paste ("Si")
  }else {
    paste ("No")
  }
}

Determinar_Ganador(100,125,70)
[1] "votaciones alteradas"
Determinar_Ganador(100,50,45)
[1] "Si"
Determinar_Ganador(100,25,10)
[1] "No"

**####Ejercicio 10: Una función es un grupo de instrucciones que toma valores de entradas para
generar un resultado. Pruébelo con operaciones resta,multiplicación, división.**

Suma<-function(a,b){
+   a+b
+ }
 Suma(3,4)
[1] 7

Resta<-function(a,b){
+   a-b
+ }
 Resta(7,5)
[1] 2

Multiplicar<-function(a,b){
+   a*b
+ }
 Multiplicar(4,15)
[1] 60

 Dividir<-function(a,b){
+   a/b
+ }
 Dividir(8,2)
[1] 4

**####Ejercicio 11: Cree dos funciones, una que genere la diferencia entre las áreas de dos
rectángulos y otra de las áreas de un círculo:**

AreaCirculo<-function(radio1,radio2){
+   ((pi*radio1^2)-(pi*(radio2^2)))
+ }
 AreaCirculo(16,5)
[1] 725.7079

AreaRectangulo<-function(base1,altura1,base2,altura2){
+   ((base1*altura1)-(base2*altura2))
+ }
 AreaRectangulo(50,10,25,5)
[1] 375

**####Ejercicio Opcional: Ejecute el siguiente código y diga cuales son las ventajas y desventajas de hacer un loop con lista o rango**
for(i in listaDeNumeros){
+   print(i)
+ }
[1] 2
[1] 5
[1] 6
[1] 2
[1] 12
[1] 5
[1] 6
[1] 10
[1] 11
[1] 20
[1] 15   

<la ventaja es que agiliza la escritura o identificacion de la lista con solo especificar su nombre, representando i como cada numero haciendo mas facil efectuar cambios dentro de esta misma.




