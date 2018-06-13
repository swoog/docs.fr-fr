---
title: 'Comment : appeler une procédure surchargée (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], overloading
- procedures [Visual Basic], calling
- procedures [Visual Basic], multiple versions
- procedure calls [Visual Basic], overloaded
ms.assetid: 3bb331fb-f6bc-406f-9ca0-9609b497014c
ms.openlocfilehash: 802a312d6ec6640594f3c6b662202d1ffcf2376d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33649124"
---
# <a name="how-to-call-an-overloaded-procedure-visual-basic"></a>Comment : appeler une procédure surchargée (Visual Basic)
L’avantage de la surcharge d’une procédure est la flexibilité de l’appel. Le code appelant peut obtenir les informations que nécessaires pour passer à la procédure, puis appelez un seul nom de procédure, quel que soit les arguments, il passe.  
  
### <a name="to-call-a-procedure-that-has-more-than-one-version-defined"></a>Pour appeler une procédure qui possède plusieurs versions définies  
  
1.  Dans le code appelant, déterminez les données à passer à la procédure.  
  
2.  Écrire l’appel de procédure de façon normale, présenter les données dans la liste d’arguments. Assurez-vous que les arguments correspondent à la liste des paramètres de l’une des versions définies pour la procédure.  
  
3.  Il est inutile de déterminer la version de la procédure à appeler. Visual Basic passe le contrôle à la version correspondant à votre liste d’arguments.  
  
     L’exemple suivant appelle la `post` procédure déclarée dans [Comment : définir plusieurs Versions d’une procédure](./how-to-define-multiple-versions-of-a-procedure.md). Il obtient l’identification de client, détermine s’il est un `String` ou `Integer`, puis, dans les deux cas, appelle la même procédure.  
  
     [!code-vb[VbVbcnProcedures#56](./codesnippet/VisualBasic/how-to-call-an-overloaded-procedure_1.vb)]  
  
     [!code-vb[VbVbcnProcedures#57](./codesnippet/VisualBasic/how-to-call-an-overloaded-procedure_2.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Procédures](./index.md)  
 [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)  
 [Surcharge de procédure](./procedure-overloading.md)  
 [Procédures de dépannage](./troubleshooting-procedures.md)  
 [Guide pratique : définir plusieurs versions d’une procédure](./how-to-define-multiple-versions-of-a-procedure.md)  
 [Guide pratique : surcharger une procédure qui accepte des paramètres optionnels](./how-to-overload-a-procedure-that-takes-optional-parameters.md)  
 [Guide pratique : surcharger une procédure qui accepte un nombre indéfini de paramètres](./how-to-overload-a-procedure-that-takes-an-indefinite-number-of-parameters.md)  
 [Considérations sur les surcharges de procédures](./considerations-in-overloading-procedures.md)  
 [Résolution de surcharge](./overload-resolution.md)  
 [Overloads](../../../../visual-basic/language-reference/modifiers/overloads.md)
