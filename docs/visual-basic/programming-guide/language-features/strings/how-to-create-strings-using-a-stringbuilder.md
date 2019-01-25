---
title: 'Procédure : Créer des chaînes à l’aide de StringBuilder en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- StringBuilder class
- strings [Visual Basic], using StringBuilder
ms.assetid: 9c042880-aa16-432e-9ccb-cd00abda9ae3
ms.openlocfilehash: 84f0f41cf8ee23466d47dae3b1068c3bc5334072
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54528444"
---
# <a name="how-to-create-strings-using-a-stringbuilder-in-visual-basic"></a>Procédure : Créer des chaînes à l’aide de StringBuilder en Visual Basic
Cet exemple construit une longue chaîne à partir de plusieurs chaînes plus petites à l’aide de la <xref:System.Text.StringBuilder> classe. Le <xref:System.Text.StringBuilder> classe est plus efficace que le `&=` opérateur pour concaténer plusieurs chaînes.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée une instance de la <xref:System.Text.StringBuilder> classe, ajoute 1 000 chaînes à cette instance, puis retourne sa représentation sous forme de chaîne.  
  
 [!code-vb[VbVbalrStrings#70](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-create-strings-using-a-stringbuilder_1.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Utilisation de la classe StringBuilder](../../../../standard/base-types/stringbuilder.md)
- [&= (opérateur)](../../../../visual-basic/language-reference/operators/and-assignment-operator.md)
- [Chaînes](../../../../visual-basic/programming-guide/language-features/strings/index.md)
- [Création de chaînes](../../../../standard/base-types/creating-new.md)
- [Manipulation de chaînes](../../../../standard/base-types/manipulating-strings.md)
- [Exemples de chaînes](https://msdn.microsoft.com/library/be9e82a3-dc95-4aaa-9396-61b66e467e02(v=vs.100))
