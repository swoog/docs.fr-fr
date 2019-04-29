---
title: Fonction InitDbgTransportManager
ms.date: 03/30/2017
api_name:
- InitDbgTransportManager
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- InitDbgTransportManager
helpviewer_keywords:
- remote debugging API [Silverlight]
- InitDbgTransportManager function
- Silverlight, remote debugging
ms.assetid: a30102ff-c52e-48c9-b3a9-aa14286a42b2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 74cb2c7d1f79d23e1331cc7192ba2d6acfd9835c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61761648"
---
# <a name="initdbgtransportmanager-function"></a><span data-ttu-id="b9d11-102">Fonction InitDbgTransportManager</span><span class="sxs-lookup"><span data-stu-id="b9d11-102">InitDbgTransportManager Function</span></span>
<span data-ttu-id="b9d11-103">Initialise le gestionnaire de transport pour se connecter à une cible distante pour l'énumération des processus et du runtime.</span><span class="sxs-lookup"><span data-stu-id="b9d11-103">Initializes the transport manager to connect to a remote target for process and runtime enumeration.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b9d11-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9d11-104">Syntax</span></span>  
  
```  
HRESULT InitDbgTransportManager ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="b9d11-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b9d11-105">Return Value</span></span>  
 <span data-ttu-id="b9d11-106">S_OK</span><span class="sxs-lookup"><span data-stu-id="b9d11-106">S_OK</span></span>  
 <span data-ttu-id="b9d11-107">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="b9d11-107">Success.</span></span>  
  
 <span data-ttu-id="b9d11-108">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="b9d11-108">E_OUTOFMEMORY</span></span>  
 <span data-ttu-id="b9d11-109">La fonction n'a pas pu allouer de mémoire pour un gestionnaire de transport.</span><span class="sxs-lookup"><span data-stu-id="b9d11-109">The function was unable to allocate memory for a transport manager.</span></span>  
  
 <span data-ttu-id="b9d11-110">E_FAIL (ou autres codes de retour E_)</span><span class="sxs-lookup"><span data-stu-id="b9d11-110">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="b9d11-111">Autres échecs.</span><span class="sxs-lookup"><span data-stu-id="b9d11-111">Other failures.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b9d11-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9d11-112">Requirements</span></span>  
 <span data-ttu-id="b9d11-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b9d11-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b9d11-114">**En-tête :** CoreClrRemoteDebuggingInterfaces.h</span><span class="sxs-lookup"><span data-stu-id="b9d11-114">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="b9d11-115">**Bibliothèque :** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="b9d11-115">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="b9d11-116">**Versions du .NET framework :** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="b9d11-116">**.NET Framework Versions:** 3.5 SP1</span></span>
