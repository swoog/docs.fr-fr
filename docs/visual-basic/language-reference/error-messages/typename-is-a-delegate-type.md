---
title: '&#39;&lt;TypeName&gt; &#39; est un type délégué'
ms.date: 07/20/2015
f1_keywords:
- bc32008
- vbc32008
helpviewer_keywords:
- BC32008
ms.assetid: dc6abba0-a9ad-450f-8899-87265bc84abc
ms.openlocfilehash: c6d4244ce72dedee50b65ba19978149ce86b9e87
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33595646"
---
# <a name="39lttypenamegt39-is-a-delegate-type"></a><span data-ttu-id="3e5ec-102">&#39;&lt;TypeName&gt; &#39; est un type délégué</span><span class="sxs-lookup"><span data-stu-id="3e5ec-102">&#39;&lt;typename&gt;&#39; is a delegate type</span></span>
<span data-ttu-id="3e5ec-103">'\<nom_type >' est un type délégué.</span><span class="sxs-lookup"><span data-stu-id="3e5ec-103">'\<typename>' is a delegate type.</span></span> <span data-ttu-id="3e5ec-104">Une construction déléguée accepte une seule expression AddressOf en tant que liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="3e5ec-104">Delegate construction permits only a single AddressOf expression as an argument list.</span></span> <span data-ttu-id="3e5ec-105">Souvent une expression AddressOf peut être utilisée au lieu d’une construction de délégué.</span><span class="sxs-lookup"><span data-stu-id="3e5ec-105">Often an AddressOf expression can be used instead of a delegate construction.</span></span>  
  
 <span data-ttu-id="3e5ec-106">A `New` clause crée une instance d’une classe déléguée fournit une liste d’arguments non valide au constructeur délégué.</span><span class="sxs-lookup"><span data-stu-id="3e5ec-106">A `New` clause creating an instance of a delegate class supplies an invalid argument list to the delegate constructor.</span></span>  
  
 <span data-ttu-id="3e5ec-107">Vous pouvez fournir une seule `AddressOf` expression lors de la création d’une nouvelle instance de délégué.</span><span class="sxs-lookup"><span data-stu-id="3e5ec-107">You can supply only a single `AddressOf` expression when creating a new delegate instance.</span></span>  
  
 <span data-ttu-id="3e5ec-108">Cette erreur peut se produire si vous ne passez pas d’arguments au constructeur délégué, si vous passez plusieurs arguments, ou si vous passez un argument unique qui n’est pas valide `AddressOf` expression.</span><span class="sxs-lookup"><span data-stu-id="3e5ec-108">This error can result if you do not pass any arguments to the delegate constructor, if you pass more than one argument, or if you pass a single argument that is not a valid `AddressOf` expression.</span></span>  
  
 <span data-ttu-id="3e5ec-109">**ID d’erreur :** BC32008</span><span class="sxs-lookup"><span data-stu-id="3e5ec-109">**Error ID:** BC32008</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="3e5ec-110">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="3e5ec-110">To correct this error</span></span>  
  
-   <span data-ttu-id="3e5ec-111">Utiliser un seul `AddressOf` expression dans la liste d’arguments pour la classe déléguée dans la `New` clause.</span><span class="sxs-lookup"><span data-stu-id="3e5ec-111">Use a single `AddressOf` expression in the argument list for the delegate class in the `New` clause.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e5ec-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e5ec-112">See Also</span></span>  
 [<span data-ttu-id="3e5ec-113">New (opérateur)</span><span class="sxs-lookup"><span data-stu-id="3e5ec-113">New Operator</span></span>](../../../visual-basic/language-reference/operators/new-operator.md)  
 [<span data-ttu-id="3e5ec-114">AddressOf (opérateur)</span><span class="sxs-lookup"><span data-stu-id="3e5ec-114">AddressOf Operator</span></span>](../../../visual-basic/language-reference/operators/addressof-operator.md)  
 [<span data-ttu-id="3e5ec-115">Délégués</span><span class="sxs-lookup"><span data-stu-id="3e5ec-115">Delegates</span></span>](../../../visual-basic/programming-guide/language-features/delegates/index.md)  
 [<span data-ttu-id="3e5ec-116">Guide pratique : appeler une méthode déléguée</span><span class="sxs-lookup"><span data-stu-id="3e5ec-116">How to: Invoke a Delegate Method</span></span>](../../../visual-basic/programming-guide/language-features/delegates/how-to-invoke-a-delegate-method.md)
