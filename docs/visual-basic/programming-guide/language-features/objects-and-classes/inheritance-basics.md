---
title: Éléments fondamentaux de l'héritage (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- derived classes [Visual Basic], inheritance
- MyClass keyword [Visual Basic], using
- MyBase keyword [Visual Basic], using
- Inherits statement [Visual Basic], inheritance
- overriding, Overridable keyword
- MustInherit keyword [Visual Basic], using
- Overrides keyword [Visual Basic], using
- inheritance
- MustInherit classes [Visual Basic]
- MustOverride keyword [Visual Basic], using
- classes [Visual Basic], derived
- NotInheritable keyword [Visual Basic], using
- base classes [Visual Basic], extending properties and methods [Visual Basic]
- NotOverridable keyword [Visual Basic], using
- base classes [Visual Basic], inheritance
- abstract classes [Visual Basic], inheritance
- overriding, Overrides keyword
ms.assetid: dfc8deba-f5b3-4d1d-a937-7cb826446fc5
ms.openlocfilehash: 5e4b8511145e758bf3d6328141be0e526965dccf
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61758468"
---
# <a name="inheritance-basics-visual-basic"></a>Éléments fondamentaux de l'héritage (Visual Basic)
Le `Inherits` instruction est utilisée pour déclarer une nouvelle classe, appelée un *classe dérivée*, basé sur une classe existante, appelée un *classe de base*. Les classes dérivées héritent et peuvent étendre les propriétés, les méthodes, les événements, les champs et les constantes définies dans la classe de base. La section suivante décrit certaines des règles pour l’héritage et les modificateurs que vous pouvez utiliser pour modifier les façon dont les classes héritent ou sont héritées :  
  
- Par défaut, toutes les classes sont héritées, sauf si marqué avec le `NotInheritable` mot clé. Les classes peuvent hériter d’autres classes dans votre projet ou à partir de classes dans d’autres assemblys qui fait référence à votre projet.  
  
- Contrairement aux langages qui permettent l’héritage multiple, Visual Basic ne permet qu’un seul héritage dans les classes ; Autrement dit, les classes dérivées peuvent avoir qu’une seule classe de base. Bien que l’héritage multiple n’est pas autorisée dans les classes, les classes peuvent implémenter plusieurs interfaces, qui peuvent accomplir efficacement les mêmes objectifs.  
  
- Pour empêcher l’exposition des éléments restreints dans une classe de base, le type d’accès d’une classe dérivée doit être égal à ou plus restrictif que sa classe de base. Par exemple, un `Public` classe ne peut pas hériter une `Friend` ou un `Private` (classe) et un `Friend` classe ne peut pas hériter une `Private` classe.  
  
## <a name="inheritance-modifiers"></a>Modificateurs d’héritage  
 Visual Basic présente les modificateurs pour prendre en charge l’héritage ni les instructions de niveau classe suivantes :  
  
- `Inherits` instruction : Spécifie la classe de base.  
  
- `NotInheritable` modificateur : empêche les programmeurs d’utilisation de la classe comme classe de base.  
  
