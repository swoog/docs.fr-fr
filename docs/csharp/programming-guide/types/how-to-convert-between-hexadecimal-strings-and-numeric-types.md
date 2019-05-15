---
title: 'Procédure : Effectuer une conversion entre des chaînes hexadécimales et des types numériques - Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- hexadecimal strings [C#], converting to numeric type
- conversions [C#], hexidecimal strings
- strings [C#], converting hexadecimal strings
- hexadecimal strings [C#]
ms.assetid: 7115c49f-7d1d-40c3-8bd9-aae0cc1d46b6
ms.openlocfilehash: 99d30d6c2b50569312ff2d732a34020ab29ce81c
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64595070"
---
# <a name="how-to-convert-between-hexadecimal-strings-and-numeric-types-c-programming-guide"></a><span data-ttu-id="1de97-102">Procédure : Effectuer une conversion entre des chaînes hexadécimales et des types numériques (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="1de97-102">How to: Convert Between Hexadecimal Strings and Numeric Types (C# Programming Guide)</span></span>
<span data-ttu-id="1de97-103">Ces exemples montrent comment effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="1de97-103">These examples show you how to perform the following tasks:</span></span>  
  
- <span data-ttu-id="1de97-104">Obtenir la valeur hexadécimale de chaque caractère dans une chaîne ([string](../../../csharp/language-reference/keywords/string.md)).</span><span class="sxs-lookup"><span data-stu-id="1de97-104">Obtain the hexadecimal value of each character in a [string](../../../csharp/language-reference/keywords/string.md).</span></span>  
  
- <span data-ttu-id="1de97-105">Obtenir la valeur [char](../../../csharp/language-reference/keywords/char.md) qui correspond à chaque valeur d’une chaîne hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="1de97-105">Obtain the [char](../../../csharp/language-reference/keywords/char.md) that corresponds to each value in a hexadecimal string.</span></span>  
  
- <span data-ttu-id="1de97-106">Convertir une `string` hexadécimale en [int](../../../csharp/language-reference/keywords/int.md).</span><span class="sxs-lookup"><span data-stu-id="1de97-106">Convert a hexadecimal `string` to an [int](../../../csharp/language-reference/keywords/int.md).</span></span>  
  
- <span data-ttu-id="1de97-107">Convertir une `string` hexadécimale en [float](../../../csharp/language-reference/keywords/float.md).</span><span class="sxs-lookup"><span data-stu-id="1de97-107">Convert a hexadecimal `string` to a [float](../../../csharp/language-reference/keywords/float.md).</span></span>  
  
- <span data-ttu-id="1de97-108">Convertir un tableau d’[octets](../../../csharp/language-reference/keywords/byte.md) en `string` hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="1de97-108">Convert a [byte](../../../csharp/language-reference/keywords/byte.md) array to a hexadecimal `string`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1de97-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="1de97-109">Example</span></span>  
 <span data-ttu-id="1de97-110">Cet exemple génère la valeur hexadécimale de chaque caractère dans une `string`.</span><span class="sxs-lookup"><span data-stu-id="1de97-110">This example outputs the hexadecimal value of each character in a `string`.</span></span> <span data-ttu-id="1de97-111">Il convertit d’abord la `string` en un tableau de caractères.</span><span class="sxs-lookup"><span data-stu-id="1de97-111">First it parses the `string` to an array of characters.</span></span> <span data-ttu-id="1de97-112">Ensuite, il appelle <xref:System.Convert.ToInt32%28System.Char%29> sur chaque caractère afin d’obtenir sa valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="1de97-112">Then it calls <xref:System.Convert.ToInt32%28System.Char%29> on each character to obtain its numeric value.</span></span> <span data-ttu-id="1de97-113">Pour finir, il représente le nombre sous forme hexadécimale dans une `string`.</span><span class="sxs-lookup"><span data-stu-id="1de97-113">Finally, it formats the number as its hexadecimal representation in a `string`.</span></span>  
  
 [!code-csharp[csProgGuideTypes#30](~/samples/snippets/csharp/VS_Snippets_VBCSharp/CsProgGuideTypes/CS/Class1.cs#30)]  
  
## <a name="example"></a><span data-ttu-id="1de97-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="1de97-114">Example</span></span>  
 <span data-ttu-id="1de97-115">Cet exemple analyse une `string` de valeurs hexadécimales et génère le caractère correspondant à chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="1de97-115">This example parses a `string` of hexadecimal values and outputs the character corresponding to each hexadecimal value.</span></span> <span data-ttu-id="1de97-116">Il appelle d’abord la méthode [Split(Char\[\])](xref:System.String.Split(System.Char[])) pour obtenir chaque valeur hexadécimale sous la forme d’une `string` individuelle dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="1de97-116">First it calls the [Split(Char\[\])](xref:System.String.Split(System.Char[])) method to obtain each hexadecimal value as an individual `string` in an array.</span></span> <span data-ttu-id="1de97-117">Ensuite, il appelle <xref:System.Convert.ToInt32%28System.String%2CSystem.Int32%29> pour convertir la valeur hexadécimale en valeur décimale représentée sous forme d’objet [int](../../../csharp/language-reference/keywords/int.md). Il illustre deux manières d’obtenir le caractère correspondant à ce code de caractère.</span><span class="sxs-lookup"><span data-stu-id="1de97-117">Then it calls <xref:System.Convert.ToInt32%28System.String%2CSystem.Int32%29> to convert the hexadecimal value to a decimal value represented as an [int](../../../csharp/language-reference/keywords/int.md). It shows two different ways to obtain the character corresponding to that character code.</span></span> <span data-ttu-id="1de97-118">La première technique utilise `string`, qui retourne le caractère correspondant à l’argument entier sous forme de <xref:System.Char.ConvertFromUtf32%28System.Int32%29>.</span><span class="sxs-lookup"><span data-stu-id="1de97-118">The first technique uses <xref:System.Char.ConvertFromUtf32%28System.Int32%29>, which returns the character corresponding to the integer argument as a `string`.</span></span> <span data-ttu-id="1de97-119">La deuxième technique effectue un cast explicite de l’`int` en [char](../../../csharp/language-reference/keywords/char.md).</span><span class="sxs-lookup"><span data-stu-id="1de97-119">The second technique explicitly casts the `int` to a [char](../../../csharp/language-reference/keywords/char.md).</span></span>  
  
 [!code-csharp[csProgGuideTypes#31](~/samples/snippets/csharp/VS_Snippets_VBCSharp/CsProgGuideTypes/CS/Class1.cs#31)]  
  
## <a name="example"></a><span data-ttu-id="1de97-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="1de97-120">Example</span></span>  
 <span data-ttu-id="1de97-121">Cet exemple montre une autre façon de convertir un `string` hexadécimal en entier, en appelant la méthode <xref:System.Int32.Parse%28System.String%2CSystem.Globalization.NumberStyles%29>.</span><span class="sxs-lookup"><span data-stu-id="1de97-121">This example shows another way to convert a hexadecimal `string` to an integer, by calling the <xref:System.Int32.Parse%28System.String%2CSystem.Globalization.NumberStyles%29> method.</span></span>  
  
 [!code-csharp[csProgGuideTypes#32](~/samples/snippets/csharp/VS_Snippets_VBCSharp/CsProgGuideTypes/CS/Class1.cs#32)]  
  
## <a name="example"></a><span data-ttu-id="1de97-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="1de97-122">Example</span></span>  
 <span data-ttu-id="1de97-123">L’exemple suivant montre comment convertir un `string` hexadécimal en [float](../../../csharp/language-reference/keywords/float.md) à l’aide de la classe <xref:System.BitConverter?displayProperty=nameWithType> et de la méthode <xref:System.UInt32.Parse%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="1de97-123">The following example shows how to convert a hexadecimal `string` to a [float](../../../csharp/language-reference/keywords/float.md) by using the <xref:System.BitConverter?displayProperty=nameWithType> class and the <xref:System.UInt32.Parse%2A?displayProperty=nameWithType> method.</span></span>  
  
 [!code-csharp[csProgGuideTypes#39](~/samples/snippets/csharp/VS_Snippets_VBCSharp/CsProgGuideTypes/CS/Class1.cs#39)]  
  
## <a name="example"></a><span data-ttu-id="1de97-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="1de97-124">Example</span></span>  
 <span data-ttu-id="1de97-125">L’exemple suivant montre comment convertir un tableau d’[octets](../../../csharp/language-reference/keywords/byte.md) en chaîne hexadécimale à l’aide de la classe <xref:System.BitConverter?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="1de97-125">The following example shows how to convert a [byte](../../../csharp/language-reference/keywords/byte.md) array to a hexadecimal string by using the <xref:System.BitConverter?displayProperty=nameWithType> class.</span></span>  
  
 [!code-csharp[csProgGuideTypes#38](~/samples/snippets/csharp/VS_Snippets_VBCSharp/CsProgGuideTypes/CS/Class1.cs#38)]  
  
## <a name="see-also"></a><span data-ttu-id="1de97-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1de97-126">See also</span></span>

- [<span data-ttu-id="1de97-127">Standard Numeric Format Strings</span><span class="sxs-lookup"><span data-stu-id="1de97-127">Standard Numeric Format Strings</span></span>](../../../standard/base-types/standard-numeric-format-strings.md)
- [<span data-ttu-id="1de97-128">Types</span><span class="sxs-lookup"><span data-stu-id="1de97-128">Types</span></span>](../../../csharp/programming-guide/types/index.md)
- [<span data-ttu-id="1de97-129">Guide pratique pour déterminer si une chaîne représente une valeur numérique</span><span class="sxs-lookup"><span data-stu-id="1de97-129">How to: Determine Whether a String Represents a Numeric Value</span></span>](../../../csharp/programming-guide/strings/how-to-determine-whether-a-string-represents-a-numeric-value.md)
