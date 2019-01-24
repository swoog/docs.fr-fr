---
title: 'Procédure : Créer une chaîne à partir d’un tableau de valeurs Char (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- examples [Visual Basic], arrays
- examples [Visual Basic], Char data type
ms.assetid: 69f94e85-d57c-4ccc-a62a-426e829f5c5e
ms.openlocfilehash: a067474d6b32589a34b031d5c3ea4e5a4be55834
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54611460"
---
# <a name="how-to-create-a-string-from-an-array-of-char-values-visual-basic"></a>Procédure : Créer une chaîne à partir d’un tableau de valeurs Char (Visual Basic)
Cet exemple crée la chaîne « abcd » à partir de différents caractères.  
  
## <a name="example"></a>Exemple  
 [!code-vb[VbVbalrStrings#61](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-create-a-string-from-an-array-of-char-values_1.vb)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cette méthode n’a aucune exigence particulière.  
  
 La syntaxe `"a"c`, où un seul `c` suit un caractère unique entre guillemets, est utilisé pour créer un caractère littéral.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Les caractères null (équivalent à `Chr(0)`) dans la chaîne de produire des résultats inattendus lors de l’utilisation de la chaîne. Le caractère null sera inclus dans la chaîne, mais pas les caractères qui suivent le caractère null seront affichera dans certaines situations.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.String>
- [Char (type de données)](../../../../visual-basic/language-reference/data-types/char-data-type.md)
- [Types de données](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
