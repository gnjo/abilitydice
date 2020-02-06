# abilitydice
str pie mag vit agi luc and op1 op2

```
let b=a={str,pie,mag,vit,agi,luc,op1,op2}...
let rand=xrand(Date.now())
flgdice('str',a,b,rand)

function flgdice(name,me,tar,rand){
 let num=100+(me-tar)
 return (rand(1,num)>50)
}
```
