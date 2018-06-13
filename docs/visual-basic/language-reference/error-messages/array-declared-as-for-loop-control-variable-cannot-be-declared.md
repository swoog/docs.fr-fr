---
title: Un tableau déclaré en tant que variable de contrôle de boucle for ne peut pas être déclaré avec une taille initiale
ms.date: 07/20/2015
f1_keywords:
- vbc32039
- bc32039
helpviewer_keywords:
- BC32039
ms.assetid: 1d8b6560-c9eb-4b71-a038-24c6f5a5ce46
ms.openlocfilehash: f6cf397b1e76313ab399d5e39a43ae0263df619c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33587982"
---
# <a name="array-declared-as-for-loop-control-variable-cannot-be-declared-with-an-initial-size"></a><span data-ttu-id="59f30-102">Un tableau déclaré en tant que variable de contrôle de boucle for ne peut pas être déclaré avec une taille initiale</span><span class="sxs-lookup"><span data-stu-id="59f30-102">Array declared as for loop control variable cannot be declared with an initial size</span></span>
<span data-ttu-id="59f30-103">A `For Each` boucle utilise un tableau comme sa *élément* variable d’itération initialise mais ce tableau.</span><span class="sxs-lookup"><span data-stu-id="59f30-103">A `For Each` loop uses an array as its *element* iteration variable but initializes that array.</span></span>  
  
 <span data-ttu-id="59f30-104">Les instructions suivantes montrent comment cette erreur peut être générée.</span><span class="sxs-lookup"><span data-stu-id="59f30-104">The following statements show how this error can be generated.</span></span>  
  
```  
Dim arrayList As New List(Of Integer())  
For Each listElement() As Integer In arrayList  
For Each listElement(1) As Integer In arrayList  
```  
  
 <span data-ttu-id="59f30-105">La première `For Each` instruction est la méthode correcte pour accéder aux éléments de `arrayList`.</span><span class="sxs-lookup"><span data-stu-id="59f30-105">The first `For Each` statement is the correct way to access elements of `arrayList`.</span></span> <span data-ttu-id="59f30-106">La seconde `For Each` instruction génère cette erreur.</span><span class="sxs-lookup"><span data-stu-id="59f30-106">The second `For Each` statement generates this error.</span></span>  
  
 <span data-ttu-id="59f30-107">**ID d’erreur :** BC32039</span><span class="sxs-lookup"><span data-stu-id="59f30-107">**Error ID:** BC32039</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="59f30-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="59f30-108">To correct this error</span></span>  
  
-   <span data-ttu-id="59f30-109">Supprimez l’initialisation de la déclaration de la *élément* variable d’itération.</span><span class="sxs-lookup"><span data-stu-id="59f30-109">Remove the initialization from the declaration of the *element* iteration variable.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59f30-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59f30-110">See Also</span></span>  
 [<span data-ttu-id="59f30-111">For...Next (instruction)</span><span class="sxs-lookup"><span data-stu-id="59f30-111">For...Next Statement</span></span>](../../../visual-basic/language-reference/statements/for-next-statement.md)  
 [<span data-ttu-id="59f30-112">Tableaux</span><span class="sxs-lookup"><span data-stu-id="59f30-112">Arrays</span></span>](../../../visual-basic/programming-guide/language-features/arrays/index.md)  
 [<span data-ttu-id="59f30-113">Collections</span><span class="sxs-lookup"><span data-stu-id="59f30-113">Collections</span></span>](../../../standard/collections/index.md)
