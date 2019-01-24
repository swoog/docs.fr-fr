---
title: Absence de souris
ms.date: 07/20/2015
f1_keywords:
- vbrMouse_NoMouseIsPresent
ms.assetid: 4472fd57-4217-4463-9d3c-dc4a8fe88f1b
ms.openlocfilehash: f69371ea2db1aba5d3ad501ab41a9ea6e646ad3b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54557875"
---
# <a name="no-mouse-is-present"></a><span data-ttu-id="27375-102">Absence de souris</span><span class="sxs-lookup"><span data-stu-id="27375-102">No mouse is present</span></span>
<span data-ttu-id="27375-103">L’une des propriétés de l’objet `My.Computer.Mouse` a été appelée, mais aucune souris ou aucun port de souris n’est installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="27375-103">One of the properties of the `My.Computer.Mouse` object was called, but the computer has no mouse or mouse port installed.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="27375-104">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="27375-104">To correct this error</span></span>  
  
-   <span data-ttu-id="27375-105">Ajoutez un bloc `Try...Catch` autour de l’appel à la propriété de l’objet `My.Computer.Mouse` .</span><span class="sxs-lookup"><span data-stu-id="27375-105">Add a `Try...Catch` block around the call to the property of the `My.Computer.Mouse` object.</span></span>  
  
     <span data-ttu-id="27375-106">— ou —</span><span class="sxs-lookup"><span data-stu-id="27375-106">— or —</span></span>  
  
-   <span data-ttu-id="27375-107">Installez une souris sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="27375-107">Install a mouse on the computer.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="27375-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27375-108">See also</span></span>
- [<span data-ttu-id="27375-109">My.Computer.Mouse</span><span class="sxs-lookup"><span data-stu-id="27375-109">My.Computer.Mouse</span></span>](xref:Microsoft.VisualBasic.Devices.Mouse)
- [<span data-ttu-id="27375-110">Gestion des exceptions et des erreurs en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="27375-110">Exception and Error Handling in Visual Basic</span></span>](https://msdn.microsoft.com/library/3e351e73-cf23-40ab-8b60-05794160529e)
- [<span data-ttu-id="27375-111">Try...Catch...Finally (instruction)</span><span class="sxs-lookup"><span data-stu-id="27375-111">Try...Catch...Finally Statement</span></span>](../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
