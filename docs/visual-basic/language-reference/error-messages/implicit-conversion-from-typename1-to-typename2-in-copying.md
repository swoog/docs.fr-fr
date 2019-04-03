---
title: Option Strict On interdit le passage du type '<typename1>' au type '<typename2>' lors de la recopie de la valeur du paramètre 'ByRef' '<parametername>' dans l'argument correspondant.
ms.date: 07/20/2015
f1_keywords:
- vbc41999
- bc41999
helpviewer_keywords:
- BC41999
ms.assetid: ae48c738-dff8-4c0f-8931-bbb70b2c8b03
ms.openlocfilehash: 7b02659d96b08c592b25ddf3ef1f99114c3ee269
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58831759"
---
# <a name="implicit-conversion-from-typename1-to-typename2-in-copying-the-value-of-byref-parameter-parametername-back-to-the-matching-argument"></a><span data-ttu-id="c87fd-102">Conversion implicite de '\<nom_type1 >' à '\<nom_type2 >' lors de la copie de la valeur du paramètre 'ByRef' '\<nom_paramètre >' dans l’argument correspondant.</span><span class="sxs-lookup"><span data-stu-id="c87fd-102">Implicit conversion from '\<typename1>' to '\<typename2>' in copying the value of 'ByRef' parameter '\<parametername>' back to the matching argument.</span></span>
<span data-ttu-id="c87fd-103">Une procédure est appelée avec un [ByRef](../../../visual-basic/language-reference/modifiers/byref.md) argument d’un type autre que celui de son paramètre correspondant.</span><span class="sxs-lookup"><span data-stu-id="c87fd-103">A procedure is called with a [ByRef](../../../visual-basic/language-reference/modifiers/byref.md) argument of a different type than that of its corresponding parameter.</span></span>  
  
 <span data-ttu-id="c87fd-104">Si vous passez un argument `ByRef`, Visual Basic copie parfois la valeur d’argument dans une variable locale dans la procédure au lieu de passer une référence.</span><span class="sxs-lookup"><span data-stu-id="c87fd-104">If you pass an argument `ByRef`, Visual Basic sometimes copies the argument value into a local variable in the procedure instead of passing a reference.</span></span> <span data-ttu-id="c87fd-105">Dans ce cas, lorsque la procédure est retournée, Visual Basic doit copier la valeur de variable locale dans l’argument dans le code appelant.</span><span class="sxs-lookup"><span data-stu-id="c87fd-105">In such a case, when the procedure returns, Visual Basic must then copy the local variable value back into the argument in the calling code.</span></span>  
  
 <span data-ttu-id="c87fd-106">Si une valeur d’argument `ByRef` est copiée dans la procédure, et si l’argument et le paramètre sont du même type, aucune conversion n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c87fd-106">If a `ByRef` argument value is copied into the procedure and the argument and parameter are of the same type, no conversion is necessary.</span></span> <span data-ttu-id="c87fd-107">Mais si les types sont différents, Visual Basic doit convertir dans les deux sens.</span><span class="sxs-lookup"><span data-stu-id="c87fd-107">But if the types are different, Visual Basic must convert in both directions.</span></span> <span data-ttu-id="c87fd-108">Étant donné que vous ne pouvez pas utiliser `CType` ou un des autres mots clés de conversion sur un argument de procédure ou de paramètre, une telle conversion est toujours implicite.</span><span class="sxs-lookup"><span data-stu-id="c87fd-108">Because you cannot use `CType` or any of the other conversion keywords on a procedure argument or parameter, such a conversion is always implicit.</span></span>  
  
 <span data-ttu-id="c87fd-109">Par défaut, ce message est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="c87fd-109">By default, this message is a warning.</span></span> <span data-ttu-id="c87fd-110">Pour plus d’informations sur le masquage des avertissements ou leur traitement en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="c87fd-110">For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="c87fd-111">**ID d’erreur :** BC41999</span><span class="sxs-lookup"><span data-stu-id="c87fd-111">**Error ID:** BC41999</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="c87fd-112">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="c87fd-112">To correct this error</span></span>  
  
-   <span data-ttu-id="c87fd-113">Si possible, utilisez un argument d’appel du même type que le paramètre de procédure pour Visual Basic n’a pas besoin d’effectuer de conversion.</span><span class="sxs-lookup"><span data-stu-id="c87fd-113">If possible, use a calling argument of the same type as the procedure parameter, so Visual Basic does not need to do any conversion.</span></span>  
  
-   <span data-ttu-id="c87fd-114">Si vous devez appeler la procédure avec un type d’argument différent du type de paramètre, mais n’avez pas besoin de retourner une valeur dans l’argument d’appel, définissez le paramètre sur [ByVal](../../../visual-basic/language-reference/modifiers/byval.md) au lieu de `ByRef`.</span><span class="sxs-lookup"><span data-stu-id="c87fd-114">If you need to call the procedure with an argument type different from the parameter type but do not need to return a value into the calling argument, define the parameter to be [ByVal](../../../visual-basic/language-reference/modifiers/byval.md) instead of `ByRef`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c87fd-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c87fd-115">See also</span></span>

- [<span data-ttu-id="c87fd-116">Procédures</span><span class="sxs-lookup"><span data-stu-id="c87fd-116">Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/index.md)
- [<span data-ttu-id="c87fd-117">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="c87fd-117">Procedure Parameters and Arguments</span></span>](../../../visual-basic/programming-guide/language-features/procedures/procedure-parameters-and-arguments.md)
- [<span data-ttu-id="c87fd-118">Passage d’un argument par valeur et par référence</span><span class="sxs-lookup"><span data-stu-id="c87fd-118">Passing Arguments by Value and by Reference</span></span>](../../../visual-basic/programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)
- [<span data-ttu-id="c87fd-119">Conversions implicites et explicites</span><span class="sxs-lookup"><span data-stu-id="c87fd-119">Implicit and Explicit Conversions</span></span>](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
