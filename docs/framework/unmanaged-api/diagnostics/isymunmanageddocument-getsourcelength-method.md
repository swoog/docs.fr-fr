---
title: ISymUnmanagedDocument::GetSourceLength, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetSourceLength
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetSourceLength
helpviewer_keywords:
- GetSourceLength method [.NET Framework debugging]
- ISymUnmanagedDocument::GetSourceLength method [.NET Framework debugging]
ms.assetid: e087dbbb-f4fb-4fbe-8292-e4f1a14d0df2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 11ab9f8077a4b2a9e97c321c6edbe629dc0de19d
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57500731"
---
# <a name="isymunmanageddocumentgetsourcelength-method"></a><span data-ttu-id="4cf19-102">ISymUnmanagedDocument::GetSourceLength, méthode</span><span class="sxs-lookup"><span data-stu-id="4cf19-102">ISymUnmanagedDocument::GetSourceLength Method</span></span>
<span data-ttu-id="4cf19-103">Obtient la longueur, en octets, de la source incorporée.</span><span class="sxs-lookup"><span data-stu-id="4cf19-103">Gets the length, in bytes, of the embedded source.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4cf19-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cf19-104">Syntax</span></span>  
  
```  
HRESULT GetSourceLength(  
    [out, retval]  ULONG32*  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4cf19-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4cf19-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="4cf19-106">[out] Pointeur vers une variable qui indique la longueur, en octets, de la source incorporée.</span><span class="sxs-lookup"><span data-stu-id="4cf19-106">[out] A pointer to a variable that indicates the length, in bytes, of the embedded source.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4cf19-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4cf19-107">Return Value</span></span>  
 <span data-ttu-id="4cf19-108">S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="4cf19-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4cf19-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cf19-109">See also</span></span>
- [<span data-ttu-id="4cf19-110">ISymUnmanagedDocument, interface</span><span class="sxs-lookup"><span data-stu-id="4cf19-110">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
