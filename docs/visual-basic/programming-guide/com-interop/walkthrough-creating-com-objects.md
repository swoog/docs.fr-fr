---
title: 'Procédure pas à pas : Création d’objets COM avec Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- COM interop [Visual Basic], creating COM objects
- COM objects, creating
- COM interop [Visual Basic], walkthroughs
- object creation [Visual Basic], COM objects
- COM objects, walkthroughs
ms.assetid: 7b07a463-bc72-4392-9ba0-9dfcb697a44f
ms.openlocfilehash: 6b079db3ccc07494bdfdf7dba49c27fe14dca4e5
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56973936"
---
# <a name="walkthrough-creating-com-objects-with-visual-basic"></a>Procédure pas à pas : Création d’objets COM avec Visual Basic
Lorsque vous créez de nouvelles applications ou composants, il est préférable de créer des assemblys .NET Framework. Toutefois, Visual Basic facilite également l’exposition d’un composant .NET Framework à COM. Cela vous permet de fournir de nouveaux composants pour des suites d’applications antérieures qui requièrent des composants COM. Cette procédure pas à pas montre comment utiliser Visual Basic pour exposer [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] objets en tant qu’objets COM, avec et sans le modèle de classe COM.  
  
 Pour exposer des objets COM, le plus simple consiste à l’aide du modèle de classe COM. Le modèle de classe COM crée une nouvelle classe, puis configure votre projet pour générer la couche d’interopérabilité et de la classe en tant qu’objet COM et l’inscrire auprès du système d’exploitation.  
  
> [!NOTE]
>  Bien que vous pouvez également exposer une classe créée dans Visual Basic en tant qu’objet COM pour le code non managé à utiliser, il n’est pas un véritable objet COM et ne peut pas être utilisé par Visual Basic. Pour plus d’informations, consultez [interopérabilité COM dans les Applications .NET Framework](../../../visual-basic/programming-guide/com-interop/com-interoperability-in-net-framework-applications.md).  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-a-com-object-by-using-the-com-class-template"></a>Pour créer un objet COM en utilisant le modèle de classe COM  
  
1.  Ouvrez un nouveau projet d’Application de Windows à partir de la **fichier** menu en cliquant sur **nouveau projet**.  
  
2.  Dans le **nouveau projet** boîte de dialogue sous la **Types de projets** champ, vérifiez que Windows est sélectionné. Sélectionnez **bibliothèque de classes** à partir de la **modèles** liste, puis cliquez sur **OK**. Le nouveau projet s’affiche.  
  
3.  Sélectionnez **ajouter un nouvel élément** à partir de la **projet** menu. La boîte de dialogue **Ajouter un nouvel élément** s’affiche.  
  
4.  Sélectionnez **classe COM** à partir de la **modèles** liste, puis cliquez sur **ajouter**. Visual Basic ajoute une nouvelle classe et configure le nouveau projet pour COM interop.  
  
5.  Ajoutez le code telles que les propriétés, méthodes et événements à la classe COM.  
  
6.  Sélectionnez **générer ClassLibrary1** à partir de la **Build** menu. Visual Basic génère l’assembly et inscrit l’objet COM avec le système d’exploitation.  
  
## <a name="creating-com-objects-without-the-com-class-template"></a>Création d’objets COM sans le modèle de classe COM  
 Vous pouvez également créer une classe COM manuellement au lieu de l’aide du modèle de classe COM. Cette procédure est utile quand vous travaillez à partir de la ligne de commande ou lorsque vous souhaitez mieux contrôler la façon dont les objets COM sont définies.  
  
#### <a name="to-set-up-your-project-to-generate-a-com-object"></a>Pour configurer votre projet pour générer un objet COM  
  
1.  Ouvrez un nouveau projet d’Application de Windows à partir de la **fichier** menu en cliquant sur **NewProject**.  
  
2.  Dans le **nouveau projet** boîte de dialogue sous la **Types de projets** champ, vérifiez que Windows est sélectionné. Sélectionnez **bibliothèque de classes** à partir de la **modèles** liste, puis cliquez sur **OK**. Le nouveau projet s’affiche.  
  
