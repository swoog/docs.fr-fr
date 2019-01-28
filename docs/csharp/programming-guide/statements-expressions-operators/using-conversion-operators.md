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
ms.openlocfilehash: d6b271c0d716a9b5dfb49b825d843d4345471147
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54578570"
---
# <a name="using-conversion-operators-c-programming-guide"></a><span data-ttu-id="f2ced-102">Utilisation d'opérateurs de conversion (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="f2ced-102">Using Conversion Operators (C# Programming Guide)</span></span>
<span data-ttu-id="f2ced-103">Vous pouvez utiliser des opérateurs de conversion `implicit`, qui sont plus faciles à utiliser, ou des opérateurs de conversion `explicit`, qui indiquent clairement à toute personne lisant le code que vous convertissez un type.</span><span class="sxs-lookup"><span data-stu-id="f2ced-103">You can use `implicit` conversion operators, which are easier to use, or `explicit` conversion operators, which clearly indicate to anyone reading the code that you're converting a type.</span></span> <span data-ttu-id="f2ced-104">Cette rubrique illustre les deux types d’opérateurs de conversion.</span><span class="sxs-lookup"><span data-stu-id="f2ced-104">This topic demonstrates both types of conversion operator.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f2ced-105">Pour plus d’informations sur les conversions de type simple, consultez [Guide pratique pour convertir une chaîne en nombre](../../../csharp/programming-guide/types/how-to-convert-a-string-to-a-number.md), [Guide pratique pour convertir un tableau d’octets en int](../../../csharp/programming-guide/types/how-to-convert-a-byte-array-to-an-int.md), [Guide pratique pour effectuer une conversion entre des chaînes hexadécimales et des types numériques](../../../csharp/programming-guide/types/how-to-convert-between-hexadecimal-strings-and-numeric-types.md) ou <xref:System.Convert>.</span><span class="sxs-lookup"><span data-stu-id="f2ced-105">For information about simple type conversions, see [How to: Convert a String to a Number](../../../csharp/programming-guide/types/how-to-convert-a-string-to-a-number.md), [How to: Convert a byte Array to an int](../../../csharp/programming-guide/types/how-to-convert-a-byte-array-to-an-int.md), [How to: Convert Between Hexadecimal Strings and Numeric Types](../../../csharp/programming-guide/types/how-to-convert-between-hexadecimal-strings-and-numeric-types.md), or <xref:System.Convert>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f2ced-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="f2ced-106">Example</span></span>  
 <span data-ttu-id="f2ced-107">Voici un exemple d’opérateur de conversion explicite.</span><span class="sxs-lookup"><span data-stu-id="f2ced-107">This is an example of an explicit conversion operator.</span></span> <span data-ttu-id="f2ced-108">Cet opérateur convertit le type <xref:System.Byte> en un type valeur appelé `Digit`.</span><span class="sxs-lookup"><span data-stu-id="f2ced-108">This operator converts from the type <xref:System.Byte> to a value type called `Digit`.</span></span> <span data-ttu-id="f2ced-109">Étant donné que tous les octets ne pouvant pas être convertis en un chiffre, la conversion est explicite, ce qui signifie qu’un cast doit être utilisé, comme indiqué dans la méthode `Main`.</span><span class="sxs-lookup"><span data-stu-id="f2ced-109">Because not all bytes can be converted to a digit, the conversion is explicit, meaning that a cast must be used, as shown in the `Main` method.</span></span>  
  
 [!code-csharp[csProgGuideStatements#11](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/using-conversion-operators_1.cs)]  
  
## <a name="example"></a><span data-ttu-id="f2ced-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="f2ced-110">Example</span></span>  
 <span data-ttu-id="f2ced-111">L’exemple suivant montre un opérateur de conversion implicite en définissant un opérateur de conversion qui annule ce que l’exemple précédent a fait : il effectue une conversion d’une classe de valeur appelée `Digit` en type <xref:System.Byte> intégral.</span><span class="sxs-lookup"><span data-stu-id="f2ced-111">This example demonstrates an implicit conversion operator by defining a conversion operator that undoes what the previous example did: it converts from a value class called `Digit` to the integral <xref:System.Byte> type.</span></span> <span data-ttu-id="f2ced-112">Étant donné que tout chiffre peut être converti en <xref:System.Byte>, il n’est pas nécessaire de forcer les utilisateurs à être explicites à propos de la conversion.</span><span class="sxs-lookup"><span data-stu-id="f2ced-112">Because any digit can be converted to a <xref:System.Byte>, there's no need to force users to be explicit about the conversion.</span></span>  
  
 [!code-csharp[csProgGuideStatements#12](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/using-conversion-operators_2.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="f2ced-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2ced-113">See also</span></span>

- [<span data-ttu-id="f2ced-114">Référence C#</span><span class="sxs-lookup"><span data-stu-id="f2ced-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="f2ced-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="f2ced-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="f2ced-116">Opérateurs de conversion</span><span class="sxs-lookup"><span data-stu-id="f2ced-116">Conversion Operators</span></span>](../../../csharp/programming-guide/statements-expressions-operators/conversion-operators.md)
- [<span data-ttu-id="f2ced-117">is</span><span class="sxs-lookup"><span data-stu-id="f2ced-117">is</span></span>](../../../csharp/language-reference/keywords/is.md)
