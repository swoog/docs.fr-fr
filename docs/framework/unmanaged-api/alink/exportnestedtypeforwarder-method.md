---
title: ExportNestedTypeForwarder, méthode
ms.date: 03/30/2017
api_name:
- IALink.ExportNestedTypeForwarder
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ExportNestedTypeForwarder
helpviewer_keywords:
- ExportNestedTypeForwarder method
ms.assetid: 886ea6c5-6b26-4b88-8bf6-448d6d191950
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4dfb31a2fad8a07b3821ac85bbb43b25693f11d8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33404095"
---
# <a name="exportnestedtypeforwarder-method"></a><span data-ttu-id="99065-102">ExportNestedTypeForwarder, méthode</span><span class="sxs-lookup"><span data-stu-id="99065-102">ExportNestedTypeForwarder Method</span></span>
<span data-ttu-id="99065-103">Ajoute un redirecteur de type pour un type imbriqué à la table de type de l’assembly donné.</span><span class="sxs-lookup"><span data-stu-id="99065-103">Adds a type forwarder for a nested type to the type table of the given assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="99065-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99065-104">Syntax</span></span>  
  
```  
HRESULT ExportNestedTypeForwarder(  
    mdAssembly      AssemblyID,  
    mdToken         FileToken,  
    mdTypeDef       TypeToken,  
    mdExportedType  ParentType,  
    LPCWSTR         pszTypename,  
    DWORD           dwFlags,  
    mdExportedType* pType  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="99065-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99065-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="99065-106">ID de l’assembly à exporter à partir de.</span><span class="sxs-lookup"><span data-stu-id="99065-106">ID of the assembly to export from.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="99065-107">ID de jeton ou l’assembly du fichier qui définit le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="99065-107">File token or assembly ID of file that defines the type.</span></span>  
  
 `TypeToken`  
 <span data-ttu-id="99065-108">Jeton pour le type.</span><span class="sxs-lookup"><span data-stu-id="99065-108">Token for the type.</span></span>  
  
 `ParentType`  
 <span data-ttu-id="99065-109">Jeton de type parent.</span><span class="sxs-lookup"><span data-stu-id="99065-109">Token of parent type.</span></span>  
  
 `pszTypename`  
 <span data-ttu-id="99065-110">Nom de type qualifié complet à exporter.</span><span class="sxs-lookup"><span data-stu-id="99065-110">Fully qualified type name to export.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="99065-111">`ComType` indicateurs tels que `tdPublic` ou `tdNested`.</span><span class="sxs-lookup"><span data-stu-id="99065-111">`ComType` flags such as `tdPublic` or `tdNested`.</span></span>  
  
 `pType`  
 <span data-ttu-id="99065-112">Reçoit le jeton de type d’exportation.</span><span class="sxs-lookup"><span data-stu-id="99065-112">Receives token of export type.</span></span> <span data-ttu-id="99065-113">Cela est nécessaire uniquement pour émettre des types imbriqués.</span><span class="sxs-lookup"><span data-stu-id="99065-113">This is necessary only for emitting nested types.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="99065-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="99065-114">Return Value</span></span>  
 <span data-ttu-id="99065-115">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="99065-115">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="99065-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="99065-116">Requirements</span></span>  
 <span data-ttu-id="99065-117">Requiert alink.h</span><span class="sxs-lookup"><span data-stu-id="99065-117">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="99065-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99065-118">See Also</span></span>  
 [<span data-ttu-id="99065-119">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="99065-119">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="99065-120">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="99065-120">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="99065-121">API ALink</span><span class="sxs-lookup"><span data-stu-id="99065-121">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
