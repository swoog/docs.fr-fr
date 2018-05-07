---
title: Combinaison de protocoles d'approbation dans les scénarios fédérés
ms.date: 03/30/2017
ms.assetid: d7b5fee9-2246-4b09-b8d7-9e63cb817279
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: bca23ba16c69c6d21ed7cf49aaebb8d2ed079f5e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="mixing-trust-protocols-in-federated-scenarios"></a>Combinaison de protocoles d'approbation dans les scénarios fédérés
Il peut exister des scénarios où des clients fédérés communiquent avec un WSDL de service et un service de jeton de sécurité (STS) qui n'ont pas la même version d'approbation. Le WSDL de service peut contenir une assertion `RequestSecurityTokenTemplate` avec les éléments WS-Trust qui sont de versions différentes par rapport à STS. Dans ce cas, un client Windows Communication Foundation (WCF) convertit les éléments de WS-Trust reçus à partir de la `RequestSecurityTokenTemplate` pour correspondre à STS version d’approbation. WCF gère les versions d’approbation ne correspondent pas uniquement pour les liaisons standards. Tous les paramètres d’algorithme standard reconnus par WCF font partie de la liaison standard. Cette rubrique décrit le comportement WCF avec différents paramètres d’approbation entre le service et le STS.  
  
## <a name="rp-feb-2005-and-sts-feb-2005"></a>RP février 2005 et STS février 2005  
 Le WSDL pour la partie de confiance (RP) contient les éléments suivants dans la section `RequestSecurityTokenTemplate` :  
  
-   `CanonicalizationAlgorithm`  
  
-   `EncryptionAlgorithm`  
  
-   `EncryptWith`  
  
-   `SignWith`  
  
-   `KeySize`  
  
-   `KeyType`  
  
 Le fichier de configuration client contient une liste de paramètres.  
  
 WCF ne peut pas différencier les paramètres client et le service ; Il ajoute tous les paramètres et les envoie dans le `RequestSecurityTokenTemplate` (RST).  
  
## <a name="rp-trust-13-and-sts-trust-13"></a>Version d'approbation RP 1.3 et Version d'approbation STS 1.3  
 Le WSDL pour la partie de confiance (RP) contient les éléments suivants dans la section `RequestSecurityTokenTemplate` :  
  
-   `CanonicalizationAlgorithm`  
  
-   `EncryptionAlgorithm`  
  
-   `EncryptWith`  
  
-   `SignWith`  
  
-   `KeySize`  
  
-   `KeyType`  
  
-   `KeyWrapAlgorithm`  
  
 Le fichier de configuration client contient un élément `secondaryParameters` qui encapsule les paramètres spécifié par la partie de confiance.  
  
 WCF supprime le `EncryptionAlgorithm`, `CanonicalizationAlgorithm` et `KeyWrapAlgorithm` éléments à partir de l’élément de niveau supérieur sous le RST si ceux-ci sont présents dans le `SecondaryParameters` élément. WCF ajoute la `SecondaryParameters` élément au RST sortant non modifié.  
  
## <a name="rp-trust-feb-2005-and-sts-trust-13"></a>Version d'approbation RP février 2005 et Version d'approbation STS 1.3  
 Le WSDL pour la partie de confiance (RP) contient les éléments suivants dans la section `RequestSecurityTokenTemplate` :  
  
-   `CanonicalizationAlgorithm`  
  
-   `EncryptionAlgorithm`  
  
-   `EncryptWith`  
  
-   `SignWith`  
  
-   `KeySize`  
  
-   `KeyType`  
  
 Le fichier de configuration client contient une liste de paramètres.  
  
 À partir du fichier de configuration client, WCF ne peut pas faire la différence entre les paramètres de service et le client. Par conséquent, WCF convertit tous les paramètres à un espace de noms de la version 1.3 de confiance.  
  
 WCF gère le `KeyType`, `KeySize`, et `TokenType` éléments comme suit :  
  
-   Téléchargez le WSDL, créez la liaison et assignez `KeyType`, `KeySize` et `TokenType` à partir des paramètres RP. Le fichier de configuration client est alors généré.  
  
-   Le client peut maintenant modifier tout paramètre dans le fichier de configuration.  
  
-   Pendant l’exécution, WCF copie tous les paramètres spécifiés dans le `AdditionalTokenParameters` section du fichier de configuration client sauf `KeyType`, `KeySize` et `TokenType`, car ces paramètres sont pris en compte pendant le fichier de configuration génération.  
  
## <a name="rp-trust-13-and-sts-trust-feb-2005"></a>Version d'approbation RP 1.3 et Version d'approbation STS février 2005  
 Le WSDL pour la partie de confiance (RP) contient les éléments suivants dans la section `RequestSecurityTokenTemplate` :  
  
-   `CanonicalizationAlgorithm`  
  
-   `EncryptionAlgorithm`  
  
-   `EncryptWith`  
  
-   `SignWith`  
  
-   `KeySize`  
  
-   `KeyType`  
  
-   `KeyWrapAlgorithm`  
  
 Le fichier de configuration client contient un élément `secondaryParamters` qui encapsule les paramètres spécifié par la partie de confiance.  
  
 WCF copie tous les paramètres spécifiés dans la `SecondaryParameters` section à l’élément RST de niveau supérieur, mais ne les convertit ne pas l’espace de noms WS-Trust 2005.
