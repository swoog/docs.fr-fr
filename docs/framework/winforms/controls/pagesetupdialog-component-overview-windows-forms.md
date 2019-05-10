---
title: Vue d'ensemble du composant PageSetupDialog (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- PageSetupDialog
helpviewer_keywords:
- Page Setup dialog box [Windows Forms], displaying
- PageSetupDialog component
ms.assetid: 791caacb-a5ca-4fca-bad9-1a5721ad697c
ms.openlocfilehash: 989183b6152dfccb6167d89433317cea596d83c5
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211741"
---
# <a name="pagesetupdialog-component-overview-windows-forms"></a>Vue d'ensemble du composant PageSetupDialog (Windows Forms)

Les formulaires Windows <xref:System.Windows.Forms.PageSetupDialog> composant est une boîte de dialogue préconfigurée utilisée pour définir les détails de la page pour l’impression dans les applications Windows. Utilisez-le dans votre application Windows comme une solution simple pour les utilisateurs pour définir les préférences de pages au lieu de configurer votre propre boîte de dialogue. Vous pouvez autoriser les utilisateurs à définir la bordure et des marges, en-têtes et pieds de page et l’orientation portrait ou paysage. En vous appuyant sur des boîtes de dialogue Windows standard, vous pouvez créer des applications dont la fonction de base est immédiatement familière aux utilisateurs.

## <a name="key-properties-and-methods"></a>Méthodes et propriétés de clé

Utilisez le <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> méthode pour afficher la boîte de dialogue au moment de l’exécution. Ce composant a vous pouvez définir les propriétés relatives à une seule page (<xref:System.Drawing.Printing.PrintDocument> classe) ou des documents (<xref:System.Drawing.Printing.PageSettings> classe). En outre, le <xref:System.Windows.Forms.PageSetupDialog> composant peut être utilisé pour déterminer les paramètres d’imprimante spécifiques, qui sont stockés dans le <xref:System.Drawing.Printing.PrinterSettings> classe.

Lorsqu’il est ajouté à un formulaire, le <xref:System.Windows.Forms.PageSetupDialog> composant apparaît dans la barre d’état en bas du Concepteur Windows Forms dans Visual Studio.

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.PageSetupDialog>
- [PageSetupDialog, composant](pagesetupdialog-component-windows-forms.md)
