---
title: Constructeur &#39; &lt;nom&gt; &#39; ne peut pas s’appeler lui-même
ms.date: 07/20/2015
f1_keywords:
- bc30298
- vbc30298
helpviewer_keywords:
- BC30298
ms.assetid: 2d77b7f4-0640-4f89-9c65-f101fd2847c0
ms.openlocfilehash: 069de813a0426230e19cddf14c3b83d40a602a41
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33588994"
---
# <a name="constructor-39ltnamegt39-cannot-call-itself"></a><span data-ttu-id="920ad-102">Constructeur &#39; &lt;nom&gt; &#39; ne peut pas s’appeler lui-même</span><span class="sxs-lookup"><span data-stu-id="920ad-102">Constructor &#39;&lt;name&gt;&#39; cannot call itself</span></span>
<span data-ttu-id="920ad-103">A `Sub New` procédure dans une classe ou une structure s’appelle elle-même.</span><span class="sxs-lookup"><span data-stu-id="920ad-103">A `Sub New` procedure in a class or structure calls itself.</span></span>  
  
 <span data-ttu-id="920ad-104">Est de l’objectif d’un constructeur pour initialiser une instance d’une classe ou structure lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="920ad-104">The purpose of a constructor is to initialize an instance of a class or structure when it is first created.</span></span> <span data-ttu-id="920ad-105">Une classe ou structure peut avoir plusieurs constructeurs fournies ont tous des listes de paramètres différentes.</span><span class="sxs-lookup"><span data-stu-id="920ad-105">A class or structure can have several constructors, provided they all have different parameter lists.</span></span> <span data-ttu-id="920ad-106">Un constructeur est autorisé à appeler un autre constructeur pour effectuer ses fonctionnalités en plus de son propre.</span><span class="sxs-lookup"><span data-stu-id="920ad-106">A constructor is permitted to call another constructor to perform its functionality in addition to its own.</span></span> <span data-ttu-id="920ad-107">Ne peut pas s’appeler lui-même un constructeur, mais en fait il entraînerait une récurrence infinie si autorisé.</span><span class="sxs-lookup"><span data-stu-id="920ad-107">But it is meaningless for a constructor to call itself, and in fact it would result in infinite recursion if permitted.</span></span>  
  
 <span data-ttu-id="920ad-108">**ID d’erreur :** BC30298</span><span class="sxs-lookup"><span data-stu-id="920ad-108">**Error ID:** BC30298</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="920ad-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="920ad-109">To correct this error</span></span>  
  
1.  <span data-ttu-id="920ad-110">Vérifiez la liste des paramètres du constructeur appelé.</span><span class="sxs-lookup"><span data-stu-id="920ad-110">Check the parameter list of the constructor being called.</span></span> <span data-ttu-id="920ad-111">Il doit être différent de celui du constructeur qui effectue l’appel.</span><span class="sxs-lookup"><span data-stu-id="920ad-111">It should be different from that of the constructor making the call.</span></span>  
  
2.  <span data-ttu-id="920ad-112">Si vous ne souhaitez pas appeler un autre constructeur, supprimez le `Sub New` intégralité de l’appel.</span><span class="sxs-lookup"><span data-stu-id="920ad-112">If you do not intend to call a different constructor, remove the `Sub New` call entirely.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="920ad-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="920ad-113">See Also</span></span>  
 [<span data-ttu-id="920ad-114">Durée de vie d’un objet : création et destruction des objets</span><span class="sxs-lookup"><span data-stu-id="920ad-114">Object Lifetime: How Objects Are Created and Destroyed</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md)
