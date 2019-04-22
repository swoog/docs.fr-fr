---
title: Le fichier est déjà ouvert.
ms.date: 07/20/2015
f1_keywords:
- vbrID55
ms.assetid: d674a0fb-ef16-4cc2-9da7-709a8a07dbea
ms.openlocfilehash: 401801c7c9072ce11f9eafdb84f2b377669ae545
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59770358"
---
# <a name="file-already-open"></a>Le fichier est déjà ouvert.
Parfois, un fichier doit être fermé avant un autre `FileOpen` ou autre opération peut se produire. Cette erreur peut avoir plusieurs causes, dont les suivantes :  
  
-   Un mode de sortie séquentielle `FileOpen` opération a été exécutée pour un fichier qui est déjà ouvert  
  
-   Une instruction fait référence à un fichier ouvert.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Fermez le fichier avant d’exécuter l’instruction.  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.FileSystem.FileOpen%2A>
