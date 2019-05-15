---
title: Me, My, MyBase et MyClass dans Visual Basic
ms.date: 07/20/2015
f1_keywords:
- MyClass
- vb.Me
- MyBase
- vb.MyBase
- Me
- vb.MyClass
- vb.This
- vb.My
helpviewer_keywords:
- My object
- self-reference [Visual Basic], Me keyword
- MyClass keyword [Visual Basic], relationship to similar programming elements
- Me keyword [Visual Basic], relationship to similar programming elements
- Me keyword [Visual Basic], referring to the current instance of an object
- Me keyword [Visual Basic]
- self-reference
- current instance [Visual Basic], Me keyword
- MyBase keyword [Visual Basic], relationship to similar programming elements
ms.assetid: f8e241ae-b1ed-4886-9aa0-08c632154029
ms.openlocfilehash: 3eca756429c5fec8f324a17350844b59baf9ccf7
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65586251"
---
# <a name="me-my-mybase-and-myclass-in-visual-basic"></a>Me, My, MyBase et MyClass dans Visual Basic
`Me`, `My`, `MyBase`, et `MyClass` en Visual Basic ont des noms similaires, mais à des fins différentes. Cette rubrique décrit chacune de ces entités afin de les distinguer.  
  
## <a name="me"></a>Me  
 Le `Me` mot clé permet de faire référence à l’instance spécifique d’une classe ou structure dans laquelle le code est en cours d’exécution. `Me` se comporte comme une variable objet ou une variable de structure faisant référence à l’instance actuelle. À l’aide de `Me` est particulièrement utile pour transmettre des informations sur l’instance en cours d’exécution d’une classe ou une structure à une procédure dans une autre classe, structure ou module.  
  
 Par exemple, supposons que vous avez la procédure suivante dans un module.  
  
```  
Sub ChangeFormColor(FormName As Form)  
   Randomize()  
   FormName.BackColor = Color.FromArgb(Rnd() * 256, Rnd() * 256, Rnd() * 256)  
End Sub  
```  
  
 Vous pouvez appeler cette procédure et passer l’instance actuelle de la <xref:System.Windows.Forms.Form> classe en tant qu’argument à l’aide de l’instruction suivante.  
  
```  
ChangeFormColor(Me)  
```  
  
## <a name="my"></a>My  
 Le `My` fonctionnalité offre un accès facile et intuitif à un nombre de classes .NET Framework, l’activation de l’utilisateur de Visual Basic interagir avec l’ordinateur, application, paramètres, ressources et ainsi de suite.  
  
## <a name="mybase"></a>MyBase  
 Le `MyBase` mot clé se comporte comme une variable objet faisant référence à la classe de base de l’instance actuelle d’une classe. `MyBase` est couramment utilisé pour accéder aux membres de classe de base qui sont substitués ou occultés dans une classe dérivée. `MyBase.New` est utilisé pour appeler explicitement un constructeur de classe de base à partir d’un constructeur de classe dérivée.  
  
## <a name="myclass"></a>MyClass  
 Le `MyClass` mot clé se comporte comme une variable objet faisant référence à l’instance actuelle d’une classe implémentée à l’origine. `MyClass` est similaire à `Me`, mais tous les appels de méthode sur celui-ci sont traités comme si la méthode était `NotOverridable`.  
  
## <a name="see-also"></a>Voir aussi

- [Éléments fondamentaux de l’héritage](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
