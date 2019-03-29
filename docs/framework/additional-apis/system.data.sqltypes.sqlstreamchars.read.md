---
title: SqlStreamChars.Read (Char [], Int32, Int32), méthode (System.Data.SqlTypes)
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Read
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: df92acfd4050eb16d3a101b20b9b44560273f4d5
ms.sourcegitcommit: d938c39afb9216db377d0f0ecdaa53936a851059
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58633645"
---
# <a name="sqlstreamcharsreadchar-int32-int32-method"></a>Méthode de SqlStreamChars.Read (Char [], Int32, Int32)

En cas de substitution dans une classe dérivée, lit le jeu de caractères suivant dans le flux d’entrée. L’assembly qui contient cette méthode a une relation de friend avec SQLAccess.dll. Il est prévu pour une utilisation par SQL Server. Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.

```csharp
public abstract int Read (char[] buffer, int offset, int count);
```

## <a name="parameters"></a>Paramètres

`buffer`\
Un tableau de caractères à lire.

`offset`\
Un décalage relatif à l’origine.

`count`\
Le nombre de caractères à lire à partir du flux actuel.

## <a name="returns"></a>Returns (Retours)

<xref:System.Int32>\
Nombre total de caractères lus dans la mémoire tampon.

## <a name="remarks"></a>Notes

> [!WARNING]
> Le `SqlStreamChars.Read` méthode est privée et qu’il n’est pas destiné à être utilisé directement dans votre code.
>
> Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.

## <a name="requirements"></a>Configuration requise

**Espace de noms :** <xref:System.Data.SqlTypes>

**Assembly :** System.Data (dans System.Data.dll)

**Versions du .NET framework :** Disponible à partir de 2.0.