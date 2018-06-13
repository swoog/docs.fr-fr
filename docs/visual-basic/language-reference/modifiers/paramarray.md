---
title: ParamArray (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.ParamArray
- ParamArray
helpviewer_keywords:
- ParamArray keyword [Visual Basic]
- ParamArray keyword [Visual Basic], syntax
ms.assetid: a5f18789-92bd-488f-9c7e-cf3719963635
ms.openlocfilehash: be8ddb7f9ba08535d12890d1c5c82a9b7b485f3d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33597358"
---
# <a name="paramarray-visual-basic"></a><span data-ttu-id="dd092-102">ParamArray (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="dd092-102">ParamArray (Visual Basic)</span></span>
<span data-ttu-id="dd092-103">Spécifie qu’un paramètre de procédure prend un tableau facultatif d’éléments du type spécifié.</span><span class="sxs-lookup"><span data-stu-id="dd092-103">Specifies that a procedure parameter takes an optional array of elements of the specified type.</span></span> <span data-ttu-id="dd092-104">`ParamArray` peut être utilisé uniquement sur le dernier paramètre d’une liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="dd092-104">`ParamArray` can be used only on the last parameter of a parameter list.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dd092-105">Notes</span><span class="sxs-lookup"><span data-stu-id="dd092-105">Remarks</span></span>  
 <span data-ttu-id="dd092-106">`ParamArray` vous permet de passer un nombre arbitraire d’arguments à la procédure.</span><span class="sxs-lookup"><span data-stu-id="dd092-106">`ParamArray` allows you to pass an arbitrary number of arguments to the procedure.</span></span> <span data-ttu-id="dd092-107">A `ParamArray` paramètre est toujours déclaré à l’aide de [ByVal](../../../visual-basic/language-reference/modifiers/byval.md).</span><span class="sxs-lookup"><span data-stu-id="dd092-107">A `ParamArray` parameter is always declared using [ByVal](../../../visual-basic/language-reference/modifiers/byval.md).</span></span>  
  
 <span data-ttu-id="dd092-108">Vous pouvez fournir un ou plusieurs arguments à une `ParamArray` type de paramètre en passant un tableau de données appropriés, une liste séparée par des virgules des valeurs, ou rien du tout.</span><span class="sxs-lookup"><span data-stu-id="dd092-108">You can supply one or more arguments to a `ParamArray` parameter by passing an array of the appropriate data type, a comma-separated list of values, or nothing at all.</span></span> <span data-ttu-id="dd092-109">Pour plus d’informations, consultez « Appel d’un ParamArray » dans [tableaux de paramètres](../../../visual-basic/programming-guide/language-features/procedures/parameter-arrays.md).</span><span class="sxs-lookup"><span data-stu-id="dd092-109">For details, see "Calling a ParamArray" in [Parameter Arrays](../../../visual-basic/programming-guide/language-features/procedures/parameter-arrays.md).</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="dd092-110">Si vous travaillez dans un tableau qui peut être indéfiniment volumineux, il existe un risque de saturer la capacité interne de votre application.</span><span class="sxs-lookup"><span data-stu-id="dd092-110">Whenever you deal with an array which can be indefinitely large, there is a risk of overrunning some internal capacity of your application.</span></span> <span data-ttu-id="dd092-111">Si vous acceptez un tableau de paramètres à partir du code appelant, vous devez tester sa longueur et prenez les mesures appropriées si elle est trop grande pour votre application.</span><span class="sxs-lookup"><span data-stu-id="dd092-111">If you accept a parameter array from the calling code, you should test its length and take appropriate steps if it is too large for your application.</span></span>  
  
 <span data-ttu-id="dd092-112">Le modificateur `ParamArray` peut être utilisé dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="dd092-112">The `ParamArray` modifier can be used in these contexts:</span></span>  
  
 [<span data-ttu-id="dd092-113">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="dd092-113">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 [<span data-ttu-id="dd092-114">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="dd092-114">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [<span data-ttu-id="dd092-115">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="dd092-115">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [<span data-ttu-id="dd092-116">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="dd092-116">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="dd092-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd092-117">See Also</span></span>  
 [<span data-ttu-id="dd092-118">Mots clés</span><span class="sxs-lookup"><span data-stu-id="dd092-118">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)  
 [<span data-ttu-id="dd092-119">tableaux de paramètres</span><span class="sxs-lookup"><span data-stu-id="dd092-119">Parameter Arrays</span></span>](../../../visual-basic/programming-guide/language-features/procedures/parameter-arrays.md)