- `MustInherit` modificateur — Spécifie que la classe est destinée à utiliser comme une classe de base. Instances de `MustInherit` classes ne peuvent pas être créées directement ; elles peuvent uniquement être créées comme base des instances de classe d’une classe dérivée. (Autres langages de programmation, tels que C++ et C#, utilisent le terme *classe abstraite* pour décrire une telle classe.)  
  
## <a name="overriding-properties-and-methods-in-derived-classes"></a>Substitution de propriétés et méthodes dans les Classes dérivées  
 Par défaut, une classe dérivée hérite des propriétés et méthodes à partir de sa classe de base. Si une propriété héritée ou une méthode doit se comporter différemment dans la classe dérivée, il peut être *substitution*. Autrement dit, vous pouvez définir une nouvelle implémentation de la méthode dans la classe dérivée. Les modificateurs suivants sont utilisés pour contrôler la façon dont les propriétés et les méthodes sont substituées :  
  
- `Overridable` : Permet à une propriété ou méthode dans une classe de substitution dans une classe dérivée.  
  
- `Overrides` : Substitue un `Overridable` propriété ou méthode définie dans la classe de base.  
  
- `NotOverridable` — Empêche une propriété ou méthode en cours de substitution dans une classe qui hérite. Par défaut, `Public` sont des méthodes `NotOverridable`.  
  
- `MustOverride` — Nécessite qu’une classe dérivée substituer la propriété ou méthode. Lorsque le `MustOverride` mot clé est utilisé, la définition de méthode se compose uniquement le `Sub`, `Function`, ou `Property` instruction. Aucune autre instruction n’est autorisées et, en particulier aucune `End Sub` ou `End Function` instruction. `MustOverride` les méthodes doivent être déclarées dans `MustInherit` classes.  
  
 Supposons que vous souhaitez définir des classes pour gérer les salaires. Vous pouvez définir un générique `Payroll` classe qui contient un `RunPayroll` méthode qui calcule les salaires pour une semaine type. Vous pouvez ensuite utiliser `Payroll` comme classe de base pour une plus spécialisées `BonusPayroll` (classe), qui pouvait être utilisée lors de la distribution de primes aux employés.  
  
 Le `BonusPayroll` classe peut hériter et remplacer, le `PayEmployee` méthode définie dans la base de `Payroll` classe.  
  
 L’exemple suivant définit une classe de base, `Payroll,` et une classe dérivée, `BonusPayroll`, qui substitue une méthode héritée, `PayEmployee`. Une procédure, `RunPayroll`, crée et passe ensuite un `Payroll` objet et un `BonusPayroll` objet à une fonction, `Pay`, qui exécute le `PayEmployee` méthode des deux objets.  
  
 [!code-vb[VbVbalrOOP#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#28)]  
  
## <a name="the-mybase-keyword"></a>Le mot clé MyBase  
 Le `MyBase` mot clé se comporte comme une variable objet qui fait référence à la classe de base de l’instance actuelle d’une classe. `MyBase` est fréquemment utilisé pour accéder aux membres de classe de base qui sont substitués ou occultés dans une classe dérivée. En particulier, `MyBase.New` est utilisé pour appeler explicitement un constructeur de classe de base à partir d’un constructeur de classe dérivée.  
  
 Par exemple, supposons que vous concevez une classe dérivée qui substitue une méthode héritée de la classe de base. La méthode substituée peut appeler la méthode dans la classe de base et modifiez la valeur de retour comme indiqué dans le fragment de code suivant :  
  
 [!code-vb[VbVbalrOOP#109](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#109)]  
  
 La liste suivante décrit les restrictions sur l’utilisation de `MyBase`:  
  
- `MyBase` fait référence à la classe de base immédiate et à ses membres hérités. Il ne peut pas être utilisé pour accéder à `Private` membres dans la classe.  
  
- `MyBase` est un mot clé, pas un objet réel. `MyBase` ne peut pas être assigné à une variable, passés à des procédures ou utilisé dans un `Is` comparaison.  
  
- La méthode qui `MyBase` qualifie ne doit pas être définie dans la classe de base immédiate ; il peut être définie à la place dans une classe de base héritée indirectement. Dans l’ordre pour une référence qualifiée par `MyBase` pour compiler correctement, une classe de base doit contenir une méthode qui correspond au nom et les types de paramètres qui apparaissent dans l’appel.  
  
- Vous ne pouvez pas utiliser `MyBase` pour appeler `MustOverride` méthodes de la classe de base.  
  
- `MyBase` ne peut pas être utilisé pour se qualifier lui-même. Par conséquent, le code suivant n’est pas valide :  
  
     `MyBase.MyBase.BtnOK_Click()`  
  
- `MyBase` ne peut pas être utilisé dans des modules.  
  
- `MyBase` ne peut pas être utilisé pour accéder aux membres de classe de base qui sont marqués comme `Friend` si la classe de base se trouve dans un autre assembly.  
  
 Pour plus d’informations et un autre exemple, consultez [Comment : Accéder à une Variable masquée par une classe dérivée](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-access-a-variable-hidden-by-a-derived-class.md).  
  
## <a name="the-myclass-keyword"></a>Le mot clé MyClass  
 Le `MyClass` mot clé se comporte comme une variable objet qui fait référence à l’instance actuelle d’une classe implémentée à l’origine. `MyClass` ressemble à `Me`, mais chaque méthode et propriété appeler sur `MyClass` est traitée comme si la méthode ou propriété ont été [NotOverridable](../../../../visual-basic/language-reference/modifiers/notoverridable.md). Par conséquent, la méthode ou propriété n’est pas affectée par la substitution dans une classe dérivée.  
  
- `MyClass` est un mot clé, pas un objet réel. `MyClass` ne peut pas être assigné à une variable, passés à des procédures ou utilisé dans un `Is` comparaison.  
  
- `MyClass` fait référence à la classe conteneur et ses membres hérités.  
  
- `MyClass` peut être utilisé comme qualificateur pour `Shared` membres.  
  
- `MyClass` ne peut pas être utilisé à l’intérieur d’un `Shared` (méthode), mais peut être utilisé pour accéder à un membre partagé d’une classe à l’intérieur d’une méthode d’instance.  
  
- `MyClass` ne peut pas être utilisé dans des modules standard.  
  
- `MyClass` peut être utilisé pour qualifier une méthode qui est définie dans une classe de base et ne possède aucune implémentation de la méthode fournie dans cette classe. Une telle référence a la même signification que `MyBase.` *méthode*.  
  
 L’exemple suivant compare `Me` et `MyClass`.  
  
```vb
Class baseClass  
    Public Overridable Sub testMethod()  
        MsgBox("Base class string")  
    End Sub  
    Public Sub useMe()  
        ' The following call uses the calling class's method, even if   
        ' that method is an override.  
        Me.testMethod()  
    End Sub  
    Public Sub useMyClass()  
        ' The following call uses this instance's method and not any  
        ' override.  
        MyClass.testMethod()  
    End Sub  
End Class  
Class derivedClass : Inherits baseClass  
    Public Overrides Sub testMethod()  
        MsgBox("Derived class string")  
    End Sub  
End Class  
Class testClasses  
    Sub startHere()  
        Dim testObj As derivedClass = New derivedClass()  
        ' The following call displays "Derived class string".  
        testObj.useMe()  
        ' The following call displays "Base class string".  
        testObj.useMyClass()  
    End Sub  
End Class  
```  
  
 Même si `derivedClass` substitue `testMethod`, le `MyClass` mot clé dans `useMyClass` annule les effets de substitution et le compilateur résout l’appel à la version de la classe de base de `testMethod`.  
  
## <a name="see-also"></a>Voir aussi

- [Inherits (instruction)](../../../../visual-basic/language-reference/statements/inherits-statement.md)
- [Me, My, MyBase et MyClass](../../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
