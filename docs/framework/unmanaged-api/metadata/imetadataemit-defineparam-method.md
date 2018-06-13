---
title: IMetaDataEmit::DefineParam, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineParam
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineParam
helpviewer_keywords:
- IMetaDataEmit::DefineParam method [.NET Framework metadata]
- DefineParam method [.NET Framework metadata]
ms.assetid: d86a3d14-4796-4909-9591-dfafe3de5ce4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5d49ac70aceb76f69711ea4bf514f69697ac156c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33447370"
---
# <a name="imetadataemitdefineparam-method"></a>IMetaDataEmit::DefineParam, méthode
Crée une définition de paramètre avec la signature spécifiée pour la méthode référencée par le jeton spécifié et obtient un jeton pour cette définition de paramètre.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT DefineParam (  
    [in]  mdMethodDef md,   
    [in]  ULONG       ulParamSeq,   
    [in]  LPCWSTR     szName,   
    [in]  DWORD       dwParamFlags,   
    [in]  DWORD       dwCPlusTypeFlag,   
    [in]  void const  *pValue,  
    [in]  ULONG       cchValue,   
    [out] mdParamDef  *ppd   
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `md`  
 [in] Le jeton pour la méthode dont le paramètre est défini.  
  
 `ulParamSeq`  
 [in] Numéro de séquence du paramètre.  
  
 `szName`  
 [in] Le nom du paramètre au format Unicode.  
  
 `dwParamFlags`  
 [in] Indicateurs pour le paramètre. Il s’agit d’un masque de bits de `CorParamAttr` valeurs.  
  
 `dwCPlusTypeFlag`  
 [in] `ELEMENT_TYPE_` *\** pour la valeur de constante.  
  
 `pValue`  
 [in] La valeur de constante pour le paramètre.  
  
 `cchValue`  
 [in] La taille, en caractères Unicode de `pValue`.  
  
 `ppd`  
 [out] Le `mdParamDef` jeton assigné.  
  
## <a name="remarks"></a>Notes  
 Les valeurs de séquence dans `ulParamSeq` commencent à 1 pour les paramètres. Une valeur de retour a un numéro de séquence 0.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IMetaDataEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [IMetaDataEmit2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
