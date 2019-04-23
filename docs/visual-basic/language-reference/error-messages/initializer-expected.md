---
title: Initialiseur attendu
ms.date: 07/20/2015
f1_keywords:
- vbc30996
- bc30996
helpviewer_keywords:
- BC30996
ms.assetid: 6e183fe0-8888-43ed-a062-01571079455f
ms.openlocfilehash: 0795fdc1c4b177e13979d7555cd7588217b8cb4c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59334963"
---
# <a name="initializer-expected"></a><span data-ttu-id="08e39-102">Initialiseur attendu</span><span class="sxs-lookup"><span data-stu-id="08e39-102">Initializer expected</span></span>
<span data-ttu-id="08e39-103">Vous avez tenté de déclarer une instance d’une classe à l’aide d’un initialiseur d’objet dans lequel la liste d’initialisation est vide, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="08e39-103">You have tried to declare an instance of a class by using an object initializer in which the initialization list is empty, as shown in the following example.</span></span>  
  
 `' Not valid.`  
  
 `' Dim aStudent As New Student With {}`  
  
 <span data-ttu-id="08e39-104">Au moins un champ ou une propriété doit être initialisée dans la liste d’initialiseurs, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="08e39-104">At least one field or property must be initialized in the initializer list, as shown in the following example.</span></span>  
  
 `Dim aStudent As New Student With {.year = "Senior"}`  
  
 <span data-ttu-id="08e39-105">**ID d’erreur :** BC30996</span><span class="sxs-lookup"><span data-stu-id="08e39-105">**Error ID:** BC30996</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="08e39-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="08e39-106">To correct this error</span></span>  
  
1. <span data-ttu-id="08e39-107">Initialiser au moins un champ ou une propriété dans l’initialiseur ou n’utilisez pas un initialiseur d’objet.</span><span class="sxs-lookup"><span data-stu-id="08e39-107">Initialize at least one field or property in the initializer, or do not use an object initializer.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="08e39-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08e39-108">See also</span></span>

- [<span data-ttu-id="08e39-109">Initialiseurs d’objets : Types nommés et anonymes</span><span class="sxs-lookup"><span data-stu-id="08e39-109">Object Initializers: Named and Anonymous Types</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-initializers-named-and-anonymous-types.md)
- [<span data-ttu-id="08e39-110">Guide pratique pour Déclarez un objet à l’aide d’un initialiseur d’objet</span><span class="sxs-lookup"><span data-stu-id="08e39-110">How to: Declare an Object by Using an Object Initializer</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-declare-an-object-by-using-an-object-initializer.md)
