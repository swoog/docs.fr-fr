---
title: 'Procédure : Forcer un Argument d’être passés par valeur (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], arguments
- procedures [Visual Basic], parameters
- procedure arguments
- Visual Basic code, procedures
- arguments [Visual Basic], ByVal
- arguments [Visual Basic], passing by value
- procedure parameters
- procedures [Visual Basic], calling
- arguments [Visual Basic], in parentheses
- procedure arguments [Visual Basic], in parentheses
- arguments [Visual Basic], changing value
ms.assetid: 77b4f2d2-1055-4c2f-a521-874d1db86946
ms.openlocfilehash: 497ae11b858b7d164ba3b5607ff2109254a154de
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58842042"
---
# <a name="how-to-force-an-argument-to-be-passed-by-value-visual-basic"></a>Procédure : Forcer un Argument d’être passés par valeur (Visual Basic)
La déclaration de procédure détermine le mécanisme de passage. Si un paramètre est déclaré [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md), Visual Basic s’attend à passer l’argument correspondant par référence. Ainsi, la procédure modifier la valeur de l’élément de programmation sous-jacent à l’argument dans le code appelant. Si vous souhaitez protéger l’élément sous-jacent contre une telle modification, vous pouvez remplacer le `ByRef` appeler de mécanisme de passage dans la procédure en plaçant le nom de l’argument entre parenthèses. Ces parenthèses sont ajoutent les parenthèses entourant la liste d’arguments de l’appel.  
  
 Le code appelant ne peut pas remplacer un [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md) mécanisme.  
  
### <a name="to-force-an-argument-to-be-passed-by-value"></a>Pour forcer un argument à passer par valeur  
  
-   Si le paramètre correspondant est déclaré `ByVal` dans la procédure, vous n’avez pas besoin de prendre des mesures supplémentaires. Visual Basic doit déjà passer l’argument par valeur.  
  
-   Si le paramètre correspondant est déclaré `ByRef` dans la procédure, mettez l’argument entre parenthèses dans l’appel de procédure.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant substitue un `ByRef` déclaration de paramètre. Dans l’appel qui force `ByVal`, notez les deux niveaux de parenthèses.  
  
 [!code-vb[VbVbcnProcedures#39](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#39)]  
  
 [!code-vb[VbVbcnProcedures#40](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#40)]  
  
 Lorsque `str` est placée entre parenthèses supplémentaires dans la liste d’arguments, le `setNewString` procédure ne peut pas modifier sa valeur dans le code appelant, et `MsgBox` affiche « Ne peut pas être remplacé si passé ByVal ». Lorsque `str` n’est pas placée entre parenthèses supplémentaires, la procédure peut le modifier, et `MsgBox` affiche « Il s’agit d’une nouvelle valeur pour l’argument inString. »  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Lorsque vous passez une variable par référence, vous devez utiliser le `ByRef` mot clé pour spécifier ce mécanisme.  
  
 La valeur par défaut en Visual Basic consiste à passer des arguments par valeur. Toutefois, il est conseillé en programmation pour inclure le [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md) ou [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md) keyword avec chaque paramètre déclaré. Cela rend votre code plus facile à lire.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Si une procédure déclare un paramètre [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md), l’exécution correcte du code peut dépendre de la possibilité de modifier l’élément sous-jacent dans le code appelant. Si le code appelant substitue ce mécanisme appelant en plaçant l’argument entre parenthèses, ou s’il passe un argument non modifiable, la procédure ne peut pas modifier l’élément sous-jacent. Cela peut produire des résultats inattendus dans le code appelant.  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Il y a toujours un risque de permettre à une procédure modifier la valeur sous-jacente à un argument dans le code appelant. Assurez-vous que cette valeur pour être modifié et être prêt à vérifier la validité avant de l’utiliser.  
  
## <a name="see-also"></a>Voir aussi

- [Procédures](./index.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Guide pratique pour Passer des Arguments à une procédure](./how-to-pass-arguments-to-a-procedure.md)
- [Passage d’un argument par valeur et par référence](./passing-arguments-by-value-and-by-reference.md)
- [Différences entre les arguments modifiables et non modifiables](./differences-between-modifiable-and-nonmodifiable-arguments.md)
- [Différences entre le passage d’un argument par valeur et par référence](./differences-between-passing-an-argument-by-value-and-by-reference.md)
- [Guide pratique pour Modifier la valeur d’un Argument de procédure](./how-to-change-the-value-of-a-procedure-argument.md)
- [Guide pratique pour Protéger un Argument de procédure contre les modifications de valeur](./how-to-protect-a-procedure-argument-against-value-changes.md)
- [Passage des arguments par position et par nom](./passing-arguments-by-position-and-by-name.md)
- [Value Types and Reference Types](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)
