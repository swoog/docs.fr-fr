---
title: Tutoriel sur l’interpolation de chaîne - Guides de démarrage rapide local en C#
description: Ce guide de démarrage rapide montre comment utiliser la fonctionnalité d’interpolation de chaîne en C# pour insérer les résultats d’expressions mises en forme dans une chaîne plus grande.
author: rpetrusha
ms.author: ronpet
ms.date: 04/14/2018
ms.topic: get-started-article
ms.prod: .net
ms.technology: devlang-csharp
ms.devlang: csharp
ms.custom: mvc
ms.openlocfilehash: 7ef904e30475d2cc0584f2baf56bc33a68e172d4
ms.sourcegitcommit: 2e8acae16ae802f2d6d04e3ce0a6dbf04e476513
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2018
---
# <a name="string-interpolation"></a><span data-ttu-id="edd4f-103">Interpolation de chaîne</span><span class="sxs-lookup"><span data-stu-id="edd4f-103">String interpolation</span></span>

<span data-ttu-id="edd4f-104">Ce guide de démarrage rapide explique comment utiliser l’[interpolation de chaîne](../language-reference/tokens/interpolated.md) en C# pour insérer des valeurs dans une chaîne de résultat unique.</span><span class="sxs-lookup"><span data-stu-id="edd4f-104">This quickstart teaches you how to use C# [string interpolation](../language-reference/tokens/interpolated.md) to insert values into a single result string.</span></span> <span data-ttu-id="edd4f-105">Vous allez écrire un code en C# et afficher les résultats de la compilation et de l’exécution du code.</span><span class="sxs-lookup"><span data-stu-id="edd4f-105">You write C# code and see the results of compiling and running it.</span></span> <span data-ttu-id="edd4f-106">Le guide de démarrage rapide contient une série de leçons qui expliquent comment insérer des valeurs dans une chaîne et mettre en forme ces valeurs de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="edd4f-106">The quickstart contains a series of lessons that show you how to insert values into a string and format those values in different ways.</span></span>

