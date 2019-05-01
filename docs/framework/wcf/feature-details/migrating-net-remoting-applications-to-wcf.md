---
title: Migration d'applications .NET Remoting vers WCF
ms.date: 03/30/2017
helpviewer_keywords:
- ',NET remoting [WCF]'
ms.assetid: 24793465-65ae-4308-8c12-dce4fd12a583
ms.openlocfilehash: 4040fb0ac223f91705a49b733f6a1f42d144068e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62046604"
---
# <a name="migrating-net-remoting-applications-to-wcf"></a><span data-ttu-id="e2fb6-102">Migration d'applications .NET Remoting vers WCF</span><span class="sxs-lookup"><span data-stu-id="e2fb6-102">Migrating .NET Remoting Applications to WCF</span></span>
<span data-ttu-id="e2fb6-103">**Cette rubrique est spécifique à une technologie héritée qui assure la compatibilité descendante avec des applications existantes et n'est pas recommandée en cas de nouveau développement. Les applications distribuées doivent maintenant être développées à l’aide de WCF.**</span><span class="sxs-lookup"><span data-stu-id="e2fb6-103">**This topic is specific to a legacy technology that is retained for backward compatibility with existing applications and is not recommended for new development. Distributed applications should now be developed using WCF.**</span></span>  
  
 <span data-ttu-id="e2fb6-104">Il existe deux façons de tirer parti de WCF avec les applications .NET Remoting existantes : l’intégration et migration.</span><span class="sxs-lookup"><span data-stu-id="e2fb6-104">There are two ways to take advantage of WCF with existing .NET Remoting applications: integration and migration.</span></span> <span data-ttu-id="e2fb6-105">Intégration vous permet d’avoir .NET Remoting 2.0 et WCF en cours d’exécution côte à côte, ce qui vous permet d’exposer les mêmes objets métier sur ces deux technologies simultanément sans avoir à modifier votre code .NET Remoting 2.0 existant.</span><span class="sxs-lookup"><span data-stu-id="e2fb6-105">Integration allows you to have .NET Remoting 2.0 and WCF running side by side, letting you expose the same business objects over both technologies simultaneously without having to modify your existing .NET Remoting 2.0 code.</span></span> <span data-ttu-id="e2fb6-106">L'intégration requiert l'utilisation de [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] 2.0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e2fb6-106">Integration requires that you are running on [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] 2.0 or greater.</span></span> <span data-ttu-id="e2fb6-107">Si vous souhaitez tirer parti des fonctionnalités de WCF et que vous n’avez pas besoin de compatibilité de la communication avec les systèmes Remoting 2.0, vous pouvez migrer votre ensemble du service WCF.</span><span class="sxs-lookup"><span data-stu-id="e2fb6-107">If you want to take advantage of WCF features and do not need wire compatibility with Remoting 2.0 systems, you can migrate your entire service to WCF.</span></span> <span data-ttu-id="e2fb6-108">Migration de .NET Remoting 2.0 vers WCF nécessite des modifications à l’interface de l’objet distant et ses paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="e2fb6-108">Migration from .NET Remoting 2.0 to WCF requires changes to the remote object's interface and its configuration settings.</span></span> <span data-ttu-id="e2fb6-109">Ces deux rubriques couvertes dans [de Remoting vers Windows Communication Foundation](https://go.microsoft.com/fwlink/?LinkId=74403).</span><span class="sxs-lookup"><span data-stu-id="e2fb6-109">Both of these topics are covered in [From Remoting to the Windows Communication Foundation](https://go.microsoft.com/fwlink/?LinkId=74403).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e2fb6-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2fb6-110">See also</span></span>

- [<span data-ttu-id="e2fb6-111">Vue d’ensemble conceptuelle</span><span class="sxs-lookup"><span data-stu-id="e2fb6-111">Conceptual Overview</span></span>](../../../../docs/framework/wcf/conceptual-overview.md)
