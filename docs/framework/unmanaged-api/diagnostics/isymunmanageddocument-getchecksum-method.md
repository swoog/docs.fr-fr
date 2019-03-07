---
title: ISymUnmanagedDocument::GetCheckSum, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetCheckSum
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetCheckSum
helpviewer_keywords:
- ISymUnmanagedDocument::GetCheckSum method [.NET Framework debugging]
- GetCheckSum method [.NET Framework debugging]
ms.assetid: 9bc881b3-e2ce-48a7-ad69-17eaaa304120
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 80cda4c31ca78e0350639df809ec1e9f1dcbbaea
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57498248"
---
# <a name="isymunmanageddocumentgetchecksum-method"></a><span data-ttu-id="ed69c-102">ISymUnmanagedDocument::GetCheckSum, méthode</span><span class="sxs-lookup"><span data-stu-id="ed69c-102">ISymUnmanagedDocument::GetCheckSum Method</span></span>
<span data-ttu-id="ed69c-103">Obtient la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="ed69c-103">Gets the checksum.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ed69c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed69c-104">Syntax</span></span>  
  
```  
HRESULT GetCheckSum(  
    [in]  ULONG32  cData,  
    [out] ULONG32  *pcData,  
    [out, size_is(cData), length_is(*pcData)] BYTE data[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ed69c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed69c-105">Parameters</span></span>  
 `cData`  
 <span data-ttu-id="ed69c-106">[in] La longueur de la mémoire tampon fournie par le `data` paramètre</span><span class="sxs-lookup"><span data-stu-id="ed69c-106">[in] The length of the buffer provided by the `data` parameter</span></span>  
  
 `pcData`  
 <span data-ttu-id="ed69c-107">[out] La taille et la longueur de la somme de contrôle, en octets.</span><span class="sxs-lookup"><span data-stu-id="ed69c-107">[out] The size and length of the checksum, in bytes.</span></span>  
  
 `data`  
 <span data-ttu-id="ed69c-108">[out] La mémoire tampon qui reçoit la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="ed69c-108">[out] The buffer that receives the checksum.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ed69c-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ed69c-109">Return Value</span></span>  
 <span data-ttu-id="ed69c-110">S_OK si la méthode réussit ; Sinon, un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ed69c-110">S_OK if the method succeeds; otherwise, an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed69c-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed69c-111">See also</span></span>
- [<span data-ttu-id="ed69c-112">ISymUnmanagedDocument, interface</span><span class="sxs-lookup"><span data-stu-id="ed69c-112">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