3.  Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis cliquez sur **Propriétés**. Le **Concepteur de projets** s’affiche.  
  
4.  Cliquez sur l’onglet **Compiler**.  
  
5.  Sélectionnez le **inscrire pour COM Interop** case à cocher.  
  
#### <a name="to-set-up-the-code-in-your-class-to-create-a-com-object"></a>Pour définir le code dans votre classe pour créer un objet COM  
  
1.  Dans **l’Explorateur de solutions**, double-cliquez sur **Class1.vb** pour afficher son code.  
  
2.  Renommez la classe `ComClass1`.  
  
3.  Ajoutez les constantes suivantes à `ComClass1`. Ils stockera les constantes de l’identificateur global Unique (GUID) qui les objets COM sont nécessaires pour avoir.  
  
     [!code-vb[VbVbalrInterop#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrInterop/VB/Class1.vb#2)]  
  
4.  Dans le menu **Outils**, cliquez sur **Créer un Guid**. Dans la boîte de dialogue **Créer un Guid**, cliquez sur **Format du Registre**, puis sur **Copier**. Cliquez sur **Quitter**.  
  
5.  Remplacez la chaîne vide pour la `ClassId` avec le GUID, supprimer le caractère de début et de fin une accolade. Par exemple, si le GUID fourni par Guidgen est `"{2C8B0AEE-02C9-486e-B809-C780A11530FE}"` puis votre code doit se présenter comme suit.  
  
     [!code-vb[VbVbalrInterop#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrInterop/VB/Class1.vb#3)]  
  
6.  Répétez les étapes précédentes pour le `InterfaceId` et `EventsId` constantes, comme dans l’exemple suivant.  
  
     [!code-vb[VbVbalrInterop#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrInterop/VB/Class1.vb#4)]  
  
    > [!NOTE]
    >  Assurez-vous que les GUID sont nouveaux et uniques ; Sinon, votre composant COM pourrait être en conflit avec d’autres composants.  
  
7.  Ajouter le `ComClass` attribut `ComClass1`, en spécifiant les GUID pour l’ID de classe, les ID d’Interface et les ID d’événements comme dans l’exemple suivant :  
  
     [!code-vb[VbVbalrInterop#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrInterop/VB/Class1.vb#5)]  
  
8.  Les classes COM doivent avoir un sans paramètre `Public Sub New()` constructeur ou la classe n’inscrira pas correctement. Ajoutez un constructeur sans paramètre à la classe :  
  
     [!code-vb[VbVbalrInterop#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrInterop/VB/Class1.vb#6)]  
  
9. Ajoutez des propriétés, méthodes et événements à la classe, en terminant par un `End Class` instruction. Sélectionnez **générer la Solution** à partir de la **Build** menu. Visual Basic génère l’assembly et inscrit l’objet COM avec le système d’exploitation.  
  
    > [!NOTE]
    >  Les objets COM que vous générez avec Visual Basic ne peut pas être utilisés par d’autres applications Visual Basic, car ils ne sont pas des objets COM trues. Tente d’ajouter des références à ces objets COM déclenchera une erreur. Pour plus d’informations, consultez [interopérabilité COM dans les Applications .NET Framework](../../../visual-basic/programming-guide/com-interop/com-interoperability-in-net-framework-applications.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.ComClassAttribute>
- [COM Interop](../../../visual-basic/programming-guide/com-interop/index.md)
- [Procédure pas à pas : Implémentation de l’héritage avec les objets COM](../../../visual-basic/programming-guide/com-interop/walkthrough-implementing-inheritance-with-com-objects.md)
- [#Region (directive)](../../../visual-basic/language-reference/directives/region-directive.md)
- [Interopérabilité COM dans les applications .NET Framework](../../../visual-basic/programming-guide/com-interop/com-interoperability-in-net-framework-applications.md)
- [Dépannage des problèmes liés à l’interopérabilité](../../../visual-basic/programming-guide/com-interop/troubleshooting-interoperability.md)
