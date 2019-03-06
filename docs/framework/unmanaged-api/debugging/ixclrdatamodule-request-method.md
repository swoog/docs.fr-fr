---
title: IXCLRDataModule::Request (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataModule::Request Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule::Request Method
helpviewer.keywords:
- IXCLRDataModule::Request Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 336e47d531fc880571165cd55f117825cd1a2abb
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57374867"
---
# <a name="ixclrdatamodulerequest-method"></a>IXCLRDataModule::Request (méthode)

Demandes pour remplir la mémoire tampon spécifiée avec les données du module.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>Syntaxe
```
HRESULT Request([in] ULONG32 reqCode,
    [in] ULONG32 inBufferSize,
    [in, size_is(inBufferSize)] BYTE* inBuffer,
    [in] ULONG32 outBufferSize,
    [out, size_is(outBufferSize)] BYTE* outBuffer);
```

### <a name="parameters"></a>Paramètres

`reqCode`\
[in] Type à envoyer de demande.

`inBufferSize`\
[in] taille de la mémoire tampon d’entrée à transmettre.

`inBuffer`\
[in, size_is(inBufferSize)] Pointeur de mémoire tampon pour les données brutes à envoyer dans la demande.

`outBufferSize`\
[in] Taille de la mémoire tampon de sortie.

`outBuffer`\
[out, size_is(outBufferSize)] Pointeur de mémoire tampon utilisée pour stocker la réponse de la demande.

## <a name="remarks"></a>Notes

La méthode fournie fait partie de la `IXCLRDataModule` interface et correspond à l’emplacement 36e de la table de la méthode virtuelle.

## <a name="requirements"></a>Spécifications

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
**En-tête :** Aucun.   
**Bibliothèque :** Aucun.  
**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>Voir aussi
- [Débogage](index.md)
- [Interface de IXCLRDataModule](ixclrdatamodule-interface.md)