---
title: Les instructions 'Line' ne sont plus prises en charge (erreur du compilateur Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- bc30830
- vbc30830
helpviewer_keywords:
- BC30830
ms.assetid: 4734bc1d-882e-4555-b498-1f1ec0399d16
ms.openlocfilehash: 7616bcdc39ab479049586534fac22f1e2d96a700
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58831837"
---
# <a name="line-statements-are-no-longer-supported-visual-basic-compiler-error"></a>Les instructions 'Line' ne sont plus prises en charge (erreur du compilateur Visual Basic)
Instructions de ligne ne sont plus prises en charge. Fonctionnalité d’e/s de fichier est disponible en tant que `Microsoft.VisualBasic.FileSystem.LineInput` et fonctionnalités graphiques sont disponible en tant que `System.Drawing.Graphics.DrawLine`.  
  
 **ID d’erreur :** BC30830  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Accès aux fichiers, utilisez `Microsoft.VisualBasic.FileSystem.LineInput`.  
  
2.  Pour des graphiques, utilisez `System.Drawing.Graphics.Drawline`.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.IO>
- <xref:System.Drawing>
- [Accès au fichier avec Visual Basic](../../../visual-basic/developing-apps/programming/drives-directories-files/file-access.md)
