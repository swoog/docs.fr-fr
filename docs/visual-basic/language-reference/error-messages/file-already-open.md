---
title: Le fichier est déjà ouvert.
ms.date: 07/20/2015
f1_keywords:
- vbrID55
ms.assetid: d674a0fb-ef16-4cc2-9da7-709a8a07dbea
ms.openlocfilehash: 8ec878e04b0128c997c5be51d2c714d55abcde8c
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64665117"
---
# <a name="file-already-open"></a><span data-ttu-id="a8b38-102">Le fichier est déjà ouvert.</span><span class="sxs-lookup"><span data-stu-id="a8b38-102">File already open</span></span>
<span data-ttu-id="a8b38-103">Parfois, un fichier doit être fermé avant un autre `FileOpen` ou autre opération peut se produire.</span><span class="sxs-lookup"><span data-stu-id="a8b38-103">Sometimes a file must be closed before another `FileOpen` or other operation can occur.</span></span> <span data-ttu-id="a8b38-104">Cette erreur peut avoir plusieurs causes, dont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a8b38-104">Among the possible causes of this error are:</span></span>  
  
- <span data-ttu-id="a8b38-105">Un mode de sortie séquentielle `FileOpen` opération a été exécutée pour un fichier qui est déjà ouvert</span><span class="sxs-lookup"><span data-stu-id="a8b38-105">A sequential output mode `FileOpen` operation was executed for a file that is already open</span></span>  
  
- <span data-ttu-id="a8b38-106">Une instruction fait référence à un fichier ouvert.</span><span class="sxs-lookup"><span data-stu-id="a8b38-106">A statement refers to an open file.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="a8b38-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="a8b38-107">To correct this error</span></span>  
  
1. <span data-ttu-id="a8b38-108">Fermez le fichier avant d’exécuter l’instruction.</span><span class="sxs-lookup"><span data-stu-id="a8b38-108">Close the file before executing the statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a8b38-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8b38-109">See also</span></span>

- <xref:Microsoft.VisualBasic.FileSystem.FileOpen%2A>
