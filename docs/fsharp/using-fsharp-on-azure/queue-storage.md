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
# <a name="get-started-with-azure-queue-storage-using-f"></a><span data-ttu-id="458af-104">Prise en main Azure Queue storage à l’aide de F\#</span><span class="sxs-lookup"><span data-stu-id="458af-104">Get started with Azure Queue storage using F\#</span></span>

<span data-ttu-id="458af-105">Stockage de file d’attente Azure fournit la messagerie cloud entre les composants d’application.</span><span class="sxs-lookup"><span data-stu-id="458af-105">Azure Queue storage provides cloud messaging between application components.</span></span> <span data-ttu-id="458af-106">Dans la conception d’applications à grande échelle, les composants d’application sont souvent découplés, afin qu’ils peuvent mettre à l’échelle indépendamment.</span><span class="sxs-lookup"><span data-stu-id="458af-106">In designing applications for scale, application components are often decoupled, so that they can scale independently.</span></span> <span data-ttu-id="458af-107">Stockage file d’attente offre une messagerie asynchrone pour la communication entre les composants d’application, qu’ils soient exécutés dans le cloud, sur le bureau, sur un serveur local ou sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="458af-107">Queue storage delivers asynchronous messaging for communication between application components, whether they are running in the cloud, on the desktop, on an on-premises server, or on a mobile device.</span></span> <span data-ttu-id="458af-108">Stockage file d’attente prend également en charge la gestion des tâches asynchrones et la création de flux de travail de processus.</span><span class="sxs-lookup"><span data-stu-id="458af-108">Queue storage also supports managing asynchronous tasks and building process work flows.</span></span>

### <a name="about-this-tutorial"></a><span data-ttu-id="458af-109">À propos de ce didacticiel</span><span class="sxs-lookup"><span data-stu-id="458af-109">About this tutorial</span></span>

<span data-ttu-id="458af-110">Ce didacticiel montre comment écrire F# code de certaines tâches courantes à l’aide d’Azure Queue storage.</span><span class="sxs-lookup"><span data-stu-id="458af-110">This tutorial shows how to write F# code for some common tasks using Azure Queue storage.</span></span> <span data-ttu-id="458af-111">Tâches couvertes incluent la création et suppression de files d’attente et ajout, la lecture et suppression des messages de file d’attente.</span><span class="sxs-lookup"><span data-stu-id="458af-111">Tasks covered include creating and deleting queues and adding, reading, and deleting queue messages.</span></span>

<span data-ttu-id="458af-112">Pour obtenir une vue d’ensemble conceptuelle de stockage de file d’attente, consultez [le guide de .NET pour le stockage de file d’attente](/azure/storage/storage-dotnet-how-to-use-queues).</span><span class="sxs-lookup"><span data-stu-id="458af-112">For a conceptual overview of queue storage, please see [the .NET guide for queue storage](/azure/storage/storage-dotnet-how-to-use-queues).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="458af-113">Prérequis</span><span class="sxs-lookup"><span data-stu-id="458af-113">Prerequisites</span></span>

<span data-ttu-id="458af-114">Pour utiliser ce guide, vous devez d’abord [créer un compte de stockage Azure](/azure/storage/storage-create-storage-account).</span><span class="sxs-lookup"><span data-stu-id="458af-114">To use this guide, you must first [create an Azure storage account](/azure/storage/storage-create-storage-account).</span></span>
<span data-ttu-id="458af-115">Vous devez également votre clé d’accès de stockage pour ce compte.</span><span class="sxs-lookup"><span data-stu-id="458af-115">You'll also need your storage access key for this account.</span></span>

## <a name="create-an-f-script-and-start-f-interactive"></a><span data-ttu-id="458af-116">Créer un F# de Script et démarrer F# Interactive</span><span class="sxs-lookup"><span data-stu-id="458af-116">Create an F# Script and Start F# Interactive</span></span>

