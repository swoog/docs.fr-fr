---
title: Erreur d’accès de fichier de chemin d’accès
ms.date: 07/20/2015
f1_keywords:
- vbrID75
ms.assetid: 6ce3a161-7316-46bd-a785-0d50e5414020
ms.openlocfilehash: 4f18c9216aa24840bc205534a97124d12698cb98
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59342152"
---
# <a name="pathfile-access-error"></a>Erreur dans le chemin d’accès
Pendant une opération d’accès au fichier ou d’accès au disque, le système d’exploitation ne peut pas établir une connexion entre le chemin d’accès et le nom de fichier.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Assurez-vous que la spécification de fichier est correctement formatée. Un nom de fichier peut contenir un qualifié complet (absolu) ou par rapport chemin d’accès. Un chemin d’accès qualifié complet commence par le nom du lecteur (si le chemin d’accès est sur un autre lecteur) et répertorie le chemin d’accès explicite à partir de la racine du fichier. N’importe quel chemin d’accès qui n’est pas qualifié complet est relatif le lecteur actuel et le répertoire.  
  
2. Assurez-vous que vous n’avez pas essayé d’enregistrer un fichier qui remplace un fichier en lecture seule existant. Si c’est le cas, modifiez l’attribut en lecture seule du fichier cible ou enregistrez le fichier avec un autre nom de fichier.  
  
3. Assurez-vous que vous n’avez pas tenté d’ouvrir un fichier en lecture seule dans séquentiel `Output` ou `Append` mode. Si c’est le cas, ouvrez le fichier dans `Input` mode ou modifier l’attribut en lecture seule du fichier.  
  
4. Assurez-vous que vous n’avez pas tenté de modifier un projet Visual Basic dans une base de données ou un document.  
  
## <a name="see-also"></a>Voir aussi

- [Types d'erreurs](../../../visual-basic/programming-guide/language-features/error-types.md)
