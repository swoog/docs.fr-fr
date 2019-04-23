---
title: Vue d'ensemble du contrôle Label (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- Label
helpviewer_keywords:
- images [Windows Forms], displaying in labels
- labels
- Label control [Windows Forms], about Label control
ms.assetid: dcad7f44-11b7-4c55-b0c0-d984ade43d7d
ms.openlocfilehash: cc38b0f3ded9e3c2a5a4146eb6bb474921d1e19f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59210085"
---
# <a name="label-control-overview-windows-forms"></a>Vue d'ensemble du contrôle Label (Windows Forms)
Windows Forms <xref:System.Windows.Forms.Label> contrôles sont utilisés pour afficher le texte ou les images qui ne sont pas modifiables par l’utilisateur. Ils sont utilisés pour identifier des objets sur un formulaire — pour décrire ce que fait un contrôle lorsque vous cliquez dessus, par exemple, ou pour afficher des informations en réponse à un événement d’exécution ou dans votre application. Par exemple, vous pouvez utiliser des étiquettes pour ajouter des légendes pour les zones de texte, zones de liste, zones de liste déroulante et ainsi de suite. Vous pouvez également écrire du code qui modifie le texte affiché par une étiquette en réponse aux événements au moment de l’exécution. Par exemple, si votre application prend quelques minutes pour traiter une modification, vous pouvez afficher un message d’état de traitement dans une étiquette.  
  
## <a name="working-with-the-label-control"></a>Utilisation du contrôle d’étiquette  
 Étant donné que le <xref:System.Windows.Forms.Label> contrôle ne peut pas recevoir le focus, il peut également servir à créer des clés d’accès pour d’autres contrôles. Une clé d’accès permet à un utilisateur de sélectionner l’autre contrôle en appuyant sur la touche ALT et la clé d’accès. Pour plus d’informations, consultez [création de clés d’accès rapide pour les contrôles Windows Forms](how-to-create-access-keys-for-windows-forms-controls.md) et [Comment : Créer des clés d’accès avec les contrôles Label Windows Forms](how-to-create-access-keys-with-windows-forms-label-controls.md).  
  
 La légende affichée dans l’étiquette est contenue dans le <xref:System.Windows.Forms.Label.Text%2A> propriété. Le <xref:System.Windows.Forms.Label.TextAlign%2A> propriété vous permet de définir l’alignement du texte dans l’étiquette. Pour plus d'informations, voir [Procédure : Définir le texte affiché par un Windows Forms contrôle](how-to-set-the-text-displayed-by-a-windows-forms-control.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Label>
- [Guide pratique pour Taille d’un contrôle d’étiquette Windows Forms pour s’ajuster à son contenu](how-to-size-a-windows-forms-label-control-to-fit-its-contents.md)
- [Guide pratique pour Créer des clés d’accès avec les contrôles Label Windows Forms](how-to-create-access-keys-with-windows-forms-label-controls.md)
