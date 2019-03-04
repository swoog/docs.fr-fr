---
title: Utilisation d'opérateurs de conversion - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- conversions [C#], operators
- conversion operators [C#]
- operators [C#], conversion
- user-defined conversions [C#]
- implicit conversion operators [C#]
- explicit conversion operators [C#]
ms.assetid: caf36e89-c6c0-4b87-9f9e-85780a45c9a4
ms.openlocfilehash: 888339661ba1cb2e0b702f284d9f27b3217e74c1
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56973156"
---
# <a name="using-conversion-operators-c-programming-guide"></a><span data-ttu-id="f0e99-102">Utilisation d'opérateurs de conversion (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="f0e99-102">Using Conversion Operators (C# Programming Guide)</span></span>
<span data-ttu-id="f0e99-103">Vous pouvez utiliser des opérateurs de conversion `implicit`, qui sont plus faciles à utiliser, ou des opérateurs de conversion `explicit`, qui indiquent clairement à toute personne lisant le code que vous convertissez un type.</span><span class="sxs-lookup"><span data-stu-id="f0e99-103">You can use `implicit` conversion operators, which are easier to use, or `explicit` conversion operators, which clearly indicate to anyone reading the code that you're converting a type.</span></span> <span data-ttu-id="f0e99-104">Cette rubrique illustre les deux types d’opérateurs de conversion.</span><span class="sxs-lookup"><span data-stu-id="f0e99-104">This topic demonstrates both types of conversion operator.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f0e99-105">Pour plus d’informations sur les conversions de type simple, consultez [Guide pratique pour convertir une chaîne en nombre](../../../csharp/programming-guide/types/how-to-convert-a-string-to-a-number.md), [Guide pratique pour convertir un tableau d’octets en int](../../../csharp/programming-guide/types/how-to-convert-a-byte-array-to-an-int.md), [Guide pratique pour effectuer une conversion entre des chaînes hexadécimales et des types numériques](../../../csharp/programming-guide/types/how-to-convert-between-hexadecimal-strings-and-numeric-types.md) ou <xref:System.Convert>.</span><span class="sxs-lookup"><span data-stu-id="f0e99-105">For information about simple type conversions, see [How to: Convert a String to a Number](../../../csharp/programming-guide/types/how-to-convert-a-string-to-a-number.md), [How to: Convert a byte Array to an int](../../../csharp/programming-guide/types/how-to-convert-a-byte-array-to-an-int.md), [How to: Convert Between Hexadecimal Strings and Numeric Types](../../../csharp/programming-guide/types/how-to-convert-between-hexadecimal-strings-and-numeric-types.md), or <xref:System.Convert>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f0e99-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="f0e99-106">Example</span></span>  
 <span data-ttu-id="f0e99-107">Voici un exemple d’opérateur de conversion explicite.</span><span class="sxs-lookup"><span data-stu-id="f0e99-107">This is an example of an explicit conversion operator.</span></span> <span data-ttu-id="f0e99-108">Cet opérateur convertit le type <xref:System.Byte> en un type valeur appelé `Digit`.</span><span class="sxs-lookup"><span data-stu-id="f0e99-108">This operator converts from the type <xref:System.Byte> to a value type called `Digit`.</span></span> <span data-ttu-id="f0e99-109">Étant donné que tous les octets ne pouvant pas être convertis en un chiffre, la conversion est explicite, ce qui signifie qu’un cast doit être utilisé, comme indiqué dans la méthode `Main`.</span><span class="sxs-lookup"><span data-stu-id="f0e99-109">Because not all bytes can be converted to a digit, the conversion is explicit, meaning that a cast must be used, as shown in the `Main` method.</span></span>  
  
 [!code-csharp[csProgGuideStatements#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideStatements/CS/Statements.cs#11)]  
  
## <a name="example"></a><span data-ttu-id="f0e99-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="f0e99-110">Example</span></span>  
 <span data-ttu-id="f0e99-111">L’exemple suivant montre un opérateur de conversion implicite en définissant un opérateur de conversion qui annule ce que l’exemple précédent a fait : il effectue une conversion d’une classe de valeur appelée `Digit` en type <xref:System.Byte> intégral.</span><span class="sxs-lookup"><span data-stu-id="f0e99-111">This example demonstrates an implicit conversion operator by defining a conversion operator that undoes what the previous example did: it converts from a value class called `Digit` to the integral <xref:System.Byte> type.</span></span> <span data-ttu-id="f0e99-112">Étant donné que tout chiffre peut être converti en <xref:System.Byte>, il n’est pas nécessaire de forcer les utilisateurs à être explicites à propos de la conversion.</span><span class="sxs-lookup"><span data-stu-id="f0e99-112">Because any digit can be converted to a <xref:System.Byte>, there's no need to force users to be explicit about the conversion.</span></span>  
  
 [!code-csharp[csProgGuideStatements#12](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideStatements/CS/Statements.cs#12)]  
  
## <a name="see-also"></a><span data-ttu-id="f0e99-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0e99-113">See also</span></span>

- [<span data-ttu-id="f0e99-114">Référence C#</span><span class="sxs-lookup"><span data-stu-id="f0e99-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="f0e99-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="f0e99-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="f0e99-116">Opérateurs de conversion</span><span class="sxs-lookup"><span data-stu-id="f0e99-116">Conversion Operators</span></span>](../../../csharp/programming-guide/statements-expressions-operators/conversion-operators.md)
- [<span data-ttu-id="f0e99-117">is</span><span class="sxs-lookup"><span data-stu-id="f0e99-117">is</span></span>](../../../csharp/language-reference/keywords/is.md)
