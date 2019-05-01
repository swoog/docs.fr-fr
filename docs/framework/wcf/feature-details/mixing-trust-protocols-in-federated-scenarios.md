---
title: Combinaison de protocoles d'approbation dans les scénarios fédérés
ms.date: 03/30/2017
ms.assetid: d7b5fee9-2246-4b09-b8d7-9e63cb817279
ms.openlocfilehash: ce5c3a1875d84d98068dcc78d8346a88bc0b28f3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62046683"
---
# <a name="mixing-trust-protocols-in-federated-scenarios"></a><span data-ttu-id="3293a-102">Combinaison de protocoles d'approbation dans les scénarios fédérés</span><span class="sxs-lookup"><span data-stu-id="3293a-102">Mixing Trust Protocols in Federated Scenarios</span></span>
<span data-ttu-id="3293a-103">Il peut exister des scénarios où des clients fédérés communiquent avec un WSDL de service et un service de jeton de sécurité (STS) qui n'ont pas la même version d'approbation.</span><span class="sxs-lookup"><span data-stu-id="3293a-103">There may be scenarios in which federated clients communicate with a service and a Security Token Service (STS) that do not have the same trust version.</span></span> <span data-ttu-id="3293a-104">Le WSDL de service peut contenir une assertion `RequestSecurityTokenTemplate` avec les éléments WS-Trust qui sont de versions différentes par rapport à STS.</span><span class="sxs-lookup"><span data-stu-id="3293a-104">The service WSDL can contain a `RequestSecurityTokenTemplate` assertion with WS-Trust elements that are of different versions than the STS.</span></span> <span data-ttu-id="3293a-105">Dans ce cas, un client Windows Communication Foundation (WCF) convertit les éléments de WS-Trust reçus à partir de la `RequestSecurityTokenTemplate` pour faire correspondre le STS version d’approbation.</span><span class="sxs-lookup"><span data-stu-id="3293a-105">In such cases, a Windows Communication Foundation (WCF) client converts the WS-Trust elements received from the `RequestSecurityTokenTemplate` to match the STS trust version.</span></span> <span data-ttu-id="3293a-106">WCF gère les versions d’approbation qui ne correspondent pas uniquement pour les liaisons standards.</span><span class="sxs-lookup"><span data-stu-id="3293a-106">WCF handles mismatched trust versions only for standard bindings.</span></span> <span data-ttu-id="3293a-107">Tous les paramètres d’algorithme standard reconnus par WCF font partie de la liaison standard.</span><span class="sxs-lookup"><span data-stu-id="3293a-107">All standard algorithm parameters that are recognized by WCF are part of the standard binding.</span></span> <span data-ttu-id="3293a-108">Cette rubrique décrit le comportement WCF avec différents paramètres d’approbation entre le service et le STS.</span><span class="sxs-lookup"><span data-stu-id="3293a-108">This topic describes the WCF behavior with various trust settings between the service and the STS.</span></span>  
  
## <a name="rp-feb-2005-and-sts-feb-2005"></a><span data-ttu-id="3293a-109">RP février 2005 et STS février 2005</span><span class="sxs-lookup"><span data-stu-id="3293a-109">RP Feb 2005 and STS Feb 2005</span></span>  
 <span data-ttu-id="3293a-110">Le WSDL pour la partie de confiance (RP) contient les éléments suivants dans la section `RequestSecurityTokenTemplate` :</span><span class="sxs-lookup"><span data-stu-id="3293a-110">The WSDL for Relying Party (RP) contains the following elements within the `RequestSecurityTokenTemplate` section:</span></span>  
  
- `CanonicalizationAlgorithm`  
  
- `EncryptionAlgorithm`  
  
- `EncryptWith`  
  
- `SignWith`  
  
- `KeySize`  
  
- `KeyType`  
  
 <span data-ttu-id="3293a-111">Le fichier de configuration client contient une liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="3293a-111">The client configuration file contains a list of parameters.</span></span>  
  
 <span data-ttu-id="3293a-112">WCF ne peut pas différencier les paramètres client et le service ; Il ajoute tous les paramètres et les envoie dans le `RequestSecurityTokenTemplate` (RST).</span><span class="sxs-lookup"><span data-stu-id="3293a-112">WCF cannot differentiate between the client and service parameters; it adds all the parameters and sends them in the `RequestSecurityTokenTemplate` (RST).</span></span>  
  
## <a name="rp-trust-13-and-sts-trust-13"></a><span data-ttu-id="3293a-113">Version d'approbation RP 1.3 et Version d'approbation STS 1.3</span><span class="sxs-lookup"><span data-stu-id="3293a-113">RP Trust 1.3 and STS Trust 1.3</span></span>  
 <span data-ttu-id="3293a-114">Le WSDL pour la partie de confiance (RP) contient les éléments suivants dans la section `RequestSecurityTokenTemplate` :</span><span class="sxs-lookup"><span data-stu-id="3293a-114">The WSDL for RP contains the following elements within the `RequestSecurityTokenTemplate` section:</span></span>  
  
- `CanonicalizationAlgorithm`  
  
- `EncryptionAlgorithm`  
  
- `EncryptWith`  
  
- `SignWith`  
  
- `KeySize`  
  
- `KeyType`  
  
