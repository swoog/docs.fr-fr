---
title: Prise en main stockage file d’attente Azure à l’aideF#
description: Files d’attente Azure fournissent une messagerie fiable et asynchrone entre les composants de l’application. Messagerie cloud permet de composants de votre application à l’échelle indépendamment.
author: sylvanc
ms.date: 09/20/2016
ms.openlocfilehash: 58a46dfe905a32be77a13d11df8f0544546ea0ed
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56974274"
---
# <a name="get-started-with-azure-queue-storage-using-f"></a>Prise en main Azure Queue storage à l’aide de F\#

Stockage de file d’attente Azure fournit la messagerie cloud entre les composants d’application. Dans la conception d’applications à grande échelle, les composants d’application sont souvent découplés, afin qu’ils peuvent mettre à l’échelle indépendamment. Stockage file d’attente offre une messagerie asynchrone pour la communication entre les composants d’application, qu’ils soient exécutés dans le cloud, sur le bureau, sur un serveur local ou sur un appareil mobile. Stockage file d’attente prend également en charge la gestion des tâches asynchrones et la création de flux de travail de processus.

### <a name="about-this-tutorial"></a>À propos de ce didacticiel

Ce didacticiel montre comment écrire F# code de certaines tâches courantes à l’aide d’Azure Queue storage. Tâches couvertes incluent la création et suppression de files d’attente et ajout, la lecture et suppression des messages de file d’attente.

Pour obtenir une vue d’ensemble conceptuelle de stockage de file d’attente, consultez [le guide de .NET pour le stockage de file d’attente](/azure/storage/storage-dotnet-how-to-use-queues).

## <a name="prerequisites"></a>Prérequis

Pour utiliser ce guide, vous devez d’abord [créer un compte de stockage Azure](/azure/storage/storage-create-storage-account).
Vous devez également votre clé d’accès de stockage pour ce compte.

## <a name="create-an-f-script-and-start-f-interactive"></a>Créer un F# de Script et démarrer F# Interactive

Les exemples de cet article peuvent être utilisées dans un F# application ou un F# script. Pour créer un F# de script, créez un fichier avec le `.fsx` extension, par exemple `queues.fsx`, dans votre F# environnement de développement.

Ensuite, utilisez un [Gestionnaire de package](package-management.md) comme [Paket](https://fsprojects.github.io/Paket/) ou [NuGet](https://www.nuget.org/) pour installer le `WindowsAzure.Storage` package et référence `WindowsAzure.Storage.dll` dans votre script à l’aide d’un `#r`directive.

### <a name="add-namespace-declarations"></a>Ajoutez les déclarations d’espace de noms

Ajoutez le code suivant `open` instructions au début de la `queues.fsx` fichier :

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L1-L3)]

### <a name="get-your-connection-string"></a>Obtenir votre chaîne de connexion

Vous aurez besoin d’une chaîne de connexion de stockage Azure pour ce didacticiel. Pour plus d’informations sur les chaînes de connexion, consultez [configuration des chaînes de connexion stockage](/azure/storage/storage-configure-connection-string).

Pour ce didacticiel, vous allez entrer votre chaîne de connexion dans votre script, comme suit :

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L9-L9)]

Toutefois, il s’agit de **déconseillé** projets de réel. Votre clé de compte de stockage est similaire au mot de passe racine pour votre compte de stockage. Veillez toujours à protéger votre clé de compte de stockage. Évitez de la communiquer à d’autres utilisateurs, coder en dur, ou l’enregistrer dans un fichier texte brut qui n’est accessible à d’autres personnes. Vous pouvez régénérer votre clé à l’aide du portail Azure si vous pensez qu’il a peut-être été compromise.

Applications de réel, la meilleure façon de conserver votre chaîne de connexion de stockage est dans un fichier de configuration. Pour extraire la chaîne de connexion à partir d’un fichier de configuration, vous pouvez effectuer ceci :

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L11-L13)]

L’utilisation d’Azure Configuration Manager est facultative. Vous pouvez également utiliser une API telle que du .NET Framework `ConfigurationManager` type.

### <a name="parse-the-connection-string"></a>Analyser la chaîne de connexion

Pour analyser la chaîne de connexion, utilisez :

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L19-L20)]

Ceci renverra un `CloudStorageAccount`.

### <a name="create-the-queue-service-client"></a>Créer le client de service de file d’attente

Le `CloudQueueClient` classe vous permet de récupérer des files d’attente stockées dans stockage file d’attente. Voici une façon de créer le client du service :

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L26-L26)]

Vous êtes maintenant prêt à écrire du code qui lit et écrit des données dans stockage file d’attente.

## <a name="create-a-queue"></a>Créer une file d’attente

Cet exemple montre comment créer une file d’attente si elle n’existe pas déjà :

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L32-L36)]

## <a name="insert-a-message-into-a-queue"></a>Insérer un message dans une file d’attente

Pour insérer un message dans une file d’attente existante, commencez par créer un `CloudQueueMessage`. Ensuite, appelez le `AddMessage` (méthode). Un `CloudQueueMessage` peut être créé à partir d’une chaîne (au format UTF-8) ou un `byte` tableau, comme suit :

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L42-L44)]

