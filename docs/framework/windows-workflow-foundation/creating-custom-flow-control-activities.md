---
title: Création d'activités de contrôle de flux personnalisées
ms.date: 03/30/2017
ms.assetid: 27f409f6-2d1d-4cfb-9765-93eb2ad667d5
ms.openlocfilehash: de1378cc0dd304db37aefd437d1ce6feac9f2ed2
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57724658"
---
# <a name="creating-custom-flow-control-activities"></a>Création d'activités de contrôle de flux personnalisées
Le .Net Framework contient diverses activités de contrôle de flux dont le fonctionnement est similaire à celui de structures de programmation abstraite (telles que <xref:System.Activities.Statements.Flowchart>) ou aux instructions de programmation standard (telles que <xref:System.Activities.Statements.If>). Cette rubrique décrit l’architecture d’un des exemples de projets, [ForEach Non générique](./samples/non-generic-foreach.md).  
  
## <a name="creating-the-custom-class"></a>Création de la classe personnalisée  
 Étant donné que la classe ForEach non générique devra planifier des activités enfants, elle devra dériver de <xref:System.Activities.NativeActivity>, puisque les activités qui dérivent de <xref:System.Workflow.Activities.CodeActivity> ne disposent pas de cette fonctionnalité.  
  
```  
public sealed class ForEach : NativeActivity  
    {  
```  
  
 La classe personnalisée requiert que plusieurs membres stockent les données utilisées par l'activité et fournissent des fonctionnalités permettant d'exécuter les activités enfants de l'activité. Ces membres incluent :  
  
-   `valueEnumerator`: Les éléments non publics <xref:System.Activities.Variable%601> de type <xref:System.Collections.IEnumerator> permet d’itérer sur la collection d’éléments. Ce membre est de type <xref:System.Activities.Variable%601>, car il est utilisé en interne dans l'activité, plutôt qu'un argument ou une propriété publique, qui serait utilisé si cet objet avait une origine externe à l'activité.  
  
-   `OnChildComplete`: Le grand public <xref:System.Activities.CompletionCallback> propriété qui s’exécute lorsque chaque enfant termine l’exécution. Ce membre est défini comme une propriété CLR, puisque sa valeur ne changera pas dans les différentes instances de l'activité.  
  
-   `Values`: La collection d’entrées utilisée pour les itérations de l’activité enfant. Ce membre est de type <xref:System.Activities.InArgument%601>, puisque l'origine des données est extérieure à l'activité, mais le contenu des collection n'est pas supposé changer au cours de l'exécution de l'activité. Si l’activité nécessitait que la fonctionnalité modifie le contenu de cette collection au cours de l’exécution de l’activité (pour ajouter ou supprimer des activités, par exemple), ce membre aurait été défini comme <xref:System.Activities.ActivityAction>, qui aurait ensuite été évalué lors de chaque accès, de sorte que l’activité ait accès aux modifications.  
  
-   `Body`: Ce membre définit l’activité doit être exécuté pour chaque élément dans le `Values` collection. Ce membre est défini comme <xref:System.Activities.ActivityAction> de sorte qu'il est évalué chaque fois qu'on y accède.  
  
-   `Execute`: Cette méthode utilise la `InternalExecute`, `OnForEachComplete`, et `GetStateAndExecute` des membres non publics pour planifier l’exécution et l’affecter au gestionnaire d’achèvement de l’activité enfant défini dans le membre de corps.  
  
-   `CacheMetadata`: Ce membre fournit au runtime les informations nécessaires exécuter l’activité. Par défaut, la méthode `CacheMetadata` d'une activité indique au runtime tous les membres publics de l'activité, mais puisque cette activité utilise des membres privés pour certaines fonctionnalités, elle doit signaler leur existence au runtime de telle sorte qu'il en soit informé. Dans ce cas, la fonction `CacheMetadata` est remplacée afin que le membre `valueEnumerator` soit accessible. Ce membre crée également un argument pour les valeurs de l'activité afin qu'elles puissent être passées dans l'activité au cours de l'exécution.
