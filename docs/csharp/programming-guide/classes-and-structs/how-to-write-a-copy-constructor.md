---
title: 'Comment : écrire un constructeur de copie (Guide de programmation C#)'
ms.date: 07/20/2015
helpviewer_keywords:
- C# Language, copy constructor
- copy constructor [C#]
ms.assetid: fba899b5-fc41-428e-a745-3ebdbf37990a
ms.openlocfilehash: d6ecfc3659dcf533db0f4e7b67fdffd620a584fd
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44271609"
---
# <a name="how-to-write-a-copy-constructor-c-programming-guide"></a>Comment : écrire un constructeur de copie (Guide de programmation C#)
C# ne fournit pas de constructeur de copie pour les objets, mais vous pouvez en écrire un vous-même.  
  
## <a name="example"></a>Exemple  
 Dans l’exemple suivant, la `Person`[classe](../../../csharp/language-reference/keywords/class.md) définit un constructeur de copie qui prend comme argument une instance de `Person`. Les valeurs des propriétés de l’argument sont assignées aux propriétés de la nouvelle instance de `Person`. Le code contient un autre constructeur de copie qui envoie les propriétés `Name` et `Age` de l’instance que vous voulez copier au constructeur d’instance de la classe.  
  
 [!code-csharp[csProgGuideObjects#16](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-write-a-copy-constructor_1.cs)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ICloneable>  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Classes et structs](../../../csharp/programming-guide/classes-and-structs/index.md)  
- [Constructeurs](../../../csharp/programming-guide/classes-and-structs/constructors.md)  
- [Finaliseurs](../../../csharp/programming-guide/classes-and-structs/destructors.md)
