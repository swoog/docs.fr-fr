---
title: "Didacticiel sur les chaînes interpolées - Guides de démarrage rapide local en C#"
description: "Dans ce guide de démarrage rapide sur les chaînes interpolées, vous écrivez du code C# de façon à inclure le résultat d’une expression dans une chaîne plus grande."
author: rpetrusha
ms.author: ronpet
ms.date: 01/11/2018
ms.topic: get-started-article
ms.prod: .net
ms.technology: devlang-csharp
ms.devlang: csharp
ms.custom: mvc
ms.openlocfilehash: b6089b69eb350fce29f86f19f5abeb44acb4b6b4
ms.sourcegitcommit: 96cc82cac4650adfb65ba351506d8a8fbcd17b5c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2018
---
# <a name="interpolated-strings"></a><span data-ttu-id="4c02e-103">Chaînes interpolées</span><span class="sxs-lookup"><span data-stu-id="4c02e-103">Interpolated strings</span></span>

<span data-ttu-id="4c02e-104">Ce guide de démarrage rapide explique comment utiliser des chaînes interpolées en C# pour insérer des valeurs dans une chaîne à sortie unique.</span><span class="sxs-lookup"><span data-stu-id="4c02e-104">This quickstart teaches you how to use interpolated strings in C# to insert values into a single ouput string.</span></span> <span data-ttu-id="4c02e-105">Vous allez écrire un code en C# et afficher les résultats de la compilation et de l’exécution du code.</span><span class="sxs-lookup"><span data-stu-id="4c02e-105">You write C# code and see the results of compiling and running it.</span></span> <span data-ttu-id="4c02e-106">Le guide de démarrage rapide contient une série de leçons qui insèrent des valeurs dans des chaînes et mettent en forme ces valeurs de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="4c02e-106">The quickstart contains a series of lessons that insert values into strings, and format those values in different ways.</span></span>

