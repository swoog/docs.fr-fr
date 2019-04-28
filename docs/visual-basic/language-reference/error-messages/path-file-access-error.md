---
title: Erreur d’accès de fichier de chemin d’accès
ms.date: 07/20/2015
f1_keywords:
- vbrID75
ms.assetid: 6ce3a161-7316-46bd-a785-0d50e5414020
ms.openlocfilehash: 4f18c9216aa24840bc205534a97124d12698cb98
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61799175"
---
# <a name="pathfile-access-error"></a><span data-ttu-id="777f7-102">Erreur dans le chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="777f7-102">Path/File access error</span></span>
<span data-ttu-id="777f7-103">Pendant une opération d’accès au fichier ou d’accès au disque, le système d’exploitation ne peut pas établir une connexion entre le chemin d’accès et le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="777f7-103">During a file-access or disk-access operation, the operating system could not make a connection between the path and the file name.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="777f7-104">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="777f7-104">To correct this error</span></span>  
  
1. <span data-ttu-id="777f7-105">Assurez-vous que la spécification de fichier est correctement formatée.</span><span class="sxs-lookup"><span data-stu-id="777f7-105">Make sure the file specification is correctly formatted.</span></span> <span data-ttu-id="777f7-106">Un nom de fichier peut contenir un qualifié complet (absolu) ou par rapport chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="777f7-106">A file name can contain a fully qualified (absolute) or relative path.</span></span> <span data-ttu-id="777f7-107">Un chemin d’accès qualifié complet commence par le nom du lecteur (si le chemin d’accès est sur un autre lecteur) et répertorie le chemin d’accès explicite à partir de la racine du fichier.</span><span class="sxs-lookup"><span data-stu-id="777f7-107">A fully qualified path starts with the drive name (if the path is on another drive) and lists the explicit path from the root to the file.</span></span> <span data-ttu-id="777f7-108">N’importe quel chemin d’accès qui n’est pas qualifié complet est relatif le lecteur actuel et le répertoire.</span><span class="sxs-lookup"><span data-stu-id="777f7-108">Any path that is not fully qualified is relative to the current drive and directory.</span></span>  
  
2. <span data-ttu-id="777f7-109">Assurez-vous que vous n’avez pas essayé d’enregistrer un fichier qui remplace un fichier en lecture seule existant.</span><span class="sxs-lookup"><span data-stu-id="777f7-109">Make sure that you did not attempt to save a file that would replace an existing read-only file.</span></span> <span data-ttu-id="777f7-110">Si c’est le cas, modifiez l’attribut en lecture seule du fichier cible ou enregistrez le fichier avec un autre nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="777f7-110">If this is the case, change the read-only attribute of the target file, or save the file with a different file name.</span></span>  
  
3. <span data-ttu-id="777f7-111">Assurez-vous que vous n’avez pas tenté d’ouvrir un fichier en lecture seule dans séquentiel `Output` ou `Append` mode.</span><span class="sxs-lookup"><span data-stu-id="777f7-111">Make sure you did not attempt to open a read-only file in sequential `Output` or `Append` mode.</span></span> <span data-ttu-id="777f7-112">Si c’est le cas, ouvrez le fichier dans `Input` mode ou modifier l’attribut en lecture seule du fichier.</span><span class="sxs-lookup"><span data-stu-id="777f7-112">If this is the case, open the file in `Input` mode or change the read-only attribute of the file.</span></span>  
  
4. <span data-ttu-id="777f7-113">Assurez-vous que vous n’avez pas tenté de modifier un projet Visual Basic dans une base de données ou un document.</span><span class="sxs-lookup"><span data-stu-id="777f7-113">Make sure you did not attempt to change a Visual Basic project within a database or document.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="777f7-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="777f7-114">See also</span></span>

- [<span data-ttu-id="777f7-115">Types d’erreurs</span><span class="sxs-lookup"><span data-stu-id="777f7-115">Error Types</span></span>](../../../visual-basic/programming-guide/language-features/error-types.md)
