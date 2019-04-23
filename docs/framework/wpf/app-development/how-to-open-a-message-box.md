---
title: 'Procédure : Ouvrir une boîte de message'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- message boxes [WPF], opening
- opening message boxes [WPF]
ms.assetid: acaad17f-af43-4eca-a004-f1c9e7c6f292
ms.openlocfilehash: cf7534cdee5e17d53e95294573023d660135e395
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59101105"
---
# <a name="how-to-open-a-message-box"></a>Procédure : Ouvrir une boîte de message
Cet exemple montre comment ouvrir une boîte de message.  
  
## <a name="example"></a>Exemple  
 Une boîte de message est une boîte de dialogue modale préfabriquée pour afficher des informations pour les utilisateurs. Une boîte de message est ouverte en appelant la méthode statique <xref:System.Windows.MessageBox.Show%2A> méthode de la <xref:System.Windows.MessageBox> classe. Lorsque <xref:System.Windows.MessageBox.Show%2A> est appelée, le message est passé à l’aide d’un paramètre de chaîne. Plusieurs surcharges de <xref:System.Windows.MessageBox.Show%2A> vous permettent de configurer l’apparence d’une boîte de message (voir <xref:System.Windows.MessageBox>).  
  
 [!code-csharp[MessageBoxSnippets#MessageBoxShow1CODE](~/samples/snippets/csharp/VS_Snippets_Wpf/MessageBoxSnippets/CSharp/Show1Window.xaml.cs#messageboxshow1code)]
 [!code-vb[MessageBoxSnippets#MessageBoxShow1CODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MessageBoxSnippets/visualbasic/show1window.xaml.vb#messageboxshow1code)]  
  
## <a name="see-also"></a>Voir aussi

- [MessageBox, exemple](https://go.microsoft.com/fwlink/?LinkID=160023)
