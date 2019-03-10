---
title: 'Procédure : Exposer les propriétés des contrôles constitutifs'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- user controls [Windows Forms], exposing constituent controls
- controls [Windows Forms], constituent
- custom controls [Windows Forms], exposing properties
- constituent controls
ms.assetid: 5c1ec98b-aa48-4823-986e-4712551cfdf1
ms.openlocfilehash: 75ee93b7a601b4fc1480dca708d78740664c9a85
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57704516"
---
# <a name="how-to-expose-properties-of-constituent-controls"></a>Procédure : Exposer les propriétés des contrôles constitutifs
Les contrôles qui composent un contrôle composite sont appelés *contrôles constitutifs*. Ces contrôles sont normalement déclarés privés et est donc pas accessible par le développeur. Si vous souhaitez rendre les propriétés de ces contrôles accessibles aux utilisateurs de futures, vous devez les exposer à l’utilisateur. Pour exposer une propriété d’un contrôle qui le composent en créant une propriété dans le contrôle utilisateur et à l’aide de la `get` et `set` accesseurs pour répercuter la modification dans la propriété privée du contrôle constitutif.  
  
 Envisagez d’un contrôle utilisateur hypothétique avec un bouton qui le composent nommé `MyButton`. Dans cet exemple, lorsque l’utilisateur demande la `ConstituentButtonBackColor` propriété, la valeur stockée dans le <xref:System.Windows.Forms.Control.BackColor%2A> propriété du `MyButton` est remis. Lorsque l’utilisateur assigne une valeur à cette propriété, cette valeur est automatiquement passée à la <xref:System.Windows.Forms.Control.BackColor%2A> propriété du `MyButton` et `set` code s’exécutera, changez la couleur du `MyButton`.  
  
 L’exemple suivant montre comment exposer les <xref:System.Windows.Forms.Control.BackColor%2A> propriété du bouton constitutif :  
  
```vb  
Public Property ButtonColor() as System.Drawing.Color  
   Get  
      Return MyButton.BackColor  
   End Get  
   Set(Value as System.Drawing.Color)  
      MyButton.BackColor = Value  
   End Set  
End Property  
```  
  
```csharp  
public Color ButtonColor  
{  
   get  
   {  
      return(myButton.BackColor);  
   }  
   set  
   {  
      myButton.BackColor = value;  
   }  
}  
```  
  
### <a name="to-expose-a-property-of-a-constituent-control"></a>Pour exposer une propriété de contrôle constitutif  
  
1.  Créez une propriété publique pour votre contrôle utilisateur.  
  
2.  Dans la `get` section de la propriété, écrivez du code qui Récupère la valeur de la propriété que vous souhaitez exposer.  
  
3.  Dans la `set` section de la propriété, écrivez du code qui transmet la valeur de la propriété à la propriété exposée du contrôle constitutif.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.UserControl>
- [Propriétés dans les contrôles Windows Forms](properties-in-windows-forms-controls.md)
- [Variétés de contrôles personnalisés](varieties-of-custom-controls.md)
