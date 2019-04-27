---
title: Propriété SqlStreamChars.IsNull (System.Data.SqlTypes)
author: stevestein
ms.author: sstein
ms.date: 12/19/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.IsNull
- System.Data.SqlTypes.SqlStreamChars.get_IsNull
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: ec00b0afa1597c3ae6488c12fe5a0667dad70e2d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61675219"
---
# <a name="sqlstreamcharsisnull-property"></a>Propriété de SqlStreamChars.IsNull

En cas de substitution dans une classe dérivée, obtient une valeur qui indique si le flux est `null`. L’assembly qui contient cette propriété a une relation de friend avec SQLAccess.dll. Il est prévu pour une utilisation par SQL Server. Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.

## <a name="syntax"></a>Syntaxe

```csharp
public abstract bool IsNull { get; }
```

## <a name="property-value"></a>Valeur de propriété

<xref:System.Boolean>\
`true` Si le flux est `null`; sinon, `false`.

## <a name="remarks"></a>Notes

> [!WARNING]
> Le `SqlStreamChars.IsNull` propriété est privée et qu’il n’est pas destinée à être utilisé directement dans votre code.
>
> Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.

## <a name="requirements"></a>Configuration requise

**Espace de noms :** <xref:System.Data.SqlTypes>

**Assembly :** System.Data (dans System.Data.dll)

**Versions du .NET framework :** Disponible à partir de 2.0.