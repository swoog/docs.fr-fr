---
title: Créer un fournisseur UI Automation côté client
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- UI Automation, creating client-side provider
- client-side UI Automation provider, creating
ms.assetid: d91edaf2-be28-41ec-a508-af421cb43c3d
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: 76fa74a31e7198d0f380a4db71a4789fd7b0a31a
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47196107"
---
# <a name="create-a-client-side-ui-automation-provider"></a>Créer un fournisseur UI Automation côté client
> [!NOTE]
>  Cette documentation s'adresse aux développeurs .NET Framework qui souhaitent utiliser les classes [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] managées définies dans l'espace de noms <xref:System.Windows.Automation>. Pour plus d’informations sur [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], consultez [Windows Automation API : UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).  
  
 Cette rubrique contient un exemple de code qui montre comment implémenter un fournisseur UI Automation côté client.  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant peut être généré dans une [!INCLUDE[TLA#tla_dll](../../../includes/tlasharptla-dll-md.md)] qui implémente un fournisseur côté client très simple pour une fenêtre de console. Le code ne dispose pas de fonctionnalités utiles, mais il est destiné à présenter les étapes de base de l’installation d’un assembly de fournisseur pouvant être inscrit par une application cliente UI Automation.  
  
 [!code-csharp[UIAClientSideProvider_snip#101](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAClientSideProvider_snip/CSharp/CSProviderProgram.cs#101)]
 [!code-vb[UIAClientSideProvider_snip#101](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAClientSideProvider_snip/visualbasic/csproviderprogram.vb#101)]  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble des fournisseurs UI Automation](../../../docs/framework/ui-automation/ui-automation-providers-overview.md)  
 [Inscrire un assembly de fournisseur côté client](../../../docs/framework/ui-automation/register-a-client-side-provider-assembly.md)
