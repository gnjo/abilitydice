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

　難易度。
　新参：敵の生命力三割減。練成無し。三章まで。
　識者：練成無し。クリア後、新章登場。
  有段：練成有り。レベルキャップ有り。
　古残：敵の生命力五割増し。練成有り。
　練成無しは、一度クリアすると有りとなる。 
 
 アイテムは、名称八文字と練成記号六文字。で、様々に表す事ができる。
 練成記号が六文字あるものは、再度練成可能。英字のみ変更できる。
 抽出すれば、別のアイテムに練成できる。その場合は、抽出練成を同時に行う。
 抽出元のアイテムは消滅。但し、抽出練成を行う度に練成側の数字は最大５まで上がる。 
 *B3+A3 > *B3+A4
 素材一つと、三本まで入る。
```
```
生命力と魔法量は同じ。
全てのスキルコストは生命力で支払われる。レミナウス以外。
最大値の生命力依存。ランク１と５は支払えない場合は１でとどまるが、他のランクは使用できなくなる。
ランク１：３％、１止まり。
ランク２：４％、使用不可。
ランク３：５％、使用不可。
ランク４：７％、使用不可。
ランク５：３０％　蘇生等。１止まり。
```
Lev Str Ber Mag Vit Agi Quo and op1 op2
```
//stats table
Agi //Agillity
Ber //Berief
Cha //Charm issue, attack to alley by fifty.
Dar //Dark magic break
Exp //Expup
Fir //Fire magic break
Goo //Goodsup
HPs //Hitpoint
Ice //Ice magic break
Jud //Judgement magic break
Kee //Keep once life
Lev //Level
Mag //Magic
Nig //Nightmare issue, dont action, but aweken.
Ogr //Ogrelic issue, dont magic and strange up.
Poi //Poison issue, walk and turn the damage.
Quo //Quority dice
Rec //Recovery dot heal
Str //Strange
Thu //Thunder magic break
Unt //Untonic issue, dont attack by fifty.
Vit //Vitality
Woo //Woody issue, dont action never ever.
X //wepon damage base
Y //slash times
Z //dodge base
```
```
//-lica -lic -ca -li -c
//skill table
Agi //Agillitica
Bac //Backli back to the stair on floor
Cha //Charmlic heal
Dar //DarkMagic
Esc //Escapli
Fir //FireMagic
Gow //Goodwalkli
Hea //Healica
Ice //IceMagic
Jud //JudgementMagic 
Kin //Kindhealic heal status issue anyone of one.
Lev //Levelica base level up while battle
Mad //MagicDecli decreese to enemy
Nig //Nightmarlic heal
Ogr //Ogrelic heal
Poi //Poisolica heal
Que //Queeqli rate of kill
Rea //Realiveli reserve the reborn
Sla //Slashlic
Thu //ThunderMagic
Unt //Untonica heal
Vis //Visitalic
Woo //Woodlic heal
Xpo //Xpowli charge self
Yar //Yarnslashlic enemy slash times down
Zip //Zippli dodge base up
```

```
魔法職は、通常戦に有利。近接職は、ボス戦に有利。
スキルは五まで。マジックユーザは自身が詠唱可能なら二重詠唱となる。
1:FireMagic of once
2:FireMagic of twice
3:FireMagic of arrow
4:FireMagic of all
5:FireMagic of kor //kill or reborn
　単複列界特。種。
　火焔、氷爆、雷鳴。
　斬払、突払、壊払。
　睡夢、麻痺、暗黒。
　猛毒、畏怖、混乱。
　治癒、挑発、庇護。
　遠吠、警戒、脱兎。
　転移。
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

