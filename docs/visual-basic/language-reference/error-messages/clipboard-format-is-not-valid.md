---
title: Format de Presse-papiers non valide
ms.date: 07/20/2015
f1_keywords:
- vbrID460
ms.assetid: 71a4a045-65bb-417d-b3bd-99a9fa3c53f6
ms.openlocfilehash: 15bc530d1030a8c4d720321ea249fdd7fb6cd8b6
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64623100"
---
# <a name="clipboard-format-is-not-valid"></a>Format de Presse-papiers non valide
Le format de Presse-papiers spécifié n’est pas compatible avec la méthode en cours d’exécution. Parmi les causes possibles de cette erreur sont :  
  
- À l’aide du Presse-papiers `GetText` ou `SetText` méthode avec un format de Presse-papiers autre que `vbCFText` ou `vbCFLink`.  
  
- À l’aide du Presse-papiers `GetData` ou `SetData` méthode avec un format de Presse-papiers autre que `vbCFBitmap`, `vbCFDIB`, ou `vbCFMetafile`.  
  
- À l’aide de la `GetData` ou `SetData` méthodes d’un `DataObject` avec un format de Presse-papiers dans la plage réservée par Microsoft Windows pour des formats (& HC000 - & HFFFF), lorsque ce format de Presse-papiers n’a pas été inscrit avec Microsoft Windows .  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Supprimer le format non valide et spécifier une valide.  
  
## <a name="see-also"></a>Voir aussi

- [Presse-papiers : Ajout d’autres formats](/cpp/mfc/clipboard-adding-other-formats)
