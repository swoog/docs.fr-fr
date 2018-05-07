---
title: Protocole de messagerie fiable version 1.0
ms.date: 03/30/2017
ms.assetid: a5509a5c-de24-4bc2-9a48-19138055dcce
ms.openlocfilehash: f45a0d5e50e9ab8a07a203d2c40ad36ef298a40d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="reliable-messaging-protocol-version-10"></a>Protocole de messagerie fiable version 1.0
Cette rubrique couvre les détails d’implémentation de Windows Communication Foundation (WCF) pour la messagerie WS-Reliable protocole février 2005 (version 1.0) nécessaire pour l’interopérabilité via le transport HTTP. WCF suit la spécification WS-Reliable Messaging avec les contraintes et les éclaircissements présentés dans cette rubrique. Notez que le protocole WS-ReliableMessaging version 1.0 est implémenté à partir de [!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)].  
  
 La messagerie WS-Reliable février 2005 protocole est implémenté dans WCF par le <xref:System.ServiceModel.Channels.ReliableSessionBindingElement>.  
  
 Pour plus de simplicité, la rubrique utilise les rôles suivants :  
  
-   Initiateur : client qui initialise la création de la séquence de message WS-Reliable.  
  
-   Répondeur : service qui reçoit les demandes de l'initiateur.  
  
 Ce document utilise les préfixes et les espaces de noms répertoriés dans le tableau suivant.  
  
|Préfixe|Espace de noms|  
|------------|---------------|  
|wsrm|http://schemas.xmlsoap.org/ws/2005/02/rm|  
|netrm|http://schemas.microsoft.com/ws/2006/05/rm|  
|s|http://www.w3.org/2003/05/soap-envelope|  
|wsa|http://schemas.xmlsoap.org/ws/2005/08/addressing|  
|wsse|http://docs.oasis-open.org/wss/2004/01/oasis-200401-wssecurity-secext-1.0.xsd|  
  
## <a name="messaging"></a>Messagerie  
  
### <a name="sequence-establishment-messages"></a>Messages d'établissement de séquence  
 WCF implémente `CreateSequence` et `CreateSequenceResponse` messages pour établir une séquence de message fiable. Les contraintes suivantes s'appliquent :  
  
-   B1101 : L’initiateur WCF ne génère pas de l’élément Expires facultatif dans le `CreateSequence` message ou, dans les cas lorsque le `CreateSequence` message contient un `Offer` élément, le paramètre facultatif `Expires` élément dans le `Offer` élément.  
  
-   B1102 : Lors de l’accès à la `CreateSequence` d’un message, WCF`Responder` envoie et reçoit les deux `Expires` éléments si elles existent, mais n’utilisent pas leurs valeurs.  
  
 La messagerie WS-Reliable introduit le mécanisme `Offer` pour établir deux séquences corrélées réciproques qui forment une session.  
  
-   R1103 : si `CreateSequence` contient un élément `Offer`, le répondeur de messagerie fiable doit soit accepter la séquence et répondre avec `CreateSequenceResponse` contenant un élément `wsrm:Accept`, formant deux séquences réciproques corrélées, soit rejeter la demande `CreateSequence`.  
  
-   R1104 : l'`SequenceAcknowledgement` et les messages d'application qui passent sur la séquence réciproque doivent être envoyés à la référence de point de terminaison `ReplyTo` de `CreateSequence`.  
  
-   R1105 : les références de point de terminaison `AcksTo` et `ReplyTo` dans `CreateSequence` doivent avoir des valeurs d'adresse qui correspondent au niveau des octets.  
  
     Le répondeur WCF vérifie que la partie de l’URI de la `AcksTo` et `ReplyTo` EPR est identiques avant de créer une séquence.  
  
-   R1106 : les références de point de terminaison `AcksTo` et `ReplyTo` dans `CreateSequence` doivent avoir le même jeu de paramètres de référence.  
  
     WCF n’applique pas, mais part du principe que [paramètres de référence] de `AcksTo` et `ReplyTo` sur `CreateSequence` sont identiques et utilise [paramètres de référence] à partir de `ReplyTo` référence de point de terminaison pour les accusés de réception et les messages de séquence inverse.  
  
-   R1107 : lorsque deux séquences réciproques sont établies à l'aide du mécanisme `Offer`, l'`SequenceAcknowledgement` et les messages d'application qui traversent les séquences réciproques doivent être envoyés à la référence de point de terminaison `ReplyTo` de `CreateSequence`.  
  
