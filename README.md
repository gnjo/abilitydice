# dice
```
　補正は、最大値加算制。蓄積されない。最大のもののみ適用。
　武具におけるネームドの位置づけ。体力上昇は装飾につく。
　記号と英数字で示す。*B3 +A3
　？？？：は未鑑定。武具名は判る。値段でもある程度判る。
　＋：基礎能力テーブルの補正。
　＊：スキルテーブルの補正。
　英字は、能力値補正の系統。
　練成は末尾に更に三文字つく。基礎能力のみ。*B3+A3

　末尾は武器なら攻撃回数。防具なら防御機会。装飾なら生命力増加。

　難易度。
　新参：敵の生命力三割減。練成無し。三章まで。
　識者：練成無し。クリア後、新章登場。
　古残：敵の生命力五割増し。練成有り。
　練成無しは、一度クリアすると有りとなる。
 
 
 アイテムは、名称八文字と練成記号六文字。で、様々に表す事ができる。
 練成記号が六文字あるものは、再度練成可能。英字のみ変更できる。
 抽出すれば、別のアイテムに練成できる。その場合は、抽出練成を同時に行う。
 抽出元のアイテムは消滅。但し、抽出練成を行う度に練成側の数字は最大九まで上がる。 
 *B3+A3 > *B3+A4
```
Lev Str Ber Mag Vit Agi Quo and op1 op2
```
//stats table
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
//skill table
A
B
C
D
E
F
G
H
I
J
K
L
M
N
O
P
Q
R
S
T
U
V
W
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

