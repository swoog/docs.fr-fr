---
title: 'Comment : initialiser un dictionnaire avec un initialiseur de collection (Guide de programmation C#)'
ms.date: 07/20/2015
helpviewer_keywords:
- collection initializers [C#], with Dictionary
ms.assetid: 25283922-f8ee-40dc-a639-fac30804ec71
ms.openlocfilehash: b8c44ebbdc89d72398c3380d708b45d0b7dfdad3
ms.sourcegitcommit: 2d8b7488d94101b534ca3e9780b1c1e840233405
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/23/2018
ms.locfileid: "39198456"
---
# <a name="how-to-initialize-a-dictionary-with-a-collection-initializer-c-programming-guide"></a>Comment : initialiser un dictionnaire avec un initialiseur de collection (Guide de programmation C#)
Un <xref:System.Collections.Generic.Dictionary`2> contient une collection de paires clé/valeur. Sa méthode <xref:System.Collections.Generic.Dictionary`2.Add*> prend deux paramètres, un pour la clé et un pour la valeur. Pour initialiser un <xref:System.Collections.Generic.Dictionary`2> ou toute collection dont la méthode `Add` prend plusieurs paramètres, mettez chaque jeu de paramètres entre accolades, comme illustré dans l’exemple suivant.  
  
## <a name="example"></a>Exemple  
 Dans l’exemple de code suivant, un <xref:System.Collections.Generic.Dictionary`2> est initialisé avec des instances de type `StudentName`.  
  
 [!code-csharp[csProgGuideLINQ#34](../../../csharp/programming-guide/arrays/codesnippet/CSharp/how-to-initialize-a-dictionary-with-a-collection-initializer_1.cs)]  
  
 Notez les deux paires d’accolades dans chaque élément de la collection. Les accolades les plus intérieures encadrent l’initialiseur d’objet pour le `StudentName`, et les accolades les plus extérieures encadrent l’initialiseur pour la paire clé/valeur qui sera ajoutée à `students`<xref:System.Collections.Generic.Dictionary`2>. Pour finir, l’initialiseur de collection entier pour le dictionnaire est placé entre accolades.  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Pour exécuter ce code, copiez et collez la classe dans un projet d’application console Visual C# qui a été créé dans Visual Studio. Par défaut, ce projet cible la version 3.5 du [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)], et il a une référence à System.Core.dll et une directive using pour System.Linq. Si un ou plusieurs de ces éléments requis sont manquants dans le projet, vous pouvez les ajouter manuellement.  
  
## <a name="see-also"></a>Voir aussi  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Initialiseurs d’objets et de collections](../../../csharp/programming-guide/classes-and-structs/object-and-collection-initializers.md)
