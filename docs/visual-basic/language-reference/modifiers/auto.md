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
ms.openlocfilehash: e4beb320b3aa0cadb790dd3ab92255496bc32f05
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58843836"
---
# <a name="auto-visual-basic"></a>Auto (Visual Basic)
Spécifie que Visual Basic doit marshaler les chaînes selon les règles de .NET Framework en fonction du nom externe de la procédure externe déclarée.  
  
 Lorsque vous appelez une procédure définie en dehors de votre projet, le compilateur Visual Basic n’a pas accès aux informations qu’il doit avoir appeler la procédure correctement. Ces informations incluent où se trouve la procédure, comment il est identifié, sa séquence d’appel et de type de retour, et chaîne de jeu de caractères qu’il utilise. Le [instruction Declare](../../../visual-basic/language-reference/statements/declare-statement.md) crée une référence à une procédure externe et fournit ces informations nécessaires.  
  
 Le `charsetmodifier` dans le `Declare` instruction fournit les informations de jeu de caractères pour marshaler des chaînes lors d’un appel à la procédure externe. Elle affecte également la façon dont Visual Basic recherche le fichier externe pour le nom de la procédure externe. Le `Auto` modificateur Spécifie que Visual Basic doit marshaler les chaînes selon les règles de .NET Framework et qu’elle doit déterminer le caractère de base défini de la plateforme d’exécution et, éventuellement, modifiez le nom de procédure externe si initial de recherche échoue. Pour plus d’informations, consultez « Jeux de caractères » dans [instruction Declare](../../../visual-basic/language-reference/statements/declare-statement.md).  
  
 Si aucun modificateur de jeu de caractères est spécifié, `Ansi` est la valeur par défaut.  
  
## <a name="remarks"></a>Notes  
 Le `Auto` modificateur peut être utilisé dans ce contexte :  
  
 [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
## <a name="smart-device-developer-notes"></a>Remarques sur le développement Smart Device  
 Ce mot clé n’est pas pris en charge.  
  
## <a name="see-also"></a>Voir aussi

- [Ansi](../../../visual-basic/language-reference/modifiers/ansi.md)
- [Unicode](../../../visual-basic/language-reference/modifiers/unicode.md)
- [Mots clés](../../../visual-basic/language-reference/keywords/index.md)