-   R1108 : lorsque deux séquences réciproques sont établies à l'aide du mécanisme Offer, la propriété `[address]` de l'élément enfant `wsrm:AcksTo` de la référence de point de terminaison de l'élément `wsrm:Accept` de la `CreateSequenceResponse` doit correspondre octet par octet à l'URI de destination de `CreateSequence`.  
  
-   R1109 : lorsque deux séquences réciproques sont établies à l'aide du mécanisme `Offer`, les messages envoyés par l'initiateur et les accusés de réception des messages envoyés par le répondeur doivent être envoyés à la même référence de point de terminaison.  
  
     WCF utilise la messagerie WS-Reliable pour établir des sessions fiables entre l’initiateur et le répondeur. Implémentation de la messagerie WS-Reliable de WCF fournit une session fiable pour, demande-réponse et unidirectionnels intégral duplex modèles de messagerie. La messagerie WS-Reliable `Offer` mécanisme sur `CreateSequence` / `CreateSequenceResponse` vous permet d’établir deux séquences réciproques corrélées et fournit un protocole de session qui convient à tous les points de terminaison de message. Étant donné que WCF fournit une garantie de sécurité pour une telle session, y compris la protection de bout en bout pour l’intégrité de session, il est pratique vérifier les messages destinés au même correspondant arrivent à la même destination. Cela permet également la superposition des accusés de réception de séquence sur les messages d'application. Par conséquent, les contraintes R1104, R1105 et R1108 s’appliquent à WCF.  
  
 Exemple de message `CreateSequence`.  
  
```xml  
<s:Envelope>  
  <s:Header>  
    <a:Action s:mustUnderstand="1">  
      http://schemas.xmlsoap.org/ws/2005/02/rm/CreateSequence  
    </a:Action>  
    <a:ReplyTo>  
      <a:Address>          
         http://Business456.com/clientA        
      </a:Address>  
    </a:ReplyTo>  
    <a:MessageID>  
      urn:uuid:addabbbf-60cb-44d3-8c5b-9e0841629a36  
    </a:MessageID>  
    <a:To s:mustUnderstand="1">  
      http://Business456.com/clientA  
    </a:To>  
  </s:Header>  
  <s:Body>  
    <wsrm:CreateSequence>  
      <wsrm:AcksTo>  
       <wsa:Address>  
         http://Business456.com/clientA  
       </wsa:Address>  
     </wsrm:AcksTo>  
     <wsrm:Offer>  
      <wsrm:Identifier>  
        urn:uuid:0afb8d36-bf26-4776-b8cf-8c91fddb5496  
      </wsrm:Identifier>  
     </wsrm:Offer>  
   </wsrm:CreateSequence>  
  </s:Body>  
</s:Envelope>  
```  
  
 Exemple de message `CreateSequenceResponse`.  
  
```xml  
<s:Envelope>  
  <s:Header>  
    <a:Action s:mustUnderstand="1">  
      http://schemas.xmlsoap.org/ws/2005/02/rm/CreateSequenceResponse  
    </a:Action>  
    <a:RelatesTo>  
      urn:uuid:addabbbf-60cb-44d3-8c5b-9e0841629a36  
    </a:RelatesTo>  
    <a:To s:mustUnderstand="1">  
      http://Business456.com/clientA  
    </a:To>  
  </s:Header>  
  <s:Body>  
   <wsrm:CreateSequenceResponse>  
    <Identifier>  
     urn:uuid:eea0a36c-b38a-43e8-8c76-2fabe2d76386  
    </Identifier>  
    <Accept>  
    <AcksTo>  
      <a:Address>  
        http://BusinessABC.com/serviceA  
      </a:Address>  
    </AcksTo>  
    </Accept>  
   </wsrm:CreateSequenceResponse>  
  </s:Body>  
</s:Envelope>  
```  
  
### <a name="sequence"></a>Séquence  
 Voici une liste des contraintes qui s'appliquent aux séquences :  
  
-   B1201:WCF génère et ne dépassant pas de numéros de séquence accède à `xs:long`de valeur inclusive maximale, 9223372036854775807.  
  
-   B1202:WCF génère toujours un vide dernier message avec l’URI d’action de http://schemas.xmlsoap.org/ws/2005/02/rm/LastMessage.  
  