## <a name="peek-at-the-next-message"></a>Lire le message suivant

Vous pouvez lire furtivement le message au début d’une file d’attente, sans le supprimer de la file d’attente, en appelant le `PeekMessage` (méthode).

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L50-L52)]

## <a name="get-the-next-message-for-processing"></a>Obtenez le message suivant pour le traitement

Vous pouvez récupérer le message au début d’une file d’attente pour le traitement en appelant le `GetMessage` (méthode).

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L58-L59)]

Vous indiquez ultérieurement un traitement réussi du message à l’aide de `DeleteMessage`.

## <a name="change-the-contents-of-a-queued-message"></a>Modifier le contenu d’un message en file d’attente

Vous pouvez modifier le contenu d’un message récupéré sur place dans la file d’attente. Si le message représente une tâche, vous pouvez utiliser cette fonctionnalité pour mettre à jour l’état de la tâche. Le code suivant met à jour le message de file d’attente avec un nouveau contenu et définit le délai de visibilité pour étendre les 60 secondes. Cela enregistre l’état du travail associé au message et accorde au client une minute supplémentaire pour continuer à travailler sur le message. Vous pouvez utiliser cette technique pour effectuer le suivi de plusieurs étapes de flux de travail sur les messages de file d’attente, sans avoir à recommencer depuis le début, si une étape de traitement échoue en raison d’une défaillance matérielle ou logicielle. En règle générale, vous conservez aussi un nombre de nouvelles tentatives et si le message est retenté plus d’un certain nombre de fois, vous le supprimez. Cela empêche un message qui déclenche une erreur d’application chaque fois qu’elle est traitée.

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L65-L69)]

## <a name="de-queue-the-next-message"></a>File d’attente le message suivant

Votre code enlève un message à partir d’une file d’attente en deux étapes. Lorsque vous appelez `GetMessage`, vous obtenez le message suivant dans une file d’attente. Un message renvoyé par `GetMessage` devient invisible par les autres codes lisant les messages de cette file d’attente. Par défaut, ce message reste invisible pendant 30 secondes. Pour terminer la suppression du message de la file d’attente, vous devez également appeler `DeleteMessage`. Ce processus en deux étapes de la suppression d’un message garantit que si votre code ne parvient pas à traiter un message en raison d’une défaillance matérielle ou logicielle, une autre instance de votre code peut obtenir le même message et réessayez. Votre code appelle `DeleteMessage` avec le bouton droit une fois que le message a été traité.

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L75-L76)]

## <a name="use-async-workflows-with-common-queue-storage-apis"></a>Utiliser des flux de travail asynchrone avec les API de stockage file d’attente communes

Cet exemple montre comment utiliser un flux de travail asynchrone avec les API de stockage file d’attente communes.

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L82-L91)]

## <a name="additional-options-for-de-queuing-messages"></a>Options supplémentaires pour les files d’attente de messages

Il existe deux façons de personnaliser extraction d’un message à partir d’une file d’attente.
Tout d’abord, vous pouvez obtenir un lot de messages (jusqu'à 32). En second lieu, vous pouvez définir un délai d’expiration de l’invisibilité plus ou moins longtemps, votre code plus ou moins de temps pour traiter complètement chaque message. Le code suivant exemple utilise `GetMessages` pour obtenir 20 messages dans un appel et puis traite chaque message. Il définit également le délai d’expiration de l’invisibilité sur cinq minutes pour chaque message. Notez que les 5 minutes démarre pour tous les messages en même temps, par conséquent, une fois les 5 minutes écoulées après l’appel à `GetMessages`, tous les messages n’ont pas été supprimés redeviennent visibles.

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L97-L99)]

## <a name="get-the-queue-length"></a>Obtenir la longueur de file d’attente

Vous pouvez obtenir une estimation du nombre de messages dans une file d’attente. Le `FetchAttributes` méthode demande au service de file d’attente d’extraire les attributs de la file d’attente, y compris le nombre de messages. Le `ApproximateMessageCount` propriété retourne la dernière valeur extraite par la `FetchAttributes` méthode, sans appeler le service de file d’attente.

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L105-L106)]

## <a name="delete-a-queue"></a>Supprimer une file d’attente

Pour supprimer une file d’attente et tous les messages qu’elle contient, appelez le `Delete` méthode sur l’objet de file d’attente.

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L112-L113)]

## <a name="next-steps"></a>Étapes suivantes

Maintenant que vous avez appris les bases du stockage de file d’attente, suivez ces liens pour en savoir plus sur les tâches de stockage plus complexes.

- [API de stockage Azure pour .NET](/dotnet/api/overview/azure/storage)
- [Fournisseur de Type de stockage Azure](https://github.com/fsprojects/AzureStorageTypeProvider)
- [Blog de l’équipe stockage Azure](https://blogs.msdn.microsoft.com/windowsazurestorage/)
- [Configurer les chaînes de connexion de stockage Azure](/azure/storage/common/storage-configure-connection-string)
- [Référence de l’API REST des Services de stockage Azure](/rest/api/storageservices/Azure-Storage-Services-REST-API-Reference)
