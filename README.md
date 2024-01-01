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