-   B1203 : WCF reçoit et remet un message avec un en-tête de séquence qui contient un `LastMessage` élément tant que l’URI action n’est pas http://schemas.xmlsoap.org/ws/2005/02/rm/LastMessage.  
  
 Exemple d'en-tête Sequence.  
  
```xml  
<wsrm:Sequence>  
  <wsrm:Identifier>  
    urn:uuid:addabbbf-60cb-44d3-8c5b-9e0841629a36  
  </wsrm:Identifier>  
  <wsrm:MessageNumber>  
    10  
  </wsrm:MessageNumber>  
  <wsrm:LastMessage/>  
 </wsrm:Sequence>  
```  
  
### <a name="ackrequested-header"></a>En-tête AckRequested  
 WCF utilise `AckRequested` en-tête comme un mécanisme de persistance. WCF ne génère pas le paramètre facultatif `MessageNumber` élément. Lorsqu’il reçoit un message avec un `AckRequested` en-tête qui contient le `MessageNumber` élément, WCF ignore le `MessageNumber` valeur de l’élément, comme indiqué dans l’exemple suivant.  
  
```xml  
<wsrm:AckRequested>  
  <wsrm:Identifier>  
    urn:uuid:addabbbf-60cb-44d3-8c5b-9e0841629a36  
  </wsrm:Identifier>  
</wsrm:AckRequested>  
```  
  
### <a name="sequenceacknowledgement-header"></a>En-tête SequenceAcknowledgement  
 WCF utilise le mécanisme de superposition des accusés de réception de séquence fournis dans la messagerie WS-Reliable.  
  
-   R1401 : lorsque deux séquences réciproques sont établies à l'aide du mécanisme `Offer`, l'en-tête `SequenceAcknowledgement` peut être inclus dans tout message d'application transmis au destinataire souhaité.  
  
-   B1402 : Lorsque WCF doit générer un accusé de réception avant de recevoir un message de séquence (par exemple, pour répondre à une `AckRequested` message), WCF génère une `SequenceAcknowledgement` en-tête qui contient la plage 0-0, comme indiqué dans l’exemple suivant.  
  
    ```xml  
    <wsrm:SequenceAcknowledgement>  
      <wsrm:Identifier>  
        urn:uuid:addabbbf-60cb-44d3-8c5b-9e0841629a36  
      </wsrm:Identifier>  
      <wsrm:AcknowledgementRange Upper="0" Lower="0"/>  
    </wsrm:SequenceAcknowledgement>  
    ```  
  
-   B1403 : WCF ne génère pas `SequenceAcknowledgement` en-têtes qui contiennent un `Nack` élément mais prend en charge `Nack` éléments.  
  
### <a name="ws-reliablemessaging-faults"></a>Erreurs de la messagerie WS-Reliable  
 Voici une liste de contraintes qui s’appliquent à l’implémentation de WCF d’erreurs de la messagerie WS-Reliable :  
  
-   B1501 : WCF ne génère pas `MessageNumberRollover` erreurs.  
  
-   Peut générer un point de terminaison B1502:WCF `CreateSequenceRefused` comme décrit dans la spécification des erreurs.  
  
-   B1503:when le point de terminaison de service atteint sa limite de connexions et ne peut pas traiter de nouvelles connexions, WCF génère un autre `CreateSequenceRefused` sous-code, d’erreur `netrm:ConnectionLimitReached`, comme illustré dans l’exemple suivant.  
  
    ```xml  
    <s:Envelope>  
      <s:Header>  
        <wsa:Action>  
          http://schemas.xmlsoap.org/ws/2005/08/addressing/fault  
        </wsa:Action>  
      </s:Header>  
      <s:Body>  
        <s:Fault>  
          <s:Code>  
            <s:Value>  
              s:Receiver  
            </s:Value>  
            <s:Subcode>  
              <s:Value>  
                wsrm:CreateSequenceRefused  
              </s:Value>  
              <s:Subcode>  
                <s:Value>  
                  netrm:ConnectionLimitReached  
                </s:Value>  
              </s:Subcode>  
            </s:Subcode>  
          </s:Code>  
          <s:Reason>  
            <s:Text xml:lang="en">  
              [Reason]  
            </s:Text>  
          </s:Reason>  
        </s:Fault>  
      </s:Body>  
    </s:Envelope>  
    ```  
  
