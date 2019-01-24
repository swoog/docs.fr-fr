---
title: Default (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Default
helpviewer_keywords:
- defaults, properties
- properties [Visual Basic], default
- default properties, in Visual Basic
- Default keyword [Visual Basic]
- default properties
ms.assetid: 45fce9b9-d212-4b2d-ab86-6e359b8b57af
ms.openlocfilehash: b63fa66c9cda1e439e3917ca62377f68028fc049
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54497839"
---
# <a name="default-visual-basic"></a><span data-ttu-id="cfa96-102">Default (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="cfa96-102">Default (Visual Basic)</span></span>
<span data-ttu-id="cfa96-103">Identifie une propriété comme la propriété par défaut de sa classe, une structure ou une interface.</span><span class="sxs-lookup"><span data-stu-id="cfa96-103">Identifies a property as the default property of its class, structure, or interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cfa96-104">Notes</span><span class="sxs-lookup"><span data-stu-id="cfa96-104">Remarks</span></span>  
 <span data-ttu-id="cfa96-105">Une classe, une structure ou une interface peut désigner au plus une de ses propriétés comme le *propriété par défaut*, à condition que la propriété prend au moins un paramètre.</span><span class="sxs-lookup"><span data-stu-id="cfa96-105">A class, structure, or interface can designate at most one of its properties as the *default property*, provided that property takes at least one parameter.</span></span> <span data-ttu-id="cfa96-106">Si le code fait référence à une classe ou structure sans spécifier un membre, Visual Basic résout qu’une référence à la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="cfa96-106">If code makes a reference to a class or structure without specifying a member, Visual Basic resolves that reference to the default property.</span></span>  
  
 <span data-ttu-id="cfa96-107">Propriétés par défaut peuvent entraîner une légère réduction dans les caractères de code source, mais ils peuvent rendre votre code plus difficile à lire.</span><span class="sxs-lookup"><span data-stu-id="cfa96-107">Default properties can result in a small reduction in source code-characters, but they can make your code more difficult to read.</span></span> <span data-ttu-id="cfa96-108">Si le code appelant n’est pas familiarisé avec votre classe ou structure, lorsqu’il fait référence au nom de classe ou structure il ne peut pas être certains que cette référence accède à la classe ou structure lui-même ou une propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="cfa96-108">If the calling code is not familiar with your class or structure, when it makes a reference to the class or structure name it cannot be certain whether that reference accesses the class or structure itself, or a default property.</span></span> <span data-ttu-id="cfa96-109">Cela peut entraîner des erreurs du compilateur ou des erreurs de logique d’exécution subtiles.</span><span class="sxs-lookup"><span data-stu-id="cfa96-109">This can lead to compiler errors or subtle run-time logic errors.</span></span>  
  
 <span data-ttu-id="cfa96-110">Vous pouvez légèrement réduire les risques d’erreurs de propriété par défaut en utilisant toujours la [Option Strict, instruction](../../../visual-basic/language-reference/statements/option-strict-statement.md) pour définir le contrôle de type du compilateur `On`.</span><span class="sxs-lookup"><span data-stu-id="cfa96-110">You can somewhat reduce the chance of default property errors by always using the [Option Strict Statement](../../../visual-basic/language-reference/statements/option-strict-statement.md) to set compiler type checking to `On`.</span></span>  
  
 <span data-ttu-id="cfa96-111">Si vous envisagez d’utiliser une classe prédéfinie ou une structure dans votre code, vous devez déterminer s’il possède une propriété par défaut et si c’est le cas, ce que son nom est.</span><span class="sxs-lookup"><span data-stu-id="cfa96-111">If you are planning to use a predefined class or structure in your code, you must determine whether it has a default property, and if so, what its name is.</span></span>  
  
 <span data-ttu-id="cfa96-112">En raison de ces inconvénients, vous devez envisager de ne pas définir les propriétés par défaut.</span><span class="sxs-lookup"><span data-stu-id="cfa96-112">Because of these disadvantages, you should consider not defining default properties.</span></span> <span data-ttu-id="cfa96-113">Pour la lisibilité du code, vous devez également envisager de toujours faire explicitement référence à toutes les propriétés, même les propriétés par défaut.</span><span class="sxs-lookup"><span data-stu-id="cfa96-113">For code readability, you should also consider always referring to all properties explicitly, even default properties.</span></span>  
  
 <span data-ttu-id="cfa96-114">Le `Default` modificateur peut être utilisé dans ce contexte :</span><span class="sxs-lookup"><span data-stu-id="cfa96-114">The `Default` modifier can be used in this context:</span></span>  
  
 [<span data-ttu-id="cfa96-115">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="cfa96-115">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="cfa96-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfa96-116">See also</span></span>
- [<span data-ttu-id="cfa96-117">Guide pratique pour Déclarer et appeler une propriété par défaut en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cfa96-117">How to: Declare and Call a Default Property in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-declare-and-call-a-default-property.md)
- [<span data-ttu-id="cfa96-118">Mots clés</span><span class="sxs-lookup"><span data-stu-id="cfa96-118">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
