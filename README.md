# dice
Lev Str Ber Mag Vit Agi Quo and op1 op2

```
Agi //Agillity
Ber //Berief
Che //Charm issue, attack to alley by fifty.
Dar //Dark magic
Exp //Expup
Fir //Fire magic
Goo //Goodsup
HPs //Hitpoint
Ice //Ice magic
Jud //Judgement magic
Kee //Keep once life
Lev //Level
Mag //Magic
Nig //Nightmare issue, dont action, but aweken.
Ogr //Ogreed issue, dont magic and strange up.
Poi //Poison issue, walk and turn the damage.
Quo //Quority dice
Rec //Recovery dot keep
Str //Strange
Thu //Thunder
Unt //Untonic issue, dont attack by fifty.
Vit //Vitality
Woo //Woody issue, dont action never ever.
X //wepon damage base
Y //slash times
Z //dodge base
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

