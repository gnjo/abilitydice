# abilitydice
str pie mag vit agi luc and op1 op2

```
let b=a={str,pie,mag,vit,agi,luc,op1,op2}...
let rand=xrand(Date.now())
flgdice('str',a,b,rand)

function flgdice(name,me,tar,rand){
 let a=(me)?me[name]||0:0,b=(tar)?tar[name]||0:0
 let num=100+(a-b)
 return (rand(1,num)>50)
}
```