<span data-ttu-id="458af-117">Les exemples de cet article peuvent être utilisées dans un F# application ou un F# script.</span><span class="sxs-lookup"><span data-stu-id="458af-117">The samples in this article can be used in either an F# application or an F# script.</span></span> <span data-ttu-id="458af-118">Pour créer un F# de script, créez un fichier avec le `.fsx` extension, par exemple `queues.fsx`, dans votre F# environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="458af-118">To create an F# script, create a file with the `.fsx` extension, for example `queues.fsx`, in your F# development environment.</span></span>

<span data-ttu-id="458af-119">Ensuite, utilisez un [Gestionnaire de package](package-management.md) comme [Paket](https://fsprojects.github.io/Paket/) ou [NuGet](https://www.nuget.org/) pour installer le `WindowsAzure.Storage` package et référence `WindowsAzure.Storage.dll` dans votre script à l’aide d’un `#r`directive.</span><span class="sxs-lookup"><span data-stu-id="458af-119">Next, use a [package manager](package-management.md) such as [Paket](https://fsprojects.github.io/Paket/) or [NuGet](https://www.nuget.org/) to install the `WindowsAzure.Storage` package and reference `WindowsAzure.Storage.dll` in your script using a `#r` directive.</span></span>

### <a name="add-namespace-declarations"></a><span data-ttu-id="458af-120">Ajoutez les déclarations d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="458af-120">Add namespace declarations</span></span>

<span data-ttu-id="458af-121">Ajoutez le code suivant `open` instructions au début de la `queues.fsx` fichier :</span><span class="sxs-lookup"><span data-stu-id="458af-121">Add the following `open` statements to the top of the `queues.fsx` file:</span></span>

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L1-L3)]

### <a name="get-your-connection-string"></a><span data-ttu-id="458af-122">Obtenir votre chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="458af-122">Get your connection string</span></span>

<span data-ttu-id="458af-123">Vous aurez besoin d’une chaîne de connexion de stockage Azure pour ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="458af-123">You'll need an Azure Storage connection string for this tutorial.</span></span> <span data-ttu-id="458af-124">Pour plus d’informations sur les chaînes de connexion, consultez [configuration des chaînes de connexion stockage](/azure/storage/storage-configure-connection-string).</span><span class="sxs-lookup"><span data-stu-id="458af-124">For more information about connection strings, see [Configure Storage Connection Strings](/azure/storage/storage-configure-connection-string).</span></span>

<span data-ttu-id="458af-125">Pour ce didacticiel, vous allez entrer votre chaîne de connexion dans votre script, comme suit :</span><span class="sxs-lookup"><span data-stu-id="458af-125">For the tutorial, you'll enter your connection string in your script, like this:</span></span>

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L9-L9)]

<span data-ttu-id="458af-126">Toutefois, il s’agit de **déconseillé** projets de réel.</span><span class="sxs-lookup"><span data-stu-id="458af-126">However, this is **not recommended** for real projects.</span></span> <span data-ttu-id="458af-127">Votre clé de compte de stockage est similaire au mot de passe racine pour votre compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="458af-127">Your storage account key is similar to the root password for your storage account.</span></span> <span data-ttu-id="458af-128">Veillez toujours à protéger votre clé de compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="458af-128">Always be careful to protect your storage account key.</span></span> <span data-ttu-id="458af-129">Évitez de la communiquer à d’autres utilisateurs, coder en dur, ou l’enregistrer dans un fichier texte brut qui n’est accessible à d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="458af-129">Avoid distributing it to other users, hard-coding it, or saving it in a plain-text file that is accessible to others.</span></span> <span data-ttu-id="458af-130">Vous pouvez régénérer votre clé à l’aide du portail Azure si vous pensez qu’il a peut-être été compromise.</span><span class="sxs-lookup"><span data-stu-id="458af-130">You can regenerate your key using the Azure Portal if you believe it may have been compromised.</span></span>