### <a name="ws-addressing-faults"></a>Erreurs WS-Addressing  
 Étant donné que la messagerie WS-Reliable utilise WS-Addressing, implémentation de la messagerie WS-Reliable WCF peut générer des erreurs WS-Addressing. Cette section décrit les erreurs de WS-Addressing WCF génère explicitement au niveau de la couche de messagerie WS-Reliable :  
  
-   B1601:WCF génère l’erreur d’en-tête de Message Addressing requis lorsqu’une des conditions suivantes est vraie :  
  
    -   Un message n'a pas d'en-tête `Sequence` ni d'en-tête `Action`.  
  
    -   Un message `CreateSequence` n'a pas d'en-tête `MessageId`.  
  
    -   Un message `CreateSequence` n'a pas d'en-tête `ReplyTo`.  
  
-   B1602:WCF génère l’erreur pas pris en charge par Action en réponse à un message qui est manquant, un `Sequence` en-tête et a une `Action` en-tête n’est pas reconnu dans la spécification WS-Reliable Messaging.  
  
-   B1603:WCF génère l’erreur de point de terminaison non disponible pour indiquer que le point de terminaison ne traite pas la séquence suite basée l’examen de la `CreateSequence` en-têtes d’adressage du message.  
  
## <a name="protocol-composition"></a>Composition du protocole  
  
### <a name="composition-with-ws-addressing"></a>Composition avec WS-Addressing  
 WCF prend en charge deux versions de WS-Addressing : WS-Addressing 2004/08 [WS-ADDR] et W3C WS-Addressing 1.0 Recommendations [WS-ADDR-CORE] et [WS-ADDR-SOAP].  
  
 Bien que la spécification de la messagerie WS-Reliable mentionne WS-Addressing 2004/08 uniquement, cela ne constitue pas une restriction en ce qui concerne la version WS-Addressing à utiliser. Voici une liste de contraintes qui s’appliquent à WCF :  
  
-   R2101 : les deux WS-Addressing 2004/08 et WS-Addressing 1.0 peuvent être utilisé avec la messagerie WS-Reliable.  
  
-   R2102:A une seule version de WS-Addressing doit être utilisée dans une séquence WS-Reliable Messaging donnée ou une paire de séquences réciproques corrélées à l’aide de la `wsrm:Offer` mécanisme.  
  
### <a name="composition-with-soap"></a>Composition avec SOAP  
 WCF prend en charge l’utilisation de SOAP 1.1 et SOAP 1.2 avec la messagerie WS-Reliable.  
  
### <a name="composition-with-ws-security-and-ws-secureconversation"></a>Composition avec WS-Security et WS-SecureConversation  
 WCF offre une protection pour les séquences de messagerie WS-Reliable à l’aide du Transport (HTTPS) sécurisée, la composition avec WS-Security et composition avec WS-Secure Conversation. Voici une liste de contraintes qui s’appliquent à WCF :  
  
-   R2301 : pour protéger l’intégrité d’une séquence WS-ReliableMessaging en plus de l’intégrité et la confidentialité des messages individuels, WCF requiert que WS-Secure Conversation doit être utilisée.  
  
-   R2302:AWS-session de Secure Conversation doit être établie avant d’établir des séquences de messagerie WS-Reliable.  
  
-   R2303 : si la durée de vie de la séquence de messagerie WS-Reliable dépasse celle de la session WS-Secure Conversation, le `SecurityContextToken` établi à l'aide de WS-Secure Conversation doit être renouvelé par le biais de la liaison WS-Secure Conversation Renewal correspondante.  
  
-   B2304:ws-séquence de messagerie fiable ou une paire de séquences réciproques corrélées sont toujours liées à une seule session WS-SecureConversation.  
  
     La source WCF génère le `wsse:SecurityTokenReference` élément dans la section d’extensibilité d’élément de la `CreateSequence` message.  
  
-   R2305:when composé avec WS-Secure Conversation, un `CreateSequence` message doit contenir la `wsse:SecurityTokenReference` élément.  
  
## <a name="ws-reliable-messaging-ws-policy-assertion"></a>Assertion WS-Policy de la messagerie WS-Reliable  
 WCF utilise l’Assertion WS-Policy de la messagerie WS-Reliable `wsrm:RMAssertion` pour décrire les capacités de points de terminaison. Voici une liste de contraintes qui s’appliquent à WCF :  
  
