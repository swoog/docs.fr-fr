---
title: Utilisation d'une activité personnalisée
ms.date: 03/30/2017
ms.assetid: 8f356419-681a-4175-ae93-878eee970249
ms.openlocfilehash: 47ddd42168445aa23eaaded6fd19ffe4698e4117
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59973354"
---
# <a name="using-a-custom-activity"></a>Utilisation d'une activité personnalisée
Les activités qui dérivent de la classe <xref:System.Activities.Activity> ou de ses sous-classes peuvent être composées de plus grands workflows, ou créées directement dans le code. Cette rubrique explique comment utiliser des activités personnalisées dans les workflows créés dans le code ou dans le concepteur.  
  
> [!NOTE]
>  Activités personnalisées peuvent être utilisées dans le même projet que celui dans lequel elles sont définies, tant que l’activité personnalisée et l’activité qui l’utilise sont compilées (c.-à-d. chargée par un type d’instanciation généré par le processus de génération) si l’activité de référence est chargée. dynamiquement (par exemple, en utilisant ActivityXAMLServices), puis l’assembly référencé doit être placé dans un autre projet ou le XAML généré par le concepteur doit être modifié manuellement pour y parvenir.  
  
#### <a name="using-a-custom-activity-to-a-workflow-project"></a>Utilisation d'une activité personnalisée dans un projet de workflow  
  
1. Ajoutez une référence du projet hôte au projet de bibliothèque d'activités qui contient l'activité personnalisée.  
  
2. Générez la solution.  
  
3. Pour utiliser l'activité personnalisée dans le concepteur, recherchez l'activité personnalisée dans la boîte à outils, puis faites glisser l'activité sur l'aire du concepteur.  
  
4. Pour utiliser l'activité personnalisée dans le code, ajoutez une instruction Using qui fait référence au projet d'activité personnalisée, puis passez une nouvelle instance de l'activité à <xref:System.Activities.WorkflowInvoker.Invoke%2A>.
