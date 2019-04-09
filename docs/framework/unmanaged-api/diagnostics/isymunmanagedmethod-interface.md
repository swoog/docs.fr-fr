---
title: ISymUnmanagedMethod, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod
helpviewer_keywords:
- ISymUnmanagedMethod interface [.NET Framework debugging]
ms.assetid: f204d74c-cc79-4092-83bb-60654be95649
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c29656a4787c674886505a3be2508470460dfc10
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59136524"
---
# <a name="isymunmanagedmethod-interface"></a>ISymUnmanagedMethod, interface
Représente une méthode dans le magasin de symboles. Cette interface fournit l’accès aux seuls les attributs liés aux symboles d’une méthode, au lieu des attributs de type.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[GetNamespace, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getnamespace-method.md)|Obtient l’espace de noms dans lequel cette méthode est définie.|  
|[GetOffset, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getoffset-method.md)|Retourne le décalage au sein de cette méthode qui correspond à une position donnée dans un document.|  
|[GetParameters, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getparameters-method.md)|Obtient les paramètres de cette méthode.|  
|[GetRanges, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getranges-method.md)|Une position donnée dans un document, retourne un tableau de début et fin paires d’offsets qui correspondent aux plages de langage intermédiaire Microsoft (MSIL) qui traite de la position au sein de cette méthode.|  
|[GetRootScope, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getrootscope-method.md)|Obtient la portée lexicale racine au sein de cette méthode. Cette portée englobe la totalité de la méthode.|  
|[GetScopeFromOffset, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getscopefromoffset-method.md)|Obtient la portée lexicale la plus englobante dans cette méthode qui englobe l’offset donné.|  
|[GetSequencePointCount, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getsequencepointcount-method.md)|Obtient le nombre de points de séquence au sein de cette méthode.|  
|[GetSequencePoints, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getsequencepoints-method.md)|Obtient tous les points de séquence au sein de cette méthode.|  
|[GetSourceStartEnd, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-getsourcestartend-method.md)|Obtient les positions de document de début et de fin de la source de cette méthode.|  
|[GetToken, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-gettoken-method.md)|Retourne le jeton de métadonnées pour cette méthode.|  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces du magasin de symboles de diagnostics](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
