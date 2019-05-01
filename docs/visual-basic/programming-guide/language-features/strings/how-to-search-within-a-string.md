---
title: 'Procédure : Recherche dans une chaîne (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], finding
- strings [Visual Basic], searching
- examples [Visual Basic], strings
ms.assetid: ae4c79e0-08ea-489f-bdb2-5eb6d355f284
ms.openlocfilehash: b690aa78a2cf07b0db5bdd28d7d71ed4a79fbf61
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62032082"
---
# <a name="how-to-search-within-a-string-visual-basic"></a>Procédure : Recherche dans une chaîne (Visual Basic)
Cet exemple appelle la <xref:System.String.IndexOf%2A> méthode sur un <xref:System.String> objet pour signaler l’index de la première occurrence d’une sous-chaîne.  
  
## <a name="example"></a>Exemple  
 [!code-vb[VbVbalrStrings#71](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#71)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
- Un `Imports` instruction spécifiant le <xref:System> espace de noms. Pour plus d’informations, consultez [Instruction Imports (espace de noms et type .NET)](../../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md).  
  
## <a name="robust-programming"></a>Programmation fiable  
 Le <xref:System.String.IndexOf%2A> méthode signale l’emplacement du premier caractère de la première occurrence de la sous-chaîne. L’index est basé sur 0, ce qui signifie que le premier caractère d’une chaîne a un index de 0.  
  
 Si <xref:System.String.IndexOf%2A> ne trouve pas la sous-chaîne, elle retourne -1.  
  
 Le <xref:System.String.IndexOf%2A> méthode respecte la casse et utilise la culture actuelle.  
  
 Pour un contrôle optimal des erreurs, vous souhaiterez peut-être placer la chaîne de recherche dans les `Try` de blocs à un [essayez... Catch... Instruction finally](../../../../visual-basic/language-reference/statements/try-catch-finally-statement.md) construction.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.String.IndexOf%2A>
- [Try...Catch...Finally (instruction)](../../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
- [Introduction aux chaînes en Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)
- [Chaînes](../../../../visual-basic/programming-guide/language-features/strings/index.md)
