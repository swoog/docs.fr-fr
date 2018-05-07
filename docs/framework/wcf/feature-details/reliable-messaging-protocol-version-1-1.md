---
title: Protocole de messagerie fiable version 1,1
ms.date: 03/30/2017
ms.assetid: 0da47b82-f8eb-42da-8bfe-e56ce7ba6f59
ms.openlocfilehash: 8ff02bc6953ec1e5030dd0b592a352b7e23ab0d6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="reliable-messaging-protocol-version-11"></a>Protocole de messagerie fiable version 1,1
Cette rubrique couvre les détails d’implémentation de Windows Communication Foundation (WCF) pour la messagerie WS-Reliable protocole février 2007 (version 1.1) nécessaire pour l’interopérabilité via le transport HTTP. WCF suit la spécification WS-ReliableMessaging avec les contraintes et les éclaircissements présentés dans cette rubrique. Notez que le protocole de la version 1.1 de WS-ReliableMessaging est implémenté en commençant par le [!INCLUDE[netfx35_long](../../../../includes/netfx35-long-md.md)].  
  
 Le WS-ReliableMessaging de février 2007 protocole est implémenté dans WCF par le <xref:System.ServiceModel.Channels.ReliableSessionBindingElement>.  
  
 Pour plus de simplicité, la rubrique utilise les rôles suivants :  
  
-   Initiateur : client qui initialise la création de séquence de message WS-Reliable .  
  
-   Répondeur : service qui reçoit les demandes de l'initiateur.  
  
 Ce document utilise les préfixes et les espaces de noms répertoriés dans le tableau suivant.  
  
|Préfixe|Espace de noms|  
|-|-|  
|wsrm|http://docs.oasis-open.org/ws-rx/wsrm/200702|  
|netrm|http://schemas.microsoft.com/ws/2006/05/rm|  
|s|http://www.w3.org/2003/05/soap-envelope|  
|wsa|http://schemas.xmlsoap.org/ws/2005/08/addressing|  
|wsse|http://docs.oasis-open.org/wss/2004/01/oasis-200401-wssecurity-secext-1.0.xsd|  
|wsrmp|http://docs.oasis-open.org/ws-rx/wsrmp/200702|  
|netrmp|http://schemas.microsoft.com/ws-rx/wsrmp/200702|  
|wsp|(WS-Policy 1.2 ou WS-Policy 1.5)|  
  
## <a name="messaging"></a>Messagerie  
  
### <a name="sequence-creation"></a>Création de la séquence  
 WCF implémente `CreateSequence` et `CreateSequenceResponse` de séquence de messages pour établir une messagerie fiable. Les contraintes suivantes s'appliquent :  
  
-   B1101 : L’initiateur WCF utilise la même référence de point de terminaison en tant que le `CreateSequence` du message `ReplyTo`, `AcksTo` et `Offer/Endpoint`.  
  
-   R1102 : les références de point de terminaison `AcksTo`, `ReplyTo` et `Offer/Endpoint` dans le message `CreateSequence` doivent avoir des valeurs d'adresse avec des représentations sous forme de chaîne identiques qui correspondent à l'octet.  
  
    -   Le répondeur WCF vérifie que la partie de l’URI de la `AcksTo`, `ReplyTo` et `Endpoint` les références de point de terminaison sont identiques avant de créer une séquence.  
  
-   R1103 : les références de point de terminaison `AcksTo`, `ReplyTo` et `Offer/Endpoint` dans le message `CreateSequence` doivent avoir le même jeu de paramètres de référence.  
  
    -   WCF n’applique pas, mais part du principe qui font référence les paramètres de la `AcksTo`, `ReplyTo` et `Offer/Endpoint` référence de point de terminaison sur `CreateSequence` sont identiques et utilise les paramètres de référence à partir de la `ReplyTo` référence de point de terminaison pour accusés de réception et les messages de séquence inverse.  
  
-   B1104 : L’initiateur WCF ne génère pas le paramètre facultatif `Expires` ou `Offer/Expires` élément dans le `CreateSequence` message.  
  
-   B1105 : Lors de l’accès le `CreateSequence` message, le répondeur WCF utilise le `Expires` valeur dans le `CreateSequence` élément en tant que le `Expires` valeur dans le `CreateSequenceResponse` élément. Dans le cas contraire, le répondeur WCF lit et ignore le `Expires` et `Offer/Expires` valeurs.  
  
