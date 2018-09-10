---
title: =&gt;, opérateur (Informations de référence sur C#)
ms.date: 10/02/2017
f1_keywords:
- =>_CSharpKeyword
helpviewer_keywords:
- lambda operator [C#]
- => operator [C#]
- lambda expressions [C#], => operator
ms.openlocfilehash: b9216cf61b6b9368112f769d952457df4aab4297
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44183299"
---
# <a name="gt-operator-c-reference"></a><span data-ttu-id="df231-102">=&gt;, opérateur (Informations de référence sur C#)</span><span class="sxs-lookup"><span data-stu-id="df231-102">=&gt; Operator (C# Reference)</span></span>

<span data-ttu-id="df231-103">L’opérateur `=>` peut être utilisé de deux façons en C# :</span><span class="sxs-lookup"><span data-stu-id="df231-103">The `=>` operator can be used in two ways in C#:</span></span>

- <span data-ttu-id="df231-104">Comme [l’opérateur lambda](#lamba-operator) dans une [expression lambda](../../lambda-expressions.md), il sépare les variables d’entrée du corps du lambda.</span><span class="sxs-lookup"><span data-stu-id="df231-104">As the [lambda operator](#lamba-operator) in a [lambda expression](../../lambda-expressions.md), it separates the input variables from the lambda body.</span></span>
 
- <span data-ttu-id="df231-105">Dans une [définition de corps d’expression](#expression-body-definition), il sépare un nom de membre de l’implémentation du membre.</span><span class="sxs-lookup"><span data-stu-id="df231-105">In an [expression body definition](#expression-body-definition), it separates a member name from the member implementation.</span></span> 

## <a name="lambda-operator"></a><span data-ttu-id="df231-106">Opérateur lamdba</span><span class="sxs-lookup"><span data-stu-id="df231-106">Lambda operator</span></span>

<span data-ttu-id="df231-107">Le jeton `=>` est appelé opérateur lambda.</span><span class="sxs-lookup"><span data-stu-id="df231-107">The `=>` token is called the lambda operator.</span></span> <span data-ttu-id="df231-108">Il est utilisé dans les *expressions lambda* pour séparer les variables d’entrée du côté gauche et le corps lambda du côté droit.</span><span class="sxs-lookup"><span data-stu-id="df231-108">It is used in *lambda expressions* to separate the input variables on the left side from the lambda body on the right side.</span></span> <span data-ttu-id="df231-109">Les expressions lambda sont des expressions inline similaires aux méthodes anonymes, mais plus flexibles ; elles sont largement utilisées dans les requêtes LINQ qui sont exprimées dans la syntaxe des méthodes.</span><span class="sxs-lookup"><span data-stu-id="df231-109">Lambda expressions are inline expressions similar to anonymous methods but more flexible; they are used extensively in LINQ queries that are expressed in method syntax.</span></span> <span data-ttu-id="df231-110">Pour plus d’informations, consultez [Expressions lambda](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="df231-110">For more information, see [Lambda Expressions](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md).</span></span>  
  
 <span data-ttu-id="df231-111">L’exemple suivant montre deux façons de rechercher et d’afficher la longueur de la chaîne la plus courte dans un tableau de chaînes.</span><span class="sxs-lookup"><span data-stu-id="df231-111">The following example shows two ways to find and display the length of the shortest string in an array of strings.</span></span> <span data-ttu-id="df231-112">La première partie de l’exemple applique une expression lambda (`w => w.Length`) à chaque élément du tableau `words`, puis utilise la méthode <xref:System.Linq.Enumerable.Min%2A> pour rechercher la plus petite longueur.</span><span class="sxs-lookup"><span data-stu-id="df231-112">The first part of the example applies a lambda expression (`w => w.Length`) to each element of the `words` array and then uses the <xref:System.Linq.Enumerable.Min%2A> method to find the smallest length.</span></span> <span data-ttu-id="df231-113">À titre de comparaison, la deuxième partie de l’exemple montre une solution plus longue qui utilise la syntaxe de requête à faire la même chose.</span><span class="sxs-lookup"><span data-stu-id="df231-113">For comparison, the second part of the example shows a longer solution that uses query syntax to do the same thing.</span></span>  
  
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
  
### <a name="remarks"></a><span data-ttu-id="df231-114">Notes</span><span class="sxs-lookup"><span data-stu-id="df231-114">Remarks</span></span>  
 <span data-ttu-id="df231-115">L’opérateur `=>` a la même priorité que l’opérateur d’affectation (`=`) et est associatif à droite.</span><span class="sxs-lookup"><span data-stu-id="df231-115">The `=>` operator has the same precedence as the assignment operator (`=`) and is right-associative.</span></span>  
  
 <span data-ttu-id="df231-116">Vous pouvez spécifier explicitement le type de la variable d’entrée ou laisser le compilateur l’inférer. Dans les deux cas, la variable est fortement typée à la compilation.</span><span class="sxs-lookup"><span data-stu-id="df231-116">You can specify the type of the input variable explicitly or let the compiler infer it; in either case, the variable is strongly typed at compile time.</span></span> <span data-ttu-id="df231-117">Quand vous spécifiez un type, vous devez placer le nom de type et le nom de la variable entre parenthèses, comme le montre l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="df231-117">When you specify a type, you must enclose the type name and the variable name in parentheses, as the following example shows.</span></span>  
  
```csharp  
int shortestWordLength = words.Min((string w) => w.Length);  
```  
  
### <a name="example"></a><span data-ttu-id="df231-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="df231-118">Example</span></span>  
 <span data-ttu-id="df231-119">L’exemple suivant montre comment écrire une expression lambda pour la surcharge de l’opérateur de requête standard <xref:System.Linq.Enumerable.Where%2A?displayProperty=nameWithType>, qui prend deux arguments.</span><span class="sxs-lookup"><span data-stu-id="df231-119">The following example shows how to write a lambda expression for the overload of the standard query operator <xref:System.Linq.Enumerable.Where%2A?displayProperty=nameWithType> that takes two arguments.</span></span> <span data-ttu-id="df231-120">Comme l’expression lambda a plusieurs paramètres, les paramètres doivent être placés entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="df231-120">Because the lambda expression has more than one parameter, the parameters must be enclosed in parentheses.</span></span> <span data-ttu-id="df231-121">Le deuxième paramètre, `index`, représente l’index de l’élément actif dans la collection.</span><span class="sxs-lookup"><span data-stu-id="df231-121">The second parameter, `index`, represents the index of the current element in the collection.</span></span> <span data-ttu-id="df231-122">L’expression `Where` retourne toutes les chaînes dont les longueurs sont inférieures à leurs emplacements d’index dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="df231-122">The `Where` expression returns all the strings whose lengths are less than their index positions in the array.</span></span>  
  
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
## <a name="expression-body-definition"></a><span data-ttu-id="df231-123">Définition de corps d’expression</span><span class="sxs-lookup"><span data-stu-id="df231-123">Expression body definition</span></span>

<span data-ttu-id="df231-124">Une définition de corps d’expression fournit l’implémentation d’un membre sous une forme très concise et lisible.</span><span class="sxs-lookup"><span data-stu-id="df231-124">An expression body definition provides a member's implementation in a highly condensed, readable form.</span></span> <span data-ttu-id="df231-125">Elle a la syntaxe générale suivante :</span><span class="sxs-lookup"><span data-stu-id="df231-125">It has the following general syntax:</span></span>

```csharp
member => expression;
```
<span data-ttu-id="df231-126">où *expression* est une expression valide.</span><span class="sxs-lookup"><span data-stu-id="df231-126">where *expression* is a valid expression.</span></span> <span data-ttu-id="df231-127">Notez que *expression* peut être une *expression d’instruction* seulement si le type de retour du membre est `void`, ou si le membre est un constructeur ou un finaliseur.</span><span class="sxs-lookup"><span data-stu-id="df231-127">Note that *expression* can be a *statement expression* only if the member's return type is `void`, or if the member is a constructor or a finalizer.</span></span>

<span data-ttu-id="df231-128">Les définitions de corps d’expression pour les méthodes et les instructions Get de propriété sont prises en charge à compter de C# 6.</span><span class="sxs-lookup"><span data-stu-id="df231-128">Expression body definitions for methods and property get statements are supported starting with C# 6.</span></span> <span data-ttu-id="df231-129">Les définitions de corps d’expression pour les constructeurs, les finaliseurs, les instructions Set de propriété et les indexeurs sont prises en charge à compter de C# 7.</span><span class="sxs-lookup"><span data-stu-id="df231-129">Expression body definitions for constructors, finalizers, property set statements, and indexers are supported starting with C# 7.</span></span>

<span data-ttu-id="df231-130">Voici une définition de corps d’expression pour une méthode `Person.ToString` :</span><span class="sxs-lookup"><span data-stu-id="df231-130">The following is an expression body definition for a `Person.ToString` method:</span></span>

```csharp
public override string ToString() => $"{fname} {lname}".Trim();
```

<span data-ttu-id="df231-131">Il s’agit d’une version raccourcie de la définition de méthode suivante :</span><span class="sxs-lookup"><span data-stu-id="df231-131">It is a shorthand version of the following method definition:</span></span>

```csharp
public override string ToString()
{
   return $"{fname} {lname}".Trim();
}
```
<span data-ttu-id="df231-132">Pour plus d’informations sur les définitions de corps d’expression, consultez [Membres expression-bodied](../../programming-guide/statements-expressions-operators/expression-bodied-members.md).</span><span class="sxs-lookup"><span data-stu-id="df231-132">For more detailed information on expression body definitions, see [Expression-bodied members](../../programming-guide/statements-expressions-operators/expression-bodied-members.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="df231-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df231-133">See Also</span></span>

- [<span data-ttu-id="df231-134">Référence C#</span><span class="sxs-lookup"><span data-stu-id="df231-134">C# Reference</span></span>](../../../csharp/language-reference/index.md)   
- [<span data-ttu-id="df231-135">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="df231-135">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)   
- [<span data-ttu-id="df231-136">Expressions lambda</span><span class="sxs-lookup"><span data-stu-id="df231-136">Lambda Expressions</span></span>](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md)   
- <span data-ttu-id="df231-137">[Membres expression-bodied](../../programming-guide/statements-expressions-operators/expression-bodied-members.md).</span><span class="sxs-lookup"><span data-stu-id="df231-137">[Expression-bodied members](../../programming-guide/statements-expressions-operators/expression-bodied-members.md).</span></span>