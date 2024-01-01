# Typescript
Typescript Concepts

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

### Type with function

```ts
type username = (n: number | string , m : number) => number;

const fun : username = (v,m) => {
 return 34;
}
fun('kamlesh',34)

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
