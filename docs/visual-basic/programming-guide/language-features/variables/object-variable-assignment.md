---
title: Assignation des variables objets (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Nothing keyword [Visual Basic], object variable assignment
- object variables [Visual Basic], initializing
- variables [Visual Basic], initializing
- objects [Visual Basic], current instance
- object variables [Visual Basic], assigning
- variables [Visual Basic], object variables
- current instance [Visual Basic], defined
- variables [Visual Basic], assigning
- assignment statements [Visual Basic], object variable assignment
- Me keyword [Visual Basic], as object variable
ms.assetid: 3706811d-fd40-44fe-8727-d692e8e55d6d
ms.openlocfilehash: 571b09a0783ec0dfd09970b000faec39dca682b3
ms.sourcegitcommit: 4621e67f69e7a9503ea93313ff60d69683207889
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2018
ms.locfileid: "49995361"
---
# <a name="object-variable-assignment-visual-basic"></a>Assignation des variables objets (Visual Basic)
Vous utilisez une instruction d’assignation normale pour assigner un objet à une variable objet. Vous pouvez affecter une expression d’objet ou le [rien](../../../../visual-basic/language-reference/nothing.md) mot clé, comme dans l’exemple suivant illustre.  
  
```  
Dim thisObject As Object  
' The following statement assigns an object reference.  
thisObject = Form1  
' The following statement discontinues association with any object.  
thisObject = Nothing  
```  
  
 `Nothing` signifie qu’il n’existe aucun objet actuellement affecté à la variable.  
  
## <a name="initialization"></a>Initialisation  
 Lorsque votre code commence à exécuter, vos variables objet sont initialisées à `Nothing`. Ceux dont les déclarations incluent l’initialisation sont réinitialisés aux valeurs que vous spécifiez quand les instructions de déclaration sont exécutées.  
  
 Vous pouvez inclure l’initialisation dans votre déclaration à l’aide de la [New](../../../../visual-basic/language-reference/operators/new-operator.md) mot clé. Les instructions de déclaration suivantes déclarent des variables objets `testUri` et `ver` et leur attribuer des objets spécifiques. Chacun utilise un des constructeurs surchargés de la classe appropriée pour initialiser l’objet.  
  
```  
Dim testUri As New System.Uri("https://www.microsoft.com")  
Dim ver As New System.Version(6, 1, 0)  
```  
  
## <a name="disassociation"></a>Dissociation  
 Affectation à une variable objet `Nothing` interrompt l’association de la variable et un objet spécifique. Cela vous empêche de modifier accidentellement l’objet en modifiant la variable. Il vous permet également de tester si la variable objet pointe vers un objet valide, comme le montre l’exemple suivant.  
  
```  
If otherObject IsNot Nothing Then  
    ' otherObject refers to a valid object, so your code can use it.  
End If  
```  
  
 Si l’objet désigné par votre variable est dans une autre application, ce test ne peut pas déterminer si cette application a terminé ou invalider l’objet.  
  
 Une variable objet avec la valeur `Nothing` est également appelé un *référence null*.  
  
## <a name="current-instance"></a>Instance actuelle  
 Le *instance actuelle* d’un objet est celui dans lequel le code est en cours d’exécution. Dans la mesure où tout le code s’exécute à l’intérieur d’une procédure, l’instance actuelle est celui dans lequel la procédure a été appelée.  
  
 Le `Me` mot clé agit comme une variable objet faisant référence à l’instance actuelle. Si une procédure n’est pas [partagé](../../../../visual-basic/language-reference/modifiers/shared.md), il peut utiliser le `Me` mot clé pour obtenir un pointeur vers l’instance actuelle. Les procédures partagées ne peut pas être associés à une instance spécifique d’une classe.  
  
 À l’aide de `Me` est particulièrement utile pour passer l’instance actuelle à une procédure dans un autre module. Par exemple, supposons que vous avez un nombre de documents XML et que vous souhaitez ajouter un texte standard à toutes les. L’exemple suivant définit une procédure pour ce faire.  
  
```  
Sub addStandardText(XmlDoc As System.Xml.XmlDocument)  
    XmlDoc.CreateTextNode("This text goes into every XML document.")  
End Sub  
```  
  
 Chaque objet de document XML peut ensuite appeler la procédure et passer son instance actuelle en tant qu’argument. Cela est illustré par l'exemple suivant.  
  
```  
addStandardText(Me)  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)  
 [Déclaration des variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variable-declaration.md)  
 [Valeurs des variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variable-values.md)  
 [Comment : déclarer une Variable objet et lui assigner un objet en Visual Basic](../../../../visual-basic/programming-guide/language-features/variables/how-to-declare-an-object-variable-and-assign-an-object-to-it.md)  
 [Guide pratique : faire en sorte qu'une variable objet ne fasse pas référence à une instance](../../../../visual-basic/programming-guide/language-features/variables/how-to-make-an-object-variable-not-refer-to-any-instance.md)  
 [Me, My, MyBase et MyClass](../../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
