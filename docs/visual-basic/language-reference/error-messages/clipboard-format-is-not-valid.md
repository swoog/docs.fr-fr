---
title: Format de Presse-papiers non valide
ms.date: 07/20/2015
f1_keywords:
- vbrID460
ms.assetid: 71a4a045-65bb-417d-b3bd-99a9fa3c53f6
ms.openlocfilehash: 5ec077be30b0afc8917d431dc9bd73c8dd41be89
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58817173"
---
# <a name="clipboard-format-is-not-valid"></a>Format de Presse-papiers non valide
Le format de Presse-papiers spécifié n’est pas compatible avec la méthode en cours d’exécution. Parmi les causes possibles de cette erreur sont :  
  
-   À l’aide du Presse-papiers `GetText` ou `SetText` méthode avec un format de Presse-papiers autre que `vbCFText` ou `vbCFLink`.  
  
-   À l’aide du Presse-papiers `GetData` ou `SetData` méthode avec un format de Presse-papiers autre que `vbCFBitmap`, `vbCFDIB`, ou `vbCFMetafile`.  
  
-   À l’aide de la `GetData` ou `SetData` méthodes d’un `DataObject` avec un format de Presse-papiers dans la plage réservée par Microsoft Windows pour des formats (& HC000 - & HFFFF), lorsque ce format de Presse-papiers n’a pas été inscrit avec Microsoft Windows .  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Supprimer le format non valide et spécifier une valide.  
  
## <a name="see-also"></a>Voir aussi

- [Presse-papiers : Ajout d’autres Formats](/cpp/mfc/clipboard-adding-other-formats)
