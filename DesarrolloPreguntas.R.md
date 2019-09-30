listaDeNumeros <- list(2,5,6,2,1,5,6,10,11,20,15)
listaDeNumeros[5]

####Ejercicio1####

listaDeNumeros[0]

listaDeNumeros[15]

listaDeNumeros[9] 

listaDeNumeros[-3]

####Ejercicio2####

unlist(listaDeNumeros[5])

if(listaDeNumeros[5]>0){
print("SE CUMPLE")
}

if(listaDeNumeros[6]>3){
print("SE CUMPLE")
}

if(listaDeNumeros[8]>4){
print("SE CUMPLE")
}

if(listaDeNumeros[5]+1>0){
print(“SE CUMPLE”)
}

if(unlist(listaDeNumeros[5])+1>0){
  print("SE CUMPLE")
}

####Ejercicio3####

listaDeNumeros[5] <- 12

####Ejercicio4####

length(listaDeNumeros)

####Ejercicio5####

5:20
listaDeNumeros[5] <- 12
length(listaDeNumeros)
valorInicial <- 5 
valorFinal <- 20

20:5
valorInicial <- 20
valorFinal <- 5

  length(listaDeNumeros):3

####Ejercicio6####

for(i in 1 : 100){
  print(paste("cuento ",i," misisipis"))
}

####Ejercicio7####

for(i in (listaDeNumeros)){
  print(paste("numero ",i," de la lista"))
}

####Ejercicio8####

for(i in listaDeNumeros){
  if (i%%2==0){
    print("PAR")
  }else{
    print("IMPAR")
  }
}

####Ejercicio9####

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
Determinar_Ganador(100,50,45)
Determinar_Ganador(100,25,10)

####Ejercicio10####

Suma<-function(a,b){
  a+b
}
Suma(3,4)

Resta<-function(a,b){
  a-b
}
Resta(7,5)

Multiplicar<-function(a,b){
  a*b
}
Multiplicar(4,15)

Dividir<-function(a,b){
  a/b
}
Dividir(8,2)

####Ejercicio11####

AreaCirculo<-function(radio1,radio2){
  ((pi*radio1^2)-(pi*(radio2^2)))
}
AreaCirculo(16,5)

AreaRectangulo<-function(base1,altura1,base2,altura2){
  ((base1*altura1)-(base2*altura2))
}
AreaRectangulo(50,10,25,5)

####Opcional####

for(i in listaDeNumeros){
  print(i)
}

