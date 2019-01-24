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
# <a name="an-invalid-name-was-specified-for-the-event-log"></a>Un nom de fichier non valide a été spécifié pour le journal des événements
Un nom de fichier non valide a été spécifié pour le journal des événements. Cette erreur est généralement due à des caractères non valides dans le nom, à un nom de fichier vide ou à un nom de fichier trop long.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Si le nom spécifié fait plus de huit caractères, vérifiez qu’il n’existe aucun conflit avec les noms des autres journaux des événements. Seuls les huit premiers caractères sont évalués pour déterminer si le nom est unique.  
  
-   Si vous fournissez un chemin, vérifiez qu’il est correctement analysé.  
  
-   Vérifiez que le nom ne contient aucun caractère non valide. Les caractères `<`, `>`, `:`, `"`, `/`, `\`et `|`ne peuvent pas être utilisés dans un nom de fichier.  
  
## <a name="see-also"></a>Voir aussi
- [Guide pratique pour Analyser des chemins](../../visual-basic/developing-apps/programming/drives-directories-files/how-to-parse-file-paths.md)
- [Guide pratique pour Renommer un fichier](../../visual-basic/developing-apps/programming/drives-directories-files/how-to-rename-a-file.md)

