---
title: Protocole de messagerie fiable version 1,1
ms.date: 03/30/2017
ms.assetid: 0da47b82-f8eb-42da-8bfe-e56ce7ba6f59
ms.openlocfilehash: 6b8732e0b48797c219b53bb8bf70e1ba57e25c42
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61933989"
---
# <a name="reliable-messaging-protocol-version-11"></a><span data-ttu-id="0c9a0-102">Protocole de messagerie fiable version 1,1</span><span class="sxs-lookup"><span data-stu-id="0c9a0-102">Reliable Messaging Protocol version 1.1</span></span>
<span data-ttu-id="0c9a0-103">Cette rubrique traite des détails d’implémentation de Windows Communication Foundation (WCF) pour le WS-ReliableMessaging protocole février 2007 (version 1.1) nécessaire pour l’interopérabilité utilisant le transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-103">This topic covers Windows Communication Foundation (WCF) implementation details for the WS-ReliableMessaging February 2007 (version 1.1) protocol necessary for interoperation using the HTTP transport.</span></span> <span data-ttu-id="0c9a0-104">WCF suit la spécification de WS-ReliableMessaging avec les contraintes et les éclaircissements présentés dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-104">WCF follows the WS-ReliableMessaging specification with the constraints and clarifications explained in this topic.</span></span> <span data-ttu-id="0c9a0-105">Notez que le protocole de la version 1.1 WS-ReliableMessaging est implémenté en commençant par le [!INCLUDE[netfx35_long](../../../../includes/netfx35-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="0c9a0-105">Note that the WS-ReliableMessaging version 1.1 protocol is implemented starting with the [!INCLUDE[netfx35_long](../../../../includes/netfx35-long-md.md)].</span></span>  
  
 <span data-ttu-id="0c9a0-106">Le WS-ReliableMessaging février 2007 protocole est implémenté dans WCF par le <xref:System.ServiceModel.Channels.ReliableSessionBindingElement>.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-106">The WS-ReliableMessaging February 2007 protocol is implemented in WCF by the <xref:System.ServiceModel.Channels.ReliableSessionBindingElement>.</span></span>  
  
 <span data-ttu-id="0c9a0-107">Pour plus de simplicité, la rubrique utilise les rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="0c9a0-107">For convenience, the topic uses the following roles:</span></span>  
  
-   <span data-ttu-id="0c9a0-108">Initiateur : Le client qui lance la création de séquence de Message WS-Reliable.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-108">Initiator: The client that initiates WS-Reliable Message sequence creation.</span></span>  
  
-   <span data-ttu-id="0c9a0-109">Répondeur : Le service qui reçoit des demandes de l’initiateur.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-109">Responder: The service that receives the initiator's requests.</span></span>  
  
 <span data-ttu-id="0c9a0-110">Ce document utilise les préfixes et les espaces de noms répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-110">This document uses the prefixes and namespaces in the following table.</span></span>  
  
|<span data-ttu-id="0c9a0-111">Préfixe</span><span class="sxs-lookup"><span data-stu-id="0c9a0-111">Prefix</span></span>|<span data-ttu-id="0c9a0-112">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0c9a0-112">Namespace</span></span>|  
|-|-|  
|<span data-ttu-id="0c9a0-113">wsrm</span><span class="sxs-lookup"><span data-stu-id="0c9a0-113">wsrm</span></span>|http://docs.oasis-open.org/ws-rx/wsrm/200702|  
|<span data-ttu-id="0c9a0-114">netrm</span><span class="sxs-lookup"><span data-stu-id="0c9a0-114">netrm</span></span>|http://schemas.microsoft.com/ws/2006/05/rm|  
|<span data-ttu-id="0c9a0-115">s</span><span class="sxs-lookup"><span data-stu-id="0c9a0-115">s</span></span>|http://www.w3.org/2003/05/soap-envelope|  
|<span data-ttu-id="0c9a0-116">wsa</span><span class="sxs-lookup"><span data-stu-id="0c9a0-116">wsa</span></span>|http://schemas.xmlsoap.org/ws/2005/08/addressing|  
|<span data-ttu-id="0c9a0-117">wsse</span><span class="sxs-lookup"><span data-stu-id="0c9a0-117">wsse</span></span>|http://docs.oasis-open.org/wss/2004/01/oasis-200401-wssecurity-secext-1.0.xsd|  
|<span data-ttu-id="0c9a0-118">wsrmp</span><span class="sxs-lookup"><span data-stu-id="0c9a0-118">wsrmp</span></span>|http://docs.oasis-open.org/ws-rx/wsrmp/200702|  
|<span data-ttu-id="0c9a0-119">netrmp</span><span class="sxs-lookup"><span data-stu-id="0c9a0-119">netrmp</span></span>|http://schemas.microsoft.com/ws-rx/wsrmp/200702|  
|<span data-ttu-id="0c9a0-120">wsp</span><span class="sxs-lookup"><span data-stu-id="0c9a0-120">wsp</span></span>|<span data-ttu-id="0c9a0-121">(WS-Policy 1.2 ou WS-Policy 1.5)</span><span class="sxs-lookup"><span data-stu-id="0c9a0-121">(Either WS-Policy 1.2 or WS-Policy 1.5)</span></span>|  
  
## <a name="messaging"></a><span data-ttu-id="0c9a0-122">Messagerie</span><span class="sxs-lookup"><span data-stu-id="0c9a0-122">Messaging</span></span>  
  
### <a name="sequence-creation"></a><span data-ttu-id="0c9a0-123">Création de la séquence</span><span class="sxs-lookup"><span data-stu-id="0c9a0-123">Sequence Creation</span></span>  
 <span data-ttu-id="0c9a0-124">WCF implémente `CreateSequence` et `CreateSequenceResponse` séquence de messages pour établir une messagerie fiable.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-124">WCF implements `CreateSequence` and `CreateSequenceResponse` messages to establish a reliable messaging sequence.</span></span> <span data-ttu-id="0c9a0-125">Les contraintes suivantes s'appliquent :</span><span class="sxs-lookup"><span data-stu-id="0c9a0-125">The following constraints apply:</span></span>  
  
-   <span data-ttu-id="0c9a0-126">B1101 : L’initiateur WCF utilise la même référence de point de terminaison en tant que le `CreateSequence` du message `ReplyTo`, `AcksTo` et `Offer/Endpoint`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-126">B1101: The WCF Initiator uses the same endpoint reference as the `CreateSequence` message’s `ReplyTo`, `AcksTo` and `Offer/Endpoint`.</span></span>  
  
-   <span data-ttu-id="0c9a0-127">R1102 : Le `AcksTo`, `ReplyTo` et `Offer/Endpoint` références de point de terminaison dans le `CreateSequence` message doit avoir des valeurs d’adresse avec des représentations sous forme de chaîne identique tels qu’ils correspondent au niveau des octets.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-127">R1102: The `AcksTo`, `ReplyTo` and `Offer/Endpoint` endpoint references in the `CreateSequence` message must have address values with identical string representations such that they match the octet-wise.</span></span>  
  
    -   <span data-ttu-id="0c9a0-128">Le répondeur WCF vérifie que la portion d’URI de la `AcksTo`, `ReplyTo` et `Endpoint` références de point de terminaison sont identiques avant de créer une séquence.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-128">The WCF Responder verifies that the URI portion of the `AcksTo`, `ReplyTo` and `Endpoint` endpoint references are identical before creating a sequence.</span></span>  
  
-   <span data-ttu-id="0c9a0-129">R1103 : Le `AcksTo`, `ReplyTo` et `Offer/Endpoint` références de point de terminaison dans le `CreateSequence` message doit avoir le même jeu de paramètres de référence.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-129">R1103: The `AcksTo`, `ReplyTo` and `Offer/Endpoint` endpoint references in the `CreateSequence` message should have the same set of reference parameters.</span></span>  
  
    -   <span data-ttu-id="0c9a0-130">WCF n’applique pas, mais part du principe qui référencent les paramètres de la `AcksTo`, `ReplyTo` et `Offer/Endpoint` fait référence à point de terminaison sur `CreateSequence` sont identiques et utilise les paramètres de référence de la `ReplyTo` référence de point de terminaison pour accusés de réception et les messages de séquence réciproque.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-130">WCF does not enforce, but assumes that reference parameters of the `AcksTo`, `ReplyTo` and `Offer/Endpoint` endpoint references on `CreateSequence` are identical and uses reference parameters from the `ReplyTo` endpoint reference for acknowledgements and converse sequence messages.</span></span>  
  
-   <span data-ttu-id="0c9a0-131">B1104 : L’initiateur WCF ne génère pas le paramètre facultatif `Expires` ou `Offer/Expires` élément dans le `CreateSequence` message.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-131">B1104: The WCF Initiator does not generate the optional `Expires` or `Offer/Expires` element in the `CreateSequence` message.</span></span>  
  
-   <span data-ttu-id="0c9a0-132">B1105 : Lors de l’accès le `CreateSequence` message, le répondeur WCF utilise le `Expires` valeur dans le `CreateSequence` élément en tant que le `Expires` valeur dans le `CreateSequenceResponse` élément.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-132">B1105: When accessing the `CreateSequence` message, the WCF Responder uses the `Expires` value in the `CreateSequence` element as the `Expires` value in the `CreateSequenceResponse` element.</span></span> <span data-ttu-id="0c9a0-133">Sinon, le répondeur WCF lit et ignore le `Expires` et `Offer/Expires` valeurs.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-133">Otherwise, the WCF Responder reads and ignores the `Expires` and `Offer/Expires` values.</span></span>  
  
-   <span data-ttu-id="0c9a0-134">B1106 : Lorsque vous accédez à la `CreateSequenceResponse` message, l’initiateur WCF lit l’élément facultatif `Expires` valeur mais ne l’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-134">B1106: When accessing the `CreateSequenceResponse` message, the WCF Initiator reads the optional `Expires` value but does not use it.</span></span>  
  
-   <span data-ttu-id="0c9a0-135">B1107 : L’initiateur de WCF et le répondeur génèrent toujours facultatif `IncompleteSequenceBehavior` élément dans le `CreateSequence/Offer` et `CreateSequenceResponse` éléments.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-135">B1107: The WCF Initiator and Responder always generate the optional `IncompleteSequenceBehavior` element in the `CreateSequence/Offer` and `CreateSequenceResponse` elements.</span></span>  
  
-   <span data-ttu-id="0c9a0-136">B1108 : WCF utilise uniquement le `DiscardFollowingFirstGap` et `NoDiscard` des valeurs dans le `IncompleteSequenceBehavior` élément.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-136">B1108: WCF uses only the `DiscardFollowingFirstGap` and `NoDiscard` values in the `IncompleteSequenceBehavior` element.</span></span>  
  
    -   <span data-ttu-id="0c9a0-137">WS-ReliableMessaging utilise le mécanisme `Offer` pour établir deux séquences corrélées réciproques qui forment une session.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-137">WS-ReliableMessaging utilizes the `Offer` mechanism to establish the two converse correlated sequences that form a session.</span></span>  
  
-   <span data-ttu-id="0c9a0-138">B1109 : Si `CreateSequence` contient un `Offer` élément, le répondeur WCF unidirectionnel rejette la séquence présentée en répondant avec un `CreateSequenceResponse` sans un `Accept` élément.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-138">B1109: If `CreateSequence` contains an `Offer` element, the one way WCF Responder rejects the offered sequence by responding with a `CreateSequenceResponse` without an `Accept` element.</span></span>  
  
-   <span data-ttu-id="0c9a0-139">B1110 : Si un répondeur de messagerie fiable rejette la séquence présentée, l’initiateur WCF provoque des erreurs la séquence récemment établie.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-139">B1110: If a Reliable Messaging Responder rejects the offered sequence, the WCF Initiator faults the newly established sequence.</span></span>  
  
-   <span data-ttu-id="0c9a0-140">B1111 : Si `CreateSequence` ne contient pas une `Offer` élément, le répondeur WCF bidirectionnel rejette la séquence présentée en répondant avec un `CreateSequenceRefused` pannes.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-140">B1111: If `CreateSequence` does not contain an `Offer` element, the two-way WCF Responder rejects the offered sequence by responding with a `CreateSequenceRefused` fault.</span></span>  
  
-   <span data-ttu-id="0c9a0-141">R1112 : Lorsque deux séquences réciproques sont établies à l’aide de la `Offer` mécanisme, le `[address]` propriété de la `CreateSequenceResponse/Accept/AcksTo` référence de point de terminaison doit correspondre à l’URI de destination de la `CreateSequence` octets de message pour les octets.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-141">R1112: When two converse sequences are established using the `Offer` mechanism, the `[address]` property of the `CreateSequenceResponse/Accept/AcksTo` endpoint reference must match the destination URI of the `CreateSequence` message byte for byte.</span></span>  
  
-   <span data-ttu-id="0c9a0-142">R1113 : Lorsque deux séquences réciproques sont établies à l’aide de la `Offer` mécanisme, tous les messages sur les deux séquences circulant de l’initiateur au répondeur doivent être envoyés à la même référence de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-142">R1113: When two converse sequences are established using the `Offer` mechanism, all messages on both sequences flowing from the Initiator to the Responder must be sent to the same endpoint reference.</span></span>  
  
 <span data-ttu-id="0c9a0-143">WCF utilise WS-ReliableMessaging pour établir des sessions fiables entre l’initiateur et le répondeur.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-143">WCF uses WS-ReliableMessaging to establish reliable sessions between the Initiator and the Responder.</span></span> <span data-ttu-id="0c9a0-144">L’implémentation de WCF WS-ReliableMessaging fournit une session fiable pour intégral demande-réponse et unidirectionnels, modèles de messagerie en duplex.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-144">The WCF WS-ReliableMessaging implementation provides a reliable session for one-way, request-reply and full duplex messaging patterns.</span></span> <span data-ttu-id="0c9a0-145">Le mécanisme WS-ReliableMessaging `Offer` sur `CreateSequence` et `CreateSequenceResponse` vous permet d'établir deux séquences réciproques corrélées et fournit un protocole de session qui convient à tous les points de terminaison de message.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-145">The WS-ReliableMessaging `Offer` mechanism on `CreateSequence` and `CreateSequenceResponse` lets you establish two correlated converse sequences and provides a session protocol that is suitable for all message endpoints.</span></span> <span data-ttu-id="0c9a0-146">Étant donné que WCF fournit une garantie de sécurité pour une telle session, y compris la protection de bout en bout pour l’intégrité de session, il est pratique de s’assurer que les messages destinés à la même partie arrivent à la même destination.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-146">Because WCF provides a security guarantee for such a session including end-to-end protection for session integrity, it is practical to ensure that messages intended for the same party arrive at the same destination.</span></span> <span data-ttu-id="0c9a0-147">Cela autorise également la « superposition » des accusés de réception de séquence sur les messages d'application.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-147">This also allows "piggy-backing" of sequence acknowledgements on application messages.</span></span> <span data-ttu-id="0c9a0-148">Par conséquent, les contraintes R1102, R1112 et R1113 s’appliquent à WCF.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-148">Therefore, constraints R1102, R1112, and R1113 apply to WCF.</span></span>  
  
 <span data-ttu-id="0c9a0-149">Exemple de message `CreateSequence`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-149">An example of a `CreateSequence` message.</span></span>  
  
```xml  
<s:Envelope>  
  <s:Header>  
    <wsa:Action s:mustUnderstand="1">http://docs.oasis-open.org/ws-rx/wsrm/200702/CreateSequence</wsa:Action>  
    <wsa:MessageID>urn:uuid:949cca61-8813-42ff-ab33-18d9e3fa82fa</wsa:MessageID>  
    <wsa:ReplyTo>  
        <wsa:Address>http://Business456.com/clientA</wsa:Address>   
    </wsa:ReplyTo>  
    <wsa:To s:mustUnderstand="1">http://BusinessABC.com/serviceA</wsa:To>  
  </s:Header>  
  <s:Body>  
    <wsrm:CreateSequence>  
      <wsrm:AcksTo>  
        <wsa:Address>http://Business456.com/clientA</wsa:Address>  
      </wsrm:AcksTo>  
      <wsrm:Offer>  
        <wsrm:Identifier>urn:uuid:066b4730-fc82-458a-a5c1-210be4fb4e4e</wsrm:Identifier>  
        <wsrm:Endpoint>  
          <wsa:Address>http://Business456.com/clientA</wsa:Address>  
        </wsrm:Endpoint>  
        <wsrm:IncompleteSequenceBehavior>DiscardFollowingFirstGap</wsrm:IncompleteSequenceBehavior>  
      </wsrm:Offer>  
    </wsrm:CreateSequence>  
  </s:Body>  
</s:Envelope>  
```  
  
 <span data-ttu-id="0c9a0-150">Exemple de message `CreateSequenceResponse`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-150">An example of a `CreateSequenceResponse` message.</span></span>  
  
```xml  
<s:Envelope>  
  <s:Header>  
    <wsa:Action s:mustUnderstand="1">http://docs.oasis-open.org/ws-rx/wsrm/200702/CreateSequenceResponse</wsa:Action>  
    <wsa:RelatesTo>urn:uuid:949cca61-8813-42ff-ab33-18d9e3fa82fa</wsa:RelatesTo>  
    <wsa:To s:mustUnderstand="1">http://Business456.com/clientA</wsa:To>  
  </s:Header>  
  <s:Body>  
    <wsrm:CreateSequenceResponse>  
      <wsrm:Identifier>urn:uuid:656652b8-9af2-4e94-9d07-2dc21c05ed27</wsrm:Identifier>  
      <wsrm:IncompleteSequenceBehavior>DiscardFollowingFirstGap</wsrm:IncompleteSequenceBehavior>  
      <wsrm:Accept>  
        <wsrm:AcksTo>  
          <wsa:Address>http://BusinessABC.com/serviceA</wsa:Address>  
        </wsrm:AcksTo>  
      </wsrm:Accept>  
    </wsrm:CreateSequenceResponse>  
  </s:Body>  
</s:Envelope>  
```  
  
### <a name="closing-a-sequence"></a><span data-ttu-id="0c9a0-151">Fermeture d'une séquence</span><span class="sxs-lookup"><span data-stu-id="0c9a0-151">Closing a Sequence</span></span>  
 <span data-ttu-id="0c9a0-152">WCF utilise le `CloseSequence` et `CloseSequenceResponse` messages pour un arrêt initié par la source de messagerie fiable.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-152">WCF uses the `CloseSequence` and `CloseSequenceResponse` messages for a Reliable Messaging source-initiated shutdown.</span></span> <span data-ttu-id="0c9a0-153">La destination de messagerie fiable de WCF n’initie pas l’arrêt et la source de messagerie fiable WCF ne prend pas en charge un arrêt initié par la destination de messagerie fiable.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-153">The WCF Reliable Messaging destination does not initiate shutdown and the WCF Reliable Messaging source does not support a Reliable Messaging destination-initiated shutdown.</span></span> <span data-ttu-id="0c9a0-154">Les contraintes suivantes s'appliquent :</span><span class="sxs-lookup"><span data-stu-id="0c9a0-154">The following constraints apply:</span></span>  
  
-   <span data-ttu-id="0c9a0-155">B1201 : La source de messagerie fiable WCF envoie toujours un `CloseSequence` message pour arrêter la séquence.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-155">B1201: The WCF Reliable Messaging source always sends a `CloseSequence` message to shut down the sequence.</span></span>  
  
-   <span data-ttu-id="0c9a0-156">B1202 : La source de messagerie fiable attend un accusé de réception de la gamme complète des messages de séquence avant d’envoyer le `CloseSequence` message.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-156">B1202: The Reliable Messaging source waits for acknowledgement of the full range of sequence messages before sending the `CloseSequence` message.</span></span>  
  
-   <span data-ttu-id="0c9a0-157">B1203 : La source de messagerie fiable inclut toujours le paramètre facultatif `LastMsgNumber` élément, sauf si la séquence ne contient pas de messages.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-157">B1203: The Reliable Messaging source always includes the optional `LastMsgNumber` element unless the sequence does not contain messages.</span></span>  
  
-   <span data-ttu-id="0c9a0-158">R1204 : La destination de messagerie fiable ne doit pas lancer arrêt en envoyant un `CloseSequence` message.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-158">R1204: The Reliable Messaging destination must not initiate shutdown by sending a `CloseSequence` message.</span></span>  
  
-   <span data-ttu-id="0c9a0-159">B1205 : À la réception une `CloseSequence` message, la source de messagerie fiable WCF considère que la séquence est incomplète et envoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-159">B1205: Upon receiving a `CloseSequence` message, the WCF Reliable Messaging source considers the sequence incomplete and sends a fault.</span></span>  
  
 <span data-ttu-id="0c9a0-160">Exemple de message `CloseSequence`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-160">An example of a `CloseSequence` message.</span></span>  
  
```xml  
<s:Envelope>  
  <s:Header>  
    <wsa:Action s:mustUnderstand="1">http://docs.oasis-open.org/ws-rx/wsrm/200702/CloseSequence</wsa:Action>  
    <wsa:MessageID>urn:uuid:6ce1d4c3-e1c1-474f-a8c9-4210e37f7877</wsa:MessageID>  
    <wsa:ReplyTo>  
      <wsa:Address>http://Business456.com/clientA</wsa:Address>  
    </wsa:ReplyTo>  
    <wsa:To s:mustUnderstand="1">http://BusinessABC.com/serviceA</wsa:To>  
  </s:Header>  
  <s:Body>  
    <wsrm:CloseSequence>  
      <wsrm:Identifier>urn:uuid:656652b8-9af2-4e94-9d07-2dc21c05ed27</wsrm:Identifier>  
      <wsrm:LastMsgNumber>30</wsrm:LastMsgNumber>  
    </wsrm:CloseSequence>  
  </s:Body>  
</s:Envelope>  
Example CloseSequenceResponse message:  
<s:Envelope>  
  <s:Header>  
    <wsrm:SequenceAcknowledgement>  
      <wsrm:Identifier>urn:uuid:656652b8-9af2-4e94-9d07-2dc21c05ed27</wsrm:Identifier>  
      <wsrm:AcknowledgementRange Lower="1" Upper="30"></wsrm:AcknowledgementRange>  
      <wsrm:Final></wsrm:Final>  
      <netrm:BufferRemaining>8</netrm:BufferRemaining>  
    </wsrm:SequenceAcknowledgement>  
    <wsa:Action s:mustUnderstand="1">http://docs.oasis-open.org/ws-rx/wsrm/200702/CloseSequenceResponse</wsa:Action>  
    <wsa:RelatesTo>urn:uuid:6ce1d4c3-e1c1-474f-a8c9-4210e37f7877</wsa:RelatesTo>  
    <wsa:To s:mustUnderstand="1">http://Business456.com/clientA</wsa:To>  
  </s:Header>  
  <s:Body>  
    <wsrm:CloseSequenceResponse>  
      <wsrm:Identifier>urn:uuid:656652b8-9af2-4e94-9d07-2dc21c05ed27</wsrm:Identifier>  
    </wsrm:CloseSequenceResponse>  
  </s:Body>  
</s:Envelope>  
```  
  
### <a name="sequence-termination"></a><span data-ttu-id="0c9a0-161">Séquence d'arrêt</span><span class="sxs-lookup"><span data-stu-id="0c9a0-161">Sequence Termination</span></span>  
 <span data-ttu-id="0c9a0-162">WCF utilise principalement le `TerminateSequence/TerminateSequenceResponse` la négociation de la fin de la `CloseSequence/CloseSequenceResponse` protocole de transfert.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-162">WCF primarily uses the `TerminateSequence/TerminateSequenceResponse` handshake after completing the `CloseSequence/CloseSequenceResponse` handshake.</span></span> <span data-ttu-id="0c9a0-163">La destination de messagerie fiable de WCF n’initie pas l’arrêt et la source de messagerie fiable ne prend pas en charge un arrêt initié par la destination de messagerie fiable.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-163">The WCF Reliable Messaging destination does not initiate termination and the Reliable Messaging source does not support a Reliable Messaging destination-initiated termination.</span></span> <span data-ttu-id="0c9a0-164">Les contraintes suivantes s'appliquent :</span><span class="sxs-lookup"><span data-stu-id="0c9a0-164">The following constraints apply:</span></span>  
  
-   <span data-ttu-id="0c9a0-165">B1301 : L’initiateur WCF envoie uniquement le `TerminateSequence` message après la réussite de la `CloseSequence/CloseSequenceResponse` protocole de transfert.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-165">B1301: The WCF Initiator only sends the `TerminateSequence` message after the successful completion of the `CloseSequence/CloseSequenceResponse` handshake.</span></span>  
  
-   <span data-ttu-id="0c9a0-166">R1302 : WCF valide le fait que le `LastMsgNumber` élément est cohérent dans tous les `CloseSequence` et `TerminateSequence` messages pour une séquence donnée.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-166">R1302: WCF validates that the `LastMsgNumber` element is consistent across all `CloseSequence` and `TerminateSequence` messages for a given sequence.</span></span> <span data-ttu-id="0c9a0-167">Cela signifie que `LastMsgNumber` est soit absent sur tous les messages `CloseSequence` et `TerminateSequence`, soit présent et identique sur tous les messages `CloseSequence` et `TerminateSequence`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-167">This means that `LastMsgNumber` is either not present on all `CloseSequence` and `TerminateSequence` messages, or it is present and identical on all `CloseSequence` and `TerminateSequence` messages.</span></span>  
  
-   <span data-ttu-id="0c9a0-168">B1303 : Lors de la réception une `TerminateSequence` message après le `CloseSequence/CloseSequenceResponse` protocole de transfert, la destination de messagerie fiable répond avec un `TerminateSequenceResponse` message.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-168">B1303: When receiving a `TerminateSequence` message after the `CloseSequence/CloseSequenceResponse` handshake, the Reliable Messaging destination responds with a `TerminateSequenceResponse` message.</span></span> <span data-ttu-id="0c9a0-169">Étant donné que la source de messagerie fiable a l'accusé de réception final avant d'envoyer le message `TerminateSequence`, la destination de messagerie fiable sait sans doute que la séquence se termine, et libère immédiatement les ressources.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-169">Because the Reliable Messaging source has the final acknowledgement before sending the `TerminateSequence` message, the Reliable Messaging destination knows without doubt that the sequence ends, and reclaims resources immediately.</span></span>  
  
-   <span data-ttu-id="0c9a0-170">B1304 : Lors de la réception une `TerminateSequence` message antérieures à la `CloseSequence/CloseSequenceResponse` protocole de transfert, la destination de messagerie fiable WCF répond avec un `TerminateSequenceResponse` message.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-170">B1304: When receiving a `TerminateSequence` message prior to the `CloseSequence/CloseSequenceResponse` handshake, the WCF Reliable Messaging destination responds with a `TerminateSequenceResponse` message.</span></span> <span data-ttu-id="0c9a0-171">Si la destination de messagerie fiable détermine que la séquence ne contient aucune incohérence, elle attend l'heure spécifiée par la destination d'une application avant de libérer des ressources afin de permettre au client de recevoir l'accusé de réception final.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-171">If the Reliable Messaging destination determines that there are no inconsistencies in the sequence, the Reliable Messaging destination waits for an application destination-specified time before reclaiming resources, to allow the client the chance to receive the final acknowledgement.</span></span> <span data-ttu-id="0c9a0-172">Sinon, la destination de messagerie fiable libère immédiatement des ressources et indique à la destination d'application que la séquence se termine en déclenchant l'événement `Faulted`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-172">Otherwise, the Reliable Messaging destination reclaims resources immediately and indicates to the application destination that the sequence ends with doubt by raising the `Faulted` event.</span></span>  
  
 <span data-ttu-id="0c9a0-173">Exemple de message `TerminateSequence`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-173">An example of a `TerminateSequence` message.</span></span>  
  
```xml  
<s:Envelope>  
  <s:Header>  
    <wsa:Action s:mustUnderstand="1">http://docs.oasis-open.org/ws-rx/wsrm/200702/TerminateSequence</wsa:Action>  
    <wsa:MessageID>urn:uuid:3597a398-4f3c-40f4-9335-8f1515572fdf</wsa:MessageID>  
    <wsa:ReplyTo>  
      <wsa:Address>http://Business456.com/clientA</wsa:Address>  
    </wsa:ReplyTo>  
    <wsa:To s:mustUnderstand="1">http://BusinessABC.com/serviceA</wsa:To>  
  </s:Header>  
  <s:Body>  
    <wsrm:TerminateSequence>  
      <wsrm:Identifier>urn:uuid:656652b8-9af2-4e94-9d07-2dc21c05ed27</wsrm:Identifier>  
      <wsrm:LastMsgNumber>30</wsrm:LastMsgNumber>  
      </wsrm:TerminateSequence>  
  </s:Body>  
</s:Envelope>  
Example TerminateSequenceResponse message:  
<s:Envelope>  
  <s:Header>  
    <wsrm:SequenceAcknowledgement>  
      <wsrm:Identifier>urn:uuid:656652b8-9af2-4e94-9d07-2dc21c05ed27</wsrm:Identifier>  
      <wsrm:AcknowledgementRange Lower="1" Upper="30"></wsrm:AcknowledgementRange>  
      <wsrm:Final></wsrm:Final>  
      <netrm:BufferRemaining>8</netrm:BufferRemaining>  
    </wsrm:SequenceAcknowledgement>  
    <wsa:Action s:mustUnderstand="1">http://docs.oasis-open.org/ws-rx/wsrm/200702/TerminateSequenceResponse</wsa:Action>  
    <wsa:RelatesTo>urn:uuid:3597a398-4f3c-40f4-9335-8f1515572fdf</wsa:RelatesTo>  
    <wsa:To s:mustUnderstand="1">://Business456.com/clientA</wsa:To>  
  </s:Header>  
  <s:Body>  
    <wsrm:TerminateSequenceResponse>  
      <wsrm:Identifier>urn:uuid:656652b8-9af2-4e94-9d07-2dc21c05ed27</wsrm:Identifier>  
    </wsrm:TerminateSequenceResponse>  
  </s:Body>  
</s:Envelope>  
```  
  
### <a name="sequences"></a><span data-ttu-id="0c9a0-174">Séquences</span><span class="sxs-lookup"><span data-stu-id="0c9a0-174">Sequences</span></span>  
 <span data-ttu-id="0c9a0-175">Voici une liste des contraintes qui s'appliquent aux séquences :</span><span class="sxs-lookup"><span data-stu-id="0c9a0-175">The following is a list of constraints that apply to sequences:</span></span>  
  
-   <span data-ttu-id="0c9a0-176">B1401:WCF génère et ne dépassant pas de numéros de séquence d’accès `xs:long`de valeur maximale, 9223372036854775807.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-176">B1401:WCF generates and accesses sequence numbers no higher than `xs:long`’s maximum inclusive value, 9223372036854775807.</span></span>  
  
 <span data-ttu-id="0c9a0-177">Exemple d'en-tête `Sequence`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-177">An example of a `Sequence` header.</span></span>  
  
```xml  
<wsrm:Sequence s:mustUnderstand="1">  
  <wsrm:Identifier>urn:uuid:656652b8-9af2-4e94-9d07-2dc21c05ed27</wsrm:Identifier>  
  <wsrm:MessageNumber>1</wsrm:MessageNumber>  
</wsrm:Sequence>  
```  
  
### <a name="request-acknowledgement"></a><span data-ttu-id="0c9a0-178">Demander un accusé de réception</span><span class="sxs-lookup"><span data-stu-id="0c9a0-178">Request Acknowledgement</span></span>  
 <span data-ttu-id="0c9a0-179">WCF utilise le `AckRequested` en-tête comme un mécanisme keep-alive.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-179">WCF uses the `AckRequested` header as a keep-alive mechanism.</span></span>  
  
 <span data-ttu-id="0c9a0-180">Exemple d'en-tête `AckRequested`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-180">An example of an `AckRequested` header.</span></span>  
  
```xml  
<wsrm:AckRequested>  
  <wsrm:Identifier>urn:uuid:656652b8-9af2-4e94-9d07-2dc21c05ed27</wsrm:Identifier>  
</wsrm:AckRequested>  
```  
  
### <a name="sequenceacknowledgement"></a><span data-ttu-id="0c9a0-181">SequenceAcknowledgement</span><span class="sxs-lookup"><span data-stu-id="0c9a0-181">SequenceAcknowledgement</span></span>  
 <span data-ttu-id="0c9a0-182">WCF utilise un mécanisme de « superposition » des accusés de réception de séquence fournis dans la messagerie WS-Reliable.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-182">WCF uses a "piggy-back" mechanism for sequence acknowledgements provided in WS-Reliable Messaging.</span></span> <span data-ttu-id="0c9a0-183">Les contraintes suivantes s'appliquent :</span><span class="sxs-lookup"><span data-stu-id="0c9a0-183">The following constraints apply:</span></span>  
  
-   <span data-ttu-id="0c9a0-184">R1601 : Lorsque deux séquences réciproques sont établies à l’aide de la `Offer` mécanisme, le `SequenceAcknowledgement` en-tête peut être inclus dans n’importe quel message d’application transmis au destinataire prévu.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-184">R1601: When two converse sequences are established using the `Offer` mechanism, the `SequenceAcknowledgement` header may be included in any application message transmitted to the intended recipient.</span></span> <span data-ttu-id="0c9a0-185">Le point de terminaison distant doit être en mesure d'accéder à un en-tête `SequenceAcknowledgement` superposé.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-185">The remote endpoint must be able to access a piggybacked `SequenceAcknowledgement` header.</span></span>  
  
-   <span data-ttu-id="0c9a0-186">B1602 : WCF ne génère pas `SequenceAcknowledgement` en-têtes contenant `Nack` éléments.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-186">B1602: WCF does not generate `SequenceAcknowledgement` headers that contain `Nack` elements.</span></span> <span data-ttu-id="0c9a0-187">WCF valide que chaque `Nack` élément contient un numéro de séquence, mais sinon ignore le `Nack` élément et valeur.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-187">WCF validates that each `Nack` element contains a sequence number, but otherwise ignores the `Nack` element and value.</span></span>  
  
 <span data-ttu-id="0c9a0-188">Exemple d'en-tête `SequenceAcknowledgement`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-188">An example of a `SequenceAcknowledgement` header.</span></span>  
  
```xml  
<wsrm:SequenceAcknowledgement>  
  <wsrm:Identifier>urn:uuid:656652b8-9af2-4e94-9d07-2dc21c05ed27</wsrm:Identifier>  
  <wsrm:AcknowledgementRange Lower="1" Upper="1"></wsrm:AcknowledgementRange>  
</wsrm:SequenceAcknowledgement>  
```  
  
### <a name="ws-reliablemessaging-faults"></a><span data-ttu-id="0c9a0-189">Erreurs de la messagerie WS-Reliable</span><span class="sxs-lookup"><span data-stu-id="0c9a0-189">WS-ReliableMessaging Faults</span></span>  
 <span data-ttu-id="0c9a0-190">Voici une liste de contraintes qui s’appliquent à l’implémentation WCF d’erreurs de WS-ReliableMessaging.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-190">The following is a list of constraints that apply to the WCF implementation of WS-ReliableMessaging faults.</span></span> <span data-ttu-id="0c9a0-191">Les contraintes suivantes s'appliquent :</span><span class="sxs-lookup"><span data-stu-id="0c9a0-191">The following constraints apply:</span></span>  
  
-   <span data-ttu-id="0c9a0-192">B1701 : WCF ne génère pas `MessageNumberRollover` erreurs.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-192">B1701: WCF does not generate `MessageNumberRollover` faults.</span></span>  
  
-   <span data-ttu-id="0c9a0-193">B1702 : Sur SOAP 1.2, lorsque le point de terminaison de service atteint sa limite de connexion et ne peut pas traiter les nouvelles connexions, WCF génère imbriquée `CreateSequenceRefused` sous-code, d’erreur `netrm:ConnectionLimitReached`, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-193">B1702: Over SOAP 1.2, when the service endpoint reaches its connection limit and cannot process new connections, WCF generates a nested `CreateSequenceRefused` fault subcode, `netrm:ConnectionLimitReached`, as shown in the following example.</span></span>  
  
```xml  
<s:Envelope>  
  <s:Header>  
    <wsa:Action>http://docs.oasis-open.org/ws-rx/wsrm/200702/fault</wsa:Action>  
  </s:Header>  
  <s:Body>  
    <s:Fault>  
      <s:Code>  
        <s:Value>s:Receiver</s:Value>  
        <s:Subcode>  
          <s:Value>wsrm:CreateSequenceRefused</s:Value>  
          <s:Subcode>  
            <s:Value>netrm:ConnectionLimitReached</s:Value>  
          </s:Subcode>  
        </s:Subcode>  
      </s:Code>  
      <s:Reason>  
        <s:Text xml:lang="en">Server 'http://BusinessABC.com/serviceA' is too busy to process this request. Try again later.</s:Text>  
      </s:Reason>  
    </s:Fault>  
  </s:Body>  
</s:Envelope>  
```  
  
### <a name="ws-addressing-faults"></a><span data-ttu-id="0c9a0-194">Erreurs WS-Addressing</span><span class="sxs-lookup"><span data-stu-id="0c9a0-194">WS-Addressing Faults</span></span>  
 <span data-ttu-id="0c9a0-195">Étant donné que WS-ReliableMessaging utilise WS-Addressing, l’implémentation de WCF WS-ReliableMessaging peut générer et transmettre des erreurs WS-Addressing.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-195">Because WS-ReliableMessaging uses WS-Addressing, the WCF WS-ReliableMessaging implementation may generate and transmit WS-Addressing faults.</span></span> <span data-ttu-id="0c9a0-196">Cette section décrit les erreurs WS-Addressing que WCF génère et transmet au niveau de la couche WS-ReliableMessaging explicitement :</span><span class="sxs-lookup"><span data-stu-id="0c9a0-196">This section covers the WS-Addressing faults that WCF explicitly generates and transmits at the WS-ReliableMessaging layer:</span></span>  
  
-   <span data-ttu-id="0c9a0-197">B1801:WCF génère et transmet le `Message Addressing Header Required` d’erreur lorsqu’une des opérations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="0c9a0-197">B1801:WCF generates and transmits the `Message Addressing Header Required` fault when one of the following is true:</span></span>  
  
    -   <span data-ttu-id="0c9a0-198">Il manque un en-tête `CreateSequence` à un message `CloseSequence`, `TerminateSequence` ou `MessageId`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-198">A `CreateSequence`, `CloseSequence` or `TerminateSequence` message is missing a `MessageId` header.</span></span>  
  
    -   <span data-ttu-id="0c9a0-199">Il manque un en-tête `CreateSequence` à un message `CloseSequence`, `TerminateSequence` ou `ReplyTo`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-199">A `CreateSequence`, `CloseSequence` or `TerminateSequence` message is missing a `ReplyTo` header.</span></span>  
  
    -   <span data-ttu-id="0c9a0-200">Il manque un en-tête `CreateSequenceResponse` à un message `CloseSequenceResponse`, `TerminateSequenceResponse` ou `RelatesTo`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-200">A `CreateSequenceResponse`, `CloseSequenceResponse`, or `TerminateSequenceResponse` message is missing a `RelatesTo` header.</span></span>  
  
-   <span data-ttu-id="0c9a0-201">B1802:WCF génère et transmet le `Endpoint Unavailable` indiquer il n’y a aucun point de terminaison qui écoute la panne peut traiter la séquence en fonction de l’examen des en-têtes d’adressage dans le `CreateSequence` message.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-201">B1802:WCF generates and transmits the `Endpoint Unavailable` fault to indicate there is no endpoint listening that can process the sequence based on examination of the addressing headers in the `CreateSequence` message.</span></span>  
  
## <a name="protocol-composition"></a><span data-ttu-id="0c9a0-202">Composition du protocole</span><span class="sxs-lookup"><span data-stu-id="0c9a0-202">Protocol Composition</span></span>  
  
### <a name="composition-with-ws-addressing"></a><span data-ttu-id="0c9a0-203">Composition avec WS-Addressing</span><span class="sxs-lookup"><span data-stu-id="0c9a0-203">Composition with WS-Addressing</span></span>  
 <span data-ttu-id="0c9a0-204">WCF prend en charge deux versions de WS-Addressing : WS-Addressing 2004/08 [WS-ADDR] et W3C WS-Addressing 1.0 recommandations [WS-ADDR-CORE] et [WS-ADDR-SOAP].</span><span class="sxs-lookup"><span data-stu-id="0c9a0-204">WCF supports two versions of WS-Addressing: WS-Addressing 2004/08 [WS-ADDR] and W3C WS-Addressing 1.0 Recommendations [WS-ADDR-CORE] and [WS-ADDR-SOAP].</span></span>  
  
 <span data-ttu-id="0c9a0-205">Si la spécification WS-ReliableMessaging mentionne WS-Addressing 2004/08 uniquement, elle ne limite pas la version WS-Addressing à utiliser.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-205">While the WS-ReliableMessaging specification mentions only WS-Addressing 2004/08, it does not restrict the WS-Addressing version to be used.</span></span> <span data-ttu-id="0c9a0-206">Voici une liste de contraintes qui s’appliquent à WCF :</span><span class="sxs-lookup"><span data-stu-id="0c9a0-206">The following is a list of constraints that apply to WCF:</span></span>  
  
-   <span data-ttu-id="0c9a0-207">R2101 : WS-Addressing 2004/08 et WS-Addressing 1.0 peuvent être utilisé avec la messagerie WS-Reliable.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-207">R2101: Both WS-Addressing 2004/08 and WS-Addressing 1.0 can be used with WS-Reliable Messaging.</span></span>  
  
-   <span data-ttu-id="0c9a0-208">R2102 : Une seule version de WS-Addressing doit être utilisée tout au long d’une séquence WS-ReliableMessaging donnée ou une paire de séquences réciproques corrélées à l’aide de la `Offer` mécanisme.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-208">R2102: A single version of WS-Addressing must be used throughout a given WS-ReliableMessaging sequence or a pair of converse sequences correlated by using the `Offer` mechanism.</span></span>  
  
### <a name="composition-with-soap"></a><span data-ttu-id="0c9a0-209">Composition avec SOAP</span><span class="sxs-lookup"><span data-stu-id="0c9a0-209">Composition with SOAP</span></span>  
 <span data-ttu-id="0c9a0-210">WCF prend en charge l’utilisation de SOAP 1.1 et SOAP 1.2 avec WS-Reliable Messaging.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-210">WCF supports the use of both SOAP 1.1 and SOAP 1.2 with WS-Reliable Messaging.</span></span>  
  
### <a name="composition-with-ws-security-and-ws-secureconversation"></a><span data-ttu-id="0c9a0-211">Composition avec WS-Security et WS-SecureConversation</span><span class="sxs-lookup"><span data-stu-id="0c9a0-211">Composition with WS-Security and WS-SecureConversation</span></span>  
 <span data-ttu-id="0c9a0-212">WCF fournit une protection pour les séquences de WS-ReliableMessaging à l’aide de sécurisé de Transport (HTTPS), de composition avec WS-Security et de composition avec WS-Secure Conversation.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-212">WCF provides protection for WS-ReliableMessaging sequences by using secure Transport (HTTPS), composition with WS-Security, and composition with WS-Secure Conversation.</span></span> <span data-ttu-id="0c9a0-213">Le protocole WS-ReliableMessaging 1.1, WS-Security 1.1 et le protocole WS-Secure Conversation 1.3 doivent être utilisés ensemble.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-213">The WS-ReliableMessaging 1.1 protocol, WS-Security 1.1 and WS-Secure Conversation 1.3 protocol should be used together.</span></span> <span data-ttu-id="0c9a0-214">Voici une liste de contraintes qui s’appliquent à WCF :</span><span class="sxs-lookup"><span data-stu-id="0c9a0-214">The following is a list of constraints that apply to WCF:</span></span>  
  
-   <span data-ttu-id="0c9a0-215">R2301 : Pour protéger l’intégrité d’une séquence WS-ReliableMessaging en plus de l’intégrité et la confidentialité des messages individuels, WCF requiert que WS-Secure Conversation doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-215">R2301: To protect the integrity of a WS-ReliableMessaging sequence in addition to the integrity and confidentiality of individual messages, WCF requires that WS-Secure Conversation must be used.</span></span>  
  
-   <span data-ttu-id="0c9a0-216">R2302:AWS-session Secure Conversation doit être établie avant l’établissement ou des séquences WS-ReliableMessaging.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-216">R2302:AWS-Secure Conversation session must be established prior to establishing WS-ReliableMessaging sequence(s).</span></span>  
  
-   <span data-ttu-id="0c9a0-217">R2303 : Si la durée de vie de séquence WS-ReliableMessaging dépasse WS-Secure Conversation durée de vie de session, le `SecurityContextToken` établi à l’aide de WS-Secure Conversation doit être renouvelée à l’aide de la liaison WS-Secure Conversation Renewal correspondante.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-217">R2303: If the WS-ReliableMessaging sequence lifetime exceeds the WS-Secure Conversation session’s lifetime, the `SecurityContextToken` established by using WS-Secure Conversation must be renewed by using the corresponding WS-Secure Conversation Renewal binding.</span></span>  
  
-   <span data-ttu-id="0c9a0-218">B2304:ws-séquence ReliableMessaging ou une paire de séquences réciproques corrélées est toujours liée à une seule session WS-SecureConversation.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-218">B2304:WS-ReliableMessaging sequence or a pair of correlated converse sequences are always bound to a single WS-SecureConversation session.</span></span>  
  
-   <span data-ttu-id="0c9a0-219">R2305 : Lorsqu’il est composé avec WS-Secure Conversation, le répondeur WCF requiert que le `CreateSequence` message contiennent le `wsse:SecurityTokenReference` élément et le `wsrm:UsesSequenceSTR` en-tête.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-219">R2305: When composed with WS-Secure Conversation, the WCF responder requires that the `CreateSequence` message contain the `wsse:SecurityTokenReference` element and the `wsrm:UsesSequenceSTR` header.</span></span>  
  
 <span data-ttu-id="0c9a0-220">Exemple d'en-tête `UsesSequenceSTR`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-220">An example of a `UsesSequenceSTR` header.</span></span>  
  
```xml  
<wsrm:UsesSequenceSTR></wsrm:UsesSequenceSTR>  
```  
  
### <a name="composition-with-ssltls-sessions"></a><span data-ttu-id="0c9a0-221">Composition avec les sessions SSL/TLS</span><span class="sxs-lookup"><span data-stu-id="0c9a0-221">Composition with SSL/TLS sessions</span></span>  
 <span data-ttu-id="0c9a0-222">WCF ne prend pas en charge la composition avec les sessions SSL/TLS :</span><span class="sxs-lookup"><span data-stu-id="0c9a0-222">WCF does not support composition with SSL/TLS sessions:</span></span>  
  
-   <span data-ttu-id="0c9a0-223">B2401 : WCF ne génère pas le `wsrm:UsesSequenceSSL` en-tête.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-223">B2401: WCF does not generate the `wsrm:UsesSequenceSSL` header.</span></span>  
  
-   <span data-ttu-id="0c9a0-224">R2402 : Un initiateur de messagerie fiable ne doit pas envoyer un `CreateSequence` message avec un `wsrm:UsesSequenceSSL` en-tête à un répondeur de WCF.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-224">R2402: A Reliable Messaging Initiator must not send a `CreateSequence` message with a `wsrm:UsesSequenceSSL` header to a WCF Responder.</span></span>  
  
### <a name="composition-with-ws-policy"></a><span data-ttu-id="0c9a0-225">Composition avec WS-Policy</span><span class="sxs-lookup"><span data-stu-id="0c9a0-225">Composition with WS-Policy</span></span>  
 <span data-ttu-id="0c9a0-226">WCF prend en charge deux versions de WS-Policy : WS-Policy 1.2 et WS-Policy 1.5.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-226">WCF supports two versions of WS-Policy: WS-Policy 1.2 and WS-Policy 1.5.</span></span>  
  
## <a name="ws-reliablemessaging-ws-policy-assertion"></a><span data-ttu-id="0c9a0-227">Assertion WS-Policy de la messagerie WS-ReliableMessaging</span><span class="sxs-lookup"><span data-stu-id="0c9a0-227">WS-ReliableMessaging WS-Policy Assertion</span></span>  
 <span data-ttu-id="0c9a0-228">WCF utilise l’Assertion de WS-Policy WS-ReliableMessaging `wsrm:RMAssertion` pour décrire les capacités de points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-228">WCF uses WS-ReliableMessaging WS-Policy Assertion `wsrm:RMAssertion` to describe endpoints capabilities.</span></span> <span data-ttu-id="0c9a0-229">Voici une liste de contraintes qui s’appliquent à WCF :</span><span class="sxs-lookup"><span data-stu-id="0c9a0-229">The following is a list of constraints that apply to WCF:</span></span>  
  
-   <span data-ttu-id="0c9a0-230">B3001 : WCF attache `wsrmn:RMAssertion` WS-Policy Assertion aux `wsdl:binding` éléments.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-230">B3001: WCF attaches `wsrmn:RMAssertion` WS-Policy Assertion to `wsdl:binding` elements.</span></span> <span data-ttu-id="0c9a0-231">WCF prend en charge des pièces jointes aux `wsdl:binding` et `wsdl:port` éléments.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-231">WCF supports both attachments to `wsdl:binding` and `wsdl:port` elements.</span></span>  
  
-   <span data-ttu-id="0c9a0-232">B3002 : WCF ne génère jamais le `wsp:Optional` balise.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-232">B3002: WCF never generates the `wsp:Optional` tag.</span></span>  
  
-   <span data-ttu-id="0c9a0-233">B3003 : Lorsque vous accédez à la `wsrmp:RMAssertion` Assertion WS-Policy, WCF ignore le `wsp:Optional` balise et traite la stratégie WS-RM comme obligatoire.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-233">B3003: When accessing the `wsrmp:RMAssertion` WS-Policy Assertion, WCF ignores the `wsp:Optional` tag and treats the WS-RM policy as mandatory.</span></span>  
  
-   <span data-ttu-id="0c9a0-234">R3004 : Étant donné que WCF ne compose pas avec les sessions SSL/TLS, WCF n’accepte pas de stratégie spécifie `wsrmp:SequenceTransportSecurity`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-234">R3004: Because WCF does not compose with SSL/TLS sessions, WCF does not accept policy that specifies `wsrmp:SequenceTransportSecurity`.</span></span>  
  
-   <span data-ttu-id="0c9a0-235">B3005 : WCF génère toujours la `wsrmp:DeliveryAssurance` élément.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-235">B3005: WCF always generates the `wsrmp:DeliveryAssurance` element.</span></span>  
  
-   <span data-ttu-id="0c9a0-236">B3006 : WCF spécifie toujours le `wsrmp:ExactlyOnce` garantie de remise.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-236">B3006: WCF always specifies the `wsrmp:ExactlyOnce` delivery assurance.</span></span>  
  
-   <span data-ttu-id="0c9a0-237">B3007 : WCF génère et lit les propriétés suivantes de l’assertion WS-ReliableMessaging et assure leur contrôle sur WCF`ReliableSessionBindingElement`:</span><span class="sxs-lookup"><span data-stu-id="0c9a0-237">B3007: WCF generates and reads the following properties of the WS-ReliableMessaging assertion and provides control over them on the WCF`ReliableSessionBindingElement`:</span></span>  
  
    -   `netrmp:InactivityTimeout`  
  
    -   `netrmp:AcknowledgementInterval`  
  
     <span data-ttu-id="0c9a0-238">Exemple de `RMAssertion`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-238">An example of a `RMAssertion`.</span></span>  
  
    ```xml  
    <wsrmp:RMAssertion>  
      <wsp:Policy>  
        <wsrmp:SequenceSTR/>  
        <wsrmp:DeliveryAssurance>  
          <wsp:Policy>  
            <wsrmp:ExactlyOnce/>  
            <wsrmp:InOrder/>  
          </wsp:Policy>  
        </wsrmp:DeliveryAssurance>  
      </wsp:Policy>  
      <netrmp:InactivityTimeout Milliseconds="600000"/>  
      <netrmp:AcknowledgementInterval Milliseconds="200"/>  
    </wsrmp:RMAssertion>  
    ```  
  
## <a name="flow-control-ws-reliablemessaging-extension"></a><span data-ttu-id="0c9a0-239">Extension de messagerie WS-Reliable pour le contrôle de flux</span><span class="sxs-lookup"><span data-stu-id="0c9a0-239">Flow Control WS-ReliableMessaging Extension</span></span>  
 <span data-ttu-id="0c9a0-240">WCF utilise WS-ReliableMessaging extensibilité pour renforcer le contrôle facultatif sur le flux de message de séquence.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-240">WCF uses WS-ReliableMessaging extensibility to provide optional additional tighter control over sequence message flow.</span></span>  
  
 <span data-ttu-id="0c9a0-241">Contrôle de flux est activé en définissant le <xref:System.ServiceModel.Channels.ReliableSessionBindingElement.FlowControlEnabled?displayProperty=nameWithType> propriété `true`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-241">Flow control is enabled by setting the <xref:System.ServiceModel.Channels.ReliableSessionBindingElement.FlowControlEnabled?displayProperty=nameWithType> property to `true`.</span></span> <span data-ttu-id="0c9a0-242">Voici une liste de contraintes qui s’appliquent à WCF :</span><span class="sxs-lookup"><span data-stu-id="0c9a0-242">The following is a list of constraints that apply to WCF:</span></span>  
  
-   <span data-ttu-id="0c9a0-243">B4001 : Lorsque le contrôle de flux de messagerie fiable est activé, WCF génère un `netrm:BufferRemaining` élément dans l’élément d’extensibilité de la `SequenceAcknowledgement` en-tête, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-243">B4001: When Reliable Messaging Flow Control is enabled, WCF generates a `netrm:BufferRemaining` element in the element extensibility of the `SequenceAcknowledgement` header, as shown in the following example.</span></span>  
  
    ```xml  
    <wsrm:SequenceAcknowledgement>  
      <wsrm:Identifier>urn:uuid:656652b8-9af2-4e94-9d07-2dc21c05ed27</wsrm:Identifier>  
      <wsrm:AcknowledgementRange Upper="1" Lower="1"/>             
      <netrm:BufferRemaining>8</netrm:BufferRemaining>  
    </wsrm:SequenceAcknowledgement>  
    ```  
  
-   <span data-ttu-id="0c9a0-244">B4002 : Même lorsque contrôle de flux de messagerie fiable est activé, WCF ne nécessite pas un `netrm:BufferRemaining` élément dans le `SequenceAcknowledgement` en-tête.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-244">B4002: Even when Reliable Messaging Flow Control is enabled, WCF does not require a `netrm:BufferRemaining` element in the `SequenceAcknowledgement` header.</span></span>  
  
-   <span data-ttu-id="0c9a0-245">B4003 : Destination de messagerie fiable WCF utilise `netrm:BufferRemaining` pour indiquer combien de nouveaux messages elle peut mettre en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-245">B4003: WCF Reliable Messaging Destination uses `netrm:BufferRemaining` to indicate how many new messages it can buffer.</span></span>  
  
-   <span data-ttu-id="0c9a0-246">B4004:when fiable de flux de contrôle de messagerie est activé, la Source de messagerie fiable WCF utilise la valeur de `netrm:BufferRemaining` pour limiter la transmission des messages.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-246">B4004:When Reliable Messaging Flow Control is enabled, the WCF Reliable Messaging Source uses the value of `netrm:BufferRemaining` to throttle message transmission.</span></span>  
  
-   <span data-ttu-id="0c9a0-247">B4005 : WCF génère `netrm:BufferRemaining` entier des valeurs comprises entre 0 et inclusif de 4096 et lit les valeurs de nombre entier compris entre 0 et `xs:int`de `maxInclusive` valeur 214748364 inclusif.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-247">B4005: WCF generates `netrm:BufferRemaining` integer values between 0 and 4096 inclusive, and reads integer values between 0 and `xs:int`’s `maxInclusive` value 214748364 inclusive.</span></span>  
  
## <a name="message-exchange-patterns"></a><span data-ttu-id="0c9a0-248">Modèles d’échange de messages</span><span class="sxs-lookup"><span data-stu-id="0c9a0-248">Message Exchange Patterns</span></span>  
 <span data-ttu-id="0c9a0-249">Cette section décrit le comportement de WCF lorsque WS-ReliableMessaging est utilisé pour différents modèles d’échange de Message.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-249">This section describes WCF's behavior when WS-ReliableMessaging is used for different Message Exchange Patterns.</span></span> <span data-ttu-id="0c9a0-250">Pour chaque modèle d'échange de messages, les deux scénarios de déploiements suivants sont considérés :</span><span class="sxs-lookup"><span data-stu-id="0c9a0-250">For each Message Exchange Pattern the following two deployments scenarios are considered:</span></span>  
  
-   <span data-ttu-id="0c9a0-251">Initiateur non adressable : L’initiateur est derrière un pare-feu ; Répondeur peut remettre des messages à l’initiateur uniquement sur les réponses HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-251">Non-Addressable Initiator: Initiator is behind a firewall; Responder can deliver messages to the Initiator only on HTTP responses.</span></span>  
  
-   <span data-ttu-id="0c9a0-252">Initiateur adressable : Initiateur et le répondeur peuvent recevoir des requêtes HTTP ; en d’autres termes, les deux connexions HTTP réciproques peuvent être établies.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-252">Addressable Initiator: Initiator and Responder both can be sent HTTP requests; in other words, two converse HTTP connections can be established.</span></span>  
  
### <a name="one-way-non-addressable-initiator"></a><span data-ttu-id="0c9a0-253">Initiateur unidirectionnel, non adressable</span><span class="sxs-lookup"><span data-stu-id="0c9a0-253">One-way, Non-addressable Initiator</span></span>  
  
#### <a name="binding"></a><span data-ttu-id="0c9a0-254">Liaison</span><span class="sxs-lookup"><span data-stu-id="0c9a0-254">Binding</span></span>  
 <span data-ttu-id="0c9a0-255">WCF fournit un modèle d’échange de messages unidirectionnel à l’aide d’une séquence sur un canal HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-255">WCF provides a one-way message exchange pattern using one sequence over one HTTP channel.</span></span> <span data-ttu-id="0c9a0-256">WCF utilise les requêtes HTTP pour transmettre tous les messages à partir de l’initiateur pour les répondeur et les réponses HTTP pour transmettre les messages du répondeur à l’initiateur.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-256">WCF uses HTTP requests to transmit all messages from the Initiator to the Responder and HTTP responses to transmit all messages from the Responder to the Initiator.</span></span>  
  
#### <a name="createsequence-exchange"></a><span data-ttu-id="0c9a0-257">Échange CreateSequence</span><span class="sxs-lookup"><span data-stu-id="0c9a0-257">CreateSequence Exchange</span></span>  
 <span data-ttu-id="0c9a0-258">L’initiateur de WCF transmet un `CreateSequence` message sans aucune `Offer` élément sur une requête HTTP et attend le `CreateSequenceResponse` message sur la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-258">The WCF Initiator transmits a `CreateSequence` message with no `Offer` element on an HTTP request and expects the `CreateSequenceResponse` message on the HTTP response.</span></span> <span data-ttu-id="0c9a0-259">Le répondeur WCF crée une séquence et transmet le `CreateSequenceResponse` message sans aucune `Accept` élément sur la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-259">The WCF Responder creates a sequence and transmits the `CreateSequenceResponse` message with no `Accept` element on the HTTP response.</span></span>  
  
#### <a name="sequenceacknowledgement"></a><span data-ttu-id="0c9a0-260">SequenceAcknowledgement</span><span class="sxs-lookup"><span data-stu-id="0c9a0-260">SequenceAcknowledgement</span></span>  
 <span data-ttu-id="0c9a0-261">L’initiateur WCF traite les accusés de réception sur la réponse de tous les messages sauf le `CreateSequence` message et les messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-261">The WCF Initiator processes acknowledgements on the reply of all messages except the `CreateSequence` message and fault messages.</span></span> <span data-ttu-id="0c9a0-262">Le répondeur de WCF transmet toujours un accusé de réception autonome sur la réponse HTTP à tous les séquence et `AckRequested` messages.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-262">The WCF Responder always transmits a stand-alone acknowledgement on the HTTP response to all sequence and `AckRequested` messages.</span></span>  
  
#### <a name="closesequence-exchange"></a><span data-ttu-id="0c9a0-263">Échange CloseSequence</span><span class="sxs-lookup"><span data-stu-id="0c9a0-263">CloseSequence Exchange</span></span>  
 <span data-ttu-id="0c9a0-264">L’initiateur de WCF transmet un `CloseSequence` message sur une requête HTTP et attend le `CreateSequenceResponse` message sur la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-264">The WCF Initiator transmits a `CloseSequence` message on an HTTP request and expects the `CreateSequenceResponse` message on the HTTP response.</span></span> <span data-ttu-id="0c9a0-265">Le répondeur de WCF transmet le `CloseSequenceResponse` message sur la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-265">The WCF Responder transmits the `CloseSequenceResponse` message on the HTTP response.</span></span>  
  
#### <a name="terminatesequence-exchange"></a><span data-ttu-id="0c9a0-266">Échange TerminateSequence</span><span class="sxs-lookup"><span data-stu-id="0c9a0-266">TerminateSequence Exchange</span></span>  
 <span data-ttu-id="0c9a0-267">L’initiateur de WCF transmet un `TerminateSequence` message sur une requête HTTP et attend le `TerminateSequenceResponse` message sur la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-267">The WCF Initiator transmits a `TerminateSequence` message on an HTTP request and expects the `TerminateSequenceResponse` message on the HTTP response.</span></span> <span data-ttu-id="0c9a0-268">Le répondeur de WCF transmet le `TerminateSequenceResponse` message sur la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-268">The WCF Responder transmits the `TerminateSequenceResponse` message on the HTTP response.</span></span>  
  
### <a name="one-way-addressable-initiator"></a><span data-ttu-id="0c9a0-269">Initiateur unidirectionnel, adressable</span><span class="sxs-lookup"><span data-stu-id="0c9a0-269">One Way, Addressable Initiator</span></span>  
  
#### <a name="binding"></a><span data-ttu-id="0c9a0-270">Liaison</span><span class="sxs-lookup"><span data-stu-id="0c9a0-270">Binding</span></span>  
 <span data-ttu-id="0c9a0-271">WCF fournit un modèle d’échange de messages unidirectionnel à l’aide d’une séquence sur un trafic entrant et un canal HTTP sortant.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-271">WCF provides a one-way message exchange pattern using one sequence over one inbound and one outbound HTTP channel.</span></span> <span data-ttu-id="0c9a0-272">WCF utilise les requêtes HTTP pour transmettre tous les messages.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-272">WCF uses the HTTP requests to transmit all messages.</span></span> <span data-ttu-id="0c9a0-273">Toutes les réponses HTTP ont un corps vide et le code d'état HTTP 202.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-273">All HTTP responses have an empty body and HTTP 202 status code.</span></span>  
  
#### <a name="createsequence-exchange"></a><span data-ttu-id="0c9a0-274">Échange CreateSequence</span><span class="sxs-lookup"><span data-stu-id="0c9a0-274">CreateSequence Exchange</span></span>  
 <span data-ttu-id="0c9a0-275">L’initiateur de WCF transmet un `CreateSequence` message sans aucune `Offer` élément sur une requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-275">The WCF Initiator transmits a `CreateSequence` message with no `Offer` element on an HTTP request.</span></span> <span data-ttu-id="0c9a0-276">Le répondeur WCF crée une séquence et transmet le `CreateSequenceResponse` message sans aucune `Accept` élément sur une requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-276">The WCF Responder creates a sequence and transmits the `CreateSequenceResponse` message with no `Accept` element on an HTTP request.</span></span>  
  
### <a name="duplex-addressable-initiator"></a><span data-ttu-id="0c9a0-277">Initiateur duplex, adressable</span><span class="sxs-lookup"><span data-stu-id="0c9a0-277">Duplex, Addressable Initiator</span></span>  
  
#### <a name="binding"></a><span data-ttu-id="0c9a0-278">Liaison</span><span class="sxs-lookup"><span data-stu-id="0c9a0-278">Binding</span></span>  
 <span data-ttu-id="0c9a0-279">WCF fournit un modèle d’échange de messages asynchrone complet, bidirectionnel à l’aide de deux séquences sur un trafic entrant et un canal HTTP sortant.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-279">WCF provides a fully-asynchronous, two-way message exchange pattern using two sequences over one inbound and one outbound HTTP channel.</span></span> <span data-ttu-id="0c9a0-280">Ce modèle d’échange de messages peut être combiné avec le modèle d’échange de messages initiateur `Request/Reply`, `Addressable` d’une manière limitée.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-280">This message exchange pattern can be mixed with the `Request/Reply`, `Addressable` Initiator message exchange pattern in a limited way.</span></span> <span data-ttu-id="0c9a0-281">WCF utilise les requêtes HTTP pour transmettre tous les messages.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-281">WCF uses HTTP requests to transmit all messages.</span></span> <span data-ttu-id="0c9a0-282">Toutes les réponses HTTP ont un corps vide et le code d'état HTTP 202.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-282">All HTTP responses have an empty body and HTTP 202 status code.</span></span>  
  
#### <a name="createsequence-exchange"></a><span data-ttu-id="0c9a0-283">Échange CreateSequence</span><span class="sxs-lookup"><span data-stu-id="0c9a0-283">CreateSequence Exchange</span></span>  
 <span data-ttu-id="0c9a0-284">L’initiateur de WCF transmet un `CreateSequence` message avec un `Offer` élément sur une requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-284">The WCF Initiator transmits a `CreateSequence` message with an `Offer` element on an HTTP request.</span></span> <span data-ttu-id="0c9a0-285">Le répondeur de WCF garantit que le `CreateSequence` a un `Offer` élément, puis crée une séquence et transmet le `CreateSequenceResponse` message avec un `Accept` élément.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-285">The WCF Responder ensures that the `CreateSequence` has an `Offer` element, then creates a sequence and transmits the `CreateSequenceResponse` message with an `Accept` element.</span></span>  
  
#### <a name="sequence-lifetime"></a><span data-ttu-id="0c9a0-286">Durée de vie de séquence</span><span class="sxs-lookup"><span data-stu-id="0c9a0-286">Sequence Lifetime</span></span>  
 <span data-ttu-id="0c9a0-287">WCF traite les deux séquences comme une session duplex complète.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-287">WCF treats the two sequences as one fully-duplex session.</span></span>  
  
 <span data-ttu-id="0c9a0-288">Lors de la génération d’une erreur qui fait échouer une séquence, WCF attend le point de terminaison distant d’erreur les deux séquences.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-288">Upon generating a fault that faults one sequence, WCF expects the remote endpoint to fault both sequences.</span></span> <span data-ttu-id="0c9a0-289">À la lecture d’une erreur qui fait échouer une séquence, WCF provoque des erreurs les deux séquences.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-289">Upon reading a fault that faults one sequence, WCF faults both sequences.</span></span>  
  
 <span data-ttu-id="0c9a0-290">WCF peut fermer sa séquence sortante et continuer à traiter les messages sur sa séquence entrante.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-290">WCF can close its outbound sequence and continue to process messages on its inbound sequence.</span></span> <span data-ttu-id="0c9a0-291">À l’inverse, WCF peut traiter la fermeture de la séquence entrante et continuer à envoyer des messages sur sa séquence sortante.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-291">Conversely, WCF can process the close of the inbound sequence and continue to send messages on its outbound sequence.</span></span>  
  
### <a name="request-reply-and-one-way-non-addressable-initiator"></a><span data-ttu-id="0c9a0-292">Initiateur demande-réponse, unidirectionnel et non adressable</span><span class="sxs-lookup"><span data-stu-id="0c9a0-292">Request-Reply and One-Way, Non-Addressable Initiator</span></span>  
  
#### <a name="binding"></a><span data-ttu-id="0c9a0-293">Liaison</span><span class="sxs-lookup"><span data-stu-id="0c9a0-293">Binding</span></span>  
 <span data-ttu-id="0c9a0-294">WCF fournit un unidirectionnel et modèle d’échange de message demande-réponse à l’aide de deux séquences sur un canal HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-294">WCF provides a one-way and request-reply message exchange pattern using two sequences over one HTTP channel.</span></span> <span data-ttu-id="0c9a0-295">WCF utilise les requêtes HTTP pour transmettre tous les messages à partir de l’initiateur pour les répondeur et les réponses HTTP pour transmettre les messages du répondeur à l’initiateur.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-295">WCF uses HTTP requests to transmit all messages from the Initiator to the Responder and HTTP responses to transmit all messages from the Responder to the Initiator.</span></span>  
  
#### <a name="createsequence-exchange"></a><span data-ttu-id="0c9a0-296">Échange CreateSequence</span><span class="sxs-lookup"><span data-stu-id="0c9a0-296">CreateSequence Exchange</span></span>  
 <span data-ttu-id="0c9a0-297">L’initiateur de WCF transmet un `CreateSequence` message avec un `Offer` élément sur une requête HTTP et attend le `CreateSequenceResponse` message sur la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-297">The WCF Initiator transmits a `CreateSequence` message with an `Offer` element on an HTTP request and expects the `CreateSequenceResponse` message on the HTTP response.</span></span> <span data-ttu-id="0c9a0-298">Le répondeur WCF crée une séquence et transmet le `CreateSequenceResponse` message avec un `Accept` élément sur la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-298">The WCF Responder creates a sequence and transmits the `CreateSequenceResponse` message with an `Accept` element on the HTTP response.</span></span>  
  
#### <a name="one-way-message"></a><span data-ttu-id="0c9a0-299">Message unidirectionnel</span><span class="sxs-lookup"><span data-stu-id="0c9a0-299">One-way Message</span></span>  
 <span data-ttu-id="0c9a0-300">Pour effectuer un échange de messages unidirectionnel avec succès, l’initiateur de WCF transmet un message de séquence de demande sur la requête HTTP et reçoit un autonome `SequenceAcknowledgement` message sur la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-300">To complete a one-way message exchange successfully, the WCF Initiator transmits a request sequence message on the HTTP request and receives a standalone `SequenceAcknowledgement` message on the HTTP response.</span></span> <span data-ttu-id="0c9a0-301">`SequenceAcknowledgement` doit accepter le message transmis.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-301">The `SequenceAcknowledgement` must acknowledge the message transmitted.</span></span>  
  
 <span data-ttu-id="0c9a0-302">Le répondeur WCF peut répondre à la demande avec un accusé de réception, une erreur ou une réponse avec un corps vide et le code d’état HTTP 202.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-302">The WCF Responder may reply to the request with an acknowledgement, a fault, or a response with an empty body and HTTP 202 status code.</span></span>  
  
#### <a name="two-way-messages"></a><span data-ttu-id="0c9a0-303">Messages bidirectionnels</span><span class="sxs-lookup"><span data-stu-id="0c9a0-303">Two Way Messages</span></span>  
 <span data-ttu-id="0c9a0-304">Pour terminer avec succès un protocole d’échange de messages bidirectionnel, l’initiateur de WCF transmet un message de séquence de demande sur la requête HTTP et reçoit un message de séquence de réponse sur la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-304">To complete a two way message exchange protocol successfully, the WCF Initiator transmits a request sequence message on the HTTP request and receives a reply sequence message on the HTTP response.</span></span> <span data-ttu-id="0c9a0-305">La réponse doit contenir un `SequenceAcknowledgement` qui accuse réception du message de séquence de demande transmis.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-305">The response must carry a `SequenceAcknowledgement` acknowledging the request sequence message transmitted.</span></span>  
  
 <span data-ttu-id="0c9a0-306">Le répondeur WCF peut répondre à la demande avec une réponse d’application, une erreur ou une réponse avec un corps vide et le code d’état HTTP 202.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-306">The WCF Responder may reply to the request with an application reply, a fault or a response with an empty body and HTTP 202 status code.</span></span>  
  
 <span data-ttu-id="0c9a0-307">En raison de la présence de messages unidirectionnels et du délai d'attente des réponses d'application, le numéro de séquence du message de séquence de demande et le numéro de séquence du message de réponse n'ont aucune corrélation.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-307">Because of the presence of one-way messages and the timing of application replies, the request sequence message’s sequence number and the response message’s sequence number have no correlation.</span></span>  
  
#### <a name="retrying-replies"></a><span data-ttu-id="0c9a0-308">Nouvelles tentatives de réponses</span><span class="sxs-lookup"><span data-stu-id="0c9a0-308">Retrying Replies</span></span>  
 <span data-ttu-id="0c9a0-309">WCF s’appuie sur une corrélation demande-réponse HTTP pour la corrélation protocole d’échange de messages bidirectionnel.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-309">WCF relies on HTTP request-reply correlation for two-way message exchange protocol correlation.</span></span> <span data-ttu-id="0c9a0-310">Pour cette raison, l’initiateur WCF ne s’arrête pas une nouvelle tentative d’un message de séquence de demande lorsque le message de séquence de demande est accepté mais plutôt lorsque la réponse HTTP contient un `SequenceAcknowledgement`, réponse d’application ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-310">Because of this, the WCF Initiator does not stop retrying a request sequence message when the request sequence message is acknowledged but rather when the HTTP response carries a `SequenceAcknowledgement`, application reply, or fault.</span></span> <span data-ttu-id="0c9a0-311">Le répondeur WCF réessaie des réponses sur la réponse HTTP de la demande à laquelle la réponse est corrélée.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-311">The WCF Responder retries replies on the HTTP response of the request to which the reply is correlated.</span></span>  
  
#### <a name="closesequence-exchange"></a><span data-ttu-id="0c9a0-312">Échange CloseSequence</span><span class="sxs-lookup"><span data-stu-id="0c9a0-312">CloseSequence Exchange</span></span>  
 <span data-ttu-id="0c9a0-313">Après avoir reçu tous les messages de séquence de réponse et les accusés de réception pour tous les messages de séquence de demande unidirectionnels, l’initiateur de WCF transmet un `CloseSequence` de messages pour la séquence de demande sur une requête HTTP et attend le `CloseSequenceResponse` sur la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-313">After receiving all reply sequence messages and acknowledgements for all one way request sequence messages, the WCF Initiator transmits a `CloseSequence` message for the request sequence on an HTTP request and expects the `CloseSequenceResponse` on the HTTP response.</span></span>  
  
 <span data-ttu-id="0c9a0-314">La fermeture de la séquence de demande ferme implicitement la séquence de réponse.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-314">Closing the request sequence implicitly closes the reply sequence.</span></span> <span data-ttu-id="0c9a0-315">Cela signifie que l’initiateur de WCF inclut finale la séquence de réponse `SequenceAcknowledgement` sur le `CloseSequence` message et la séquence de réponse n’a pas un `CloseSequence` exchange.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-315">This means the WCF Initiator includes the reply sequence’s Final `SequenceAcknowledgement` on the `CloseSequence` message and the reply sequence does not have a `CloseSequence` exchange.</span></span>  
  
 <span data-ttu-id="0c9a0-316">Le répondeur de WCF garantit que toutes les réponses sont acceptées et transmet le `CloseSequenceResponse` message sur la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-316">The WCF Responder ensures all replies are acknowledged and transmits the `CloseSequenceResponse` message on the HTTP response.</span></span>  
  
#### <a name="terminatesequence-exchange"></a><span data-ttu-id="0c9a0-317">Échange TerminateSequence</span><span class="sxs-lookup"><span data-stu-id="0c9a0-317">TerminateSequence Exchange</span></span>  
 <span data-ttu-id="0c9a0-318">Après avoir reçu le `CloseSequenceResponse` message, l’initiateur de WCF transmet un `TerminateSequence` de messages pour la séquence de demande sur une requête HTTP et attend le `TerminateSequenceResponse` sur la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-318">After receiving the `CloseSequenceResponse` message, the WCF Initiator transmits a `TerminateSequence` message for the request sequence on an HTTP request and expects the `TerminateSequenceResponse` on the HTTP response.</span></span>  
  
 <span data-ttu-id="0c9a0-319">Comme l'échange `CloseSequence`, terminer la séquence de demande termine implicitement la séquence de réponse.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-319">Like the `CloseSequence` exchange, terminating the request sequence implicitly terminates the reply sequence.</span></span> <span data-ttu-id="0c9a0-320">Cela signifie que l’initiateur de WCF inclut final de la séquence de réponse `SequenceAcknowledgement` sur le `TerminateSequence` message et la séquence de réponse n’a pas un `TerminateSequence` exchange.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-320">This means the WCF Initiator includes the reply sequence’s final `SequenceAcknowledgement` on the `TerminateSequence` message and the reply sequence does not have a `TerminateSequence` exchange.</span></span>  
  
 <span data-ttu-id="0c9a0-321">Le répondeur de WCF transmet le `TerminateSequenceResponse` message sur la réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-321">The WCF Responder transmits the `TerminateSequenceResponse` message on the HTTP response.</span></span>  
  
### <a name="requestreply-addressable-initiator"></a><span data-ttu-id="0c9a0-322">Initiateur demande/réponse, adressable</span><span class="sxs-lookup"><span data-stu-id="0c9a0-322">Request/Reply, Addressable Initiator</span></span>  
  
#### <a name="binding"></a><span data-ttu-id="0c9a0-323">Liaison</span><span class="sxs-lookup"><span data-stu-id="0c9a0-323">Binding</span></span>  
 <span data-ttu-id="0c9a0-324">WCF fournit un modèle d’échange de message demande-réponse à l’aide de deux séquences sur un trafic entrant et un canal HTTP sortant.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-324">WCF provides a request-reply message exchange pattern using two sequences over one inbound and one outbound HTTP channel.</span></span> <span data-ttu-id="0c9a0-325">Ce modèle d'échange de messages peut être combiné avec le modèle d'échange de messages initiateur `Duplex, Addressable` d'une manière limitée.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-325">This message exchange pattern can be mixed with the `Duplex, Addressable` Initiator message exchange pattern in a limited way.</span></span> <span data-ttu-id="0c9a0-326">WCF utilise les requêtes HTTP pour transmettre tous les messages.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-326">WCF uses the HTTP requests to transmit all messages.</span></span> <span data-ttu-id="0c9a0-327">Toutes les réponses HTTP ont un corps vide et le code d'état HTTP 202.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-327">All HTTP responses have an empty body and HTTP 202 status code.</span></span>  
  
#### <a name="createsequence-exchange"></a><span data-ttu-id="0c9a0-328">Échange CreateSequence</span><span class="sxs-lookup"><span data-stu-id="0c9a0-328">CreateSequence Exchange</span></span>  
 <span data-ttu-id="0c9a0-329">L’initiateur de WCF transmet un `CreateSequence` message avec un `Offer` élément sur une requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-329">The WCF Initiator transmits a `CreateSequence` message with an `Offer` element on an HTTP request.</span></span> <span data-ttu-id="0c9a0-330">Le répondeur de WCF garantit que le `CreateSequence` a un `Offer` élément, puis crée une séquence et transmet le `CreateSequenceResponse` message avec un `Accept` élément.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-330">The WCF Responder ensures that the `CreateSequence` has an `Offer` element then creates a sequence and transmits the `CreateSequenceResponse` message with an `Accept` element.</span></span>  
  
#### <a name="requestreply-correlation"></a><span data-ttu-id="0c9a0-331">Corrélation demande/réponse</span><span class="sxs-lookup"><span data-stu-id="0c9a0-331">Request/Reply Correlation</span></span>  
 <span data-ttu-id="0c9a0-332">Les points suivants s'appliquent à toutes les demandes et réponses corrélées :</span><span class="sxs-lookup"><span data-stu-id="0c9a0-332">The following applies to all correlated requests and replies:</span></span>  
  
-   <span data-ttu-id="0c9a0-333">WCF garantit que toutes les applications demande messages portent un `ReplyTo` référence de point de terminaison et un `MessageId`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-333">WCF ensures all application request messages bear a `ReplyTo` endpoint reference and a `MessageId`.</span></span>  
  
-   <span data-ttu-id="0c9a0-334">WCF s’applique à la référence de point de terminaison local en tant que chaque message de demande application `ReplyTo`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-334">WCF applies the local endpoint reference as each application request message’s `ReplyTo`.</span></span> <span data-ttu-id="0c9a0-335">La référence de point de terminaison locale est `CreateSequence` du message `ReplyTo` pour l'initiateur et `CreateSequence` du message `To` pour le répondeur.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-335">The local endpoint reference is the `CreateSequence` message’s `ReplyTo` for the Initiator and the `CreateSequence` message’s `To` for the Responder.</span></span>  
  
-   <span data-ttu-id="0c9a0-336">WCF permet de s’assurer que demande entrante messages portent un `MessageId` et un `ReplyTo`.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-336">WCF ensures that incoming request messages bear a `MessageId` and a `ReplyTo`.</span></span>  
  
-   <span data-ttu-id="0c9a0-337">WCF garantit la `ReplyTo` URI de la référence de point de terminaison de tous les messages de demande d’application correspond à la référence de point de terminaison local comme défini précédemment.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-337">WCF ensures the `ReplyTo` endpoint reference’s URI of all application request messages match the local endpoint reference as defined earlier.</span></span>  
  
-   <span data-ttu-id="0c9a0-338">WCF permet de s’assurer que toutes les réponses portent le bon `RelatesTo` et `To` en-têtes `wsa` règles de corrélation de demande/réponse.</span><span class="sxs-lookup"><span data-stu-id="0c9a0-338">WCF ensures that all replies bear the correct `RelatesTo` and `To` headers following `wsa` request/reply correlation rules.</span></span>
