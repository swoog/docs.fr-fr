---
title: IMetaDataImport::GetPropertyProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetPropertyProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetPropertyProps
helpviewer_keywords:
- GetPropertyProps method [.NET Framework metadata]
- IMetaDataImport::GetPropertyProps method [.NET Framework metadata]
ms.assetid: dc0ff3e6-7e7d-4f6c-948d-52b28f5cb78c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a08bd5beeb9fab1cd5b703c3afc4e82aaf71dbbc
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59122601"
---
# <a name="imetadataimportgetpropertyprops-method"></a>IMetaDataImport::GetPropertyProps, méthode
Obtient les métadonnées pour la propriété représentée par le jeton spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetPropertyProps (  
   [in]  mdProperty        prop,  
   [out] mdTypeDef         *pClass,   
   [out] LPCWSTR           szProperty,   
   [in]  ULONG             cchProperty,   
   [out] ULONG             *pchProperty,   
   [out] DWORD             *pdwPropFlags,   
   [out] PCCOR_SIGNATURE   *ppvSig,   
   [out] ULONG             *pbSig,   
   [out] DWORD             *pdwCPlusTypeFlag,   
   [out] UVCP_CONSTANT     *ppDefaultValue,  
   [out] ULONG             *pcchDefaultValue,  
   [out] mdMethodDef       *pmdSetter,   
   [out] mdMethodDef       *pmdGetter,   
   [out] mdMethodDef       rmdOtherMethod[],  
   [in]  ULONG             cMax,   
   [out] ULONG             *pcOtherMethod   
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `prop`  
 [in] Un jeton qui représente la propriété à retourner les métadonnées.  
  
 `pClass`  
 [out] Pointeur vers le jeton TypeDef qui représente le type qui implémente la propriété.  
  
 `szProperty`  
 [out] Une mémoire tampon pour contenir le nom de propriété.  
  
 `cchProperty`  
 [in] La taille en caractères larges de `szProperty`.  
  
 `pchProperty`  
 [out] Le nombre de caractères étendus retournés dans `szProperty`.  
  
 `pdwPropFlags`  
 [out] Pointeur vers les indicateurs d’attribut appliqué à la propriété. Cette valeur est un masque de bits à partir de la [CorPropertyAttr](../../../../docs/framework/unmanaged-api/metadata/corpropertyattr-enumeration.md) énumération.  
  
 `ppvSig`  
 [out] Pointeur vers la signature de métadonnées de la propriété.  
  
 `pbSig`  
 [out] Le nombre d’octets retournés dans `ppvSig`.  
  
 `pdwCPlusTypeFlag`  
 [out] Un indicateur qui spécifie le type de la constante qui est la valeur par défaut de la propriété. Cette valeur provient de l’énumération CorElementType.  
  
 `ppDefaultValue`  
 [out] Un pointeur vers les octets qui stockent la valeur par défaut pour cette propriété.  
  
 `pcchDefaultValue`  
 [out] La taille en caractères larges de `ppDefaultValue`si `pdwCPlusTypeFlag` a la valeur ELEMENT_TYPE_STRING ; sinon, cette valeur n’est pas pertinente. Dans ce cas, la longueur de `ppDefaultValue` est déduit du type spécifié par `pdwCPlusTypeFlag`.  
  
 `pmdSetter`  
 [out] Pointeur vers le jeton MethodDef qui représente la méthode d’accesseur set pour la propriété.  
  
 `pmdGetter`  
 [out] Pointeur vers le jeton MethodDef qui représente la méthode d’accesseur get pour la propriété.  
  
 `rmdOtherMethod`  
 [out] Un tableau de jetons MethodDef représentant des autres méthodes associées à la propriété.  
  
 `cMax`  
 [in] Taille maximale du tableau `rmdOtherMethod`. Si vous ne fournissez pas un tableau suffisamment grand pour contenir toutes les méthodes, ils sont ignorés sans avertissement.  
  
 `pcOtherMethod`  
 [out] Le nombre de jetons MethodDef retournés dans `rmdOtherMethod`.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
