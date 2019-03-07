---
title: IMetaDataImport::EnumMethodSemantics, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumMethodSemantics
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumMethodSemantics
helpviewer_keywords:
- EnumMethodSemantics method [.NET Framework metadata]
- IMetaDataImport::EnumMethodSemantics method [.NET Framework metadata]
ms.assetid: e7e3c630-9691-46d6-94df-b5593a7bb08a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6021cd0126f4dd85b796a3110cd95a83c0f77ff4
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57466789"
---
# <a name="imetadataimportenummethodsemantics-method"></a>IMetaDataImport::EnumMethodSemantics, méthode
Énumère les propriétés et les événements de modification de propriétés auxquels la méthode spécifiée est associée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumMethodSemantics (  
   [in, out] HCORENUM    *phEnum,  
   [in]  mdMethodDef     mb,   
   [out] mdToken         rEventProp[],  
   [in]  ULONG           cMax,  
   [out] ULONG           *pcEventProp  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `phEnum`  
 [in, out] Pointeur vers l’énumérateur. Cela doit être NULL pour le premier appel de cette méthode.  
  
 `mb`  
 [in] Jeton MethodDef qui limite l’étendue de l’énumération.  
  
 `rEventProp`  
 [out] Tableau utilisé pour stocker les événements ou les propriétés.  
  
 `cMax`  
 [in] Taille maximale du tableau `rEventProp`.  
  
 `pcEventProp`  
 [out] Le nombre d’événements ou les propriétés retournées dans `rEventProp`.  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|`S_OK`|`EnumMethodSemantics` retourné avec succès.|  
|`S_FALSE`|Il n’existe aucun événements ou propriétés à énumérer. Dans ce cas, `pcEventProp` est égal à zéro.|  
  
## <a name="remarks"></a>Notes  
 Définissent de nombreux types common language runtime *propriété* `Changed` événements et `On` *propriété* `Changed` méthodes liées à leurs propriétés. Par exemple, le <xref:System.Windows.Forms.Control?displayProperty=nameWithType> type définit un <xref:System.Windows.Forms.Control.Font%2A> propriété, un <xref:System.Windows.Forms.Control.FontChanged> événement et un <xref:System.Windows.Forms.Control.OnFontChanged%2A> (méthode). La méthode d’accesseur set de la <xref:System.Windows.Forms.Control.Font%2A> les appels de propriété <xref:System.Windows.Forms.Control.OnFontChanged%2A> (méthode), qui à son tour déclenche le <xref:System.Windows.Forms.Control.FontChanged> événement. Vous appelleriez `EnumMethodSemantics` à l’aide de le MethodDef pour <xref:System.Windows.Forms.Control.OnFontChanged%2A> pour obtenir des références à la <xref:System.Windows.Forms.Control.Font%2A> propriété et le <xref:System.Windows.Forms.Control.FontChanged> événement.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
