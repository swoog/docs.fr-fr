---
title: for (référence C#)
ms.date: 07/20/2015
f1_keywords:
- for
- for_CSharpKeyword
helpviewer_keywords:
- for keyword [C#]
ms.assetid: 34041a40-2c87-467a-9ffb-a0417d8f67a8
ms.openlocfilehash: 2c099411499c6ca8396c55955bdc634e48caf621
ms.sourcegitcommit: 22c3c8f74eaa138dbbbb02eb7d720fce87fc30a9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/18/2018
---
# <a name="for-c-reference"></a><span data-ttu-id="095dd-102">for (référence C#)</span><span class="sxs-lookup"><span data-stu-id="095dd-102">for (C# reference)</span></span>

<span data-ttu-id="095dd-103">En utilisant une boucle `for`, vous pouvez exécuter une instruction ou un bloc d’instructions de manière répétée jusqu'à ce qu’une expression spécifiée corresponde à `false`.</span><span class="sxs-lookup"><span data-stu-id="095dd-103">By using a `for` loop, you can run a statement or a block of statements repeatedly until a specified expression evaluates to `false`.</span></span> <span data-ttu-id="095dd-104">Ce type de boucle est utile pour itérer des tableaux et d’autres applications pour lesquelles vous savez à l’avance combien de fois vous souhaitez effectuer une itération.</span><span class="sxs-lookup"><span data-stu-id="095dd-104">This kind of loop is useful for iterating over arrays and for other applications in which you know in advance how many times you want the loop to iterate.</span></span>
  
## <a name="example"></a><span data-ttu-id="095dd-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="095dd-105">Example</span></span>

<span data-ttu-id="095dd-106">Dans l’exemple suivant, la valeur de `i` est écrite dans la console et incrémentée de 1 à chaque itération de la boucle :</span><span class="sxs-lookup"><span data-stu-id="095dd-106">In the following example, the value of `i` is written to the console and incremented by 1 during each iteration of the loop:</span></span>
  
[!code-csharp[csrefKeywordsIteration#2](../../../csharp/language-reference/keywords/codesnippet/CSharp/for_1.cs)]
  
<span data-ttu-id="095dd-107">L’[instruction for](/dotnet/csharp/language-reference/language-specification/statements#the-for-statement) de l’exemple précédent effectue les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="095dd-107">The [for statement](/dotnet/csharp/language-reference/language-specification/statements#the-for-statement) in the previous example performs the following actions:</span></span>
  
1.  <span data-ttu-id="095dd-108">Tout d’abord, la valeur initiale de la variable `i` est établie.</span><span class="sxs-lookup"><span data-stu-id="095dd-108">First, the initial value of variable `i` is established.</span></span> <span data-ttu-id="095dd-109">Cette étape se produit une seule fois, quel que soit le nombre d’itérations de la boucle.</span><span class="sxs-lookup"><span data-stu-id="095dd-109">This step happens only once, regardless of how many times the loop repeats.</span></span> <span data-ttu-id="095dd-110">Vous pouvez considérer cette initialisation comme survenant en dehors du processus de boucle.</span><span class="sxs-lookup"><span data-stu-id="095dd-110">You can think of this initialization as happening outside the looping process.</span></span>
  
2.  <span data-ttu-id="095dd-111">Pour évaluer la condition (`i <= 5`), la valeur de `i` est comparée à 5.</span><span class="sxs-lookup"><span data-stu-id="095dd-111">To evaluate the condition (`i <= 5`), the value of `i` is compared to 5.</span></span>
  
    -   <span data-ttu-id="095dd-112">Si `i` est inférieur ou égal à 5, la condition prend la valeur `true`, et les actions suivantes se produisent.</span><span class="sxs-lookup"><span data-stu-id="095dd-112">If `i` is less than or equal to 5, the condition evaluates to `true`, and the following actions occur.</span></span>  
  
        1.  <span data-ttu-id="095dd-113">L’instruction `Console.WriteLine` dans le corps de la boucle affiche la valeur de `i`.</span><span class="sxs-lookup"><span data-stu-id="095dd-113">The `Console.WriteLine` statement in the body of the loop displays the value of `i`.</span></span>  
  
        2.  <span data-ttu-id="095dd-114">La valeur de `i` incrémentée de 1.</span><span class="sxs-lookup"><span data-stu-id="095dd-114">The value of `i` is incremented by 1.</span></span>  
  
        3.  <span data-ttu-id="095dd-115">La boucle retourne au début de l’étape 2 pour évaluer de nouveau la condition.</span><span class="sxs-lookup"><span data-stu-id="095dd-115">The loop returns to the start of step 2 to evaluate the condition again.</span></span>  
  
    -   <span data-ttu-id="095dd-116">Si `i` est supérieur à 5, la condition prend la valeur `false`, et vous quittez la boucle.</span><span class="sxs-lookup"><span data-stu-id="095dd-116">If `i` is greater than 5, the condition evaluates to `false`, and you exit the loop.</span></span>  
  
<span data-ttu-id="095dd-117">Notez que, si la valeur initiale de `i` est supérieure à 5, le corps de la boucle n’est jamais exécuté.</span><span class="sxs-lookup"><span data-stu-id="095dd-117">Note that, if the initial value of `i` is greater than 5, the body of the loop doesn't run even once.</span></span>

## <a name="sections-of-a-for-statement"></a><span data-ttu-id="095dd-118">Sections d’une instruction for</span><span class="sxs-lookup"><span data-stu-id="095dd-118">Sections of a for statement</span></span>
  
<span data-ttu-id="095dd-119">Chaque [instruction for](/dotnet/csharp/language-reference/language-specification/statements#the-for-statement) définit les sections *Initialiseur*, *Condition* et *Itérateur*.</span><span class="sxs-lookup"><span data-stu-id="095dd-119">Every [for statement](/dotnet/csharp/language-reference/language-specification/statements#the-for-statement) defines *initializer*, *condition*, and *iterator* sections.</span></span> <span data-ttu-id="095dd-120">Ces sections déterminent généralement le nombre d’itérations de la boucle.</span><span class="sxs-lookup"><span data-stu-id="095dd-120">These sections usually determine how many times the loop iterates.</span></span>  
  
```csharp  
for (initializer; condition; iterator)  
    body  
```  
  
<span data-ttu-id="095dd-121">Ces sections répondent aux objectifs suivants :</span><span class="sxs-lookup"><span data-stu-id="095dd-121">The sections serve the following purposes:</span></span>
  
-   <span data-ttu-id="095dd-122">La section Initialiseur définit les conditions initiales.</span><span class="sxs-lookup"><span data-stu-id="095dd-122">The initializer section sets the initial conditions.</span></span> <span data-ttu-id="095dd-123">Les instructions de cette section ne sont exécutées qu’une seule fois, avant l’entrée dans la boucle.</span><span class="sxs-lookup"><span data-stu-id="095dd-123">The statements in this section run only once, before you enter the loop.</span></span> <span data-ttu-id="095dd-124">La section peut contenir uniquement l’une des deux options suivantes.</span><span class="sxs-lookup"><span data-stu-id="095dd-124">The section can contain only one of the following two options.</span></span>  
  
    -   <span data-ttu-id="095dd-125">La déclaration et l’initialisation d’une variable de boucle locale, comme le montre le premier exemple (`int i = 1`).</span><span class="sxs-lookup"><span data-stu-id="095dd-125">The declaration and initialization of a local loop variable, as the first example shows (`int i = 1`).</span></span> <span data-ttu-id="095dd-126">La variable se trouve dans la boucle et n’est pas accessible en dehors de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="095dd-126">The variable is local to the loop and can't be accessed from outside the loop.</span></span>  
  
    -   <span data-ttu-id="095dd-127">Zéro ou plusieurs expressions d’instruction de la liste suivante, séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="095dd-127">Zero or more statement expressons from the following list, separated by commas.</span></span>  
  
        -   <span data-ttu-id="095dd-128">Instruction d’[assignation](../../../csharp/language-reference/operators/assignment-operator.md)</span><span class="sxs-lookup"><span data-stu-id="095dd-128">[assignment](../../../csharp/language-reference/operators/assignment-operator.md) statement</span></span>  
  
        -   <span data-ttu-id="095dd-129">Appel d’une méthode</span><span class="sxs-lookup"><span data-stu-id="095dd-129">invocation of a method</span></span>  
  
        -   <span data-ttu-id="095dd-130">Expression d’[incrémentation](../../../csharp/language-reference/operators/increment-operator.md) préfixée ou suffixée, telle que `++i` ou `i++`</span><span class="sxs-lookup"><span data-stu-id="095dd-130">prefix or postfix [increment](../../../csharp/language-reference/operators/increment-operator.md) expression, such as `++i` or `i++`</span></span>  
  
        -   <span data-ttu-id="095dd-131">Expression de [décrémentation](../../../csharp/language-reference/operators/decrement-operator.md) préfixée ou suffixée, telle que `--i` ou `i--`</span><span class="sxs-lookup"><span data-stu-id="095dd-131">prefix or postfix [decrement](../../../csharp/language-reference/operators/decrement-operator.md) expression, such as `--i` or `i--`</span></span>  
  
        -   <span data-ttu-id="095dd-132">Création d’un objet à l’aide de [new](../../../csharp/language-reference/keywords/new-operator.md)</span><span class="sxs-lookup"><span data-stu-id="095dd-132">creation of an object by using [new](../../../csharp/language-reference/keywords/new-operator.md)</span></span>  
  
        -   <span data-ttu-id="095dd-133">Expression [await](../../../csharp/language-reference/keywords/await.md)</span><span class="sxs-lookup"><span data-stu-id="095dd-133">[await](../../../csharp/language-reference/keywords/await.md) expression</span></span>  
  
-   <span data-ttu-id="095dd-134">La section Condition contient une expression booléenne qui est évaluée pour déterminer si la boucle doit s’arrêter ou s’exécuter de nouveau.</span><span class="sxs-lookup"><span data-stu-id="095dd-134">The condition section contains a boolean expression that’s evaluated to determine whether the loop should exit or should run again.</span></span>  
  
-   <span data-ttu-id="095dd-135">La section Itérateur définit ce qui se produit après chaque itération du corps de la boucle.</span><span class="sxs-lookup"><span data-stu-id="095dd-135">The iterator section defines what happens after each iteration of the body of the loop.</span></span> <span data-ttu-id="095dd-136">La section Itérateur contient zéro ou plusieurs des expressions d’instruction suivantes, séparées par des virgules :</span><span class="sxs-lookup"><span data-stu-id="095dd-136">The iterator section contains zero or more of the following statement expressions, separated by commas:</span></span>  
  
    -   <span data-ttu-id="095dd-137">Instruction d’[assignation](../../../csharp/language-reference/operators/assignment-operator.md)</span><span class="sxs-lookup"><span data-stu-id="095dd-137">[assignment](../../../csharp/language-reference/operators/assignment-operator.md) statement</span></span>  
  
    -   <span data-ttu-id="095dd-138">Appel d’une méthode</span><span class="sxs-lookup"><span data-stu-id="095dd-138">invocation of a method</span></span>  
  
    -   <span data-ttu-id="095dd-139">Expression d’[incrémentation](../../../csharp/language-reference/operators/increment-operator.md) préfixée ou suffixée, telle que `++i` ou `i++`</span><span class="sxs-lookup"><span data-stu-id="095dd-139">prefix or postfix [increment](../../../csharp/language-reference/operators/increment-operator.md) expression, such as `++i` or `i++`</span></span>  
  
    -   <span data-ttu-id="095dd-140">Expression de [décrémentation](../../../csharp/language-reference/operators/decrement-operator.md) préfixée ou suffixée, telle que `--i` ou `i--`</span><span class="sxs-lookup"><span data-stu-id="095dd-140">prefix or postfix [decrement](../../../csharp/language-reference/operators/decrement-operator.md) expression, such as `--i` or `i--`</span></span>  
  
    -   <span data-ttu-id="095dd-141">Création d’un objet à l’aide de [new](../../../csharp/language-reference/keywords/new-operator.md)</span><span class="sxs-lookup"><span data-stu-id="095dd-141">creation of an object by using [new](../../../csharp/language-reference/keywords/new-operator.md)</span></span>  
  
    -   <span data-ttu-id="095dd-142">Expression [await](../../../csharp/language-reference/keywords/await.md)</span><span class="sxs-lookup"><span data-stu-id="095dd-142">[await](../../../csharp/language-reference/keywords/await.md) expression</span></span>  
  
-   <span data-ttu-id="095dd-143">Le corps de la boucle se compose d’une instruction, d’une instruction vide ou d’un bloc d’instructions que vous créez en plaçant zéro ou plusieurs instructions entre accolades.</span><span class="sxs-lookup"><span data-stu-id="095dd-143">The body of the loop consists of a statement, an empty statement, or a block of statements, which you create by enclosing zero or more statements in braces.</span></span>  
  
     <span data-ttu-id="095dd-144">Vous pouvez quitter une boucle `for` à l’aide du mot clé [break](../../../csharp/language-reference/keywords/break.md), ou passer à l’itération suivante de la boucle à l’aide du mot clé [continue](../../../csharp/language-reference/keywords/continue.md).</span><span class="sxs-lookup"><span data-stu-id="095dd-144">You can break out of a `for` loop by using the [break](../../../csharp/language-reference/keywords/break.md) keyword, or you can step to the next iteration by using the [continue](../../../csharp/language-reference/keywords/continue.md) keyword.</span></span> <span data-ttu-id="095dd-145">Vous pouvez quitter une boucle en utilisant une instruction [goto](../../../csharp/language-reference/keywords/goto.md), [return](../../../csharp/language-reference/keywords/return.md) ou [throw](../../../csharp/language-reference/keywords/throw.md).</span><span class="sxs-lookup"><span data-stu-id="095dd-145">You also can exit any loop by using a [goto](../../../csharp/language-reference/keywords/goto.md), [return](../../../csharp/language-reference/keywords/return.md), or [throw](../../../csharp/language-reference/keywords/throw.md) statement.</span></span>  
  
<span data-ttu-id="095dd-146">Le premier exemple de cette rubrique montre le type de boucle `for` le plus courant, qui fait les choix suivants au niveau des sections :</span><span class="sxs-lookup"><span data-stu-id="095dd-146">The first example in this topic shows the most typical kind of `for` loop, which makes the following choices for the sections:</span></span>
  
-   <span data-ttu-id="095dd-147">L’initialiseur déclare et initialise une variable de boucle locale, `i`, qui compte le nombre d’itérations de la boucle.</span><span class="sxs-lookup"><span data-stu-id="095dd-147">The initializer declares and initializes a local loop variable, `i`, that maintains a count of the iterations of the loop.</span></span>  
  
-   <span data-ttu-id="095dd-148">La condition compare la valeur de la variable de boucle par rapport à la valeur finale connue de 5.</span><span class="sxs-lookup"><span data-stu-id="095dd-148">The condition checks the value of the loop variable against a known final value, 5.</span></span>  
  
-   <span data-ttu-id="095dd-149">La section Itérateur utilise une instruction d’incrémentation suffixée, `i++`, pour calculer chaque itération de la boucle.</span><span class="sxs-lookup"><span data-stu-id="095dd-149">The iterator section uses a postfix increment statement, `i++`, to tally each iteration of the loop.</span></span>

## <a name="more-examples"></a><span data-ttu-id="095dd-150">Autres exemples</span><span class="sxs-lookup"><span data-stu-id="095dd-150">More examples</span></span>
  
<span data-ttu-id="095dd-151">L’exemple suivant montre plusieurs choix moins courants : l’attribution d’une valeur à une variable de boucle externe dans la section Initialiseur, l’appel de la méthode `Console.WriteLine` dans les sections Initialiseur et Itérateur, et la modification des valeurs de deux variables dans la section Itérateur.</span><span class="sxs-lookup"><span data-stu-id="095dd-151">The following example illustrates several less common choices: assigning a value to an external loop variable in the initializer section, invoking the `Console.WriteLine` method in both the initializer and the iterator sections, and changing the values of two variables in the iterator section.</span></span>
  
[!code-csharp[csrefKeywordsIteration#8](../../../csharp/language-reference/keywords/codesnippet/CSharp/for_2.cs)]  
  
<span data-ttu-id="095dd-152">Toutes les expressions qui définissent une instruction `for` sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="095dd-152">All of the expressions that define a `for` statement are optional.</span></span> <span data-ttu-id="095dd-153">Par exemple, l’instruction suivante crée une boucle infinie :</span><span class="sxs-lookup"><span data-stu-id="095dd-153">For example, the following statement creates an infinite loop:</span></span>
  
[!code-csharp[csrefKeywordsIteration#3](../../../csharp/language-reference/keywords/codesnippet/CSharp/for_3.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="095dd-154">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="095dd-154">C# language specification</span></span>  

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]
  
## <a name="see-also"></a><span data-ttu-id="095dd-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="095dd-155">See also</span></span>

[<span data-ttu-id="095dd-156">L’instruction for (spécification du langage C#)</span><span class="sxs-lookup"><span data-stu-id="095dd-156">The for statement (C# language specification)</span></span>](/dotnet/csharp/language-reference/language-specification/statements#the-for-statement)  
[<span data-ttu-id="095dd-157">Référence C#</span><span class="sxs-lookup"><span data-stu-id="095dd-157">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
[<span data-ttu-id="095dd-158">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="095dd-158">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
[<span data-ttu-id="095dd-159">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="095dd-159">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
[<span data-ttu-id="095dd-160">foreach, in</span><span class="sxs-lookup"><span data-stu-id="095dd-160">foreach, in</span></span>](../../../csharp/language-reference/keywords/foreach-in.md)  
[<span data-ttu-id="095dd-161">for, instruction (C++)</span><span class="sxs-lookup"><span data-stu-id="095dd-161">for Statement (C++)</span></span>](/cpp/cpp/for-statement-cpp)  
[<span data-ttu-id="095dd-162">Instructions d’itération</span><span class="sxs-lookup"><span data-stu-id="095dd-162">Iteration Statements</span></span>](../../../csharp/language-reference/keywords/iteration-statements.md)
