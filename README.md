# Ts--Cs
Typescript cheat sheet 
// Welcome to the TypeScript Playground, this is a website
// which gives you a chance to write, share and learn TypeScript.

// You could think of it in three ways:
//
//  - A location to learn TypeScript where nothing can break
//  - A place to experiment with TypeScript syntax, and share the URLs with others
//  - A sandbox to experiment with different compiler features of TypeScript

const anExampleVariable:String = "Hello World"
let num :Number = 6;
let isLoggedIn:boolean = false;
let hero:String; 
function getHero(){
    return "s"
}
hero = getHero()
console.log(hero);

console.log(anExampleVariable)

const myObj = {"id":1, "username":"Animesh"};

const addtwovalues = (key:number):number =>{
 return 7
}
console.log(addtwovalues(4));

let arr = [2,4,4,5]
const mytake = arr.map((val):number=>{
return val+2;
})
console.log(mytake)

function logErrros(errrmsg:string):void{
    console.log(errrmsg)
}
function throwerror(err:string):never{
    throw(err);
}
// 1/3rd off all the Ts for you 

// To learn more about the language, click above in "Examples" or "What's New".
// Otherwise, get started by removing these comments and the world is your playground.

//type alias
function createCourse(name:string,course:string,Price:number):{name:string,course:string,Price:number}{
return {name , course , Price}
}  

const cred:{} = createCourse("Animesh","CVSS",654);
console.log(cred);
type User = {
    name:string;
    email:string;
    readonly id:number;  //readonly use case cannot reassign 
    credDeatils?:cardDetailsimp  //optional can be given cannot be given does not give error
}
function createEvent(user:User):User{
    return {name:user.name , email:user.email , id:user.id}
}
type cardNumbertype =  { 
      cardNumber:number
}
type expiryDate = {
    lastDate:string
}
 //use of union for combining types
type cardDetailsimp =cardNumbertype &  expiryDate &{ 
    cvv:number;
}


const myEvent = createEvent({name:"A",email:"ANIMHS@YOPMAIL.COM",id:1 ,credDeatils:{cardNumber:2,lastDate:"01/09/2023",cvv:123}})
console.log(myEvent);
// myEvent.id =2; //readonly value id

//1:46

// To learn more about the language, click above in "Examples" or "What's New".
// Otherwise, get started by removing these comments and the world is your playground.
  
