---
title: Contrôles dessinés par l'utilisateur
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [Windows Forms], user-drawn
- OnPaint method [Windows Forms]
- user-drawn controls [Windows Forms]
ms.assetid: 034af4b5-457f-4160-a937-22891817faa8
ms.openlocfilehash: e9eab78695db128c0538914c5364aaa54c135403
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54509959"
---
# <a name="user-drawn-controls"></a>Contrôles dessinés par l'utilisateur
Le .NET Framework vous offre la possibilité de développer facilement vos propres contrôles. Vous pouvez créer un contrôle utilisateur, qui est un ensemble de contrôles standard liés ensemble par le code, ou vous pouvez concevoir votre propre contrôle de bout en bout des. Vous pouvez même utiliser l’héritage pour créer un contrôle qui hérite d’un contrôle existant et ajouter ses fonctionnalités inhérentes. N’importe quelle approche que vous utilisez, le .NET Framework fournit la fonctionnalité permettant de dessiner une interface graphique personnalisée pour n’importe quel contrôle que vous créez.  
  
 Peinture d’un contrôle s’effectue par l’exécution de code dans le contrôle <xref:System.Windows.Forms.Control.OnPaint%2A> (méthode). L’argument unique de la <xref:System.Windows.Forms.Control.OnPaint%2A> méthode est un <xref:System.Windows.Forms.PaintEventArgs> objet qui fournit toutes les informations et les fonctionnalités nécessaires au rendu de votre contrôle. Le <xref:System.Windows.Forms.PaintEventArgs> fournit en tant que propriétés de deux objets principal qui seront utilisés dans le rendu de votre contrôle :  
  
-   <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> objet - le rectangle qui représente la partie du contrôle qui sera dessinée. Cela peut être l’ensemble du contrôle, ou une partie du contrôle en fonction de la façon dont le contrôle est dessiné.  
  
-   <xref:System.Drawing.Graphics> objet - encapsule plusieurs méthodes qui fournissent les fonctionnalités nécessaires pour dessiner votre contrôle et les objets graphiques.  
  
 Pour plus d’informations sur la <xref:System.Drawing.Graphics> objet et comment l’utiliser, consultez [Comment : Créer des objets graphiques pour le dessin](../../../../docs/framework/winforms/advanced/how-to-create-graphics-objects-for-drawing.md).  
  
 Le <xref:System.Windows.Forms.Control.OnPaint%2A> événement est déclenché chaque fois que le contrôle est dessiné ou actualisé à l’écran et le <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> objet représente le rectangle dans lequel le dessin est effectué. Si le contrôle entier doit être actualisé, le <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> représente la taille de l’ensemble du contrôle. Si une seule partie du contrôle doit être actualisé, toutefois, le <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> objet représente uniquement la région qui doit être redessiné. Un exemple de ce cas serait lorsqu’un contrôle a été partiellement obscurci par un autre contrôle ou formulaire dans l’interface utilisateur.  
  
 Lorsque vous héritez du <xref:System.Windows.Forms.Control> (classe), vous devez substituer la <xref:System.Windows.Forms.Control.OnPaint%2A> méthode et fournir le code de rendu du graphique. Si vous souhaitez fournir une interface graphique personnalisée à un contrôle utilisateur ou un contrôle hérité, vous pouvez également le faire en substituant la <xref:System.Windows.Forms.Control.OnPaint%2A> (méthode). Voici un exemple :  
  
```vb  
Protected Overrides Sub OnPaint(ByVal e As PaintEventArgs)  
   ' Call the OnPaint method of the base class.  
   MyBase.OnPaint(e)  
  
   ' Declare and instantiate a drawing pen.  
   Using myPen As System.Drawing.Pen = New System.Drawing.Pen(Color.Aqua)  
      ' Draw an aqua rectangle in the rectangle represented by the control.  
      e.Graphics.DrawRectangle(myPen, New Rectangle(Me.Location, Me.Size))  
   End Using
End Sub  
```  
  
```csharp  
protected override void OnPaint(PaintEventArgs e)  
{  
   // Call the OnPaint method of the base class.  
   base.OnPaint(e);  
  
   // Declare and instantiate a new pen.  
   using (System.Drawing.Pen myPen = new System.Drawing.Pen(Color.Aqua))  
   {
      // Draw an aqua rectangle in the rectangle represented by the control.  
      e.Graphics.DrawRectangle(myPen, new Rectangle(this.Location,   
         this.Size));  
   }
}  
```  
  
 L’exemple précédent montre comment restituer un contrôle avec une représentation graphique très simple. Il appelle le <xref:System.Windows.Forms.Control.OnPaint%2A> méthode de la classe de base, il crée un <xref:System.Drawing.Pen> de l’objet avec lequel dessiner et dessine une ellipse dans le rectangle déterminé par le <xref:System.Windows.Forms.Control.Location%2A> et <xref:System.Windows.Forms.Control.Size%2A> du contrôle. Bien que la plupart du code rendu sera considérablement plus complexe que celui-ci, cet exemple illustre l’utilisation de la <xref:System.Drawing.Graphics> objet contenu dans le <xref:System.Windows.Forms.PaintEventArgs> objet. Notez que si vous héritez d’une classe possédant déjà une représentation graphique, tel que <xref:System.Windows.Forms.UserControl> ou <xref:System.Windows.Forms.Button>et vous ne souhaitez pas insérer dans votre rendu, vous ne devez pas appeler votre classe de base <xref:System.Windows.Forms.Control.OnPaint%2A> méthode.  
  
 Le code dans le <xref:System.Windows.Forms.Control.OnPaint%2A> méthode de votre contrôle s’exécute lorsque le contrôle est dessiné, puis chaque fois qu’il est actualisé. Pour vous assurer que votre contrôle est redessiné chaque fois qu’il est redimensionné, ajoutez la ligne suivante au constructeur de votre contrôle :  
  
```vb  
SetStyle(ControlStyles.ResizeRedraw, True)  
```  
  
```csharp  
SetStyle(ControlStyles.ResizeRedraw, true);  
```  
  
> [!NOTE]
>  Utilisez le <xref:System.Windows.Forms.Control.Region%2A?displayProperty=nameWithType> propriété pour implémenter un contrôle non rectangulaire.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.Control.Region%2A>
- <xref:System.Windows.Forms.ControlStyles>
- <xref:System.Drawing.Graphics>
- <xref:System.Windows.Forms.Control.OnPaint%2A>
- <xref:System.Windows.Forms.PaintEventArgs>
- [Guide pratique pour Créer des objets graphiques pour le dessin](../../../../docs/framework/winforms/advanced/how-to-create-graphics-objects-for-drawing.md)
- [Contrôles constitutifs](../../../../docs/framework/winforms/controls/constituent-controls.md)
- [Variétés de contrôles personnalisés](../../../../docs/framework/winforms/controls/varieties-of-custom-controls.md)
