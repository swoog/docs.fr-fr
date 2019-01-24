---
title: Impossible de faire référence à un membre instance d'une classe à partir d'une méthode partagée ou d'un initialiseur de membre partagé sans une instance explicite de la classe
ms.date: 07/20/2015
f1_keywords:
- vbc30369
- bc30369
helpviewer_keywords:
- Shared
- BC30369
ms.assetid: 39d9466b-c1f3-4406-91a5-3d6c52d23a3d
ms.openlocfilehash: da3aa17c55a4ccc95e5f4c98d0f12712ef77d5c2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54729221"
---
# <a name="cannot-refer-to-an-instance-member-of-a-class-from-within-a-shared-method-or-shared-member-initializer-without-an-explicit-instance-of-the-class"></a><span data-ttu-id="01a4a-102">Impossible de faire référence à un membre instance d'une classe à partir d'une méthode partagée ou d'un initialiseur de membre partagé sans une instance explicite de la classe</span><span class="sxs-lookup"><span data-stu-id="01a4a-102">Cannot refer to an instance member of a class from within a shared method or shared member initializer without an explicit instance of the class</span></span>
<span data-ttu-id="01a4a-103">Vous avez essayé de faire référence à un membre non partagé d’une classe à partir d’une procédure partagée.</span><span class="sxs-lookup"><span data-stu-id="01a4a-103">You have tried to refer to a non-shared member of a class from within a shared procedure.</span></span> <span data-ttu-id="01a4a-104">L’exemple suivant illustre une telle situation.</span><span class="sxs-lookup"><span data-stu-id="01a4a-104">The following example demonstrates such a situation.</span></span>  
  
```  
Class sample  
    Public x as Integer  
    Public Shared Sub setX()  
        x = 10  
    End Sub  
End Class  
```  
  
 <span data-ttu-id="01a4a-105">Dans l’exemple précédent, l’instruction d’assignation `x = 10` génère ce message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="01a4a-105">In the preceding example, the assignment statement `x = 10` generates this error message.</span></span> <span data-ttu-id="01a4a-106">Il s’agit, car une procédure partagée tente d’accéder à une variable d’instance.</span><span class="sxs-lookup"><span data-stu-id="01a4a-106">This is because a shared procedure is attempting to access an instance variable.</span></span>  
  
 <span data-ttu-id="01a4a-107">La variable `x` est un membre d’instance, car il n’est pas déclaré en tant que [partagé](../../../visual-basic/language-reference/modifiers/shared.md).</span><span class="sxs-lookup"><span data-stu-id="01a4a-107">The variable `x` is an instance member because it is not declared as [Shared](../../../visual-basic/language-reference/modifiers/shared.md).</span></span> <span data-ttu-id="01a4a-108">Chaque instance de classe `sample` contient sa propre variable individuelle `x`.</span><span class="sxs-lookup"><span data-stu-id="01a4a-108">Each instance of class `sample` contains its own individual variable `x`.</span></span> <span data-ttu-id="01a4a-109">Lorsqu’une instance définit ou modifie la valeur de `x`, il n’affecte pas la valeur de `x` dans une autre instance.</span><span class="sxs-lookup"><span data-stu-id="01a4a-109">When one instance sets or changes the value of `x`, it does not affect the value of `x` in any other instance.</span></span>  
  
 <span data-ttu-id="01a4a-110">Toutefois, la procédure `setX` est `Shared` entre toutes les instances de classe `sample`.</span><span class="sxs-lookup"><span data-stu-id="01a4a-110">However, the procedure `setX` is `Shared` among all instances of class `sample`.</span></span> <span data-ttu-id="01a4a-111">Cela signifie qu’il n’est pas associé à une instance de la classe, mais au lieu de cela fonctionne indépendamment des instances individuelles.</span><span class="sxs-lookup"><span data-stu-id="01a4a-111">This means it is not associated with any one instance of the class, but rather operates independently of individual instances.</span></span> <span data-ttu-id="01a4a-112">Car il ne possède aucune connexion avec une instance particulière, `setX` ne peut pas accéder à une variable d’instance.</span><span class="sxs-lookup"><span data-stu-id="01a4a-112">Because it has no connection with a particular instance, `setX` cannot access an instance variable.</span></span> <span data-ttu-id="01a4a-113">Il doit fonctionner uniquement sur `Shared` variables.</span><span class="sxs-lookup"><span data-stu-id="01a4a-113">It must operate only on `Shared` variables.</span></span> <span data-ttu-id="01a4a-114">Lorsque `setX` définit ou modifie la valeur d’une variable partagée, que la nouvelle valeur est disponible pour toutes les instances de la classe.</span><span class="sxs-lookup"><span data-stu-id="01a4a-114">When `setX` sets or changes the value of a shared variable, that new value is available to all instances of the class.</span></span>  
  
 <span data-ttu-id="01a4a-115">**ID d’erreur :** BC30369</span><span class="sxs-lookup"><span data-stu-id="01a4a-115">**Error ID:** BC30369</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="01a4a-116">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="01a4a-116">To correct this error</span></span>  
  
1.  <span data-ttu-id="01a4a-117">Décidez si vous souhaitez que le membre doit être partagé entre toutes les instances de la classe, ou conservées individuels pour chaque instance.</span><span class="sxs-lookup"><span data-stu-id="01a4a-117">Decide whether you want the member to be shared among all instances of the class, or kept individual for each instance.</span></span>  
  
2.  <span data-ttu-id="01a4a-118">Si vous souhaitez une copie unique du membre à partager entre toutes les instances, ajoutez le `Shared` mot clé à la déclaration de membre.</span><span class="sxs-lookup"><span data-stu-id="01a4a-118">If you want a single copy of the member to be shared among all instances, add the `Shared` keyword to the member declaration.</span></span> <span data-ttu-id="01a4a-119">Conserver le `Shared` mot clé dans la déclaration de procédure.</span><span class="sxs-lookup"><span data-stu-id="01a4a-119">Retain the `Shared` keyword in the procedure declaration.</span></span>  
  
3.  <span data-ttu-id="01a4a-120">Si vous souhaitez que chaque instance possède sa propre copie individuelle du membre, ne spécifiez pas `Shared` pour la déclaration de membre.</span><span class="sxs-lookup"><span data-stu-id="01a4a-120">If you want each instance to have its own individual copy of the member, do not specify `Shared` for the member declaration.</span></span> <span data-ttu-id="01a4a-121">Supprimer le `Shared` mot clé à partir de la déclaration de procédure.</span><span class="sxs-lookup"><span data-stu-id="01a4a-121">Remove the `Shared` keyword from the procedure declaration.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01a4a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01a4a-122">See also</span></span>
- [<span data-ttu-id="01a4a-123">Shared</span><span class="sxs-lookup"><span data-stu-id="01a4a-123">Shared</span></span>](../../../visual-basic/language-reference/modifiers/shared.md)
