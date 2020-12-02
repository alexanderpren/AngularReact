# AngularReact
Proyecto de Angular con Componente React


Este es un proyecto de Prueba para incrustar un componente React en un Proyecto Angular.


Para realizar el despliegue y que puedan convivir ambos Proyectos estos son los pasos que realice.


1.- En el Package.json del Proyecto React, realize las sig. modificaciones:
 agregue la variable: "homepage": “.”  Esto Sirve para realizar Path Relativos.
 
2.- en el archivo de Index Principal de React:
en el getElementById, se tiene que agregar el ID con el cual sera llamado desde Angular.
en este ejemplo lo nombre : agrowareApp

3.- Se tiene que hacer el build del Proyecto para obtener los Scripts de React que despues seran llamados desde la app Angular.
comando: yarn build

4.- Los Scripts que se obtienen despues de comprimir , tienen un nombre similar a los siguientes que describo:



./build/static/js/2.<someUniqueNumbers>.chunk.js
 ./build/static/js/main.<someUniqueNumbers>.chunk.js
 ./build/static/js/runtime-main.<someUniqueNumbers>.js
  
 Estos Archivos se deberan mover hacia algun folder donde puedan ser llamados desde el despliegue de Angular. ejemplo su carpeta JS.
 
 
 despues de agregarlos al folder correspondiente en Angular, se pueden llamar como cualquier Script dentro de algun componente de Angular.
 
 
 Anotando la URL donde fueron agregados y el nombre con el que fue construido(el nombre dentro del getElementById) el Webapp React, en este caso: agrowareApp
 
 
 
 Para ver el funcionamiento de este proyecto, se puede correr, dentro del folder, el comando.
 
 python3 -m http.server 
 
 o con algun servidor que esten usando en el ambiente en el que se encuentren.
 
 
 
  