-   B1106 : Lors de l’accès à la `CreateSequenceResponse` message, l’initiateur WCF lit le paramètre facultatif `Expires` valeur mais ne l’utilise pas.  
  
-   B1107 : L’initiateur de WCF et le répondeur génèrent toujours facultatif `IncompleteSequenceBehavior` élément dans le `CreateSequence/Offer` et `CreateSequenceResponse` éléments.  
  
-   B1108 : WCF utilise uniquement le `DiscardFollowingFirstGap` et `NoDiscard` des valeurs dans le `IncompleteSequenceBehavior` élément.  
  
    -   WS-ReliableMessaging utilise le mécanisme `Offer` pour établir deux séquences corrélées réciproques qui forment une session.  
  
-   B1109 : Si `CreateSequence` contient un `Offer` élément, le répondeur WCF unidirectionnel rejette la séquence en répondant avec un `CreateSequenceResponse` sans un `Accept` élément.  
  
-   B1110 : Si un répondeur de messagerie fiable rejette la séquence, l’initiateur WCF fait échouer la séquence récemment établie.  
  
-   B1111 : Si `CreateSequence` ne contient pas un `Offer` élément, le répondeur WCF bidirectionnel rejette la séquence en répondant avec un `CreateSequenceRefused` erreur.  
  
-   R1112 : lorsque deux séquences réciproques sont établies à l'aide du mécanisme `Offer`, la propriété `[address]` de la référence du point de terminaison `CreateSequenceResponse/Accept/AcksTo` doit correspondre à l'URI de destination du message `CreateSequence` octet par octet.  
  
-   R1113 : lorsque deux séquences réciproques sont établies à l'aide du mécanisme `Offer`, tous les messages sur les deux séquences circulant de l'initiateur au répondeur doivent être envoyés à la même référence de point de terminaison.  
  
 WCF utilise WS-ReliableMessaging pour établir des sessions fiables entre l’initiateur et le répondeur. L’implémentation de WCF WS-ReliableMessaging fournit une session fiable pour, demande-réponse et unidirectionnels intégral duplex modèles de messagerie. Le mécanisme WS-ReliableMessaging `Offer` sur `CreateSequence` et `CreateSequenceResponse` vous permet d'établir deux séquences réciproques corrélées et fournit un protocole de session qui convient à tous les points de terminaison de message. WCF fournit une garantie de sécurité pour une telle session, y compris la protection de bout en bout pour l’intégrité de session, il est pratique de s’assurer que les messages destinés à la même partie arrivent à la même destination. Cela autorise également la « superposition » des accusés de réception de séquence sur les messages d'application. Par conséquent, les contraintes R1102, R1112 et R1113 s’appliquent à WCF.  
  
 Exemple de message `CreateSequence`.  
  
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
  
 Exemple de message `CreateSequenceResponse`.  
  
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
  
### <a name="closing-a-sequence"></a>Fermeture d'une séquence  
 WCF utilise le `CloseSequence` et `CloseSequenceResponse` messages pour un arrêt initié par la source de messagerie fiable. La destination de messagerie fiable WCF n’initie pas l’arrêt et la source de messagerie fiable WCF ne prend pas en charge un arrêt initié par la destination de messagerie fiable. Les contraintes suivantes s'appliquent :  
  
-   B1201 : La source de messagerie fiable WCF envoie toujours un `CloseSequence` message pour arrêter la séquence.  
  
-   B1202 : la source de la messagerie fiable attend l'accusé de réception de l'ensemble complet des messages de séquence avant d'envoyer le message `CloseSequence`.  
  
-   B1203 : la source de messagerie fiable inclut toujours l'élément `LastMsgNumber` facultatif sauf si la séquence ne contient pas de messages.  
  
-   R1204 : la destination de messagerie fiable ne doit pas initier l'arrêt en envoyant un message `CloseSequence`.  
  
-   B1205 : À recevoir un `CloseSequence` message, la source de messagerie fiable WCF considère que la séquence est incomplète et envoie une erreur.  
  
 Exemple de message `CloseSequence`.  
  
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
  
