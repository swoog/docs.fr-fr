---
title: 'Procédure : Rendre persistantes et restaurer les propriétés de portée application d’une session d’application à l’autre'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- application-scope properties [WPF], persisting
- persisting application-scope properties [WPF]
- properties [WPF], persisting
- restoring application-scope properties [WPF]
- properties [WPF], restoring
- application-scope properties [WPF], restoring
ms.assetid: 55d5904a-f444-4eb5-abd3-6bc74dd14226
ms.openlocfilehash: 99b04060d4e7c14313655010dc4fbd5ce1c90487
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59134951"
---
# <a name="how-to-persist-and-restore-application-scope-properties-across-application-sessions"></a>Procédure : Rendre persistantes et restaurer les propriétés de portée application d’une session d’application à l’autre
Cet exemple montre comment conserver les propriétés de portée application quand une application s’arrête, et comment restaurer les propriétés de portée application lorsqu’une application est ensuite lancement.  
  
## <a name="example"></a>Exemple  
 L’application rend persistantes les propriétés de portée application à et les restaure depuis le stockage isolé. Le stockage isolé est une zone de stockage protégé qui peut être utilisée en toute sécurité par les applications sans autorisation d’accès de fichier.  Le *App.xaml* fichier définit le `App_Startup` méthode comme gestionnaire pour le <xref:System.Windows.Application.Startup?displayProperty=nameWithType> événement et le `App_Exit` méthode comme un gestionnaire pour la <xref:System.Windows.Application.Exit?displayProperty=nameWithType> événement, comme indiqué dans les lignes en surbrillance le premier exemple. Le deuxième exemple montre une partie de la *App.xaml.cs* et *App.xaml.vb* fichiers qui met en surbrillance le code pour le `App_Startup` (méthode), qui restaure les propriétés de portée application et le `App_Exit` (méthode), qui enregistre les propriétés de portée application.

 [!code-xaml[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesXAML1](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/CSharp/App.xaml?highlight=1-7)]
  
 [!code-csharp[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesCODEBEHIND1](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/CSharp/App.xaml.cs?highlight=17-55)]
 [!code-vb[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesCODEBEHIND1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/visualbasic/application.xaml.vb#persistrestoreappscopepropertiescodebehind1)]
