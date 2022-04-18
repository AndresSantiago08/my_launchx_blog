---
title: "Lo que he aprendido en la segunda semana de NodeJS"
date: 2022-04-17
description: 'Lo que he visto'
---

# Hola lector!
Lo que pude aprender de la segunda semana fue:  
- Usar algunos comandos básicos de git  
  > Verificar la lista de "commits" que se realizaron de forma local: **git log**  
  > Agregar un archivo que evita que archivos o carpetas se guarden en el repositorio : **.gitignore**     
- Declaraciones de Objetos  
  Ejemplo Objeto con métodos:   
  ```Js 
  const pet = {  
  name: "Tulio",  
     // Esta es una función que se guarda como propiedad  
     sayHello: function(){  
       // this.name hace referencia a la propiedad del objeto  
        console.log(`${this.name} te saluda en español!`)  
     }  
   }  
  
  console.log("Ejemplo 4: Objeto con métodos")  
  pet.sayHello() 
  ```  
- Operadores
  > Foreach, Map, Filter, Reduce, Every, Find, FindIndex, Some, Sort.     
  Ejemplo de Map:  
  ```Js
  // Ejemplo 5: Uso de Map para convertir todos los nombres de una lista a minúsculas  
  const names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']  
  const namesToUpperCase = names.map((name) => name.toUpperCase())  
  console.log("Ejemplo 5: Uso de Map para convertir todos los nombres de una lista a minúsculas")  
  console.log(namesToUpperCase)   
  ```
- Clases y Objetos  
  > Clase vacía, Instanciar objetos de una clase, Instanciar Objeto con atributos, Métodos en los objetos,    
  > Atributos con valores por default, Getters, Setters, Métodos static, Herencia y Overriding methods.     
  Ejemplo de instanciar un objeto con atributos, métodos, Getter, Setter, método static, herencia de clase y overriding métodos.    
  ```Js
  class TwitterUser {
    constructor(name, username){
        this.name = name;
        this.username = username;
    }

    get getName(){
        return this.name;
    }

    set setName(NewName){
        this.name = NewName;
    }

    getInfo(){
        return `User ${this.name}, with username: ${this.username}`
    }
  }

  class TwitterInfo extends TwitterUser{
    constructor(name, username, joinedIn){
        super(name, username)
        this.joinedIn = joinedIn;
    }

    getStatus(followers){
        return this.getInfo() + ` has got ${followers} followers since ${this.joinedIn}`
    }

    getNumberTweets(numberTweets){
        return this.getInfo() + ` has published ${numberTweets} tweets`
    }
  }

  // Llamar a la clase TwitterUser
  const NewUser = new TwitterUser("Andres Santiago", "AndresSantiago08");
  // Mostrar nombre
  console.log(NewUser.getInfo());
  // Cambiar nombre
  NewUser.setName = "A. Santiago";
  // Mostrar la información
  console.log(NewUser.getName);
  // Guardar nuevo nombre
  const NewName = NewUser.getName;
  // Llamar a la clase TwitterInfo
  const MoreInfo = new TwitterInfo(NewName, "AndresSantiago08", "April 2013");
  // Mostrar método getStatus
  console.log(MoreInfo.getStatus(10));
  // Mostrar método getNumberTweets
  console.log(MoreInfo.getNumberTweets(875));
  
### Gracias por leer, espero te sea de utilidad.
