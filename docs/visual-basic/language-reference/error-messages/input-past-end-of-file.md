---
title: L'entrée dépasse la fin du fichier
ms.date: 07/20/2015
f1_keywords:
- vbrID62
ms.assetid: 65292704-6e7d-4622-9f50-eb655a59b016
ms.openlocfilehash: 29a9b5ce3c3f8e6a02b52beda1338fd699143570
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491335"
---
# <a name="input-past-end-of-file"></a>L'entrée dépasse la fin du fichier
Soit un `Input` instruction lit à partir d’un fichier qui est vide ou une dans laquelle toutes les données est utilisé, ou vous avez utilisé le `EOF` fonction avec un fichier ouvert pour un accès binaire.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Utilisez le `EOF` fonction immédiatement avant la `Input` instruction pour détecter la fin du fichier.  
  
2.  Si le fichier est ouvert pour un accès binaire, utilisez `Seek` et `Loc`.  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.FileSystem.Input%2A>
- <xref:Microsoft.VisualBasic.FileSystem.EOF%2A>
- <xref:Microsoft.VisualBasic.FileSystem.Seek%2A>
- <xref:Microsoft.VisualBasic.FileSystem.Loc%2A>
