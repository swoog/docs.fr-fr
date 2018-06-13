---
title: L'entrée dépasse la fin du fichier
ms.date: 07/20/2015
f1_keywords:
- vbrID62
ms.assetid: 65292704-6e7d-4622-9f50-eb655a59b016
ms.openlocfilehash: abd5f5c6e5df262d1deadd74f0a146a8d436ceb3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33586739"
---
# <a name="input-past-end-of-file"></a><span data-ttu-id="3714d-102">L'entrée dépasse la fin du fichier</span><span class="sxs-lookup"><span data-stu-id="3714d-102">Input past end of file</span></span>
<span data-ttu-id="3714d-103">Soit un `Input` instruction lit à partir d’un fichier qui est vide ou dans lequel toutes les données est utilisée, ou vous avez utilisé le `EOF` fonction avec un fichier ouvert pour un accès binaire.</span><span class="sxs-lookup"><span data-stu-id="3714d-103">Either an `Input` statement is reading from a file that is empty or one in which all the data is used, or you used the `EOF` function with a file opened for binary access.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="3714d-104">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="3714d-104">To correct this error</span></span>  
  
1.  <span data-ttu-id="3714d-105">Utilisez le `EOF` de fonction immédiatement avant la `Input` instruction pour détecter la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="3714d-105">Use the `EOF` function immediately before the `Input` statement to detect the end of the file.</span></span>  
  
2.  <span data-ttu-id="3714d-106">Si le fichier est ouvert pour un accès binaire, utilisez `Seek` et `Loc`.</span><span class="sxs-lookup"><span data-stu-id="3714d-106">If the file is opened for binary access, use `Seek` and `Loc`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3714d-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3714d-107">See Also</span></span>  
 <xref:Microsoft.VisualBasic.FileSystem.Input%2A>  
 <xref:Microsoft.VisualBasic.FileSystem.EOF%2A>  
 <xref:Microsoft.VisualBasic.FileSystem.Seek%2A>  
 <xref:Microsoft.VisualBasic.FileSystem.Loc%2A>
