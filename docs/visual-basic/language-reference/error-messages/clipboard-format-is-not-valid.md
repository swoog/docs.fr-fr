---
title: Format de Presse-papiers non valide
ms.date: 07/20/2015
f1_keywords:
- vbrID460
ms.assetid: 71a4a045-65bb-417d-b3bd-99a9fa3c53f6
ms.openlocfilehash: eef16096b269902dbaca6a344abf4c5f6a504fb7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33586219"
---
# <a name="clipboard-format-is-not-valid"></a>Format de Presse-papiers non valide
Le format de Presse-papiers spécifié n’est pas compatible avec la méthode en cours d’exécution. Parmi les causes possibles de cette erreur sont :  
  
-   À l’aide du Presse-papiers `GetText` ou `SetText` méthode avec un format de Presse-papiers autre que `vbCFText` ou `vbCFLink`.  
  
-   À l’aide du Presse-papiers `GetData` ou `SetData` méthode avec un format de Presse-papiers autre que `vbCFBitmap`, `vbCFDIB`, ou `vbCFMetafile`.  
  
-   À l’aide de la `DataObject``GetData` méthode ou `SetData` méthode avec un format de Presse-papiers dans la plage réservée par Microsoft Windows pour des formats (& HC000 - & HFFFF), lorsque ce format de Presse-papiers n’a pas été inscrit auprès de Microsoft Windows.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Supprimez le format incorrect et spécifier une valide.  
  
## <a name="see-also"></a>Voir aussi  
 [Presse-papiers : ajout d’autres formats](/cpp/mfc/clipboard-adding-other-formats)