### <a name="sequence-termination"></a>Séquence d'arrêt  
 WCF utilise principalement le `TerminateSequence/TerminateSequenceResponse` la négociation de la fin de la `CloseSequence/CloseSequenceResponse` la négociation. La destination de messagerie fiable WCF n’initie pas l’arrêt et la source de messagerie fiable ne prend pas en charge un arrêt initié par la destination de messagerie fiable. Les contraintes suivantes s'appliquent :  
  
-   B1301 : L’initiateur WCF envoie uniquement la `TerminateSequence` message après l’achèvement réussi de la `CloseSequence/CloseSequenceResponse` protocole de transfert.  
  
-   R1302 : WCF valide que le `LastMsgNumber` élément est cohérent dans tous les `CloseSequence` et `TerminateSequence` messages pour une séquence donnée. Cela signifie que `LastMsgNumber` est soit absent sur tous les messages `CloseSequence` et `TerminateSequence`, soit présent et identique sur tous les messages `CloseSequence` et `TerminateSequence`.  
  
-   B1303 : à la réception d'un message `TerminateSequence` après la négociation de sécurité `CloseSequence/CloseSequenceResponse`, la destination de messagerie fiable répond avec un message `TerminateSequenceResponse`. Étant donné que la source de messagerie fiable a l'accusé de réception final avant d'envoyer le message `TerminateSequence`, la destination de messagerie fiable sait sans doute que la séquence se termine, et libère immédiatement les ressources.  
  
-   B1304 : Lors de la réception un `TerminateSequence` message antérieures à la `CloseSequence/CloseSequenceResponse` protocole de transfert, la destination de messagerie fiable WCF répond avec un `TerminateSequenceResponse` message. Si la destination de messagerie fiable détermine que la séquence ne contient aucune incohérence, elle attend l'heure spécifiée par la destination d'une application avant de libérer des ressources afin de permettre au client de recevoir l'accusé de réception final. Sinon, la destination de messagerie fiable libère immédiatement des ressources et indique à la destination d'application que la séquence se termine en déclenchant l'événement `Faulted`.  
  
 Exemple de message `TerminateSequence`.  
  
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
  
### <a name="sequences"></a>Séquences  
 Voici une liste des contraintes qui s'appliquent aux séquences :  
  
-   B1401:WCF génère et ne dépassant pas de numéros de séquence accède à `xs:long`de valeur inclusive maximale, 9223372036854775807.  
  
 Exemple d'en-tête `Sequence`.  
  
```xml  
<wsrm:Sequence s:mustUnderstand="1">  
  <wsrm:Identifier>urn:uuid:656652b8-9af2-4e94-9d07-2dc21c05ed27</wsrm:Identifier>  
  <wsrm:MessageNumber>1</wsrm:MessageNumber>  
</wsrm:Sequence>  
```  
  
### <a name="request-acknowledgement"></a>Demander un accusé de réception  
 WCF utilise le `AckRequested` en-tête comme un mécanisme de persistance.  
  
 Exemple d'en-tête `AckRequested`.  
  
```xml  
<wsrm:AckRequested>  
  <wsrm:Identifier>urn:uuid:656652b8-9af2-4e94-9d07-2dc21c05ed27</wsrm:Identifier>  
</wsrm:AckRequested>  
```  
  
### <a name="sequenceacknowledgement"></a>SequenceAcknowledgement  
 WCF utilise un mécanisme de « superposition » des accusés de réception de séquence fournis dans la messagerie WS-Reliable. Les contraintes suivantes s'appliquent :  
  
-   R1601 : Lorsque deux séquences réciproques sont établies à l’aide de la `Offer` mécanisme, la `SequenceAcknowledgement` en-tête peut être inclus dans n’importe quel message d’application transmis au destinataire prévu. Le point de terminaison distant doit être en mesure d'accéder à un en-tête `SequenceAcknowledgement` superposé.  
  
-   B1602 : WCF ne génère pas `SequenceAcknowledgement` en-têtes qui contiennent `Nack` éléments. WCF valide que chaque `Nack` élément contient un numéro de séquence, mais sinon ignore le `Nack` élément et la valeur.  
  
 Exemple d'en-tête `SequenceAcknowledgement`.  
  
