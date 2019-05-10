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
# <a name="file-already-open"></a>Le fichier est déjà ouvert.
Parfois, un fichier doit être fermé avant un autre `FileOpen` ou autre opération peut se produire. Cette erreur peut avoir plusieurs causes, dont les suivantes :  
  
- Un mode de sortie séquentielle `FileOpen` opération a été exécutée pour un fichier qui est déjà ouvert  
  
- Une instruction fait référence à un fichier ouvert.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Fermez le fichier avant d’exécuter l’instruction.  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.FileSystem.FileOpen%2A>
