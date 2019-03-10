---
title: Propriétés dans les contrôles Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], properties overview (using code)
- controls [Windows Forms], properties
- properties [Windows Forms]
ms.assetid: 2785279b-fb57-4937-8f6b-2050e475db6f
ms.openlocfilehash: e531b80cffabb94d2589383936a425b740c9cc07
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57708910"
---
# <a name="properties-in-windows-forms-controls"></a>Propriétés dans les contrôles Windows Forms
Un contrôle Windows Forms hérite de nombreuses propriétés de la classe de base <xref:System.Windows.Forms.Control?displayProperty=nameWithType>. Ceux-ci incluent des propriétés comme <xref:System.Windows.Forms.Control.Font%2A>, <xref:System.Windows.Forms.Control.ForeColor%2A>, <xref:System.Windows.Forms.Control.BackColor%2A>, <xref:System.Windows.Forms.Control.Bounds%2A>, <xref:System.Windows.Forms.Control.ClientRectangle%2A>, <xref:System.Windows.Forms.Control.DisplayRectangle%2A>, <xref:System.Windows.Forms.Control.Enabled%2A>, <xref:System.Windows.Forms.Control.Focused%2A>, <xref:System.Windows.Forms.Control.Height%2A>, <xref:System.Windows.Forms.Control.Width%2A>, <xref:System.Windows.Forms.Control.Visible%2A>, <xref:System.Windows.Forms.Control.AutoSize%2A>et bien d’autres. Pour plus d’informations sur les propriétés héritées, consultez <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.  
  
 Vous pouvez remplacer les propriétés héritées de votre contrôle, mais aussi définir de nouvelles propriétés.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Définition d’une propriété](defining-a-property-in-windows-forms-controls.md)  
 Explique comment implémenter une propriété pour un composant ou un contrôle personnalisé et comment intégrer la propriété dans l’environnement de conception.  
  
 [Définition de valeurs par défaut avec les méthodes ShouldSerialize et Reset](defining-default-values-with-the-shouldserialize-and-reset-methods.md)  
 Explique comment définir les valeurs de propriété par défaut pour un composant ou un contrôle personnalisé.  
  
 [Événements de modification de propriété](property-changed-events.md)  
 Décrit comment activer les notifications de modification de propriété lorsqu’une valeur de propriété change.  
  
 [Guide pratique pour Exposer les propriétés des contrôles constitutifs](how-to-expose-properties-of-constituent-controls.md)  
 Explique comment exposer les propriétés des contrôles constitutifs d’un contrôle composite personnalisé.  
  
 [Implémentation de méthode dans les contrôles personnalisés](method-implementation-in-custom-controls.md)  
 Décrit comment implémenter des méthodes dans des composants et des contrôles personnalisés.  
  
## <a name="reference"></a>Référence  
 <xref:System.Windows.Forms.UserControl>  
 Décrit la classe de base pour l’implémentation des contrôles composites.  
  
 <xref:System.ComponentModel.TypeConverterAttribute>  
 Décrit l’attribut qui spécifie le <xref:System.ComponentModel.TypeConverter> à utiliser pour un type de propriété personnalisée.  
  
 <xref:System.ComponentModel.EditorAttribute>  
 Décrit l’attribut qui spécifie le <xref:System.Drawing.Design.UITypeEditor> à utiliser pour une propriété personnalisée.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Attributs dans les contrôles Windows Forms](attributes-in-windows-forms-controls.md)  
 Décrit les attributs que vous pouvez appliquer aux propriétés ou aux autres membres de vos composants et contrôles personnalisés.  
  
 [Attributs en mode design pour les composants](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/tk67c2t8(v=vs.120))  
 Répertorie les attributs de métadonnées à appliquer aux composants et aux contrôles pour qu'ils s'affichent correctement au moment du design dans les concepteurs visuels.  
  
 [Extension de la prise en charge au moment du design](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/37899azc(v=vs.120))  
 Décrit comment implémenter des classes telles que les éditeurs et concepteurs qui fournissent la prise en charge au moment du design.
