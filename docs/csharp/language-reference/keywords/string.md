---
title: string (référence C#)
ms.date: 07/20/2015
f1_keywords:
- string
- string_CSharpKeyword
helpviewer_keywords:
- strings [C#], reference
- '@ string literal'
- string literals [C#]
- string keyword [C#]
ms.assetid: 3037e558-fb22-494d-bca1-a15ade11b11a
ms.openlocfilehash: 66b1729363878f69f868b8b8fd6e9e7011426f27
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53153122"
---
# <a name="string-c-reference"></a><span data-ttu-id="4f52d-102">string (référence C#)</span><span class="sxs-lookup"><span data-stu-id="4f52d-102">string (C# Reference)</span></span>

<span data-ttu-id="4f52d-103">Le type `string` représente une séquence de zéro, un ou plusieurs caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="4f52d-103">The `string` type represents a sequence of zero or more Unicode characters.</span></span> <span data-ttu-id="4f52d-104">`string` est un alias de <xref:System.String> dans .NET.</span><span class="sxs-lookup"><span data-stu-id="4f52d-104">`string` is an alias for <xref:System.String> in .NET.</span></span>

<span data-ttu-id="4f52d-105">Bien que `string` soit un type référence, les opérateurs d’égalité (`==` et `!=`) sont définis pour comparer les valeurs d’objets `string`, pas les références.</span><span class="sxs-lookup"><span data-stu-id="4f52d-105">Although `string` is a reference type, the equality operators (`==` and `!=`) are defined to compare the values of `string` objects, not references.</span></span> <span data-ttu-id="4f52d-106">Cela permet de tester l’égalité de chaînes de façon plus intuitive.</span><span class="sxs-lookup"><span data-stu-id="4f52d-106">This makes testing for string equality more intuitive.</span></span> <span data-ttu-id="4f52d-107">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4f52d-107">For example:</span></span>

```csharp
string a = "hello";
string b = "h";
// Append to contents of 'b'
b += "ello";
Console.WriteLine(a == b);
Console.WriteLine((object)a == (object)b);
```

<span data-ttu-id="4f52d-108">Cette opération affiche « True », puis « False », car le contenu des chaînes est équivalent, mais `a` et `b` ne font pas référence à la même instance de chaîne.</span><span class="sxs-lookup"><span data-stu-id="4f52d-108">This displays "True" and then "False" because the content of the strings are equivalent, but `a` and `b` do not refer to the same string instance.</span></span>

<span data-ttu-id="4f52d-109">L’opérateur + concatène les chaînes :</span><span class="sxs-lookup"><span data-stu-id="4f52d-109">The + operator concatenates strings:</span></span>

```csharp
string a = "good " + "morning";
```

<span data-ttu-id="4f52d-110">Cela crée un objet String qui contient « good morning ».</span><span class="sxs-lookup"><span data-stu-id="4f52d-110">This creates a string object that contains "good morning".</span></span>

<span data-ttu-id="4f52d-111">Les chaînes sont *immuables* : il est impossible de changer le contenu d’un objet String après avoir créé l’objet, bien que la syntaxe semble indiquer le contraire.</span><span class="sxs-lookup"><span data-stu-id="4f52d-111">Strings are *immutable*--the contents of a string object cannot be changed after the object is created, although the syntax makes it appear as if you can do this.</span></span> <span data-ttu-id="4f52d-112">Par exemple, lorsque vous écrivez ce code, le compilateur crée en fait un nouvel objet String pour stocker la nouvelle séquence de caractères, et ce nouvel objet est assigné à b.</span><span class="sxs-lookup"><span data-stu-id="4f52d-112">For example, when you write this code, the compiler actually creates a new string object to hold the new sequence of characters, and that new object is assigned to b.</span></span> <span data-ttu-id="4f52d-113">La chaîne « h » est alors disponible pour le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="4f52d-113">The string "h" is then eligible for garbage collection.</span></span>

```csharp
string b = "h";
b += "ello";
```

<span data-ttu-id="4f52d-114">L’opérateur [] peut être utilisé pour un accès en lecture seule aux différents caractères d’un objet `string` :</span><span class="sxs-lookup"><span data-stu-id="4f52d-114">The [] operator can be used for readonly access to individual characters of a `string`:</span></span>

```csharp
string str = "test";
char x = str[2];  // x = 's';
```

<span data-ttu-id="4f52d-115">Les littéraux de chaîne sont de type `string` et peuvent être écrits sous deux formes, entre guillemets et @-quoted.</span><span class="sxs-lookup"><span data-stu-id="4f52d-115">String literals are of type `string` and can be written in two forms, quoted and @-quoted.</span></span> <span data-ttu-id="4f52d-116">Les littéraux de chaîne entre guillemets sont placés entre guillemets doubles (") :</span><span class="sxs-lookup"><span data-stu-id="4f52d-116">Quoted string literals are enclosed in double quotation marks ("):</span></span>

```csharp
"good morning"  // a string literal
```

<span data-ttu-id="4f52d-117">Les littéraux de chaîne peuvent contenir tout littéral de caractère.</span><span class="sxs-lookup"><span data-stu-id="4f52d-117">String literals can contain any character literal.</span></span> <span data-ttu-id="4f52d-118">Les séquences d’échappement sont incluses.</span><span class="sxs-lookup"><span data-stu-id="4f52d-118">Escape sequences are included.</span></span> <span data-ttu-id="4f52d-119">L’exemple suivant utilise la séquence d’échappement `\\` pour la barre oblique inverse, `\u0066` pour la lettre f et `\n` pour un saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="4f52d-119">The following example uses escape sequence `\\` for backslash, `\u0066` for the letter f, and `\n` for newline.</span></span>

```csharp
string a = "\\\u0066\n";
Console.WriteLine(a);
```

> [!NOTE]
> <span data-ttu-id="4f52d-120">Le code d’échappement `\udddd` (où `dddd` est un nombre à quatre chiffres) représente le caractère Unicode U+`dddd`.</span><span class="sxs-lookup"><span data-stu-id="4f52d-120">The escape code `\udddd` (where `dddd` is a four-digit number) represents the Unicode character U+`dddd`.</span></span> <span data-ttu-id="4f52d-121">Les codes d’échappement Unicode à huit chiffres sont également reconnus : `\Udddddddd`.</span><span class="sxs-lookup"><span data-stu-id="4f52d-121">Eight-digit Unicode escape codes are also recognized: `\Udddddddd`.</span></span>

<span data-ttu-id="4f52d-122">Les littéraux de chaîne textuelle commencent par `@` et sont placés entre guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="4f52d-122">Verbatim string literals start with `@` and are also enclosed in double quotation marks.</span></span> <span data-ttu-id="4f52d-123">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4f52d-123">For example:</span></span>

```csharp
@"good morning"  // a string literal
```

<span data-ttu-id="4f52d-124">L’avantage des chaînes textuelles est que les séquences d’échappement *ne sont pas* traitées, ce qui facilite l’écriture, par exemple, d’un nom de fichier complet :</span><span class="sxs-lookup"><span data-stu-id="4f52d-124">The advantage of verbatim strings is that escape sequences are *not* processed, which makes it easy to write, for example, a fully qualified file name:</span></span>

```csharp
@"c:\Docs\Source\a.txt"  // rather than "c:\\Docs\\Source\\a.txt"
```

<span data-ttu-id="4f52d-125">Pour inclure un guillemet double dans une chaîne @-quoted, doublez-le :</span><span class="sxs-lookup"><span data-stu-id="4f52d-125">To include a double quotation mark in an @-quoted string, double it:</span></span>

```csharp
@"""Ahoy!"" cried the captain." // "Ahoy!" cried the captain.
```

<span data-ttu-id="4f52d-126">Pour d’autres utilisations du caractère spécial `@`, consultez [@ -- Identificateur de chaîne textuelle](../tokens/verbatim.md).</span><span class="sxs-lookup"><span data-stu-id="4f52d-126">For other uses of the `@` special character, see [@ -- verbatim identifier](../tokens/verbatim.md).</span></span>

<span data-ttu-id="4f52d-127">Pour plus d’informations sur les chaînes en C#, consultez la rubrique [Chaînes](../../programming-guide/strings/index.md).</span><span class="sxs-lookup"><span data-stu-id="4f52d-127">For more information about strings in C#, see [Strings](../../programming-guide/strings/index.md).</span></span>

## <a name="example"></a><span data-ttu-id="4f52d-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="4f52d-128">Example</span></span>

[!code-csharp[csrefKeywordsTypes#17](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#17)]  

## <a name="c-language-specification"></a><span data-ttu-id="4f52d-129">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="4f52d-129">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="4f52d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f52d-130">See also</span></span>

- [<span data-ttu-id="4f52d-131">Référence C#</span><span class="sxs-lookup"><span data-stu-id="4f52d-131">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="4f52d-132">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="4f52d-132">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="4f52d-133">Bonnes pratiques pour l’utilisation de chaînes</span><span class="sxs-lookup"><span data-stu-id="4f52d-133">Best Practices for Using Strings</span></span>](../../../standard/base-types/best-practices-strings.md)
- [<span data-ttu-id="4f52d-134">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="4f52d-134">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="4f52d-135">Types référence</span><span class="sxs-lookup"><span data-stu-id="4f52d-135">Reference Types</span></span>](reference-types.md)
- [<span data-ttu-id="4f52d-136">Types valeur</span><span class="sxs-lookup"><span data-stu-id="4f52d-136">Value Types</span></span>](value-types.md)
- [<span data-ttu-id="4f52d-137">Opérations de chaînes de base</span><span class="sxs-lookup"><span data-stu-id="4f52d-137">Basic String Operations</span></span>](../../../standard/base-types/basic-string-operations.md)
- [<span data-ttu-id="4f52d-138">Création de chaînes</span><span class="sxs-lookup"><span data-stu-id="4f52d-138">Creating New Strings</span></span>](../../../standard/base-types/creating-new.md)
- [<span data-ttu-id="4f52d-139">Tableau des formats des résultats numériques</span><span class="sxs-lookup"><span data-stu-id="4f52d-139">Formatting Numeric Results Table</span></span>](formatting-numeric-results-table.md)
