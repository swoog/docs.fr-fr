---
title: L'entrée dépasse la fin du fichier
ms.date: 07/20/2015
f1_keywords:
- vbrID62
ms.assetid: 65292704-6e7d-4622-9f50-eb655a59b016
ms.openlocfilehash: 5da14c7a28ecdcd023fc6439cb6ed64444c1183b
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59342776"
---
# <a name="input-past-end-of-file"></a>L'entrée dépasse la fin du fichier
Soit un `Input` instruction lit à partir d’un fichier qui est vide ou une dans laquelle toutes les données est utilisé, ou vous avez utilisé le `EOF` fonction avec un fichier ouvert pour un accès binaire.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Utilisez le `EOF` fonction immédiatement avant la `Input` instruction pour détecter la fin du fichier.  
  
2. Si le fichier est ouvert pour un accès binaire, utilisez `Seek` et `Loc`.  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.FileSystem.Input%2A>
- <xref:Microsoft.VisualBasic.FileSystem.EOF%2A>
- <xref:Microsoft.VisualBasic.FileSystem.Seek%2A>
- <xref:Microsoft.VisualBasic.FileSystem.Loc%2A>
