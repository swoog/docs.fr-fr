---
title: Impossible de créer le fichier temporaire nécessaire
ms.date: 07/20/2015
f1_keywords:
- vbrID322
ms.assetid: 53617b5b-eb06-4188-b4c2-8607cb9fbc79
ms.openlocfilehash: 658c2ab1dc210bf472646bce529ae5ffd7f67bc5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61649983"
---
# <a name="cant-create-necessary-temporary-file"></a><span data-ttu-id="b48c0-102">Impossible de créer le fichier temporaire nécessaire</span><span class="sxs-lookup"><span data-stu-id="b48c0-102">Can't create necessary temporary file</span></span>
<span data-ttu-id="b48c0-103">Le lecteur est complet qui contient le répertoire spécifié par la variable d’environnement TEMP, ou la variable d’environnement TEMP spécifie un lecteur non valide ou en lecture seule ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="b48c0-103">Either the drive is full that contains the directory specified by the TEMP environment variable, or the TEMP environment variable specifies an invalid or read-only drive or directory.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b48c0-104">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="b48c0-104">To correct this error</span></span>  
  
1. <span data-ttu-id="b48c0-105">Supprimez les fichiers à partir du lecteur, si elle est complète.</span><span class="sxs-lookup"><span data-stu-id="b48c0-105">Delete files from the drive, if full.</span></span>  
  
2. <span data-ttu-id="b48c0-106">Spécifiez un lecteur différent dans la variable d’environnement TEMP.</span><span class="sxs-lookup"><span data-stu-id="b48c0-106">Specify a different drive in the TEMP environment variable.</span></span>  
  
3. <span data-ttu-id="b48c0-107">Spécifiez un lecteur valide pour la variable d’environnement TEMP.</span><span class="sxs-lookup"><span data-stu-id="b48c0-107">Specify a valid drive for the TEMP environment variable.</span></span>  
  
4. <span data-ttu-id="b48c0-108">Supprimez la restriction en lecture seule à partir du lecteur actuellement spécifié ou le répertoire.</span><span class="sxs-lookup"><span data-stu-id="b48c0-108">Remove the read-only restriction from the currently specified drive or directory.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b48c0-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b48c0-109">See also</span></span>

- [<span data-ttu-id="b48c0-110">Types d’erreurs</span><span class="sxs-lookup"><span data-stu-id="b48c0-110">Error Types</span></span>](../../../visual-basic/programming-guide/language-features/error-types.md)
