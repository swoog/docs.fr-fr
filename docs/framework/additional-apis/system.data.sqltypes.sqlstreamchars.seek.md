---
title: Méthode SqlStreamChars.Seek (Int64, SeekOrigin) (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.Seek
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: aab3195ec0d300a7f001f98f2d646c85be939356
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152552"
---
# <a name="sqlstreamcharsseekint64-seekorigin-method"></a>Méthode de SqlStreamChars.Seek (Int64, SeekOrigin)

En cas de remplacement dans une classe dérivée, définit la position dans le flux actuel. L’assembly qui contient cette méthode a une relation de friend avec SQLAccess.dll. Il est prévu pour une utilisation par SQL Server. Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.

```csharp
public abstract long Seek (long offset, System.IO.SeekOrigin origin);
```

## <a name="parameters"></a>Paramètres

`offset`\
Offset d’octet par rapport à `origin`.

`origin`\
Une des valeurs d’énumération qui indique le point de référence à partir de laquelle obtenir la nouvelle position.

## <a name="returns"></a>Returns (Retours)

<xref:System.Int32>\
Nouvelle position dans le flux actuel.

## <a name="remarks"></a>Notes

> [!WARNING]
> Le `SqlStreamChars.Seek` méthode est privée et qu’il n’est pas destiné à être utilisé directement dans votre code.
>
> Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.

## <a name="requirements"></a>Spécifications

**Espace de noms :** <xref:System.Data.SqlTypes>

**Assembly :** System.Data (dans System.Data.dll)

**Versions du .NET framework :** Disponible à partir de 2.0.