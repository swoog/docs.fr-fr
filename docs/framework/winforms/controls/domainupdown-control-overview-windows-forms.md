---
title: Vue d'ensemble du contrôle DomainUpDown (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- DomainUpDown
helpviewer_keywords:
- spin button control [Windows Forms], about spin button
- DomainUpDown control [Windows Forms], about DomainUpDown control
ms.assetid: 3f40f9c1-20ad-4331-b9b5-b0127eb36eb3
ms.openlocfilehash: bfe3e7239f77c6f1a0d9bb46a96c704653b43364
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61972066"
---
# <a name="domainupdown-control-overview-windows-forms"></a>Vue d'ensemble du contrôle DomainUpDown (Windows Forms)
Les formulaires Windows <xref:System.Windows.Forms.DomainUpDown> contrôle est essentiellement une combinaison d’une zone de texte et deux boutons de déplacement vers le haut ou vers le bas dans une liste. Le contrôle affiche et définit une chaîne de texte à partir d’une liste de choix. L’utilisateur peut sélectionner la chaîne en cliquant sur les boutons pour vous déplacer dans une liste haut et bas ou en appuyant sur les touches de direction haut et bas, en tapant une chaîne qui correspond à un élément dans la liste. Une utilisation possible pour ce contrôle est pour la sélection d’éléments dans une liste de noms triés par ordre alphabétique.  
  
> [!NOTE]
>  Pour trier la liste, définissez la <xref:System.Windows.Forms.DomainUpDown.Sorted%2A> propriété `true`.  
  
 La fonction de ce contrôle est très similaire à la zone de liste ou une zone de liste déroulante, mais il occupe très peu d’espace.  
  
## <a name="key-properties"></a>Propriétés de clé  
 Les principales propriétés du contrôle sont <xref:System.Windows.Forms.DomainUpDown.Items%2A>, <xref:System.Windows.Forms.UpDownBase.ReadOnly%2A>, et <xref:System.Windows.Forms.DomainUpDown.Wrap%2A>. Le <xref:System.Windows.Forms.DomainUpDown.Items%2A> propriété contient la liste des objets dont les valeurs texte sont affichés dans le contrôle. Si <xref:System.Windows.Forms.UpDownBase.ReadOnly%2A> est défini sur `false`, le contrôle complète automatiquement le texte tapé par l’utilisateur et correspond à une valeur dans la liste. Si <xref:System.Windows.Forms.DomainUpDown.Wrap%2A> est défini sur `true`, le défilement au-delà du dernier élément vous dirigera vers le premier élément dans la liste et vice versa. Les principales méthodes du contrôle sont <xref:System.Windows.Forms.DomainUpDown.UpButton%2A> et <xref:System.Windows.Forms.DomainUpDown.DownButton%2A>.  
  
 Ce contrôle affiche uniquement les chaînes de texte. Si vous souhaitez un contrôle qui affiche des valeurs numériques, utilisez le <xref:System.Windows.Forms.NumericUpDown> contrôle. Pour plus d’informations, consultez [vue d’ensemble du contrôle NumericUpDown](numericupdown-control-overview-windows-forms.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DomainUpDown>
- [DomainUpDown, contrôle](domainupdown-control-windows-forms.md)
