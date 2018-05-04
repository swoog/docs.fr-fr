---
title: '&lt;commonBehaviors&gt;'
ms.date: 03/30/2017
ms.assetid: 5260aeca-388d-4e82-94c0-124fa8054cf5
ms.openlocfilehash: aaf89f73b6de250aaa572b8fef31e5a1ebd5482b
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltcommonbehaviorsgt"></a>&lt;commonBehaviors&gt;
La section `commonBehaviors` peut uniquement être définie dans le fichier machine.config. Elle définit deux collections enfants nommées `endpointBehaviors` et `serviceBehaviors`.  Chaque collection définit des éléments de comportement consommés respectivement par tous les points de terminaison et services de [!INCLUDE[indigo2](../../../../../includes/indigo2-md.md)] sur l'ordinateur. Les comportements définis dans `endpointBehaviors` sont appliqués uniquement aux clients et les comportements définis dans `serviceBehaviors` s'appliquent uniquement aux services. Si un comportement est défini dans les sections `commonBehaviors` et `behaviors`, le comportement dans la section `behaviors` a la préférence.
