---
title: Vue d'ensemble du contrôle LinkLabel (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- LinkLabel
helpviewer_keywords:
- links [Windows Forms], LinkLabel control
- Label control [Windows Forms], about Label control
- LinkLabel control [Windows Forms], about LinkLabel control
ms.assetid: 9e248549-10ca-43a3-bb5e-60f583d369f1
ms.openlocfilehash: 541467b0f1285d372e5f6d502d9d8f28c8c6333e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59083125"
---
# <a name="linklabel-control-overview-windows-forms"></a>Vue d'ensemble du contrôle LinkLabel (Windows Forms)
Les formulaires Windows <xref:System.Windows.Forms.LinkLabel> contrôle vous permet d’ajouter des liens Web dans les applications Windows Forms. Vous pouvez utiliser la <xref:System.Windows.Forms.LinkLabel> contrôle pour tous les éléments que vous pouvez utiliser le <xref:System.Windows.Forms.Label> de contrôle pour ; vous pouvez également définir une partie du texte sous forme de lien à un fichier, un dossier ou une page Web.  
  
## <a name="what-you-can-do-with-the-linklabel-control"></a>Ce que vous pouvez faire avec le contrôle LinkLabel  
 En plus de toutes les propriétés, méthodes et événements de la <xref:System.Windows.Forms.Label> contrôle, le <xref:System.Windows.Forms.LinkLabel> contrôle possède des propriétés pour des liens hypertexte et les couleurs de lien. Le <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> propriété définit la zone de texte qui active le lien. Le <xref:System.Windows.Forms.LinkLabel.LinkColor%2A>, <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A>, et <xref:System.Windows.Forms.LinkLabel.ActiveLinkColor%2A> propriétés définissent les couleurs du lien. Le <xref:System.Windows.Forms.LinkLabel.LinkClicked> événement détermine ce qui se passe lorsque le texte du lien est sélectionné.  
  
 L’utilisation la plus simple du <xref:System.Windows.Forms.LinkLabel> contrôle consiste à afficher un lien unique en utilisant le <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> propriété, mais vous pouvez également afficher plusieurs liens hypertexte à l’aide de la <xref:System.Windows.Forms.LinkLabel.Links%2A> propriété. Le <xref:System.Windows.Forms.LinkLabel.Links%2A> propriété vous permet d’accéder à une collection de liens. Vous pouvez également spécifier des données dans le <xref:System.Windows.Forms.LinkLabel.Link.LinkData%2A> propriété individuelle de chaque <xref:System.Windows.Forms.LinkLabel.Link> objet. La valeur de la <xref:System.Windows.Forms.LinkLabel.Link.LinkData%2A> propriété peut être utilisée pour stocker l’emplacement d’un fichier d’Affichage ou l’adresse d’un site Web.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.LinkLabel>
- [Vue d'ensemble du contrôle Label](label-control-overview-windows-forms.md)
- [Guide pratique pour Lier à un objet ou la Page Web avec un contrôle LinkLabel Windows Forms](link-to-an-object-or-web-page-with-wf-linklabel-control.md)
- [Guide pratique pour Modifier l’apparence du contrôle LinkLabel Windows Forms](how-to-change-the-appearance-of-the-windows-forms-linklabel-control.md)
