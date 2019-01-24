---
title: CreateALink, fonction
ms.date: 03/30/2017
api_name:
- CreateALink
api_location:
- alink.dll
api_type:
- DLLExport
f1_keywords:
- CreateALink
helpviewer_keywords:
- CreateALink function
- Alink API, CreateALink function
ms.assetid: fc73bcb9-6af6-44d8-bc39-2f4400325dae
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f809395de68b596f769f9396da8668bf296b1aa2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54675039"
---
# <a name="createalink-function"></a><span data-ttu-id="24059-102">CreateALink, fonction</span><span class="sxs-lookup"><span data-stu-id="24059-102">CreateALink Function</span></span>
<span data-ttu-id="24059-103">Crée une instance de l’utilitaire Assembly Linker et définit un pointeur vers l’interface spécifiée.</span><span class="sxs-lookup"><span data-stu-id="24059-103">Creates an instance of the Assembly Linker and sets a pointer to the specified interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24059-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24059-104">Syntax</span></span>  
  
```  
HRESULT CreateALink (  
   REFIID riid,  
   IUnknown **ppInterface  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="24059-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24059-105">Parameters</span></span>  
  
|<span data-ttu-id="24059-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="24059-106">Parameter</span></span>|<span data-ttu-id="24059-107">Description</span><span class="sxs-lookup"><span data-stu-id="24059-107">Description</span></span>|  
|---------------|-----------------|  
|`riid`|<span data-ttu-id="24059-108">Le nom physique d’une des interfaces Assembly Linker.</span><span class="sxs-lookup"><span data-stu-id="24059-108">The physical name of one of the Assembly Linker interfaces.</span></span>|  
|`ppInterface`|<span data-ttu-id="24059-109">L’emplacement qui réussit, contient un pointeur vers le `riid` interface.</span><span class="sxs-lookup"><span data-stu-id="24059-109">The location that on successful completion contains a pointer to the `riid` interface.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="24059-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="24059-110">Requirements</span></span>  
 <span data-ttu-id="24059-111">**Bibliothèque**: alink.dll</span><span class="sxs-lookup"><span data-stu-id="24059-111">**Library**: alink.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="24059-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24059-112">See also</span></span>
- [<span data-ttu-id="24059-113">Al.exe (Assembly Linker)</span><span class="sxs-lookup"><span data-stu-id="24059-113">Al.exe (Assembly Linker)</span></span>](../../../../docs/framework/tools/al-exe-assembly-linker.md)