-   B3001 : WCF associe `wsrm:RMAssertion` Assertion WS-Policy pour `wsdl:binding` éléments. WCF prend en charge des pièces jointes aux `wsdl:binding` et `wsdl:port` éléments.  
  
-   B3002 : WCF prend en charge les propriétés facultatives suivantes d’assertion de messagerie WS-Reliable et assure leur contrôle sur WCF`ReliableMessagingBindingElement`:  
  
    -   `wsrm:InactivityTimeout`  
  
    -   `wsrm:AcknowledgementInterval`  
  
     Voici un exemple.  
  
    ```xml  
    <wsrm:RMAssertion>  
      <wsrm:InactivityTimeout Milliseconds="600000" />  
      <wsrm:AcknowledgementInterval Milliseconds="200" />  
    </wsrm:RMAssertion>  
    ```  
  
## <a name="flow-control-ws-reliable-messaging-extension"></a>Extension de messagerie WS-Reliable pour le contrôle de flux  
 WCF utilise extensibilité de la messagerie WS-Reliable pour renforcer le contrôle facultatif sur le flux de message de séquence.  
  
 Contrôle de flux est activé en définissant le `ReliableSessionBindingElement`de `FlowControlEnabled``bool` propriété `true`. Voici une liste de contraintes qui s’appliquent à WCF :  
  
-   B4001 : Lorsque le contrôle de flux de messagerie fiable est activée, WCF génère une `netrm:BufferRemaining` élément dans l’élément d’extensibilité de la `SequenceAcknowledgement` en-tête.  
  
-   B4002 : Lorsque le contrôle de flux de messagerie fiable est activée, WCF ne requiert pas qu’un `netrm:BufferRemaining` élément soit présent dans `SequenceAcknowledgement` en-tête, comme indiqué dans l’exemple suivant.  
  
    ```xml  
    <wsrm:SequenceAcknowledgement>  
      <wsrm:Identifier>  
        http://fabrikam123.com/abc  
      </wsrm:Identifier>  
      <wsrm:AcknowledgementRange Upper="1" Lower="1"/>             
      <netrm:BufferRemaining>  
        8  
      </netrm:BufferRemaining>  
    </wsrm:SequenceAcknowledgement>  
    ```  
  
-   B4003 : WCF utilise `netrm:BufferRemaining` pour indiquer combien de nouveaux messages la Destination de messagerie fiable peut mettre en mémoire tampon.  
  
-   B4004 : le Service de messagerie fiable WCF limite le nombre de messages transmis lorsque l’application de destination de messagerie fiable ne peut pas recevoir des messages rapidement. La destination de la messagerie fiable met en mémoire tampon les messages et la valeur de l’élément tombe à 0.  
  
-   B4005 : WCF génère `netrm:BufferRemaining` entier de valeurs comprises entre 0 et 4096 inclus et lit les valeurs de nombre entier compris entre 0 et `xs:int`de `maxInclusive` valeur 214748364 inclus.  
  
## <a name="message-exchange-patterns"></a>Modèles d’échange de messages  
 Cette section décrit le comportement de WCF lors de la messagerie WS-Reliable est utilisée pour différents modèles d’échange de Message. Pour chaque modèle d’échange de messages, les deux scénarios de déploiements suivants sont considérés :  
  
-   Initiateur non adressable : l'initiateur est derrière un pare-feu ; le répondeur peut remettre des messages à celui-ci uniquement sur les réponses HTTP.  
  
-   Initiateur adressable : l'initiateur et le répondeur peuvent tous les deux recevoir des requêtes HTTP ; en d'autres termes, deux connexions HTTP réciproques peuvent être établies.  
  
### <a name="one-way-non-addressable-initiator"></a>Initiateur unidirectionnel, non adressable  
  
#### <a name="binding"></a>Liaison  
 WCF fournit un modèle d’échange de messages unidirectionnels à l’aide d’une séquence sur un canal HTTP. WCF utilise les requêtes HTTP pour transmettre les messages à partir du RMS au RMD et la réponse HTTP pour transmettre les messages du RMD au RMS.  
  
