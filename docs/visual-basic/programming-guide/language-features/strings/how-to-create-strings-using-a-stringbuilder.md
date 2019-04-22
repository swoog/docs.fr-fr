---
title: 'Procédure : Créer des chaînes à l’aide de StringBuilder en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- StringBuilder class
- strings [Visual Basic], using StringBuilder
ms.assetid: 9c042880-aa16-432e-9ccb-cd00abda9ae3
ms.openlocfilehash: 00fefcc138164288d872cd339f165dc6ffc0131a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58834190"
---
# <a name="how-to-create-strings-using-a-stringbuilder-in-visual-basic"></a>Procédure : Créer des chaînes à l’aide de StringBuilder en Visual Basic
Cet exemple construit une longue chaîne à partir de plusieurs chaînes plus petites à l’aide de la <xref:System.Text.StringBuilder> classe. Le <xref:System.Text.StringBuilder> classe est plus efficace que le `&=` opérateur pour concaténer plusieurs chaînes.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée une instance de la <xref:System.Text.StringBuilder> classe, ajoute 1 000 chaînes à cette instance, puis retourne sa représentation sous forme de chaîne.  
  
 [!code-vb[VbVbalrStrings#70](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#70)]  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation de la classe StringBuilder](../../../../standard/base-types/stringbuilder.md)
- [&= (opérateur)](../../../../visual-basic/language-reference/operators/and-assignment-operator.md)
- [Chaînes](../../../../visual-basic/programming-guide/language-features/strings/index.md)
- [Création de chaînes](../../../../standard/base-types/creating-new.md)
- [Manipulation de chaînes](../../../../standard/base-types/manipulating-strings.md)
