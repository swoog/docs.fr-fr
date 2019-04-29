---
title: LPOVERLAPPED_COMPLETION_ROUTINE (pointeur fonction)
ms.date: 03/30/2017
api_name:
- LPOVERLAPPED_COMPLETION_ROUTINE
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- LPOVERLAPPED_COMPLETION_ROUTINE
helpviewer_keywords:
- LPOVERLAPPED_COMPLETION_ROUTINE function pointer [.NET Framework hosting]
ms.assetid: 5fb645d9-b818-401c-8c2c-c30d86de58ba
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ce2ce6dd1210eef94e77b5d6a2d58a35cf971e6d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61765256"
---
# <a name="lpoverlappedcompletionroutine-function-pointer"></a><span data-ttu-id="cc984-102">LPOVERLAPPED_COMPLETION_ROUTINE (pointeur fonction)</span><span class="sxs-lookup"><span data-stu-id="cc984-102">LPOVERLAPPED_COMPLETION_ROUTINE Function Pointer</span></span>
<span data-ttu-id="cc984-103">Pointe vers une fonction qui avertit l’hôte lorsqu’un chevauchement (autrement dit, asynchrone) e/s sur un appareil est terminée.</span><span class="sxs-lookup"><span data-stu-id="cc984-103">Points to a function that notifies the host when an overlapped (that is, asynchronous) I/O to a device has completed.</span></span>  
  
 <span data-ttu-id="cc984-104">Ce pointeur de fonction a été déconseillé dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="cc984-104">This function pointer has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc984-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc984-105">Syntax</span></span>  
  
```  
typedef VOID (*LPOVERLAPPED_COMPLETION_ROUTINE) (  
    [in] DWORD  dwErrorCode,  
    [in] DWORD  dwNumberOfBytesTransfered,  
    [in] LPVOID lpOverlapped  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cc984-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc984-106">Parameters</span></span>  
 `dwErrorCode`  
 <span data-ttu-id="cc984-107">[in] Une valeur qui est un code d’erreur si l’appareil a été fermée ; Sinon, cette valeur est zéro.</span><span class="sxs-lookup"><span data-stu-id="cc984-107">[in] A value that is an error code if the device has been closed; otherwise, this value is zero.</span></span>  
  
 <span data-ttu-id="cc984-108">Fermeture d’un périphérique entraîne tout en attente d’e/s à l’appareil pour être achevée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="cc984-108">Closing a device causes all pending I/O to the device to be completed immediately.</span></span>  
  
 `dwNumberOfBytesTransfered`  
 <span data-ttu-id="cc984-109">[in] Le nombre d’octets transférés par l’opération d’e/s.</span><span class="sxs-lookup"><span data-stu-id="cc984-109">[in] The number of bytes transferred by the I/O operation.</span></span>  
  
 `lpOverlapped`  
 <span data-ttu-id="cc984-110">[in] Un pointeur vers une structure qui contient des informations à utiliser pour terminer la demande d’e/s.</span><span class="sxs-lookup"><span data-stu-id="cc984-110">[in] A pointer to a structure that contains information to be used to complete the I/O request.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cc984-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cc984-111">Remarks</span></span>  
 <span data-ttu-id="cc984-112">La fonction à laquelle `LPOVERLAPPED_COMPLETION_ROUTINE` points est une fonction de rappel et doit être implémentée par le writer de l’application d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="cc984-112">The function to which `LPOVERLAPPED_COMPLETION_ROUTINE` points is a callback function and must be implemented by the writer of the hosting application.</span></span> <span data-ttu-id="cc984-113">La fonction de rappel permet à l’hôte traiter la demande d’e/s terminée.</span><span class="sxs-lookup"><span data-stu-id="cc984-113">The callback function allows the host to process the completed I/O request.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cc984-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc984-114">Requirements</span></span>  
 <span data-ttu-id="cc984-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cc984-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cc984-116">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="cc984-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="cc984-117">**Bibliothèque :** MSCorWks.dll</span><span class="sxs-lookup"><span data-stu-id="cc984-117">**Library:** MSCorWks.dll</span></span>  
  
 <span data-ttu-id="cc984-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cc984-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc984-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc984-119">See also</span></span>

- [<span data-ttu-id="cc984-120">Fonctions d’hébergement CLR dépréciées</span><span class="sxs-lookup"><span data-stu-id="cc984-120">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
