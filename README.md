# Typescript
Typescript Concepts
### Getter and setter

```ts
getter and setter function 

class Profile{
    public id : number
    constructor(public height : number  , protected  weight : number , power:number){
         this.id = Math.floor(Math.random() * 100);
    }


    get getmyheight() : object{
        return [this.height , this.weight];
    }

    
    public set setmyweight(v : number) {
        this.weight = v;
    }
    
}

const newProfile = new Profile(23,23,434);
newProfile.setmyweight = 90;
console.log(newProfile.getmyheight);

```



### how to define a type

```ts
const arr : string[] = ['kaml','as','asf'];                                 // array of string - method -1
const arr : Array<string> = ['asdfsdf','sdfasf'];                           // array of string - method -2 
let num:(number | string)[] = ['asdf','asdf','sf',343];                     // array of string or number or both 
let num : Array<number | string> = [234,34,343 , 'sd' , 'sdf'];
```

### Rest operator
```ts
rest operator

const fun = (a:number , ...b:number[]):number => {
       console.log(b);
       return a;
}

fun(34,34,12,23,34,23,12,12,12,12,32,2323,2);
```





### Interface 

```ts
interface obj {
        firstname?: string,  // optional
        lastname ?: string,  // optional
        age:number,
        gender:string,
        salary: number | null ,     // salary could be number or null
        status : boolean
}

// note : interface ko extends kar sakthe hai.
```

```ts
interface newobj extends obj {

}
```
```ts
interface obj {
            firstname?: string,
            lastname ?: string,
            age:number    ,
            gender ?:string ,
            salary?: number | null ,
            status ?: boolean
}

type Funtype = (n : number , m : number ) => void   ;

interface newobj extends obj {
    scolor: boolean,
    fun : Funtype
}

const gigi : newobj = {
  scolor:true ,
  age:34,
  fun:(n, m) =>{
     console.log(n*m);
  }
}
```

### Type with arrow function  

```ts
type username = (n: number | string , m : number) => number;

const fun : username = (v,m) => {
 return 34;
}
fun('kamlesh',34)

```

### Type with normal function
```ts
type myType = (n : number , m : number) => number

const lol :myType   = function normalfunction ( n , m) {
      return n;
}

lol(3,4);
```


### Type with Object
```ts

type obj = {
    firstname:string,
    lastname :string ,
    age:number,
    statusmarriage:boolean,
}

const newobj:obj = {
    firstname: "mahesh",
    lastname: "kumar",
    age: 30,
    statusmarriage: false
}

```

### Tuple

```ts
tuple
let arr : [ number , number , number ] = [243.23 , 23.23 , 232.323 ];

```

### Function with Objects

```ts
type obj = {
    name : string , 
    stock : number , 
    price : number , 
    photo : string 
    readonly  id : string ,
}

const productOne  = (product : obj ) =>{
   console.log(product);
   console.log(product.name);
   console.log(product.stock);
}; 

productOne({
    name :'kamlesh',
    stock : 33,
    price: 343,
    photo : 'asdf',
    id : 'gjgjgj'
})
```

### Never type
```ts
never type


 const errorhandlerwithnevertype = () =>{  // never type
     throw new Error();
 }
 
 const  errorhandlerwitherrortype = () =>{  // error type
     return new Error(); 
 }


```
### Type Assertion

```ts
 Type assertion
 
first syntax
const a = document.getElementById('btn') as HTMLElement; recommended


second syntax
const b = <HTMLElement>document.getElementById('btn');

third syntax
const c = document.getElementById('btn')!;


const myform = document.querySelector('form')!;

```