<span data-ttu-id="4c02e-107">Ce guide de démarrage rapide suppose que vous disposez d’un ordinateur que vous pouvez utiliser pour le développement.</span><span class="sxs-lookup"><span data-stu-id="4c02e-107">This quickstart expects that you have a machine you can use for development.</span></span> <span data-ttu-id="4c02e-108">La rubrique .NET [Bien démarrer en 10 minutes](https://www.microsoft.com/net/core) contient des instructions pour configurer votre environnement de développement local sur Mac, PC ou Linux.</span><span class="sxs-lookup"><span data-stu-id="4c02e-108">The .NET topic [Get Started in 10 minutes](https://www.microsoft.com/net/core) has instructions for setting up your local development environment on Mac, PC or Linux.</span></span> <span data-ttu-id="4c02e-109">Une brève vue d’ensemble des commandes que vous utiliserez est disponible dans la [présentation des guides de démarrage rapide local](local-environment.md), avec des liens vers des informations complémentaires.</span><span class="sxs-lookup"><span data-stu-id="4c02e-109">A quick overview of the commands you'll use is in the [introduction to the local quickstarts](local-environment.md) with links to more details.</span></span> 

## <a name="create-an-interpolated-string"></a><span data-ttu-id="4c02e-110">Créer une chaîne interpolée</span><span class="sxs-lookup"><span data-stu-id="4c02e-110">Create an interpolated string</span></span>

<span data-ttu-id="4c02e-111">Créez un répertoire nommé **interpolated-quickstart**.</span><span class="sxs-lookup"><span data-stu-id="4c02e-111">Create a directory named **interpolated-quickstart**.</span></span> <span data-ttu-id="4c02e-112">Faites-en le répertoire actif et exécutez la commande suivante à partir d’une fenêtre de console :</span><span class="sxs-lookup"><span data-stu-id="4c02e-112">Make it the current directory and run the following command from a console window:</span></span>

```console
dotnet new console -n interpolated -o .
```

<span data-ttu-id="4c02e-113">Cette commande crée une nouvelle application console .NET Core dans le répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="4c02e-113">This command creates a new .NET Core console application in the current directory.</span></span>

<span data-ttu-id="4c02e-114">Ouvrez **Program.cs** dans votre éditeur favori, puis remplacez la ligne `Console.WriteLine("Hello World!");` par le code qui suit, en remplaçant `<name>` par votre nom :</span><span class="sxs-lookup"><span data-stu-id="4c02e-114">Open **Program.cs** in your favorite editor, and replace the line `Console.WriteLine("Hello World!");` with the following code, where you replace `<name>` with your name:</span></span>

```csharp
var name = "<name>";
Console.WriteLine($"Hello, {name}. It's a pleasure to meet you!");
```
<span data-ttu-id="4c02e-115">Essayez ce code en tapant `dotnet run` dans la fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="4c02e-115">Try this code by typing `dotnet run` in your console window.</span></span> <span data-ttu-id="4c02e-116">Quand vous exécutez le programme, il affiche une chaîne unique qui inclut votre nom dans le message d’accueil.</span><span class="sxs-lookup"><span data-stu-id="4c02e-116">When you run the program, it displays a single string that includes your name in the greeting.</span></span> <span data-ttu-id="4c02e-117">La chaîne qui se trouve dans l’appel de méthode <xref:System.Console.WriteLine%2A> est une *chaîne interpolée*.</span><span class="sxs-lookup"><span data-stu-id="4c02e-117">The string included in the <xref:System.Console.WriteLine%2A> method call is an *interpolated string*.</span></span> <span data-ttu-id="4c02e-118">C’est un genre de modèle qui vous permet de construire une chaîne unique (appelée *chaîne de résultat*) à partir d’une chaîne qui comprend du code incorporé.</span><span class="sxs-lookup"><span data-stu-id="4c02e-118">It's a kind of template that lets you construct a single string (called the *result string*) from a string that includes embedded code.</span></span> <span data-ttu-id="4c02e-119">Les chaînes interpolées sont particulièrement utiles pour insérer des valeurs dans une chaîne ou pour concaténer (joindre) des chaînes.</span><span class="sxs-lookup"><span data-stu-id="4c02e-119">Interpolated strings are particularly useful for inserting values into a string or concatenating (joining together) strings.</span></span> 
    
<span data-ttu-id="4c02e-120">Cet exemple simple contient les deux éléments que chaque chaîne interpolée doit avoir :</span><span class="sxs-lookup"><span data-stu-id="4c02e-120">This simple example contains the two elements that every interpolated string must have:</span></span> 

- <span data-ttu-id="4c02e-121">Un littéral de chaîne qui commence par le caractère `$` avant ses guillemets ouvrants.</span><span class="sxs-lookup"><span data-stu-id="4c02e-121">A string literal that begins with the `$` character before its opening quotation mark character.</span></span> <span data-ttu-id="4c02e-122">Il ne peut pas y avoir d’espace entre le symbole `$` et les guillemets.</span><span class="sxs-lookup"><span data-stu-id="4c02e-122">There can't be any spaces between the `$` symbol and the quotation mark character.</span></span> <span data-ttu-id="4c02e-123">(Si vous voulez voir ce qui se passe si vous en incluez un, insérez un espace après le caractère `$`, enregistrez le fichier et réexécutez le programme en tapant `dotnet run` dans la fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="4c02e-123">(If you'd like to see what happens if you include one, insert a space after the `$` character, save the file, and run the program again by typing `dotnet run` in the console window.</span></span> <span data-ttu-id="4c02e-124">Le compilateur C# affiche un message d’erreur « Erreur CS1056 : caractère inattendu ’$’ ».)</span><span class="sxs-lookup"><span data-stu-id="4c02e-124">The C# compiler displays an error message, "error CS1056: Unexpected character '$'".)</span></span> 

- <span data-ttu-id="4c02e-125">Une ou plusieurs *expressions interpolées*.</span><span class="sxs-lookup"><span data-stu-id="4c02e-125">One or more *interpolated expressions*.</span></span> <span data-ttu-id="4c02e-126">Une expression interpolée est indiquée par des accolades ouvrantes et fermantes (`{` et `}`).</span><span class="sxs-lookup"><span data-stu-id="4c02e-126">An interpolated expression is indicated by an opening and closing brace (`{` and `}`).</span></span> <span data-ttu-id="4c02e-127">Vous pouvez placer n’importe quelle expression C# qui retourne une valeur (notamment `null`) à l’intérieur des accolades.</span><span class="sxs-lookup"><span data-stu-id="4c02e-127">You can put any C# expression that returns a value (including `null`) inside the braces.</span></span> 

<span data-ttu-id="4c02e-128">Essayons quelques autres exemples de chaînes interpolées avec d’autres types de données.</span><span class="sxs-lookup"><span data-stu-id="4c02e-128">Let's try a few more interpolated string examples with some other data types.</span></span>
    
## <a name="include-different-data-types"></a><span data-ttu-id="4c02e-129">Inclure différents types de données</span><span class="sxs-lookup"><span data-stu-id="4c02e-129">Include different data types</span></span>

<span data-ttu-id="4c02e-130">Dans la section précédente, vous avez utilisé une chaîne interpolée pour insérer une chaîne à l’intérieur d’une autre.</span><span class="sxs-lookup"><span data-stu-id="4c02e-130">In the previous section, you used an interpolated string to insert one string inside of another.</span></span> <span data-ttu-id="4c02e-131">Une expression de chaîne interpolée peut toutefois être de n’importe quel type de données.</span><span class="sxs-lookup"><span data-stu-id="4c02e-131">An interpolated string expression can be any data type, though.</span></span> <span data-ttu-id="4c02e-132">Essayons une chaîne interpolée qui a des valeurs de plusieurs types de données.</span><span class="sxs-lookup"><span data-stu-id="4c02e-132">Let's try an interpolated string that has values of multiple data types.</span></span> 
    
<span data-ttu-id="4c02e-133">L’exemple suivant comprend des expressions interpolées avec un objet `Vegetable`, un membre de l’énumération `Unit`, une valeur <xref:System.DateTime> et une valeur <xref:System.Decimal>.</span><span class="sxs-lookup"><span data-stu-id="4c02e-133">The following example includes interpolated expressions with a `Vegetable` object, a member of the `Unit` enumeration, a <xref:System.DateTime> value, and a <xref:System.Decimal> value.</span></span> <span data-ttu-id="4c02e-134">Remplacez tout le code C# dans votre éditeur par le code suivant, puis utilisez la commande `console run` pour l’exécuter :</span><span class="sxs-lookup"><span data-stu-id="4c02e-134">Replace all of the C# code in your editor with the following code, and then use the `console run` command to run it:</span></span>

```csharp
using System;

public class Vegetable
{
   public Vegetable(string name) => Name = name;
   
   public string Name { get; }
   
   public override string ToString() => Name;
}

public class Example
{
   public enum Unit { item, pound, ounce, dozen };
   
   public static void Main()
   {
      var item = new Vegetable("eggplant");
      var date = DateTime.Now;
      var price = 1.99m;
      var unit = Unit.item;
      Console.WriteLine($"On {date}, the price of {item} was {price} per {unit}.");
   }
}
```
    
<span data-ttu-id="4c02e-135">Notez que la deuxième expression interpolée comprend l’objet `item` dans la chaîne de résultat affichée dans la console, et dans ce cas la chaîne « eggplant » est insérée dans la chaîne de résultat.</span><span class="sxs-lookup"><span data-stu-id="4c02e-135">Note that the second interpolated expression includes the `item` object in the result string that's displayed to the console, and in this case the string "eggplant" is inserted into the result string.</span></span> <span data-ttu-id="4c02e-136">Cela est dû au fait que lorsque le type d’une expression interpolée n’est pas une chaîne, le compilateur Visual C# effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4c02e-136">That's because, when the type of an interpolated expression is not a string, the C# compiler does the following:</span></span>

- <span data-ttu-id="4c02e-137">Si l’expression interpolée est `null`, elle retourne une chaîne vide (« », ou <xref:System.String.Empty?displayProperty=nameWithType>).</span><span class="sxs-lookup"><span data-stu-id="4c02e-137">If the interpolated expression is `null`, the interpolated expression returns an empty string ("", or <xref:System.String.Empty?displayProperty=nameWithType>).</span></span>

- <span data-ttu-id="4c02e-138">Si l’expression interpolée n’est pas `null`, la méthode `ToString` du type de l’expression interpolée est appelée.</span><span class="sxs-lookup"><span data-stu-id="4c02e-138">If the interpolated expression is not `null`, the `ToString` method of the type of the interpolated expression is called.</span></span> <span data-ttu-id="4c02e-139">Vous pouvez tester cela en commentant la définition de la méthode `Vegetable.ToString` dans l’exemple en plaçant un symbole de commentaire (`//`) devant elle.</span><span class="sxs-lookup"><span data-stu-id="4c02e-139">You can test this by commenting out the definition of the `Vegetable.ToString` method in the example by putting a comment symbol (`//`) in front of it.</span></span> <span data-ttu-id="4c02e-140">Dans la sortie, la chaîne « eggplant » est remplacée par le nom de type, « Vegetable », ce qui est le comportement par défaut de la méthode <xref:System.Object.ToString?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="4c02e-140">In the output, the string "eggplant" is replaced by the type name, "Vegetable", which is the default behavior of the <xref:System.Object.ToString?displayProperty=nameWithType> method.</span></span>   

<span data-ttu-id="4c02e-141">Dans la sortie de cet exemple, la date est trop précise (le prix des aubergines ne varie pas chaque seconde) et la valeur du prix n’indique pas de devise.</span><span class="sxs-lookup"><span data-stu-id="4c02e-141">In the output from this example, the date is too precise (the price of eggplant does not vary by the second), and the price value doesn't indicate a unit of currency.</span></span> <span data-ttu-id="4c02e-142">Dans la section suivante, vous découvrirez comment résoudre ces problèmes en contrôlant le format des chaînes retournées par les expressions interpolées.</span><span class="sxs-lookup"><span data-stu-id="4c02e-142">In the next section, you'll learn how to fix those issues by controlling the format of strings returned by interpolated expressions.</span></span>

## <a name="control-the-formatting-of-interpolated-expressions"></a><span data-ttu-id="4c02e-143">Contrôler la mise en forme des expressions interpolées</span><span class="sxs-lookup"><span data-stu-id="4c02e-143">Control the formatting of interpolated expressions</span></span>

<span data-ttu-id="4c02e-144">Dans la section précédente, deux chaînes à la mise en forme incorrecte ont été insérées dans la chaîne de résultat.</span><span class="sxs-lookup"><span data-stu-id="4c02e-144">In the previous section, two poorly formatted strings were inserted into the result string.</span></span> <span data-ttu-id="4c02e-145">L’une était une valeur de date et d’heure pour laquelle seule la date était appropriée.</span><span class="sxs-lookup"><span data-stu-id="4c02e-145">One was a date and time value for which only the date was appropriate.</span></span> <span data-ttu-id="4c02e-146">La deuxième était un prix qui n’indiquait pas la monnaie locale.</span><span class="sxs-lookup"><span data-stu-id="4c02e-146">The second was a price that did not indicate its unit of currency.</span></span> <span data-ttu-id="4c02e-147">Ces deux problèmes sont faciles à résoudre.</span><span class="sxs-lookup"><span data-stu-id="4c02e-147">Both issues are easy to address.</span></span> <span data-ttu-id="4c02e-148">Les expressions interpolées peuvent inclure des *chaînes de format* qui gèrent la mise en forme de types particuliers.</span><span class="sxs-lookup"><span data-stu-id="4c02e-148">Interpolated expressions can include *format strings* that control the formatting of particular types.</span></span> <span data-ttu-id="4c02e-149">Modifiez l’appel à `Console.WriteLine` dans l’exemple précédent de façon à inclure le spécificateur de format pour les champs de date et de prix, comme indiqué sur la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="4c02e-149">Modify the call to `Console.WriteLine` from the previous example to include the format specifier for the date and price fields as shown in the following line:</span></span>

```csharp
Console.WriteLine($"On {date:d}, the price of {item} was {price:C2} per {unit}.");
```
    
<span data-ttu-id="4c02e-150">Vous spécifiez une chaîne de format en plaçant après l’expression interpolée un signe deux-points et la chaîne de format.</span><span class="sxs-lookup"><span data-stu-id="4c02e-150">You specify a format string by following the interpolated expression with a colon and the format string.</span></span> <span data-ttu-id="4c02e-151">« d » est une [chaîne de format de date et d’heure standard](../../standard/base-types/standard-date-and-time-format-strings.md#the-short-date-d-format-specifier) qui représente le format de date courte.</span><span class="sxs-lookup"><span data-stu-id="4c02e-151">"d" is a [standard date and time format string](../../standard/base-types/standard-date-and-time-format-strings.md#the-short-date-d-format-specifier) that represents the short date format.</span></span> <span data-ttu-id="4c02e-152">« C2 » est une [chaîne de format numérique standard](../../standard/base-types/standard-numeric-format-strings.md#the-currency-c-format-specifier) qui représente un nombre sous forme de valeur monétaire avec deux chiffres après la virgule.</span><span class="sxs-lookup"><span data-stu-id="4c02e-152">"C2" is a  [standard numeric format string](../../standard/base-types/standard-numeric-format-strings.md#the-currency-c-format-specifier) that represents a number as a currency value with two digits after the decimal point.</span></span>

<span data-ttu-id="4c02e-153">Plusieurs types dans les bibliothèques .NET Standard prennent en charge un ensemble prédéfini de chaînes de format.</span><span class="sxs-lookup"><span data-stu-id="4c02e-153">A number of types in the .NET Standard libraries support a predefined set of format strings.</span></span> <span data-ttu-id="4c02e-154">Il s’agit notamment de tous les types numériques et des types de date et d’heure.</span><span class="sxs-lookup"><span data-stu-id="4c02e-154">These include all the numeric types and the date and time types.</span></span> <span data-ttu-id="4c02e-155">Pour obtenir une liste complète des types qui prennent en charge les chaînes de format, consultez [Chaînes de format et types de bibliothèque de classes .NET](../../standard/base-types/formatting-types.md#stringRef) dans l’article [Mise en forme des types dans .NET](../../standard/base-types/formatting-types.md).</span><span class="sxs-lookup"><span data-stu-id="4c02e-155">For a complete list of types that support format strings, see [Format Strings and .NET Class Library Types](../../standard/base-types/formatting-types.md#stringRef) in the [Formatting Types in .NET](../../standard/base-types/formatting-types.md) article.</span></span> <span data-ttu-id="4c02e-156">Tout type peut prendre en charge un ensemble de chaînes de format, et vous pouvez également développer des extensions de mise en forme personnalisées qui fournissent une mise en forme personnalisée pour des types existants.</span><span class="sxs-lookup"><span data-stu-id="4c02e-156">Any type can support a set of format strings, and you can also develop custom formatting extensions that provide custom formatting for existing types.</span></span> <span data-ttu-id="4c02e-157">Pour plus d’informations sur la mise en forme personnalisée à l’aide d’une implémentation<xref:System.ICustomFormatter>, consultez [Mise en forme personnalisée avec ICustomFormatter](../../standard/base-types/formatting-types.md#custom-formatting-with-icustomformatter) dans l’article [Mise en forme des types dans .NET](../../standard/base-types/formatting-types.md).</span><span class="sxs-lookup"><span data-stu-id="4c02e-157">For information on custom formatting by providing an <xref:System.ICustomFormatter> implementation, see [Custom Formatting with ICustomFormatter](../../standard/base-types/formatting-types.md#custom-formatting-with-icustomformatter) in the [Formatting Types in .NET](../../standard/base-types/formatting-types.md) article.</span></span>

<span data-ttu-id="4c02e-158">Essayez de modifier les chaînes de format dans votre éditeur de texte et, à chaque modification, relancez le programme pour voir comment celles-ci affectent la mise en forme de la date et de l’heure et la valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="4c02e-158">Try modifying the format strings in your text editor and, each time you make a change, rerun the program to see how the changes affect the formatting of the date and time and the numeric value.</span></span> <span data-ttu-id="4c02e-159">Remplacez le « d » dans `{date:d}` par « t » (pour afficher le format d’heure courte), « y » (pour afficher l’année et mois) et « yyyy » (pour afficher l’année sous forme de nombre à quatre chiffres).</span><span class="sxs-lookup"><span data-stu-id="4c02e-159">Change the "d" in `{date:d}` to "t" (to display the short time format), "y" (to display the year and month), and "yyyy" (to display the year as a four-digit number).</span></span> <span data-ttu-id="4c02e-160">Remplacez le « C2 » dans `{price:C2}` par « e » (pour la notation exponentielle) et « F3 » (pour une valeur numérique avec trois chiffres après la virgule).</span><span class="sxs-lookup"><span data-stu-id="4c02e-160">Change the "C2" in `{price:C2}` to "e" (for exponential notation) and "F3" (for a numeric value with three digits after the decimal point).</span></span>

<span data-ttu-id="4c02e-161">En plus de la mise en forme, vous pouvez aussi contrôler la largeur de champ et l’alignement des chaînes retournées par une expression interpolée.</span><span class="sxs-lookup"><span data-stu-id="4c02e-161">In addition to controlling formatting, you can also control the field width and alignment of the strings returned by an interpolated expression.</span></span> <span data-ttu-id="4c02e-162">Dans la section suivante, vous allez découvrir comment effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="4c02e-162">In the next section, you'll learn how to do this.</span></span>

## <a name="control-the-field-width-and-alignment-of-interpolated-expressions"></a><span data-ttu-id="4c02e-163">Contrôler la largeur de champ et l’alignement des expressions interpolées</span><span class="sxs-lookup"><span data-stu-id="4c02e-163">Control the field width and alignment of interpolated expressions</span></span>

<span data-ttu-id="4c02e-164">En règle générale, quand la chaîne retournée par une expression interpolée est comprise dans une chaîne de résultat, elle ne comporte aucun espace de début ou de fin.</span><span class="sxs-lookup"><span data-stu-id="4c02e-164">Ordinarily, when the string returned by an interpolated expression is included in a result string, it has no leading or trailing spaces.</span></span> <span data-ttu-id="4c02e-165">En particulier pour les instances dans lesquelles vous travaillez avec un jeu de données, les expressions interpolées vous permettent de spécifier la largeur d’un champ et son alignement.</span><span class="sxs-lookup"><span data-stu-id="4c02e-165">Particularly for instances in which you are working with a set of data, interpolated expressions let you specify a field width and its alignment.</span></span> <span data-ttu-id="4c02e-166">Pour voir cela, remplacez tout le code dans votre éditeur de texte par le code suivant, puis tapez `console run` pour exécuter le programme :</span><span class="sxs-lookup"><span data-stu-id="4c02e-166">To see this, replace all the code in your text editor with the following code, then type `console run` to execute the program:</span></span>
    
```csharp
using System;
using System.Collections.Generic;

public class Example
{
   public static void Main()
   {
      var titles = new Dictionary<string, string>();
      titles.Add("Doyle, Arthur Conan", "Hound of the Baskervilles, The");
      titles.Add("London, Jack", "Call of the Wild, The");
      titles.Add("Shakespeare, William", "Tempest, The");

      Console.WriteLine("Author and Title List");
      Console.WriteLine($"\n{"Author",-25}    {"Title",30}\n");
      foreach (var title in titles)
         Console.WriteLine($"{title.Key,-25}     {title.Value,30}");
   }
}
```
    
<span data-ttu-id="4c02e-167">Les noms des auteurs sont alignés à gauche, et leurs titres sont alignés à droite.</span><span class="sxs-lookup"><span data-stu-id="4c02e-167">The names of authors are left-aligned, and the titles they wrote are right-aligned.</span></span> <span data-ttu-id="4c02e-168">Vous spécifiez l’alignement en ajoutant une virgule (« , ») après l’expression et en spécifiant la largeur du champ.</span><span class="sxs-lookup"><span data-stu-id="4c02e-168">You specify the alignment by adding a comma (",") after the expression and designating the field width.</span></span> <span data-ttu-id="4c02e-169">Si la largeur du champ est un nombre positif, le champ est aligné à droite :</span><span class="sxs-lookup"><span data-stu-id="4c02e-169">If the field width is a positive number, the field is right-aligned:</span></span>

```text
{expression, width}
```

<span data-ttu-id="4c02e-170">Si la largeur du champ est un nombre négatif, le champ est aligné à gauche :</span><span class="sxs-lookup"><span data-stu-id="4c02e-170">If the field width is a negative number, the field is left-aligned:</span></span>

```text
{expression, -width}
```

<span data-ttu-id="4c02e-171">Essayez de supprimer les signes négatifs des expressions interpolées `{"Author",-25}` et `{title.Key,-25}`, puis réexécutez l’exemple, comme avec le code suivant :</span><span class="sxs-lookup"><span data-stu-id="4c02e-171">Try removing the negative signs from the `{"Author",-25}` and `{title.Key,-25}` interpolated expressions and run the example again, as the following code does:</span></span>

```csharp
Console.WriteLine($"\n{"Author",25}    {"Title",30}\n");
foreach (var title in titles)
   Console.WriteLine($"{title.Key,25}     {title.Value,30}");
```

<span data-ttu-id="4c02e-172">Cette fois, les informations sur l’auteur sont alignées à droite.</span><span class="sxs-lookup"><span data-stu-id="4c02e-172">This time, the author information is right-aligned.</span></span>

<span data-ttu-id="4c02e-173">Vous pouvez combiner une largeur de champ et une chaîne de format dans une même expression interpolée.</span><span class="sxs-lookup"><span data-stu-id="4c02e-173">You can combine a field width and a format string in a single interpolated expression.</span></span> <span data-ttu-id="4c02e-174">La largeur du champ figure en premier, suivie d’un signe deux-points et de la chaîne de format.</span><span class="sxs-lookup"><span data-stu-id="4c02e-174">The field width comes first, followed by a colon and the format string.</span></span> <span data-ttu-id="4c02e-175">Remplacez tout le code à l’intérieur de la méthode `Main` par le code suivant, qui affiche trois chaînes mises en forme avec des largeurs de champ définies.</span><span class="sxs-lookup"><span data-stu-id="4c02e-175">Replace all of the code inside the `Main` method with the following code, which displays three formatted strings with defined field widths.</span></span> <span data-ttu-id="4c02e-176">Ensuite, exécutez le programme en entrant la commande `dotnet run`.</span><span class="sxs-lookup"><span data-stu-id="4c02e-176">Then run the program by entering the `dotnet run` command.</span></span>

```csharp
Console.WriteLine($"{DateTime.Now,-20:d} Hour {DateTime.Now,-10:HH} {1063.342,15:N2} feet");
```
<span data-ttu-id="4c02e-177">La sortie ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="4c02e-177">The output looks something like the following:</span></span>

```console
1/11/2018            Hour 09                1,063.34 feet
```

<span data-ttu-id="4c02e-178">Vous avez terminé le guide de démarrage rapide sur les chaînes interpolées.</span><span class="sxs-lookup"><span data-stu-id="4c02e-178">You've completed the interpolated strings quickstart.</span></span> 
    
<span data-ttu-id="4c02e-179">Vous pouvez passer au démarrage rapide [Tableaux et collections](arrays-and-collections.md) dans votre propre environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="4c02e-179">You can continue with the [Arrays and collections](arrays-and-collections.md) quickstart in your own development environment.</span></span>

<span data-ttu-id="4c02e-180">Plus d’informations sur l’utilisation des chaînes interpolées, consultez la rubrique [Chaînes interpolées](../language-reference/keywords/interpolated-strings.md) dans les informations de référence sur C#.</span><span class="sxs-lookup"><span data-stu-id="4c02e-180">You can learn more about working with interpolated strings in the [Interpolated Strings](../language-reference/keywords/interpolated-strings.md) topic in the C# Reference.</span></span>

