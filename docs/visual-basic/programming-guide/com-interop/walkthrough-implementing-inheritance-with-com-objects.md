---
title: 'Procédure pas à pas : Implémentation de l’héritage avec les objets COM (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- inheritance [Visual Basic], COM reusability
- base classes [Visual Basic], COM reusability
- inheritance [Visual Basic], walkthroughs
- derived classes [Visual Basic], COM reusability
ms.assetid: f8e7263a-de13-48d1-b67c-ca1adf3544d9
ms.openlocfilehash: 79d80a1a91911a361bd21f1f3f74424f4f656a18
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64620052"
---
# <a name="walkthrough-implementing-inheritance-with-com-objects-visual-basic"></a>Procédure pas à pas : Implémentation de l’héritage avec les objets COM (Visual Basic)
Vous pouvez dériver des classes Visual Basic à partir de `Public` classes dans les objets COM, même ceux créés dans les versions antérieures de Visual Basic. Les propriétés et méthodes des classes héritées d’objets COM peuvent être substituées ou surchargées comme les propriétés et méthodes de toute autre classe de base peuvent être substituées ou surchargés. L’héritage d’objets COM est utile lorsque vous avez une bibliothèque de classe existante que vous ne souhaitez pas recompiler.  
  
 La procédure suivante montre comment utiliser Visual Basic 6.0 pour créer un objet COM contenant une classe et ensuite l’utiliser comme une classe de base.  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-build-the-com-object-that-is-used-in-this-walkthrough"></a>Pour créer l’objet COM qui est utilisé dans cette procédure pas à pas  
  
1. Dans Visual Basic 6.0, ouvrez un nouveau projet de DLL ActiveX. Un projet nommé `Project1` est créé. Il a une classe nommée `Class1`.  
  
2. Dans le **Explorateur de projets**, avec le bouton droit **Project1**, puis cliquez sur **Propriétés Projet1**. Le **propriétés du projet** boîte de dialogue s’affiche.  
  
3. Sur le **général** onglet de la **propriétés du projet** boîte de dialogue, changez le nom du projet en tapant `ComObject1` dans le **nom_projet** champ.  
  
4. Dans le **Explorateur de projets**, avec le bouton droit `Class1`, puis cliquez sur **propriétés**. Le **propriétés** fenêtre de la classe s’affiche.  
  
5. Modifier le `Name` propriété `MathFunctions`.  
  
6. Dans le **Explorateur de projets**, avec le bouton droit `MathFunctions`, puis cliquez sur **afficher le Code**. Le **éditeur de Code** s’affiche.  
  
7. Ajoutez une variable locale pour contenir la valeur de propriété :  
  
    ```  
    ' Local variable to hold property value  
    Private mvarProp1 As Integer  
    ```  
  
8. Ajouter une propriété `Let` et propriété `Get` procédures de propriété :  
  
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
  
10. Créer et inscrire l’objet COM en cliquant sur **Créer ComObject1.dll** sur le **fichier** menu.  
  
    > [!NOTE]
    >  Bien que vous pouvez également exposer une classe créée avec Visual Basic en tant qu’objet COM, il n’est pas un véritable objet COM et ne peut pas être utilisé dans cette procédure pas à pas. Pour plus d’informations, consultez [interopérabilité COM dans les Applications .NET Framework](../../../visual-basic/programming-guide/com-interop/com-interoperability-in-net-framework-applications.md).  
  
## <a name="interop-assemblies"></a>Assemblys PIA  
 Dans la procédure suivante, vous allez créer un assembly d’interopérabilité, qui fait Office de pont entre le code non managé (par exemple, un objet COM) et le code managé qu'utilise Visual Studio. L’assembly d’interopérabilité qui crée de Visual Basic gère de nombreux détails de l’utilisation avec des objets COM, tel que *le marshaling d’interopérabilité*, le processus empaqueter des paramètres et valeurs de retour dans les données équivalents types lorsqu’ils passent à et à partir des objets COM. La référence dans l’application Visual Basic pointe vers l’assembly d’interopérabilité, pas l’objet COM réel.  
  
#### <a name="to-use-a-com-object-with-visual-basic-2005-and-later-versions"></a>Pour utiliser un objet COM avec Visual Basic 2005 et versions ultérieures  
  
1. Ouvrez un nouveau projet d’application Windows Visual Basic.  
  
2. Dans le menu **Projet**, cliquez sur **Ajouter une référence**.  
  
     La boîte de dialogue **Ajouter une référence** s’affiche.  
  
