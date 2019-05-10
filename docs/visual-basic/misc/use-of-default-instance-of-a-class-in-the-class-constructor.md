---
title: L’utilisation de l’instance par défaut d’une classe dans le constructeur de classe pourrait entraîner des appels récurrents infinis
ms.date: 07/20/2015
ms.assetid: 9645b47f-7de5-46d0-bb45-d5fdaa8aaa2a
ms.openlocfilehash: 1cad1e3cf3943e945d519aee061a877c91684b4a
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64623470"
---
# <a name="use-of-default-instance-of-a-class-in-the-class-constructor-could-lead-to-infinite-recursive-call"></a><span data-ttu-id="f8efa-102">L’utilisation de l’instance par défaut d’une classe dans le constructeur de classe pourrait entraîner des appels récurrents infinis</span><span class="sxs-lookup"><span data-stu-id="f8efa-102">Use of Default Instance of a class in the class constructor could lead to infinite recursive call</span></span>
<span data-ttu-id="f8efa-103">Une instance par défaut d’une classe a été utilisée dans le constructeur de la classe.</span><span class="sxs-lookup"><span data-stu-id="f8efa-103">A default instance of a class has been used in the constructor of the class.</span></span> <span data-ttu-id="f8efa-104">Cela peut entraîner un appel récurrent infini, également appelé « boucle infinie ».</span><span class="sxs-lookup"><span data-stu-id="f8efa-104">This can lead to an infinite recursive call, also known as an infinite loop.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f8efa-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="f8efa-105">To correct this error</span></span>  
  
- <span data-ttu-id="f8efa-106">Supprimez l’instance par défaut du constructeur de la classe.</span><span class="sxs-lookup"><span data-stu-id="f8efa-106">Remove the default instance from the class constructor.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8efa-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8efa-107">See also</span></span>

- [<span data-ttu-id="f8efa-108">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="f8efa-108">Constructors</span></span>](~/docs/visual-basic/programming-guide/concepts/object-oriented-programming.md#constructors)
