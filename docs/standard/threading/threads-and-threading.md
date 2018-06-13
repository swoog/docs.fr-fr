---
title: Threads et threading
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- multiple threads
- threading [.NET Framework]
- threading [.NET Framework], multiple threads
ms.assetid: 5baac3aa-e603-4fa6-9f89-0f2c1084e6b1
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4380c509a08ebe59f9561a9e6fc596458768917f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33592182"
---
# <a name="threads-and-threading"></a>Threads et threading
Les systèmes d’exploitation utilisent des processus pour séparer les différentes applications qu’ils exécutent. Les threads sont l’unité de base à laquelle un système d’exploitation alloue du temps processeur, et plusieurs threads peuvent exécuter du code au sein de ce processus. Chaque thread maintient des gestionnaires d’exceptions, une priorité de planification et un ensemble de structures utilisé par le système pour enregistrer le contexte du thread jusqu'à sa planification. Le contexte du thread comprend toutes les informations dont le thread a besoin pour reprendre l’exécution sans interruption, notamment son ensemble de registres d’UC et de pile, dans l’espace d’adressage de son processus hôte.  
  
 .NET Framework subdivise chaque processus de système d’exploitation en plusieurs sous-processus gérés et légers, appelés domaines d’application et représentés par <xref:System.AppDomain?displayProperty=nameWithType>. Un ou plusieurs threads managés (représentés par <xref:System.Threading.Thread?displayProperty=nameWithType>) peuvent s’exécuter dans un ou plusieurs domaines d’application, au sein du même processus géré. Bien que chaque domaine d’application démarre avec un seul thread, le code qu’il contient permet de créer des domaines d’application et des threads supplémentaires. Par conséquent, un thread managé peut se déplacer librement entre les domaines d’application d’un même processus géré ; il est possible de n’avoir qu’un seul thread qui évolue entre différents domaines d’application.  
  
 Un système d’exploitation qui prend en charge le mode multitâche préemptif produit l’effet d’une exécution simultanée de plusieurs threads provenant de plusieurs processus. Pour cela, il répartit le temps processeur disponible entre les threads qui en ont besoin, en allouant une tranche de temps à chaque thread les uns après les autres. Le thread en cours d’exécution est suspendu lorsque sa tranche de temps est écoulée et un autre thread reprend l’exécution. Lorsque le système passe d’un thread à un autre, il enregistre le contexte du thread préempté et recharge le contexte enregistré du thread suivant dans la file d’attente de threads.  
  
 La longueur de chaque tranche de temps dépend du système d’exploitation et du processeur. Dans la mesure où elle est petite, plusieurs threads semblent s’exécuter en même temps, même s’il n’y a qu’un processeur. C’est le cas sur les systèmes multiprocesseurs, où les threads exécutables sont distribués entre les processeurs disponibles.  
  
