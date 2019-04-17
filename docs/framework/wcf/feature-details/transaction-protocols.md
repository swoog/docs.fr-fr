---
title: Protocoles de transaction
ms.date: 03/30/2017
ms.assetid: 2820b0ec-2f32-430c-b299-1f0e95e1f2dc
ms.openlocfilehash: 3f4824ac6098f33b7bde4f29d3e0950783dfd213
ms.sourcegitcommit: 438919211260bb415fc8f96ca3eabc33cf2d681d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2019
ms.locfileid: "59613575"
---
# <a name="transaction-protocols"></a><span data-ttu-id="c462b-102">Protocoles de transaction</span><span class="sxs-lookup"><span data-stu-id="c462b-102">Transaction Protocols</span></span>
<span data-ttu-id="c462b-103">Windows Communication Foundation (WCF) implémente les protocoles WS-Atomic Transaction et WS-Coordination.</span><span class="sxs-lookup"><span data-stu-id="c462b-103">Windows Communication Foundation (WCF) implements WS-Atomic Transaction and WS-Coordination protocols.</span></span>  
  
|<span data-ttu-id="c462b-104">Spécification/Document</span><span class="sxs-lookup"><span data-stu-id="c462b-104">Specification/Document</span></span>|<span data-ttu-id="c462b-105">Version</span><span class="sxs-lookup"><span data-stu-id="c462b-105">Version</span></span>|<span data-ttu-id="c462b-106">Lien</span><span class="sxs-lookup"><span data-stu-id="c462b-106">Link</span></span>|  
|-----------------------------|-------------|----------|  
|<span data-ttu-id="c462b-107">WS-Coordination</span><span class="sxs-lookup"><span data-stu-id="c462b-107">WS-Coordination</span></span>|<span data-ttu-id="c462b-108">1.0</span><span class="sxs-lookup"><span data-stu-id="c462b-108">1.0</span></span><br /><br /> <span data-ttu-id="c462b-109">1.1</span><span class="sxs-lookup"><span data-stu-id="c462b-109">1.1</span></span>|<https://go.microsoft.com/fwlink/?LinkId=96104><br /><br /> [https://go.microsoft.com/fwlink/?LinkId=96079](https://go.microsoft.com/fwlink/?LinkId=96079)|  
|<span data-ttu-id="c462b-110">WS-AtomicTransaction</span><span class="sxs-lookup"><span data-stu-id="c462b-110">WS-AtomicTransaction</span></span>|<span data-ttu-id="c462b-111">1.0</span><span class="sxs-lookup"><span data-stu-id="c462b-111">1.0</span></span><br /><br /> <span data-ttu-id="c462b-112">1.1</span><span class="sxs-lookup"><span data-stu-id="c462b-112">1.1</span></span>|<https://go.microsoft.com/fwlink/?LinkId=96080><br /><br /> https://go.microsoft.com/fwlink/?LinkId=96081|  
  
 <span data-ttu-id="c462b-113">L’interopérabilité sur ces spécifications de protocole est requise à deux niveaux : entre les applications et entre les gestionnaires de transactions (consultez la figure suivante).</span><span class="sxs-lookup"><span data-stu-id="c462b-113">Interoperability on these protocol specifications is required at two levels: between applications and between transaction managers (see the following figure).</span></span> <span data-ttu-id="c462b-114">Les spécifications décrivent de manière très détaillée les formats de message et l'échange de messages pour les deux niveaux d'interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="c462b-114">Specifications describe in great detail the message formats and message exchange for both interoperability levels.</span></span> <span data-ttu-id="c462b-115">Une certain niveau de sécurité, de fiabilité et des encodages pour l'échange interapplication s'appliquent de la même manière que pour l'échange entre applications normal.</span><span class="sxs-lookup"><span data-stu-id="c462b-115">Certain security, reliability, and encodings for application-to-application exchange apply as they do for regular application exchange.</span></span> <span data-ttu-id="c462b-116">Toutefois, l'interopérabilité réussie entre les gestionnaires de transactions requiert un contrat sur la liaison spécifique, car il n'est généralement pas configuré par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c462b-116">However, successful interoperability between transaction managers requires agreement on the particular binding, because it is usually not configured by the user.</span></span>  
  
 <span data-ttu-id="c462b-117">Cette rubrique décrit une composition de la spécification WS-AT (WS-Atomic Transaction) avec sécurité et décrit la liaison sécurisée utilisée pour la communication entre les gestionnaires de transactions.</span><span class="sxs-lookup"><span data-stu-id="c462b-117">This topic describes a composition of the WS-Atomic Transaction (WS-AT) specification with security and describes the secure binding used for communication between transaction managers.</span></span> <span data-ttu-id="c462b-118">L'approche décrite dans ce document a été testée avec succès avec d'autres implémentations de WS-AT et WS-Coordination, dont IBM, IONA, Sun Microsystems, etc.</span><span class="sxs-lookup"><span data-stu-id="c462b-118">The approach described in this document has been successfully tested with other implementations of WS-AT and WS-Coordination including IBM, IONA, Sun Microsystems, and others.</span></span>  
  
 <span data-ttu-id="c462b-119">La figure suivante illustre l’interopérabilité entre les deux gestionnaires de transactions, Gestionnaire de transactions 1 et 2 du Gestionnaire de Transaction et les deux applications, Application 1 et 2 de l’Application :</span><span class="sxs-lookup"><span data-stu-id="c462b-119">The following figure depicts the interoperability between two transaction managers, Transaction Manager 1 and Transaction Manager 2, and two applications, Application 1 and Application 2:</span></span>  
  
 ![Capture d’écran qui illustre l’interaction entre la transaction gestionnaires.](./media/transaction-protocols/transaction-managers-flow.gif)  
  
 <span data-ttu-id="c462b-121">Examinons un scénario WS-Coordination/WS-Atomic Transaction classique avec un Initiateur (I) et un Participant (P).</span><span class="sxs-lookup"><span data-stu-id="c462b-121">Consider a typical WS-Coordination/WS-Atomic Transaction scenario with one Initiator (I) and one Participant (P).</span></span> <span data-ttu-id="c462b-122">L’Initiateur et le Participant ont des Gestionnaires de transactions (ITM et PTM, respectivement).</span><span class="sxs-lookup"><span data-stu-id="c462b-122">Both Initiator and Participant have Transaction Managers, (ITM and PTM, respectively).</span></span> <span data-ttu-id="c462b-123">La validation en deux phases est désignée sous le terme « 2PC » dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="c462b-123">Two-phase commit is referred to as 2PC in this topic.</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="c462b-124">1. CreateCoordinationContext</span><span class="sxs-lookup"><span data-stu-id="c462b-124">1. CreateCoordinationContext</span></span>|<span data-ttu-id="c462b-125">12. Réponse de message d'application</span><span class="sxs-lookup"><span data-stu-id="c462b-125">12. Application Message Response</span></span>|  
