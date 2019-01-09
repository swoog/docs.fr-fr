---
title: Méthode SqlStreamChars.Close (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.Close
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 893ee729b864d381c4e4686024687f309d15d214
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152652"
---
# <a name="sqlstreamcharsclose-method"></a>SqlStreamChars.Close (méthode)

Ferme le flux actuel et libère toutes les ressources système associées au flux. L’assembly qui contient cette méthode a une relation de friend avec SQLAccess.dll. Il est prévu pour une utilisation par SQL Server. Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.

```csharp
public virtual void Close ();
```

## <a name="remarks"></a>Notes

> [!WARNING]
> Le `SqlStreamChars.Close` méthode est privée et qu’il n’est pas destiné à être utilisé directement dans votre code.
>
> Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.

## <a name="requirements"></a>Spécifications

**Espace de noms :** <xref:System.Data.SqlTypes>

**Assembly :** System.Data (dans System.Data.dll)

**Versions du .NET framework :** Disponible à partir de 2.0.