---
title: Méthodes de sélection du contrôle Button Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- Button control [Windows Forms], selecting
ms.assetid: fe2fc058-5118-4f70-b264-6147d64a7a8d
ms.openlocfilehash: 86ef0da37ec35b991557af97a97bc9ca3da2d68c
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57717256"
---
# <a name="ways-to-select-a-windows-forms-button-control"></a>Méthodes de sélection du contrôle Button Windows Forms
Un contrôle button Windows Forms peut être sélectionné comme suit :  
  
-   Utilisez une souris pour cliquer sur le bouton.  
  
-   Appeler le bouton <xref:System.Windows.Forms.Control.Click> événement dans le code.  
  
-   Déplacer le focus sur le bouton en appuyant sur la touche TAB, puis choisissez le bouton en appuyant sur la touche espace ou entrée.  
  
-   Appuyez sur la touche d’accès rapide (ALT + la lettre soulignée) pour le bouton. Pour plus d’informations sur les clés d’accès, consultez [Comment : Créer des clés d’accès pour les contrôles de Windows Forms](how-to-create-access-keys-for-windows-forms-controls.md).  
  
-   Si le bouton est le bouton « accepter » du formulaire, en appuyant sur entrée choisit le bouton, même si un autre contrôle a le focus, sauf si ce contrôle est un autre bouton, une zone de texte multiligne ou un contrôle personnalisé qui intercepte la touche ENTRÉE.  
  
-   Si le bouton est le bouton « cancel » du formulaire, en appuyant sur ÉCHAP choisit le bouton, même si un autre contrôle a le focus.  
  
-   Appelez le <xref:System.Windows.Forms.Button.PerformClick%2A> méthode afin de sélectionner le bouton par programme.  
  
## <a name="see-also"></a>Voir aussi
- [Vue d'ensemble du contrôle Button](button-control-overview-windows-forms.md)
- [Guide pratique pour Répondre aux clics de bouton Windows Forms](how-to-respond-to-windows-forms-button-clicks.md)
- [Button, contrôle](button-control-windows-forms.md)
