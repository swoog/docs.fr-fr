---
title: 'Procédure : Créer une zone de texte en lecture seule (Windows Forms)'
ms.date: 03/30/2017
helpviewer_keywords:
- TextBox control [Windows Forms], read-only
- read-only text boxes
- text boxes [Windows Forms], read-only
ms.assetid: 60baa9ab-fa57-44ad-bb7c-61b05aa64296
ms.openlocfilehash: be85eedf272e596ceb10e7510b8c99ce6aed0727
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59130726"
---
# <a name="how-to-create-a-read-only-text-box-windows-forms"></a>Procédure : Créer une zone de texte en lecture seule (Windows Forms)
Vous pouvez transformer une zone de texte modifiable Windows Forms en un contrôle en lecture seule. Par exemple, la zone de texte peut afficher une valeur qui est généralement de modification, mais ne peut pas être actuellement, en raison de l’état de l’application.  
  
### <a name="to-create-a-read-only-text-box"></a>Pour créer une zone de texte en lecture seule  
  
1.  Définir le <xref:System.Windows.Forms.TextBox> du contrôle <xref:System.Windows.Forms.TextBoxBase.ReadOnly%2A> propriété `true`. Avec la propriété définie sur `true`, les utilisateurs peuvent toujours faire défiler et mettre en surbrillance du texte dans une zone de texte sans autoriser de modification. Un **copie** commande est fonctionnelle dans une zone de texte, mais **couper** et **coller** commandes ne sont pas.  
  
    > [!NOTE]
    >  Le <xref:System.Windows.Forms.TextBoxBase.ReadOnly%2A> propriété affecte uniquement l’interaction utilisateur au moment de l’exécution. Vous pouvez toujours modifier contenu de zone de texte par programmation au moment de l’exécution en modifiant le <xref:System.Windows.Forms.TextBox.Text%2A> propriété de la zone de texte.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.TextBox>
- [Vue d’ensemble du contrôle TextBox](textbox-control-overview-windows-forms.md)
- [Procédure : contrôler le point d’insertion dans un contrôle TextBox Windows Forms](how-to-control-the-insertion-point-in-a-windows-forms-textbox-control.md)
- [Procédure : créer une zone de texte pour un mot de passe avec le contrôle TextBox Windows Forms](how-to-create-a-password-text-box-with-the-windows-forms-textbox-control.md)
- [Procédure : mettre des guillemets dans une chaîne](how-to-put-quotation-marks-in-a-string-windows-forms.md)
- [Procédure : sélectionner du texte dans le contrôle TextBox Windows Forms](how-to-select-text-in-the-windows-forms-textbox-control.md)
- [Procédure : voir plusieurs lignes dans le contrôle TextBox Windows Forms](how-to-view-multiple-lines-in-the-windows-forms-textbox-control.md)
- [TextBox, contrôle](textbox-control-windows-forms.md)
