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
ms.openlocfilehash: b494b8b776f4cb0eb534233c5a03ab2d34a698ef
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59115620"
---
# <a name="createalink-function"></a><span data-ttu-id="75b94-102">CreateALink, fonction</span><span class="sxs-lookup"><span data-stu-id="75b94-102">CreateALink Function</span></span>
<span data-ttu-id="75b94-103">Crée une instance de l’utilitaire Assembly Linker et définit un pointeur vers l’interface spécifiée.</span><span class="sxs-lookup"><span data-stu-id="75b94-103">Creates an instance of the Assembly Linker and sets a pointer to the specified interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="75b94-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75b94-104">Syntax</span></span>  
  
```  
HRESULT CreateALink (  
   REFIID riid,  
   IUnknown **ppInterface  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="75b94-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75b94-105">Parameters</span></span>  
  
|<span data-ttu-id="75b94-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="75b94-106">Parameter</span></span>|<span data-ttu-id="75b94-107">Description</span><span class="sxs-lookup"><span data-stu-id="75b94-107">Description</span></span>|  
|---------------|-----------------|  
|`riid`|<span data-ttu-id="75b94-108">Le nom physique d’une des interfaces Assembly Linker.</span><span class="sxs-lookup"><span data-stu-id="75b94-108">The physical name of one of the Assembly Linker interfaces.</span></span>|  
|`ppInterface`|<span data-ttu-id="75b94-109">L’emplacement qui réussit, contient un pointeur vers le `riid` interface.</span><span class="sxs-lookup"><span data-stu-id="75b94-109">The location that on successful completion contains a pointer to the `riid` interface.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="75b94-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75b94-110">Requirements</span></span>  
 <span data-ttu-id="75b94-111">**Bibliothèque**: alink.dll</span><span class="sxs-lookup"><span data-stu-id="75b94-111">**Library**: alink.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="75b94-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75b94-112">See also</span></span>

- [<span data-ttu-id="75b94-113">Al.exe (Assembly Linker)</span><span class="sxs-lookup"><span data-stu-id="75b94-113">Al.exe (Assembly Linker)</span></span>](../../../../docs/framework/tools/al-exe-assembly-linker.md)
