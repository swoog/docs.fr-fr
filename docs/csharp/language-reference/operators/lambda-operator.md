---
title: =&gt;, opérateur (Informations de référence sur C#)
ms.date: 10/02/2017
f1_keywords:
- =>_CSharpKeyword
helpviewer_keywords:
- lambda operator [C#]
- => operator [C#]
- lambda expressions [C#], => operator
ms.openlocfilehash: d1565e262fbd3ebcee2d1576a2a0c8ed3ba8ce38
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="gt-operator-c-reference"></a>=&gt;, opérateur (Informations de référence sur C#)

L’opérateur `=>` peut être utilisé de deux façons en C# :

- Comme [l’opérateur lambda](#lamba-operator) dans une [expression lambda](../../lambda-expressions.md), il sépare les variables d’entrée du corps du lambda.
 
- Dans une [définition de corps d’expression](#expression-body-definition), il sépare un nom de membre de l’implémentation du membre. 

## <a name="lambda-operator"></a>Opérateur lamdba

Le jeton `=>` est appelé opérateur lambda. Il est utilisé dans les *expressions lambda* pour séparer les variables d’entrée du côté gauche et le corps lambda du côté droit. Les expressions lambda sont des expressions inline similaires aux méthodes anonymes, mais plus flexibles ; elles sont largement utilisées dans les requêtes LINQ qui sont exprimées dans la syntaxe des méthodes. Pour plus d’informations, consultez [Expressions lambda](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md).  
  
 L’exemple suivant montre deux façons de rechercher et d’afficher la longueur de la chaîne la plus courte dans un tableau de chaînes. La première partie de l’exemple applique une expression lambda (`w => w.Length`) à chaque élément du tableau `words`, puis utilise la méthode <xref:System.Linq.Enumerable.Min%2A> pour rechercher la plus petite longueur. À titre de comparaison, la deuxième partie de l’exemple montre une solution plus longue qui utilise la syntaxe de requête à faire la même chose.  
  
```csharp  
string[] words = { "cherry", "apple", "blueberry" };  
  
// Use method syntax to apply a lambda expression to each element  
// of the words array.   
int shortestWordLength = words.Min(w => w.Length);  
Console.WriteLine(shortestWordLength);  
  
// Compare the following code that uses query syntax.  
// Get the lengths of each word in the words array.  
var query = from w in words  
            select w.Length;  
// Apply the Min method to execute the query and get the shortest length.  
int shortestWordLength2 = query.Min();  
Console.WriteLine(shortestWordLength2);  
  
// Output:   
// 5  
// 5  
```  
  
### <a name="remarks"></a>Notes  
 L’opérateur `=>` a la même priorité que l’opérateur d’affectation (`=`) et est associatif à droite.  
  
 Vous pouvez spécifier explicitement le type de la variable d’entrée ou laisser le compilateur l’inférer. Dans les deux cas, la variable est fortement typée à la compilation. Quand vous spécifiez un type, vous devez placer le nom de type et le nom de la variable entre parenthèses, comme le montre l’exemple suivant.  
  
```csharp  
int shortestWordLength = words.Min((string w) => w.Length);  
```  
  
### <a name="example"></a>Exemple  
 L’exemple suivant montre comment écrire une expression lambda pour la surcharge de l’opérateur de requête standard <xref:System.Linq.Enumerable.Where%2A?displayProperty=nameWithType>, qui prend deux arguments. Comme l’expression lambda a plusieurs paramètres, les paramètres doivent être placés entre parenthèses. Le deuxième paramètre, `index`, représente l’index de l’élément actif dans la collection. L’expression `Where` retourne toutes les chaînes dont les longueurs sont inférieures à leurs emplacements d’index dans le tableau.  
  
```csharp  
static void Main(string[] args)  
{  
    string[] digits = { "zero", "one", "two", "three", "four", "five",   
            "six", "seven", "eight", "nine" };  
  
    Console.WriteLine("Example that uses a lambda expression:");  
    var shortDigits = digits.Where((digit, index) => digit.Length < index);  
    foreach (var sD in shortDigits)  
    {  
        Console.WriteLine(sD);  
    }  
  
    // Output:  
    // Example that uses a lambda expression:  
    // five  
    // six  
    // seven  
    // eight  
    // nine  
}  
```  
## <a name="expression-body-definition"></a>Définition de corps d’expression

Une définition de corps d’expression fournit l’implémentation d’un membre sous une forme très concise et lisible. Elle a la syntaxe générale suivante :

```csharp
member => expression;
```
où *expression* est une expression valide. Notez que *expression* peut être une *expression d’instruction* seulement si le type de retour du membre est `void`, ou si le membre est un constructeur ou un finaliseur.

Les définitions de corps d’expression pour les méthodes et les instructions Get de propriété sont prises en charge à compter de C# 6. Les définitions de corps d’expression pour les constructeurs, les finaliseurs, les instructions Set de propriété et les indexeurs sont prises en charge à compter de C# 7.

Voici une définition de corps d’expression pour une méthode `Person.ToString` :

```csharp
public override string ToString() => $"{fname} {lname}".Trim();
```

Il s’agit d’une version raccourcie de la définition de méthode suivante :

```csharp
public override string ToString()
{
   return $"{fname} {lname}".Trim();
}
```
Pour plus d’informations sur les définitions de corps d’expression, consultez [Membres expression-bodied](../../programming-guide/statements-expressions-operators/expression-bodied-members.md).

## <a name="see-also"></a>Voir aussi  
[Référence du langage C#](../../../csharp/language-reference/index.md)   
[Guide de programmation C#](../../../csharp/programming-guide/index.md)   
[Expressions lambda](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md)   
[Membres expression-bodied](../../programming-guide/statements-expressions-operators/expression-bodied-members.md).