---
title: Le fichier est déjà ouvert.
ms.date: 07/20/2015
f1_keywords:
- vbrID55
ms.assetid: d674a0fb-ef16-4cc2-9da7-709a8a07dbea
ms.openlocfilehash: 401801c7c9072ce11f9eafdb84f2b377669ae545
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59301319"
---
# <a name="file-already-open"></a><span data-ttu-id="da7ec-102">Le fichier est déjà ouvert.</span><span class="sxs-lookup"><span data-stu-id="da7ec-102">File already open</span></span>
<span data-ttu-id="da7ec-103">Parfois, un fichier doit être fermé avant un autre `FileOpen` ou autre opération peut se produire.</span><span class="sxs-lookup"><span data-stu-id="da7ec-103">Sometimes a file must be closed before another `FileOpen` or other operation can occur.</span></span> <span data-ttu-id="da7ec-104">Cette erreur peut avoir plusieurs causes, dont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="da7ec-104">Among the possible causes of this error are:</span></span>  
  
-   <span data-ttu-id="da7ec-105">Un mode de sortie séquentielle `FileOpen` opération a été exécutée pour un fichier qui est déjà ouvert</span><span class="sxs-lookup"><span data-stu-id="da7ec-105">A sequential output mode `FileOpen` operation was executed for a file that is already open</span></span>  
  
-   <span data-ttu-id="da7ec-106">Une instruction fait référence à un fichier ouvert.</span><span class="sxs-lookup"><span data-stu-id="da7ec-106">A statement refers to an open file.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="da7ec-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="da7ec-107">To correct this error</span></span>  
  
1. <span data-ttu-id="da7ec-108">Fermez le fichier avant d’exécuter l’instruction.</span><span class="sxs-lookup"><span data-stu-id="da7ec-108">Close the file before executing the statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="da7ec-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da7ec-109">See also</span></span>

- <xref:Microsoft.VisualBasic.FileSystem.FileOpen%2A>
