---
title: Un nom de fichier non valide a été spécifié pour le journal des événements
ms.date: 07/20/2015
ms.assetid: b1b158bd-f13f-4371-a8af-31c0e86ae6be
ms.openlocfilehash: 242c5394011fd018a03f81b9b56bcfd7015682dd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54604393"
---
# <a name="an-invalid-name-was-specified-for-the-event-log"></a><span data-ttu-id="9664a-102">Un nom de fichier non valide a été spécifié pour le journal des événements</span><span class="sxs-lookup"><span data-stu-id="9664a-102">An invalid name was specified for the event log</span></span>
<span data-ttu-id="9664a-103">Un nom de fichier non valide a été spécifié pour le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="9664a-103">An invalid name was specified for the event log.</span></span> <span data-ttu-id="9664a-104">Cette erreur est généralement due à des caractères non valides dans le nom, à un nom de fichier vide ou à un nom de fichier trop long.</span><span class="sxs-lookup"><span data-stu-id="9664a-104">Usually this is a result of invalid characters in the name, a blank file name, or a file name that is too long.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="9664a-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="9664a-105">To correct this error</span></span>  
  
-   <span data-ttu-id="9664a-106">Si le nom spécifié fait plus de huit caractères, vérifiez qu’il n’existe aucun conflit avec les noms des autres journaux des événements.</span><span class="sxs-lookup"><span data-stu-id="9664a-106">If the specified name is more than eight characters, make sure there is no conflict with the names of other event logs.</span></span> <span data-ttu-id="9664a-107">Seuls les huit premiers caractères sont évalués pour déterminer si le nom est unique.</span><span class="sxs-lookup"><span data-stu-id="9664a-107">Only the first eight characters are evaluated when determining if the name is unique.</span></span>  
  
-   <span data-ttu-id="9664a-108">Si vous fournissez un chemin, vérifiez qu’il est correctement analysé.</span><span class="sxs-lookup"><span data-stu-id="9664a-108">If supplying a path, make sure it is parsed correctly.</span></span>  
  
-   <span data-ttu-id="9664a-109">Vérifiez que le nom ne contient aucun caractère non valide.</span><span class="sxs-lookup"><span data-stu-id="9664a-109">Check that there are no invalid characters in the name.</span></span> <span data-ttu-id="9664a-110">Les caractères `<`, `>`, `:`, `"`, `/`, `\`et `|`ne peuvent pas être utilisés dans un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="9664a-110">Characters that cannot be used in a file name include `<`, `>`, `:`, `"`, `/`, `\`, and `|`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9664a-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9664a-111">See also</span></span>
- [<span data-ttu-id="9664a-112">Guide pratique pour Analyser des chemins</span><span class="sxs-lookup"><span data-stu-id="9664a-112">How to: Parse File Paths</span></span>](../../visual-basic/developing-apps/programming/drives-directories-files/how-to-parse-file-paths.md)
- [<span data-ttu-id="9664a-113">Guide pratique pour Renommer un fichier</span><span class="sxs-lookup"><span data-stu-id="9664a-113">How to: Rename a File</span></span>](../../visual-basic/developing-apps/programming/drives-directories-files/how-to-rename-a-file.md)