```xml  
<wsrm:SequenceAcknowledgement>  
  <wsrm:Identifier>urn:uuid:656652b8-9af2-4e94-9d07-2dc21c05ed27</wsrm:Identifier>  
  <wsrm:AcknowledgementRange Lower="1" Upper="1"></wsrm:AcknowledgementRange>  
</wsrm:SequenceAcknowledgement>  
```  
  
### <a name="ws-reliablemessaging-faults"></a>Erreurs de la messagerie WS-Reliable  
 Voici une liste de contraintes qui s’appliquent à l’implémentation de WCF d’erreurs WS-ReliableMessaging. Les contraintes suivantes s'appliquent :  
  
-   B1701 : WCF ne génère pas `MessageNumberRollover` erreurs.  
  
-   B1702 : Sur SOAP 1.2, lorsque le point de terminaison de service atteint sa limite de connexions et ne peut pas traiter de nouvelles connexions, WCF génère une liste imbriquée `CreateSequenceRefused` sous-code, d’erreur `netrm:ConnectionLimitReached`, comme illustré dans l’exemple suivant.  
  
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
  
### <a name="ws-addressing-faults"></a>Erreurs WS-Addressing  
 Étant donné que WS-ReliableMessaging utilise WS-Addressing, l’implémentation de WCF WS-ReliableMessaging peut générer et transmettre des erreurs WS-Addressing. Cette section décrit les erreurs WS-Addressing WCF génère explicitement et transmet au niveau de la couche WS-ReliableMessaging :  
  
-   B1801:WCF génère et transmet le `Message Addressing Header Required` d’erreur lorsque l’une des valeurs suivantes est vraie :  
  
    -   Il manque un en-tête `CreateSequence` à un message `CloseSequence`, `TerminateSequence` ou `MessageId`.  
  
    -   Il manque un en-tête `CreateSequence` à un message `CloseSequence`, `TerminateSequence` ou `ReplyTo`.  
  
    -   Il manque un en-tête `CreateSequenceResponse` à un message `CloseSequenceResponse`, `TerminateSequenceResponse` ou `RelatesTo`.  
  
-   B1802:WCF génère et transmet le `Endpoint Unavailable` indiquent il n’y a aucun point de terminaison qui écoute la panne peut traiter la séquence en fonction de l’examen des en-têtes d’adressage dans le `CreateSequence` message.  
  
## <a name="protocol-composition"></a>Composition du protocole  
  
### <a name="composition-with-ws-addressing"></a>Composition avec WS-Addressing  
 WCF prend en charge deux versions de WS-Addressing : WS-Addressing 2004/08 [WS-ADDR] et W3C WS-Addressing 1.0 Recommendations [WS-ADDR-CORE] et [WS-ADDR-SOAP].  
  
 Si la spécification WS-ReliableMessaging mentionne WS-Addressing 2004/08 uniquement, elle ne limite pas la version WS-Addressing à utiliser. Voici une liste de contraintes qui s’appliquent à WCF :  
  
-   R2101 : WS-Addressing 2004/08 et WS-Addressing 1.0 peuvent être utilisés ensemble avec la messagerie WS-Reliable.  
  
-   R2102 : une version unique de WS-Addressing doit être utilisée dans l'ensemble d'une séquence WS-ReliableMessaging ou une paire de séquences réciproques corrélées à l'aide du mécanisme `Offer`.  
  
### <a name="composition-with-soap"></a>Composition avec SOAP  
 WCF prend en charge l’utilisation de SOAP 1.1 et SOAP 1.2 avec la messagerie WS-Reliable.  
  
### <a name="composition-with-ws-security-and-ws-secureconversation"></a>Composition avec WS-Security et WS-SecureConversation  
 WCF offre une protection pour les séquences de WS-ReliableMessaging à l’aide du Transport (HTTPS) sécurisée, la composition avec WS-Security et composition avec WS-Secure Conversation. Le protocole WS-ReliableMessaging 1.1, WS-Security 1.1 et le protocole WS-Secure Conversation 1.3 doivent être utilisés ensemble. Voici une liste de contraintes qui s’appliquent à WCF :  
  
-   R2301 : Pour protéger l’intégrité d’une séquence WS-ReliableMessaging en plus de l’intégrité et la confidentialité des messages individuels, WCF requiert que WS-Secure Conversation doit être utilisée.  
  