|<span data-ttu-id="c462b-126">2. CreateCoordinationContextResponse</span><span class="sxs-lookup"><span data-stu-id="c462b-126">2. CreateCoordinationContextResponse</span></span>|<span data-ttu-id="c462b-127">13. Commit (achèvement)</span><span class="sxs-lookup"><span data-stu-id="c462b-127">13. Commit (Completion)</span></span>|  
|<span data-ttu-id="c462b-128">3. Register (achèvement)</span><span class="sxs-lookup"><span data-stu-id="c462b-128">3. Register (Completion)</span></span>|<span data-ttu-id="c462b-129">14. Prepare (2PC)</span><span class="sxs-lookup"><span data-stu-id="c462b-129">14. Prepare (2PC)</span></span>|  
|<span data-ttu-id="c462b-130">4. RegisterResponse</span><span class="sxs-lookup"><span data-stu-id="c462b-130">4. RegisterResponse</span></span>|<span data-ttu-id="c462b-131">15. Prepare (2PC)</span><span class="sxs-lookup"><span data-stu-id="c462b-131">15. Prepare (2PC)</span></span>|  
|<span data-ttu-id="c462b-132">5. Message d'application</span><span class="sxs-lookup"><span data-stu-id="c462b-132">5. Application Message</span></span>|<span data-ttu-id="c462b-133">16. Prepared (2PC)</span><span class="sxs-lookup"><span data-stu-id="c462b-133">16. Prepared (2PC)</span></span>|  
|<span data-ttu-id="c462b-134">6. CreateCoordinationContext avec Context</span><span class="sxs-lookup"><span data-stu-id="c462b-134">6. CreateCoordinationContext with Context</span></span>|<span data-ttu-id="c462b-135">17. Prepared (2PC)</span><span class="sxs-lookup"><span data-stu-id="c462b-135">17. Prepared (2PC)</span></span>|  
|<span data-ttu-id="c462b-136">7. Register (durable)</span><span class="sxs-lookup"><span data-stu-id="c462b-136">7. Register (Durable)</span></span>|<span data-ttu-id="c462b-137">18. Committed (achèvement)</span><span class="sxs-lookup"><span data-stu-id="c462b-137">18. Committed (Completion)</span></span>|  
|<span data-ttu-id="c462b-138">8. RegisterResponse</span><span class="sxs-lookup"><span data-stu-id="c462b-138">8. RegisterResponse</span></span>|<span data-ttu-id="c462b-139">19. Commit (2PC)</span><span class="sxs-lookup"><span data-stu-id="c462b-139">19. Commit (2PC)</span></span>|  
|<span data-ttu-id="c462b-140">9. CreateCoordinationContextResponse</span><span class="sxs-lookup"><span data-stu-id="c462b-140">9. CreateCoordinationContextResponse</span></span>|<span data-ttu-id="c462b-141">20. Commit (2PC)</span><span class="sxs-lookup"><span data-stu-id="c462b-141">20. Commit (2PC)</span></span>|  
|<span data-ttu-id="c462b-142">10. Register (durable)</span><span class="sxs-lookup"><span data-stu-id="c462b-142">10. Register (Durable)</span></span>|<span data-ttu-id="c462b-143">21. Committed (2PC)</span><span class="sxs-lookup"><span data-stu-id="c462b-143">21. Committed (2PC)</span></span>|  
|<span data-ttu-id="c462b-144">11. RegisterResponse</span><span class="sxs-lookup"><span data-stu-id="c462b-144">11. RegisterResponse</span></span>|<span data-ttu-id="c462b-145">22. Committed (2PC)</span><span class="sxs-lookup"><span data-stu-id="c462b-145">22. Committed (2PC)</span></span>|  
  
 <span data-ttu-id="c462b-146">Ce document décrit une composition de la spécification WS-AtomicTransaction avec sécurité et décrit la liaison sécurisée utilisée pour la communication entre les gestionnaires de transactions.</span><span class="sxs-lookup"><span data-stu-id="c462b-146">This document describes a composition of the WS-AtomicTransaction specification with security and describes the secure binding used for communication between transaction managers.</span></span> <span data-ttu-id="c462b-147">L'approche décrite dans ce document a été testée avec succès avec d'autres implémentations de WS-AT et WS-Coordination.</span><span class="sxs-lookup"><span data-stu-id="c462b-147">The approach described in this document has been successfully tested with other implementations of WS-AT and WS-Coordination.</span></span>  
  
 <span data-ttu-id="c462b-148">La figure et le tableau présentent quatre classes de messages du point de vue de sécurité :</span><span class="sxs-lookup"><span data-stu-id="c462b-148">The figure and table illustrate four classes of messages from the viewpoint of security:</span></span>  
  
-   <span data-ttu-id="c462b-149">Messages d'activation (CreateCoordinationContext et CreateCoordinationContextResponse).</span><span class="sxs-lookup"><span data-stu-id="c462b-149">Activation messages (CreateCoordinationContext and CreateCoordinationContextResponse).</span></span>  
  
-   <span data-ttu-id="c462b-150">Messages d'inscription (Register et RegisterResponse)</span><span class="sxs-lookup"><span data-stu-id="c462b-150">Registration messages (Register and RegisterResponse)</span></span>  
  
-   <span data-ttu-id="c462b-151">Messages de protocole (Prepare, Rollback, Commit, Aborted, etc).</span><span class="sxs-lookup"><span data-stu-id="c462b-151">Protocol messages (Prepare, Rollback, Commit, Aborted, and so on).</span></span>  
  
-   <span data-ttu-id="c462b-152">Messages d'application</span><span class="sxs-lookup"><span data-stu-id="c462b-152">Application messages.</span></span>  
  
 <span data-ttu-id="c462b-153">Les trois premières classes de message sont considérées comme des messages de gestionnaire de transactions et leur configuration de liaison est décrite dans la section « Échange de messages d’application » développée ultérieurement dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="c462b-153">The first three message classes are considered Transaction Manager messages and their binding configuration is described in the "Application Message Exchange" later in this topic.</span></span> <span data-ttu-id="c462b-154">La quatrième classe de message concerne les messages interapplication et est décrite dans la section « Exemples de message » développée ultérieurement dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="c462b-154">The fourth class of message is application to application messages and is described in the "Message Examples" section later in this topic.</span></span> <span data-ttu-id="c462b-155">Cette section décrit les liaisons de protocole utilisées pour chacune de ces classes par WCF.</span><span class="sxs-lookup"><span data-stu-id="c462b-155">This section describes the protocol bindings used for each of these classes by WCF.</span></span>  
  
 <span data-ttu-id="c462b-156">Les espaces de noms XML suivants et préfixes associés sont utilisés dans l'ensemble de ce document.</span><span class="sxs-lookup"><span data-stu-id="c462b-156">The following XML Namespaces and associated prefixes are used throughout this document.</span></span>  
  
