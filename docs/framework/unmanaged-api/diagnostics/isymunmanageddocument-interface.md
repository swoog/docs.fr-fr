---
title: ISymUnmanagedDocument, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument
helpviewer_keywords:
- ISymUnmanagedDocument interface [.NET Framework debugging]
ms.assetid: 5c26b366-6e81-467c-9dd0-02dd26fee0a3
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 33213aced635549dd439cf679d89367a71baa7c7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61939774"
---
# <a name="isymunmanageddocument-interface"></a><span data-ttu-id="abac9-102">ISymUnmanagedDocument, interface</span><span class="sxs-lookup"><span data-stu-id="abac9-102">ISymUnmanagedDocument Interface</span></span>
<span data-ttu-id="abac9-103">Représente un document référencé par un magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="abac9-103">Represents a document referenced by a symbol store.</span></span> <span data-ttu-id="abac9-104">Un document est défini par une adresse Web (URL) et un GUID de type de document.</span><span class="sxs-lookup"><span data-stu-id="abac9-104">A document is defined by a uniform resource locator (URL) and a document type GUID.</span></span> <span data-ttu-id="abac9-105">Vous pouvez rechercher le document, quel que soit la façon dont elle est stockée à l’aide de l’URL et le GUID de type de document.</span><span class="sxs-lookup"><span data-stu-id="abac9-105">You can locate the document regardless of how it is stored by using the URL and document type GUID.</span></span> <span data-ttu-id="abac9-106">Vous pouvez stocker la source de document dans le magasin de symboles et en la récupérant via cette interface.</span><span class="sxs-lookup"><span data-stu-id="abac9-106">You can store the document source in the symbol store and retrieve it through this interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="abac9-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="abac9-107">Methods</span></span>  
  
|<span data-ttu-id="abac9-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="abac9-108">Method</span></span>|<span data-ttu-id="abac9-109">Description</span><span class="sxs-lookup"><span data-stu-id="abac9-109">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="abac9-110">FindClosestLine, méthode</span><span class="sxs-lookup"><span data-stu-id="abac9-110">FindClosestLine Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-findclosestline-method.md)|<span data-ttu-id="abac9-111">Retourne la ligne la plus proche constituant un point de séquence, la fonction d’une ligne dans ce document qui peut être ou non un point de séquence.</span><span class="sxs-lookup"><span data-stu-id="abac9-111">Returns the closest line that is a sequence point, given a line in this document that may or may not be a sequence point.</span></span>|  
|[<span data-ttu-id="abac9-112">GetCheckSum, méthode</span><span class="sxs-lookup"><span data-stu-id="abac9-112">GetCheckSum Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getchecksum-method.md)|<span data-ttu-id="abac9-113">Obtient la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="abac9-113">Gets the checksum.</span></span>|  
|[<span data-ttu-id="abac9-114">GetCheckSumAlgorithmId, méthode</span><span class="sxs-lookup"><span data-stu-id="abac9-114">GetCheckSumAlgorithmId Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getchecksumalgorithmid-method.md)|<span data-ttu-id="abac9-115">Obtient l’identificateur d’algorithme de somme de contrôle, ou retourne un GUID de tous les zéros s’il n’existe aucune somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="abac9-115">Gets the checksum algorithm identifier, or returns a GUID of all zeros if there is no checksum.</span></span>|  
|[<span data-ttu-id="abac9-116">GetDocumentType, méthode</span><span class="sxs-lookup"><span data-stu-id="abac9-116">GetDocumentType Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getdocumenttype-method.md)|<span data-ttu-id="abac9-117">Obtient le type de document de ce document.</span><span class="sxs-lookup"><span data-stu-id="abac9-117">Gets the document type of this document.</span></span>|  
|[<span data-ttu-id="abac9-118">GetLanguage, méthode</span><span class="sxs-lookup"><span data-stu-id="abac9-118">GetLanguage Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getlanguage-method.md)|<span data-ttu-id="abac9-119">Obtient l’identificateur de langue de ce document.</span><span class="sxs-lookup"><span data-stu-id="abac9-119">Gets the language identifier of this document.</span></span>|  
|[<span data-ttu-id="abac9-120">GetLanguageVendor, méthode</span><span class="sxs-lookup"><span data-stu-id="abac9-120">GetLanguageVendor Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getlanguagevendor-method.md)|<span data-ttu-id="abac9-121">Obtient le fournisseur de langage de ce document.</span><span class="sxs-lookup"><span data-stu-id="abac9-121">Gets the language vendor of this document.</span></span>|  
|[<span data-ttu-id="abac9-122">GetSourceLength, méthode</span><span class="sxs-lookup"><span data-stu-id="abac9-122">GetSourceLength Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getsourcelength-method.md)|<span data-ttu-id="abac9-123">Obtient la longueur, en octets, de la source incorporée.</span><span class="sxs-lookup"><span data-stu-id="abac9-123">Gets the length, in bytes, of the embedded source.</span></span>|  
|[<span data-ttu-id="abac9-124">GetSourceRange, méthode</span><span class="sxs-lookup"><span data-stu-id="abac9-124">GetSourceRange Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getsourcerange-method.md)|<span data-ttu-id="abac9-125">Retourne la plage spécifiée de la source incorporée dans la mémoire tampon donnée.</span><span class="sxs-lookup"><span data-stu-id="abac9-125">Returns the specified range of the embedded source into the given buffer.</span></span>|  
|[<span data-ttu-id="abac9-126">GetURL, méthode</span><span class="sxs-lookup"><span data-stu-id="abac9-126">GetURL Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-geturl-method.md)|<span data-ttu-id="abac9-127">Retourne l’URL de ce document.</span><span class="sxs-lookup"><span data-stu-id="abac9-127">Returns the URL for this document.</span></span>|  
|[<span data-ttu-id="abac9-128">HasEmbeddedSource, méthode</span><span class="sxs-lookup"><span data-stu-id="abac9-128">HasEmbeddedSource Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-hasembeddedsource-method.md)|<span data-ttu-id="abac9-129">Retourne `true` si le document a la source incorporée dans les symboles de débogage ; sinon, retourne `false`.</span><span class="sxs-lookup"><span data-stu-id="abac9-129">Returns `true` if the document has source embedded in the debugging symbols; otherwise, returns `false`.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="abac9-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abac9-130">See also</span></span>

- [<span data-ttu-id="abac9-131">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="abac9-131">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
