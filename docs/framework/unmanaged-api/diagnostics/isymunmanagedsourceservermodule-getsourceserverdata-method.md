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
ms.openlocfilehash: ea8052152b08732906c707648f361bba4d83a276
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59173574"
---
# <a name="isymunmanagedsourceservermodulegetsourceserverdata-method"></a><span data-ttu-id="917ff-102">ISymUnmanagedSourceServerModule::GetSourceServerData, méthode</span><span class="sxs-lookup"><span data-stu-id="917ff-102">ISymUnmanagedSourceServerModule::GetSourceServerData Method</span></span>
<span data-ttu-id="917ff-103">Retourne les données du serveur source pour le module.</span><span class="sxs-lookup"><span data-stu-id="917ff-103">Returns the source server data for the module.</span></span> <span data-ttu-id="917ff-104">L’appelant doit libérer des ressources à l’aide de `CoTaskMemFree`.</span><span class="sxs-lookup"><span data-stu-id="917ff-104">The caller must free resources by using `CoTaskMemFree`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="917ff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="917ff-105">Syntax</span></span>  
  
```  
HRESULT GetSourceServerData(  
    [out] ULONG* pDataByteCount,   
    [out, size_is (, *pDataByteCount)] BYTE** ppData);  
```  
  
## <a name="parameters"></a><span data-ttu-id="917ff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="917ff-106">Parameters</span></span>  
 `pDataByteCount`  
 <span data-ttu-id="917ff-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en octets, des données de serveur source.</span><span class="sxs-lookup"><span data-stu-id="917ff-107">[out] A pointer to a `ULONG32` that receives the size, in bytes, of the source server data.</span></span>  
  
 `ppData`  
 <span data-ttu-id="917ff-108">[out] Un pointeur vers le texte retourné `pDataByteCount` valeur.</span><span class="sxs-lookup"><span data-stu-id="917ff-108">[out] A pointer to the returned `pDataByteCount` value.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="917ff-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="917ff-109">Return Value</span></span>  
 <span data-ttu-id="917ff-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="917ff-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="917ff-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="917ff-111">Requirements</span></span>  
 <span data-ttu-id="917ff-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="917ff-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="917ff-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="917ff-113">See also</span></span>

- [<span data-ttu-id="917ff-114">ISymUnmanagedSourceServerModule, interface</span><span class="sxs-lookup"><span data-stu-id="917ff-114">ISymUnmanagedSourceServerModule Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsourceservermodule-interface.md)
