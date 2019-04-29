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
# <a name="inheritance-basics-visual-basic"></a><span data-ttu-id="b8045-102">Éléments fondamentaux de l'héritage (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b8045-102">Inheritance Basics (Visual Basic)</span></span>
<span data-ttu-id="b8045-103">Le `Inherits` instruction est utilisée pour déclarer une nouvelle classe, appelée un *classe dérivée*, basé sur une classe existante, appelée un *classe de base*.</span><span class="sxs-lookup"><span data-stu-id="b8045-103">The `Inherits` statement is used to declare a new class, called a *derived class*, based on an existing class, known as a *base class*.</span></span> <span data-ttu-id="b8045-104">Les classes dérivées héritent et peuvent étendre les propriétés, les méthodes, les événements, les champs et les constantes définies dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="b8045-104">Derived classes inherit, and can extend, the properties, methods, events, fields, and constants defined in the base class.</span></span> <span data-ttu-id="b8045-105">La section suivante décrit certaines des règles pour l’héritage et les modificateurs que vous pouvez utiliser pour modifier les façon dont les classes héritent ou sont héritées :</span><span class="sxs-lookup"><span data-stu-id="b8045-105">The following section describes some of the rules for inheritance, and the modifiers you can use to change the way classes inherit or are inherited:</span></span>  
  
- <span data-ttu-id="b8045-106">Par défaut, toutes les classes sont héritées, sauf si marqué avec le `NotInheritable` mot clé.</span><span class="sxs-lookup"><span data-stu-id="b8045-106">By default, all classes are inheritable unless marked with the `NotInheritable` keyword.</span></span> <span data-ttu-id="b8045-107">Les classes peuvent hériter d’autres classes dans votre projet ou à partir de classes dans d’autres assemblys qui fait référence à votre projet.</span><span class="sxs-lookup"><span data-stu-id="b8045-107">Classes can inherit from other classes in your project or from classes in other assemblies that your project references.</span></span>  
  
- <span data-ttu-id="b8045-108">Contrairement aux langages qui permettent l’héritage multiple, Visual Basic ne permet qu’un seul héritage dans les classes ; Autrement dit, les classes dérivées peuvent avoir qu’une seule classe de base.</span><span class="sxs-lookup"><span data-stu-id="b8045-108">Unlike languages that allow multiple inheritance, Visual Basic allows only single inheritance in classes; that is, derived classes can have only one base class.</span></span> <span data-ttu-id="b8045-109">Bien que l’héritage multiple n’est pas autorisée dans les classes, les classes peuvent implémenter plusieurs interfaces, qui peuvent accomplir efficacement les mêmes objectifs.</span><span class="sxs-lookup"><span data-stu-id="b8045-109">Although multiple inheritance is not allowed in classes, classes can implement multiple interfaces, which can effectively accomplish the same ends.</span></span>  
  
- <span data-ttu-id="b8045-110">Pour empêcher l’exposition des éléments restreints dans une classe de base, le type d’accès d’une classe dérivée doit être égal à ou plus restrictif que sa classe de base.</span><span class="sxs-lookup"><span data-stu-id="b8045-110">To prevent exposing restricted items in a base class, the access type of a derived class must be equal to or more restrictive than its base class.</span></span> <span data-ttu-id="b8045-111">Par exemple, un `Public` classe ne peut pas hériter une `Friend` ou un `Private` (classe) et un `Friend` classe ne peut pas hériter une `Private` classe.</span><span class="sxs-lookup"><span data-stu-id="b8045-111">For example, a `Public` class cannot inherit a `Friend` or a `Private` class, and a `Friend` class cannot inherit a `Private` class.</span></span>  
  
## <a name="inheritance-modifiers"></a><span data-ttu-id="b8045-112">Modificateurs d’héritage</span><span class="sxs-lookup"><span data-stu-id="b8045-112">Inheritance Modifiers</span></span>  
 <span data-ttu-id="b8045-113">Visual Basic présente les modificateurs pour prendre en charge l’héritage ni les instructions de niveau classe suivantes :</span><span class="sxs-lookup"><span data-stu-id="b8045-113">Visual Basic introduces the following class-level statements and modifiers to support inheritance:</span></span>  
  
- <span data-ttu-id="b8045-114">`Inherits` instruction : Spécifie la classe de base.</span><span class="sxs-lookup"><span data-stu-id="b8045-114">`Inherits` statement — Specifies the base class.</span></span>  
  
