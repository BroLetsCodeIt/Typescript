# Typescript
Typescript Concepts

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