3. Sur le **COM** onglet, double-cliquez sur `ComObject1` dans le **nom du composant** liste et cliquez sur **OK**.  
  
4. Dans le menu **Projet** , cliquez sur **Ajouter un nouvel élément**.  
  
     La boîte de dialogue **Ajouter un nouvel élément** s’affiche.  
  
5. Dans le **modèles** volet, cliquez sur **classe**.  
  
     Le nom de fichier par défaut, `Class1.vb`, apparaît dans le **nom** champ. Modifiez ce champ à MathClass.vb et cliquez sur **ajouter**. Cette opération crée une classe nommée `MathClass`et affiche son code.  
  
6. Ajoutez le code suivant au début du `MathClass` d’hériter de la classe COM.  
  
     [!code-vb[VbVbalrInterop#31](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrInterop/VB/Class1.vb#31)]  
  
7. Surcharger la méthode publique de la classe de base en ajoutant le code suivant à `MathClass`:  
  
     [!code-vb[VbVbalrInterop#32](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrInterop/VB/Class1.vb#32)]  
  
8. Étendez la classe héritée en ajoutant le code suivant à `MathClass`:  
  
     [!code-vb[VbVbalrInterop#33](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrInterop/VB/Class1.vb#33)]  
  
 La nouvelle classe hérite des propriétés de la classe de base dans l’objet COM, surcharge une méthode et définit une nouvelle méthode pour étendre la classe.  
  
#### <a name="to-test-the-inherited-class"></a>Pour tester la classe héritée  
  
1. Ajouter un bouton à votre formulaire de démarrage, puis double-cliquez dessus pour afficher son code.  
  
2. Dans le bouton `Click` procédure de gestionnaire d’événements, ajoutez le code suivant pour créer une instance de `MathClass` et appeler les méthodes surchargées :  
  
     [!code-vb[VbVbalrInterop#34](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrInterop/VB/Class1.vb#34)]  
  
3. Exécutez le projet en appuyant sur F5.  
  
 Lorsque vous cliquez sur le bouton sur le formulaire, le `AddNumbers` méthode est appelée tout d’abord avec `Short` numéros, de type de données et Visual Basic choisit la méthode appropriée à partir de la classe de base. Le deuxième appel à `AddNumbers` est dirigé vers la méthode de surcharge à partir de `MathClass`. Le troisième appel appelle le `SubtractNumbers` (méthode), qui étend la classe. La propriété dans la classe de base est définie, et la valeur est affichée.  
  
## <a name="next-steps"></a>Étapes suivantes  
 Vous avez peut-être remarqué que surchargées `AddNumbers` fonction semble avoir les données du mêmes type que la méthode héritée de la classe de base de l’objet COM. Il s’agit, car les arguments et les paramètres de la méthode de classe de base sont définis en tant qu’entiers 16 bits dans Visual Basic 6.0, mais elles sont exposées sous forme d’entiers 16 bits de type `Short` dans les versions ultérieures de Visual Basic. La nouvelle fonction accepte des entiers 32 bits et surcharge de la fonction de la classe de base.  
  
 Lorsque vous travaillez avec des objets COM, vérifiez que les taille et les types des paramètres. Par exemple, lorsque vous utilisez un objet COM qui accepte un objet de collection Visual Basic 6.0 en tant qu’argument, vous ne peut pas fournir une collection à partir d’une version ultérieure de Visual Basic.  
  
 Propriétés et méthodes héritées des classes COM peuvent être substituées, ce qui signifie que vous pouvez déclarer une propriété locale ou une méthode qui remplace une propriété ou méthode héritée d’une classe COM de base. Les règles de substitution des propriétés COM héritées sont similaires aux règles de substitution des autres propriétés et méthodes avec les exceptions suivantes :  
  
- Si vous substituez une propriété ou une méthode héritée d’une classe COM, vous devez substituer toutes les autres propriétés et méthodes héritées.  
  
- Les propriétés qui utilisent `ByRef` paramètres ne peut pas être substituées.  
  
## <a name="see-also"></a>Voir aussi

- [Interopérabilité COM dans les applications .NET Framework](../../../visual-basic/programming-guide/com-interop/com-interoperability-in-net-framework-applications.md)
- [Inherits (instruction)](../../../visual-basic/language-reference/statements/inherits-statement.md)
- [Short (type de données)](../../../visual-basic/language-reference/data-types/short-data-type.md)
