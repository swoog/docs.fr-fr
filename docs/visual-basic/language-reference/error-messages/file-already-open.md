---
title: Le fichier est déjà ouvert.
ms.date: 07/20/2015
f1_keywords:
- vbrID55
ms.assetid: d674a0fb-ef16-4cc2-9da7-709a8a07dbea
ms.openlocfilehash: 75a08b411a4afd7ea8e11953f1d465b082faa712
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33586668"
---
# <a name="file-already-open"></a><span data-ttu-id="b6ba2-102">Le fichier est déjà ouvert.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-102">File already open</span></span>
<span data-ttu-id="b6ba2-103">Un fichier doit parfois être fermé avant un autre `FileOpen` ou autre opération ne peut se produire.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-103">Sometimes a file must be closed before another `FileOpen` or other operation can occur.</span></span> <span data-ttu-id="b6ba2-104">Cette erreur peut avoir plusieurs causes, dont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6ba2-104">Among the possible causes of this error are:</span></span>  
  
-   <span data-ttu-id="b6ba2-105">Un mode de sortie séquentielle `FileOpen` opération a été exécutée pour un fichier qui est déjà ouvert</span><span class="sxs-lookup"><span data-stu-id="b6ba2-105">A sequential output mode `FileOpen` operation was executed for a file that is already open</span></span>  
  
-   <span data-ttu-id="b6ba2-106">Une instruction fait référence à un fichier ouvert.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-106">A statement refers to an open file.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b6ba2-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="b6ba2-107">To correct this error</span></span>  
  
1.  <span data-ttu-id="b6ba2-108">Fermez le fichier avant d’exécuter l’instruction.</span><span class="sxs-lookup"><span data-stu-id="b6ba2-108">Close the file before executing the statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b6ba2-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6ba2-109">See Also</span></span>  
 <xref:Microsoft.VisualBasic.FileSystem.FileOpen%2A>