<span data-ttu-id="458af-131">Applications de réel, la meilleure façon de conserver votre chaîne de connexion de stockage est dans un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="458af-131">For real applications, the best way to maintain your storage connection string is in a configuration file.</span></span> <span data-ttu-id="458af-132">Pour extraire la chaîne de connexion à partir d’un fichier de configuration, vous pouvez effectuer ceci :</span><span class="sxs-lookup"><span data-stu-id="458af-132">To fetch the connection string from a configuration file, you can do this:</span></span>

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L11-L13)]

<span data-ttu-id="458af-133">L’utilisation d’Azure Configuration Manager est facultative.</span><span class="sxs-lookup"><span data-stu-id="458af-133">Using Azure Configuration Manager is optional.</span></span> <span data-ttu-id="458af-134">Vous pouvez également utiliser une API telle que du .NET Framework `ConfigurationManager` type.</span><span class="sxs-lookup"><span data-stu-id="458af-134">You can also use an API such as the .NET Framework's `ConfigurationManager` type.</span></span>

### <a name="parse-the-connection-string"></a><span data-ttu-id="458af-135">Analyser la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="458af-135">Parse the connection string</span></span>

<span data-ttu-id="458af-136">Pour analyser la chaîne de connexion, utilisez :</span><span class="sxs-lookup"><span data-stu-id="458af-136">To parse the connection string, use:</span></span>

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L19-L20)]

<span data-ttu-id="458af-137">Ceci renverra un `CloudStorageAccount`.</span><span class="sxs-lookup"><span data-stu-id="458af-137">This will return a `CloudStorageAccount`.</span></span>

### <a name="create-the-queue-service-client"></a><span data-ttu-id="458af-138">Créer le client de service de file d’attente</span><span class="sxs-lookup"><span data-stu-id="458af-138">Create the Queue service client</span></span>

<span data-ttu-id="458af-139">Le `CloudQueueClient` classe vous permet de récupérer des files d’attente stockées dans stockage file d’attente.</span><span class="sxs-lookup"><span data-stu-id="458af-139">The `CloudQueueClient` class enables you to retrieve queues stored in Queue storage.</span></span> <span data-ttu-id="458af-140">Voici une façon de créer le client du service :</span><span class="sxs-lookup"><span data-stu-id="458af-140">Here's one way to create the service client:</span></span>

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L26-L26)]

<span data-ttu-id="458af-141">Vous êtes maintenant prêt à écrire du code qui lit et écrit des données dans stockage file d’attente.</span><span class="sxs-lookup"><span data-stu-id="458af-141">Now you are ready to write code that reads data from and writes data to Queue storage.</span></span>

## <a name="create-a-queue"></a><span data-ttu-id="458af-142">Créer une file d’attente</span><span class="sxs-lookup"><span data-stu-id="458af-142">Create a queue</span></span>

<span data-ttu-id="458af-143">Cet exemple montre comment créer une file d’attente si elle n’existe pas déjà :</span><span class="sxs-lookup"><span data-stu-id="458af-143">This example shows how to create a queue if it doesn't already exist:</span></span>

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L32-L36)]

## <a name="insert-a-message-into-a-queue"></a><span data-ttu-id="458af-144">Insérer un message dans une file d’attente</span><span class="sxs-lookup"><span data-stu-id="458af-144">Insert a message into a queue</span></span>

<span data-ttu-id="458af-145">Pour insérer un message dans une file d’attente existante, commencez par créer un `CloudQueueMessage`.</span><span class="sxs-lookup"><span data-stu-id="458af-145">To insert a message into an existing queue, first create a new `CloudQueueMessage`.</span></span> <span data-ttu-id="458af-146">Ensuite, appelez le `AddMessage` (méthode).</span><span class="sxs-lookup"><span data-stu-id="458af-146">Next, call the `AddMessage` method.</span></span> <span data-ttu-id="458af-147">Un `CloudQueueMessage` peut être créé à partir d’une chaîne (au format UTF-8) ou un `byte` tableau, comme suit :</span><span class="sxs-lookup"><span data-stu-id="458af-147">A `CloudQueueMessage` can be created from either a string (in UTF-8 format) or a `byte` array, like this:</span></span>

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L42-L44)]

