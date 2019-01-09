---
title: SqlStreamChars.Write (Char [], Int32, Int32), méthode (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.Write
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: e8c8ee7ab7a744c1a1d18212f1c7f9788c91ea0d
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152572"
---
# <a name="sqlstreamcharswritechar-int32-int32-method"></a>Méthode de SqlStreamChars.Write (Char [], Int32, Int32)

En cas de substitution dans une classe dérivée, écrit une séquence de caractères dans le flux actuel et avance la position actuelle dans ce flux du nombre de caractères écrits. L’assembly qui contient cette méthode a une relation de friend avec SQLAccess.dll. Il est prévu pour une utilisation par SQL Server. Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.

```csharp
public abstract void Write (char[] buffer, int offset, int count);
```

## <a name="parameters"></a>Paramètres

`buffer`  
Un tableau de caractères à écrire.

`offset`  
Un décalage relatif à l’origine.

`count`  
Le nombre de caractères à écrire dans le flux actuel.

## <a name="remarks"></a>Notes

> [!WARNING]
> Le `SqlStreamChars.Write` méthode est privée et qu’il n’est pas destiné à être utilisé directement dans votre code.
>
> Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.

## <a name="requirements"></a>Spécifications

**Espace de noms :** <xref:System.Data.SqlTypes>

**Assembly :** System.Data (dans System.Data.dll)

**Versions du .NET framework :** Disponible à partir de 2.0.