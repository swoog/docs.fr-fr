---
title: IMetaDataTables::GetString, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetString
helpviewer_keywords:
- IMetaDataTables::GetString method [.NET Framework metadata]
- GetString method, IMetaDataTables interface [.NET Framework metadata]
ms.assetid: 895c35cf-b95d-4e3b-93b5-cfc1cf9044fc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3ed3501930b94eae59cf38355f8255ecf4165bcc
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33449580"
---
# <a name="imetadatatablesgetstring-method"></a><span data-ttu-id="9f974-102">IMetaDataTables::GetString, méthode</span><span class="sxs-lookup"><span data-stu-id="9f974-102">IMetaDataTables::GetString Method</span></span>
<span data-ttu-id="9f974-103">Obtient la chaîne à l’index spécifié à partir de la colonne de table dans l’étendue actuelle de la référence.</span><span class="sxs-lookup"><span data-stu-id="9f974-103">Gets the string at the specified index from the table column in the current reference scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f974-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f974-104">Syntax</span></span>  
  
```  
HRESULT GetString (   
    [in]  ULONG       ixString,  
    [out] const char  **ppString  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9f974-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f974-105">Parameters</span></span>  
 `ixString`  
 <span data-ttu-id="9f974-106">[in] Index auquel commencer à rechercher la valeur suivante.</span><span class="sxs-lookup"><span data-stu-id="9f974-106">[in] The index at which to start to search for the next value.</span></span>  
  
 `ppString`  
 <span data-ttu-id="9f974-107">[out] Pointeur vers un pointeur vers la valeur de la chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="9f974-107">[out] A pointer to a pointer to the returned string value.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9f974-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9f974-108">Requirements</span></span>  
 <span data-ttu-id="9f974-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9f974-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9f974-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="9f974-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9f974-111">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9f974-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9f974-112">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9f974-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f974-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f974-113">See Also</span></span>  
 [<span data-ttu-id="9f974-114">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="9f974-114">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)  
 [<span data-ttu-id="9f974-115">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="9f974-115">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