## <a name="peek-at-the-next-message"></a><span data-ttu-id="458af-148">Lire le message suivant</span><span class="sxs-lookup"><span data-stu-id="458af-148">Peek at the next message</span></span>

<span data-ttu-id="458af-149">Vous pouvez lire furtivement le message au début d’une file d’attente, sans le supprimer de la file d’attente, en appelant le `PeekMessage` (méthode).</span><span class="sxs-lookup"><span data-stu-id="458af-149">You can peek at the message in the front of a queue, without removing it from the queue, by calling the `PeekMessage` method.</span></span>

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L50-L52)]

## <a name="get-the-next-message-for-processing"></a><span data-ttu-id="458af-150">Obtenez le message suivant pour le traitement</span><span class="sxs-lookup"><span data-stu-id="458af-150">Get the next message for processing</span></span>

<span data-ttu-id="458af-151">Vous pouvez récupérer le message au début d’une file d’attente pour le traitement en appelant le `GetMessage` (méthode).</span><span class="sxs-lookup"><span data-stu-id="458af-151">You can retrieve the message at the front of a queue for processing by calling the `GetMessage` method.</span></span>

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L58-L59)]

<span data-ttu-id="458af-152">Vous indiquez ultérieurement un traitement réussi du message à l’aide de `DeleteMessage`.</span><span class="sxs-lookup"><span data-stu-id="458af-152">You later indicate successful processing of the message by using `DeleteMessage`.</span></span>

## <a name="change-the-contents-of-a-queued-message"></a><span data-ttu-id="458af-153">Modifier le contenu d’un message en file d’attente</span><span class="sxs-lookup"><span data-stu-id="458af-153">Change the contents of a queued message</span></span>

<span data-ttu-id="458af-154">Vous pouvez modifier le contenu d’un message récupéré sur place dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="458af-154">You can change the contents of a retrieved message in-place in the queue.</span></span> <span data-ttu-id="458af-155">Si le message représente une tâche, vous pouvez utiliser cette fonctionnalité pour mettre à jour l’état de la tâche.</span><span class="sxs-lookup"><span data-stu-id="458af-155">If the message represents a work task, you could use this feature to update the status of the work task.</span></span> <span data-ttu-id="458af-156">Le code suivant met à jour le message de file d’attente avec un nouveau contenu et définit le délai de visibilité pour étendre les 60 secondes.</span><span class="sxs-lookup"><span data-stu-id="458af-156">The following code updates the queue message with new contents, and sets the visibility timeout to extend another 60 seconds.</span></span> <span data-ttu-id="458af-157">Cela enregistre l’état du travail associé au message et accorde au client une minute supplémentaire pour continuer à travailler sur le message.</span><span class="sxs-lookup"><span data-stu-id="458af-157">This saves the state of work associated with the message, and gives the client another minute to continue working on the message.</span></span> <span data-ttu-id="458af-158">Vous pouvez utiliser cette technique pour effectuer le suivi de plusieurs étapes de flux de travail sur les messages de file d’attente, sans avoir à recommencer depuis le début, si une étape de traitement échoue en raison d’une défaillance matérielle ou logicielle.</span><span class="sxs-lookup"><span data-stu-id="458af-158">You could use this technique to track multi-step workflows on queue messages, without having to start over from the beginning if a processing step fails due to hardware or software failure.</span></span> <span data-ttu-id="458af-159">En règle générale, vous conservez aussi un nombre de nouvelles tentatives et si le message est retenté plus d’un certain nombre de fois, vous le supprimez.</span><span class="sxs-lookup"><span data-stu-id="458af-159">Typically, you would keep a retry count as well, and if the message is retried more than some number of times, you would delete it.</span></span> <span data-ttu-id="458af-160">Cela empêche un message qui déclenche une erreur d’application chaque fois qu’elle est traitée.</span><span class="sxs-lookup"><span data-stu-id="458af-160">This protects against a message that triggers an application error each time it is processed.</span></span>

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L65-L69)]