#### <a name="createsequence-exchange"></a>Échange CreateSequence  
 L’initiateur WCF génère une `CreateSequence` message sans offre. Le répondeur de WCF garantit la `CreateSequence` n’a aucune offre avant de créer une séquence. Le répondeur WCF répond à la `CreateSequence` demande avec un `CreateSequenceResponse` message.  
  
#### <a name="sequenceacknowledgement"></a>SequenceAcknowledgement  
 L’initiateur WCF traite les accusés de réception de la réponse de tous les messages sauf le `CreateSequence` message et les messages d’erreur. Le répondeur WCF génère toujours un accusé de réception autonome dans la réponse pour les deux séquences et `AckRequested` messages.  
  
#### <a name="terminatesequence-message"></a>Message TerminateSequence  
 WCF traite `TerminateSequence` comme une opération unidirectionnelle, ce qui signifie que la réponse HTTP a un corps vide et le code d’état HTTP 202.  
  
### <a name="one-way-addressable-initiator"></a>Initiateur unidirectionnel, adressable  
  
#### <a name="binding"></a>Liaison  
 WCF fournit un modèle d’échange de messages unidirectionnels à l’aide d’une séquence sur entrante et un canal Http sortant. WCF utilise les requêtes HTTP pour transmettre les messages. Toutes les réponses HTTP ont un corps vide et le code d'état HTTP 202.  
  
#### <a name="createsequence-exchange"></a>Échange CreateSequence  
 L’initiateur WCF génère une `CreateSequence` message sans offre. Le répondeur de WCF garantit que le `CreateSequence` n’a aucune offre avant de créer une séquence. Le répondeur WCF transmet le `CreateSequenceResponse` message sur une requête HTTP adressée avec la `ReplyTo` référence de point de terminaison.  
  
### <a name="duplex-addressable-initiator"></a>Initiateur duplex, adressable  
  
#### <a name="binding"></a>Liaison  
 WCF fournit un modèle d’échange de messages asynchrone complet, bidirectionnel utilise deux séquences sur un canal entrant et sortant HTTP. WCF utilise les requêtes HTTP pour transmettre les messages. Toutes les réponses HTTP ont un corps vide et le code d'état HTTP 202.  
  
#### <a name="createsequence-exchange"></a>Échange CreateSequence  
 L’initiateur WCF génère une `CreateSequence` message avec une offre. Le répondeur de WCF garantit que le `CreateSequence` a une offre avant de créer une séquence. WCF envoie le `CreateSequenceResponse` sur la requête HTTP adressée à la `CreateSequence`de `ReplyTo` référence de point de terminaison.  
  
#### <a name="sequence-lifetime"></a>Durée de vie de séquence  
 WCF traite les deux séquences comme une session duplex complète.  
  
 Générer une erreur qui fait échouer une séquence, WCF attend le point de terminaison distant pour les deux séquences d’erreur. Lors de la lecture d’une erreur qui fait échouer une séquence, WCF fait échouer les deux séquences.  
  
 WCF peut fermer sa séquence sortante et continuer à traiter les messages sur sa séquence entrante. À l’inverse, WCF peut traiter la fermeture de la séquence entrante et continuer à envoyer des messages sur sa séquence sortante.  
  
### <a name="request-reply-non-addressable-initiator"></a>Initiateur demande-réponse, non adressable  
  
#### <a name="binding"></a>Liaison  
 WCF fournit unidirectionnel et modèle d’échange de messages demande-réponse à l’aide de deux séquences sur un canal HTTP. WCF utilise les requêtes HTTP pour transmettre les messages de la séquence de demande et les réponses HTTP pour transmettre des messages de la séquence de réponse.  
  
#### <a name="createsequence-exchange"></a>Échange CreateSequence  
 L’initiateur WCF génère une `CreateSequence` message avec une offre. Le répondeur de WCF garantit que le `CreateSequence` a une offre avant de créer une séquence. Le répondeur WCF répond à la `CreateSequence` demande avec un `CreateSequenceResponse` message.  
  
#### <a name="one-way-message"></a>Message unidirectionnel  
 Pour terminer avec succès à un protocole d’échange de messages unidirectionnels, l’initiateur de WCF transmet un message de séquence de demande sur la requête HTTP et reçoit un autonome `SequenceAcknowledgement` message dans la réponse HTTP. `SequenceAcknowledgement` doit accepter le message transmis.  
  
 Le répondeur WCF peut répondre à la demande avec un accusé de réception, une erreur ou une réponse avec un corps vide et le code d’état HTTP 202.  
  