|<span data-ttu-id="c462b-157">Préfixe</span><span class="sxs-lookup"><span data-stu-id="c462b-157">Prefix</span></span>|<span data-ttu-id="c462b-158">Version</span><span class="sxs-lookup"><span data-stu-id="c462b-158">Version</span></span>|<span data-ttu-id="c462b-159">URI d'espace de noms</span><span class="sxs-lookup"><span data-stu-id="c462b-159">Namespace URI</span></span>|  
|------------|-------------|-------------------|  
|<span data-ttu-id="c462b-160">s11</span><span class="sxs-lookup"><span data-stu-id="c462b-160">s11</span></span>||<https://go.microsoft.com/fwlink/?LinkId=96014>|  
|<span data-ttu-id="c462b-161">wsa</span><span class="sxs-lookup"><span data-stu-id="c462b-161">wsa</span></span>|<span data-ttu-id="c462b-162">Pre-1.0</span><span class="sxs-lookup"><span data-stu-id="c462b-162">Pre-1.0</span></span><br /><br /> <span data-ttu-id="c462b-163">1.0</span><span class="sxs-lookup"><span data-stu-id="c462b-163">1.0</span></span>|http://www.w3.org/2004/08/addressing<br /><br /> <https://go.microsoft.com/fwlink/?LinkId=96022>|  
|<span data-ttu-id="c462b-164">wscoor</span><span class="sxs-lookup"><span data-stu-id="c462b-164">wscoor</span></span>|<span data-ttu-id="c462b-165">1.0</span><span class="sxs-lookup"><span data-stu-id="c462b-165">1.0</span></span><br /><br /> <span data-ttu-id="c462b-166">1.1</span><span class="sxs-lookup"><span data-stu-id="c462b-166">1.1</span></span>|<https://go.microsoft.com/fwlink/?LinkId=96078><br /><br /> [https://go.microsoft.com/fwlink/?LinkId=96079](https://go.microsoft.com/fwlink/?LinkId=96079)|  
|<span data-ttu-id="c462b-167">wsat</span><span class="sxs-lookup"><span data-stu-id="c462b-167">wsat</span></span>|<span data-ttu-id="c462b-168">1.0</span><span class="sxs-lookup"><span data-stu-id="c462b-168">1.0</span></span><br /><br /> <span data-ttu-id="c462b-169">1.1</span><span class="sxs-lookup"><span data-stu-id="c462b-169">1.1</span></span>|<https://go.microsoft.com/fwlink/?LinkId=96080><br /><br /> [https://go.microsoft.com/fwlink/?LinkId=96081](https://go.microsoft.com/fwlink/?LinkId=96081)|  
|<span data-ttu-id="c462b-170">t</span><span class="sxs-lookup"><span data-stu-id="c462b-170">t</span></span>|<span data-ttu-id="c462b-171">Pre-1.3</span><span class="sxs-lookup"><span data-stu-id="c462b-171">Pre-1.3</span></span><br /><br /> <span data-ttu-id="c462b-172">1.3</span><span class="sxs-lookup"><span data-stu-id="c462b-172">1.3</span></span>|<https://go.microsoft.com/fwlink/?LinkId=96082><br /><br /> [https://go.microsoft.com/fwlink/?LinkId=96100](https://go.microsoft.com/fwlink/?LinkId=96100)|  
|<span data-ttu-id="c462b-173">o</span><span class="sxs-lookup"><span data-stu-id="c462b-173">o</span></span>||<https://go.microsoft.com/fwlink/?LinkId=96101>|  
|<span data-ttu-id="c462b-174">xsd</span><span class="sxs-lookup"><span data-stu-id="c462b-174">xsd</span></span>||<https://go.microsoft.com/fwlink/?LinkId=96102>|  
  
## <a name="transaction-manager-bindings"></a><span data-ttu-id="c462b-175">Liaisons de gestionnaire de transactions</span><span class="sxs-lookup"><span data-stu-id="c462b-175">Transaction Manager Bindings</span></span>  
 <span data-ttu-id="c462b-176">R1001 : Les gestionnaires de transactions participant à une transaction WS-AT 1.0 doivent utiliser SOAP 1.1 et WS-Addressing 2004/08 pour WS-Atomic Transaction et les échanges de messages WS-Coordination.</span><span class="sxs-lookup"><span data-stu-id="c462b-176">R1001: Transaction Managers participating in a WS-AT 1.0 transaction must use SOAP 1.1 and WS-Addressing 2004/08 for WS-Atomic Transaction and WS-Coordination message exchanges.</span></span>  
  
 <span data-ttu-id="c462b-177">R1002 : Les gestionnaires de transactions participant à une transaction WS-AT 1.1 doivent utiliser SOAP 1.1 et WS-Addressing 2005/08 pour WS-Atomic Transaction et les échanges de messages WS-Coordination.</span><span class="sxs-lookup"><span data-stu-id="c462b-177">R1002: Transaction Managers participating in a WS-AT 1.1 transaction must use SOAP 1.1 and WS-Addressing 2005/08 for WS-Atomic Transaction and WS-Coordination message exchanges.</span></span>  
  
 <span data-ttu-id="c462b-178">Les messages d’application ne sont pas contraints à ces liaisons et sont décrits ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="c462b-178">Application messages are not constrained to these bindings and are described later.</span></span>  
  
### <a name="transaction-manager-https-binding"></a><span data-ttu-id="c462b-179">Liaison HTTPS de gestionnaire de transactions</span><span class="sxs-lookup"><span data-stu-id="c462b-179">Transaction Manager HTTPS Binding</span></span>  
 <span data-ttu-id="c462b-180">La liaison HTTPS de gestionnaire de transactions s'appuie uniquement sur le transport de sécurité pour assurer la sécurité et établir la confiance entre chaque paire expéditeur-récepteur dans l'arborescence de transactions.</span><span class="sxs-lookup"><span data-stu-id="c462b-180">The transaction manager HTTPS binding relies solely on transport security to achieve security and establish trust between each sender-receiver pair in the transaction tree.</span></span>  
  
#### <a name="https-transport-configuration"></a><span data-ttu-id="c462b-181">Configuration du transport HTTPS</span><span class="sxs-lookup"><span data-stu-id="c462b-181">HTTPS Transport Configuration</span></span>  
 <span data-ttu-id="c462b-182">Les certificats X.509 permettent d'établir l'identité de gestionnaire de transactions.</span><span class="sxs-lookup"><span data-stu-id="c462b-182">X.509 certificates are used to establish Transaction Manager Identity.</span></span> <span data-ttu-id="c462b-183">L'authentification client/serveur est requise, et l'autorisation client/serveur est considérée comme un détail d'implémentation :</span><span class="sxs-lookup"><span data-stu-id="c462b-183">Client/server authentication is required, and client/server authorization is left as an implementation detail:</span></span>  
  
-   <span data-ttu-id="c462b-184">R1111 : Certificats X.509 présentés sur le câble doivent avoir un nom de sujet qui correspond au nom de domaine complet (FQDN) de l’ordinateur d’origine.</span><span class="sxs-lookup"><span data-stu-id="c462b-184">R1111: X.509 certificates presented over the wire must have a subject name that matches the fully qualified domain name (FQDN) of the originating machine.</span></span>  
  
-   <span data-ttu-id="c462b-185">B1112 : DNS doit être fonctionnel entre chaque paire expéditeur-récepteur dans le système pour les vérifications du nom de sujet X.509 réussisse.</span><span class="sxs-lookup"><span data-stu-id="c462b-185">B1112: DNS must be functional between each sender-receiver pair in the system for X.509 subject name checks to succeed.</span></span>  
  
#### <a name="activation-and-registration-binding-configuration"></a><span data-ttu-id="c462b-186">Configuration de liaison d'activation et d'inscription</span><span class="sxs-lookup"><span data-stu-id="c462b-186">Activation and Registration Binding Configuration</span></span>  
 <span data-ttu-id="c462b-187">WCF nécessite une liaison duplex de demande/réponse avec corrélation sur HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c462b-187">WCF requires request/reply duplex binding with correlation over HTTPS.</span></span> <span data-ttu-id="c462b-188">(Pour plus d'informations sur la corrélation et les descriptions des modèles d'échange de messages demande/réponse, consultez WS-Atomic Transaction, section 8.)</span><span class="sxs-lookup"><span data-stu-id="c462b-188">(For more information about correlation and descriptions of the request/reply message exchange patterns, see WS-Atomic Transaction, Section 8.)</span></span>  
  
#### <a name="2pc-protocol-binding-configuration"></a><span data-ttu-id="c462b-189">Configuration de liaison de protocole 2PC</span><span class="sxs-lookup"><span data-stu-id="c462b-189">2PC Protocol Binding Configuration</span></span>  
 <span data-ttu-id="c462b-190">WCF prend en charge les messages monodirectionnels (datagramme) via le protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c462b-190">WCF supports one-way (datagram) messages over HTTPS.</span></span> <span data-ttu-id="c462b-191">La corrélation au sein des messages est considérée comme un détail d'implémentation.</span><span class="sxs-lookup"><span data-stu-id="c462b-191">Correlation among the messages is left as an implementation detail.</span></span>  
  
 <span data-ttu-id="c462b-192">B1131 : Les implémentations doivent prendre en charge `wsa:ReferenceParameters` comme décrit dans WS-Addressing pour assurer la corrélation des messages de protocole 2PC de WCF.</span><span class="sxs-lookup"><span data-stu-id="c462b-192">B1131: Implementations must support `wsa:ReferenceParameters` as described in WS-Addressing to achieve correlation of WCF’s 2PC messages.</span></span>  
  
