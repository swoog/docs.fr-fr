---
title: Accès à une chaîne de base zéro et Accès d’une chaîne de base dans Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], indexing
ms.assetid: 0ed39f35-d68e-421d-ae14-460a5c0373b8
ms.openlocfilehash: cc8f286de41d7e44225e889e73ff3c7b1fdbd881
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65591747"
---
# <a name="zero-based-vs-one-based-string-access-in-visual-basic"></a><span data-ttu-id="b9cd0-102">Accès à une chaîne de base zéro et Accès d’une chaîne de base dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b9cd0-102">Zero-based vs. One-based String Access in Visual Basic</span></span>
<span data-ttu-id="b9cd0-103">Cette rubrique compare la façon dont Visual Basic et .NET Framework fournissent l’accès aux caractères dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="b9cd0-103">This topic compares how Visual Basic and the .NET Framework provide access to the characters in a string.</span></span> <span data-ttu-id="b9cd0-104">Le .NET Framework fournit toujours un accès de base zéro aux caractères dans une chaîne, tandis que Visual Basic fournit l’accès de base zéro et un, en fonction de la fonction.</span><span class="sxs-lookup"><span data-stu-id="b9cd0-104">The .NET Framework always provides zero-based access to the characters in a string, whereas Visual Basic provides zero-based and one-based access, depending on the function.</span></span>  
  
## <a name="one-based"></a><span data-ttu-id="b9cd0-105">Basé sur un</span><span class="sxs-lookup"><span data-stu-id="b9cd0-105">One-Based</span></span>  
 <span data-ttu-id="b9cd0-106">Pour obtenir un exemple d’une fonction Visual Basic basé sur 1, envisagez le `Mid` (fonction).</span><span class="sxs-lookup"><span data-stu-id="b9cd0-106">For an example of a one-based Visual Basic function, consider the `Mid` function.</span></span> <span data-ttu-id="b9cd0-107">Il accepte un argument qui indique la position de caractère à laquelle la sous-chaîne démarre, en commençant à la position 1.</span><span class="sxs-lookup"><span data-stu-id="b9cd0-107">It takes an argument that indicates the character position at which the substring will start, starting with position 1.</span></span> <span data-ttu-id="b9cd0-108">Le .NET Framework <xref:System.String.Substring%2A?displayProperty=nameWithType> méthode prend un index du caractère dans la chaîne à laquelle la sous-chaîne doit démarrer, en commençant à la position 0.</span><span class="sxs-lookup"><span data-stu-id="b9cd0-108">The .NET Framework <xref:System.String.Substring%2A?displayProperty=nameWithType> method takes an index of the character in the string at which the substring is to start, starting with position 0.</span></span> <span data-ttu-id="b9cd0-109">Par conséquent, si vous avez une chaîne « ABCDE », les caractères individuels sont numérotés 1,2,3,4,5 pour une utilisation avec le `Mid` (fonction), mais 0,1,2,3,4 pour une utilisation avec le <xref:System.String.Substring%2A?displayProperty=nameWithType> (méthode).</span><span class="sxs-lookup"><span data-stu-id="b9cd0-109">Thus, if you have a string "ABCDE", the individual characters are numbered 1,2,3,4,5 for use with the `Mid` function, but 0,1,2,3,4 for use with the <xref:System.String.Substring%2A?displayProperty=nameWithType> method.</span></span>  
  
## <a name="zero-based"></a><span data-ttu-id="b9cd0-110">Base zéro</span><span class="sxs-lookup"><span data-stu-id="b9cd0-110">Zero-Based</span></span>  
 <span data-ttu-id="b9cd0-111">Pour obtenir un exemple d’une fonction Visual Basic de base zéro, envisagez le `Split` (fonction).</span><span class="sxs-lookup"><span data-stu-id="b9cd0-111">For an example of a zero-based Visual Basic function, consider the `Split` function.</span></span> <span data-ttu-id="b9cd0-112">Il fractionne une chaîne et retourne un tableau contenant les sous-chaînes.</span><span class="sxs-lookup"><span data-stu-id="b9cd0-112">It splits a string and returns an array containing the substrings.</span></span> <span data-ttu-id="b9cd0-113">Le .NET Framework <xref:System.String.Split%2A?displayProperty=nameWithType> méthode également fractionne une chaîne et retourne un tableau contenant les sous-chaînes.</span><span class="sxs-lookup"><span data-stu-id="b9cd0-113">The .NET Framework <xref:System.String.Split%2A?displayProperty=nameWithType> method also splits a string and returns an array containing the substrings.</span></span> <span data-ttu-id="b9cd0-114">Étant donné que le `Split` (fonction) et <xref:System.String.Split%2A> méthode retournent des tableaux de .NET Framework, ils doivent être de base zéro.</span><span class="sxs-lookup"><span data-stu-id="b9cd0-114">Because the `Split` function and <xref:System.String.Split%2A> method return .NET Framework arrays, they must be zero-based.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b9cd0-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9cd0-115">See also</span></span>

- <xref:Microsoft.VisualBasic.Strings.Mid%2A>
- <xref:Microsoft.VisualBasic.Strings.Split%2A>
- <xref:System.String.Substring%2A>
- <xref:System.String.Split%2A>
- [<span data-ttu-id="b9cd0-116">Introduction aux chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b9cd0-116">Introduction to Strings in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)
