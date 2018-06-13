---
title: ISymUnmanagedSourceServerModule::GetSourceServerData, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSourceServerModule.GetSourceServerData
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSourceServerModule::GetSourceServerData
helpviewer_keywords:
- ISymUnmanagedSourceServerModule::GetSourceServerData method [.NET Framework debugging]
- GetSourceServerData method [.NET Framework debugging]
ms.assetid: 20bdf8ff-2d15-4c64-8950-6888f642d6c0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: afc041896615e906ac49eed9a7be139dff217463
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33427009"
---
# <a name="isymunmanagedsourceservermodulegetsourceserverdata-method"></a><span data-ttu-id="efefb-102">ISymUnmanagedSourceServerModule::GetSourceServerData, méthode</span><span class="sxs-lookup"><span data-stu-id="efefb-102">ISymUnmanagedSourceServerModule::GetSourceServerData Method</span></span>
<span data-ttu-id="efefb-103">Retourne les données du serveur source pour le module.</span><span class="sxs-lookup"><span data-stu-id="efefb-103">Returns the source server data for the module.</span></span> <span data-ttu-id="efefb-104">L’appelant doit libérer des ressources à l’aide de `CoTaskMemFree`.</span><span class="sxs-lookup"><span data-stu-id="efefb-104">The caller must free resources by using `CoTaskMemFree`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="efefb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efefb-105">Syntax</span></span>  
  
```  
HRESULT GetSourceServerData(  
    [out] ULONG* pDataByteCount,   
    [out, size_is (, *pDataByteCount)] BYTE** ppData);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="efefb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="efefb-106">Parameters</span></span>  
 `pDataByteCount`  
 <span data-ttu-id="efefb-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en octets, les source des données du serveur.</span><span class="sxs-lookup"><span data-stu-id="efefb-107">[out] A pointer to a `ULONG32` that receives the size, in bytes, of the source server data.</span></span>  
  
 `ppData`  
 <span data-ttu-id="efefb-108">[out] Un pointeur vers retourné `pDataByteCount` valeur.</span><span class="sxs-lookup"><span data-stu-id="efefb-108">[out] A pointer to the returned `pDataByteCount` value.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="efefb-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="efefb-109">Return Value</span></span>  
 <span data-ttu-id="efefb-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="efefb-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="efefb-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="efefb-111">Requirements</span></span>  
 <span data-ttu-id="efefb-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="efefb-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="efefb-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efefb-113">See Also</span></span>  
 [<span data-ttu-id="efefb-114">ISymUnmanagedSourceServerModule, interface</span><span class="sxs-lookup"><span data-stu-id="efefb-114">ISymUnmanagedSourceServerModule Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsourceservermodule-interface.md)
