---
title: Chaîne de modèle non valide
ms.date: 07/20/2015
ms.assetid: ec1aecdb-5339-4a93-be71-eec56b1d7438
ms.openlocfilehash: 7390b9b32eea248969813b52f8d9799798718de0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59298680"
---
# <a name="invalid-pattern-string"></a>Chaîne de modèle non valide
La chaîne de modèle spécifiée dans l’opération `Like` d’une recherche n’est pas valide.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Examinez les caractères valides des expressions de liste.  
  
2. Dans la plage de modèles, vérifiez que le caractère de début de plage est inférieur au caractère de fin de plage, comme dans `[a-z]`.  
  
3. Dans la plage de modèles, vérifiez que plusieurs traits d’union ne se situent pas les uns à côté des autres, comme dans `[a--z]`.  
  
4. Terminez les plages de modèles par un crochet fermant.  
  
## <a name="see-also"></a>Voir aussi

- [Like (opérateur)](../../visual-basic/language-reference/operators/like-operator.md)
