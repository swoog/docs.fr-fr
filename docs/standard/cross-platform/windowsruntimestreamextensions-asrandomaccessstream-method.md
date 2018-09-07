---
title: WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream), méthode
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
api_name:
- System.IO.WindowsRuntimeStreamExtensions.AsRandomAccessStream
api_location:
- System.Runtime.WindowsRuntime.dll
ms.assetid: dcc72283-caed-49ee-b45d-ccaf94e97129
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8935a8c282bbe812ad76ac6d4228c38ab12626a4
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44059649"
---
# <a name="windowsruntimestreamextensionsasrandomaccessstreamsystemiostream-method"></a>WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream), méthode

[Pris en charge dans le .NET Framework 4.5.1 et versions ultérieures]

Convertit le flux spécifié en flux d'accès aléatoire.

**Namespace :** <xref:System.IO?displayProperty=nameWithType> 
 **Assembly :** System.Runtime.WindowsRuntime (dans System.Runtime.WindowsRuntime.dll)

## <a name="syntax"></a>Syntaxe

```csharp
[CLSCompliantAttribute(false)]
public static IRandomAccessStream AsRandomAccessStream(Stream stream)
```

```vb
'Declaration
<ExtensionAttribute> _
<CLSCompliantAttribute(False)> _
Public Shared Function AsRandomAccessStream ( _
        stream As Stream) As IRandomAccessStream
```

## <a name="parameters"></a>Paramètres

`stream`

Type : <xref:System.IO.Stream?displayProperty=nameWithType>  
Flux à convertir.

## <a name="return-value"></a>Valeur de retour

Type : <xref:Windows.Storage.Streams.RandomAccessStream>  
Un [!INCLUDE[wrt](../../../includes/wrt-md.md)] flux d’accès aléatoire, qui représente le flux converti.

## <a name="exceptions"></a>Exceptions

|Exception|Condition|
|---------------|---------------|
|<xref:System.NotSupportedException>|Le flux à convertir ne prend pas en charge la recherche.|

## <a name="remarks"></a>Notes

Cette méthode d'extension est disponible uniquement lorsque vous développez des applications Windows Store. Cette méthode offre un moyen pratique de travailler avec des flux dans les applications Windows Store. Le flux .NET Framework à convertir doit prendre en charge la recherche. Pour plus d'informations, voir la méthode <xref:System.IO.Stream.Seek%2A?displayProperty=nameWithType>.

> [!IMPORTANT]
> Cette API est prise en charge dans le .NET Framework 4.5.1 et versions ultérieures, mais pas dans la version 4.5.

## <a name="version-information"></a>Informations sur la version

**.NET pour les applications du Windows Store**

Prise en charge dans : Windows 8.1

## <a name="see-also"></a>Voir aussi

-[System.IO.WindowsRuntimeStreamExtensions](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions(v=vs.110).aspx)
-[Comment : effectuer une conversion entre les flux .NET Framework et les flux de Runtime de Windows](../io/how-to-convert-between-dotnet-streams-and-winrt-streams.md)