### <a name="transaction-manager-mixed-security-binding"></a><span data-ttu-id="c462b-193">Liaison de sécurité mixte de gestionnaire de transactions</span><span class="sxs-lookup"><span data-stu-id="c462b-193">Transaction Manager Mixed Security Binding</span></span>  
 <span data-ttu-id="c462b-194">Cette autre liaison (mode mixte) utilise le transport de sécurité combiné avec le modèle WS-Coordination Issued Token à des fins d’établissement d’identité.</span><span class="sxs-lookup"><span data-stu-id="c462b-194">This is an alternate (mixed mode) binding that uses transport security combined with the WS-Coordination Issued Token model for identity establishment purposes.</span></span> <span data-ttu-id="c462b-195">L’activation et l’inscription sont les seuls éléments qui diffèrent entre les deux liaisons.</span><span class="sxs-lookup"><span data-stu-id="c462b-195">Activation and Registration are the only elements that differ between the two bindings.</span></span>  
  
#### <a name="https-transport-configuration"></a><span data-ttu-id="c462b-196">Configuration du transport HTTPS</span><span class="sxs-lookup"><span data-stu-id="c462b-196">HTTPS Transport Configuration</span></span>  
 <span data-ttu-id="c462b-197">Les certificats X.509 permettent d'établir l'identité de gestionnaire de transactions.</span><span class="sxs-lookup"><span data-stu-id="c462b-197">X.509 certificates are used to establish Transaction Manager Identity.</span></span> <span data-ttu-id="c462b-198">L'authentification client/serveur est requise, et l'autorisation client/serveur est considérée comme un détail d'implémentation.</span><span class="sxs-lookup"><span data-stu-id="c462b-198">Client/Server authentication is required, and client/server authorization is left as an implementation detail.</span></span>  
  
#### <a name="activation-message-binding-configuration"></a><span data-ttu-id="c462b-199">Configuration de liaison de message d’activation</span><span class="sxs-lookup"><span data-stu-id="c462b-199">Activation Message Binding Configuration</span></span>  
 <span data-ttu-id="c462b-200">En général, les messages d’activation ne participent pas à l’interopérabilité car ils se produisent habituellement entre une application et son gestionnaire de transactions local.</span><span class="sxs-lookup"><span data-stu-id="c462b-200">Activation Messages usually do not participate in interoperability because they typically occur between an application and its local Transaction Manager.</span></span>  
  
 <span data-ttu-id="c462b-201">B1221 : WCF utilise la liaison HTTPS duplex (décrite dans [protocoles de messagerie](../../../../docs/framework/wcf/feature-details/messaging-protocols.md)) pour les messages d’Activation.</span><span class="sxs-lookup"><span data-stu-id="c462b-201">B1221: WCF uses duplex HTTPS binding (described in [Messaging Protocols](../../../../docs/framework/wcf/feature-details/messaging-protocols.md)) for Activation messages.</span></span> <span data-ttu-id="c462b-202">Les messages de demande et de réponse sont corrélés à l'aide de WS-Addressing 2004/08 pour WS-AT 1.0 et WS-Addressing 2005/08 pour WS-AT 1.1.</span><span class="sxs-lookup"><span data-stu-id="c462b-202">Request and Reply messages are correlated using WS-Addressing 2004/08 for WS-AT 1.0 and WS-Addressing 2005/08 for WS-AT 1.1.</span></span>  
  
 <span data-ttu-id="c462b-203">La spécification WS-Atomic Transaction, section 8, fournit des informations supplémentaires sur la corrélation et les modèles d'échange de messages.</span><span class="sxs-lookup"><span data-stu-id="c462b-203">WS-Atomic Transaction specification, Section 8, describes further details about correlation and the message exchange patterns.</span></span>  
  
-   <span data-ttu-id="c462b-204">R1222 : À la réception une `CreateCoordinationContext`, le coordinateur doit émettre un `SecurityContextToken` avec secret associé `STx`.</span><span class="sxs-lookup"><span data-stu-id="c462b-204">R1222: Upon receiving a `CreateCoordinationContext`, the Coordinator must issue a `SecurityContextToken` with associated secret `STx`.</span></span> <span data-ttu-id="c462b-205">Ce jeton est retourné à l'intérieur d'un en-tête `t:IssuedTokens` selon la spécification WS-Trust.</span><span class="sxs-lookup"><span data-stu-id="c462b-205">This token is returned inside a `t:IssuedTokens` header following WS-Trust specification.</span></span>  
  
-   <span data-ttu-id="c462b-206">R1223 : Si l’Activation se produit dans un contexte de Coordination existant, le `t:IssuedTokens` en-tête avec le `SecurityContextToken` associé existant contexte doit transmettre sur le `CreateCoordinationContext` message.</span><span class="sxs-lookup"><span data-stu-id="c462b-206">R1223: If Activation occurs within an existing Coordination Context, the `t:IssuedTokens` header with the `SecurityContextToken` associated with existing Context must flow on the `CreateCoordinationContext` message.</span></span>  
  
 <span data-ttu-id="c462b-207">Un nouveau `t:IssuedTokens` en-tête doit être généré pour attacher à sortant `wscoor:CreateCoordinationContextResponse` message.</span><span class="sxs-lookup"><span data-stu-id="c462b-207">A new `t:IssuedTokens` header should be generated for attaching to the outgoing `wscoor:CreateCoordinationContextResponse` message.</span></span>  
  
#### <a name="registration-message-binding-configuration"></a><span data-ttu-id="c462b-208">Configuration de liaison de message d'inscription</span><span class="sxs-lookup"><span data-stu-id="c462b-208">Registration Message Binding Configuration</span></span>  
 <span data-ttu-id="c462b-209">B1231 : WCF utilise la liaison HTTPS duplex (décrite dans [protocoles de messagerie](../../../../docs/framework/wcf/feature-details/messaging-protocols.md)).</span><span class="sxs-lookup"><span data-stu-id="c462b-209">B1231: WCF uses duplex HTTPS binding (described in [Messaging Protocols](../../../../docs/framework/wcf/feature-details/messaging-protocols.md)).</span></span> <span data-ttu-id="c462b-210">Les messages de demande et de réponse sont corrélés à l'aide de WS-Addressing 2004/08 pour WS-AT 1.0 et WS-Addressing 2005/08 pour WS-AT 1.1.</span><span class="sxs-lookup"><span data-stu-id="c462b-210">Request and Reply messages are correlated using WS-Addressing 2004/08 for WS-AT 1.0 and WS-Addressing 2005/08 for WS-AT 1.1.</span></span>  
  
 <span data-ttu-id="c462b-211">WS-AtomicTransaction, section 8, fournit des informations supplémentaires sur la corrélation et des descriptions des modèles d’échange de messages.</span><span class="sxs-lookup"><span data-stu-id="c462b-211">WS-AtomicTransaction, Section 8, describes further details about correlation and descriptions of the message exchange patterns.</span></span>  
  
 <span data-ttu-id="c462b-212">R1232 : Sortant `wscoor:Register` messages doivent utiliser le `IssuedTokenOverTransport` mode d’authentification décrit dans [protocoles de sécurité](../../../../docs/framework/wcf/feature-details/security-protocols.md).</span><span class="sxs-lookup"><span data-stu-id="c462b-212">R1232: Outgoing `wscoor:Register` messages must use the `IssuedTokenOverTransport` authentication mode described in [Security Protocols](../../../../docs/framework/wcf/feature-details/security-protocols.md).</span></span>  
  
 <span data-ttu-id="c462b-213">Le `wsse:Timestamp` élément doit être signé à l’aide de la `SecurityContextToken STx` émis.</span><span class="sxs-lookup"><span data-stu-id="c462b-213">The `wsse:Timestamp` element must be signed using the `SecurityContextToken STx` issued.</span></span> <span data-ttu-id="c462b-214">Cette signature est une preuve de possession du jeton associée à une transaction spécifique et est utilisée pour authentifier un participant qui s’inscrit à la transaction.</span><span class="sxs-lookup"><span data-stu-id="c462b-214">This signature is a proof of possession of the token associated with particular transaction and is used to authenticate a participant enlisting in the transaction.</span></span> <span data-ttu-id="c462b-215">Le message RegistrationResponse est renvoyé sur HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c462b-215">The RegistrationResponse message is sent back over HTTPS.</span></span>  
  
