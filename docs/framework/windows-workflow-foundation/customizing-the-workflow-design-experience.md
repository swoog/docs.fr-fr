---
title: Personnalisation de l'expérience de conception de workflow
ms.date: 03/30/2017
helpviewer_keywords:
- extending [WF], Workflow Designer
ms.assetid: 98135077-0f5d-4d16-9337-01094e843537
ms.openlocfilehash: 87b49b025cfb27812933511b76c5a024cde4995a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54680299"
---
# <a name="customizing-the-workflow-design-experience"></a><span data-ttu-id="f0a6e-102">Personnalisation de l'expérience de conception de workflow</span><span class="sxs-lookup"><span data-stu-id="f0a6e-102">Customizing the Workflow Design Experience</span></span>

<span data-ttu-id="f0a6e-103">Les scénarios destinés à la conception d'activités personnalisées et au réhébergement du [!INCLUDE[wfd1](../../../includes/wfd1-md.md)] ont été considérablement simplifiés dans [!INCLUDE[netfx40_short](../../../includes/netfx40-short-md.md)].</span><span class="sxs-lookup"><span data-stu-id="f0a6e-103">The scenarios for designing custom activities and for rehosting the [!INCLUDE[wfd1](../../../includes/wfd1-md.md)] have been greatly simplified in [!INCLUDE[netfx40_short](../../../includes/netfx40-short-md.md)].</span></span> <span data-ttu-id="f0a6e-104">Le développement et le déploiement sont maintenant à la fois plus facile et plus souple.</span><span class="sxs-lookup"><span data-stu-id="f0a6e-104">Development and deployment are now both easier and more flexible.</span></span> <span data-ttu-id="f0a6e-105">La modification d’infrastructure clé est que le nouveau modèle de programmation concepteur activité repose sur Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="f0a6e-105">The key infrastructural change is that the new activity designer programming model is built upon Windows Presentation Foundation (WPF).</span></span> <span data-ttu-id="f0a6e-106">Cela vous permet de définir des concepteurs d'activités de façon déclarative et de réhéberger le [!INCLUDE[wfd2](../../../includes/wfd2-md.md)] dans d'autres applications en toute simplicité.</span><span class="sxs-lookup"><span data-stu-id="f0a6e-106">This gives you the ability to define activity designers declaratively and to rehost the [!INCLUDE[wfd2](../../../includes/wfd2-md.md)] in other applications with comparative easy.</span></span> <span data-ttu-id="f0a6e-107">Lors du réhébergement, un éditeur d'expressions personnalisé peut être développé pour prendre en charge IntelliSense ou un domaine d'expression simplifié.</span><span class="sxs-lookup"><span data-stu-id="f0a6e-107">When rehosting, a custom expression editor can be developed to support IntelliSense or a simplified expression domain.</span></span> <span data-ttu-id="f0a6e-108">L’intégration avec Windows Communication Foundation (WCF) est devenue plus transparente avec l’utilisation des services de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="f0a6e-108">The integration with Windows Communication Foundation (WCF) has become more seamless with use of workflow services.</span></span> <span data-ttu-id="f0a6e-109">Les concepteurs d’activités personnalisées et l’arborescence d’éléments de modèle peuvent être utilisés pour améliorer les expériences au moment du design dans les concepteurs de workflow réhébergés.</span><span class="sxs-lookup"><span data-stu-id="f0a6e-109">Custom activity designers and the Model Item Tree can be used to enhance design time experiences in rehosted workflow designers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f0a6e-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f0a6e-110">In This Section</span></span>

 [<span data-ttu-id="f0a6e-111">Utilisation de concepteurs d’activités et de modèles d’activité personnalisés</span><span class="sxs-lookup"><span data-stu-id="f0a6e-111">Using Custom Activity Designers and Templates</span></span>](../../../docs/framework/windows-workflow-foundation/using-custom-activity-designers-and-templates.md)

 <span data-ttu-id="f0a6e-112">Explique comment créer de nouveaux concepteurs d'activités et modèles d'activité personnalisés.</span><span class="sxs-lookup"><span data-stu-id="f0a6e-112">Describes how to create new custom activity designers and templates.</span></span>

 [<span data-ttu-id="f0a6e-113">Réhébergement du concepteur de flux de travail</span><span class="sxs-lookup"><span data-stu-id="f0a6e-113">Rehosting the Workflow Designer</span></span>](../../../docs/framework/windows-workflow-foundation/rehosting-the-workflow-designer.md)

 <span data-ttu-id="f0a6e-114">Décrit comment ré-héberger le [!INCLUDE[wfd1](../../../includes/wfd1-md.md)] en dehors de Visual Studio et comment afficher les erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="f0a6e-114">Describes how to re-host the [!INCLUDE[wfd1](../../../includes/wfd1-md.md)] outside of Visual Studio and how to display validation errors.</span></span>

 [<span data-ttu-id="f0a6e-115">Utilisation d’un éditeur d’expressions personnalisé</span><span class="sxs-lookup"><span data-stu-id="f0a6e-115">Using a Custom Expression Editor</span></span>](../../../docs/framework/windows-workflow-foundation/using-a-custom-expression-editor.md)

 <span data-ttu-id="f0a6e-116">Décrit comment implémenter un éditeur d’expressions personnalisées à utiliser avec les concepteurs de workflow réhébergés en dehors de Visual Studio 2010.</span><span class="sxs-lookup"><span data-stu-id="f0a6e-116">Describes how to implement a custom expression editor to use with workflow designers rehosted outside of Visual Studio 2010.</span></span>

## <a name="reference"></a><span data-ttu-id="f0a6e-117">Référence</span><span class="sxs-lookup"><span data-stu-id="f0a6e-117">Reference</span></span>

<xref:System.Activities.Presentation.ActivityDesigner>

## <a name="see-also"></a><span data-ttu-id="f0a6e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0a6e-118">See also</span></span>

- [<span data-ttu-id="f0a6e-119">Extension de Windows Workflow Foundation</span><span class="sxs-lookup"><span data-stu-id="f0a6e-119">Extending Windows Workflow Foundation</span></span>](../../../docs/framework/windows-workflow-foundation/extend.md)
- [<span data-ttu-id="f0a6e-120">Concepteur</span><span class="sxs-lookup"><span data-stu-id="f0a6e-120">Designer</span></span>](../../../docs/framework/windows-workflow-foundation/samples/designer.md)
- [<span data-ttu-id="f0a6e-121">Concepteurs d’activités personnalisées</span><span class="sxs-lookup"><span data-stu-id="f0a6e-121">Custom Activity Designers</span></span>](../../../docs/framework/windows-workflow-foundation/samples/custom-activity-designers.md)
- [<span data-ttu-id="f0a6e-122">Réhébergement du concepteur</span><span class="sxs-lookup"><span data-stu-id="f0a6e-122">Designer ReHosting</span></span>](../../../docs/framework/windows-workflow-foundation/samples/designer-rehosting.md)