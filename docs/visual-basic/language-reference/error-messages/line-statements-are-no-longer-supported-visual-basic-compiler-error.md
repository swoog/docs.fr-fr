---
title: '&#39;Ligne&#39; instructions ne sont plus pris en charge (erreur du compilateur Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- bc30830
- vbc30830
helpviewer_keywords:
- BC30830
ms.assetid: 4734bc1d-882e-4555-b498-1f1ec0399d16
ms.openlocfilehash: 06bba0ebfc2faec24f4720c45de3bdcfec993499
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33587877"
---
# <a name="39line39-statements-are-no-longer-supported-visual-basic-compiler-error"></a>&#39;Ligne&#39; instructions ne sont plus pris en charge (erreur du compilateur Visual Basic)
Instructions de ligne ne sont plus prises en charge. La fonctionnalité d’e/s de fichier est disponible en tant que `Microsoft.VisualBasic.FileSystem.LineInput` et fonctionnalités graphiques est disponible en tant que `System.Drawing.Graphics.DrawLine`.  
  
 **ID d’erreur :** BC30830  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Accès au fichier, utilisez `Microsoft.VisualBasic.FileSystem.LineInput`.  
  
2.  Si des graphiques, utilisez `System.Drawing.Graphics.Drawline`.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.IO>  
 <xref:System.Drawing>  
 [Accès au fichier avec Visual Basic](../../../visual-basic/developing-apps/programming/drives-directories-files/file-access.md)
