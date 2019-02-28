---
title: 'Procédure : Appeler une procédure surchargée (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], overloading
- procedures [Visual Basic], calling
- procedures [Visual Basic], multiple versions
- procedure calls [Visual Basic], overloaded
ms.assetid: 3bb331fb-f6bc-406f-9ca0-9609b497014c
ms.openlocfilehash: f13fdae9617fa2af21978979cad6f90a15140a4a
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56969997"
---
# <a name="how-to-call-an-overloaded-procedure-visual-basic"></a>Procédure : Appeler une procédure surchargée (Visual Basic)
L’avantage de la surcharge d’une procédure est la flexibilité de l’appel. Le code appelant peut obtenir les informations que nécessaires pour passer à la procédure, puis appelez un seul nom de procédure, quel que soit les arguments, il a réussi.  
  
### <a name="to-call-a-procedure-that-has-more-than-one-version-defined"></a>Pour appeler une procédure qui possède plusieurs versions définies  
  
1.  Dans le code appelant, déterminez les données à transmettre à la procédure.  
  
2.  Écrire l’appel de procédure de façon normale, présenter les données dans la liste d’arguments. N’oubliez pas les arguments correspondent à la liste des paramètres dans une des versions définies pour la procédure.  
  
3.  Il est inutile déterminer la version de la procédure à appeler. Visual Basic passe le contrôle à la version correspondant à votre liste d’arguments.  
  
     L’exemple suivant appelle la `post` procédure déclarée dans [Comment : Définir plusieurs Versions d’une procédure](./how-to-define-multiple-versions-of-a-procedure.md). Il obtient l’identification de client, détermine s’il est un `String` ou un `Integer`, puis, dans les deux cas, appelle la même procédure.  
  
     [!code-vb[VbVbcnProcedures#56](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#56)]  
  
     [!code-vb[VbVbcnProcedures#57](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#57)]  
  
## <a name="see-also"></a>Voir aussi
- [Procédures](./index.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Surcharge de procédure](./procedure-overloading.md)
- [Procédures de dépannage](./troubleshooting-procedures.md)
- [Guide pratique pour Définir plusieurs Versions d’une procédure](./how-to-define-multiple-versions-of-a-procedure.md)
- [Guide pratique pour Surcharger une procédure qui accepte des paramètres optionnels](./how-to-overload-a-procedure-that-takes-optional-parameters.md)
- [Guide pratique pour Surcharger une procédure qui accepte un nombre indéfini de paramètres](./how-to-overload-a-procedure-that-takes-an-indefinite-number-of-parameters.md)
- [Considérations sur les surcharges de procédures](./considerations-in-overloading-procedures.md)
- [Résolution de surcharge](./overload-resolution.md)
- [Overloads](../../../../visual-basic/language-reference/modifiers/overloads.md)