## <a name="de-queue-the-next-message"></a><span data-ttu-id="458af-161">File d’attente le message suivant</span><span class="sxs-lookup"><span data-stu-id="458af-161">De-queue the next message</span></span>

<span data-ttu-id="458af-162">Votre code enlève un message à partir d’une file d’attente en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="458af-162">Your code de-queues a message from a queue in two steps.</span></span> <span data-ttu-id="458af-163">Lorsque vous appelez `GetMessage`, vous obtenez le message suivant dans une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="458af-163">When you call `GetMessage`, you get the next message in a queue.</span></span> <span data-ttu-id="458af-164">Un message renvoyé par `GetMessage` devient invisible par les autres codes lisant les messages de cette file d’attente.</span><span class="sxs-lookup"><span data-stu-id="458af-164">A message returned from `GetMessage` becomes invisible to any other code reading messages from this queue.</span></span> <span data-ttu-id="458af-165">Par défaut, ce message reste invisible pendant 30 secondes.</span><span class="sxs-lookup"><span data-stu-id="458af-165">By default, this message stays invisible for 30 seconds.</span></span> <span data-ttu-id="458af-166">Pour terminer la suppression du message de la file d’attente, vous devez également appeler `DeleteMessage`.</span><span class="sxs-lookup"><span data-stu-id="458af-166">To finish removing the message from the queue, you must also call `DeleteMessage`.</span></span> <span data-ttu-id="458af-167">Ce processus en deux étapes de la suppression d’un message garantit que si votre code ne parvient pas à traiter un message en raison d’une défaillance matérielle ou logicielle, une autre instance de votre code peut obtenir le même message et réessayez.</span><span class="sxs-lookup"><span data-stu-id="458af-167">This two-step process of removing a message assures that if your code fails to process a message due to hardware or software failure, another instance of your code can get the same message and try again.</span></span> <span data-ttu-id="458af-168">Votre code appelle `DeleteMessage` avec le bouton droit une fois que le message a été traité.</span><span class="sxs-lookup"><span data-stu-id="458af-168">Your code calls `DeleteMessage` right after the message has been processed.</span></span>

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L75-L76)]

## <a name="use-async-workflows-with-common-queue-storage-apis"></a><span data-ttu-id="458af-169">Utiliser des flux de travail asynchrone avec les API de stockage file d’attente communes</span><span class="sxs-lookup"><span data-stu-id="458af-169">Use Async workflows with common Queue storage APIs</span></span>

<span data-ttu-id="458af-170">Cet exemple montre comment utiliser un flux de travail asynchrone avec les API de stockage file d’attente communes.</span><span class="sxs-lookup"><span data-stu-id="458af-170">This example shows how to use an async workflow with common Queue storage APIs.</span></span>

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L82-L91)]

## <a name="additional-options-for-de-queuing-messages"></a><span data-ttu-id="458af-171">Options supplémentaires pour les files d’attente de messages</span><span class="sxs-lookup"><span data-stu-id="458af-171">Additional options for de-queuing messages</span></span>

<span data-ttu-id="458af-172">Il existe deux façons de personnaliser extraction d’un message à partir d’une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="458af-172">There are two ways you can customize message retrieval from a queue.</span></span>
<span data-ttu-id="458af-173">Tout d’abord, vous pouvez obtenir un lot de messages (jusqu'à 32).</span><span class="sxs-lookup"><span data-stu-id="458af-173">First, you can get a batch of messages (up to 32).</span></span> <span data-ttu-id="458af-174">En second lieu, vous pouvez définir un délai d’expiration de l’invisibilité plus ou moins longtemps, votre code plus ou moins de temps pour traiter complètement chaque message.</span><span class="sxs-lookup"><span data-stu-id="458af-174">Second, you can set a longer or shorter invisibility timeout, allowing your code more or less time to fully process each message.</span></span> <span data-ttu-id="458af-175">Le code suivant exemple utilise `GetMessages` pour obtenir 20 messages dans un appel et puis traite chaque message.</span><span class="sxs-lookup"><span data-stu-id="458af-175">The following code example uses `GetMessages` to get 20 messages in one call and then processes each message.</span></span> <span data-ttu-id="458af-176">Il définit également le délai d’expiration de l’invisibilité sur cinq minutes pour chaque message.</span><span class="sxs-lookup"><span data-stu-id="458af-176">It also sets the invisibility timeout to five minutes for each message.</span></span> <span data-ttu-id="458af-177">Notez que les 5 minutes démarre pour tous les messages en même temps, par conséquent, une fois les 5 minutes écoulées après l’appel à `GetMessages`, tous les messages n’ont pas été supprimés redeviennent visibles.</span><span class="sxs-lookup"><span data-stu-id="458af-177">Note that the 5 minutes starts for all messages at the same time, so after 5 minutes have passed since the call to `GetMessages`, any messages which have not been deleted will become visible again.</span></span>

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L97-L99)]