#### <a name="2pc-protocol-binding-configuration"></a><span data-ttu-id="c462b-216">Configuration de liaison de protocole 2PC</span><span class="sxs-lookup"><span data-stu-id="c462b-216">2PC Protocol Binding Configuration</span></span>  
 <span data-ttu-id="c462b-217">WCF prend en charge les messages monodirectionnels (datagramme) via le protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c462b-217">WCF supports one-way (datagram) messages over HTTPS.</span></span> <span data-ttu-id="c462b-218">La corrélation au sein des messages est considérée comme un détail d'implémentation.</span><span class="sxs-lookup"><span data-stu-id="c462b-218">Correlation among the messages is left as an implementation detail.</span></span>  
  
 <span data-ttu-id="c462b-219">B1241 : Les implémentations doivent prendre en charge `wsa:ReferenceParameters` comme décrit dans WS-Addressing pour assurer la corrélation des messages de protocole 2PC de WCF.</span><span class="sxs-lookup"><span data-stu-id="c462b-219">B1241: Implementations must support `wsa:ReferenceParameters` as described in WS-Addressing to achieve correlation of WCF’s 2PC messages.</span></span>  
  
## <a name="application-message-exchange"></a><span data-ttu-id="c462b-220">Échange de messages d'application</span><span class="sxs-lookup"><span data-stu-id="c462b-220">Application Message Exchange</span></span>  
 <span data-ttu-id="c462b-221">Les applications sont libres d’utiliser n’importe quelle liaison spécifique pour les messages interapplication, tant que la liaison satisfait aux exigences de sécurité suivantes :</span><span class="sxs-lookup"><span data-stu-id="c462b-221">Applications are free to use any particular binding for application-to-application messages, as long as the binding meets the following security requirements:</span></span>  
  
-   <span data-ttu-id="c462b-222">R2001 : Messages de l’application vers l’application doivent passer la `t:IssuedTokens` en-tête avec le `CoordinationContext` dans l’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="c462b-222">R2001: Application-to-application messages must flow the `t:IssuedTokens` header along with the `CoordinationContext` in the header of the message.</span></span>  
  
-   <span data-ttu-id="c462b-223">R2002 : L’intégrité et la confidentialité de `t:IssuedToken` doit être fourni.</span><span class="sxs-lookup"><span data-stu-id="c462b-223">R2002: Integrity and confidentiality of `t:IssuedToken` must be provided.</span></span>  
  
 <span data-ttu-id="c462b-224">L'en-tête `CoordinationContext` contient `wscoor:Identifier`.</span><span class="sxs-lookup"><span data-stu-id="c462b-224">The `CoordinationContext` header contains `wscoor:Identifier`.</span></span> <span data-ttu-id="c462b-225">Alors que la définition de `xsd:AnyURI` autorise l’utilisation d’URI absolus et relatifs, WCF prend uniquement en charge `wscoor:Identifiers`, qui sont des URI absolus.</span><span class="sxs-lookup"><span data-stu-id="c462b-225">While the definition of `xsd:AnyURI` allows the use of both absolute and relative URIs, WCF supports only `wscoor:Identifiers`, which are absolute URIs.</span></span>  
  
 <span data-ttu-id="c462b-226">B2003 : Si le `wscoor:Identifier` de la `wscoor:CoordinationContext` est un URI relatif, erreurs seront retournées à partir des services WCF transactionnels.</span><span class="sxs-lookup"><span data-stu-id="c462b-226">B2003: If the `wscoor:Identifier` of the `wscoor:CoordinationContext` is a relative URI, faults will be returned from transactional WCF services.</span></span>  
  
## <a name="message-examples"></a><span data-ttu-id="c462b-227">Exemples de message</span><span class="sxs-lookup"><span data-stu-id="c462b-227">Message Examples</span></span>  
  
### <a name="createcoordinationcontext-requestresponse-messages"></a><span data-ttu-id="c462b-228">Messages de demande/réponse CreateCoordinationContext</span><span class="sxs-lookup"><span data-stu-id="c462b-228">CreateCoordinationContext Request/Response Messages</span></span>  
 <span data-ttu-id="c462b-229">Les messages suivants suivent un modèle de demande/réponse.</span><span class="sxs-lookup"><span data-stu-id="c462b-229">The following messages follow a request/response pattern.</span></span>  
  
#### <a name="createcoordinationcontext-with-wscoor-10"></a><span data-ttu-id="c462b-230">CreateCoordinationContext avec WSCoor 1.0</span><span class="sxs-lookup"><span data-stu-id="c462b-230">CreateCoordinationContext with WSCoor 1.0</span></span>  
  
```xml  
<s:Envelope>  
  <s:Header>  
    <a:Action>http://.../ws/2004/10/wscoor/CreateCoordinationContext</Action>  
    <a:MessageID>urn:uuid:069f5104-fd88-4264-9f99-60032a82854e</MessageID>  
    <a:ReplyTo>  
      <Address>https://...</a:Address>  
    </a:ReplyTo>  
    <a:To>https://...</a:To>  
    <wsse:Security>  
      <u:Timestamp>  
        <wsu:Created>2005-12-15T23:36:09.921Z</u:Created>  
        <wsu:Expires>2005-12-15T23:41:09.921Z</u:Expires>  
      </u:Timestamp>  
    </wsse:Security>  
  </s:Header>  
  <s:Body xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">  
    <wscoor:CreateCoordinationContext>  
      <wscoor:CoordinationType>...</wscoor:CoordinationType>  
    </wscoor:CreateCoordinationContext>  
  </s:Body>  
</s11:Envelope>  
```  
  
#### <a name="createcoordinationcontext-with-wscoor-11"></a><span data-ttu-id="c462b-231">CreateCoordinationContext avec WSCoor 1.1</span><span class="sxs-lookup"><span data-stu-id="c462b-231">CreateCoordinationContext with WSCoor 1.1</span></span>  
  
```xml  
<s:Envelope>   
<s:Header>  
<a:Action>http://docs.oasis-open.org/ws-tx/wscoor/2006/06/CreateCoordinationContext</Action>  
<a:MessageID>urn:uuid:069f5104-fd88-4264-9f99-60032a82854e</MessageID>  
<a:ReplyTo>   
<Address>https://...</a:Address>   
</a:ReplyTo>   
<a:To>https://...</a:To>   
<wsse:Security>  
 <u:Timestamp>  
<wsu:Created>2005-12-15T23:36:09.921Z</u:Created>  
<wsu:Expires>2005-12-15T23:41:09.921Z</u:Expires>  
</u:Timestamp>   
</wsse:Security>   
</s:Header>   
<s:Body xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">  
<wscoor:CreateCoordinationContext>  
<wscoor:CoordinationType>...</wscoor:CoordinationType>  
</wscoor:CreateCoordinationContext>  
 </s:Body>  
</s11:Envelope>  
```  
  