- <span data-ttu-id="b8045-115">`NotInheritable` modificateur : empêche les programmeurs d’utilisation de la classe comme classe de base.</span><span class="sxs-lookup"><span data-stu-id="b8045-115">`NotInheritable` modifier — Prevents programmers from using the class as a base class.</span></span>  
  
- <span data-ttu-id="b8045-116">`MustInherit` modificateur — Spécifie que la classe est destinée à utiliser comme une classe de base.</span><span class="sxs-lookup"><span data-stu-id="b8045-116">`MustInherit` modifier — Specifies that the class is intended for use as a base class only.</span></span> <span data-ttu-id="b8045-117">Instances de `MustInherit` classes ne peuvent pas être créées directement ; elles peuvent uniquement être créées comme base des instances de classe d’une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="b8045-117">Instances of `MustInherit` classes cannot be created directly; they can only be created as base class instances of a derived class.</span></span> <span data-ttu-id="b8045-118">(Autres langages de programmation, tels que C++ et C#, utilisent le terme *classe abstraite* pour décrire une telle classe.)</span><span class="sxs-lookup"><span data-stu-id="b8045-118">(Other programming languages, such as C++ and C#, use the term *abstract class* to describe such a class.)</span></span>  
  
## <a name="overriding-properties-and-methods-in-derived-classes"></a><span data-ttu-id="b8045-119">Substitution de propriétés et méthodes dans les Classes dérivées</span><span class="sxs-lookup"><span data-stu-id="b8045-119">Overriding Properties and Methods in Derived Classes</span></span>  
 <span data-ttu-id="b8045-120">Par défaut, une classe dérivée hérite des propriétés et méthodes à partir de sa classe de base.</span><span class="sxs-lookup"><span data-stu-id="b8045-120">By default, a derived class inherits properties and methods from its base class.</span></span> <span data-ttu-id="b8045-121">Si une propriété héritée ou une méthode doit se comporter différemment dans la classe dérivée, il peut être *substitution*.</span><span class="sxs-lookup"><span data-stu-id="b8045-121">If an inherited property or method has to behave differently in the derived class it can be *overridden*.</span></span> <span data-ttu-id="b8045-122">Autrement dit, vous pouvez définir une nouvelle implémentation de la méthode dans la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="b8045-122">That is, you can define a new implementation of the method in the derived class.</span></span> <span data-ttu-id="b8045-123">Les modificateurs suivants sont utilisés pour contrôler la façon dont les propriétés et les méthodes sont substituées :</span><span class="sxs-lookup"><span data-stu-id="b8045-123">The following modifiers are used to control how properties and methods are overridden:</span></span>  
  
- <span data-ttu-id="b8045-124">`Overridable` : Permet à une propriété ou méthode dans une classe de substitution dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="b8045-124">`Overridable` — Allows a property or method in a class to be overridden in a derived class.</span></span>  
  
- <span data-ttu-id="b8045-125">`Overrides` : Substitue un `Overridable` propriété ou méthode définie dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="b8045-125">`Overrides` — Overrides an `Overridable` property or method defined in the base class.</span></span>  
  
- <span data-ttu-id="b8045-126">`NotOverridable` — Empêche une propriété ou méthode en cours de substitution dans une classe qui hérite.</span><span class="sxs-lookup"><span data-stu-id="b8045-126">`NotOverridable` — Prevents a property or method from being overridden in an inheriting class.</span></span> <span data-ttu-id="b8045-127">Par défaut, `Public` sont des méthodes `NotOverridable`.</span><span class="sxs-lookup"><span data-stu-id="b8045-127">By default, `Public` methods are `NotOverridable`.</span></span>  
  
- <span data-ttu-id="b8045-128">`MustOverride` — Nécessite qu’une classe dérivée substituer la propriété ou méthode.</span><span class="sxs-lookup"><span data-stu-id="b8045-128">`MustOverride` — Requires that a derived class override the property or method.</span></span> <span data-ttu-id="b8045-129">Lorsque le `MustOverride` mot clé est utilisé, la définition de méthode se compose uniquement le `Sub`, `Function`, ou `Property` instruction.</span><span class="sxs-lookup"><span data-stu-id="b8045-129">When the `MustOverride` keyword is used, the method definition consists of just the `Sub`, `Function`, or `Property` statement.</span></span> <span data-ttu-id="b8045-130">Aucune autre instruction n’est autorisées et, en particulier aucune `End Sub` ou `End Function` instruction.</span><span class="sxs-lookup"><span data-stu-id="b8045-130">No other statements are allowed, and specifically there is no `End Sub` or `End Function` statement.</span></span> <span data-ttu-id="b8045-131">`MustOverride` les méthodes doivent être déclarées dans `MustInherit` classes.</span><span class="sxs-lookup"><span data-stu-id="b8045-131">`MustOverride` methods must be declared in `MustInherit` classes.</span></span>  
  
 <span data-ttu-id="b8045-132">Supposons que vous souhaitez définir des classes pour gérer les salaires.</span><span class="sxs-lookup"><span data-stu-id="b8045-132">Suppose you want to define classes to handle payroll.</span></span> <span data-ttu-id="b8045-133">Vous pouvez définir un générique `Payroll` classe qui contient un `RunPayroll` méthode qui calcule les salaires pour une semaine type.</span><span class="sxs-lookup"><span data-stu-id="b8045-133">You could define a generic `Payroll` class that contains a `RunPayroll` method that calculates payroll for a typical week.</span></span> <span data-ttu-id="b8045-134">Vous pouvez ensuite utiliser `Payroll` comme classe de base pour une plus spécialisées `BonusPayroll` (classe), qui pouvait être utilisée lors de la distribution de primes aux employés.</span><span class="sxs-lookup"><span data-stu-id="b8045-134">You could then use `Payroll` as a base class for a more specialized `BonusPayroll` class, which could be used when distributing employee bonuses.</span></span>  
  
 <span data-ttu-id="b8045-135">Le `BonusPayroll` classe peut hériter et remplacer, le `PayEmployee` méthode définie dans la base de `Payroll` classe.</span><span class="sxs-lookup"><span data-stu-id="b8045-135">The `BonusPayroll` class can inherit, and override, the `PayEmployee` method defined in the base `Payroll` class.</span></span>  
  
 <span data-ttu-id="b8045-136">L’exemple suivant définit une classe de base, `Payroll,` et une classe dérivée, `BonusPayroll`, qui substitue une méthode héritée, `PayEmployee`.</span><span class="sxs-lookup"><span data-stu-id="b8045-136">The following example defines a base class, `Payroll,` and a derived class, `BonusPayroll`, which overrides an inherited method, `PayEmployee`.</span></span> <span data-ttu-id="b8045-137">Une procédure, `RunPayroll`, crée et passe ensuite un `Payroll` objet et un `BonusPayroll` objet à une fonction, `Pay`, qui exécute le `PayEmployee` méthode des deux objets.</span><span class="sxs-lookup"><span data-stu-id="b8045-137">A procedure, `RunPayroll`, creates and then passes a `Payroll` object and a `BonusPayroll` object to a function, `Pay`, that executes the `PayEmployee` method of both objects.</span></span>  
  
 [!code-vb[VbVbalrOOP#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#28)]  
  
## <a name="the-mybase-keyword"></a><span data-ttu-id="b8045-138">Le mot clé MyBase</span><span class="sxs-lookup"><span data-stu-id="b8045-138">The MyBase Keyword</span></span>  
 <span data-ttu-id="b8045-139">Le `MyBase` mot clé se comporte comme une variable objet qui fait référence à la classe de base de l’instance actuelle d’une classe.</span><span class="sxs-lookup"><span data-stu-id="b8045-139">The `MyBase` keyword behaves like an object variable that refers to the base class of the current instance of a class.</span></span> <span data-ttu-id="b8045-140">`MyBase` est fréquemment utilisé pour accéder aux membres de classe de base qui sont substitués ou occultés dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="b8045-140">`MyBase` is frequently used to access base class members that are overridden or shadowed in a derived class.</span></span> <span data-ttu-id="b8045-141">En particulier, `MyBase.New` est utilisé pour appeler explicitement un constructeur de classe de base à partir d’un constructeur de classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="b8045-141">In particular, `MyBase.New` is used to explicitly call a base class constructor from a derived class constructor.</span></span>  
  
 <span data-ttu-id="b8045-142">Par exemple, supposons que vous concevez une classe dérivée qui substitue une méthode héritée de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="b8045-142">For example, suppose you are designing a derived class that overrides a method inherited from the base class.</span></span> <span data-ttu-id="b8045-143">La méthode substituée peut appeler la méthode dans la classe de base et modifiez la valeur de retour comme indiqué dans le fragment de code suivant :</span><span class="sxs-lookup"><span data-stu-id="b8045-143">The overridden method can call the method in the base class and modify the return value as shown in the following code fragment:</span></span>  
  
 [!code-vb[VbVbalrOOP#109](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#109)]  
  
 <span data-ttu-id="b8045-144">La liste suivante décrit les restrictions sur l’utilisation de `MyBase`:</span><span class="sxs-lookup"><span data-stu-id="b8045-144">The following list describes restrictions on using `MyBase`:</span></span>  
  
- <span data-ttu-id="b8045-145">`MyBase` fait référence à la classe de base immédiate et à ses membres hérités.</span><span class="sxs-lookup"><span data-stu-id="b8045-145">`MyBase` refers to the immediate base class and its inherited members.</span></span> <span data-ttu-id="b8045-146">Il ne peut pas être utilisé pour accéder à `Private` membres dans la classe.</span><span class="sxs-lookup"><span data-stu-id="b8045-146">It cannot be used to access `Private` members in the class.</span></span>  
  
- <span data-ttu-id="b8045-147">`MyBase` est un mot clé, pas un objet réel.</span><span class="sxs-lookup"><span data-stu-id="b8045-147">`MyBase` is a keyword, not a real object.</span></span> <span data-ttu-id="b8045-148">`MyBase` ne peut pas être assigné à une variable, passés à des procédures ou utilisé dans un `Is` comparaison.</span><span class="sxs-lookup"><span data-stu-id="b8045-148">`MyBase` cannot be assigned to a variable, passed to procedures, or used in an `Is` comparison.</span></span>  
  
- <span data-ttu-id="b8045-149">La méthode qui `MyBase` qualifie ne doit pas être définie dans la classe de base immédiate ; il peut être définie à la place dans une classe de base héritée indirectement.</span><span class="sxs-lookup"><span data-stu-id="b8045-149">The method that `MyBase` qualifies does not have to be defined in the immediate base class; it may instead be defined in an indirectly inherited base class.</span></span> <span data-ttu-id="b8045-150">Dans l’ordre pour une référence qualifiée par `MyBase` pour compiler correctement, une classe de base doit contenir une méthode qui correspond au nom et les types de paramètres qui apparaissent dans l’appel.</span><span class="sxs-lookup"><span data-stu-id="b8045-150">In order for a reference qualified by `MyBase` to compile correctly, some base class must contain a method matching the name and types of parameters that appear in the call.</span></span>  
  
- <span data-ttu-id="b8045-151">Vous ne pouvez pas utiliser `MyBase` pour appeler `MustOverride` méthodes de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="b8045-151">You cannot use `MyBase` to call `MustOverride` base class methods.</span></span>  
  
- <span data-ttu-id="b8045-152">`MyBase` ne peut pas être utilisé pour se qualifier lui-même.</span><span class="sxs-lookup"><span data-stu-id="b8045-152">`MyBase` cannot be used to qualify itself.</span></span> <span data-ttu-id="b8045-153">Par conséquent, le code suivant n’est pas valide :</span><span class="sxs-lookup"><span data-stu-id="b8045-153">Therefore, the following code is not valid:</span></span>  
  
     `MyBase.MyBase.BtnOK_Click()`  
  
- <span data-ttu-id="b8045-154">`MyBase` ne peut pas être utilisé dans des modules.</span><span class="sxs-lookup"><span data-stu-id="b8045-154">`MyBase` cannot be used in modules.</span></span>  
  
- <span data-ttu-id="b8045-155">`MyBase` ne peut pas être utilisé pour accéder aux membres de classe de base qui sont marqués comme `Friend` si la classe de base se trouve dans un autre assembly.</span><span class="sxs-lookup"><span data-stu-id="b8045-155">`MyBase` cannot be used to access base class members that are marked as `Friend` if the base class is in a different assembly.</span></span>  
  
 <span data-ttu-id="b8045-156">Pour plus d’informations et un autre exemple, consultez [Comment : Accéder à une Variable masquée par une classe dérivée](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-access-a-variable-hidden-by-a-derived-class.md).</span><span class="sxs-lookup"><span data-stu-id="b8045-156">For more information and another example, see [How to: Access a Variable Hidden by a Derived Class](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-access-a-variable-hidden-by-a-derived-class.md).</span></span>  
  
## <a name="the-myclass-keyword"></a><span data-ttu-id="b8045-157">Le mot clé MyClass</span><span class="sxs-lookup"><span data-stu-id="b8045-157">The MyClass Keyword</span></span>  
 <span data-ttu-id="b8045-158">Le `MyClass` mot clé se comporte comme une variable objet qui fait référence à l’instance actuelle d’une classe implémentée à l’origine.</span><span class="sxs-lookup"><span data-stu-id="b8045-158">The `MyClass` keyword behaves like an object variable that refers to the current instance of a class as originally implemented.</span></span> <span data-ttu-id="b8045-159">`MyClass` ressemble à `Me`, mais chaque méthode et propriété appeler sur `MyClass` est traitée comme si la méthode ou propriété ont été [NotOverridable](../../../../visual-basic/language-reference/modifiers/notoverridable.md).</span><span class="sxs-lookup"><span data-stu-id="b8045-159">`MyClass` resembles `Me`, but every method and property call on `MyClass` is treated as if the method or property were [NotOverridable](../../../../visual-basic/language-reference/modifiers/notoverridable.md).</span></span> <span data-ttu-id="b8045-160">Par conséquent, la méthode ou propriété n’est pas affectée par la substitution dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="b8045-160">Therefore, the method or property is not affected by overriding in a derived class.</span></span>  
  
- <span data-ttu-id="b8045-161">`MyClass` est un mot clé, pas un objet réel.</span><span class="sxs-lookup"><span data-stu-id="b8045-161">`MyClass` is a keyword, not a real object.</span></span> <span data-ttu-id="b8045-162">`MyClass` ne peut pas être assigné à une variable, passés à des procédures ou utilisé dans un `Is` comparaison.</span><span class="sxs-lookup"><span data-stu-id="b8045-162">`MyClass` cannot be assigned to a variable, passed to procedures, or used in an `Is` comparison.</span></span>  
  
- <span data-ttu-id="b8045-163">`MyClass` fait référence à la classe conteneur et ses membres hérités.</span><span class="sxs-lookup"><span data-stu-id="b8045-163">`MyClass` refers to the containing class and its inherited members.</span></span>  
  
- <span data-ttu-id="b8045-164">`MyClass` peut être utilisé comme qualificateur pour `Shared` membres.</span><span class="sxs-lookup"><span data-stu-id="b8045-164">`MyClass` can be used as a qualifier for `Shared` members.</span></span>  
  
- <span data-ttu-id="b8045-165">`MyClass` ne peut pas être utilisé à l’intérieur d’un `Shared` (méthode), mais peut être utilisé pour accéder à un membre partagé d’une classe à l’intérieur d’une méthode d’instance.</span><span class="sxs-lookup"><span data-stu-id="b8045-165">`MyClass` cannot be used inside a `Shared` method, but can be used inside an instance method to access a shared member of a class.</span></span>  
  
- <span data-ttu-id="b8045-166">`MyClass` ne peut pas être utilisé dans des modules standard.</span><span class="sxs-lookup"><span data-stu-id="b8045-166">`MyClass` cannot be used in standard modules.</span></span>  
  
- <span data-ttu-id="b8045-167">`MyClass` peut être utilisé pour qualifier une méthode qui est définie dans une classe de base et ne possède aucune implémentation de la méthode fournie dans cette classe.</span><span class="sxs-lookup"><span data-stu-id="b8045-167">`MyClass` can be used to qualify a method that is defined in a base class and that has no implementation of the method provided in that class.</span></span> <span data-ttu-id="b8045-168">Une telle référence a la même signification que `MyBase.` *méthode*.</span><span class="sxs-lookup"><span data-stu-id="b8045-168">Such a reference has the same meaning as `MyBase.`*Method*.</span></span>  
  
 <span data-ttu-id="b8045-169">L’exemple suivant compare `Me` et `MyClass`.</span><span class="sxs-lookup"><span data-stu-id="b8045-169">The following example compares `Me` and `MyClass`.</span></span>  
  
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
  
 <span data-ttu-id="b8045-170">Même si `derivedClass` substitue `testMethod`, le `MyClass` mot clé dans `useMyClass` annule les effets de substitution et le compilateur résout l’appel à la version de la classe de base de `testMethod`.</span><span class="sxs-lookup"><span data-stu-id="b8045-170">Even though `derivedClass` overrides `testMethod`, the `MyClass` keyword in `useMyClass` nullifies the effects of overriding, and the compiler resolves the call to the base class version of `testMethod`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b8045-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8045-171">See also</span></span>

- [<span data-ttu-id="b8045-172">Inherits (instruction)</span><span class="sxs-lookup"><span data-stu-id="b8045-172">Inherits Statement</span></span>](../../../../visual-basic/language-reference/statements/inherits-statement.md)
- [<span data-ttu-id="b8045-173">Me, My, MyBase et MyClass</span><span class="sxs-lookup"><span data-stu-id="b8045-173">Me, My, MyBase, and MyClass</span></span>](../../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
