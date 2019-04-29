---
title: Définition d'une propriété dans les contrôles Windows Forms
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- properties [Windows Forms], defining in code
- custom controls [Windows Forms], defining properties in code
ms.assetid: c2eb8277-a842-4d99-89a9-647b901a0434
ms.openlocfilehash: 905578454b0bc6b5e74202d15c91645fed0fd461
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61780651"
---
# <a name="defining-a-property-in-windows-forms-controls"></a>Définition d'une propriété dans les contrôles Windows Forms
Vous trouverez une vue d’ensemble de propriétés sur la page [Vue d’ensemble des propriétés](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/65zdfbdt(v=vs.120)). Il est important de prendre en compte plusieurs points avant de définir une propriété :  
  
- Vous devez appliquer des attributs aux propriétés que vous définissez. Les attributs spécifient la manière dont le concepteur doit afficher une propriété. Pour plus d’informations, consultez la page [Attributs au moment du design des composants](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/tk67c2t8(v=vs.120)).  
  
- Si la modification de la propriété affecte l’affichage visuel du contrôle, appelez le <xref:System.Windows.Forms.Control.Invalidate%2A> (méthode) (que votre contrôle hérite <xref:System.Windows.Forms.Control>) à partir de la `set` accesseur. <xref:System.Windows.Forms.Control.Invalidate%2A> à son tour appelle la <xref:System.Windows.Forms.Control.OnPaint%2A> (méthode), qui redessine le contrôle. Appels multiples à <xref:System.Windows.Forms.Control.Invalidate%2A> entraîne un appel unique à <xref:System.Windows.Forms.Control.OnPaint%2A> pour plus d’efficacité.  
  
- La bibliothèque de classes .NET Framework fournit des convertisseurs de type pour les types de données courants : entiers, nombres décimaux, valeurs booléennes, etc. L’objectif d’un convertisseur de type consiste généralement à fournir une conversion de chaînes en valeurs (des données de chaîne vers d’autres types de données). Les types de données courants sont associés à des convertisseurs de type par défaut qui convertissent les valeurs en chaînes et les chaînes vers les types de données adéquats. Si vous définissez une propriété d’un type de donnée personnalisé (autrement dit, non standard), il vous faudra appliquer un attribut qui spécifie le convertisseur de type à associer à cette propriété. Vous pouvez également utiliser un attribut pour associer un éditeur de type avec interface utilisateur personnalisé à une propriété. Un éditeur de type avec interface utilisateur fournit une interface utilisateur permettant de modifier un type de données ou une propriété. Par exemple, un sélecteur de couleurs est un éditeur de type avec interface utilisateur. Des exemples d’attributs sont donnés à la fin de cette rubrique.  
  
    > [!NOTE]
    >  S’il n’y a pas de convertisseur de type ou d’éditeur de type avec interface utilisateur disponible pour votre propriété personnalisée, vous pouvez en implémenter un en suivant les instructions de la page [Étendre la prise en charge au moment du design](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/37899azc(v=vs.120)).  
  
 Le fragment de code suivant montre définit une propriété personnalisée nommée `EndColor` pour le contrôle personnalisé `FlashTrackBar`.  
  
```vb  
Public Class FlashTrackBar  
   Inherits Control  
   ...  
   ' Private data member that backs the EndColor property.  
   Private _endColor As Color = Color.LimeGreen  
  
   ' The Category attribute tells the designer to display  
   ' it in the Flash grouping.   
   ' The Description attribute provides a description of  
   ' the property.   
   <Category("Flash"), _  
   Description("The ending color of the bar.")>  _  
   Public Property EndColor() As Color  
      ' The public property EndColor accesses _endColor.  
      Get  
         Return _endColor  
      End Get  
      Set  
         _endColor = value  
         If Not (baseBackground Is Nothing) And showGradient Then  
            baseBackground.Dispose()  
            baseBackground = Nothing  
         End If  
         ' The Invalidate method calls the OnPaint method, which redraws    
         ' the control.  
         Invalidate()  
      End Set  
   End Property  
   ...  
End Class  
```  
  
```csharp  
public class FlashTrackBar : Control {  
   ...  
   // Private data member that backs the EndColor property.  
   private Color endColor = Color.LimeGreen;  
   // The Category attribute tells the designer to display  
   // it in the Flash grouping.   
   // The Description attribute provides a description of  
   // the property.   
   [  
   Category("Flash"),  
   Description("The ending color of the bar.")  
   ]  
   // The public property EndColor accesses endColor.  
   public Color EndColor {  
      get {  
         return endColor;  
      }  
      set {  
         endColor = value;  
         if (baseBackground != null && showGradient) {  
            baseBackground.Dispose();  
            baseBackground = null;  
         }  
         // The Invalidate method calls the OnPaint method, which redraws   
         // the control.  
         Invalidate();  
      }  
   }  
   ...  
}  
```  
  
 Le fragment de code suivant associe un convertisseur de type et un éditeur de type avec interface utilisateur à la propriété `Value`. Dans ce cas `Value` est un entier et possède un convertisseur de type par défaut, mais la <xref:System.ComponentModel.TypeConverterAttribute> attribut s’applique à un convertisseur de type personnalisé (`FlashTrackBarValueConverter`) qui permet au concepteur pour l’afficher sous forme de pourcentage. L’éditeur de type avec interface utilisateur, `FlashTrackBarValueEditor`, permet d’afficher visuellement le pourcentage. Cet exemple montre également que le convertisseur de type ou l’éditeur spécifié par le <xref:System.ComponentModel.TypeConverterAttribute> ou <xref:System.ComponentModel.EditorAttribute> attribut remplace le convertisseur par défaut.  
  
```vb  
<Category("Flash"), _  
TypeConverter(GetType(FlashTrackBarValueConverter)), _  
Editor(GetType(FlashTrackBarValueEditor), _  
GetType(UITypeEditor)), _  
Description("The current value of the track bar.  You can enter an actual value or a percentage.")>  _  
Public ReadOnly Property Value() As Integer  
...  
End Property  
```  
  
```csharp  
[  
Category("Flash"),   
TypeConverter(typeof(FlashTrackBarValueConverter)),  
Editor(typeof(FlashTrackBarValueEditor), typeof(UITypeEditor)),  
Description("The current value of the track bar.  You can enter an actual value or a percentage.")  
]  
public int Value {  
...  
}  
```  
  
## <a name="see-also"></a>Voir aussi

- [Propriétés dans les contrôles Windows Forms](properties-in-windows-forms-controls.md)
- [Définition de valeurs par défaut avec les méthodes ShouldSerialize et Reset](defining-default-values-with-the-shouldserialize-and-reset-methods.md)
- [Événements de modification de propriété](property-changed-events.md)
- [Attributs dans les contrôles Windows Forms](attributes-in-windows-forms-controls.md)
