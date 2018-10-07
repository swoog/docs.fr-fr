---
title: Compteurs de performance WCF
ms.date: 03/30/2017
helpviewer_keywords:
- performance counters [WCF]
ms.assetid: f559b2bd-ed83-4988-97a1-e88f06646609
ms.openlocfilehash: d0ad7ee0bc3ea1d15197e6b8d9888d60b21a2f15
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/07/2018
ms.locfileid: "48846214"
---
# <a name="wcf-performance-counters"></a>Compteurs de performance WCF
Windows Communication Foundation (WCF) inclut un grand ensemble de compteurs de performances pour vous aider à mesurer les performances de votre application.  
  
## <a name="enabling-performance-counters"></a>Activation des compteurs de performance  
 Vous pouvez activer les compteurs de performances pour un service WCF via le fichier de configuration app.config du service WCF comme suit :  
  
```xml  
<configuration>  
    <system.serviceModel>  
        <diagnostics performanceCounters="All" />  
    </system.serviceModel>  
</configuration>  
```  
  
 L'attribut `performanceCounters` peut être configuré pour activer un type spécifique de compteurs de performance. Les valeurs valides sont les suivantes :  
  
-   All : tous les compteurs de catégorie (ServiceModelService, ServiceModelEndpoint et ServiceModelOperation) sont activés.  
  
-   ServiceOnly : seuls les compteurs de catégorie ServiceModelService sont activés. Valeur par défaut.  
  
-   Off : les compteurs de performance ServiceModel* sont désactivés.  
  
 Si vous souhaitez activer les compteurs de performances pour toutes les applications WCF, vous pouvez placer les paramètres de configuration dans le fichier Machine.config.  Veuillez consulter la **augmentation de la taille de mémoire pour les compteurs de performances** section ci-dessous pour plus d’informations sur la configuration de mémoire suffisante pour les compteurs de performances sur votre ordinateur.  
  
 Si vous utilisez des points d’extensibilité WCF tels que les appelants d’opération personnalisé, vous devez aussi émettre vos propres compteurs de performances. Il s’agit, car si vous implémentez un point d’extensibilité, WCF peut ne plus émettre les données de compteur de performances standard dans le chemin d’accès par défaut. Si vous n'implémentez par la prise en charge manuelle des compteurs de performance, il est possible que vous ne voyiez pas les données de compteurs de performance attendues.  
  
 Vous pouvez aussi activer des compteurs de performance dans votre code comme suit.  
  
```  
using System.Configuration;  
using System.ServiceModel.Configuration;  
using System.ServiceModel.Diagnostics;  
Configuration config = ConfigurationManager.OpenExeConfiguration(  
    ConfigurationUserLevel.None);  
ServiceModelSectionGroup sg = ServiceModelSectionGroup.GetSectionGroup(config);  
sg.Diagnostic.PerformanceCounters = PerformanceCounterScope.All;  
config.Save();  
```  
  
## <a name="viewing-performance-data"></a>Affichage des données de performance  
 Pour consulter des données capturées par les compteurs de performance, vous pouvez utiliser l'analyseur de performances (Perfmon.exe) fourni avec Windows. Vous pouvez lancer cet outil en accédant à **Démarrer**, puis cliquez sur **exécuter** et type `perfmon.exe` dans la boîte de dialogue.  
  
> [!NOTE]
>  Les instances de compteur de performance peuvent être diffusées avant le traitement des derniers messages par le répartiteur de point de terminaison. Il se peut alors que les données de performance de certains messages ne soient pas capturées.  
  
## <a name="increasing-memory-size-for-performance-counters"></a>Augmentation de la taille de la mémoire pour les compteurs de performance  
 WCF utilise la mémoire partagée séparée pour ses catégories de compteur de performances.  
  
 Par défaut, la mémoire partagée séparée a pour valeur un quart de la taille de la mémoire globale des compteurs de performance. La mémoire globale des compteurs de performance par défaut est de 524 288 octets. Par conséquent, les trois catégories de compteur de performance WCF ont une taille par défaut d’environ 128 Ko chacune. Selon les caractéristiques d’exécution des applications WCF sur un ordinateur, mémoire de compteur de performance peut être saturée. Dans ce cas, WCF écrit une erreur dans le journal des événements application. Le contenu de l'erreur indique qu'un compteur de performance n'a pas été chargé, et l'entrée contient l'exception « System.InvalidOperationException : mémoire insuffisante pour afficher le fichier des compteurs personnalisés ». Si le suivi est activé au niveau de l'erreur, cette défaillance est également suivie. Si la mémoire de compteur de performance est épuisée, continuer à exécuter vos applications WCF avec les compteurs de performance activés peut entraîner une dégradation des performances. Si vous êtes un administrateur de l'ordinateur, vous devez le configurer pour allouer suffisamment de mémoire afin de prendre en charge le nombre maximal de compteurs de performance pouvant exister à tout moment.  
  
 Vous pouvez modifier la quantité de mémoire de compteur de performances pour les catégories WCF dans le Registre. Pour cela, vous devez ajouter une nouvelle valeur DWORD nommée `FileMappingSize` aux trois emplacements suivants et lui affecter en octets la valeur désirée. Redémarrez votre ordinateur afin que ces modifications prennent effet.  
  
-   HKLM\System\CurrentControlSet\Services\ServiceModelEndpoint 4.0.0.0\Performance  
  
-   HKLM\System\CurrentControlSet\Services\ServiceModelOperation 4.0.0.0\Performance  
  
