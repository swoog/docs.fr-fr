---
title: Pointeurs de souris dans les Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- pointers [Windows Forms], setting
- mouse pointers
- mouse cursors
- mouse pointers [Windows Forms], setting
- cursors [Windows Forms], setting
- mouse [Windows Forms], cursors
ms.assetid: c3400d85-de5b-42e8-abc3-d6088d69ee53
ms.openlocfilehash: c018986498bfbd7e492c3e7a26c94e0baa0576d5
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57712732"
---
# <a name="mouse-pointers-in-windows-forms"></a>Pointeurs de souris dans les Windows Forms
La souris *pointeur*, qui est parfois appelé curseur, est une bitmap qui spécifie un point de focus sur l’écran de l’utilisateur avec la souris. Cette rubrique fournit une vue d’ensemble du pointeur de la souris dans les Windows Forms et décrit quelques-unes des façons de modifier et de contrôler le pointeur de la souris.  
  
## <a name="accessing-the-mouse-pointer"></a>Le pointeur de la souris de l’accès à  
 Le pointeur de la souris est représenté par le <xref:System.Windows.Forms.Cursor> classe et chacune <xref:System.Windows.Forms.Control> a un <xref:System.Windows.Forms.Control.Cursor%2A?displayProperty=nameWithType> propriété qui spécifie le pointeur pour ce contrôle. Le <xref:System.Windows.Forms.Cursor> classe contient des propriétés qui décrivent le pointeur, tels que le <xref:System.Windows.Forms.Cursor.Position%2A> et <xref:System.Windows.Forms.Cursor.HotSpot%2A> propriétés et méthodes qui peuvent modifier l’apparence du pointeur, telles que la <xref:System.Windows.Forms.Cursor.Show%2A>, <xref:System.Windows.Forms.Cursor.Hide%2A>, et <xref:System.Windows.Forms.Cursor.DrawStretched%2A> méthodes.  
  
## <a name="controlling-the-mouse-pointer"></a>Contrôler le pointeur de la souris  
 Vous pouvez être amené à limiter la zone dans laquelle le pointeur de la souris peut être utilisé ou modifier la position de la souris. Vous pouvez obtenir ou définir l’emplacement actuel de la souris à l’aide de la <xref:System.Windows.Forms.Cursor.Position%2A> propriété de la <xref:System.Windows.Forms.Cursor>. En outre, vous pouvez limiter la zone le pointeur de la souris peut être utilisé s’applique le <xref:System.Windows.Forms.Cursor.Clip%2A> propriété. Par défaut, la zone de découpage est tout l’écran.  
  
## <a name="changing-the-mouse-pointer"></a>Modification du pointeur de la souris  
 Modification du pointeur de la souris est un moyen important de fournir des commentaires à l’utilisateur. Par exemple, le pointeur de la souris peut être modifié dans les gestionnaires de la <xref:System.Windows.Forms.Control.MouseEnter> et <xref:System.Windows.Forms.Control.MouseLeave> événements pour indiquer à l’utilisateur que les calculs sont produisent et de limiter l’interaction utilisateur dans le contrôle. Parfois, le pointeur de la souris change en raison d’événements système, tels que lorsque votre application est impliquée dans une opération de glisser-déplacer.  
  
 Le principal moyen de modifier le pointeur de la souris est en définissant le <xref:System.Windows.Forms.Control.Cursor%2A?displayProperty=nameWithType> ou <xref:System.Windows.Forms.Control.DefaultCursor%2A> propriété d’un contrôle vers un nouveau <xref:System.Windows.Forms.Cursor>. Pour obtenir des exemples de modification du pointeur de la souris, consultez l’exemple de code dans la <xref:System.Windows.Forms.Cursor> classe. En outre, le <xref:System.Windows.Forms.Cursors> classe expose un ensemble de <xref:System.Windows.Forms.Cursor> objets pour de nombreux types de pointeurs, telles qu’un pointeur qui ressemble à une main. Pour afficher le pointeur d’attente, qui ressemble à un sablier, chaque fois que le pointeur de la souris est sur le contrôle, utilisez la <xref:System.Windows.Forms.Control.UseWaitCursor%2A> propriété de la <xref:System.Windows.Forms.Control> classe.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.Cursor>
- [Entrée de la souris dans une application Windows Forms](mouse-input-in-a-windows-forms-application.md)
- [Fonctionnalité de glisser-déposer dans les Windows Forms](drag-and-drop-functionality-in-windows-forms.md)
