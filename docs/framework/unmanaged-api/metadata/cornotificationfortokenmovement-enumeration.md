---
title: CorNotificationForTokenMovement, énumération
ms.date: 03/30/2017
api_name:
- CorNotificationForTokenMovement
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorNotificationForTokenMovement
helpviewer_keywords:
- CorNotificationForTokenMovement enumeration [.NET Framework metadata]
ms.assetid: 1edd1670-976a-4fc8-bef7-7c41e60ad989
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 15c5e8b34f2748868611bd7dc47ef73c491b1338
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59189428"
---
# <a name="cornotificationfortokenmovement-enumeration"></a>CorNotificationForTokenMovement, énumération
Spécifie les notifications qui seront envoyées au client d’API de métadonnées lorsqu’un remappage de jeton se produit.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorNotificationForTokenMovement {  
  
    MDNotifyDefault             = 0x0000000f,  
    MDNotifyAll                 = 0xffffffff,  
    MDNotifyNone                = 0x00000000,  
    MDNotifyMethodDef           = 0x00000001,  
    MDNotifyMemberRef           = 0x00000002,  
    MDNotifyFieldDef            = 0x00000004,  
    MDNotifyTypeRef             = 0x00000008,  
  
    MDNotifyTypeDef             = 0x00000010,  
    MDNotifyParamDef            = 0x00000020,  
    MDNotifyInterfaceImpl       = 0x00000040,  
    MDNotifyProperty            = 0x00000080,  
    MDNotifyEvent               = 0x00000100,  
    MDNotifySignature           = 0x00000200,  
    MDNotifyTypeSpec            = 0x00000400,  
    MDNotifyCustomAttribute     = 0x00000800,  
    MDNotifySecurityValue       = 0x00001000,  
    MDNotifyPermission          = 0x00002000,  
    MDNotifyModuleRef           = 0x00004000,  
  
    MDNotifyNameSpace           = 0x00008000,  
  
    MDNotifyAssemblyRef         = 0x01000000,  
    MDNotifyFile                = 0x02000000,  
    MDNotifyExportedType        = 0x04000000,  
    MDNotifyResource            = 0x08000000  
  
} CorNotificationForTokenMovement;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`MDNotifyDefault`|Notifier quand `mdTypeRef`, `mdMethodDef`, `mdMemberRef`, ou `mdFieldDef` déplacement de jetons.|  
|`MDNotifyAll`|Notifier lorsque n’importe quel jeton se déplace.|  
|`MDNotifyNone`|Ne pas avertir lorsque le déplacement des jetons.|  
|`MDNotifyMethodDef`|Notifier quand un `mdMethodDef` se déplace du jeton.|  
|`MDNotifyMemberRef`|Notifier quand un `mdMemberRef` se déplace du jeton.|  
|`MDNotifyFieldDef`|Notifier quand un `mdFieldDef` se déplace du jeton.|  
|`MDNotifyTypeRef`|Notifier quand un `mdTypeRef` se déplace du jeton.|  
|`MDNotifyTypeDef`|Notifier quand un `mdTypeDef` se déplace du jeton.|  
|`MDNotifyParamDef`|Notifier quand un `mdParamDef` se déplace du jeton.|  
|`MDNotifyInterfaceImpl`|Notifier quand un `mdInterfaceImpl` se déplace du jeton.|  
|`MDNotifyProperty`|Notifier quand un `mdProperty` se déplace du jeton.|  
|`MDNotifyEvent`|Notifier quand un `mdEvent` se déplace du jeton.|  
|`MDNotifySignature`|Notifier quand un `mdSignature` se déplace du jeton.|  
|`MDNotifyTypeSpec`|Notifier quand un `mdTypeSpec` se déplace du jeton.|  
|`MDNotifyCustomAttribute`|Notifier quand un `mdCustomAttribute` se déplace du jeton.|  
|`MDNotifySecurityValue`|Notifier quand un `mdSecurityValue` se déplace du jeton.|  
|`MDNotifyPermission`|Notifier quand un `mdPermission` se déplace du jeton.|  
|`MDNotifyModuleRef`|Notifier quand un `mdModuleRef` se déplace du jeton.|  
|`MDNotifyNameSpace`|Notifier quand un `mdNameSpace` se déplace du jeton.|  
|`MDNotifyAssemblyRef`|Notifier quand un `mdAssemblyRef` se déplace du jeton.|  
|`MDNotifyFile`|Notifier quand un `mdFile` se déplace du jeton.|  
|`MDNotifyExportedType`|Notifier quand un `mdExportedType` se déplace du jeton.|  
|`MDNotifyResource`|Notifier quand un `mdManifestResource` se déplace du jeton.|  
  
## <a name="remarks"></a>Notes  
 Un jeton peut être re-mappé (autrement dit, déplacé) pendant une fusion des métadonnées.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorHdr.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