## <a name="get-the-queue-length"></a><span data-ttu-id="458af-178">Obtenir la longueur de file d’attente</span><span class="sxs-lookup"><span data-stu-id="458af-178">Get the queue length</span></span>

<span data-ttu-id="458af-179">Vous pouvez obtenir une estimation du nombre de messages dans une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="458af-179">You can get an estimate of the number of messages in a queue.</span></span> <span data-ttu-id="458af-180">Le `FetchAttributes` méthode demande au service de file d’attente d’extraire les attributs de la file d’attente, y compris le nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="458af-180">The `FetchAttributes` method asks the Queue service to retrieve the queue attributes, including the message count.</span></span> <span data-ttu-id="458af-181">Le `ApproximateMessageCount` propriété retourne la dernière valeur extraite par la `FetchAttributes` méthode, sans appeler le service de file d’attente.</span><span class="sxs-lookup"><span data-stu-id="458af-181">The `ApproximateMessageCount` property returns the last value retrieved by the `FetchAttributes` method, without calling the Queue service.</span></span>

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L105-L106)]

## <a name="delete-a-queue"></a><span data-ttu-id="458af-182">Supprimer une file d’attente</span><span class="sxs-lookup"><span data-stu-id="458af-182">Delete a queue</span></span>

<span data-ttu-id="458af-183">Pour supprimer une file d’attente et tous les messages qu’elle contient, appelez le `Delete` méthode sur l’objet de file d’attente.</span><span class="sxs-lookup"><span data-stu-id="458af-183">To delete a queue and all the messages contained in it, call the `Delete` method on the queue object.</span></span>

[!code-fsharp[QueueStorage](../../../samples/snippets/fsharp/azure/queue-storage.fsx#L112-L113)]

## <a name="next-steps"></a><span data-ttu-id="458af-184">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="458af-184">Next steps</span></span>

<span data-ttu-id="458af-185">Maintenant que vous avez appris les bases du stockage de file d’attente, suivez ces liens pour en savoir plus sur les tâches de stockage plus complexes.</span><span class="sxs-lookup"><span data-stu-id="458af-185">Now that you've learned the basics of Queue storage, follow these links to learn about more complex storage tasks.</span></span>

- [<span data-ttu-id="458af-186">API de stockage Azure pour .NET</span><span class="sxs-lookup"><span data-stu-id="458af-186">Azure Storage APIs for .NET</span></span>](/dotnet/api/overview/azure/storage)
- [<span data-ttu-id="458af-187">Fournisseur de Type de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="458af-187">Azure Storage Type Provider</span></span>](https://github.com/fsprojects/AzureStorageTypeProvider)
- [<span data-ttu-id="458af-188">Blog de l’équipe stockage Azure</span><span class="sxs-lookup"><span data-stu-id="458af-188">Azure Storage Team Blog</span></span>](https://blogs.msdn.microsoft.com/windowsazurestorage/)
- [<span data-ttu-id="458af-189">Configurer les chaînes de connexion de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="458af-189">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)
- [<span data-ttu-id="458af-190">Référence de l’API REST des Services de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="458af-190">Azure Storage Services REST API Reference</span></span>](/rest/api/storageservices/Azure-Storage-Services-REST-API-Reference)
