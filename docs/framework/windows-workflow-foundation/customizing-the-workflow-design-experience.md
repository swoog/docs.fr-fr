---
title: Personnalisation de l'expérience de conception de workflow
ms.date: 03/30/2017
helpviewer_keywords:
- extending [WF], Workflow Designer
ms.assetid: 98135077-0f5d-4d16-9337-01094e843537
ms.openlocfilehash: 2d6ef24d00baa4df6dfc8e0af69c1d489b79a41f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61945988"
---
# <a name="customizing-the-workflow-design-experience"></a>Personnalisation de l'expérience de conception de workflow

Les scénarios destinés à la conception d'activités personnalisées et au réhébergement du [!INCLUDE[wfd1](../../../includes/wfd1-md.md)] ont été considérablement simplifiés dans [!INCLUDE[netfx40_short](../../../includes/netfx40-short-md.md)]. Le développement et le déploiement sont maintenant à la fois plus facile et plus souple. La modification d’infrastructure clé est que le nouveau modèle de programmation concepteur activité repose sur Windows Presentation Foundation (WPF). Cela vous permet de définir des concepteurs d'activités de façon déclarative et de réhéberger le [!INCLUDE[wfd2](../../../includes/wfd2-md.md)] dans d'autres applications en toute simplicité. Lors du réhébergement, un éditeur d'expressions personnalisé peut être développé pour prendre en charge IntelliSense ou un domaine d'expression simplifié. L’intégration avec Windows Communication Foundation (WCF) est devenue plus transparente avec l’utilisation des services de flux de travail. Les concepteurs d'activités personnalisées et l'arborescence d'éléments de modèle peuvent être utilisés pour améliorer les expériences au moment du design dans les concepteurs de workflow réhébergés.

## <a name="in-this-section"></a>Dans cette section

 [Utilisation de concepteurs d’activités et de modèles d’activité personnalisés](using-custom-activity-designers-and-templates.md)

 Explique comment créer de nouveaux concepteurs d'activités et modèles d'activité personnalisés.

 [Réhébergement du concepteur de flux de travail](rehosting-the-workflow-designer.md)

 Décrit comment ré-héberger le [!INCLUDE[wfd1](../../../includes/wfd1-md.md)] en dehors de Visual Studio et comment afficher les erreurs de validation.

 [Utilisation d’un éditeur d’expressions personnalisé](using-a-custom-expression-editor.md)

 Décrit comment implémenter un éditeur d’expressions personnalisées à utiliser avec les concepteurs de workflow réhébergés en dehors de Visual Studio 2010.

## <a name="reference"></a>Référence

<xref:System.Activities.Presentation.ActivityDesigner>

## <a name="see-also"></a>Voir aussi

- [Extension de Windows Workflow Foundation](extend.md)
- [Concepteur](./samples/designer.md)
- [Concepteurs d’activités personnalisées](./samples/custom-activity-designers.md)
- [Réhébergement du concepteur](./samples/designer-rehosting.md)