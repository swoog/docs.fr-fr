---
title: 'Procédure : hériter de contrôles Windows Forms existants'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- inheritance [Windows Forms], Windows Forms custom controls
- custom controls [Windows Forms], inheritance
ms.assetid: 1e1fc8ea-c615-4cf0-a356-16d6df7444ab
ms.openlocfilehash: 788addee7c024577d029626da4aeb86d0ca9076a
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59300526"
---
# <a name="how-to-inherit-from-existing-windows-forms-controls"></a>Procédure : hériter de contrôles Windows Forms existants
Si vous souhaitez étendre les fonctionnalités d’un contrôle existant, vous pouvez créer un contrôle dérivé d’un contrôle existant par héritage. Lorsque vous héritez d’un contrôle existant, vous héritez de toutes les fonctionnalités et propriétés visuelles de ce contrôle. Par exemple, si vous avez créé un contrôle hérité de <xref:System.Windows.Forms.Button>, votre aura l’aspect et le comportement standard <xref:System.Windows.Forms.Button> contrôle. Vous pourrez ensuite étendre ou modifier les fonctionnalités de votre nouveau contrôle en implémentant des méthodes et des propriétés personnalisées. Dans certains cas, vous pouvez également modifier l’apparence visuelle du contrôle hérité en substituant ses <xref:System.Windows.Forms.Control.OnPaint%2A> (méthode).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-create-an-inherited-control"></a>Pour créer un contrôle hérité  
  
1. Créez un projet d’**application Windows Forms**.  
  
2. Dans le menu **Projet**, sélectionnez **Ajouter un nouvel élément**.  
  
     La boîte de dialogue **Ajouter un nouvel élément** s’affiche.  
  
3. Dans la boîte de dialogue **Ajouter un nouvel élément**, double-cliquez sur **Contrôle personnalisé**.  
  
     Un contrôle personnalisé est ajouté à votre projet.  
  
4. Si vous utilisez Visual Basic, en haut de l’**Explorateur de solutions**, cliquez sur **Afficher tous les fichiers**. Développez CustomControl1.vb, puis ouvrez CustomControl1.Designer.vb dans l’éditeur de code.  
  
5. Si vous utilisez C#, ouvrez CustomControl1.cs dans l’éditeur de code.  
  
6. Recherchez la déclaration de classe qui hérite de <xref:System.Windows.Forms.Control>.  
  
7. Remplacez la classe de base par le contrôle dont vous voulez hériter.  
  
     Par exemple, si vous voulez hériter <xref:System.Windows.Forms.Button>, modifiez la déclaration de classe à ce qui suit :  
  
    ```vb  
    Partial Class CustomControl1  
        Inherits System.Windows.Forms.Button  
    ```  
  
    ```csharp  
    public partial class CustomControl1 : System.Windows.Forms.Button  
    ```  
  
8. Si vous utilisez Visual Basic, enregistrez et fermez CustomControl1.Designer.vb. Ouvrez CustomControl1.vb dans l’éditeur de code.  
  
9. Implémentez les méthodes ou propriétés personnalisées que votre contrôle intégrera.  
  
10. Si vous souhaitez modifier l’aspect graphique de votre contrôle, substituez le <xref:System.Windows.Forms.Control.OnPaint%2A> (méthode).  
  
    > [!NOTE]
    >  Substitution de <xref:System.Windows.Forms.Control.OnPaint%2A> vous autorisera pas à modifier l’apparence de tous les contrôles. Les contrôles dont tout la peinture effectuée par Windows (par exemple, <xref:System.Windows.Forms.TextBox>) appellent jamais leur <xref:System.Windows.Forms.Control.OnPaint%2A> (méthode) et n’utiliseront donc jamais le code personnalisé. Reportez-vous à la documentation d’aide pour le contrôle particulier que vous souhaitez modifier pour vérifier si le <xref:System.Windows.Forms.Control.OnPaint%2A> méthode n’est disponible. Pour obtenir la liste de tous les contrôles Windows Forms, consultez [Contrôles à utiliser dans les Windows Forms](controls-to-use-on-windows-forms.md). Si un contrôle n’a pas <xref:System.Windows.Forms.Control.OnPaint%2A> répertorié comme une méthode membre, vous ne pouvez pas modifier son apparence en substituant cette méthode. Pour plus d’informations sur la peinture personnalisée, consultez [Peinture et rendu personnalisés des contrôles](custom-control-painting-and-rendering.md).  
  
    ```vb  
    Protected Overrides Sub OnPaint(ByVal e As _  
       System.Windows.Forms.PaintEventArgs)  
       MyBase.OnPaint(e)  
       ' Insert code to do custom painting.   
       ' If you want to completely change the appearance of your control,  
       ' do not call MyBase.OnPaint(e).  
    End Sub  
    ```  
  
    ```csharp  
    protected override void OnPaint(PaintEventArgs pe)  
    {  
       base.OnPaint(pe);  
       // Insert code to do custom painting.  
       // If you want to completely change the appearance of your control,  
       // do not call base.OnPaint(pe).  
    }  
    ```  
  
11. Enregistrez et testez votre contrôle.  
  
## <a name="see-also"></a>Voir aussi

- [Variétés de contrôles personnalisés](varieties-of-custom-controls.md)
- [Procédure : hériter de la classe Control](how-to-inherit-from-the-control-class.md)
- [Procédure : hériter de la classe UserControl](how-to-inherit-from-the-usercontrol-class.md)
- [Procédure : créer des contrôles pour Windows Forms](how-to-author-controls-for-windows-forms.md)
- [Dépannage des gestionnaires d'événements hérités dans Visual Basic](~/docs/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers.md)
- [Procédure pas à pas : héritage d’un contrôle Windows Forms avec Visual Basic](walkthrough-inheriting-from-a-windows-forms-control-with-visual-basic.md)
- [Procédure pas à pas : Héritage d'un contrôle Windows Forms à l'aide de Visual C#](walkthrough-inheriting-from-a-windows-forms-control-with-visual-csharp.md)