-   R2302:AWS-session de Secure Conversation doit être établie avant d’établir des séquences de WS-ReliableMessaging.  
  
-   R2303 : si la durée de vie de la séquence WS-ReliableMessaging dépasse celle de la session WS-Secure Conversation, le `SecurityContextToken` établi à l'aide de WS-Secure Conversation doit être renouvelé par le biais de la liaison de renouvellement WS-Secure Conversation correspondante.  
  
-   B2304:WS-ReliableMessaging séquence ou une paire de séquences réciproques corrélées sont toujours liées à une seule session WS-SecureConversation.  
  
-   R2305 : Lorsqu’il est composé avec WS-Secure Conversation, le répondeur WCF requiert que le `CreateSequence` message contient la `wsse:SecurityTokenReference` élément et le `wsrm:UsesSequenceSTR` en-tête.  
  
 Exemple d'en-tête `UsesSequenceSTR`.  
  
```xml  
<wsrm:UsesSequenceSTR></wsrm:UsesSequenceSTR>  
```  
  
### <a name="composition-with-ssltls-sessions"></a>Composition avec les sessions SSL/TLS  
 WCF ne prend pas en charge la composition avec les sessions SSL/TLS :  
  
-   B2401 : WCF ne génère pas le `wsrm:UsesSequenceSSL` en-tête.  
  
-   R2402 : Un initiateur de messagerie fiable ne doit pas envoyer un `CreateSequence` des messages avec un `wsrm:UsesSequenceSSL` en-tête à un répondeur de WCF.  
  
### <a name="composition-with-ws-policy"></a>Composition avec WS-Policy  
 WCF prend en charge deux versions de WS-Policy : WS-Policy 1.2 et WS-Policy 1.5.  
  
## <a name="ws-reliablemessaging-ws-policy-assertion"></a>Assertion WS-Policy de la messagerie WS-ReliableMessaging  
 WCF utilise l’Assertion de WS-Policy WS-ReliableMessaging `wsrm:RMAssertion` pour décrire les capacités de points de terminaison. Voici une liste de contraintes qui s’appliquent à WCF :  
  
-   B3001 : WCF associe `wsrmn:RMAssertion` Assertion WS-Policy pour `wsdl:binding` éléments. WCF prend en charge des pièces jointes aux `wsdl:binding` et `wsdl:port` éléments.  
  
-   B3002 : WCF génère jamais la `wsp:Optional` balise.  
  
-   B3003 : Lors de l’accès à la `wsrmp:RMAssertion` Assertion WS-Policy, WCF ignore le `wsp:Optional` de balise et traite la stratégie de WS-RM comme obligatoire.  
  
-   R3004 : Étant donné que WCF ne compose pas avec les sessions SSL/TLS, WCF n’accepte pas de stratégie qui spécifie `wsrmp:SequenceTransportSecurity`.  
  
-   B3005 : WCF génère toujours le `wsrmp:DeliveryAssurance` élément.  
  
-   B3006 : WCF spécifie toujours le `wsrmp:ExactlyOnce` garantie de remise.  
  
-   B3007 : WCF génère et lit les propriétés suivantes de l’assertion WS-ReliableMessaging et assure leur contrôle sur WCF`ReliableSessionBindingElement`:  
  
    -   `netrmp:InactivityTimeout`  
  
    -   `netrmp:AcknowledgementInterval`  
  
     Exemple de `RMAssertion`.  
  
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
  
## <a name="flow-control-ws-reliablemessaging-extension"></a>Extension de messagerie WS-Reliable pour le contrôle de flux  
 WCF utilise WS-ReliableMessaging extensibilité pour renforcer le contrôle facultatif sur le flux de message de séquence.  
  
 Contrôle de flux est activé en définissant le `ReliableSessionBindingElement`de `FlowControlEnabled``boolean` propriété `true`. Voici une liste de contraintes qui s’appliquent à WCF :  
  
