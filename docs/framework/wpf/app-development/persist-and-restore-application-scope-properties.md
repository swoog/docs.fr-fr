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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59977650"
---
# <a name="how-to-persist-and-restore-application-scope-properties-across-application-sessions"></a><span data-ttu-id="243a2-102">Procédure : Rendre persistantes et restaurer les propriétés de portée application d’une session d’application à l’autre</span><span class="sxs-lookup"><span data-stu-id="243a2-102">How to: Persist and Restore Application-Scope Properties Across Application Sessions</span></span>
<span data-ttu-id="243a2-103">Cet exemple montre comment conserver les propriétés de portée application quand une application s’arrête, et comment restaurer les propriétés de portée application lorsqu’une application est ensuite lancement.</span><span class="sxs-lookup"><span data-stu-id="243a2-103">This example shows how to persist application-scope properties when an application shuts down, and how to restore application-scope properties when an application is next launch.</span></span>  
  
## <a name="example"></a><span data-ttu-id="243a2-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="243a2-104">Example</span></span>  
 <span data-ttu-id="243a2-105">L’application rend persistantes les propriétés de portée application à et les restaure depuis le stockage isolé.</span><span class="sxs-lookup"><span data-stu-id="243a2-105">The application persists application-scope properties to, and restores them from, isolated storage.</span></span> <span data-ttu-id="243a2-106">Le stockage isolé est une zone de stockage protégé qui peut être utilisée en toute sécurité par les applications sans autorisation d’accès de fichier.</span><span class="sxs-lookup"><span data-stu-id="243a2-106">Isolated storage is a protected storage area that can safely be used by applications without file access permission.</span></span>  <span data-ttu-id="243a2-107">Le *App.xaml* fichier définit le `App_Startup` méthode comme gestionnaire pour le <xref:System.Windows.Application.Startup?displayProperty=nameWithType> événement et le `App_Exit` méthode comme un gestionnaire pour la <xref:System.Windows.Application.Exit?displayProperty=nameWithType> événement, comme indiqué dans les lignes en surbrillance le premier exemple.</span><span class="sxs-lookup"><span data-stu-id="243a2-107">The *App.xaml* file defines the `App_Startup` method as the handler for the <xref:System.Windows.Application.Startup?displayProperty=nameWithType> event, and the `App_Exit` method as the handler for the  <xref:System.Windows.Application.Exit?displayProperty=nameWithType> event, as shown in the highlighted lines of the first example.</span></span> <span data-ttu-id="243a2-108">Le deuxième exemple montre une partie de la *App.xaml.cs* et *App.xaml.vb* fichiers qui met en surbrillance le code pour le `App_Startup` (méthode), qui restaure les propriétés de portée application et le `App_Exit` (méthode), qui enregistre les propriétés de portée application.</span><span class="sxs-lookup"><span data-stu-id="243a2-108">The second example shows a portion of the *App.xaml.cs* and *App.xaml.vb* files that highlights the code for the `App_Startup` method, which restores application-scope properties, and the `App_Exit` method, which saves application-scope properties.</span></span>

 [!code-xaml[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesXAML1](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/CSharp/App.xaml?highlight=1-7)]
  
 [!code-csharp[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesCODEBEHIND1](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/CSharp/App.xaml.cs?highlight=17-55)]
 [!code-vb[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesCODEBEHIND1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/visualbasic/application.xaml.vb#persistrestoreappscopepropertiescodebehind1)]
