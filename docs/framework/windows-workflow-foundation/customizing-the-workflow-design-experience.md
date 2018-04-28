---
title: Personnalisation de l'expérience de conception de workflow
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- extending [WF], Workflow Designer
ms.assetid: 98135077-0f5d-4d16-9337-01094e843537
caps.latest.revision: 13
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 37296298bda514d507b8fe65af516de74289d6a0
ms.sourcegitcommit: 2042de78fcdceebb6b8ac4b7a292b93e8782cbf5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2018
---
# <a name="customizing-the-workflow-design-experience"></a><span data-ttu-id="83396-102">Personnalisation de l'expérience de conception de workflow</span><span class="sxs-lookup"><span data-stu-id="83396-102">Customizing the Workflow Design Experience</span></span>
<span data-ttu-id="83396-103">Les scénarios destinés à la conception d'activités personnalisées et au réhébergement du [!INCLUDE[wfd1](../../../includes/wfd1-md.md)] ont été considérablement simplifiés dans [!INCLUDE[netfx40_short](../../../includes/netfx40-short-md.md)].</span><span class="sxs-lookup"><span data-stu-id="83396-103">The scenarios for designing custom activities and for rehosting the [!INCLUDE[wfd1](../../../includes/wfd1-md.md)] have been greatly simplified in [!INCLUDE[netfx40_short](../../../includes/netfx40-short-md.md)].</span></span> <span data-ttu-id="83396-104">Le développement et le déploiement sont maintenant à la fois plus facile et plus souple.</span><span class="sxs-lookup"><span data-stu-id="83396-104">Development and deployment are now both easier and more flexible.</span></span> <span data-ttu-id="83396-105">La modification apportée à l’infrastructure de clé est que le nouveau modèle de programmation concepteur activité repose sur Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="83396-105">The key infrastructural change is that the new activity designer programming model is built upon Windows Presentation Foundation (WPF).</span></span> <span data-ttu-id="83396-106">Cela vous permet de définir des concepteurs d'activités de façon déclarative et de réhéberger le [!INCLUDE[wfd2](../../../includes/wfd2-md.md)] dans d'autres applications en toute simplicité.</span><span class="sxs-lookup"><span data-stu-id="83396-106">This gives you the ability to define activity designers declaratively and to rehost the [!INCLUDE[wfd2](../../../includes/wfd2-md.md)] in other applications with comparative easy.</span></span> <span data-ttu-id="83396-107">Lors du réhébergement, un éditeur d'expressions personnalisé peut être développé pour prendre en charge IntelliSense ou un domaine d'expression simplifié.</span><span class="sxs-lookup"><span data-stu-id="83396-107">When rehosting, a custom expression editor can be developed to support IntelliSense or a simplified expression domain.</span></span> <span data-ttu-id="83396-108">L'intégration à [!INCLUDE[indigo1](../../../includes/indigo1-md.md)] est devenue plus transparente avec l'utilisation de services de workflow.</span><span class="sxs-lookup"><span data-stu-id="83396-108">The integration with [!INCLUDE[indigo1](../../../includes/indigo1-md.md)] has become more seamless with use of workflow services.</span></span> <span data-ttu-id="83396-109">Les concepteurs d’activités personnalisées et l’arborescence d’éléments de modèle peuvent être utilisés pour améliorer les expériences au moment du design dans les concepteurs de workflow réhébergés.</span><span class="sxs-lookup"><span data-stu-id="83396-109">Custom activity designers and the Model Item Tree can be used to enhance design time experiences in rehosted workflow designers.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="83396-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="83396-110">In This Section</span></span>  
 [<span data-ttu-id="83396-111">Utilisation de concepteurs d’activités et de modèles d’activité personnalisés</span><span class="sxs-lookup"><span data-stu-id="83396-111">Using Custom Activity Designers and Templates</span></span>](../../../docs/framework/windows-workflow-foundation/using-custom-activity-designers-and-templates.md)  
 <span data-ttu-id="83396-112">Explique comment créer de nouveaux concepteurs d'activités et modèles d'activité personnalisés.</span><span class="sxs-lookup"><span data-stu-id="83396-112">Describes how to create new custom activity designers and templates.</span></span>  
  
 [<span data-ttu-id="83396-113">Réhébergement du concepteur de flux de travail</span><span class="sxs-lookup"><span data-stu-id="83396-113">Rehosting the Workflow Designer</span></span>](../../../docs/framework/windows-workflow-foundation/rehosting-the-workflow-designer.md)  
 <span data-ttu-id="83396-114">Explique comment réhéberger le [!INCLUDE[wfd1](../../../includes/wfd1-md.md)] en dehors de Visual Studio et comment afficher les erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="83396-114">Describes how to re-host the [!INCLUDE[wfd1](../../../includes/wfd1-md.md)] outside of Visual Studio and how to display validation errors.</span></span>  
  
 [<span data-ttu-id="83396-115">Utilisation d’un éditeur d’expressions personnalisé</span><span class="sxs-lookup"><span data-stu-id="83396-115">Using a Custom Expression Editor</span></span>](../../../docs/framework/windows-workflow-foundation/using-a-custom-expression-editor.md)  
 <span data-ttu-id="83396-116">Explique comment implémenter un éditeur d'expressions personnalisé à utiliser avec les concepteurs de workflow réhébergés en dehors de [!INCLUDE[vs2010](../../../includes/vs2010-md.md)].</span><span class="sxs-lookup"><span data-stu-id="83396-116">Describes how to implement a custom expression editor to use with workflow designers rehosted outside of [!INCLUDE[vs2010](../../../includes/vs2010-md.md)].</span></span>  
  
## <a name="reference"></a><span data-ttu-id="83396-117">Référence</span><span class="sxs-lookup"><span data-stu-id="83396-117">Reference</span></span>  
 <xref:System.Activities.Presentation.ActivityDesigner>  
  
## <a name="see-also"></a><span data-ttu-id="83396-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83396-118">See Also</span></span>  
 [<span data-ttu-id="83396-119">Extension de Windows Workflow Foundation</span><span class="sxs-lookup"><span data-stu-id="83396-119">Extending Windows Workflow Foundation</span></span>](../../../docs/framework/windows-workflow-foundation/extend.md)  
 [<span data-ttu-id="83396-120">Concepteur</span><span class="sxs-lookup"><span data-stu-id="83396-120">Designer</span></span>](../../../docs/framework/windows-workflow-foundation/samples/designer.md)  
 [<span data-ttu-id="83396-121">Concepteurs d’activités personnalisées</span><span class="sxs-lookup"><span data-stu-id="83396-121">Custom Activity Designers</span></span>](../../../docs/framework/windows-workflow-foundation/samples/custom-activity-designers.md)  
 [<span data-ttu-id="83396-122">Réhébergement du concepteur</span><span class="sxs-lookup"><span data-stu-id="83396-122">Designer ReHosting</span></span>](../../../docs/framework/windows-workflow-foundation/samples/designer-rehosting.md)
