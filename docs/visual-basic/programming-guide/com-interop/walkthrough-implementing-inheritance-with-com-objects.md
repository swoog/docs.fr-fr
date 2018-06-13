---
title: "Procédure pas à pas : implémentation de l'héritage avec les objets COM (Visual Basic)"
ms.date: 07/20/2015
helpviewer_keywords:
- inheritance [Visual Basic], COM reusability
- base classes [Visual Basic], COM reusability
- inheritance [Visual Basic], walkthroughs
- derived classes [Visual Basic], COM reusability
ms.assetid: f8e7263a-de13-48d1-b67c-ca1adf3544d9
ms.openlocfilehash: a1c1b7c247d3277c6614a4774395650c4c069c2f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33644301"
---
# <a name="walkthrough-implementing-inheritance-with-com-objects-visual-basic"></a>Procédure pas à pas : implémentation de l'héritage avec les objets COM (Visual Basic)
Vous pouvez dériver des classes Visual Basic à partir de `Public` classes dans les objets COM, même ceux créés dans les versions antérieures de Visual Basic. Les propriétés et méthodes des classes héritées d’objets COM peuvent être substituées ou surchargées comme les propriétés et méthodes de toute autre classe de base peuvent être remplacées ou surchargés. L’héritage à partir des objets COM est utile lorsque vous disposez d’une bibliothèque de classe existante que vous ne souhaitez pas recompiler.  
  
 La procédure suivante montre comment utiliser Visual Basic 6.0 pour créer un objet COM qui contient une classe, puis l’utiliser comme classe de base.  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-build-the-com-object-that-is-used-in-this-walkthrough"></a>Pour générer l’objet COM qui est utilisé dans cette procédure pas à pas  
  
1.  Dans Visual Basic 6.0, ouvrez un nouveau projet de DLL ActiveX. Un projet nommé `Project1` est créé. Il comporte une classe nommée `Class1`.  
  
2.  Dans le **Explorateur de projets**, avec le bouton droit **Projet1**, puis cliquez sur **Propriétés Projet1**. Le **propriétés du projet** boîte de dialogue s’affiche.  
  
3.  Sur le **général** onglet de la **propriétés du projet** boîte de dialogue, changez le nom du projet en tapant `ComObject1` dans les **nom du projet** champ.  
  
4.  Dans le **Explorateur de projets**, avec le bouton droit `Class1`, puis cliquez sur **propriétés**. Le **propriétés** fenêtre de la classe s’affiche.  
  
5.  Modifier la `Name` propriété `MathFunctions`.  
  
6.  Dans le **Explorateur de projets**, avec le bouton droit `MathFunctions`, puis cliquez sur **afficher le Code**. Le **éditeur de Code** s’affiche.  
  
7.  Ajoutez une variable locale pour stocker la valeur de propriété :  
  
    ```  
    ' Local variable to hold property value  
    Private mvarProp1 As Integer  
    ```  
  
8.  Ajoutez la propriété `Let` et la propriété `Get` procédures de propriété :  
  
    ```  
    Public Property Let Prop1(ByVal vData As Integer)  
       'Used when assigning a value to the property.  
       mvarProp1 = vData  
    End Property  
    Public Property Get Prop1() As Integer  
       'Used when retrieving a property's value.  
       Prop1 = mvarProp1  
    End Property  
    ```  
  
9. Ajouter une fonction :  
  
    ```  
    Function AddNumbers(   
       ByVal SomeNumber As Integer,   
       ByVal AnotherNumber As Integer) As Integer  
  
       AddNumbers = SomeNumber + AnotherNumber  
    End Function  
    ```  
  
10. Créer et inscrire l’objet COM en cliquant sur **Créer ComObject1.dll** sur la **fichier** menu.  
  
    > [!NOTE]
    >  Bien que vous pouvez également exposer une classe créée avec Visual Basic en tant qu’objet COM, il n’est pas un objet COM réel et ne peut pas être utilisé dans cette procédure pas à pas. Pour plus d’informations, consultez [interopérabilité COM dans les Applications .NET Framework](../../../visual-basic/programming-guide/com-interop/com-interoperability-in-net-framework-applications.md).  
  
## <a name="interop-assemblies"></a>Assemblys d’interopérabilité  
 Dans la procédure suivante, vous allez créer un assembly d’interopérabilité, qui fait Office de pont entre le code non managé (par exemple, un objet COM) et le code managé, que Visual Studio utilise. L’assembly PIA Visual Basic crée gère de nombreux détails de l’utilisation avec des objets COM, tel que *le marshaling d’interopérabilité*, le processus empaqueter des paramètres et valeurs de retour des données de l’équivalentes de types lors de leur déplacement à et à partir des objets COM. La référence de l’application Visual Basic pointe vers l’assembly d’interopérabilité, pas l’objet COM réel.  
  
#### <a name="to-use-a-com-object-with-visual-basic-2005-and-later-versions"></a>Pour utiliser un objet COM avec Visual Basic 2005 et versions ultérieures  
  
1.  Ouvrez un nouveau projet d’application Windows Visual Basic.  
  
