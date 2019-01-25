---
title: 'Procédure : Déterminer le Type désigné par une Variable d’objet (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- TypeOf operator [Visual Basic], determining object variable type
- variables [Visual Basic], object
- object variables [Visual Basic], determining type
ms.assetid: 6f6a138d-58a4-40d1-9f4e-0a3c598eaf81
ms.openlocfilehash: 149af116f2b848082367b33d826bace8345cee05
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54571176"
---
# <a name="how-to-determine-what-type-an-object-variable-refers-to-visual-basic"></a>Procédure : Déterminer le Type désigné par une Variable d’objet (Visual Basic)
Une variable objet contient un pointeur vers les données stockées ailleurs. Le type de ces données peut changer pendant l’exécution. À tout moment, vous pouvez utiliser la <xref:System.Type.GetTypeCode%2A> méthode pour déterminer le type d’exécution actuel, ou le [TypeOf, opérateur](../../../../visual-basic/language-reference/operators/typeof-operator.md) pour déterminer si l’actuel type au moment de l’exécution est compatible avec un type spécifié.  
  
### <a name="to-determine-the-exact-type-an-object-variable-currently-refers-to"></a>Pour déterminer que le type exact auquel une variable objet actuellement fait référence à  
  
1.  Sur la variable objet, appelez le <xref:System.Object.GetType%2A> méthode pour récupérer un <xref:System.Type?displayProperty=nameWithType> objet.  
  
    ```  
    Dim myObject As Object  
    myObject.GetType()  
    ```  
  
2.  Sur le <xref:System.Type?displayProperty=nameWithType> de classe, appelez la méthode partagée <xref:System.Type.GetTypeCode%2A> pour récupérer le <xref:System.TypeCode> valeur d’énumération pour le type d’objet.  
  
    ```  
    Dim myObject As Object  
    Dim datTyp As Integer = Type.GetTypeCode(myObject.GetType())  
    MsgBox("myObject currently has type code " & CStr(datTyp))  
    ```  
  
     Vous pouvez tester le <xref:System.TypeCode> valeur d’énumération par rapport à tout membre d’énumération est dignes d’intérêt, telles que `Double`.  
  
### <a name="to-determine-whether-an-object-variables-type-is-compatible-with-a-specified-type"></a>Pour déterminer si un objet type de variable est compatible avec un type spécifié  
  
-   Utilisez le `TypeOf` opérateur en association avec le [opérateur Is](../../../../visual-basic/language-reference/operators/is-operator.md) pour tester l’objet avec un `TypeOf`... `Is` expression.  
  
    ```  
    If TypeOf objA Is System.Windows.Forms.Control Then  
        MsgBox("objA is compatible with the Control class")  
    End If  
    ```  
  
     Le `TypeOf`... `Is` expression retourne `True` si l’objet de l’exécution type est compatible avec le type spécifié.  
  
     Le critère de compatibilité varie selon que le type spécifié est une classe, une structure ou une interface. En règle générale, les types sont compatibles si l’objet est du même type que, hérite ou implémente le type spécifié. Pour plus d’informations, consultez [TypeOf, opérateur](../../../../visual-basic/language-reference/operators/typeof-operator.md).  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Notez que le type spécifié ne peut pas être une variable ou une expression. Il doit être le nom d’un type défini, comme une classe, une structure ou une interface. Cela inclut les types intrinsèques tels que `Integer` et `String`.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Object.GetType%2A>
- <xref:System.Type?displayProperty=nameWithType>
- <xref:System.Type.GetTypeCode%2A>
- <xref:System.TypeCode>
- [Variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
- [Valeurs des variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variable-values.md)
- [Object (type de données)](../../../../visual-basic/language-reference/data-types/object-data-type.md)
