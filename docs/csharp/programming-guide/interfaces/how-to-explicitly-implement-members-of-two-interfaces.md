---
title: 'Comment : implémenter de manière explicite des membres de deux interfaces (Guide de programmation C#)'
ms.date: 07/20/2015
helpviewer_keywords:
- inheritance [C#], explicitly implementing interface members
- interfaces [C#], explicitly implementing with inheritance
ms.assetid: 8b402ddc-dff9-4869-89cb-d718c764e68e
ms.openlocfilehash: c73089fdbf1350c1aff68ac3e8e78be00e21b931
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33339038"
---
# <a name="how-to-explicitly-implement-members-of-two-interfaces-c-programming-guide"></a>Comment : implémenter de manière explicite des membres de deux interfaces (Guide de programmation C#)
L’implémentation explicite d’une [interface](../../../csharp/language-reference/keywords/interface.md) permet également au programmeur d’implémenter deux interfaces qui ont les mêmes noms de membres et donnent à chaque membre d’interface une implémentation distincte. L’exemple suivant affiche les dimensions d’une zone dans les unités de mesure à la fois métriques et britanniques. La [classe](../../../csharp/language-reference/keywords/class.md) Box implémente deux interfaces, IEnglishDimensions et IMetricDimensions, qui représentent les différents systèmes de mesure. Les deux interfaces ont des noms de membres identiques, Length et Width.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csProgGuideInheritance#9](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-explicitly-implement-members-of-two-interfaces_1.cs)]  
  
## <a name="robust-programming"></a>Programmation fiable  
 Si vous souhaitez utiliser par défaut les unités de mesure britanniques, implémentez les méthodes Length et Width normalement, puis implémentez explicitement les méthodes Length et Width à partir de l’interface IMetricDimensions :  
  
 [!code-csharp[csProgGuideInheritance#10](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-explicitly-implement-members-of-two-interfaces_2.cs)]  
  
 Dans ce cas, vous pouvez accéder aux unités de mesure britanniques à partir de l’instance de classe et accéder aux unités métriques à partir de l’instance d’interface :  
  
 [!code-csharp[csProgGuideInheritance#11](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-explicitly-implement-members-of-two-interfaces_3.cs)]  
  
## <a name="see-also"></a>Voir aussi  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Classes et structs](../../../csharp/programming-guide/classes-and-structs/index.md)  
 [Interfaces](../../../csharp/programming-guide/interfaces/index.md)  
 [Comment : implémenter de manière explicite des membres d’interface](../../../csharp/programming-guide/interfaces/how-to-explicitly-implement-interface-members.md)