2.  Dans le menu **Projet**, cliquez sur **Ajouter une référence**.  
  
     La boîte de dialogue **Ajouter une référence** s’affiche.  
  
3.  Sur le **COM** onglet, double-cliquez sur `ComObject1` dans les **nom du composant** liste et cliquez sur **OK**.  
  
4.  Dans le menu **Projet** , cliquez sur **Ajouter un nouvel élément**.  
  
     La boîte de dialogue **Ajouter un nouvel élément** s’affiche.  
  
5.  Dans le **modèles** volet, cliquez sur **classe**.  
  
     Le nom de fichier par défaut, `Class1.vb`, apparaît dans le **nom** champ. Remplacez ce champ par MathClass.vb et cliquez sur **ajouter**. Cette opération crée une classe nommée `MathClass`et affiche son code.  
  
6.  Ajoutez le code suivant en haut du `MathClass` d’hériter de la classe COM.  
  
     [!code-vb[VbVbalrInterop#31](../../../visual-basic/programming-guide/com-interop/codesnippet/VisualBasic/walkthrough-implementing-inheritance-with-com-objects_1.vb)]  
  
7.  Surcharge de la méthode publique de la classe de base en ajoutant le code suivant à `MathClass`:  
  
     [!code-vb[VbVbalrInterop#32](../../../visual-basic/programming-guide/com-interop/codesnippet/VisualBasic/walkthrough-implementing-inheritance-with-com-objects_2.vb)]  
  
8.  Étendez la classe héritée en ajoutant le code suivant à `MathClass`:  
  
     [!code-vb[VbVbalrInterop#33](../../../visual-basic/programming-guide/com-interop/codesnippet/VisualBasic/walkthrough-implementing-inheritance-with-com-objects_3.vb)]  
  
 La nouvelle classe hérite des propriétés de la classe de base dans l’objet COM, surcharge une méthode et définit une nouvelle méthode pour étendre la classe.  
  
#### <a name="to-test-the-inherited-class"></a>Pour tester la classe héritée  
  
1.  Ajouter un bouton à votre formulaire de démarrage, puis double-cliquez dessus pour afficher son code.  
  
2.  Dans du bouton `Click` procédure gestionnaire d’événements, ajoutez le code suivant pour créer une instance de `MathClass` et appeler les méthodes surchargées :  
  
     [!code-vb[VbVbalrInterop#34](../../../visual-basic/programming-guide/com-interop/codesnippet/VisualBasic/walkthrough-implementing-inheritance-with-com-objects_4.vb)]  
  
3.  Exécutez le projet en appuyant sur F5.  
  
 Lorsque vous cliquez sur le bouton dans le formulaire, le `AddNumbers` méthode est d’abord appelée avec `Short` nombres, de type de données et Visual Basic choisit la méthode appropriée à partir de la classe de base. Le deuxième appel à `AddNumbers` est dirigé vers la méthode de surcharge à partir de `MathClass`. Le troisième appel appelle le `SubtractNumbers` (méthode), qui étend la classe. La propriété dans la classe de base est définie, et la valeur est affichée.  
  
## <a name="next-steps"></a>Étapes suivantes  
 Vous avez peut-être remarqué que surchargées `AddNumbers` fonction semble avoir les mêmes données que la méthode héritée de la classe de base de l’objet COM de type. Il s’agit, car les arguments et les paramètres de la méthode de classe de base sont définis en tant qu’entiers 16 bits dans Visual Basic 6.0, mais elles sont exposées en tant qu’entiers 16 bits de type `Short` dans les versions ultérieures de Visual Basic. La nouvelle fonction accepte les nombres entiers 32 bits et les surcharges de la fonction de la classe de base.  
  
 Lorsque vous travaillez avec des objets COM, vérifiez que les types de données et la taille des paramètres. Par exemple, lorsque vous utilisez un objet COM qui accepte un objet de collection Visual Basic 6.0 en tant qu’argument, vous ne peut pas fournir une collection à partir d’une version ultérieure de Visual Basic.  
  
 Propriétés et méthodes héritées des classes COM peuvent être remplacées, ce qui signifie que que vous pouvez déclarer une propriété locale ou une méthode qui remplace une propriété ou une méthode héritée d’une classe COM de base. Les règles de substitution des propriétés COM héritées sont similaires aux règles de substitution des autres propriétés et méthodes avec les exceptions suivantes :  
  
-   Si vous substituez une propriété ou une méthode héritée d’une classe COM, vous devez substituer toutes les autres propriétés et méthodes héritées.  
  
-   Les propriétés qui utilisent `ByRef` paramètres ne peut pas être substituées.  
  
## <a name="see-also"></a>Voir aussi  
 [Interopérabilité COM dans les applications .NET Framework](../../../visual-basic/programming-guide/com-interop/com-interoperability-in-net-framework-applications.md)  
 [Inherits (instruction)](../../../visual-basic/language-reference/statements/inherits-statement.md)  
 [Short (type de données)](../../../visual-basic/language-reference/data-types/short-data-type.md)
