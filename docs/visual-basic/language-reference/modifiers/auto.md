---
title: Auto (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Auto
helpviewer_keywords:
- Auto keyword [Visual Basic], external references
- Declare statement [Visual Basic], marshaling strings
- Auto keyword [Visual Basic]
- Auto keyword [Visual Basic], marshaling strings
ms.assetid: bf79ba95-a62c-48a5-916f-0ac7a52c13ec
ms.openlocfilehash: 414998b4bef526060e7ba4f584fa071fbd0acaa5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="auto-visual-basic"></a>Auto (Visual Basic)
Spécifie que Visual Basic doit marshaler les chaînes selon les règles de .NET Framework basées sur le nom externe de la procédure externe déclarée.  
  
 Lorsque vous appelez une procédure définie en dehors de votre projet, le compilateur Visual Basic n’a pas accès aux informations nécessaires pour appeler la procédure correctement. Ces informations comprennent où se trouve la procédure, comment il est identifié, sa séquence d’appel et de type de retour, et chaîne de jeu de caractères qu’il utilise. Le [instruction Declare](../../../visual-basic/language-reference/statements/declare-statement.md) crée une référence à une procédure externe et fournit ces informations nécessaires.  
  
 Le `charsetmodifier` dans le cadre de la `Declare` instruction fournit les informations de jeu de caractères pour marshaler des chaînes lors d’un appel à la procédure externe. Elle affecte également la façon dont Visual Basic recherche le fichier externe pour le nom de la procédure externe. Le `Auto` modificateur Spécifie que Visual Basic doit marshaler les chaînes selon les règles du .NET Framework et qu’il doit déterminer la base jeu de caractères de la plateforme d’exécution et éventuellement modifier le nom de la procédure externe si initial de recherche échoue. Pour plus d’informations, consultez « Jeux de caractères » dans [instruction Declare](../../../visual-basic/language-reference/statements/declare-statement.md).  
  
 Si aucun modificateur de jeu de caractères n’est spécifiée, `Ansi` est la valeur par défaut.  
  
## <a name="remarks"></a>Notes  
 Le `Auto` modificateur peut être utilisé dans ce contexte :  
  
 [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
## <a name="smart-device-developer-notes"></a>Remarques sur le développement Smart Device  
 Ce mot clé n’est pas pris en charge.  
  
## <a name="see-also"></a>Voir aussi  
 [Ansi](../../../visual-basic/language-reference/modifiers/ansi.md)  
 [Unicode](../../../visual-basic/language-reference/modifiers/unicode.md)  
 [Mots clés](../../../visual-basic/language-reference/keywords/index.md)
