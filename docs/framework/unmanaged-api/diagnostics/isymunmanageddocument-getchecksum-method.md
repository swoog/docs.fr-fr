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
ms.openlocfilehash: a60bf279c143559e7410d8dfd8213d3da1d05a6d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59127555"
---
# <a name="isymunmanageddocumentgetchecksum-method"></a><span data-ttu-id="072f0-102">ISymUnmanagedDocument::GetCheckSum, méthode</span><span class="sxs-lookup"><span data-stu-id="072f0-102">ISymUnmanagedDocument::GetCheckSum Method</span></span>
<span data-ttu-id="072f0-103">Obtient la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="072f0-103">Gets the checksum.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="072f0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="072f0-104">Syntax</span></span>  
  
```  
HRESULT GetCheckSum(  
    [in]  ULONG32  cData,  
    [out] ULONG32  *pcData,  
    [out, size_is(cData), length_is(*pcData)] BYTE data[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="072f0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="072f0-105">Parameters</span></span>  
 `cData`  
 <span data-ttu-id="072f0-106">[in] La longueur de la mémoire tampon fournie par le `data` paramètre</span><span class="sxs-lookup"><span data-stu-id="072f0-106">[in] The length of the buffer provided by the `data` parameter</span></span>  
  
 `pcData`  
 <span data-ttu-id="072f0-107">[out] La taille et la longueur de la somme de contrôle, en octets.</span><span class="sxs-lookup"><span data-stu-id="072f0-107">[out] The size and length of the checksum, in bytes.</span></span>  
  
 `data`  
 <span data-ttu-id="072f0-108">[out] La mémoire tampon qui reçoit la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="072f0-108">[out] The buffer that receives the checksum.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="072f0-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="072f0-109">Return Value</span></span>  
 <span data-ttu-id="072f0-110">S_OK si la méthode réussit ; Sinon, un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="072f0-110">S_OK if the method succeeds; otherwise, an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="072f0-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="072f0-111">See also</span></span>

- [<span data-ttu-id="072f0-112">ISymUnmanagedDocument, interface</span><span class="sxs-lookup"><span data-stu-id="072f0-112">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