-   B4001 : Lorsque le contrôle de flux de messagerie fiable est activée, WCF génère une `netrm:BufferRemaining` élément dans l’élément d’extensibilité de la `SequenceAcknowledgement` en-tête, comme indiqué dans l’exemple suivant.  
  
    ```xml  
    <wsrm:SequenceAcknowledgement>  
      <wsrm:Identifier>urn:uuid:656652b8-9af2-4e94-9d07-2dc21c05ed27</wsrm:Identifier>  
      <wsrm:AcknowledgementRange Upper="1" Lower="1"/>             
      <netrm:BufferRemaining>8</netrm:BufferRemaining>  
    </wsrm:SequenceAcknowledgement>  
    ```  
  
-   B4002 : Même lorsque le contrôle de flux de messagerie fiable est activée, WCF ne requiert pas qu’un `netrm:BufferRemaining` élément dans le `SequenceAcknowledgement` en-tête.  
  
-   B4003 : Utilise de Destination de messagerie fiable WCF `netrm:BufferRemaining` pour indiquer combien de nouveaux messages elle peut mettre en mémoire tampon.  
  
-   B4004:when fiable de flux de contrôle de messagerie est activé, la Source de messagerie fiable WCF utilise la valeur de `netrm:BufferRemaining` pour limiter la transmission des messages.  
  
-   B4005 : WCF génère `netrm:BufferRemaining` entier de valeurs comprises entre 0 et 4096 inclus et lit les valeurs de nombre entier compris entre 0 et `xs:int`de `maxInclusive` valeur 214748364 inclus.  
  
## <a name="message-exchange-patterns"></a>Modèles d’échange de messages  
 Cette section décrit le comportement de WCF lorsque WS-ReliableMessaging est utilisé pour différents modèles d’échange de messages. Pour chaque modèle d’échange de messages, les deux scénarios de déploiements suivants sont considérés :  
  
-   Initiateur non adressable : l'initiateur est derrière un pare-feu ; le répondeur peut remettre uniquement des messages à celui-ci sur les réponses HTTP.  
  
-   Initiateur adressable : l'initiateur et le répondeur peuvent tous les deux recevoir des requêtes HTTP ; en d'autres termes, deux connexions HTTP réciproques peuvent être établies.  
  
### <a name="one-way-non-addressable-initiator"></a>Initiateur unidirectionnel, non adressable  
  
#### <a name="binding"></a>Liaison  
 WCF fournit un modèle d’échange de messages unidirectionnels à l’aide d’une séquence sur un canal HTTP. WCF utilise les requêtes HTTP pour transmettre les messages à partir de l’initiateur pour les répondeur et les réponses HTTP pour transmettre les messages de répondeur à l’initiateur.  
  
#### <a name="createsequence-exchange"></a>Échange CreateSequence  
 L’initiateur WCF transmet un `CreateSequence` message sans aucune `Offer` élément sur une requête HTTP et attend le `CreateSequenceResponse` message dans la réponse HTTP. Le répondeur WCF crée une séquence et transmet le `CreateSequenceResponse` message sans aucune `Accept` élément sur la réponse HTTP.  
  
#### <a name="sequenceacknowledgement"></a>SequenceAcknowledgement  
 L’initiateur WCF traite les accusés de réception de la réponse de tous les messages sauf le `CreateSequence` message et les messages d’erreur. Le répondeur WCF transmet toujours un accusé de réception autonome sur la réponse HTTP à toutes les séquences et `AckRequested` messages.  
  
#### <a name="closesequence-exchange"></a>Échange CloseSequence  
 L’initiateur WCF transmet un `CloseSequence` le message sur une requête HTTP et attend le `CreateSequenceResponse` message dans la réponse HTTP. Le répondeur WCF transmet le `CloseSequenceResponse` message dans la réponse HTTP.  
  
#### <a name="terminatesequence-exchange"></a>Échange TerminateSequence  
 L’initiateur WCF transmet un `TerminateSequence` le message sur une requête HTTP et attend le `TerminateSequenceResponse` message dans la réponse HTTP. Le répondeur WCF transmet le `TerminateSequenceResponse` message dans la réponse HTTP.  
  
### <a name="one-way-addressable-initiator"></a>Initiateur unidirectionnel, adressable  
  
#### <a name="binding"></a>Liaison  
 WCF fournit un modèle d’échange de messages unidirectionnels à l’aide d’une séquence sur un trafic entrant et un canal HTTP sortant. WCF utilise les requêtes HTTP pour transmettre les messages. Toutes les réponses HTTP ont un corps vide et le code d'état HTTP 202.  
  