#### <a name="two-way-messages"></a>Messages bidirectionnels  
 Pour effectuer un protocole d’échange de messages bidirectionnel avec succès, l’initiateur de WCF transmet un message de séquence de demande sur la requête HTTP et reçoit un message de séquence de réponse sur la réponse HTTP. La réponse doit contenir un `SequenceAcknowledgement` qui accuse réception du message de séquence de demande transmis.  
  
 Le répondeur WCF peut répondre à la demande avec une réponse d’application, une erreur ou une réponse avec un corps vide et le code d’état HTTP 202.  
  
 En raison de la présence de messages unidirectionnels et du délai d'attente des réponses d'application, le numéro de séquence du message de séquence de demande et le numéro de séquence du message de réponse n'ont aucune corrélation.  
  
#### <a name="retrying-replies"></a>Nouvelles tentatives de réponses  
 WCF s’appuie sur la corrélation demande-réponse HTTP pour la corrélation protocole d’échange de messages bidirectionnel. Pour cette raison, l’initiateur WCF n’arrête pas une nouvelle tentative d’un message de séquence de demande lorsque le message de séquence de demande est accepté, mais lors de la réponse HTTP contient un accusé de réception, un message de l’utilisateur ou une erreur. Le répondeur WCF réessaie des réponses sur le tronçon de requête HTTP de la demande à laquelle la réponse est corrélée.  
  
#### <a name="lastmessage-exchange"></a>Échange LastMessage  
 L’initiateur WCF génère et transmet un dernier message vide sur le tronçon de requête HTTP. WCF requiert une réponse, mais il ignore le message de réponse réel. Le répondeur WCF répond à vide dernier message de la séquence demande avec le dernier message de la séquence de réponse vide.  
  
 Si le répondeur WCF reçoit un dernier message dans lequel l’URI action n’est pas http://schemas.xmlsoap.org/ws/2005/02/rm/LastMessage, les réponses WCF avec un dernier message. Dans le cas d'un protocole d'échange de messages bidirectionnel, le dernier message contient le message d'application ; dans le cas d'un protocole d'échange de messages unidirectionnel, le dernier message est vide.  
  
 Le répondeur WCF ne requiert pas d’accusé de réception pour le dernier message de la séquence de réponse vide.  
  
#### <a name="terminatesequence-exchange"></a>Échange TerminateSequence  
 Lorsque toutes les demandes ont reçu une réponse valide, l’initiateur WCF génère et transmet la séquence de demande `TerminateSequence` message sur le tronçon de requête HTTP. WCF requiert une réponse, mais il ignore le message de réponse réel. Le répondeur WCF répond à la séquence de demande `TerminateSequence` message avec la séquence de réponse `TerminateSequence` message.  
  
 Dans une séquence d'arrêt normale, les deux messages `TerminateSequence` incluent un `SequenceAcknowledgement` complet.  
  
### <a name="requestreply-addressable-initiator"></a>Initiateur demande/réponse, adressable  
  
#### <a name="binding"></a>Liaison  
 WCF fournit un modèle d’échange de message demande-réponse à l’aide de deux séquences sur un entrant et un canal HTTP sortant. WCF utilise les requêtes HTTP pour transmettre les messages. Toutes les réponses HTTP ont un corps vide et le code d'état HTTP 202.  
  
#### <a name="createsequence-exchange"></a>Échange CreateSequence  
 L’initiateur WCF génère une `CreateSequence` message avec une offre. Le répondeur de WCF garantit que le `CreateSequence` a une offre avant de créer une séquence. WCF envoie le `CreateSequenceResponse` sur la requête HTTP adressée à la `CreateSequence`de `ReplyTo` référence de point de terminaison.  
  
#### <a name="requestreply-correlation"></a>Corrélation demande/réponse  
 L’initiateur de WCF garantit toutes les applications demande messages portent un `MessageId` et un `ReplyTo` référence de point de terminaison. L’initiateur WCF s’applique le `CreateSequence` du message `ReplyTo` référence de point de terminaison sur chaque message de demande d’application. Le répondeur WCF requiert cette demande entrante des messages portent un `MessageId` et un `ReplyTo`. Le répondeur de WCF garantit que les URI de la référence de point de terminaison de la `CreateSequence` et tous les messages de demande d’application sont identiques.
