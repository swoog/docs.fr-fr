---
title: '&#39;&lt;TypeName&gt; &#39; ne peut pas hériter &lt;type&gt; &#39; &lt;nom_type_base&gt; &#39; , car il étend l’accès de la base de &lt;type&gt; à l’extérieur de l’assembly'
ms.date: 07/20/2015
f1_keywords:
- vbc30910
- bc30910
helpviewer_keywords:
- BC30910
ms.assetid: 68fc05c5-5d55-4742-9a3b-ea04312594f4
ms.openlocfilehash: f747b2b24f5fecc22b9e1fbc6ba26b634e9ead2c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33598422"
---
# <a name="39lttypenamegt39-cannot-inherit-from-lttypegt-39ltbasetypenamegt39-because-it-expands-the-access-of-the-base-lttypegt-outside-the-assembly"></a><span data-ttu-id="aa429-102">&#39;&lt;TypeName&gt; &#39; ne peut pas hériter &lt;type&gt; &#39; &lt;nom_type_base&gt; &#39; , car il étend l’accès de la base de &lt;type&gt; à l’extérieur de l’assembly</span><span class="sxs-lookup"><span data-stu-id="aa429-102">&#39;&lt;typename&gt;&#39; cannot inherit from &lt;type&gt; &#39;&lt;basetypename&gt;&#39; because it expands the access of the base &lt;type&gt; outside the assembly</span></span>
<span data-ttu-id="aa429-103">Une classe ou interface hérite d’une classe de base ou interface, mais ne comporte un niveau d’accès moins restrictif.</span><span class="sxs-lookup"><span data-stu-id="aa429-103">A class or interface inherits from a base class or interface but has a less restrictive access level.</span></span>  
  
 <span data-ttu-id="aa429-104">Par exemple, un `Public` interface hérite d’un `Friend` interface, ou un `Protected` hérite de la classe une `Private` classe.</span><span class="sxs-lookup"><span data-stu-id="aa429-104">For example, a `Public` interface inherits from a `Friend` interface, or a `Protected` class inherits from a `Private` class.</span></span> <span data-ttu-id="aa429-105">Cela expose la classe de base ou une interface pour accéder aux au-delà du niveau prévu.</span><span class="sxs-lookup"><span data-stu-id="aa429-105">This exposes the base class or interface to access beyond the intended level.</span></span>  
  
 <span data-ttu-id="aa429-106">**ID d’erreur :** BC30910</span><span class="sxs-lookup"><span data-stu-id="aa429-106">**Error ID:** BC30910</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="aa429-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="aa429-107">To correct this error</span></span>  
  
-   <span data-ttu-id="aa429-108">Modifier le niveau d’accès de la classe dérivée ou une interface soit au moins aussi restrictif que celui de la classe de base ou l’interface.</span><span class="sxs-lookup"><span data-stu-id="aa429-108">Change the access level of the derived class or interface to be at least as restrictive as that of the base class or interface.</span></span>  
  
     <span data-ttu-id="aa429-109">- ou -</span><span class="sxs-lookup"><span data-stu-id="aa429-109">-or-</span></span>  
  
-   <span data-ttu-id="aa429-110">Si le niveau d’accès moins restrictif, supprimez le `Inherits` instruction.</span><span class="sxs-lookup"><span data-stu-id="aa429-110">If you require the less restrictive access level, remove the `Inherits` statement.</span></span> <span data-ttu-id="aa429-111">Vous ne peut pas hériter d’une classe de base plus restreinte ou une interface.</span><span class="sxs-lookup"><span data-stu-id="aa429-111">You cannot inherit from a more restricted base class or interface.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aa429-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa429-112">See Also</span></span>  
 [<span data-ttu-id="aa429-113">Class (instruction)</span><span class="sxs-lookup"><span data-stu-id="aa429-113">Class Statement</span></span>](../../../visual-basic/language-reference/statements/class-statement.md)  
 [<span data-ttu-id="aa429-114">Interface (instruction)</span><span class="sxs-lookup"><span data-stu-id="aa429-114">Interface Statement</span></span>](../../../visual-basic/language-reference/statements/interface-statement.md)  
 [<span data-ttu-id="aa429-115">Inherits (instruction)</span><span class="sxs-lookup"><span data-stu-id="aa429-115">Inherits Statement</span></span>](../../../visual-basic/language-reference/statements/inherits-statement.md)  
 [<span data-ttu-id="aa429-116">Niveaux d’accès dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="aa429-116">Access levels in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
