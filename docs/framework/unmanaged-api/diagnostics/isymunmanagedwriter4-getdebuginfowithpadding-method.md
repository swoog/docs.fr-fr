---
title: ISymUnmanagedWriter4::GetDebugInfoWithPadding, méthode
ms.date: 03/30/2017
ms.assetid: 881e20ca-8131-4bd0-ba41-c2d6391b0fe2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 191aa16c285b3a28beed65004d65525c9214ec93
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61650737"
---
# <a name="isymunmanagedwriter4getdebuginfowithpadding-method"></a><span data-ttu-id="171eb-102">ISymUnmanagedWriter4::GetDebugInfoWithPadding, méthode</span><span class="sxs-lookup"><span data-stu-id="171eb-102">ISymUnmanagedWriter4::GetDebugInfoWithPadding Method</span></span>
<span data-ttu-id="171eb-103">Fonctionne comme [GetDebugInfo, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-getdebuginfo-method.md) , à ceci près que la chaîne de chemin d’accès est remplie avec des zéros qui suivent le caractère null de fin pour rendre les données de chaîne de taille fixe de `MAX_PATH`.</span><span class="sxs-lookup"><span data-stu-id="171eb-103">Functions the same as [GetDebugInfo Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-getdebuginfo-method.md) except that the path string is padded with zeros following the terminating null character to make the string data a fixed size of `MAX_PATH`.</span></span> <span data-ttu-id="171eb-104">Marge intérieure est obtenu uniquement si la longueur de chaîne de chemin d’accès lui-même est inférieure à `MAX_PATH`.</span><span class="sxs-lookup"><span data-stu-id="171eb-104">Padding is only given if the path string length itself is less than `MAX_PATH`.</span></span>  
  
 <span data-ttu-id="171eb-105">Cela rend plus facile à écrire des outils que les fichiers PE de différence.</span><span class="sxs-lookup"><span data-stu-id="171eb-105">This makes it easier to write tools that difference PE files.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="171eb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="171eb-106">Syntax</span></span>  
  
```idl  
HRESULT GetDebugInfoWithPadding(    [in, out] IMAGE_DEBUG_DIRECTORY *pIDD,    [in] DWORD cData,    [out] DWORD *pcData,    [out, size_is(cData), length_is(*pcData)] BYTE data[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="171eb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="171eb-107">Parameters</span></span>  
  
|<span data-ttu-id="171eb-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="171eb-108">Parameter</span></span>|<span data-ttu-id="171eb-109">Description</span><span class="sxs-lookup"><span data-stu-id="171eb-109">Description</span></span>|  
|---------------|-----------------|  
|`pIDD`||  
|`cData`||  
|`pcData`||  
|`data`||  
  
## <a name="return-value"></a><span data-ttu-id="171eb-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="171eb-110">Return Value</span></span>  
 <span data-ttu-id="171eb-111">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="171eb-111">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="171eb-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="171eb-112">Requirements</span></span>  
 <span data-ttu-id="171eb-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="171eb-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="171eb-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="171eb-114">See also</span></span>

- [<span data-ttu-id="171eb-115">ISymUnmanagedWriter4, interface</span><span class="sxs-lookup"><span data-stu-id="171eb-115">ISymUnmanagedWriter4 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter4-interface.md)
