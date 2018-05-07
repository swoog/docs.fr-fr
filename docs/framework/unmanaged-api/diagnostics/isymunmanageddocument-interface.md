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
ms.openlocfilehash: f75e517890275b90523dc42cdac3a83d871beac7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="isymunmanageddocument-interface"></a>ISymUnmanagedDocument, interface
Représente un document référencé par un magasin de symboles. Un document est défini par un localisateur de ressource uniforme (URL) et un GUID de type de document. Vous pouvez localiser le document, quelle que soit la façon dont elle est stockée à l’aide de l’URL et le GUID de type de document. Vous pouvez stocker la source de document dans le magasin de symboles et en la récupérant via cette interface.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[FindClosestLine, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-findclosestline-method.md)|Retourne la ligne la plus proche qui est un point de séquence, en fonction d’une ligne dans ce document, qui peut être ou non un point de séquence.|  
|[GetCheckSum, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getchecksum-method.md)|Obtient la somme de contrôle.|  
|[GetCheckSumAlgorithmId, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getchecksumalgorithmid-method.md)|Obtient l’identificateur d’algorithme de somme de contrôle, ou retourne un GUID de tous les zéros s’il n’existe aucune somme de contrôle.|  
|[GetDocumentType, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getdocumenttype-method.md)|Obtient le type de document de ce document.|  
|[GetLanguage, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getlanguage-method.md)|Obtient l’identificateur de langue de ce document.|  
|[GetLanguageVendor, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getlanguagevendor-method.md)|Obtient le fournisseur de langage de ce document.|  
|[GetSourceLength, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getsourcelength-method.md)|Obtient la longueur, en octets, de la source incorporée.|  
|[GetSourceRange, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-getsourcerange-method.md)|Retourne la plage spécifiée de la source incorporée dans la mémoire tampon donnée.|  
|[GetURL, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-geturl-method.md)|Retourne l’URL de ce document.|  
|[HasEmbeddedSource, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-hasembeddedsource-method.md)|Retourne `true` si le document a la source incorporée dans les symboles de débogage ; sinon, retourne `false`.|  
  
## <a name="see-also"></a>Voir aussi  
 [Interfaces du magasin de symboles de diagnostics](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
