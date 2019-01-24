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
ms.openlocfilehash: a6f8c8b522aabfce3b83b6b624bd0ca9757448ad
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54666018"
---
# <a name="isymunmanagedwriterclosemethod-method"></a><span data-ttu-id="b6cda-102">ISymUnmanagedWriter::CloseMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="b6cda-102">ISymUnmanagedWriter::CloseMethod Method</span></span>
<span data-ttu-id="b6cda-103">Ferme la méthode actuelle.</span><span class="sxs-lookup"><span data-stu-id="b6cda-103">Closes the current method.</span></span> <span data-ttu-id="b6cda-104">Une fois qu’une méthode est fermée, plus aucun symbole ne peut être définie qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="b6cda-104">Once a method is closed, no more symbols can be defined within it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b6cda-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6cda-105">Syntax</span></span>  
  
```  
HRESULT CloseMethod();  
```  
  
## <a name="return-value"></a><span data-ttu-id="b6cda-106">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b6cda-106">Return Value</span></span>  
 <span data-ttu-id="b6cda-107">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b6cda-107">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b6cda-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b6cda-108">Requirements</span></span>  
 <span data-ttu-id="b6cda-109">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="b6cda-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b6cda-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6cda-110">See also</span></span>
- [<span data-ttu-id="b6cda-111">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="b6cda-111">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
- [<span data-ttu-id="b6cda-112">OpenMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="b6cda-112">OpenMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openmethod-method.md)
