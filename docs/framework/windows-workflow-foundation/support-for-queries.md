---
title: Prise en charge des requêtes
ms.date: 03/30/2017
ms.assetid: 093c22f5-3294-4642-857a-5252233d6796
ms.openlocfilehash: 30695fcd791a0d69c31a897068d69838c80c3957
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59307949"
---
# <a name="support-for-queries"></a>Prise en charge des requêtes
Le magasin d'instances de workflow SQL enregistre un jeu de propriétés connues dans le magasin. Les utilisateurs peuvent demander des instances à partir de ces propriétés. La liste suivante comprend quelques-unes de ces propriétés connues :  
  
-   **Nom du site.** Nom du site Web qui contient le service.  
  
-   **Chemin d’accès de l’Application relatif.** Chemin d’accès à l’application relatif au site Web.  
  
-   **Chemin d’accès relatif de Service.** Chemin d’accès au service relatif à l’application.  
  
-   **Nom du service.** Nom du service.  
  
-   **Service Namespace.** Nom de l'espace de noms que le service utilise.  
  
-   **Ordinateur actuel.**  
  
-   **Dernier ordinateur**. Ordinateur sur lequel l'instance de service de workflow a été exécutée la dernière fois.  
  
> [!NOTE]
>  Pour les scénarios auto-hébergés à l'aide de l'hôte du service de workflow, seules les quatre dernières propriétés sont remplies. Pour les scénarios d'application de workflow, seule la dernière propriété est remplie.  
  
 Le runtime du workflow fournit des valeurs pour les trois premières propriétés. L’hôte de service de workflow fournit la valeur pour le **raison de l’interruption** propriété. Le Store d’Instance de Workflow SQL lui-même fournit des valeurs pour le **dernier ordinateur mis à jour** propriété.  
  
 La fonctionnalité de magasin d'instances de workflow SQL vous permet également de spécifier les propriétés personnalisées pour lesquelles vous souhaitez stocker les valeurs dans la base de données de persistance et que vous souhaitez utiliser dans les requêtes. Pour plus d’informations sur les promotions personnalisées, consultez [Store extensibilité](store-extensibility.md).  
  
## <a name="views"></a>Affichages  
 Le magasin d'instances contient les vues suivantes. Consultez [schéma de base de données de persistance](persistence-database-schema.md) pour plus d’informations.  
  
### <a name="the-instances-view"></a>Vue Instances  
 La vue Instances contient les champs suivants :  
  
1. **Id**  
  
2. **PendingTimer**  
  
3. **CreationTime**  
  
4. **LastUpdatedTime**  
  
5. **ServiceDeploymentId**  
  
6. **SuspensionExceptionName**  
  
7. **SuspensionReason**  
  
8. **ActiveBookmarks**  
  
9. **CurrentMachine**  
  
10. **LastMachine**  
  
11. **ExecutionStatus**  
  
12. **IsInitialized**  
  
13. **IsSuspended**  
  
14. **IsCompleted**  
  
15. **EncodingOption**  
  
16. **ReadWritePrimitiveDataProperties**  
  
17. **WriteOnlyPrimitiveDataProperties**  
  
18. **ReadWriteComplexDataProperties**  
  
19. **WriteOnlyComplexDataProperties**  
  
### <a name="the-servicedeployments-view"></a>Vue ServiceDeployments  
 La vue ServiceDeployments contient les champs suivants :  
  
1. **SiteName**  
  
2. **RelativeServicePath**  
  
3. **RelativeApplicationPath**  
  
4. **ServiceName**  
  
5. **ServiceNamespace**  
  
### <a name="the-instancepromotedproperties-view"></a>Vue InstancePromotedProperties  
 La vue InstancePromotedProperties contient les champs suivants. Pour plus d’informations sur les propriétés promues, consultez le [Store extensibilité](store-extensibility.md) rubrique.  
  
1. **InstanceId**  
  
2. **EncodingOption**  
  
3. **PromotionName**  
  
4. **Valeur #** (une plage de champs à partir de **Value1** à **Value64**).
