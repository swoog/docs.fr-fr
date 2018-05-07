---
title: Vue d'ensemble du contrôle DomainUpDown (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- DomainUpDown
helpviewer_keywords:
- spin button control [Windows Forms], about spin button
- DomainUpDown control [Windows Forms], about DomainUpDown control
ms.assetid: 3f40f9c1-20ad-4331-b9b5-b0127eb36eb3
ms.openlocfilehash: 21d28caf490b008570cbd6280afff3114b0f4bfc
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="domainupdown-control-overview-windows-forms"></a>Vue d'ensemble du contrôle DomainUpDown (Windows Forms)
Windows Forms <xref:System.Windows.Forms.DomainUpDown> contrôle est essentiellement une combinaison d’une zone de texte et une paire de boutons de déplacement vers le haut ou vers le bas dans une liste. Le contrôle affiche et définit une chaîne de texte à partir d’une liste de choix. L’utilisateur peut sélectionner la chaîne en cliquant sur les boutons pour vous déplacer dans une liste de haut et bas, en appuyant sur les touches de direction haut et bas ou en tapant une chaîne qui correspond à un élément dans la liste. Une utilisation possible de ce contrôle est pour la sélection d’éléments dans une liste triée par ordre alphabétique des noms.  
  
> [!NOTE]
>  Pour trier la liste, définissez la <xref:System.Windows.Forms.DomainUpDown.Sorted%2A> propriété `true`.  
  
 La fonction de ce contrôle est très similaire à la zone de liste ou zone de liste modifiable, mais il occupe très peu d’espace.  
  
## <a name="key-properties"></a>Propriétés de clé  
 Les principales propriétés du contrôle sont <xref:System.Windows.Forms.DomainUpDown.Items%2A>, <xref:System.Windows.Forms.UpDownBase.ReadOnly%2A>, et <xref:System.Windows.Forms.DomainUpDown.Wrap%2A>. Le <xref:System.Windows.Forms.DomainUpDown.Items%2A> propriété contient la liste des objets dont les valeurs de texte sont affichées dans le contrôle. Si <xref:System.Windows.Forms.UpDownBase.ReadOnly%2A> a la valeur `false`, le contrôle complète automatiquement le texte tapé par l’utilisateur et l’associe à une valeur dans la liste. Si <xref:System.Windows.Forms.DomainUpDown.Wrap%2A> a la valeur `true`, au-delà du dernier élément de défilement vous dirigera vers le premier élément dans la liste et vice versa. Les principales méthodes du contrôle sont <xref:System.Windows.Forms.DomainUpDown.UpButton%2A> et <xref:System.Windows.Forms.DomainUpDown.DownButton%2A>.  
  
 Ce contrôle affiche uniquement les chaînes de texte. Si vous souhaitez un contrôle qui affiche des valeurs numériques, utilisez le <xref:System.Windows.Forms.NumericUpDown> contrôle. Pour plus d’informations, consultez [vue d’ensemble du contrôle NumericUpDown](../../../../docs/framework/winforms/controls/numericupdown-control-overview-windows-forms.md).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.DomainUpDown>  
 [DomainUpDown, contrôle](../../../../docs/framework/winforms/controls/domainupdown-control-windows-forms.md)