#### <a name="createcoordinationcontextresponse-with-trust-pre-13-and-wscoor-10"></a><span data-ttu-id="c462b-232">CreateCoordinationContextResponse avec Trust Pre-1.3 et WSCoor 1.0</span><span class="sxs-lookup"><span data-stu-id="c462b-232">CreateCoordinationContextResponse with Trust Pre-1.3 and WSCoor 1.0</span></span>  
  
```xml  
<s:Envelope>  
  <!-- Data below is shown in the clear for  
       illustration purposes only. -->  
  <s:Header>  
    <a:Action>./ws/2004/10/wscoor/CreateCoordinationContextResponse </a:Action>  
    <a:RelatesTo>urn:uuid:069f5104-fd88-4264-9f99-60032a82854e</a:RelatesTo>  
    <a:To s:mustUnderstand="1">https://... </a:To>  
    <t:IssuedTokens>  
 <wst:RequestSecurityTokenResponse     
    xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd"  
    xmlns:wssu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd"   
    xmlns:wst="http://schemas.xmlsoap.org/ws/2005/02/trust"  
    xmlns:wsc="http://schemas.xmlsoap.org/ws/2005/02/sc"  
    xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy">  
    <wst:TokenType>http://schemas.xmlsoap.org/ws/2005/02/sc/sct</wst:TokenType>  
    <wst:RequestedSecurityToken>  
      <wsc:SecurityContextToken>  
        <wssu:Identifier>  
          http://fabrikam123.com/SCTi  
        </wssu:Identifier>  
      </wsc:SecurityContextToken>   
    </wst:RequestedSecurityToken>  
    <wsp:AppliesTo>  
        http://fabrikam123.com/CCi  
    </wsp:AppliesTo>    
    <wst:RequestedAttachedReference>  
      <wsse:SecurityTokenReference >  
        <wsse:Reference   
           ValueType="http://schemas.xmlsoap.org/ws/2005/02/sc/sct"  
           URI="http://fabrikam123.com/SCTi"/>  
      </wsse:SecurityTokenReference>  
    </wst:RequestedAttachedReference>  
    <wst:RequestedUnattachedReference>  
      <wsse:SecurityTokenReference>  
        <wsse:Reference   
          ValueType="http://schemas.xmlsoap.org/ws/2005/02/sc/sct"  
          URI="http://fabrikam123.com/SCTi"/>  
      </wsse:SecurityTokenReference>  
    </wst:RequestedUnattachedReference>  
    <wst:RequestedProofToken>  
      <wst:BinarySecret   
        Type="http://schemas.xmlsoap.org/ws/2005/02/trust/SymmetricKey">  
        <!-- base64 encoded value -->  
      </wst:BinarySecret>  
    </wst:RequestedProofToken>  
    <wst:Lifetime>  
      <wssu:Created>2005-10-24T20:19:26.526Z</wssu:Created>  
      <wssu:Expires>2005-10-25T06:24:26.526Z</wssu:Expires>  
    </wst:Lifetime>  
    <wst:KeySize>256</wst:KeySize>  
</wst:RequestSecurityTokenResponse>  
    </t:IssuedTokens>  
    <o:Security xmlns:o="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd">  
      <u:Timestamp u:Id="_0">  
        <u:Created>2005-12-15T23:36:12.015Z</u:Created>  
        <u:Expires>2005-12-15T23:41:12.015Z</u:Expires>  
      </u:Timestamp>  
    </o:Security>  
  </s:Header>  
  <s:Body>  
    <wscoor:CreateCoordinationContextResponse>  
      <wscoor:CoordinationContext>  
        <wscoor:Identifier>  
     http://fabrikam123.com/CCi  
      </wscoor:Identifier>  
        <wscoor:Expires>...</wscoor:Expires>  
        <wscoor:CoordinationType>...</wscoor:CoordinationType>  
        <wscoor:RegistrationService>  
          <a:Address>https://...</a:Address>  
          <a:ReferenceParameters>  
             ...  
          </a:ReferenceParameters>  
        </wscoor:RegistrationService>  
      </wscoor:CoordinationContext>  
    </wscoor:CreateCoordinationContextResponse>  
  </s:Body>  
</s:Envelope>  
```  
  
#### <a name="createcoordinationcontextresponse-with-trust-13-and-wscoor-11"></a><span data-ttu-id="c462b-233">CreateCoordinationContextResponse avec Trust 1.3 et WSCoor 1.1</span><span class="sxs-lookup"><span data-stu-id="c462b-233">CreateCoordinationContextResponse with Trust 1.3 and WSCoor 1.1</span></span>  
  
```xml  
<s:Envelope>  
<!-- Data below is shown in the clear for illustration purposes only. -->   
<s:Header>   
<a:Action>http://docs.oasis-open.org/ws-tx/wscoor/2006/06/CreateCoordinationContextResponse </a:Action>  
<a:RelatesTo>urn:uuid:069f5104-fd88-4264-9f99-60032a82854e</a:RelatesTo>  
<a:To s:mustUnderstand="1">https://... </a:To>   
<t:IssuedTokens>   
<wst:RequestSecurityTokenResponse   
xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd"   
xmlns:wssu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd"   
xmlns:wst="http://docs.oasis-open.org/ws-sx/ws-trust/200512"  
xmlns:wsc="http://schemas.xmlsoap.org/ws/2005/02/sc"  
xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy">  
<wst:TokenType>http://schemas.xmlsoap.org/ws/2005/02/sc/sct</wst:TokenType>  
<wst:RequestedSecurityToken>   
<wsc:SecurityContextToken>   
<wssu:Identifier> http://fabrikam123.com/SCTi  
</wssu:Identifier>   
</wsc:SecurityContextToken>   
</wst:RequestedSecurityToken>   
<wsp:AppliesTo> http://fabrikam123.com/CCi </wsp:AppliesTo>  
<wst:RequestedAttachedReference>   
<wsse:SecurityTokenReference >   
<wsse:Reference  
  ValueType="http://schemas.xmlsoap.org/ws/2005/02/sc/sct"  
  URI="http://fabrikam123.com/SCTi"/>  
</wsse:SecurityTokenReference>   
</wst:RequestedAttachedReference>   
<wst:RequestedUnattachedReference>   
<wsse:SecurityTokenReference>   
<wsse:Reference  
 ValueType="http://schemas.xmlsoap.org/ws/2005/02/sc/sct"  
 URI="http://fabrikam123.com/SCTi"/>  
</wsse:SecurityTokenReference>   
</wst:RequestedUnattachedReference>   
<wst:RequestedProofToken>   
<wst:BinarySecret  
  Type="http://docs.oasis-open.org/ws-sx/ws-trust/200512/SymmetricKey">  
  <!-- base64 encoded value -->   
</wst:BinarySecret>   
</wst:RequestedProofToken>   
<wst:Lifetime>   
<wssu:Created>2005-10-24T20:19:26.526Z</wssu:Created>  
<wssu:Expires>2005-10-25T06:24:26.526Z</wssu:Expires>  
</wst:Lifetime>   
<wst:KeySize>256</wst:KeySize>   
</wst:RequestSecurityTokenResponse>   
</t:IssuedTokens>   
<o:Security xmlns:o="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd">   
<u:Timestamp u:Id="_0">   
<u:Created>2005-12-15T23:36:12.015Z</u:Created>   
<u:Expires>2005-12-15T23:41:12.015Z</u:Expires>   
</u:Timestamp>   
</o:Security>   
</s:Header>   
<s:Body>   
<wscoor:CreateCoordinationContextResponse>   
<wscoor:CoordinationContext>   
<wscoor:Identifier> http://fabrikam123.com/CCi  
</wscoor:Identifier>   
<wscoor:Expires>...</wscoor:Expires>  
<wscoor:CoordinationType>...</wscoor:CoordinationType>  
<wscoor:RegistrationService>   
<a:Address>https://...</a:Address>  
<a:ReferenceParameters> ...  
</a:ReferenceParameters>  
</wscoor:RegistrationService>   
</wscoor:CoordinationContext>   
</wscoor:CreateCoordinationContextResponse>   
</s:Body>   
</s:Envelope>  
```  
  
