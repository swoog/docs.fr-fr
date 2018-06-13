---
title: Inscrire un assembly de fournisseur côté client
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- registering client-side provider assemblies
- client-side provider assemblies, registering
- UI Automation, registering provider assemblies
- provider assemblies, registering
ms.assetid: a03af4d9-2771-43cc-b07b-d468dca23190
author: Xansky
ms.author: mhopkins
manager: markl
ms.openlocfilehash: 166a2aa72fb718ee38fb6ef964179a6cd112deb3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33400703"
---
# <a name="register-a-client-side-provider-assembly"></a><span data-ttu-id="4d7a5-102">Inscrire un assembly de fournisseur côté client</span><span class="sxs-lookup"><span data-stu-id="4d7a5-102">Register a Client-Side Provider Assembly</span></span>
> [!NOTE]
>  <span data-ttu-id="4d7a5-103">Cette documentation s'adresse aux développeurs .NET Framework qui souhaitent utiliser les classes [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] managées définies dans l'espace de noms <xref:System.Windows.Automation>.</span><span class="sxs-lookup"><span data-stu-id="4d7a5-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="4d7a5-104">Pour obtenir les dernières informations sur [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], consultez [API Windows Automation : UI Automation](http://go.microsoft.com/fwlink/?LinkID=156746).</span><span class="sxs-lookup"><span data-stu-id="4d7a5-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](http://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="4d7a5-105">Cette rubrique montre comment inscrire une DLL qui contient des fournisseurs UI Automation côté client.</span><span class="sxs-lookup"><span data-stu-id="4d7a5-105">This topic shows how to register a DLL that contains client-side UI Automation providers.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4d7a5-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="4d7a5-106">Example</span></span>  
 <span data-ttu-id="4d7a5-107">L’exemple suivant montre comment inscrire un assembly qui contient un fournisseur pour une fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="4d7a5-107">The following example shows how to register an assembly that contains a provider for a console window.</span></span>  
  
 [!code-csharp[UIAClientSideProvider_snip#102](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAClientSideProvider_snip/CSharp/CSClientProgram.cs#102)]
 [!code-vb[UIAClientSideProvider_snip#102](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAClientSideProvider_snip/visualbasic/csclientprogram.vb#102)]  
  
## <a name="see-also"></a><span data-ttu-id="4d7a5-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d7a5-108">See Also</span></span>  
 [<span data-ttu-id="4d7a5-109">Créer un fournisseur UI Automation côté client</span><span class="sxs-lookup"><span data-stu-id="4d7a5-109">Create a Client-Side UI Automation Provider</span></span>](../../../docs/framework/ui-automation/create-a-client-side-ui-automation-provider.md)
