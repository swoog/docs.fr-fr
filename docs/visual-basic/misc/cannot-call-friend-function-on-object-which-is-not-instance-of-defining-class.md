---
title: Impossible d’appeler une fonction Friend pour un objet qui n’est pas une instance de la classe de définition.
ms.date: 07/20/2015
f1_keywords:
- vbrID97
ms.assetid: b9d821f0-8565-4f15-bb35-184789c69662
ms.openlocfilehash: c65bbb5028cf042b702bb2b8336d40512c980790
ms.sourcegitcommit: 5c1abeec15fbddcc7dbaa729fabc1f1f29f12045
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2019
ms.locfileid: "58018249"
---
# <a name="cannot-call-friend-function-on-object-which-is-not-an-instance-of-defining-class"></a><span data-ttu-id="d9919-102">Impossible d’appeler une fonction Friend pour un objet qui n’est pas une instance de la classe de définition.</span><span class="sxs-lookup"><span data-stu-id="d9919-102">Cannot call friend function on object which is not an instance of defining class</span></span>
<span data-ttu-id="d9919-103">Vous avez tenté soit d’appeler la procédure `Friend` d’une classe, soit d’accéder à une propriété ou à une méthode `Friend` interprocessus ou inter-threads.</span><span class="sxs-lookup"><span data-stu-id="d9919-103">Either you tried to call the `Friend` procedure of a class, or you tried to access a `Friend` property or method either cross-process or cross-thread.</span></span> <span data-ttu-id="d9919-104">Une procédure `Friend` peut être appelée à partir d’un module à l’extérieur de la classe, mais elle fait partie du projet dans lequel la classe est définie.</span><span class="sxs-lookup"><span data-stu-id="d9919-104">A `Friend` procedure is callable from a module outside the class, but is part of the project in which the class is defined.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="d9919-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="d9919-105">To correct this error</span></span>  
  
-   <span data-ttu-id="d9919-106">Vérifiez que vous appelez la procédure ou que vous y accédez à partir d’un module qui fait partie du projet dans lequel la classe est définie.</span><span class="sxs-lookup"><span data-stu-id="d9919-106">Ensure that you are calling or accessing the procedure from a module that is part of the project in which the class is defined.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9919-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9919-107">See also</span></span>

- [<span data-ttu-id="d9919-108">Friend</span><span class="sxs-lookup"><span data-stu-id="d9919-108">Friend</span></span>](../../visual-basic/language-reference/modifiers/friend.md)