### <a name="registration-messages"></a><span data-ttu-id="c462b-234">Messages d'inscription</span><span class="sxs-lookup"><span data-stu-id="c462b-234">Registration Messages</span></span>  
 <span data-ttu-id="c462b-235">Les messages suivants sont des messages d'inscription.</span><span class="sxs-lookup"><span data-stu-id="c462b-235">The following messages are registration messages.</span></span>  
  
#### <a name="register-with-wscoor-10"></a><span data-ttu-id="c462b-236">Register avec WSCoor 1.0</span><span class="sxs-lookup"><span data-stu-id="c462b-236">Register with WSCoor 1.0</span></span>  
  
```xml  
<s:Envelope>  
  <s:Header>  
    <a:Action>http://schemas.xmlsoap.org/ws/2004/10/wscoor/Register</a:Action>  
    <a:MessageID>urn:uuid:ed418b86-a75e-4aea-9d4e-a5d0cb5c088e</a:MessageID>  
    <a:ReplyTo>  
      <a:Address>https://...</a:Address>        
    </a:ReplyTo>  
    <a:To>https://...</a:To>  
    <wsse:Security   
      s:mustUnderstand="1"   
      xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd"  
      xmlns:wssu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd">  
      <wssu:Timestamp wssu:Id="_0" >  
        <wssu:Created>2005-12-15T23:36:13.827Z</wssu:Created>  
        <wssu:Expires>2005-12-15T23:41:13.827Z</wssu:Expires>  
      </wssu:Timestamp>  
      <wsc:SecurityContextToken>  
      <wssu:Identifier>  
          http://fabrikam123.com/SCTi  
      </wssu:Identifier>  
      </wsc:SecurityContextToken>  
      <!-- supporting signature over the timestamp -->  
      <wsse:Signature xmlns:ds="http://www.w3.org/2000/09/xmldsig#">  
        <ds:SignedInfo>  
          <ds:CanonicalizationMethod Algorithm="http://www.w3.org/2001/10/xml-exc-c14n#"/>  
          <ds:SignatureMethod Algorithm="http://www.w3.org/2000/09/xmldsig#hmac-sha1"/>  
          <ds:Reference URI="#_0">  
            <ds:Transforms>  
              <ds:Transform Algorithm="http://www.w3.org/2001/10/xml-exc-c14n#"/>  
            </ds:Transforms>  
            <ds:DigestMethod Algorithm="http://www.w3.org/2000/09/xmldsig#sha1"/>  
            <ds:DigestValue>  
              alRzyhjLgoUOYoh8cx4n75eTcUk=  
            </ds:DigestValue>  
          </ds:Reference>  
        </ds:SignedInfo>  
        <ds:SignatureValue>YZYjnVvSOVasAQqQxaaviTSWtqI=</ds:SignatureValue>  
        <ds:KeyInfo>  
          <wsse:SecurityTokenReference  
            xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd">  
            <wsse:Reference   
              URI="http://fabrikam123.com/SCTi"/>  
          </wsse:SecurityTokenReference>  
        </ds:KeyInfo>  
      </wsse:Signature>  
    </wsse:Security>  
  </s:Header>  
  <s:Body xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">  
    <wscoor:Register>  
      <wscoor:ProtocolIdentifier>...</wscoor:ProtocolIdentifier>  
      <wscoor:ParticipantProtocolService>  
        <a:Address>https://... </a:Address>  
      </wscoor:ParticipantProtocolService>  
    </wscoor:Register>  
  </s:Body>  
</s:Envelope>  
```  
  
#### <a name="register-with-wscoor-11"></a><span data-ttu-id="c462b-237">Register avec WSCoor 1.1</span><span class="sxs-lookup"><span data-stu-id="c462b-237">Register with WSCoor 1.1</span></span>  
  
```xml  
<s:Envelope>  
<s:Header>   
<a:Action>http://docs.oasis-open.org/ws-tx/wscoor/2006/06/Register</a:Action>   
<a:MessageID>urn:uuid:ed418b86-a75e-4aea-9d4e-a5d0cb5c088e</a:MessageID>  
<a:ReplyTo>   
<a:Address>https://...</a:Address>   
</a:ReplyTo>  
<a:To>https://...</a:To>   
<wsse:Security   
s:mustUnderstand="1"   
xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd"   
xmlns:wssu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd">  
<wssu:Timestamp wssu:Id="_0" >   
<wssu:Created>2005-12-15T23:36:13.827Z</wssu:Created>  
<wssu:Expires>2005-12-15T23:41:13.827Z</wssu:Expires>  
</wssu:Timestamp>   
<wsc:SecurityContextToken>   
<wssu:Identifier> http://fabrikam123.com/SCTi  
</wssu:Identifier>   
</wsc:SecurityContextToken>   
<!-- supporting signature over the timestamp -->  
<wsse:Signature xmlns:ds="http://www.w3.org/2000/09/xmldsig#">  
<ds:SignedInfo>   
<ds:CanonicalizationMethod Algorithm="http://www.w3.org/2001/10/xml-exc-c14n#"/>   
<ds:SignatureMethod Algorithm="http://www.w3.org/2000/09/xmldsig#hmac-sha1"/>   
<ds:Reference URI="#_0">   
<ds:Transforms>   
<ds:Transform Algorithm="http://www.w3.org/2001/10/xml-exc-c14n#"/>   
</ds:Transforms>   
<ds:DigestMethod  
Algorithm="http://www.w3.org/2000/09/xmldsig#sha1"/>   
<ds:DigestValue> alRzyhjLgoUOYoh8cx4n75eTcUk=  
</ds:DigestValue>   
</ds:Reference>   
</ds:SignedInfo>  
<ds:SignatureValue>YZYjnVvSOVasAQqQxaaviTSWtqI=  
</ds:SignatureValue>  
<ds:KeyInfo>   
<wsse:SecurityTokenReference xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd">  
  <wsse:Reference URI="http://fabrikam123.com/SCTi"/>  
</wsse:SecurityTokenReference>   
</ds:KeyInfo>   
</wsse:Signature>   
</wsse:Security>   
</s:Header>   
<s:Body xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">   
<wscoor:Register>   
<wscoor:ProtocolIdentifier>...</wscoor:ProtocolIdentifier>  
<wscoor:ParticipantProtocolService>   
<a:Address>https://... </a:Address>  
</wscoor:ParticipantProtocolService>   
</wscoor:Register>   
</s:Body>   
</s:Envelope>  
```  
  
#### <a name="register-response-with-wscoor-10"></a><span data-ttu-id="c462b-238">Register Response avec WSCoor 1.0</span><span class="sxs-lookup"><span data-stu-id="c462b-238">Register Response with WSCoor 1.0</span></span>  
  
