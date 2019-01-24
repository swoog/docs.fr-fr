---
title: Trop de fichiers
ms.date: 07/20/2015
f1_keywords:
- vbrID67
ms.assetid: 2ff203e2-bba6-43ae-b72f-8e92a881c98f
ms.openlocfilehash: 15e08cedbd58016959f00e1ca817019937775df2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54737229"
---
# <a name="too-many-files"></a><span data-ttu-id="b0d13-102">Trop de fichiers</span><span class="sxs-lookup"><span data-stu-id="b0d13-102">Too many files</span></span>
<span data-ttu-id="b0d13-103">Plusieurs fichiers ont été créés dans le répertoire racine autorisés par le système d’exploitation ou plus de fichiers que le nombre spécifié dans le **fichiers =** définissant dans votre fichier CONFIG. Fichier SYS.</span><span class="sxs-lookup"><span data-stu-id="b0d13-103">Either more files have been created in the root directory than the operating system permits, or more files have been opened than the number specified in the **files=** setting in your CONFIG.SYS file.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b0d13-104">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="b0d13-104">To correct this error</span></span>  
  
1.  <span data-ttu-id="b0d13-105">Si votre programme est ouverture, fermeture ou l’enregistrement des fichiers dans le répertoire racine, modifiez votre programme afin qu’il utilise un sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="b0d13-105">If your program is opening, closing, or saving files in the root directory, change your program so that it uses a subdirectory.</span></span>  
  
2.  <span data-ttu-id="b0d13-106">Augmenter le nombre de fichiers spécifiés dans votre **fichiers =** définissant dans votre fichier CONFIG. SYS et redémarrez votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b0d13-106">Increase the number of files specified in your **files=** setting in your CONFIG.SYS file, and restart your computer.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b0d13-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0d13-107">See also</span></span>
- [<span data-ttu-id="b0d13-108">Types d’erreurs</span><span class="sxs-lookup"><span data-stu-id="b0d13-108">Error Types</span></span>](../../../visual-basic/programming-guide/language-features/error-types.md)
