---
title: 'Procédure : Écrire un constructeur de copie - Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- C# Language, copy constructor
- copy constructor [C#]
ms.assetid: fba899b5-fc41-428e-a745-3ebdbf37990a
ms.openlocfilehash: daf0683060d7df5dc5e644b4b84aac3dcdea939f
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53240682"
---
# <a name="how-to-write-a-copy-constructor-c-programming-guide"></a>Procédure : Écrire un constructeur de copie (Guide de programmation C#)
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
