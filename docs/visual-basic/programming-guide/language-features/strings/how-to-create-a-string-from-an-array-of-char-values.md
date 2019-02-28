---
title: 'Procédure : Créer une chaîne à partir d’un tableau de valeurs Char (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- examples [Visual Basic], arrays
- examples [Visual Basic], Char data type
ms.assetid: 69f94e85-d57c-4ccc-a62a-426e829f5c5e
ms.openlocfilehash: 0d3a4caf0967ab77de7d91470e43e52521dbd2da
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56975509"
---
# <a name="how-to-create-a-string-from-an-array-of-char-values-visual-basic"></a>Procédure : Créer une chaîne à partir d’un tableau de valeurs Char (Visual Basic)
Cet exemple crée la chaîne « abcd » à partir de différents caractères.  
  
## <a name="example"></a>Exemple  
 [!code-vb[VbVbalrStrings#61](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#61)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cette méthode n’a aucune exigence particulière.  
  
 La syntaxe `"a"c`, où un seul `c` suit un caractère unique entre guillemets, est utilisé pour créer un caractère littéral.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Les caractères null (équivalent à `Chr(0)`) dans la chaîne de produire des résultats inattendus lors de l’utilisation de la chaîne. Le caractère null sera inclus dans la chaîne, mais pas les caractères qui suivent le caractère null seront affichera dans certaines situations.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.String>
- [Char (type de données)](../../../../visual-basic/language-reference/data-types/char-data-type.md)
- [Types de données](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
