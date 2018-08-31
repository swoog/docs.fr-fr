---
title: params (référence C#)
ms.date: 07/20/2015
f1_keywords:
- params_CSharpKeyword
- params
helpviewer_keywords:
- parameters [C#], params
- params keyword [C#]
ms.assetid: 1690815e-b52b-4967-8380-5780aff08012
ms.openlocfilehash: 692c2f61ae99f1c1c8e04a5a1bcad08814d286fe
ms.sourcegitcommit: a1e35d4e94edab384a63406c0a5438306873031b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2018
ms.locfileid: "42751949"
---
# <a name="params-c-reference"></a><span data-ttu-id="85836-102">params (référence C#)</span><span class="sxs-lookup"><span data-stu-id="85836-102">params (C# Reference)</span></span>
<span data-ttu-id="85836-103">Avec le mot clé `params`, vous pouvez spécifier un [paramètre de méthode](../../../csharp/language-reference/keywords/method-parameters.md) qui prend un nombre variable d’arguments.</span><span class="sxs-lookup"><span data-stu-id="85836-103">By using the `params` keyword, you can specify a [method parameter](../../../csharp/language-reference/keywords/method-parameters.md) that takes a variable number of arguments.</span></span>  
  
 <span data-ttu-id="85836-104">Vous pouvez envoyer une liste séparée par des virgules d’arguments du type spécifié dans la déclaration du paramètre ou envoyer un tableau d’arguments du type spécifié.</span><span class="sxs-lookup"><span data-stu-id="85836-104">You can send a comma-separated list of arguments of the type specified in the parameter declaration or an array of arguments of the specified type.</span></span> <span data-ttu-id="85836-105">Vous pouvez aussi ne pas envoyer d’arguments.</span><span class="sxs-lookup"><span data-stu-id="85836-105">You also can send no arguments.</span></span> <span data-ttu-id="85836-106">Si vous n’envoyez aucun argument, la longueur de la liste `params` est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="85836-106">If you send no arguments, the length of the `params` list is zero.</span></span>  
  
 <span data-ttu-id="85836-107">Dans une déclaration de méthode, vous ne pouvez pas spécifier de paramètre supplémentaire après le mot clé `params` et vous pouvez utiliser un seul mot clé `params`.</span><span class="sxs-lookup"><span data-stu-id="85836-107">No additional parameters are permitted after the `params` keyword in a method declaration, and only one `params` keyword is permitted in a method declaration.</span></span>  
 
 <span data-ttu-id="85836-108">Le type déclaré du paramètre `params` doit être un tableau unidimensionnel, comme le montre l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="85836-108">The declared type of the `params` parameter must be a single-dimensional array, as the following example shows.</span></span> <span data-ttu-id="85836-109">Sinon, une erreur du compilateur [CS0225](../../../csharp/misc/cs0225.md) se produit.</span><span class="sxs-lookup"><span data-stu-id="85836-109">Otherwise, a compiler error [CS0225](../../../csharp/misc/cs0225.md) occurs.</span></span>
  
## <a name="example"></a><span data-ttu-id="85836-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="85836-110">Example</span></span>  
 <span data-ttu-id="85836-111">L’exemple suivant montre différentes façons d’envoyer des arguments à un paramètre `params`.</span><span class="sxs-lookup"><span data-stu-id="85836-111">The following example demonstrates various ways in which arguments can be sent to a `params` parameter.</span></span>  
  
 [!code-csharp[csrefKeywordsMethodParams#5](../../../csharp/language-reference/keywords/codesnippet/CSharp/params_1.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="85836-112">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="85836-112">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="85836-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85836-113">See Also</span></span>  
 [<span data-ttu-id="85836-114">Référence C#</span><span class="sxs-lookup"><span data-stu-id="85836-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="85836-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="85836-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="85836-116">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="85836-116">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="85836-117">Paramètres de méthodes</span><span class="sxs-lookup"><span data-stu-id="85836-117">Method Parameters</span></span>](../../../csharp/language-reference/keywords/method-parameters.md)
