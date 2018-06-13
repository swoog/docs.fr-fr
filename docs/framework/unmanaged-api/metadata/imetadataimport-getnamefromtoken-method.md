---
title: IMetaDataImport::GetNameFromToken, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetNameFromToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetNameFromToken
helpviewer_keywords:
- GetNameFromToken method [.NET Framework metadata]
- IMetaDataImport::GetNameFromToken method [.NET Framework metadata]
ms.assetid: 32114ecf-8916-4ab2-a201-179c017344f1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a39eac88537d47535844d1f05e0741cc94142f0a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33447251"
---
# <a name="imetadataimportgetnamefromtoken-method"></a><span data-ttu-id="d7ea1-102">IMetaDataImport::GetNameFromToken, méthode</span><span class="sxs-lookup"><span data-stu-id="d7ea1-102">IMetaDataImport::GetNameFromToken Method</span></span>
<span data-ttu-id="d7ea1-103">Obtient le nom UTF-8 de l'objet référencé par le jeton de métadonnées spécifié.</span><span class="sxs-lookup"><span data-stu-id="d7ea1-103">Gets the UTF-8 name of the object referenced by the specified metadata token.</span></span> <span data-ttu-id="d7ea1-104">Cette méthode est obsolète.</span><span class="sxs-lookup"><span data-stu-id="d7ea1-104">This method is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d7ea1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7ea1-105">Syntax</span></span>  
  
```  
HRESULT GetNameFromToken (  
   [in] mdToken      tk,  
   [out] MDUTF8CSTR  *pszUtf8NamePtr  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d7ea1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7ea1-106">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="d7ea1-107">[in] Le jeton qui représente l’objet à retourner le nom.</span><span class="sxs-lookup"><span data-stu-id="d7ea1-107">[in] The token representing the object to return the name for.</span></span>  
  
 `pszUtf8NamePtr`  
 <span data-ttu-id="d7ea1-108">[out] Pointeur vers le nom d’objet UTF-8 dans le tas.</span><span class="sxs-lookup"><span data-stu-id="d7ea1-108">[out] A pointer to the UTF-8 object name in the heap.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d7ea1-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d7ea1-109">Remarks</span></span>  
 <span data-ttu-id="d7ea1-110">`GetNameFromToken` est obsolète.</span><span class="sxs-lookup"><span data-stu-id="d7ea1-110">`GetNameFromToken` is obsolete.</span></span> <span data-ttu-id="d7ea1-111">En guise d’alternative, appelez une méthode pour obtenir les propriétés du type particulier de jeton requis, tels que `GetFieldProps` pour un champ ou `GetMethodProps` pour une méthode.</span><span class="sxs-lookup"><span data-stu-id="d7ea1-111">As an alternative, call a method to get the properties of the particular type of token required, such as `GetFieldProps` for a field or `GetMethodProps` for a method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d7ea1-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d7ea1-112">Requirements</span></span>  
 <span data-ttu-id="d7ea1-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d7ea1-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d7ea1-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="d7ea1-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d7ea1-115">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d7ea1-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d7ea1-116">**Versions du .NET framework :** 1.0</span><span class="sxs-lookup"><span data-stu-id="d7ea1-116">**.NET Framework Versions:** 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d7ea1-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7ea1-117">See Also</span></span>  
 [<span data-ttu-id="d7ea1-118">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="d7ea1-118">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="d7ea1-119">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="d7ea1-119">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
