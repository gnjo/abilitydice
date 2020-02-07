# dice
lv str pie mag vit agi luc and op1 op2

```
dice(rand)
.dmg('str,pie',me,tar)
.flg('luc',me,tar,times) //if time +,flg||flg. if time -,flg&&flg
.drop('luc',me,tar,table) //table of one.

```

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

