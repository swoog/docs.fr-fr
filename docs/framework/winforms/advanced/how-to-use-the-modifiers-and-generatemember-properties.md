---
title: 'Procédure : utiliser les modificateurs et les propriétés GenerateMember'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
f1_keywords:
- Designer_GenerateMember
- Designer_Modifiers
helpviewer_keywords:
- base forms
- inheritance [Windows Forms], forms
- inherited forms [Windows Forms], Windows Forms
- inherited forms
- form inheritance
- Windows Forms, inheritance
ms.assetid: 3381a5e4-e1a3-44e2-a765-a0b758937b85
ms.openlocfilehash: 6194ef288bd43267c2b00fa6d7c6250e90b37c75
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61778857"
---
# <a name="how-to-use-the-modifiers-and-generatemember-properties"></a>Procédure : utiliser les modificateurs et les propriétés GenerateMember
Lorsque vous placez un composant sur un formulaire Windows, les deux propriétés sont fournies par l’environnement de conception : `GenerateMember` et `Modifiers`. Le `GenerateMember` propriété spécifie quand le Concepteur de formulaires Windows génère une variable membre pour un composant. Le `Modifiers` propriété est le modificateur d’accès assigné à cette variable de membre. Si la valeur de la `GenerateMember` propriété est `false`, la valeur de la `Modifiers` propriété n’a aucun effet.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-specify-whether-a-component-is-a-member-of-the-form"></a>Pour spécifier si un composant est un membre du formulaire  
  
1. Dans le Concepteur de formulaires Windows, ouvrez votre formulaire.  
  
2. Ouvrez le **boîte à outils**et sur le formulaire, placez trois <xref:System.Windows.Forms.Button> contrôles.  
  
3. Définir le `GenerateMember` et `Modifiers` propriétés pour chaque <xref:System.Windows.Forms.Button> contrôle conformément au tableau suivant.  
  
    |Nom du bouton|Valeur de GenerateMember|Valeur de modificateurs|  
    |-----------------|--------------------------|---------------------|  
    |`button1`|`true`|`private`|  
    |`button2`|`true`|`protected`|  
    |`button3`|`false`|Aucune modification|  
  
4. Générez la solution.  
  
5. Dans l’**Explorateur de solutions**, cliquez sur le bouton **Afficher tous les fichiers**.  
  
6. Ouvrez le **Form1** nœud, puis, dans le **éditeur de Code**, ouvrez le **Form1.Designer.vb** ou **Form1.Designer.cs** fichier. Ce fichier contient le code émis par le Concepteur de formulaires Windows.  
  
7. Trouver les déclarations pour les trois boutons. L’exemple de code suivant montre les différences spécifiées par le `GenerateMember` et `Modifiers` propriétés.  
  
     [!code-csharp[System.Windows.Forms.GenerateMember#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.GenerateMember/CS/Form1.cs#3)]
     [!code-vb[System.Windows.Forms.GenerateMember#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.GenerateMember/VB/Form1.vb#3)]  
  
     [!code-csharp[System.Windows.Forms.GenerateMember#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.GenerateMember/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.GenerateMember#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.GenerateMember/VB/Form1.vb#2)]  
  
> [!NOTE]
>  Par défaut, le Concepteur de formulaires Windows attribue le `private` (`Friend` en Visual Basic) modificateur aux contrôles conteneur comme <xref:System.Windows.Forms.Panel>. Si votre base de <xref:System.Windows.Forms.UserControl> ou <xref:System.Windows.Forms.Form> a un contrôle conteneur, il n’acceptera pas de nouveaux enfants dans les formulaires et contrôles hérités. La solution consiste à modifier le modificateur du contrôle conteneur de base à `protected` ou `public`.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Button>
- [Héritage visuel des Windows Forms](windows-forms-visual-inheritance.md)
- [Procédure pas à pas : Démonstration de l’héritage visuel](walkthrough-demonstrating-visual-inheritance.md)
- [Guide pratique pour Hériter des Windows Forms](how-to-inherit-windows-forms.md)
