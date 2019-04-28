---
title: NotOverridable (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.NotOverridable
- NotOverridable
helpviewer_keywords:
- sealed methods [Visual Basic]
- NotOverridable keyword [Visual Basic]
- properties [Visual Basic], redefining
- elements [Visual Basic], sealed
- sealed [elements VB]
- procedures [Visual Basic], overriding
- procedures [Visual Basic], redefining
- overriding
- methods [Visual Basic], sealed
- properties [Visual Basic], overriding
ms.assetid: 66ec6984-f5f5-4857-b362-6a3907aaf9e0
ms.openlocfilehash: 41c08a48fdb7501081e887fb5cf9f99c334c72ac
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61920651"
---
# <a name="notoverridable-visual-basic"></a><span data-ttu-id="77002-102">NotOverridable (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="77002-102">NotOverridable (Visual Basic)</span></span>
<span data-ttu-id="77002-103">Spécifie qu’une propriété ou procédure ne peut pas être substituée dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="77002-103">Specifies that a property or procedure cannot be overridden in a derived class.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="77002-104">Notes</span><span class="sxs-lookup"><span data-stu-id="77002-104">Remarks</span></span>  
 <span data-ttu-id="77002-105">Le `NotOverridable` modificateur empêche une propriété ou méthode d’être substituée dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="77002-105">The `NotOverridable` modifier prevents a property or method from being overridden in a derived class.</span></span>  <span data-ttu-id="77002-106">Le [Overridable](../../../visual-basic/language-reference/modifiers/overridable.md) modificateur permet à une propriété ou méthode dans une classe de substitution dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="77002-106">The [Overridable](../../../visual-basic/language-reference/modifiers/overridable.md) modifier allows a property or method in a class to be overridden in a derived class.</span></span> <span data-ttu-id="77002-107">Pour plus d’informations, consultez [Concepts de base de l’héritage](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md).</span><span class="sxs-lookup"><span data-stu-id="77002-107">For more information, see [Inheritance Basics](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md).</span></span>  
  
 <span data-ttu-id="77002-108">Si le `Overridable` ou `NotOverridable` modificateur n’est pas spécifié, le paramètre par défaut varie selon que la propriété ou méthode se substitue à une méthode ou propriété de classe de base.</span><span class="sxs-lookup"><span data-stu-id="77002-108">If the `Overridable` or `NotOverridable` modifier is not specified, the default setting depends on whether the property or method overrides a base class property or method.</span></span> <span data-ttu-id="77002-109">Si la propriété ou méthode substitue une méthode ou propriété de classe de base, le paramètre par défaut est `Overridable`; sinon, il est `NotOverridable`.</span><span class="sxs-lookup"><span data-stu-id="77002-109">If the property or method overrides a base class property or method, the default setting is `Overridable`; otherwise, it is `NotOverridable`.</span></span>  
  
 <span data-ttu-id="77002-110">Un élément qui ne peut pas être substitué est parfois appelé un *sealed* élément.</span><span class="sxs-lookup"><span data-stu-id="77002-110">An element that cannot be overridden is sometimes called a *sealed* element.</span></span>  
  
 <span data-ttu-id="77002-111">Vous pouvez utiliser `NotOverridable` uniquement dans une instruction de déclaration de propriété ou de procédure.</span><span class="sxs-lookup"><span data-stu-id="77002-111">You can use `NotOverridable` only in a property or procedure declaration statement.</span></span> <span data-ttu-id="77002-112">Vous pouvez spécifier `NotOverridable` uniquement sur une propriété ou procédure qui substitue une autre propriété ou procédure, autrement dit, uniquement en association avec `Overrides`.</span><span class="sxs-lookup"><span data-stu-id="77002-112">You can specify `NotOverridable` only on a property or procedure that overrides another property or procedure, that is, only in combination with `Overrides`.</span></span>  
  
## <a name="combined-modifiers"></a><span data-ttu-id="77002-113">Modificateurs combinés</span><span class="sxs-lookup"><span data-stu-id="77002-113">Combined Modifiers</span></span>  
 <span data-ttu-id="77002-114">Vous ne pouvez pas spécifier `Overridable` ou `NotOverridable` pour un `Private` (méthode).</span><span class="sxs-lookup"><span data-stu-id="77002-114">You cannot specify `Overridable` or `NotOverridable` for a `Private` method.</span></span>  
  
 <span data-ttu-id="77002-115">Vous ne pouvez pas spécifier `NotOverridable` avec `MustOverride`, `Overridable`, ou `Shared` dans la même déclaration.</span><span class="sxs-lookup"><span data-stu-id="77002-115">You cannot specify `NotOverridable` together with `MustOverride`, `Overridable`, or `Shared` in the same declaration.</span></span>  
  
## <a name="usage"></a><span data-ttu-id="77002-116">Utilisation</span><span class="sxs-lookup"><span data-stu-id="77002-116">Usage</span></span>  
 <span data-ttu-id="77002-117">Le modificateur `NotOverridable` peut être utilisé dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="77002-117">The `NotOverridable` modifier can be used in these contexts:</span></span>  
  
 [<span data-ttu-id="77002-118">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="77002-118">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [<span data-ttu-id="77002-119">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="77002-119">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [<span data-ttu-id="77002-120">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="77002-120">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="77002-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77002-121">See also</span></span>

- [<span data-ttu-id="77002-122">Modificateurs</span><span class="sxs-lookup"><span data-stu-id="77002-122">Modifiers</span></span>](../../../visual-basic/language-reference/modifiers/index.md)
- [<span data-ttu-id="77002-123">Éléments fondamentaux de l’héritage</span><span class="sxs-lookup"><span data-stu-id="77002-123">Inheritance Basics</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
- [<span data-ttu-id="77002-124">MustOverride</span><span class="sxs-lookup"><span data-stu-id="77002-124">MustOverride</span></span>](../../../visual-basic/language-reference/modifiers/mustoverride.md)
- [<span data-ttu-id="77002-125">Overridable</span><span class="sxs-lookup"><span data-stu-id="77002-125">Overridable</span></span>](../../../visual-basic/language-reference/modifiers/overridable.md)
- [<span data-ttu-id="77002-126">Overrides</span><span class="sxs-lookup"><span data-stu-id="77002-126">Overrides</span></span>](../../../visual-basic/language-reference/modifiers/overrides.md)
- [<span data-ttu-id="77002-127">Mots clés</span><span class="sxs-lookup"><span data-stu-id="77002-127">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
- [<span data-ttu-id="77002-128">Occultation dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="77002-128">Shadowing in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