<span data-ttu-id="edd4f-107">Ce guide de démarrage rapide suppose que vous disposez d’un ordinateur que vous pouvez utiliser pour le développement.</span><span class="sxs-lookup"><span data-stu-id="edd4f-107">This quickstart expects that you have a machine you can use for development.</span></span> <span data-ttu-id="edd4f-108">La rubrique .NET [Bien démarrer en 10 minutes](https://www.microsoft.com/net/core) contient des instructions pour configurer votre environnement de développement local sur Mac, PC ou Linux.</span><span class="sxs-lookup"><span data-stu-id="edd4f-108">The .NET topic [Get Started in 10 minutes](https://www.microsoft.com/net/core) has instructions for setting up your local development environment on Mac, PC or Linux.</span></span> <span data-ttu-id="edd4f-109">Une brève vue d’ensemble des commandes que vous utiliserez est disponible dans la [présentation des guides de démarrage rapide local](local-environment.md), avec des liens vers des informations complémentaires.</span><span class="sxs-lookup"><span data-stu-id="edd4f-109">A quick overview of the commands you'll use is in the [introduction to the local quickstarts](local-environment.md) with links to more details.</span></span> <span data-ttu-id="edd4f-110">Vous pouvez également suivre la [version interactive](interpolated-strings.yml) de ce guide de démarrage rapide dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="edd4f-110">You also can complete the [interactive version](interpolated-strings.yml) of this quickstart in your browser.</span></span>

## <a name="create-an-interpolated-string"></a><span data-ttu-id="edd4f-111">Créer une chaîne interpolée</span><span class="sxs-lookup"><span data-stu-id="edd4f-111">Create an interpolated string</span></span>

<span data-ttu-id="edd4f-112">Créez un répertoire nommé **interpolated**.</span><span class="sxs-lookup"><span data-stu-id="edd4f-112">Create a directory named **interpolated**.</span></span> <span data-ttu-id="edd4f-113">Faites-en le répertoire actif et exécutez la commande suivante à partir d’une fenêtre de console :</span><span class="sxs-lookup"><span data-stu-id="edd4f-113">Make it the current directory and run the following command from a console window:</span></span>

```console
dotnet new console
```

<span data-ttu-id="edd4f-114">Cette commande crée une nouvelle application console .NET Core dans le répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="edd4f-114">This command creates a new .NET Core console application in the current directory.</span></span>

<span data-ttu-id="edd4f-115">Ouvrez **Program.cs** dans votre éditeur favori, puis remplacez la ligne `Console.WriteLine("Hello World!");` par le code qui suit, en remplaçant `<name>` par votre nom :</span><span class="sxs-lookup"><span data-stu-id="edd4f-115">Open **Program.cs** in your favorite editor, and replace the line `Console.WriteLine("Hello World!");` with the following code, where you replace `<name>` with your name:</span></span>

```csharp
var name = "<name>";
Console.WriteLine($"Hello, {name}. It's a pleasure to meet you!");
```

<span data-ttu-id="edd4f-116">Essayez ce code en tapant `dotnet run` dans la fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="edd4f-116">Try this code by typing `dotnet run` in your console window.</span></span> <span data-ttu-id="edd4f-117">Quand vous exécutez le programme, il affiche une chaîne unique qui inclut votre nom dans le message d’accueil.</span><span class="sxs-lookup"><span data-stu-id="edd4f-117">When you run the program, it displays a single string that includes your name in the greeting.</span></span> <span data-ttu-id="edd4f-118">La chaîne qui se trouve dans l’appel de méthode <xref:System.Console.WriteLine%2A> est une *chaîne interpolée*.</span><span class="sxs-lookup"><span data-stu-id="edd4f-118">The string included in the <xref:System.Console.WriteLine%2A> method call is an *interpolated string*.</span></span> <span data-ttu-id="edd4f-119">C’est un genre de modèle qui vous permet de construire une chaîne unique (appelée *chaîne de résultat*) à partir d’une chaîne qui comprend du code incorporé.</span><span class="sxs-lookup"><span data-stu-id="edd4f-119">It's a kind of template that lets you construct a single string (called the *result string*) from a string that includes embedded code.</span></span> <span data-ttu-id="edd4f-120">Les chaînes interpolées sont particulièrement utiles pour insérer des valeurs dans une chaîne ou pour concaténer (joindre) des chaînes.</span><span class="sxs-lookup"><span data-stu-id="edd4f-120">Interpolated strings are particularly useful for inserting values into a string or concatenating (joining together) strings.</span></span>

<span data-ttu-id="edd4f-121">Cet exemple simple contient les deux éléments que chaque chaîne interpolée doit avoir :</span><span class="sxs-lookup"><span data-stu-id="edd4f-121">This simple example contains the two elements that every interpolated string must have:</span></span>

- <span data-ttu-id="edd4f-122">Un littéral de chaîne qui commence par le caractère `$` avant ses guillemets ouvrants.</span><span class="sxs-lookup"><span data-stu-id="edd4f-122">A string literal that begins with the `$` character before its opening quotation mark character.</span></span> <span data-ttu-id="edd4f-123">Il ne peut pas y avoir d’espace entre le symbole `$` et les guillemets.</span><span class="sxs-lookup"><span data-stu-id="edd4f-123">There can't be any spaces between the `$` symbol and the quotation mark character.</span></span> <span data-ttu-id="edd4f-124">(Si vous voulez voir ce qui se passe si vous en incluez un, insérez un espace après le caractère `$`, enregistrez le fichier et réexécutez le programme en tapant `dotnet run` dans la fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="edd4f-124">(If you'd like to see what happens if you include one, insert a space after the `$` character, save the file, and run the program again by typing `dotnet run` in the console window.</span></span> <span data-ttu-id="edd4f-125">Le compilateur C# affiche un message d’erreur « Erreur CS1056 : caractère inattendu ’$’ ».)</span><span class="sxs-lookup"><span data-stu-id="edd4f-125">The C# compiler displays an error message, "error CS1056: Unexpected character '$'".)</span></span>

- <span data-ttu-id="edd4f-126">Une ou plusieurs *expressions interpolées*.</span><span class="sxs-lookup"><span data-stu-id="edd4f-126">One or more *interpolated expressions*.</span></span> <span data-ttu-id="edd4f-127">Une expression interpolée est indiquée par des accolades ouvrantes et fermantes (`{` et `}`).</span><span class="sxs-lookup"><span data-stu-id="edd4f-127">An interpolated expression is indicated by an opening and closing brace (`{` and `}`).</span></span> <span data-ttu-id="edd4f-128">Vous pouvez placer n’importe quelle expression C# qui retourne une valeur (notamment `null`) à l’intérieur des accolades.</span><span class="sxs-lookup"><span data-stu-id="edd4f-128">You can put any C# expression that returns a value (including `null`) inside the braces.</span></span>

<span data-ttu-id="edd4f-129">Essayons quelques autres exemples d’interpolation de chaîne avec d’autres types de données.</span><span class="sxs-lookup"><span data-stu-id="edd4f-129">Let's try a few more string interpolation examples with some other data types.</span></span>

## <a name="include-different-data-types"></a><span data-ttu-id="edd4f-130">Inclure différents types de données</span><span class="sxs-lookup"><span data-stu-id="edd4f-130">Include different data types</span></span>

<span data-ttu-id="edd4f-131">Dans la section précédente, vous avez utilisé l’interpolation de chaîne pour insérer une chaîne à l’intérieur d’une autre.</span><span class="sxs-lookup"><span data-stu-id="edd4f-131">In the previous section, you used string interpolation to insert one string inside of another.</span></span> <span data-ttu-id="edd4f-132">Le résultat d’une expression interpolée peut toutefois être de n’importe quel type de données.</span><span class="sxs-lookup"><span data-stu-id="edd4f-132">The result of an interpolated expression can be of any data type, though.</span></span> <span data-ttu-id="edd4f-133">Nous allons insérer des valeurs de différents types de données dans une chaîne interpolée.</span><span class="sxs-lookup"><span data-stu-id="edd4f-133">Let's include values of various data types in an interpolated string.</span></span>

<span data-ttu-id="edd4f-134">Dans l’exemple suivant, nous commençons par définir un type de données personnalisé (`Vegetable`) qui a la [propriété](../properties.md) `Name` et la méthode `ToString`.</span><span class="sxs-lookup"><span data-stu-id="edd4f-134">In the following example, first, we define a custom data type `Vegetable` that has the `Name` [property](../properties.md) and the `ToString` method.</span></span> <span data-ttu-id="edd4f-135">Le code client peut utiliser cette méthode pour obtenir la représentation sous forme de chaîne d’une instance `Vegetable`.</span><span class="sxs-lookup"><span data-stu-id="edd4f-135">The client code can use that method to get the string representation of a `Vegetable` instance.</span></span> <span data-ttu-id="edd4f-136">Dans l’exemple, la méthode `Vegetable.ToString` retourne la valeur de la propriété `Name` qui est initialisée sur le constructeur `Vegetable` :</span><span class="sxs-lookup"><span data-stu-id="edd4f-136">In the example the `Vegetable.ToString` method returns the value of the `Name` property that is initialized at the `Vegetable` constructor:</span></span>

```csharp
public Vegetable(string name) => Name = name;
```

<span data-ttu-id="edd4f-137">Nous créons ensuite une instance du type `Vegetable` en utilisant le mot clé `new` et en ajoutant un paramètre name pour le constructeur `Vegetable` :</span><span class="sxs-lookup"><span data-stu-id="edd4f-137">We create an instance of the `Vegetable` type by using `new` keyword and providing a name parameter for the constructor `Vegetable`:</span></span>

```csharp
var item = new Vegetable("eggplant");
```

<span data-ttu-id="edd4f-138">Enfin, nous incluons la variable `item` dans une chaîne interpolée qui contient également une valeur <xref:System.DateTime>, une valeur <xref:System.Decimal> et une valeur d’[énumération](../programming-guide/enumeration-types.md) `Unit`.</span><span class="sxs-lookup"><span data-stu-id="edd4f-138">Finally, we include the `item` variable into an interpolated string that also contains a <xref:System.DateTime> value, a <xref:System.Decimal> value, and a `Unit` [enumeration](../programming-guide/enumeration-types.md) value.</span></span> <span data-ttu-id="edd4f-139">Remplacez tout le code C# dans votre éditeur par le code suivant, puis utilisez la commande `dotnet run` pour l’exécuter :</span><span class="sxs-lookup"><span data-stu-id="edd4f-139">Replace all of the C# code in your editor with the following code, and then use the `dotnet run` command to run it:</span></span>

```csharp
using System;

public class Vegetable
{
   public Vegetable(string name) => Name = name;
   
   public string Name { get; }
   
   public override string ToString() => Name;
}

public class Program
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

<span data-ttu-id="edd4f-140">Notez que l’expression interpolée `item` dans la chaîne interpolée correspond au texte « eggplant » (aubergines) dans la chaîne de résultat.</span><span class="sxs-lookup"><span data-stu-id="edd4f-140">Note that the interpolated expression `item` in the interpolated string resolves to the text "eggplant" in the result string.</span></span> <span data-ttu-id="edd4f-141">En effet, lorsque le résultat de l’expression n’est pas de type chaîne, il est résolu en une chaîne de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="edd4f-141">That's because, when the type of the expression result is not a string, the result is resolved to a string in the following way:</span></span>

- <span data-ttu-id="edd4f-142">Si l’expression interpolée a la valeur `null`, une chaîne vide («» ou <xref:System.String.Empty?displayProperty=nameWithType>) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="edd4f-142">If the interpolated expression evaluates to `null`, an empty string ("", or <xref:System.String.Empty?displayProperty=nameWithType>) is used.</span></span>

- <span data-ttu-id="edd4f-143">Si l’expression interpolée n’a pas la valeur `null`, en général, la méthode `ToString` du type du résultat est appelée.</span><span class="sxs-lookup"><span data-stu-id="edd4f-143">If the interpolated expression doesn't evaluate to `null`, typically the `ToString` method of the result type is called.</span></span> <span data-ttu-id="edd4f-144">Vous pouvez tester cela en mettant à jour l’implémentation de la méthode `Vegetable.ToString`.</span><span class="sxs-lookup"><span data-stu-id="edd4f-144">You can test this by updating the implementation of the `Vegetable.ToString` method.</span></span> <span data-ttu-id="edd4f-145">Vous pouvez aussi ne pas implémenter la méthode `ToString` étant donné que chaque type de données C# a déjà une implémentation de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="edd4f-145">You might even not implement `ToString` method since every C# data type has some implementation of this method.</span></span> <span data-ttu-id="edd4f-146">Pour tester cela, commentez la définition de la méthode `Vegetable.ToString` dans l’exemple (en la faisant précéder d’un symbole de commentaire `//`).</span><span class="sxs-lookup"><span data-stu-id="edd4f-146">To test that, comment out the definition of the `Vegetable.ToString` method in the example (to do that, put a comment symbol `//` in front of it).</span></span> <span data-ttu-id="edd4f-147">Dans la sortie, la chaîne « eggplant » (aubergines) est remplacée par le nom de type complet (« Vegetable » dans cet exemple), ce qui est le comportement par défaut de la méthode <xref:System.Object.ToString?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="edd4f-147">In the output, the string "eggplant" is replaced by the fully qualified type name ("Vegetable" in this example), which is the default behavior of the <xref:System.Object.ToString?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="edd4f-148">Le comportement par défaut de la méthode `ToString` pour un type d’énumération est de retourner la représentation sous forme de chaîne d’une valeur utilisée dans la définition de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="edd4f-148">Default behavior of the `ToString` method for an enumeration type is to return the string representation of a value used at the definition of the enumeration.</span></span>

<span data-ttu-id="edd4f-149">Dans la sortie de cet exemple, la date est trop précise (le prix des aubergines ne change pas chaque seconde) et la valeur du prix n’indique pas la devise locale.</span><span class="sxs-lookup"><span data-stu-id="edd4f-149">In the output from this example, the date is too precise (the price of eggplant doesn't change every second), and the price value doesn't indicate a unit of currency.</span></span> <span data-ttu-id="edd4f-150">Dans la section suivante, vous découvrirez comment résoudre ces problèmes en contrôlant le format des représentations sous forme de chaînes des résultats des expressions.</span><span class="sxs-lookup"><span data-stu-id="edd4f-150">In the next section, you'll learn how to fix those issues by controlling the format of string representations of the expression results.</span></span>

## <a name="control-the-formatting-of-interpolated-expressions"></a><span data-ttu-id="edd4f-151">Contrôler la mise en forme des expressions interpolées</span><span class="sxs-lookup"><span data-stu-id="edd4f-151">Control the formatting of interpolated expressions</span></span>

<span data-ttu-id="edd4f-152">Dans la section précédente, deux chaînes à la mise en forme incorrecte ont été insérées dans la chaîne de résultat.</span><span class="sxs-lookup"><span data-stu-id="edd4f-152">In the previous section, two poorly formatted strings were inserted into the result string.</span></span> <span data-ttu-id="edd4f-153">L’une était une valeur de date et d’heure pour laquelle seule la date était appropriée.</span><span class="sxs-lookup"><span data-stu-id="edd4f-153">One was a date and time value for which only the date was appropriate.</span></span> <span data-ttu-id="edd4f-154">La deuxième était un prix qui n’indiquait pas la devise locale.</span><span class="sxs-lookup"><span data-stu-id="edd4f-154">The second was a price that didn't indicate its unit of currency.</span></span> <span data-ttu-id="edd4f-155">Ces deux problèmes sont faciles à résoudre.</span><span class="sxs-lookup"><span data-stu-id="edd4f-155">Both issues are easy to address.</span></span> <span data-ttu-id="edd4f-156">En utilisant l’interpolation de chaîne, vous pouvez spécifier des *chaînes de format* qui contrôlent la mise en forme de types particuliers.</span><span class="sxs-lookup"><span data-stu-id="edd4f-156">String interpolation lets you specify *format strings* that control the formatting of particular types.</span></span> <span data-ttu-id="edd4f-157">Modifiez l’appel à `Console.WriteLine` de l’exemple précédent de façon à inclure les chaînes de format pour les expressions de date et de prix, comme indiqué dans la ligne de code suivante :</span><span class="sxs-lookup"><span data-stu-id="edd4f-157">Modify the call to `Console.WriteLine` from the previous example to include the format strings for the date and price expressions as shown in the following line:</span></span>

```csharp
Console.WriteLine($"On {date:d}, the price of {item} was {price:C2} per {unit}.");
```

<span data-ttu-id="edd4f-158">Vous spécifiez une chaîne de format en plaçant après l’expression interpolée un signe deux-points (« : ») et la chaîne de format.</span><span class="sxs-lookup"><span data-stu-id="edd4f-158">You specify a format string by following the interpolated expression with a colon (":") and the format string.</span></span> <span data-ttu-id="edd4f-159">« d » est une [chaîne de format de date et d’heure standard](../../standard/base-types/standard-date-and-time-format-strings.md#the-short-date-d-format-specifier) qui représente le format de date courte.</span><span class="sxs-lookup"><span data-stu-id="edd4f-159">"d" is a [standard date and time format string](../../standard/base-types/standard-date-and-time-format-strings.md#the-short-date-d-format-specifier) that represents the short date format.</span></span> <span data-ttu-id="edd4f-160">« C2 » est une [chaîne de format numérique standard](../../standard/base-types/standard-numeric-format-strings.md#the-currency-c-format-specifier) qui représente un nombre sous forme de valeur monétaire avec deux chiffres après la virgule.</span><span class="sxs-lookup"><span data-stu-id="edd4f-160">"C2" is a  [standard numeric format string](../../standard/base-types/standard-numeric-format-strings.md#the-currency-c-format-specifier) that represents a number as a currency value with two digits after the decimal point.</span></span>

<span data-ttu-id="edd4f-161">Plusieurs types dans les bibliothèques .NET prennent en charge un ensemble prédéfini de chaînes de format.</span><span class="sxs-lookup"><span data-stu-id="edd4f-161">A number of types in the .NET libraries support a predefined set of format strings.</span></span> <span data-ttu-id="edd4f-162">Il s’agit notamment de tous les types numériques et des types de date et d’heure.</span><span class="sxs-lookup"><span data-stu-id="edd4f-162">These include all the numeric types and the date and time types.</span></span> <span data-ttu-id="edd4f-163">Pour obtenir une liste complète des types qui prennent en charge les chaînes de format, consultez [Chaînes de format et types de bibliothèque de classes .NET](../../standard/base-types/formatting-types.md#stringRef) dans l’article [Mise en forme des types dans .NET](../../standard/base-types/formatting-types.md).</span><span class="sxs-lookup"><span data-stu-id="edd4f-163">For a complete list of types that support format strings, see [Format Strings and .NET Class Library Types](../../standard/base-types/formatting-types.md#stringRef) in the [Formatting Types in .NET](../../standard/base-types/formatting-types.md) article.</span></span>

<span data-ttu-id="edd4f-164">Essayez de modifier les chaînes de format dans votre éditeur de texte et, à chaque modification, relancez le programme pour voir comment celles-ci affectent la mise en forme de la date et de l’heure et la valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="edd4f-164">Try modifying the format strings in your text editor and, each time you make a change, rerun the program to see how the changes affect the formatting of the date and time and the numeric value.</span></span> <span data-ttu-id="edd4f-165">Remplacez le « d » dans `{date:d}` par « t » (pour afficher le format d’heure courte), « y » (pour afficher l’année et mois) et « yyyy » (pour afficher l’année sous forme de nombre à quatre chiffres).</span><span class="sxs-lookup"><span data-stu-id="edd4f-165">Change the "d" in `{date:d}` to "t" (to display the short time format), "y" (to display the year and month), and "yyyy" (to display the year as a four-digit number).</span></span> <span data-ttu-id="edd4f-166">Remplacez le « C2 » dans `{price:C2}` par « e » (pour la notation exponentielle) et « F3 » (pour une valeur numérique avec trois chiffres après la virgule).</span><span class="sxs-lookup"><span data-stu-id="edd4f-166">Change the "C2" in `{price:C2}` to "e" (for exponential notation) and "F3" (for a numeric value with three digits after the decimal point).</span></span>

<span data-ttu-id="edd4f-167">En plus de contrôler la mise en forme, vous pouvez contrôler la largeur de champ et l’alignement des chaînes mises en forme qui sont incluses dans la chaîne de résultat.</span><span class="sxs-lookup"><span data-stu-id="edd4f-167">In addition to controlling formatting, you can also control the field width and alignment of the formatted strings that are included in the result string.</span></span> <span data-ttu-id="edd4f-168">Dans la section suivante, vous allez découvrir comment effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="edd4f-168">In the next section, you'll learn how to do this.</span></span>

## <a name="control-the-field-width-and-alignment-of-interpolated-expressions"></a><span data-ttu-id="edd4f-169">Contrôler la largeur de champ et l’alignement des expressions interpolées</span><span class="sxs-lookup"><span data-stu-id="edd4f-169">Control the field width and alignment of interpolated expressions</span></span>

<span data-ttu-id="edd4f-170">En règle générale, quand le résultat d’une expression interpolée est représenté sous forme de chaîne, la chaîne est incluse dans une chaîne de résultat sans espaces de début ou de fin.</span><span class="sxs-lookup"><span data-stu-id="edd4f-170">Ordinarily, when the result of an interpolated expression is formatted to string, that string is included in a result string without leading or trailing spaces.</span></span> <span data-ttu-id="edd4f-171">Contrôler la largeur d’un champ et l’alignement du texte vous permet de rendre une sortie plus lisible, en particulier quand vous utilisez un jeu de données.</span><span class="sxs-lookup"><span data-stu-id="edd4f-171">Particularly when you work with a set of data, being able to control a field width and text alignment helps to produce a more readable output.</span></span> <span data-ttu-id="edd4f-172">Pour voir cela, remplacez tout le code dans votre éditeur de texte par le code suivant, puis tapez `dotnet run` pour exécuter le programme :</span><span class="sxs-lookup"><span data-stu-id="edd4f-172">To see this, replace all the code in your text editor with the following code, then type `dotnet run` to execute the program:</span></span>

```csharp
using System;
using System.Collections.Generic;

public class Example
{
   public static void Main()
   {
      var titles = new Dictionary<string, string>()
      {
          ["Doyle, Arthur Conan"] = "Hound of the Baskervilles, The",
          ["London, Jack"] = "Call of the Wild, The",
          ["Shakespeare, William"] = "Tempest, The"
      };

      Console.WriteLine("Author and Title List");
      Console.WriteLine();
      Console.WriteLine($"|{"Author",-25}|{"Title",30}|");
      foreach (var title in titles)
         Console.WriteLine($"|{title.Key,-25}|{title.Value,30}|");
   }
}
```

<span data-ttu-id="edd4f-173">Les noms des auteurs sont alignés à gauche, et leurs titres sont alignés à droite.</span><span class="sxs-lookup"><span data-stu-id="edd4f-173">The names of authors are left-aligned, and the titles they wrote are right-aligned.</span></span> <span data-ttu-id="edd4f-174">Vous spécifiez l’alignement en ajoutant une virgule (« , ») après une expression interpolée et en spécifiant la largeur de champ *minimum*.</span><span class="sxs-lookup"><span data-stu-id="edd4f-174">You specify the alignment by adding a comma (",") after an interpolated expression and designating the *minimum* field width.</span></span> <span data-ttu-id="edd4f-175">Si la valeur spécifiée est un nombre positif, le champ est aligné à droite.</span><span class="sxs-lookup"><span data-stu-id="edd4f-175">If the specified value is a positive number, the field is right-aligned.</span></span> <span data-ttu-id="edd4f-176">Si c’est un nombre négatif, le champ est aligné à gauche.</span><span class="sxs-lookup"><span data-stu-id="edd4f-176">If it is a negative number, the field is left-aligned.</span></span>

<span data-ttu-id="edd4f-177">Essayez de supprimer les signes négatifs du code `{"Author",-25}` et `{title.Key,-25}`, puis réexécutez l’exemple, comme avec le code suivant :</span><span class="sxs-lookup"><span data-stu-id="edd4f-177">Try removing the negative signs from the `{"Author",-25}` and `{title.Key,-25}` code and run the example again, as the following code does:</span></span>

```csharp
Console.WriteLine($"|{"Author",25}|{"Title",30}|");
foreach (var title in titles)
   Console.WriteLine($"|{title.Key,25}|{title.Value,30}|");
```

<span data-ttu-id="edd4f-178">Cette fois, les informations sur l’auteur sont alignées à droite.</span><span class="sxs-lookup"><span data-stu-id="edd4f-178">This time, the author information is right-aligned.</span></span>

<span data-ttu-id="edd4f-179">Vous pouvez combiner un spécificateur d’alignement et une chaîne de format pour une même expression interpolée.</span><span class="sxs-lookup"><span data-stu-id="edd4f-179">You can combine an alignment specifier and a format string for a single interpolated expression.</span></span> <span data-ttu-id="edd4f-180">Pour cela, spécifiez d’abord l’alignement, puis un signe deux-points et la chaîne de format.</span><span class="sxs-lookup"><span data-stu-id="edd4f-180">To do that, specify the alignment first, followed by a colon and the format string.</span></span> <span data-ttu-id="edd4f-181">Remplacez tout le code à l’intérieur de la méthode `Main` par le code suivant, qui affiche trois chaînes mises en forme avec des largeurs de champ définies.</span><span class="sxs-lookup"><span data-stu-id="edd4f-181">Replace all of the code inside the `Main` method with the following code, which displays three formatted strings with defined field widths.</span></span> <span data-ttu-id="edd4f-182">Ensuite, exécutez le programme en entrant la commande `dotnet run`.</span><span class="sxs-lookup"><span data-stu-id="edd4f-182">Then run the program by entering the `dotnet run` command.</span></span>

```csharp
Console.WriteLine($"[{DateTime.Now,-20:d}] Hour [{DateTime.Now,-10:HH}] [{1063.342,15:N2}] feet");
```

<span data-ttu-id="edd4f-183">La sortie ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="edd4f-183">The output looks something like the following:</span></span>

```console
[04/14/2018          ] Hour [16        ] [       1,063.34] feet
```

<span data-ttu-id="edd4f-184">Vous avez terminé le guide de démarrage rapide sur l’interpolation de chaîne.</span><span class="sxs-lookup"><span data-stu-id="edd4f-184">You've completed the string interpolation quickstart.</span></span>

<span data-ttu-id="edd4f-185">Vous pouvez maintenant suivre le guide de démarrage rapide [Collection de listes](arrays-and-collections.md) dans votre propre environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="edd4f-185">You can continue with the [List collection](arrays-and-collections.md) quickstart in your own development environment.</span></span>

<span data-ttu-id="edd4f-186">Pour plus d’informations sur l’interpolation de chaîne, consultez la rubrique [Interpolation de chaîne](../language-reference/tokens/interpolated.md) dans les informations de référence sur C#.</span><span class="sxs-lookup"><span data-stu-id="edd4f-186">Learn more about string interpolation in the [String interpolation](../language-reference/tokens/interpolated.md) topic in the C# Reference.</span></span>