## <a name="when-to-use-multiple-threads"></a>Quand utiliser plusieurs threads  
 Les logiciels qui nécessitent l’intervention de l’utilisateur doivent réagir aussi vite que possible aux activités de l’utilisateur pour offrir une expérience utilisateur riche. Il doit cependant effectuer en même temps les calculs nécessaires pour présenter les données à l’utilisateur aussi rapidement que possible. Si votre application utilise un seul thread d’exécution, vous pouvez combiner la [programmation asynchrone](../../../docs/standard/asynchronous-programming-patterns/calling-synchronous-methods-asynchronously.md) avec la [communication à distance .NET Framework](https://msdn.microsoft.com/library/eccb1d31-0a22-417a-97fd-f4f1f3aa4462) ou des [services web XML](https://msdn.microsoft.com/library/1e64af78-d705-4384-b08d-591a45f4379c) créés à l’aide d’ASP.NET pour utiliser le temps de traitement d’autres ordinateurs en plus des vôtres afin d’augmenter la réactivité vis-à-vis de l’utilisateur et de réduire le temps de traitement des données de votre application. Si vous effectuez des opérations riches en entrées/sorties, vous pouvez également utiliser des ports d’achèvement d’E/S pour accroître la rapidité de réaction de votre application.  
  
### <a name="advantages-of-multiple-threads"></a>Avantages des threads multiples  
 L’utilisation de plusieurs threads, toutefois, est la technique la plus puissante qui soit pour augmenter la réactivité vis-à-vis de l’utilisateur et traiter les données nécessaires pour effectuer le travail presque en même temps. Sur un ordinateur doté d’un seul processeur, plusieurs threads peuvent créer cet effet, en tirant parti des courts laps de temps entre les événements utilisateur pour traiter les données en arrière-plan. Par exemple, un utilisateur peut modifier une feuille de calcul tandis qu’un autre thread recalcule d’autres parties de cette feuille de calcul au sein de la même application.  
  
 Sans modification, la même application augmenterait considérablement la satisfaction utilisateur si elle s’exécutait sur un ordinateur doté de plusieurs processeurs. Votre domaine d’application unique pourrait utiliser plusieurs threads pour accomplir les tâches suivantes :  
  
-   communiquer sur un réseau, avec un serveur web et une base de données ;  
  
-   effectuer des opérations qui prennent beaucoup de temps ;  
  
-   différencier des tâches de priorités différentes (par exemple, un thread prioritaire gère les tâches soumises à des contraintes de temps, et un thread de priorité inférieure effectue d’autres tâches) ;  
  
-   autoriser l’interface utilisateur à rester réactive, tout en allouant du temps aux tâches en arrière-plan.  
  
### <a name="disadvantages-of-multiple-threads"></a>Inconvénients des threads multiples  
 Il est recommandé d’utiliser aussi peu de threads que possible, afin de limiter l’exploitation des ressources du système d’exploitation et d’améliorer les performances. Le threading est également soumis à des critères de ressources ; par ailleurs, il faut prendre en considération les conflits potentiels au moment de concevoir une application. Voici les exigences en matière de ressources :  
  
-   Le système utilise la mémoire pour les informations de contexte requises par les processus, les objets **AppDomain** et les threads. Par conséquent, le nombre de processus, d’objets **AppDomain** et de threads qu’il est possible de créer est limité par la mémoire disponible.  
  
-   Le fait de suivre un grand nombre de threads consomme un temps processeur non négligeable. S’il y a trop de threads, la plupart d'entre eux progresseront à peine. Si la majorité des threads en cours se trouvent dans un même processus, les threads des autres processus sont planifiés à une fréquence moindre.  
  
-   Il est difficile de contrôler l’exécution du code avec de nombreux threads, qui peut être source de nombreux bogues.  
  
-   Détruire des threads implique de savoir ce qui pourrait se produire et de gérer ces problèmes.  
  
 L’accès partagé aux ressources risque de créer des conflits. Pour les éviter, il faut synchroniser ou contrôler l’accès aux ressources partagées. À défaut d’une synchronisation appropriée (dans le même domaine d’application ou non), des problèmes peuvent survenir, par exemple, des blocages (deux threads cessent de répondre, chacun dans l’attente que l’autre se termine) et des conditions de concurrence (un résultat anormal se produit en raison d’une dépendance critique inattendue à la synchronisation de deux événements). Le système fournit des objets de synchronisation permettant de coordonner le partage de ressources entre différents threads. La réduction du nombre de threads facilite la synchronisation des ressources.  
  
 Les ressources suivantes nécessitent une synchronisation :  
  
-   ressources système (p. ex., ports de communication) ;  
  
-   ressources partagées par plusieurs processus (p. ex., descripteurs de fichiers) ;  
  
-   ressources d’un seul domaine d’application (p. ex., champs globaux, statiques et d’instance) auxquelles accèdent plusieurs threads.  
  
### <a name="threading-and-application-design"></a>Threading et de conception d’applications  
 En général, la classe <xref:System.Threading.ThreadPool> représente le moyen le plus simple de gérer plusieurs threads pour des tâches relativement courtes qui ne bloquent pas d’autres threads et si vous ne prévoyez aucune planification particulière des tâches. Toutefois, il y a différentes raisons de créer ses propres threads :  
  
-   Vous voulez qu’une tâche ait une priorité particulière.  
  
-   L’exécution d’une tâche risque de prendre longtemps (ce qui bloquerait d’autres tâches).  
  
-   Vous devez placer des threads dans un thread unique cloisonné (tous les threads **ThreadPool** se trouvent dans le multithread cloisonné).  
  
-   Vous avez besoin d’une identité stable associée au thread. Par exemple, vous devez utiliser un thread dédié pour abandonner ce thread, le suspendre ou l’identifier par son nom.  
  
-   Si vous avez besoin d’exécuter des threads d’arrière-plan qui interagissent avec l’interface utilisateur, la version 2.0 de .NET Framework fournit un composant <xref:System.ComponentModel.BackgroundWorker> qui communique à l’aide d’événements, avec un marshaling interthread vers le thread d’interface utilisateur.  
  
### <a name="threading-and-exceptions"></a>Threading et exceptions  
 Ne gérez pas les exceptions dans les threads. En règle générale, les exceptions non prises en charge dans les threads, même d’arrière-plan, mettent fin au processus. Il existe trois exceptions à cette règle :  
  
-   Une <xref:System.Threading.ThreadAbortException> est levée dans un thread, car <xref:System.Threading.Thread.Abort%2A> a été appelé.  
  
-   Une <xref:System.AppDomainUnloadedException> est levée dans un thread, car le domaine d'application est en cours de déchargement.  
  
-   Le common language runtime ou un processus hôte met fin au thread.  
  
 Pour plus d'informations, voir [Exceptions dans les threads managés](../../../docs/standard/threading/exceptions-in-managed-threads.md).  
  
> [!NOTE]
>  Dans les versions 1.0 et 1.1 de .NET Framework, le common language runtime intercepte sans assistance certaines exceptions, par exemple dans les threads de pool. Cela risque d’endommager l'état des applications et de finir par provoquer leur blocage, ce qui peut être très difficile à déboguer.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Threading.ThreadPool>  
 <xref:System.ComponentModel.BackgroundWorker>  
 [Synchronisation des données pour le multithreading](../../../docs/standard/threading/synchronizing-data-for-multithreading.md)  
 [Pool de threads managés](../../../docs/standard/threading/the-managed-thread-pool.md)
