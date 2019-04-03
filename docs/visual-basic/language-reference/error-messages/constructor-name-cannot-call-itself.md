---
title: Le constructeur '<name>' ne peut pas s'appeler lui-même
ms.date: 07/20/2015
f1_keywords:
- bc30298
- vbc30298
helpviewer_keywords:
- BC30298
ms.assetid: 2d77b7f4-0640-4f89-9c65-f101fd2847c0
ms.openlocfilehash: ef20f74055a07071ef9634973c6852ac58c3143c
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58824705"
---
# <a name="constructor-name-cannot-call-itself"></a><span data-ttu-id="674cb-102">Constructeur '\<nom >' ne peut pas s’appeler lui-même</span><span class="sxs-lookup"><span data-stu-id="674cb-102">Constructor '\<name>' cannot call itself</span></span>
<span data-ttu-id="674cb-103">Un `Sub New` procédure dans une classe ou structure s’appelle elle-même.</span><span class="sxs-lookup"><span data-stu-id="674cb-103">A `Sub New` procedure in a class or structure calls itself.</span></span>  
  
 <span data-ttu-id="674cb-104">L’objectif d’un constructeur doit initialiser une instance d’une classe ou structure lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="674cb-104">The purpose of a constructor is to initialize an instance of a class or structure when it is first created.</span></span> <span data-ttu-id="674cb-105">Une classe ou structure peut avoir plusieurs constructeurs, fournies ont tous des listes de paramètres différentes.</span><span class="sxs-lookup"><span data-stu-id="674cb-105">A class or structure can have several constructors, provided they all have different parameter lists.</span></span> <span data-ttu-id="674cb-106">Un constructeur est autorisé à appeler un autre constructeur pour exécuter ses fonctionnalités en plus de son propre.</span><span class="sxs-lookup"><span data-stu-id="674cb-106">A constructor is permitted to call another constructor to perform its functionality in addition to its own.</span></span> <span data-ttu-id="674cb-107">Mais il n’a aucune signification pour un constructeur s’appelle elle-même, et en fait il entraînerait une récurrence infinie si autorisé.</span><span class="sxs-lookup"><span data-stu-id="674cb-107">But it is meaningless for a constructor to call itself, and in fact it would result in infinite recursion if permitted.</span></span>  
  
 <span data-ttu-id="674cb-108">**ID d’erreur :** BC30298</span><span class="sxs-lookup"><span data-stu-id="674cb-108">**Error ID:** BC30298</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="674cb-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="674cb-109">To correct this error</span></span>  
  
1.  <span data-ttu-id="674cb-110">Vérifiez la liste des paramètres du constructeur appelé.</span><span class="sxs-lookup"><span data-stu-id="674cb-110">Check the parameter list of the constructor being called.</span></span> <span data-ttu-id="674cb-111">Il doit être différent de celui du constructeur qui effectue l’appel.</span><span class="sxs-lookup"><span data-stu-id="674cb-111">It should be different from that of the constructor making the call.</span></span>  
  
2.  <span data-ttu-id="674cb-112">Si vous ne souhaitez pas appeler un autre constructeur, supprimez le `Sub New` intégralité de l’appel.</span><span class="sxs-lookup"><span data-stu-id="674cb-112">If you do not intend to call a different constructor, remove the `Sub New` call entirely.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="674cb-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="674cb-113">See also</span></span>

- [<span data-ttu-id="674cb-114">Durée de vie d’objet : Comment les objets sont créés et détruits</span><span class="sxs-lookup"><span data-stu-id="674cb-114">Object Lifetime: How Objects Are Created and Destroyed</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md)
