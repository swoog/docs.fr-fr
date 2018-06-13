---
title: '&lt;commonBehaviors&gt;'
ms.date: 03/30/2017
ms.assetid: 5260aeca-388d-4e82-94c0-124fa8054cf5
ms.openlocfilehash: 0a9fab68ce240fc37d27c42d9feff969b97f93a1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33350320"
---
# <a name="ltcommonbehaviorsgt"></a><span data-ttu-id="b1146-102">&lt;commonBehaviors&gt;</span><span class="sxs-lookup"><span data-stu-id="b1146-102">&lt;commonBehaviors&gt;</span></span>
<span data-ttu-id="b1146-103">La section `commonBehaviors` peut uniquement être définie dans le fichier machine.config.</span><span class="sxs-lookup"><span data-stu-id="b1146-103">The `commonBehaviors` section can only be defined in the machine.config file.</span></span> <span data-ttu-id="b1146-104">Elle définit deux collections enfants nommées `endpointBehaviors` et `serviceBehaviors`.</span><span class="sxs-lookup"><span data-stu-id="b1146-104">It defines two child collections named `endpointBehaviors` and `serviceBehaviors`.</span></span>  <span data-ttu-id="b1146-105">Chaque collection définit des éléments de comportement consommés respectivement par tous les points de terminaison WCF et les services sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b1146-105">Each collection defines behavior elements consumed by all WCF endpoints and services on the machine respectively.</span></span> <span data-ttu-id="b1146-106">Les comportements définis dans `endpointBehaviors` sont appliqués uniquement aux clients et les comportements définis dans `serviceBehaviors` s'appliquent uniquement aux services.</span><span class="sxs-lookup"><span data-stu-id="b1146-106">Behaviors defined in `endpointBehaviors` are only applied to clients, and behaviors defined in `serviceBehaviors` are only applied to services.</span></span> <span data-ttu-id="b1146-107">Si un comportement est défini dans les sections `commonBehaviors` et `behaviors`, le comportement dans la section `behaviors` a la préférence.</span><span class="sxs-lookup"><span data-stu-id="b1146-107">If a behavior is defined in both `commonBehaviors` and `behaviors` sections, the behavior in the `behaviors` section is given preference.</span></span>
