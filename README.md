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

```
//dungeron script
//dungeron B00 - B99
#B01
{$nowfloor==="B01"}>>>#B01.loaded
{{{

}}}
map:{$$$}
title:flower graden 01
{{{
}}}
desc:{$$$}
//
side:aaa.png
face:bbb.png
ceiling:ccc.png
ground:ddd.png
//symbol 0 1 2 ...
0:b1wall.png
1:b1face.png
2:...
3:...
4:...
#B01.loaded
//event jump


{1}>>>#walk
```
