---
title: IAppIdAuthority, interface
ms.date: 03/30/2017
api_name:
- IAppIdAuthority
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAppIdAuthority
helpviewer_keywords:
- IAppIdAuthority interface [.NET Framework fusion]
ms.assetid: ec354fa1-1efd-41b0-bc43-b90597b6e253
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c803169f87c4033d7e231e8b0243f502b9246f70
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54493922"
---
# <a name="iappidauthority-interface"></a><span data-ttu-id="8bcbc-102">IAppIdAuthority, interface</span><span class="sxs-lookup"><span data-stu-id="8bcbc-102">IAppIdAuthority Interface</span></span>
<span data-ttu-id="8bcbc-103">Fournit des méthodes qui génèrent et comparer les clés pour les identités d’application et les références.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-103">Provides methods that generate and compare keys for application identities and references.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8bcbc-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8bcbc-104">Methods</span></span>  
  
|<span data-ttu-id="8bcbc-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="8bcbc-105">Method</span></span>|<span data-ttu-id="8bcbc-106">Description</span><span class="sxs-lookup"><span data-stu-id="8bcbc-106">Description</span></span>|  
|------------|-----------------|  
|`IAppIdAuthority::AreDefinitionsEqual`|<span data-ttu-id="8bcbc-107">Obtient une valeur qui indique si les deux spécifié [IDefinitionAppId](../../../../docs/framework/unmanaged-api/fusion/idefinitionappid-interface.md) instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-107">Gets a value that indicates whether the two specified [IDefinitionAppId](../../../../docs/framework/unmanaged-api/fusion/idefinitionappid-interface.md) instances are equal.</span></span> <span data-ttu-id="8bcbc-108">Vous pouvez passer la valeur d’indicateur IAPPIDAUTHORITY_ARE_DEFINITIONS_EQUAL_FLAG_IGNORE_VERSION pour ignorer leurs informations de version respective.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-108">You can pass the flag value IAPPIDAUTHORITY_ARE_DEFINITIONS_EQUAL_FLAG_IGNORE_VERSION to ignore their respective version information.</span></span>|  
|`IAppIdAuthority::AreReferencesEqual`|<span data-ttu-id="8bcbc-109">Obtient une valeur qui indique si les deux spécifié [IReferenceAppId](../../../../docs/framework/unmanaged-api/fusion/ireferenceappid-interface.md) instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-109">Gets a value that indicates whether the two specified [IReferenceAppId](../../../../docs/framework/unmanaged-api/fusion/ireferenceappid-interface.md) instances are equal.</span></span> <span data-ttu-id="8bcbc-110">Vous pouvez passer la valeur d’indicateur IAPPIDAUTHORITY_ARE_REFERENCES_EQUAL_FLAG_IGNORE_VERSION pour ignorer leurs informations de version respective.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-110">You can pass the flag value IAPPIDAUTHORITY_ARE_REFERENCES_EQUAL_FLAG_IGNORE_VERSION to ignore their respective version information.</span></span>|  
|`IAppIdAuthority::AreTextualDefinitionsEqual`|<span data-ttu-id="8bcbc-111">Obtient une valeur qui indique si les deux définitions de chaîne spécifié sont égale.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-111">Gets a value that indicates whether the two specified string definitions are equal.</span></span> <span data-ttu-id="8bcbc-112">Vous pouvez passer la valeur d’indicateur IAPPIDAUTHORITY_ARE_DEFINITIONS_EQUAL_FLAG_IGNORE_VERSION pour ignorer leurs informations de version respective.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-112">You can pass the flag value IAPPIDAUTHORITY_ARE_DEFINITIONS_EQUAL_FLAG_IGNORE_VERSION to ignore their respective version information.</span></span>|  
|`IAppIdAuthority::AreTextualReferencesEqual`|<span data-ttu-id="8bcbc-113">Obtient une valeur qui indique si les deux références de chaîne spécifié sont égaux.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-113">Gets a value that indicates whether the two specified string references are equal.</span></span> <span data-ttu-id="8bcbc-114">Vous pouvez passer la valeur d’indicateur IAPPIDAUTHORITY_ARE_REFERENCES_EQUAL_FLAG_IGNORE_VERSION pour ignorer leurs informations de version respective.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-114">You can pass the flag value IAPPIDAUTHORITY_ARE_REFERENCES_EQUAL_FLAG_IGNORE_VERSION to ignore their respective version information.</span></span>|  
|`IAppIdAuthority::CreateDefinition`|<span data-ttu-id="8bcbc-115">Obtient un pointeur d’interface généré récemment `IDefinitionAppId` instance qui représente l’assembly dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-115">Gets an interface pointer to a newly generated `IDefinitionAppId` instance that represents the assembly in the current scope.</span></span>|  
|`IAppIdAuthority::CreateReference`|<span data-ttu-id="8bcbc-116">Obtient un pointeur d’interface nouvellement créé `IReferenceAppId` qui représente l’assembly dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-116">Gets an interface pointer to a newly created `IReferenceAppId` that represents the assembly in the current scope.</span></span>|  
|`IAppIdAuthority::DefinitionToText`|<span data-ttu-id="8bcbc-117">Obtient une version de chaîne de l’objet `IDefinitionAppId`, en utilisant les valeurs d’indicateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-117">Gets a string version of the specified `IDefinitionAppId`, using the specified flag values.</span></span>|  
|`IAppIdAuthority::DoesDefinitionMatchReference`|<span data-ttu-id="8bcbc-118">Obtient une valeur qui indique si le texte spécifié `IDefinitionAppId` et `IReferenceAppId` représentent le même assembly.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-118">Gets a value that indicates whether the specified `IDefinitionAppId` and `IReferenceAppId` represent the same assembly.</span></span>|  
|`IAppIdAuthority::DoesTextualDefinitionMatchTextualReference`|<span data-ttu-id="8bcbc-119">Obtient une valeur qui indique si la chaîne de définition spécifié et la chaîne de référence représentent le même assembly.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-119">Gets a value that indicates whether the specified definition string and reference string represent the same assembly.</span></span>|  
|`IAppIdAuthority::GenerateDefinitionKey`|<span data-ttu-id="8bcbc-120">Obtient une clé de chaîne qui représente le texte spécifié `IDefinitionAppId` instance.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-120">Gets a string key that represents the specified `IDefinitionAppId` instance.</span></span>|  
|`IAppIdAuthority::GenerateReferenceKey`|<span data-ttu-id="8bcbc-121">Obtient une clé de chaîne qui représente le texte spécifié `IReferenceAppId` instance.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-121">Gets a string key that represents the specified `IReferenceAppId` instance.</span></span>|  
|`IAppIdAuthority::HashDefinition`|<span data-ttu-id="8bcbc-122">Obtient une clé de hachage pour le texte spécifié `IDefinitionAppId` instance.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-122">Gets a hash key for the specified `IDefinitionAppId` instance.</span></span>|  
|`IAppIdAuthority::HashReference`|<span data-ttu-id="8bcbc-123">Obtient une clé de hachage pour le texte spécifié `IReferenceAppId` instance.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-123">Gets a hash key for the specified `IReferenceAppId` instance.</span></span>|  
|`IAppIdAuthority::ReferenceToText`|<span data-ttu-id="8bcbc-124">Obtient une version de chaîne de l’objet `IReferenceAppId`, en utilisant les valeurs d’indicateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-124">Gets a string version of the specified `IReferenceAppId`, using the specified flag values.</span></span>|  
|`IAppIdAuthority::TextToDefinition`|<span data-ttu-id="8bcbc-125">Obtient un pointeur d’interface vers un `IDefinitionAppId` instance qui représente l’assembly référencé par la clé de chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-125">Gets an interface pointer to an `IDefinitionAppId` instance that represents the assembly referenced by the specified string key.</span></span>|  
|`IAppIdAuthority::TextToReference`|<span data-ttu-id="8bcbc-126">Obtient un pointeur d’interface vers un `IReferenceAppId` instance qui représente l’assembly référencé par la clé de chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8bcbc-126">Gets an interface pointer to an `IReferenceAppId` instance that represents the assembly referenced by the specified string key.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="8bcbc-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8bcbc-127">Requirements</span></span>  
 <span data-ttu-id="8bcbc-128">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8bcbc-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8bcbc-129">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="8bcbc-129">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="8bcbc-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8bcbc-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8bcbc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bcbc-131">See also</span></span>
- [<span data-ttu-id="8bcbc-132">Interfaces de fusion</span><span class="sxs-lookup"><span data-stu-id="8bcbc-132">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