-   HKLM\System\CurrentControlSet\Services\ServiceModelService 4.0.0.0\Performance  
  
 Lorsqu'un grand nombre d'objets (par exemple, ServiceHost) sont supprimés mais sont en attente d'être récupérés par le garbage collector, le compteur de performance `PrivateBytes` enregistre un nombre exceptionnellement élevé. Pour résoudre ce problème, vous pouvez ajouter vos propres compteurs spécifiques à l'application ou utiliser l'attribut `performanceCounters` pour activer des compteurs au niveau du service uniquement.  
  
## <a name="types-of-performance-counters"></a>Types de compteurs de performance  
 Les compteurs de performance portent sur trois niveaux différents : service, point de terminaison et opération.  
  
 Vous pouvez utiliser WMI pour récupérer le nom d'une instance de compteur de performance. Par exemple :  
  
-   Nom d’instance de compteur de service peut être obtenu via WMI [Service](../../../../../docs/framework/wcf/diagnostics/wmi/service.md) propriété « CounterInstanceName » de l’instance.  
  
-   Nom d’instance de compteur de point de terminaison peut être obtenu via WMI [point de terminaison](../../../../../docs/framework/wcf/diagnostics/wmi/endpoint.md) propriété « CounterInstanceName » de l’instance.  
  
-   Nom d’instance de compteur d’opération peut être obtenu via WMI [point de terminaison](../../../../../docs/framework/wcf/diagnostics/wmi/endpoint.md) méthode « GetOperationCounterInstanceName » de l’instance.  
  
 Pour plus d’informations sur WMI, consultez [à l’aide de Windows Management Instrumentation pour les Diagnostics](../../../../../docs/framework/wcf/diagnostics/wmi/index.md).  
  
### <a name="service-performance-counters"></a>Compteurs de performance de service  
 Les compteurs de performance de service mesurent le comportement du service dans son ensemble et peuvent être utilisés pour diagnostiquer les performances de la totalité du service. Ils se trouvent sous l'objet de performance `ServiceModelService 4.0.0.0` dans l'affichage de l'analyseur de performances. Les instances sont nommées à l'aide du modèle suivant :  
  
```  
ServiceName@ServiceBaseAddress  
```  
  
 Un compteur dans une portée de service est issu du compteur dans une collection de points de terminaison.  
  
 Les compteurs de performance pour la création d'une instance de service sont incrémentés lors de la création d'un nouveau InstanceContext. Notez qu'un nouveau InstanceContext est créé lorsque vous recevez un message de non activation (avec un service existant), ou lorsque vous vous connectez à une instance à partir d'une session, terminez la session puis reconnectez à partir d'une autre session.  
  
### <a name="endpoint-performance-counters"></a>Compteurs de performance de point de terminaison  
 Les compteurs de performance de point de terminaison vous permettent de consulter des données en reflétant la manière dont un point de terminaison accepte des messages. Ils se trouvent sous l'objet de performance `ServiceModelEndpoint 4.0.0.0` dans l'affichage de l'analyseur de performances. Les instances sont nommées à l'aide du modèle suivant :  
  
```  
(ServiceName).(ContractName)@(endpoint listener address)  
```  
  
 Les données sont semblables à celles recueillies pour des opérations individuelles, mais sont regroupées uniquement sur le point de terminaison.  
  
 Un compteur dans une portée de point de terminaison est issu des compteurs dans une collection d'opérations.  
  
> [!NOTE]
>  Si deux points de terminaison ont des noms de contrat et des adresses identiques, ils sont mappés à la même instance de compteur.  
  
### <a name="operation-performance-counters"></a>Compteurs de performance d'opération  
 Les compteurs de performance d'opération se trouvent sous l'objet de performance `ServiceModelOperation 4.0.0.0` dans l'affichage de l'analyseur de performances. Chaque opération a une instance individuelle. Autrement dit, si un contrat donné a 10 opérations, 10 instances de compteur d'opération sont associées à ce contrat. Les instances d'objet sont nommées à l'aide du modèle suivant :  
  
```  
(ServiceName).(ContractName).(OperationName)@(first endpoint listener address)  
```  
  
 Ce compteur vous permet de mesurer la manière dont l'appel est utilisé et comment l'opération s'exécute.  
  
 Lorsque les compteurs sont visibles au niveau de plusieurs portées, les données issues d'une portée supérieure sont regroupées avec les données des portées inférieures. Par exemple, `Calls` à un point de terminaison représente la somme de tous les appels d'opération dans le point de terminaison ; `Calls` à un service représente la somme de tous les appels à tous les points de terminaison dans le service.  
  
> [!NOTE]
>  Si vous avez des noms d'opération en double sur un contrat, vous recevez seulement une instance de compteur pour les deux opérations.  
  
## <a name="programming-the-wcf-performance-counters"></a>Programmation des compteurs de performance WCF  
 Plusieurs fichiers sont installés dans le dossier d’installation SDK afin que vous pouvez accéder par programmation les compteurs de performance WCF. Ces fichiers sont répertoriés comme suit.  
  
-   _ServiceModelEndpointPerfCounters.vrg  
  
-   _ServiceModelOperationPerfCounters.vrg  
  
-   _ServiceModelServicePerfCounters.vrg  
  
-   _SMSvcHostPerfCounters.vrg  
  
-   _TransactionBridgePerfCounters.vrg  
  
 Pour plus d’informations sur la façon d’accéder par programme aux compteurs, consultez [Architecture de programmation de compteur de performances](https://go.microsoft.com/fwlink/?LinkId=95179).  
  
## <a name="see-also"></a>Voir aussi  
 [Administration et diagnostics](../../../../../docs/framework/wcf/diagnostics/index.md)