#### <a name="createsequence-exchange"></a>Échange CreateSequence  
 L’initiateur WCF transmet un `CreateSequence` message sans aucune `Offer` élément sur une requête HTTP. Le répondeur WCF crée une séquence et transmet le `CreateSequenceResponse` message sans aucune `Accept` élément sur une requête HTTP.  
  
### <a name="duplex-addressable-initiator"></a>Initiateur duplex, adressable  
  
#### <a name="binding"></a>Liaison  
 WCF fournit un modèle d’échange de messages asynchrone complet, bidirectionnel utilise deux séquences sur un trafic entrant et un canal HTTP sortant. Ce modèle d'échange de messages peut être combiné avec le modèle d'échange de messages initiateur `Request/Reply`, `Addressable` d'une manière limitée. WCF utilise les requêtes HTTP pour transmettre les messages. Toutes les réponses HTTP ont un corps vide et le code d'état HTTP 202.  
  
#### <a name="createsequence-exchange"></a>Échange CreateSequence  
 L’initiateur WCF transmet un `CreateSequence` des messages avec un `Offer` élément sur une requête HTTP. Le répondeur de WCF garantit que le `CreateSequence` a un `Offer` élément, puis crée une séquence et transmet le `CreateSequenceResponse` des messages avec un `Accept` élément.  
  
#### <a name="sequence-lifetime"></a>Durée de vie de séquence  
 WCF traite les deux séquences comme une session duplex complète.  
  
 Générer une erreur qui fait échouer une séquence, WCF attend le point de terminaison distant pour les deux séquences d’erreur. Lors de la lecture d’une erreur qui fait échouer une séquence, WCF fait échouer les deux séquences.  
  
 WCF peut fermer sa séquence sortante et continuer à traiter les messages sur sa séquence entrante. À l’inverse, WCF peut traiter la fermeture de la séquence entrante et continuer à envoyer des messages sur sa séquence sortante.  
  
### <a name="request-reply-and-one-way-non-addressable-initiator"></a>Initiateur demande-réponse, unidirectionnel et non adressable  
  
#### <a name="binding"></a>Liaison  
 WCF fournit unidirectionnel et modèle d’échange de messages demande-réponse à l’aide de deux séquences sur un canal HTTP. WCF utilise les requêtes HTTP pour transmettre les messages à partir de l’initiateur pour les répondeur et les réponses HTTP pour transmettre les messages de répondeur à l’initiateur.  
  
#### <a name="createsequence-exchange"></a>Échange CreateSequence  
 L’initiateur WCF transmet un `CreateSequence` des messages avec un `Offer` élément sur une requête HTTP et attend le `CreateSequenceResponse` message dans la réponse HTTP. Le répondeur WCF crée une séquence et transmet le `CreateSequenceResponse` des messages avec un `Accept` élément sur la réponse HTTP.  
  
#### <a name="one-way-message"></a>Message unidirectionnel  
 Pour effectuer un échange de messages unidirectionnels avec succès, l’initiateur de WCF transmet un message de séquence de demande sur la requête HTTP et reçoit un autonome `SequenceAcknowledgement` message dans la réponse HTTP. `SequenceAcknowledgement` doit accepter le message transmis.  
  
 Le répondeur WCF peut répondre à la demande avec un accusé de réception, une erreur ou une réponse avec un corps vide et le code d’état HTTP 202.  
  
#### <a name="two-way-messages"></a>Messages bidirectionnels  
 Pour effectuer un protocole d’échange de messages bidirectionnel avec succès, l’initiateur de WCF transmet un message de séquence de demande sur la requête HTTP et reçoit un message de séquence de réponse sur la réponse HTTP. La réponse doit contenir un `SequenceAcknowledgement` qui accuse réception du message de séquence de demande transmis.  
  
 Le répondeur WCF peut répondre à la demande avec une réponse d’application, une erreur ou une réponse avec un corps vide et le code d’état HTTP 202.  
  
 En raison de la présence de messages unidirectionnels et du délai d'attente des réponses d'application, le numéro de séquence du message de séquence de demande et le numéro de séquence du message de réponse n'ont aucune corrélation.  
  
