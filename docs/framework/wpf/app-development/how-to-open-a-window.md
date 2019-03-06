---
title: 'Procédure : Ouvrez une fenêtre'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- windows [WPF], opening
- opening windows [WPF]
ms.assetid: 6b91b2bb-fda7-491d-a72e-139dd630a5b0
ms.openlocfilehash: 9ce7ffb3f46dd869fda7893745b531bd02d18ee1
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57373567"
---
# <a name="how-to-open-a-window"></a>Procédure : Ouvrez une fenêtre
Cet exemple montre comment ouvrir une fenêtre.  
  
## <a name="example"></a>Exemple  
 Une fenêtre est ouverte en instanciant <xref:System.Windows.Window> et en appelant le <xref:System.Windows.Window.Show%2A> (méthode). <xref:System.Windows.Window.Show%2A> Ouvre une fenêtre et retourne immédiatement sans attendre que la nouvelle fenêtre à fermer. Ce type de fenêtre est également appelé un *non modale* fenêtre et ne restreint pas l’entrée d’utilisateur.  
  
 [!code-csharp[HOWTOWindowManagementSnippets#OpenNewWindowCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/MainWindow.xaml.cs#opennewwindowcode)]
 [!code-vb[HOWTOWindowManagementSnippets#OpenNewWindowCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/mainwindow.xaml.vb#opennewwindowcode)]  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 L’instanciation <xref:System.Windows.Window> nécessite l’autorisation d’appeler des méthodes natives non sécurisées (voir <xref:System.Windows.Window.%23ctor%2A>).
