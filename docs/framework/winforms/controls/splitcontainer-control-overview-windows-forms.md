---
title: Vue d'ensemble du contrôle SplitContainer (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- SplitContainer
helpviewer_keywords:
- SplitContainer control [Windows Forms], about SplitContainer control
ms.assetid: 6de5a5f7-97a5-402d-be6d-7e2785483db5
ms.openlocfilehash: 81898e09ff513043b205cde13378ae24ee755226
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44267199"
---
# <a name="splitcontainer-control-overview-windows-forms"></a>Vue d'ensemble du contrôle SplitContainer (Windows Forms)
Le contrôle Windows Forms <xref:System.Windows.Forms.SplitContainer> peut être considéré comme un composite ; il s'agit de deux panneaux séparés par une barre mobile. Quand le pointeur de la souris est sur la barre, il change de forme pour montrer que la barre est mobile.  
  
> [!IMPORTANT]
>  Dans le **boîte à outils**, <xref:System.Windows.Forms.SplitContainer> contrôle remplace le <xref:System.Windows.Forms.Splitter> contrôle qui existait dans la version précédente de Visual Studio. Il vaut beaucoup mieux utiliser le contrôle <xref:System.Windows.Forms.SplitContainer> que le contrôle <xref:System.Windows.Forms.Splitter>. Le <xref:System.Windows.Forms.Splitter> classe est toujours incluse dans le [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] pour assurer la compatibilité avec les applications existantes, mais nous vous encourageons vivement à utiliser le <xref:System.Windows.Forms.SplitContainer> contrôle pour les nouveaux projets.  
  
 Avec la <xref:System.Windows.Forms.SplitContainer> contrôle, vous pouvez créer des interfaces utilisateur complexes ; souvent, une sélection dans un panneau détermine quels objets sont affichés dans l’autre panneau. Cette disposition est très efficace pour afficher et parcourir des informations. D’avoir deux panneaux vous permet vous agréger des informations dans les zones et la barre, ou « séparateur », permet aux utilisateurs de redimensionner les panneaux.  
  
 Plusieurs <xref:System.Windows.Forms.SplitContainer> contrôle peut également être imbriqué, et de la seconde <xref:System.Windows.Forms.SplitContainer> contrôle orientée horizontalement, pour créer des panneaux inférieur et supérieur.  
  
 N’oubliez pas que le <xref:System.Windows.Forms.SplitContainer> contrôle est accessible par le clavier par défaut ; les utilisateurs peuvent appuyer sur les touches de direction pour déplacer le séparateur si le <xref:System.Windows.Forms.SplitContainer.IsSplitterFixed%2A> propriété est définie sur `false`.  
  
 Le <xref:System.Windows.Forms.SplitContainer.Orientation%2A> propriété de la <xref:System.Windows.Forms.SplitContainer> contrôle détermine la direction du séparateur et non du contrôle lui-même. Par conséquent, lorsque cette propriété a la valeur <xref:System.Windows.Forms.Orientation.Vertical>, le séparateur s’exécute de haut en bas, la création des panneaux gauche et droite.  
  
 En outre, n’oubliez pas que la valeur de la <xref:System.Windows.Forms.SplitContainer.SplitterRectangle%2A> propriété varie selon la valeur de la <xref:System.Windows.Forms.SplitContainer.Orientation%2A> propriété. Pour plus d’informations, consultez <xref:System.Windows.Forms.SplitContainer.SplitterRectangle%2A> propriété.  
  
 Vous pouvez également restreindre la taille et le déplacement de la <xref:System.Windows.Forms.SplitContainer> contrôle. Le <xref:System.Windows.Forms.SplitContainer.FixedPanel%2A> propriété détermine le panneau qui restera la même taille après le <xref:System.Windows.Forms.SplitContainer> contrôle est redimensionné et le <xref:System.Windows.Forms.SplitContainer.IsSplitterFixed%2A> propriété détermine si le séparateur est mobile par le clavier ou la souris.  
  
> [!NOTE]
>  Même si le <xref:System.Windows.Forms.SplitContainer.IsSplitterFixed%2A> propriété est définie sur `true`, le séparateur peut encore être déplacé par programmation ; par exemple, à l’aide de la <xref:System.Windows.Forms.SplitContainer.SplitterDistance%2A> propriété.  
  
 Enfin, chaque panneau de configuration de la <xref:System.Windows.Forms.SplitContainer> contrôle a les propriétés pour déterminer sa taille individuelle.  
  
## <a name="commonly-used-properties-methods-and-events"></a>Propriétés, méthodes et événements couramment utilisés  
  
|Name|Description|  
|----------|-----------------|  
|Propriété <xref:System.Windows.Forms.SplitContainer.FixedPanel%2A>|Détermine le panneau qui restera la même taille après le <xref:System.Windows.Forms.SplitContainer> contrôle est redimensionné.|  
|Propriété <xref:System.Windows.Forms.SplitContainer.IsSplitterFixed%2A>|Détermine si le séparateur peut être déplacé par le clavier ou la souris.|  
|Propriété <xref:System.Windows.Forms.SplitContainer.Orientation%2A>|Détermine si le séparateur est disposé verticalement ou horizontalement.|  
|Propriété <xref:System.Windows.Forms.SplitContainer.SplitterDistance%2A>|Détermine la distance en pixels en partant du bord gauche ou supérieur à la barre de fractionnement mobile.|  
|Propriété <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A>|Détermine la distance minimale, en pixels, que le séparateur peut être déplacé par l’utilisateur.|  
|Propriété <xref:System.Windows.Forms.SplitContainer.SplitterWidth%2A>|Détermine l’épaisseur, en pixels, du séparateur.|  
|<xref:System.Windows.Forms.SplitContainer.SplitterMoving> Événement|Se produit lorsque le séparateur se déplace.|  
|<xref:System.Windows.Forms.SplitContainer.SplitterMoved> Événement|Se produit lorsque le séparateur a été déplacé.|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.SplitContainer>  
 [SplitContainer, contrôle](../../../../docs/framework/winforms/controls/splitcontainer-control-windows-forms.md)  
 [Exemple de contrôle SplitContainer](https://msdn.microsoft.com/library/9015fad0-7108-4d85-a83a-a72d038c4f65)
