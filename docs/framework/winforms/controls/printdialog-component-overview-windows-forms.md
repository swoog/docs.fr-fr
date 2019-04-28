---
title: Vue d'ensemble du composant PrintDialog (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- PrintDialog
helpviewer_keywords:
- Print dialog box [Windows Forms], displaying
- PrintDialog component [Windows Forms], about PrintDialog component
ms.assetid: 8327b8ac-1017-4b5e-a88b-fea9dd56999c
ms.openlocfilehash: 982c52dbe9243e69bbb0452513e78798f4d1fd0d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61903407"
---
# <a name="printdialog-component-overview-windows-forms"></a>Vue d'ensemble du composant PrintDialog (Windows Forms)
Les formulaires Windows [PrintDialog](printdialog-component-windows-forms.md) composant est une boîte de dialogue préconfigurée utilisée pour sélectionner une imprimante, choisir les pages à imprimer et déterminer les autres paramètres d’impression dans les applications Windows. Utilisez-le comme un moyen simple de sélectionner une imprimante ou des paramètres d'impression au lieu de configurer votre propre boîte de dialogue. Vous pouvez autoriser les utilisateurs à imprimer de nombreuses parties de leurs documents : imprimer tout, imprimer une plage de pages sélectionnées ou imprimer une sélection. En vous appuyant sur des boîtes de dialogue Windows standard, vous pouvez créer des applications dont la fonction de base est immédiatement familière aux utilisateurs. Le <xref:System.Windows.Forms.PrintDialog> composant hérite de la <xref:System.Windows.Forms.CommonDialog> classe.  
  
## <a name="working-with-the-component"></a>Utilisation du composant  
 Utilisez le <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> méthode pour afficher la boîte de dialogue au moment de l’exécution. Ce composant possède des propriétés relatives à un seul travail d’impression (<xref:System.Drawing.Printing.PrintDocument> classe) ou les paramètres d’une imprimante spécifique (<xref:System.Drawing.Printing.PrinterSettings> classe). Dans ce cas, peut à son tour, être partagé par plusieurs imprimantes.  
  
 Lorsqu’il est ajouté à un formulaire, le <xref:System.Windows.Forms.PrintDialog> composant apparaît dans la barre d’état en bas du Concepteur Windows Forms.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.PrintDialog>
- [PrintDialog, composant](printdialog-component-windows-forms.md)
