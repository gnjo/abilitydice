# dice
Lv Str Ber Mag Vit Agi Luc and op1 op2

```
Agi
Ber //Berief
Che //Charm
Dar //Dark
Exp //Expup
Fir //Fire
Goo //Goodsup
Hol //Holy
Ice
//J
Kee //Keep once life
Luc //Luc
Mag //Magic
Nig //Nightmare
Ogr //Ogreed
Poi //Poison
Quo //Quority Level
Rec //Recovery dot keep
Str 
Thu //Thunder
Unt //Untonic
Vit
Woo
//X
//Y
//Z
```
```

//dlv+dstat*2

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

