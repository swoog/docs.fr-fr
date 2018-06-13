---
title: SecurityBindingElement
ms.date: 03/30/2017
ms.assetid: ef93b6e6-3524-48a8-94d3-c8837f1872f9
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: ceb674ea7c20386acb821d3a41c1ad0c743a7607
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33487553"
---
# <a name="securitybindingelement"></a><span data-ttu-id="97a0d-102">SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="97a0d-102">SecurityBindingElement</span></span>
<span data-ttu-id="97a0d-103">SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="97a0d-103">SecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="97a0d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97a0d-104">Syntax</span></span>  
  
```  
class SecurityBindingElement : BindingElement  
{  
  string DefaultAlgorithmSuite;  
  boolean IncludeTimestamp;  
  string KeyEntropyMode;  
  LocalServiceSecuritySettings LocalServiceSecuritySettings;  
  string MessageSecurityVersion;  
  string SecurityHeaderLayout;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="97a0d-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="97a0d-105">Methods</span></span>  
 <span data-ttu-id="97a0d-106">La classe SecurityBindingElement ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="97a0d-106">The SecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="97a0d-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="97a0d-107">Properties</span></span>  
 <span data-ttu-id="97a0d-108">La classe SecurityBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="97a0d-108">The SecurityBindingElement class has the following properties:</span></span>  
  
### <a name="defaultalgorithmsuite"></a><span data-ttu-id="97a0d-109">DefaultAlgorithmSuite</span><span class="sxs-lookup"><span data-stu-id="97a0d-109">DefaultAlgorithmSuite</span></span>  
 <span data-ttu-id="97a0d-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="97a0d-110">Data type: string</span></span>  
  
 <span data-ttu-id="97a0d-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="97a0d-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="97a0d-112">Spécifie les algorithmes à utiliser avec la liaison.</span><span class="sxs-lookup"><span data-stu-id="97a0d-112">Specifies the algorithms to use with the binding.</span></span>  
  
### <a name="includetimestamp"></a><span data-ttu-id="97a0d-113">IncludeTimestamp</span><span class="sxs-lookup"><span data-stu-id="97a0d-113">IncludeTimestamp</span></span>  
 <span data-ttu-id="97a0d-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="97a0d-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="97a0d-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="97a0d-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="97a0d-116">Valeur booléenne qui spécifie si chaque message contient un horodatage.</span><span class="sxs-lookup"><span data-stu-id="97a0d-116">A Boolean value that specifies whether each message contains a timestamp.</span></span>  
  
### <a name="keyentropymode"></a><span data-ttu-id="97a0d-117">KeyEntropyMode</span><span class="sxs-lookup"><span data-stu-id="97a0d-117">KeyEntropyMode</span></span>  
 <span data-ttu-id="97a0d-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="97a0d-118">Data type: string</span></span>  
  
 <span data-ttu-id="97a0d-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="97a0d-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="97a0d-120">Source d'entropie utilisée pour créer des clés.</span><span class="sxs-lookup"><span data-stu-id="97a0d-120">The source of entropy used to create keys.</span></span>  
  
### <a name="localservicesecuritysettings"></a><span data-ttu-id="97a0d-121">LocalServiceSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="97a0d-121">LocalServiceSecuritySettings</span></span>  
 <span data-ttu-id="97a0d-122">Type de données : LocalServiceSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="97a0d-122">Data type: LocalServiceSecuritySettings</span></span>  
  
 <span data-ttu-id="97a0d-123">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="97a0d-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="97a0d-124">Propriétés de sécurité spécifiques d'une liaison pour le service local.</span><span class="sxs-lookup"><span data-stu-id="97a0d-124">The binding specific security properties for the local service.</span></span>  
  
### <a name="messagesecurityversion"></a><span data-ttu-id="97a0d-125">MessageSecurityVersion</span><span class="sxs-lookup"><span data-stu-id="97a0d-125">MessageSecurityVersion</span></span>  
 <span data-ttu-id="97a0d-126">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="97a0d-126">Data type: string</span></span>  
  
 <span data-ttu-id="97a0d-127">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="97a0d-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="97a0d-128">Version utilisée pour la sécurité de message.</span><span class="sxs-lookup"><span data-stu-id="97a0d-128">The version used for message security.</span></span>  
  
### <a name="securityheaderlayout"></a><span data-ttu-id="97a0d-129">SecurityHeaderLayout</span><span class="sxs-lookup"><span data-stu-id="97a0d-129">SecurityHeaderLayout</span></span>  
 <span data-ttu-id="97a0d-130">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="97a0d-130">Data type: string</span></span>  
  
 <span data-ttu-id="97a0d-131">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="97a0d-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="97a0d-132">Ordre des éléments dans l'en-tête de sécurité pour cette liaison.</span><span class="sxs-lookup"><span data-stu-id="97a0d-132">The order of elements in the security header for this binding.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="97a0d-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="97a0d-133">Requirements</span></span>  
  
|<span data-ttu-id="97a0d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="97a0d-134">MOF</span></span>|<span data-ttu-id="97a0d-135">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="97a0d-135">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="97a0d-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="97a0d-136">Namespace</span></span>|<span data-ttu-id="97a0d-137">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="97a0d-137">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="97a0d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97a0d-138">See Also</span></span>  
 <xref:System.ServiceModel.Channels.SecurityBindingElement>
