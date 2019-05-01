---
title: DomainUpDown, contrôle (Windows Forms)
ms.date: 03/30/2017
helpviewer_keywords:
- DomainUpDown control [Windows Forms]
- spin button control [Windows Forms], up-down controls
- up-down controls
- spin button control
- up-down controls [Windows Forms], spin button controls
ms.assetid: fb7cf017-e931-4a95-9d21-8caee4ee122a
ms.openlocfilehash: 83d674e3fb7ff7e715b75c635b891cd4e9703a21
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61972053"
---
# <a name="domainupdown-control-windows-forms"></a>DomainUpDown, contrôle (Windows Forms)
Les formulaires Windows <xref:System.Windows.Forms.DomainUpDown> contrôle ressemble à une combinaison d’une zone de texte et deux boutons de déplacement vers le haut ou vers le bas dans une liste. Le contrôle affiche et définit une chaîne de texte à partir d’une liste de choix. L’utilisateur peut sélectionner la chaîne en cliquant sur les boutons pour vous déplacer dans une liste haut et bas ou en appuyant sur les touches de direction haut et bas, en tapant une chaîne qui correspond à un élément dans la liste. Une utilisation possible pour ce contrôle est pour la sélection d’éléments dans une liste de noms triés par ordre alphabétique. (Pour trier la liste, définissez la <xref:System.Windows.Forms.DomainUpDown.Sorted%2A> propriété `true`.) La fonction de ce contrôle est très similaire à la zone de liste ou une zone de liste déroulante, mais il occupe très peu d’espace.  
  
 Les principales propriétés du contrôle sont <xref:System.Windows.Forms.DomainUpDown.Items%2A>, <xref:System.Windows.Forms.UpDownBase.ReadOnly%2A>, et <xref:System.Windows.Forms.DomainUpDown.Wrap%2A>. Le <xref:System.Windows.Forms.DomainUpDown.Items%2A> propriété contient la liste des objets dont les valeurs texte sont affichés dans le contrôle. Si <xref:System.Windows.Forms.UpDownBase.ReadOnly%2A> est défini sur `false`, le contrôle complète automatiquement le texte tapé par l’utilisateur et correspond à une valeur dans la liste. Si <xref:System.Windows.Forms.DomainUpDown.Wrap%2A> est défini sur `true`, le défilement au-delà du dernier élément vous dirigera vers le premier élément dans la liste et vice versa. Les principales méthodes du contrôle sont <xref:System.Windows.Forms.DomainUpDown.UpButton%2A> et <xref:System.Windows.Forms.DomainUpDown.DownButton%2A>.  
  
 Ce contrôle affiche uniquement les chaînes de texte. Si vous souhaitez un contrôle qui affiche des valeurs numériques, utilisez le <xref:System.Windows.Forms.NumericUpDown> contrôle. Pour plus d’informations, consultez [contrôle NumericUpDown](numericupdown-control-windows-forms.md) .  
  
## <a name="in-this-section"></a>Dans cette section  
 [Vue d’ensemble du contrôle DomainUpDown](domainupdown-control-overview-windows-forms.md)  
 Présente les concepts généraux de le <xref:System.Windows.Forms.DomainUpDown> contrôle, ce qui permet aux utilisateurs de parcourir et sélectionner à partir d’une liste de chaînes de texte.  
  
 [Guide pratique pour Ajouter des éléments à des contrôles DomainUpDown Windows Forms par programmation](how-to-add-items-to-windows-forms-domainupdown-controls-programmatically.md)  
 Explique comment spécifier les chaînes de texte le <xref:System.Windows.Forms.DomainUpDown> contrôle doit afficher.  
  
 [Guide pratique pour Supprimer des éléments dans des contrôles DomainUpDown Windows Forms](how-to-remove-items-from-windows-forms-domainupdown-controls.md)  
 Décrit comment supprimer des éléments à partir de la <xref:System.Windows.Forms.DomainUpDown> contrôle dans le code.  
  
## <a name="reference"></a>Référence  
 <xref:System.Windows.Forms.DomainUpDown>  
 Décrit cette classe et fournit des liens vers tous ses membres.  
  
 <xref:System.Windows.Forms.NumericUpDown>  
 Décrit cette classe et propose des liens vers tous ses membres...  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Contrôles à utiliser dans les Windows Forms](controls-to-use-on-windows-forms.md)  
 Fournit une liste complète de contrôles Windows Forms, avec des liens vers des informations sur leur utilisation.
