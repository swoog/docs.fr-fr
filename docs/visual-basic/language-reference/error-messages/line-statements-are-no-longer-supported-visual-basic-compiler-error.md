---
title: '&#39;Ligne&#39; instructions ne sont plus prises en charge (erreur du compilateur Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- bc30830
- vbc30830
helpviewer_keywords:
- BC30830
ms.assetid: 4734bc1d-882e-4555-b498-1f1ec0399d16
ms.openlocfilehash: 36226cc371ffb8a51cb8d0f918952f1c717aea10
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54702969"
---
# <a name="39line39-statements-are-no-longer-supported-visual-basic-compiler-error"></a>&#39;Ligne&#39; instructions ne sont plus prises en charge (erreur du compilateur Visual Basic)
Instructions de ligne ne sont plus prises en charge. Fonctionnalité d’e/s de fichier est disponible en tant que `Microsoft.VisualBasic.FileSystem.LineInput` et fonctionnalités graphiques sont disponible en tant que `System.Drawing.Graphics.DrawLine`.  
  
 **ID d’erreur :** BC30830  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Accès aux fichiers, utilisez `Microsoft.VisualBasic.FileSystem.LineInput`.  
  
2.  Pour des graphiques, utilisez `System.Drawing.Graphics.Drawline`.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.IO>
- <xref:System.Drawing>
- [Accès au fichier avec Visual Basic](../../../visual-basic/developing-apps/programming/drives-directories-files/file-access.md)
