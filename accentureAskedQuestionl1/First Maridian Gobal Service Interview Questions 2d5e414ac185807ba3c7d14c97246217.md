# First Maridian Gobal Service Interview Questions

1. const arr = [1, 2, 4, 5, 6]; // Range is 1 to 10  please find missing element from the array Without Javascript Predefined function

```
const arr = [1, 2, 4, 5, 6]

function findMissing(arr){
const present=[]
const missing=[]

for(var i=0;i<arr.length;i++){
   present[arr[i]]=true     // it will store [,true,true,,true,true,true]
}
for(var num=1;num<=10;num++){
    if(!present[num]){         // check 1 present[1 to 10] true become false and 
															    empty means undefine become true
        missing.push(num)
    }
}
return missinga
}

console.log(findMissing(arr))

```

1. behind the scene how this code will excute:-

let a=10

var b=10

const c=10

1. what are the Types of Error :-
    
    Syntax error :- 
    

1. difference between undefined and not defined 
2. what is callStack

---

### 1. Memory Creation Phase (Creation Phase / Hoisting Phase)

In this phase, JavaScript:

- Allocates memory for variables.
- Stores function declarations completely in memory.
- Sets up the scope chain and `this` keyword.

At this time:

- Variables are assigned memory.
- Function declarations are available before execution starts.

---

### 2. Execution Phase

In this phase, JavaScript:

- Executes the code line by line.
- Assigns actual values to variables.
- Executes function calls and creates new Function Execution Contexts when required.