```xml  
<s:Envelope>  
  <s:Header>  
    <a:Action>  
      http://schemas.xmlsoap.org/ws/2004/10/wscoor/RegisterResponse  
    </a:Action>  
    <a:MessageID>urn:uuid:ed418b86-a75e-4aea-9d4e-a5d0cb5c088d</a:MessageID>  
    <a:RelatesTo>  
      urn:uuid:ed418b86-a75e-4aea-9d4e-a5d0cb5c088e        
    </a:RelatesTo>  
    <a:To>https://...</a:To>  
    <wsse:Security   
      s:mustUnderstand="1"   
      xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd"  
      xmlns:wssu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd">  
      <wssu:Timestamp>  
        <wssu:Created>2005-12-15T23:36:13.827Z</wssu:Created>  
        <wssu:Expires>2005-12-15T23:41:13.827Z</wssu:Expires>  
      </wssu:Timestamp>  
    </wsse:Security>  
  </s:Header>  
  <s:Body xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">  
    <wscoor:RegisterResponse>  
      <wscoor:CoordinatorProtocolService>  
        <a:Address>https://...</a:Address>  
        <a:ReferenceParameters>  
          ...  
        </a:ReferenceParameters>  
      </wscoor:CoordinatorProtocolService>  
    </wscoor:RegisterResponse>  
  </s:Body>  
</s:Envelope>  
```  
  
#### <a name="register-response-with-wscoor-11"></a><span data-ttu-id="c462b-239">Register Response avec WSCoor 1.1</span><span class="sxs-lookup"><span data-stu-id="c462b-239">Register Response with WSCoor 1.1</span></span>  
  
```xml  
<s:Envelope>  
<s:Header>   
<a:Action> http://docs.oasis-open.org/ws-tx/wscoor/2006/06/RegisterResponse  
</a:Action>   
<a:MessageID>urn:uuid:ed418b86-a75e-4aea-9d4e-a5d0cb5c088d</a:MessageID>  
<a:RelatesTo> urn:uuid:ed418b86-a75e-4aea-9d4e-a5d0cb5c088e </a:RelatesTo>  
<a:To>https://...</a:To>   
<wsse:Security   
s:mustUnderstand="1"   
xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd"   
xmlns:wssu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd">   
<wssu:Timestamp>   
<wssu:Created>2005-12-15T23:36:13.827Z</wssu:Created>  
<wssu:Expires>2005-12-15T23:41:13.827Z</wssu:Expires>  
</wssu:Timestamp>   
</wsse:Security>   
</s:Header>   
<s:Body xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">   
<wscoor:RegisterResponse>   
<wscoor:CoordinatorProtocolService>  
<a:Address>https://...</a:Address>  
<a:ReferenceParameters> ... </a:ReferenceParameters>  
</wscoor:CoordinatorProtocolService>   
</wscoor:RegisterResponse>   
</s:Body>   
</s:Envelope>  
```  
  
### <a name="two-phase-commit-protocol-messages"></a><span data-ttu-id="c462b-240">Messages de protocole de validation à deux phases</span><span class="sxs-lookup"><span data-stu-id="c462b-240">Two Phase Commit Protocol Messages</span></span>  
 <span data-ttu-id="c462b-241">Le message suivant concerne le protocole de validation en deux phases (2PC).</span><span class="sxs-lookup"><span data-stu-id="c462b-241">The following message relates to the two-phase commit (2PC) protocol.</span></span>  
  
#### <a name="commit-with-wsat-10"></a><span data-ttu-id="c462b-242">COMMIT avec WSAT 1.0</span><span class="sxs-lookup"><span data-stu-id="c462b-242">Commit with WSAT 1.0</span></span>  
  
```xml  
<s:Envelope>  
  <s:Header>  
    <a:Action>http://.../ws/2004/10/wsat/Commit</a:Action>  
    <a:To>https://...</a:To>  
    <wsse:Security   
      s:mustUnderstand="1"   
      xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd"  
      xmlns:wssu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd">  
      <wssu:Timestamp wssu:Id="_0" >  
        <wssu:Created>2005-12-15T23:36:13.827Z</wssu:Created>  
        <wssu:Expires>2005-12-15T23:41:13.827Z</wssu:Expires>  
      </wssu:Timestamp>  
   </wsse:Security>  
  </s:Header>  
  <s:Body xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">  
    <wsat:Commit />  
  </s:Body>  
</s:Envelope>  
```  
  
#### <a name="commit-with-wsat-11"></a><span data-ttu-id="c462b-243">Commit avec WSAT 1.1</span><span class="sxs-lookup"><span data-stu-id="c462b-243">Commit with WSAT 1.1</span></span>  
  
```xml  
<s:Envelope>  
<s:Header>   
<a:Action>http://docs.oasis-open.org/ws-tx/wsat/2006/06</a:Action>  
<a:To>https://...</a:To>   
<wsse:Security   
s:mustUnderstand="1"   
xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd"   
xmlns:wssu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd">   
<wssu:Timestamp wssu:Id="_0" >   
<wssu:Created>2005-12-15T23:36:13.827Z</wssu:Created>  
<wssu:Expires>2005-12-15T23:41:13.827Z</wssu:Expires>  
</wssu:Timestamp>   
</wsse:Security>   
</s:Header>   
<s:Body xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">   
<wsat:Commit />   
</s:Body>   
</s:Envelope>  
```  
  
### <a name="application-messages"></a><span data-ttu-id="c462b-244">Messages d'application</span><span class="sxs-lookup"><span data-stu-id="c462b-244">Application Messages</span></span>  
 <span data-ttu-id="c462b-245">Les messages suivants sont des messages d'application.</span><span class="sxs-lookup"><span data-stu-id="c462b-245">The following messages are application messages.</span></span>  
  
#### <a name="application-message-request"></a><span data-ttu-id="c462b-246">Message d'application - demande</span><span class="sxs-lookup"><span data-stu-id="c462b-246">Application message-Request</span></span>  
  
```xml  
<s:Envelope>  
  <s:Header>  
<!-- Addressing headers, all signed-->  
    <wsse:Security s:mustUnderstand="1">  
      <wssu:Timestamp wssu:Id="timestamp">   
        <wssu:Created>2005-10-25T06:29:18.703Z</wssu:Created>  
        <wssu:Expires>2005-10-25T06:34:18.703Z</wssu:Expires>  
      </wssu:Timestamp>  
      <wsse:BinarySecurityToken   
          wssu:Id="IA_Certificate"   
          ValueType="...#X509v3"   
          EncodingType="...#Base64Binary">  
        <!-- IA certificate -->  
      </wsse:BinarySecurityToken>  
      <e:EncryptedKey Id="encrypted_key">  
            <!-- ephemeral key encrypted for PA certificate -->    
        <e:ReferenceList xmlns:e="http://www.w3.org/2001/04/xmlenc#">  
          <e:DataReference URI="#encrypted_body"/>  
          <e:DataReference URI="#encrypted_CCi"/>  
          <e:DataReference URI="#encrypted_issuedtokens"/>  
        </e:ReferenceList>  
      </e:EncryptedKey>  
      <Signature xmlns="http://www.w3.org/2000/09/xmldsig#">  
        <!-- signature over Addressing headers, Timestamp, and Body -->  
      </Signature>  
    </wsse:Security>  
    <wsse11:EncryptedHeader >  
     <!-- encrypted wscoor:CoordinationContext header containing CCi -->  
    </wsse11:EncryptedHeader>  
    <wsse11:EncryptedHeader   
      <!-- encrypted wst:IssuedTokens header containing SCTi -->  
      <!-- wst:IssuedTokens header is taken verbatim from message #2 above, omitted for brevity -->  
    </wsse11:EncryptedHeader>  
  </s:Header>  
  <s:Body wssu:Id="body">  
    <!-- encrypted content of the Body element of the application message -->      
    <e:EncryptedData Id="encrypted_body"   
           Type="http://www.w3.org/2001/04/xmlenc#Content"   
           xmlns:e="http://www.w3.org/2001/04/xmlenc#">  
...  
    </e:EncryptedData>  
  </s:Body>  
</s:Envelope>  
```
