# Code Golfing

Le _code golfing_ est un challenge ayant pour but d'accomplir un résultat avec le moins de caractères possible, au mépris de toutes les bonnes pratiques.

Cette activité permet de découvrir les subtilités des langages et de mettre en valeur le bien-fondé des bonnes pratiques.

En attendant, que le plus court gagne !

Utilisez [cet outil](https://charactercounttool.com/) pour compter les caractères.

## JS

### 1) L'addition s'il-vous-plaît

Écrivez une fonction qui prend deux nombres en paramètre et qui retourne leur addition.

Exemple :

```
function sum(number1, number2) {
  return number1 + number2;
}
```

L'appel de la fonction ne fait pas partie du comptage. Le nom de la fonction peut être modifié.

#### Record - 12 caractères (plusieurs ex-aequo)

```
f=(a,b)=>a+b
```

### 2) C'est qui le patron ?

Écrivez une fonction qui prend deux nombres en paramètre et retourne le plus grand des deux.

Exemple :

```
function compare(number1, number2) {
  if (number1 > number2) {
    return number1;
  } else {
    return number2;
  }
}
```

#### Record - 16 caractères (plusieurs ex-aequo)

```
f=(a,b)=>a>b?a:b
```

### 3) Pierre feuille ciseaux

Écrivez une fonction qui prend en paramètre soit `pierre`, soit `feuille` soit `ciseaux` et qui renvoit la contre-attaque gagnante.

```
function fight(attack) {
  if (attack === 'pierre') {
    return 'feuille';
  } else if (attack === 'feuille') {
    return 'ciseaux';
  } else {
    return 'pierre';
  }
}
```

#### Record - 47 caractères (bcalou)

```
f=a=>({p:'feuille',c:'pierre',f:'ciseaux'}[a[0]])
```

### 4) On monte en puissance

Écrivez une fonction qui prend en paramètre un nombre n et qui donne les n premiers chiffres de la suite 1 2 4 8 16... sous forme de tableau.

Par exemple, `suite(6)` devra renvoyer `[1,2,4,8,16,32]`.

Exemple :

```
function suite(quantity) {
  let number = 1;
  const result = [];

  for(let i = 0; i < quantity; i++) {
    result.push(number);
    number = number * 2;
  }

  return result;
}
```

#### Challenger - 50 caractères (Jarce B)

```
s=q=>{n=1,r=[];while(q--&&r.push(n))n*=2;return r}
```

#### Record - 38 caractères (bcalou)

```
à venir !
```

### 5) Ça passe ou ça casse

Écrivez une fonction qui récupère un texte pour en extraire uniquement les majuscules.

Par exemple, `getCaps('HeLLo WOrlD')` devra renvoyer `HLLWOD`.

```
function getCaps(text) {
  let result = '';
  const caps = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';

  for (let i = 0; i < text.length; i++) {
    if (caps.indexOf(text[i]) >= 0) {
      result += text[i];
    }
  }

  return result;
}
```

#### Record sans expression régulière - 48 caractères (Nawel B & Quentin G)

```
g=s=>s.split("").filter(c=>c<{}?c!=0:0).join("")
```

#### Record avec expression régulière - 29 caractères (Bastien P, ex-aequo bcalou)

```
s=t=>t.replace(/[a-z\s]/g,'')
```