#### <a name="retrying-replies"></a>Nouvelles tentatives de réponses  
 WCF s’appuie sur la corrélation demande-réponse HTTP pour la corrélation protocole d’échange de messages bidirectionnel. Pour cette raison, l’initiateur WCF n’arrête pas une nouvelle tentative d’un message de séquence de demande lorsque le message de séquence de demande est accepté mais plutôt lorsque la réponse HTTP contient un `SequenceAcknowledgement`, réponse de l’application ou une erreur. Le répondeur WCF réessaie des réponses sur la réponse HTTP de la demande à laquelle la réponse est corrélée.  
  
#### <a name="closesequence-exchange"></a>Échange CloseSequence  
 Après réception de tous les messages de séquence de réponse et les accusés de réception pour tous les messages de séquence de demande unidirectionnels, l’initiateur WCF transmet un `CloseSequence` de messages pour la séquence de demande sur une requête HTTP et attend le `CloseSequenceResponse` sur la réponse HTTP.  
  
 La fermeture de la séquence de demande ferme implicitement la séquence de réponse. Cela signifie que l’initiateur WCF inclut finale la séquence de réponse `SequenceAcknowledgement` sur la `CloseSequence` message et la séquence de réponse n’a pas un `CloseSequence` exchange.  
  
 Le répondeur de WCF garantit toutes les réponses sont acceptées et transmet le `CloseSequenceResponse` message dans la réponse HTTP.  
  
#### <a name="terminatesequence-exchange"></a>Échange TerminateSequence  
 Après avoir reçu le `CloseSequenceResponse` transmet des messages, l’initiateur de WCF un `TerminateSequence` de messages pour la séquence de demande sur une requête HTTP et attend le `TerminateSequenceResponse` sur la réponse HTTP.  
  
 Comme l'échange `CloseSequence`, terminer la séquence de demande termine implicitement la séquence de réponse. Cela signifie que l’initiateur WCF inclut final de la séquence de réponse `SequenceAcknowledgement` sur la `TerminateSequence` message et la séquence de réponse n’a pas un `TerminateSequence` exchange.  
  
 Le répondeur WCF transmet le `TerminateSequenceResponse` message dans la réponse HTTP.  
  
### <a name="requestreply-addressable-initiator"></a>Initiateur demande/réponse, adressable  
  
#### <a name="binding"></a>Liaison  
 WCF fournit un modèle d’échange de message demande-réponse à l’aide de deux séquences sur un trafic entrant et un canal HTTP sortant. Ce modèle d'échange de messages peut être combiné avec le modèle d'échange de messages initiateur `Duplex, Addressable` d'une manière limitée. WCF utilise les requêtes HTTP pour transmettre les messages. Toutes les réponses HTTP ont un corps vide et le code d'état HTTP 202.  
  
#### <a name="createsequence-exchange"></a>Échange CreateSequence  
 L’initiateur WCF transmet un `CreateSequence` des messages avec un `Offer` élément sur une requête HTTP. Le répondeur de WCF garantit que le `CreateSequence` a un `Offer` élément, puis crée une séquence et transmet le `CreateSequenceResponse` des messages avec un `Accept` élément.  
  
#### <a name="requestreply-correlation"></a>Corrélation demande/réponse  
 Les points suivants s'appliquent à toutes les demandes et réponses corrélées :  
  
-   WCF vérifie toutes les applications demande messages portent un `ReplyTo` référence de point de terminaison et un `MessageId`.  
  
-   WCF s’applique à la référence de point de terminaison local en tant que chaque message de demande application `ReplyTo`. La référence de point de terminaison locale est `CreateSequence` du message `ReplyTo` pour l'initiateur et `CreateSequence` du message `To` pour le répondeur.  
  
-   WCF permet de s’assurer que demande entrante des messages portent un `MessageId` et un `ReplyTo`.  
  
-   WCF garantit la `ReplyTo` URI de la référence de point de terminaison de tous les messages de demande d’application correspond à la référence de point de terminaison local définie précédemment.  
  
-   WCF permet de s’assurer que toutes les réponses Gardez le bon `RelatesTo` et `To` en-têtes `wsa` règles de corrélation de demande/réponse.
