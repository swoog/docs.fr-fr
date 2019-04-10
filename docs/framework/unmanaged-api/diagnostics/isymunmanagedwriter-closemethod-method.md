---
title: ISymUnmanagedWriter::CloseMethod, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.CloseMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::CloseMethod
helpviewer_keywords:
- ISymUnmanagedWriter::CloseMethod method [.NET Framework debugging]
- CloseMethod method [.NET Framework debugging]
ms.assetid: b8025e04-f0e5-40c8-849c-8cd51323420e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 591279a80b7d6a770127fb98eb71c056c48bdffd
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59231212"
---
# <a name="isymunmanagedwriterclosemethod-method"></a><span data-ttu-id="c291b-102">ISymUnmanagedWriter::CloseMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="c291b-102">ISymUnmanagedWriter::CloseMethod Method</span></span>
<span data-ttu-id="c291b-103">Ferme la méthode actuelle.</span><span class="sxs-lookup"><span data-stu-id="c291b-103">Closes the current method.</span></span> <span data-ttu-id="c291b-104">Une fois qu’une méthode est fermée, plus aucun symbole ne peut être définie qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="c291b-104">Once a method is closed, no more symbols can be defined within it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c291b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c291b-105">Syntax</span></span>  
  
```  
HRESULT CloseMethod();  
```  
  
## <a name="return-value"></a><span data-ttu-id="c291b-106">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c291b-106">Return Value</span></span>  
 <span data-ttu-id="c291b-107">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c291b-107">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c291b-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c291b-108">Requirements</span></span>  
 <span data-ttu-id="c291b-109">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="c291b-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c291b-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c291b-110">See also</span></span>

- [<span data-ttu-id="c291b-111">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="c291b-111">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
- [<span data-ttu-id="c291b-112">OpenMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="c291b-112">OpenMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openmethod-method.md)
