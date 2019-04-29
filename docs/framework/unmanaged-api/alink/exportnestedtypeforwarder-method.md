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
ms.openlocfilehash: 050ed0bbd4da38bede5a56ff95d0243f5f3cf1da
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61789907"
---
# <a name="exportnestedtypeforwarder-method"></a><span data-ttu-id="23f2b-102">ExportNestedTypeForwarder, méthode</span><span class="sxs-lookup"><span data-stu-id="23f2b-102">ExportNestedTypeForwarder Method</span></span>
<span data-ttu-id="23f2b-103">Ajoute un redirecteur de type pour un type imbriqué à la table de type de l’assembly donné.</span><span class="sxs-lookup"><span data-stu-id="23f2b-103">Adds a type forwarder for a nested type to the type table of the given assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="23f2b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23f2b-104">Syntax</span></span>  
  
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
  
## <a name="parameters"></a><span data-ttu-id="23f2b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23f2b-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="23f2b-106">ID de l’assembly à exporter à partir de.</span><span class="sxs-lookup"><span data-stu-id="23f2b-106">ID of the assembly to export from.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="23f2b-107">ID de jeton ou l’assembly du fichier qui définit le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="23f2b-107">File token or assembly ID of file that defines the type.</span></span>  
  
 `TypeToken`  
 <span data-ttu-id="23f2b-108">Jeton pour le type.</span><span class="sxs-lookup"><span data-stu-id="23f2b-108">Token for the type.</span></span>  
  
 `ParentType`  
 <span data-ttu-id="23f2b-109">Jeton de type parent.</span><span class="sxs-lookup"><span data-stu-id="23f2b-109">Token of parent type.</span></span>  
  
 `pszTypename`  
 <span data-ttu-id="23f2b-110">Nom de type qualifié complet à exporter.</span><span class="sxs-lookup"><span data-stu-id="23f2b-110">Fully qualified type name to export.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="23f2b-111">`ComType` indicateurs tels que `tdPublic` ou `tdNested`.</span><span class="sxs-lookup"><span data-stu-id="23f2b-111">`ComType` flags such as `tdPublic` or `tdNested`.</span></span>  
  
 `pType`  
 <span data-ttu-id="23f2b-112">Reçoit le jeton de type d’exportation.</span><span class="sxs-lookup"><span data-stu-id="23f2b-112">Receives token of export type.</span></span> <span data-ttu-id="23f2b-113">Cela est nécessaire uniquement pour émettre des types imbriqués.</span><span class="sxs-lookup"><span data-stu-id="23f2b-113">This is necessary only for emitting nested types.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="23f2b-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="23f2b-114">Return Value</span></span>  
 <span data-ttu-id="23f2b-115">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="23f2b-115">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="23f2b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23f2b-116">Requirements</span></span>  
 <span data-ttu-id="23f2b-117">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="23f2b-117">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="23f2b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23f2b-118">See also</span></span>

- [<span data-ttu-id="23f2b-119">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="23f2b-119">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="23f2b-120">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="23f2b-120">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="23f2b-121">API ALink</span><span class="sxs-lookup"><span data-stu-id="23f2b-121">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
