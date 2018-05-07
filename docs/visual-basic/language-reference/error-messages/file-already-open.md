---
title: Le fichier est déjà ouvert.
ms.date: 07/20/2015
f1_keywords:
- vbrID55
ms.assetid: d674a0fb-ef16-4cc2-9da7-709a8a07dbea
ms.openlocfilehash: 75a08b411a4afd7ea8e11953f1d465b082faa712
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="file-already-open"></a>Le fichier est déjà ouvert.
Un fichier doit parfois être fermé avant un autre `FileOpen` ou autre opération ne peut se produire. Cette erreur peut avoir plusieurs causes, dont les suivantes :  
  
-   Un mode de sortie séquentielle `FileOpen` opération a été exécutée pour un fichier qui est déjà ouvert  
  
-   Une instruction fait référence à un fichier ouvert.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Fermez le fichier avant d’exécuter l’instruction.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.FileSystem.FileOpen%2A>