- `KeyWrapAlgorithm`  
  
 <span data-ttu-id="3293a-115">Le fichier de configuration client contient un élément `secondaryParameters` qui encapsule les paramètres spécifié par la partie de confiance.</span><span class="sxs-lookup"><span data-stu-id="3293a-115">The client configuration file contains a `secondaryParameters` element that wraps the parameters specified by the RP.</span></span>  
  
 <span data-ttu-id="3293a-116">WCF supprime le `EncryptionAlgorithm`, `CanonicalizationAlgorithm` et `KeyWrapAlgorithm` éléments à partir de l’élément de niveau supérieur sous le RST si ceux-ci sont présents dans le `SecondaryParameters` élément.</span><span class="sxs-lookup"><span data-stu-id="3293a-116">WCF removes the `EncryptionAlgorithm`, `CanonicalizationAlgorithm` and `KeyWrapAlgorithm` elements from the top-level element under the RST if these are present inside the `SecondaryParameters` element.</span></span> <span data-ttu-id="3293a-117">WCF ajoute la `SecondaryParameters` élément au RST sortant non modifié.</span><span class="sxs-lookup"><span data-stu-id="3293a-117">WCF appends the `SecondaryParameters` element to the outgoing RST unmodified.</span></span>  
  
## <a name="rp-trust-feb-2005-and-sts-trust-13"></a><span data-ttu-id="3293a-118">Version d'approbation RP février 2005 et Version d'approbation STS 1.3</span><span class="sxs-lookup"><span data-stu-id="3293a-118">RP Trust Feb 2005 and STS Trust 1.3</span></span>  
 <span data-ttu-id="3293a-119">Le WSDL pour la partie de confiance (RP) contient les éléments suivants dans la section `RequestSecurityTokenTemplate` :</span><span class="sxs-lookup"><span data-stu-id="3293a-119">The WSDL for RP contains the following elements in the `RequestSecurityTokenTemplate` section:</span></span>  
  
- `CanonicalizationAlgorithm`  
  
- `EncryptionAlgorithm`  
  
- `EncryptWith`  
  
- `SignWith`  
  
- `KeySize`  
  
- `KeyType`  
  
 <span data-ttu-id="3293a-120">Le fichier de configuration client contient une liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="3293a-120">The client configuration file contains a list of parameters.</span></span>  
  
 <span data-ttu-id="3293a-121">À partir du fichier de configuration client, WCF ne peut pas faire la différence entre les paramètres de service et client.</span><span class="sxs-lookup"><span data-stu-id="3293a-121">From the client configuration file, WCF cannot differentiate between the service and client parameters.</span></span> <span data-ttu-id="3293a-122">Par conséquent, WCF convertit tous les paramètres à un espace de noms de version 1.3 de confiance.</span><span class="sxs-lookup"><span data-stu-id="3293a-122">Therefore WCF converts all the parameters to a Trust version 1.3 namespace.</span></span>  
  
 <span data-ttu-id="3293a-123">WCF gère le `KeyType`, `KeySize`, et `TokenType` éléments comme suit :</span><span class="sxs-lookup"><span data-stu-id="3293a-123">WCF handles the `KeyType`, `KeySize`, and `TokenType` elements as follows:</span></span>  
  
- <span data-ttu-id="3293a-124">Téléchargez le WSDL, créez la liaison et assignez `KeyType`, `KeySize` et `TokenType` à partir des paramètres RP.</span><span class="sxs-lookup"><span data-stu-id="3293a-124">Download the WSDL, create the binding, and assign `KeyType`, `KeySize`, and `TokenType` from the RP parameters.</span></span> <span data-ttu-id="3293a-125">Le fichier de configuration client est alors généré.</span><span class="sxs-lookup"><span data-stu-id="3293a-125">The client configuration file is then generated.</span></span>  
  
- <span data-ttu-id="3293a-126">Le client peut maintenant modifier tout paramètre dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="3293a-126">The client can now change any parameter in the configuration file.</span></span>  
  
- <span data-ttu-id="3293a-127">Pendant l’exécution, WCF copie tous les paramètres spécifiés dans le `AdditionalTokenParameters` section du fichier de configuration client sauf `KeyType`, `KeySize` et `TokenType`, car ces paramètres sont pris en compte pendant le fichier de configuration génération.</span><span class="sxs-lookup"><span data-stu-id="3293a-127">During runtime, WCF copies all parameters specified into the `AdditionalTokenParameters` section of the client configuration file except `KeyType`, `KeySize` and `TokenType`, because these parameters are accounted for during the configuration file generation.</span></span>  
  
## <a name="rp-trust-13-and-sts-trust-feb-2005"></a><span data-ttu-id="3293a-128">Version d'approbation RP 1.3 et Version d'approbation STS février 2005</span><span class="sxs-lookup"><span data-stu-id="3293a-128">RP Trust 1.3 and STS Trust Feb 2005</span></span>  
 <span data-ttu-id="3293a-129">Le WSDL pour la partie de confiance (RP) contient les éléments suivants dans la section `RequestSecurityTokenTemplate` :</span><span class="sxs-lookup"><span data-stu-id="3293a-129">The WSDL for RP contains the following elements in the `RequestSecurityTokenTemplate` section:</span></span>  
  
- `CanonicalizationAlgorithm`  
  
- `EncryptionAlgorithm`  
  
- `EncryptWith`  
  
- `SignWith`  
  
- `KeySize`  
  
- `KeyType`  
  
- `KeyWrapAlgorithm`  
  
 <span data-ttu-id="3293a-130">Le fichier de configuration client contient un élément `secondaryParamters` qui encapsule les paramètres spécifié par la partie de confiance.</span><span class="sxs-lookup"><span data-stu-id="3293a-130">The client configuration file contains a `secondaryParamters` element that wraps the parameters specified by the RP.</span></span>  
  
 <span data-ttu-id="3293a-131">WCF copie tous les paramètres spécifiés dans la `SecondaryParameters` section à l’élément RST de niveau supérieur, mais ne les convertit ne pas l’espace de noms WS-Trust 2005.</span><span class="sxs-lookup"><span data-stu-id="3293a-131">WCF copies all the parameters specified within the `SecondaryParameters` section to the top-level RST element, but does not convert them to the 2005 WS-Trust namespace.</span></span>
