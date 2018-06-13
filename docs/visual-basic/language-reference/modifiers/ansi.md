---
title: Ansi (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Ansi
helpviewer_keywords:
- Declare statement [Visual Basic], marshaling strings [Visual Basic]
- ANSI, Visual Basic
- ANSI
ms.assetid: 4f1fa6ff-5557-41ab-b6da-90baf4c15917
ms.openlocfilehash: c7037acac58de56a396bd89f595ef897743ff4e9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33595077"
---
# <a name="ansi-visual-basic"></a>Ansi (Visual Basic)
Spécifie que Visual Basic doit marshaler toutes les chaînes en valeurs American National Standards Institute (ANSI), quelle que soit le nom de la procédure externe déclarée.  
  
 Lorsque vous appelez une procédure définie en dehors de votre projet, le compilateur Visual Basic n’a pas accès aux informations nécessaires appeler la procédure correctement. Ces informations comprennent où se trouve la procédure, comment il est identifié, sa séquence d’appel et de type de retour, et chaîne de jeu de caractères qu’il utilise. Le [instruction Declare](../../../visual-basic/language-reference/statements/declare-statement.md) crée une référence à une procédure externe et fournit ces informations nécessaires.  
  
 Le `charsetmodifier` dans le cadre de la `Declare` instruction fournit les informations de jeu de caractères pour marshaler des chaînes lors d’un appel à la procédure externe. Elle affecte également la façon dont Visual Basic recherche le fichier externe pour le nom de la procédure externe. Le `Ansi` modificateur Spécifie que Visual Basic doit marshaler toutes les chaînes en valeurs ANSI et doit rechercher la procédure sans modifier son nom lors de la recherche.  
  
 Si aucun modificateur de jeu de caractères n’est spécifiée, `Ansi` est la valeur par défaut.  
  
## <a name="remarks"></a>Notes  
 Le `Ansi` modificateur peut être utilisé dans ce contexte :  
  
 [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
## <a name="smart-device-developer-notes"></a>Remarques sur le développement Smart Device  
 Ce mot clé n’est pas pris en charge.  
  
## <a name="see-also"></a>Voir aussi  
 [Auto](../../../visual-basic/language-reference/modifiers/auto.md)  
 [Unicode](../../../visual-basic/language-reference/modifiers/unicode.md)  
 [Mots clés](../../../visual-basic/language-reference/keywords/index.md)
