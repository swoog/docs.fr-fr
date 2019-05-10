---
title: Encodage d'objets binaires avec l'encodeur ByteStream
ms.date: 03/30/2017
ms.assetid: 020ee981-c889-4b12-a3ea-91823ef46444
ms.openlocfilehash: 09a919e11971f81bc76dca0e45a7eb0e70ef749e
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64626927"
---
# <a name="encoding-binary-objects-with-bytestream-encoder"></a><span data-ttu-id="42897-102">Encodage d'objets binaires avec l'encodeur ByteStream</span><span class="sxs-lookup"><span data-stu-id="42897-102">Encoding Binary Objects with ByteStream Encoder</span></span>
<span data-ttu-id="42897-103">Envoyer et recevoir des données binaires brutes avec Windows Communication Foundation (WCF) sont configuré à l’aide de <xref:System.ServiceModel.Channels.ByteStreamMessageEncodingBindingElement>.</span><span class="sxs-lookup"><span data-stu-id="42897-103">Sending and receiving raw binary data with Windows Communication Foundation (WCF) is configured using <xref:System.ServiceModel.Channels.ByteStreamMessageEncodingBindingElement>.</span></span>  
  
## <a name="byte-stream-message-encoder-architecture"></a><span data-ttu-id="42897-104">Architecture de l'encodeur de message en flux d'octets</span><span class="sxs-lookup"><span data-stu-id="42897-104">Byte Stream Message Encoder Architecture</span></span>  
 <span data-ttu-id="42897-105">L’encodeur de message binaire utilisé par WCF dispose d’aucune fonctionnalité de traitement, de validation ou d’identification des données binaires sous-jacentes dans le message.</span><span class="sxs-lookup"><span data-stu-id="42897-105">The binary message encoder used by WCF has no facility for processing, validating, or identifying the underlying binary data in the message.</span></span> <span data-ttu-id="42897-106">Le package de données est encodé au format XML, envoyé, reçu et décodé.</span><span class="sxs-lookup"><span data-stu-id="42897-106">The data package is encoded into XML, sent, received, and decoded.</span></span> <span data-ttu-id="42897-107">L'encodeur traite les données une fois qu'elles ont été transmises au transport et avant que le message soit envoyé à la file d'attente des messages.</span><span class="sxs-lookup"><span data-stu-id="42897-107">The encoder processes the data after being passed to the transport and before the message is sent to the message queue.</span></span> <span data-ttu-id="42897-108">Techniquement, l'encodeur binaire encapsule les données du message en éléments `<binary>` pour l'envoi et supprime les éléments une fois le message reçu.</span><span class="sxs-lookup"><span data-stu-id="42897-108">Functionally, the binary encoder wraps the message data in `<binary>` elements for sending and removes the elements after the message is received.</span></span>  
  
## <a name="using-the-byte-stream-message-encoder"></a><span data-ttu-id="42897-109">Utilisation de l'encodeur de message en flux d'octets</span><span class="sxs-lookup"><span data-stu-id="42897-109">Using the Byte Stream Message Encoder</span></span>  
 <span data-ttu-id="42897-110">L'exemple suivant montre un contrat de service qui implémente l'encodeur de message en flux d'octets.</span><span class="sxs-lookup"><span data-stu-id="42897-110">The following example shows a service contract that implements the byte stream message encoder.</span></span>  
  
```csharp  
[OperationContract]  
Void Myfunction(Stream stream);  
```  
  
 <span data-ttu-id="42897-111">L'exemple suivant montre le service appelé.</span><span class="sxs-lookup"><span data-stu-id="42897-111">The following example shows the service being invoked.</span></span>  
  
```csharp  
proxy.MyFunction(stream);  
```  
  
 <span data-ttu-id="42897-112">Dans le cas de l'utilisation d'un service qui implémente une infrastructure de message (tel qu'un routeur), le message est traité sans être inspecté ni validé et sans interaction avec le message, comme indiqué dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="42897-112">In the case of using a service that implements a message infrastructure (such as a router), the message is processed without inspecting, validating, or otherwise interacting with the message, as shown in the following example.</span></span>  
  
```csharp  
[OperationContract]  
void ProcessMessage(Message message) ;  
```  
  
## <a name="scenarios"></a><span data-ttu-id="42897-113">Scénarios</span><span class="sxs-lookup"><span data-stu-id="42897-113">Scenarios</span></span>  
 <span data-ttu-id="42897-114">L'encodeur en flux d'octets s'avère utile dans les scénarios suivants.</span><span class="sxs-lookup"><span data-stu-id="42897-114">The Byte Stream Encoder is useful in the following scenarios.</span></span>  
  
- <span data-ttu-id="42897-115">Transférer une image JPEG entre plusieurs ordinateurs à l’aide de WCF.</span><span class="sxs-lookup"><span data-stu-id="42897-115">Transferring a JPEG image between computers using WCF.</span></span> <span data-ttu-id="42897-116">Dans ce scénario, l'image arrive par transport depuis une source externe et les données sont transmises par les octets bruts qui forment l'image.</span><span class="sxs-lookup"><span data-stu-id="42897-116">In this scenario, the image will arrive through the transport from an outside source, and the data sent will be the raw bytes that make up the image.</span></span> <span data-ttu-id="42897-117">Un service reçoit les données binaires et affiche l'image.</span><span class="sxs-lookup"><span data-stu-id="42897-117">A service will receive the binary data and display the image.</span></span>  
  
- <span data-ttu-id="42897-118">Lecture d'informations à partir d'une file d'attente de messages et traitement de ces informations.</span><span class="sxs-lookup"><span data-stu-id="42897-118">Reading information out of a message queue and processing it.</span></span> <span data-ttu-id="42897-119">Le message est lu à partir du gestionnaire de files d'attente de messages et passé au canal de file d'attente de messages à gérer.</span><span class="sxs-lookup"><span data-stu-id="42897-119">The message will be read from a message queue manager, and passed up the message queue channel to be handled.</span></span> <span data-ttu-id="42897-120">Le canal de file d’attente de message agira comme un gestionnaire de file d’attente dans la pile de canal WCF.</span><span class="sxs-lookup"><span data-stu-id="42897-120">The message queue channel will act as a queue manager in the WCF channel stack.</span></span>  
  
 <span data-ttu-id="42897-121">Dans le cas de l'envoi d'un message sur un canal de file d'attente de messages, l'expéditeur n'a aucun contrôle sur les octets reçus du gestionnaire de files d'attente.</span><span class="sxs-lookup"><span data-stu-id="42897-121">In the case of sending a message over a message queue channel, the sender has no control over the bytes received from the queue manager.</span></span> <span data-ttu-id="42897-122">Si le processus de réception n'arrive pas à lire les octets bruts, le message sera reçu avec un formatage erroné et ne sera pas traité ; on suppose que le processus de réception a la capacité de traduire les octets reçus dans un format utilisable.</span><span class="sxs-lookup"><span data-stu-id="42897-122">If the receiving process has no capability to read raw bytes, the message will be received as badly formatted and will not be processed; it is assumed that the receiving process will have the capability of translating the received bytes back into a usable format.</span></span>
