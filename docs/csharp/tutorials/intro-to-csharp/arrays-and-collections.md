---
title: Utilisation des collections - Présentation du tutoriel C#
description: Découvrez C# en explorant la collection de listes de ce guide de démarrage rapide.
ms.date: 10/13/2017
ms.custom: mvc
ms.openlocfilehash: eaf921be2bd50b6e346f57f42e17f151ff336821
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/29/2018
ms.locfileid: "50205280"
---
# <a name="learn-to-manage-data-collections-using-the-generic-list-type"></a><span data-ttu-id="1db77-103">Apprenez à gérer les collections de données en utilisant le type de liste générique</span><span class="sxs-lookup"><span data-stu-id="1db77-103">Learn to manage data collections using the generic list type</span></span>

<span data-ttu-id="1db77-104">Ce didacticiel propose une introduction au langage C# et présente les concepts de base de la classe <xref:System.Collections.Generic.List%601>.</span><span class="sxs-lookup"><span data-stu-id="1db77-104">This introductory tutorial provides an introduction to the C# language and the basics of the <xref:System.Collections.Generic.List%601> class.</span></span>

<span data-ttu-id="1db77-105">Ce tutoriel suppose que vous disposez d’un ordinateur que vous pouvez utiliser pour le développement.</span><span class="sxs-lookup"><span data-stu-id="1db77-105">This tutorial expects you to have a machine you can use for development.</span></span> <span data-ttu-id="1db77-106">La rubrique .NET [Bien démarrer en 10 minutes](https://www.microsoft.com/net/core) contient des instructions pour configurer votre environnement de développement local sur Mac, PC ou Linux.</span><span class="sxs-lookup"><span data-stu-id="1db77-106">The .NET topic [Get Started in 10 minutes](https://www.microsoft.com/net/core) has instructions for setting up your local development environment on Mac, PC or Linux.</span></span> <span data-ttu-id="1db77-107">Vous trouverez une brève vue d’ensemble des commandes utilisées disponible dans [Se familiariser avec les outils de développement](local-environment.md), avec des liens vers des informations complémentaires.</span><span class="sxs-lookup"><span data-stu-id="1db77-107">A quick overview of the commands you'll use is in [Become familiar with the development tools](local-environment.md), with links to more details.</span></span>

## <a name="a-basic-list-example"></a><span data-ttu-id="1db77-108">Exemple de liste de base</span><span class="sxs-lookup"><span data-stu-id="1db77-108">A basic list example</span></span>

<span data-ttu-id="1db77-109">Créez un répertoire nommé **list-tutorial**.</span><span class="sxs-lookup"><span data-stu-id="1db77-109">Create a directory named **list-tutorial**.</span></span> <span data-ttu-id="1db77-110">Faites-en le répertoire actuel et exécutez `dotnet new console`.</span><span class="sxs-lookup"><span data-stu-id="1db77-110">Make that the current directory and run `dotnet new console`.</span></span>

> [!NOTE]
> <span data-ttu-id="1db77-111">Si vous venez de terminer la rubrique [Bien démarrer avec .NET en 10 minutes](https://www.microsoft.com/net), vous pouvez continuer à utiliser l’application myApp que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="1db77-111">If you just completed [Get started with .NET in 10 minutes](https://www.microsoft.com/net), you can keep using the myApp application that you just created.</span></span>

<span data-ttu-id="1db77-112">Ouvrez **Program.cs** dans votre éditeur favori, puis remplacez le code existant par le suivant :</span><span class="sxs-lookup"><span data-stu-id="1db77-112">Open **Program.cs** in your favorite editor, and replace the existing code with the following:</span></span>

```csharp
using System;
using System.Collections.Generic;

namespace list_tutorial
{
    class Program
    {
        static void Main(string[] args)
        {
            var names = new List<string> { "<name>", "Ana", "Felipe" };
            foreach (var name in names)
            {
                Console.WriteLine($"Hello {name.ToUpper()}!");
            }
        }
    }
}
```

<span data-ttu-id="1db77-113">Remplacez `<name>` par votre nom.</span><span class="sxs-lookup"><span data-stu-id="1db77-113">Replace `<name>` with your name.</span></span> <span data-ttu-id="1db77-114">Enregistrez **Program.cs**.</span><span class="sxs-lookup"><span data-stu-id="1db77-114">Save **Program.cs**.</span></span> <span data-ttu-id="1db77-115">Tapez `dotnet run` dans votre fenêtre de console pour effectuer un essai.</span><span class="sxs-lookup"><span data-stu-id="1db77-115">Type `dotnet run` in your console window to try it.</span></span>

<span data-ttu-id="1db77-116">Vous venez de créer une liste de chaînes, d’ajouter trois noms à cette liste et d’afficher les noms tout en majuscules.</span><span class="sxs-lookup"><span data-stu-id="1db77-116">You've just created a list of strings, added three names to that list, and printed out the names in all CAPS.</span></span> <span data-ttu-id="1db77-117">Vous utilisez des concepts que vous avez appris dans les tutoriels précédents pour lire la liste en boucle.</span><span class="sxs-lookup"><span data-stu-id="1db77-117">You're using concepts that you've learned in earlier tutorials to loop through the list.</span></span>

<span data-ttu-id="1db77-118">Le code permettant d’afficher les noms utilise la fonctionnalité [d’interpolation de chaîne](../../language-reference/tokens/interpolated.md).</span><span class="sxs-lookup"><span data-stu-id="1db77-118">The code to display names makes use of the [string interpolation](../../language-reference/tokens/interpolated.md) feature.</span></span>  <span data-ttu-id="1db77-119">Quand vous faites précéder une `string` du caractère `$`, vous pouvez incorporer le code C# dans la déclaration de chaîne.</span><span class="sxs-lookup"><span data-stu-id="1db77-119">When you precede a `string` with the `$` character, you can embed C# code in the string declaration.</span></span> <span data-ttu-id="1db77-120">La chaîne réelle remplace ce code C# par la valeur qu’elle génère.</span><span class="sxs-lookup"><span data-stu-id="1db77-120">The actual string replaces that C# code with the value it generates.</span></span> <span data-ttu-id="1db77-121">Dans cet exemple, elle remplace `{name.ToUpper()}` par chaque nom, converti en majuscules, car vous avez appelé la méthode <xref:System.String.ToUpper%2A>.</span><span class="sxs-lookup"><span data-stu-id="1db77-121">In this example, it replaces the `{name.ToUpper()}` with each name, converted to capital letters, because you called the <xref:System.String.ToUpper%2A> method.</span></span>

<span data-ttu-id="1db77-122">Continuons notre exploration.</span><span class="sxs-lookup"><span data-stu-id="1db77-122">Let's keep exploring.</span></span>

## <a name="modify-list-contents"></a><span data-ttu-id="1db77-123">Modifier le contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="1db77-123">Modify list contents</span></span>

<span data-ttu-id="1db77-124">La collection que vous avez créée utilise le type <xref:System.Collections.Generic.List%601>.</span><span class="sxs-lookup"><span data-stu-id="1db77-124">The collection you created uses the <xref:System.Collections.Generic.List%601> type.</span></span> <span data-ttu-id="1db77-125">Ce type stocke les séquences d’éléments.</span><span class="sxs-lookup"><span data-stu-id="1db77-125">This type stores sequences of elements.</span></span> <span data-ttu-id="1db77-126">Vous spécifiez le type des éléments entre crochets angulaires.</span><span class="sxs-lookup"><span data-stu-id="1db77-126">You specify the type of the elements between the angle brackets.</span></span>

<span data-ttu-id="1db77-127">Un aspect important du type <xref:System.Collections.Generic.List%601> est qu’il peut augmenter ou diminuer, ce qui vous permet d’ajouter ou de supprimer des éléments.</span><span class="sxs-lookup"><span data-stu-id="1db77-127">One important aspect of this <xref:System.Collections.Generic.List%601> type is that it can grow or shrink, enabling you to add or remove elements.</span></span> <span data-ttu-id="1db77-128">Ajoutez ce code avant de fermer le `}` dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="1db77-128">Add this code before the closing `}` in the `Main` method:</span></span>

```csharp
Console.WriteLine();
names.Add("Maria");
names.Add("Bill");
names.Remove("Ana");
foreach (var name in names)
{
    Console.WriteLine($"Hello {name.ToUpper()}!");
}
```

<span data-ttu-id="1db77-129">Vous avez ajouté deux noms supplémentaires à la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="1db77-129">You've added two more names to the end of the list.</span></span> <span data-ttu-id="1db77-130">Vous en avez également supprimé un.</span><span class="sxs-lookup"><span data-stu-id="1db77-130">You've also removed one as well.</span></span> <span data-ttu-id="1db77-131">Enregistrez le fichier et tapez `dotnet run` pour effectuer un essai.</span><span class="sxs-lookup"><span data-stu-id="1db77-131">Save the file, and type `dotnet run` to try it.</span></span>

<span data-ttu-id="1db77-132">La <xref:System.Collections.Generic.List%601> vous permet en outre de faire référence à des éléments individuels par **index**.</span><span class="sxs-lookup"><span data-stu-id="1db77-132">The <xref:System.Collections.Generic.List%601> enables you to reference individual items by **index** as well.</span></span> <span data-ttu-id="1db77-133">Vous placez l’index entre les jetons `[` et `]` après le nom de la liste.</span><span class="sxs-lookup"><span data-stu-id="1db77-133">You place the index between `[` and `]` tokens following the list name.</span></span> <span data-ttu-id="1db77-134">C# utilise la valeur 0 pour le premier index.</span><span class="sxs-lookup"><span data-stu-id="1db77-134">C# uses 0 for the first index.</span></span> <span data-ttu-id="1db77-135">Ajoutez le code directement sous le code que vous venez d’ajouter et effectuez un essai :</span><span class="sxs-lookup"><span data-stu-id="1db77-135">Add this code directly below the code you just added and try it:</span></span>

```csharp
Console.WriteLine($"My name is {names[0]}");
Console.WriteLine($"I've added {names[2]} and {names[3]} to the list");
```

<span data-ttu-id="1db77-136">Vous ne pouvez pas accéder à un index au-delà de la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="1db77-136">You cannot access an index beyond the end of the list.</span></span> <span data-ttu-id="1db77-137">Rappelez-vous que les index commencent à partir de 0, de sorte que le plus grand index valide correspond au nombre d’éléments de la liste moins un.</span><span class="sxs-lookup"><span data-stu-id="1db77-137">Remember that indices start at 0, so the largest valid index is one less than the number of items in the list.</span></span> <span data-ttu-id="1db77-138">Vous pouvez vérifier la longueur de la liste à l’aide de la propriété <xref:System.Collections.Generic.List%601.Count%2A>.</span><span class="sxs-lookup"><span data-stu-id="1db77-138">You can check how long the list is using the <xref:System.Collections.Generic.List%601.Count%2A> property.</span></span> <span data-ttu-id="1db77-139">Ajoutez le code suivant à la fin de la méthode Main :</span><span class="sxs-lookup"><span data-stu-id="1db77-139">Add the following code at the end of the Main method:</span></span>

```csharp
Console.WriteLine($"The list has {names.Count} people in it");
 ```

<span data-ttu-id="1db77-140">Enregistrez le fichier et tapez de nouveau `dotnet run` pour afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="1db77-140">Save the file, and type `dotnet run` again to see the results.</span></span>

## <a name="search-and-sort-lists"></a><span data-ttu-id="1db77-141">Trier les listes et y effectuer des recherches</span><span class="sxs-lookup"><span data-stu-id="1db77-141">Search and sort lists</span></span>

<span data-ttu-id="1db77-142">Nos exemples utilisent des listes relativement petites, mais vos applications peuvent souvent générer des listes contenant beaucoup plus d’éléments, qui se comptent parfois même en milliers.</span><span class="sxs-lookup"><span data-stu-id="1db77-142">Our samples use relatively small lists, but your applications may often create lists with many more elements, sometimes numbering in the thousands.</span></span> <span data-ttu-id="1db77-143">Pour rechercher des éléments dans ces collections plus volumineuses, vous devez rechercher différents éléments dans la liste.</span><span class="sxs-lookup"><span data-stu-id="1db77-143">To find elements in these larger collections, you need to search the list for different items.</span></span> <span data-ttu-id="1db77-144">La méthode <xref:System.Collections.Generic.List%601.IndexOf%2A> recherche un élément et retourne l’index de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="1db77-144">The <xref:System.Collections.Generic.List%601.IndexOf%2A> method searches for an item and returns the index of the item.</span></span> <span data-ttu-id="1db77-145">Ajoutez ce code en bas de votre méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="1db77-145">Add this code to the bottom of your `Main` method:</span></span>

```csharp
var index = names.IndexOf("Felipe");
if (index == -1)
{
    Console.WriteLine($"When an item is not found, IndexOf returns {index}");
} else
{
    Console.WriteLine($"The name {names[index]} is at index {index}");
}

index = names.IndexOf("Not Found");
if (index == -1)
{
    Console.WriteLine($"When an item is not found, IndexOf returns {index}");
} else
{
    Console.WriteLine($"The name {names[index]} is at index {index}");

}
```

<span data-ttu-id="1db77-146">Il est également possible de trier les éléments de la liste.</span><span class="sxs-lookup"><span data-stu-id="1db77-146">The items in your list can be sorted as well.</span></span> <span data-ttu-id="1db77-147">La méthode <xref:System.Collections.Generic.List%601.Sort%2A> trie tous les éléments de la liste dans l’ordre normal (par ordre alphabétique dans le cas de chaînes).</span><span class="sxs-lookup"><span data-stu-id="1db77-147">The <xref:System.Collections.Generic.List%601.Sort%2A> method sorts all the items in the list in their normal order (alphabetically in the case of strings).</span></span> <span data-ttu-id="1db77-148">Ajoutez ce code en bas de notre méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="1db77-148">Add this code to the bottom of our `Main` method:</span></span>

```csharp
names.Sort();
foreach (var name in names)
{
    Console.WriteLine($"Hello {name.ToUpper()}!");
}
```

<span data-ttu-id="1db77-149">Enregistrez le fichier et tapez `dotnet run` pour tester cette dernière version.</span><span class="sxs-lookup"><span data-stu-id="1db77-149">Save the file and type `dotnet run` to try this latest version.</span></span>

<span data-ttu-id="1db77-150">Avant de passer à la section suivante, déplaçons le code actuel dans une méthode distincte.</span><span class="sxs-lookup"><span data-stu-id="1db77-150">Before you start the next section, let's move the current code into a separate method.</span></span> <span data-ttu-id="1db77-151">Cela nous permettra de travailler plus facilement avec un nouvel exemple.</span><span class="sxs-lookup"><span data-stu-id="1db77-151">That makes it easier to start working with a new example.</span></span> <span data-ttu-id="1db77-152">Renommez votre méthode `Main` `WorkingWithStrings` et écrivez une nouvelle méthode `Main` qui appelle `WorkingWithStrings`.</span><span class="sxs-lookup"><span data-stu-id="1db77-152">Rename your `Main` method to `WorkingWithStrings` and write a new `Main` method that calls `WorkingWithStrings`.</span></span> <span data-ttu-id="1db77-153">Une fois terminé, votre code doit ressembler au code suivant :</span><span class="sxs-lookup"><span data-stu-id="1db77-153">When you have finished, your code should look like this:</span></span>

```csharp
using System;
using System.Collections.Generic;

namespace list_tutorial
{
    class Program
    {
        static void Main(string[] args)
        {
            WorkingWithStrings();
        }

        public static void WorkingWithStrings()
        {
            var names = new List<string> { "<name>", "Ana", "Felipe" };
            foreach (var name in names)
            {
                Console.WriteLine($"Hello {name.ToUpper()}!");
            }

            Console.WriteLine();
            names.Add("Maria");
            names.Add("Bill");
            names.Remove("Ana");
            foreach (var name in names)
            {
                Console.WriteLine($"Hello {name.ToUpper()}!");
            }

            Console.WriteLine($"My name is {names[0]}");
            Console.WriteLine($"I've added {names[2]} and {names[3]} to the list");

            Console.WriteLine($"The list has {names.Count} people in it");

            var index = names.IndexOf("Felipe");
            Console.WriteLine($"The name {names[index]} is at index {index}");

            var notFound = names.IndexOf("Not Found");
            Console.WriteLine($"When an item is not found, IndexOf returns {notFound}");

            names.Sort();
            foreach (var name in names)
            {
                Console.WriteLine($"Hello {name.ToUpper()}!");
            }
        }
    }
}
```

## <a name="lists-of-other-types"></a><span data-ttu-id="1db77-154">Listes d’autres types</span><span class="sxs-lookup"><span data-stu-id="1db77-154">Lists of other types</span></span>

<span data-ttu-id="1db77-155">Vous avez jusqu'à présent utilisé le type `string` dans les listes.</span><span class="sxs-lookup"><span data-stu-id="1db77-155">You've been using the `string` type in lists so far.</span></span> <span data-ttu-id="1db77-156">Nous allons maintenant créer une <xref:System.Collections.Generic.List%601> en utilisant un autre type.</span><span class="sxs-lookup"><span data-stu-id="1db77-156">Let's make a <xref:System.Collections.Generic.List%601> using a different type.</span></span> <span data-ttu-id="1db77-157">Commençons par créer un ensemble de nombres.</span><span class="sxs-lookup"><span data-stu-id="1db77-157">Let's build a set of numbers.</span></span>

<span data-ttu-id="1db77-158">Ajoutez le code suivant en bas de votre nouvelle méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="1db77-158">Add the following to the bottom of your new `Main` method:</span></span>

```csharp
var fibonacciNumbers = new List<int> {1, 1};
```

<span data-ttu-id="1db77-159">Cela crée une liste d’entiers et définit les deux premiers entiers sur la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="1db77-159">That creates a list of integers, and sets the first two integers to the value 1.</span></span> <span data-ttu-id="1db77-160">Il s’agit des deux premières valeurs d’une *séquence Fibonacci* (séquence de nombres).</span><span class="sxs-lookup"><span data-stu-id="1db77-160">These are the first two values of a *Fibonacci Sequence*, a sequence of numbers.</span></span> <span data-ttu-id="1db77-161">Chaque nombre Fibonacci suivant correspond à la somme des deux nombres précédents.</span><span class="sxs-lookup"><span data-stu-id="1db77-161">Each next Fibonacci number is found by taking the sum of the previous two numbers.</span></span> <span data-ttu-id="1db77-162">Ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="1db77-162">Add this code:</span></span>

```csharp
var previous = fibonacciNumbers[fibonacciNumbers.Count - 1];
var previous2 = fibonacciNumbers[fibonacciNumbers.Count - 2];

fibonacciNumbers.Add(previous + previous2);

foreach(var item in fibonacciNumbers)
    Console.WriteLine(item);
```

<span data-ttu-id="1db77-163">Enregistrez le fichier et tapez `dotnet run` pour afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="1db77-163">Save the file and type `dotnet run` to see the results.</span></span>

> [!TIP]
> <span data-ttu-id="1db77-164">Pour vous concentrer uniquement sur cette section, vous pouvez commenter le code qui appelle `WorkingWithStrings();`.</span><span class="sxs-lookup"><span data-stu-id="1db77-164">To concentrate on just this section, you can comment out the code that calls `WorkingWithStrings();`.</span></span> <span data-ttu-id="1db77-165">Insérez simplement deux caractères `/` devant l’appel comme suit :  `// WorkingWithStrings();`.</span><span class="sxs-lookup"><span data-stu-id="1db77-165">Just put two `/` characters in front of the call like this:  `// WorkingWithStrings();`.</span></span>

## <a name="challenge"></a><span data-ttu-id="1db77-166">Test</span><span class="sxs-lookup"><span data-stu-id="1db77-166">Challenge</span></span>

<span data-ttu-id="1db77-167">Vérifiez si vous pouvez mettre en pratique certains des concepts appris ici et dans d’autres leçons antérieures.</span><span class="sxs-lookup"><span data-stu-id="1db77-167">See if you can put together some of the concepts from this and earlier lessons.</span></span> <span data-ttu-id="1db77-168">Approfondissez à partir de ce que vous avez créé jusqu'à présent avec les nombres de Fibonacci.</span><span class="sxs-lookup"><span data-stu-id="1db77-168">Expand on what you've built so far with Fibonacci Numbers.</span></span> <span data-ttu-id="1db77-169">Essayez d’écrire le code pour générer les 20 premiers nombres de la séquence.</span><span class="sxs-lookup"><span data-stu-id="1db77-169">Try to write the code to generate the first 20 numbers in the sequence.</span></span> <span data-ttu-id="1db77-170">(Astuce, le 20ème nombre Fibonacci est 6765.)</span><span class="sxs-lookup"><span data-stu-id="1db77-170">(As a hint, the 20th Fibonacci number is 6765.)</span></span>

## <a name="complete-challenge"></a><span data-ttu-id="1db77-171">Terminer le test</span><span class="sxs-lookup"><span data-stu-id="1db77-171">Complete challenge</span></span>

<span data-ttu-id="1db77-172">Vous pouvez afficher un exemple de solution en [consultant l’exemple de code terminé sur GitHub](https://github.com/dotnet/samples/tree/master/csharp/list-quickstart/Program.cs#L13-L23).</span><span class="sxs-lookup"><span data-stu-id="1db77-172">You can see an example solution by [looking at the finished sample code on GitHub](https://github.com/dotnet/samples/tree/master/csharp/list-quickstart/Program.cs#L13-L23)</span></span>

<span data-ttu-id="1db77-173">À chaque itération de la boucle, vous sélectionnez les deux derniers entiers de la liste, les additionner et ajoutez la valeur obtenue à la liste.</span><span class="sxs-lookup"><span data-stu-id="1db77-173">With each iteration of the loop, you're taking the last two integers in the list, summing them, and adding that value to the list.</span></span> <span data-ttu-id="1db77-174">La boucle se répète jusqu'à ce que vous ayez ajouté 20 éléments à la liste.</span><span class="sxs-lookup"><span data-stu-id="1db77-174">The loop repeats until you've added 20 items to the list.</span></span>

<span data-ttu-id="1db77-175">Félicitations, vous avez terminé ce didacticiel sur les listes.</span><span class="sxs-lookup"><span data-stu-id="1db77-175">Congratulations, you've completed the list tutorial.</span></span> <span data-ttu-id="1db77-176">Vous pouvez passer au tutoriel [Introduction aux classes](introduction-to-classes.md) dans votre propre environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="1db77-176">You can continue with the [Introduction to classes](introduction-to-classes.md) tutorial in your own development environment.</span></span>

<span data-ttu-id="1db77-177">Pour plus d’informations sur l’utilisation du type `List`, consultez la rubrique du [Guide .NET](../../../standard/index.md) sur les [collections](../../../standard/collections/index.md).</span><span class="sxs-lookup"><span data-stu-id="1db77-177">You can learn more about working with the `List` type in the [.NET Guide](../../../standard/index.md) topic on [collections](../../../standard/collections/index.md).</span></span> <span data-ttu-id="1db77-178">Vous allez également en découvrir plus sur de nombreux autres types de collection.</span><span class="sxs-lookup"><span data-stu-id="1db77-178">You'll also learn about many other collection types.</span></span>