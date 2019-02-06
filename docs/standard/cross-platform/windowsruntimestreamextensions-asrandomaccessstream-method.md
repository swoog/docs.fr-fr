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
ms.openlocfilehash: d5dd2829a9a00f869af3d7f370f99361979b8106
ms.sourcegitcommit: 01ea420eaa4bf76d5fc47673294c8881379b3369
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2019
ms.locfileid: "55758792"
---
# <a name="windowsruntimestreamextensionsasrandomaccessstreamsystemiostream-method"></a><span data-ttu-id="1264f-102">WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream), méthode</span><span class="sxs-lookup"><span data-stu-id="1264f-102">WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream) Method</span></span>

<span data-ttu-id="1264f-103">[Pris en charge dans le .NET Framework 4.5.1 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="1264f-103">[Supported in the .NET Framework 4.5.1 and later versions]</span></span>

<span data-ttu-id="1264f-104">Convertit le flux spécifié en flux d'accès aléatoire.</span><span class="sxs-lookup"><span data-stu-id="1264f-104">Converts the specified stream to a random access stream.</span></span>

<span data-ttu-id="1264f-105">**Espace de noms :** <xref:System.IO?displayProperty=nameWithType>
**Assembly :** System.Runtime.WindowsRuntime (in System.Runtime.WindowsRuntime.dll)</span><span class="sxs-lookup"><span data-stu-id="1264f-105">**Namespace:** <xref:System.IO?displayProperty=nameWithType>
**Assembly:** System.Runtime.WindowsRuntime (in System.Runtime.WindowsRuntime.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1264f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1264f-106">Syntax</span></span>

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

## <a name="parameters"></a><span data-ttu-id="1264f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1264f-107">Parameters</span></span>

`stream`

<span data-ttu-id="1264f-108">Type : <xref:System.IO.Stream?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="1264f-108">Type: <xref:System.IO.Stream?displayProperty=nameWithType></span></span>  
<span data-ttu-id="1264f-109">Flux à convertir.</span><span class="sxs-lookup"><span data-stu-id="1264f-109">The stream to convert.</span></span>

## <a name="return-value"></a><span data-ttu-id="1264f-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1264f-110">Return Value</span></span>

<span data-ttu-id="1264f-111">Type : <xref:Windows.Storage.Streams.RandomAccessStream></span><span class="sxs-lookup"><span data-stu-id="1264f-111">Type: <xref:Windows.Storage.Streams.RandomAccessStream></span></span>  
<span data-ttu-id="1264f-112">Un [!INCLUDE[wrt](../../../includes/wrt-md.md)] flux d’accès aléatoire, qui représente le flux converti.</span><span class="sxs-lookup"><span data-stu-id="1264f-112">A [!INCLUDE[wrt](../../../includes/wrt-md.md)] random access stream, which represents the converted stream.</span></span>

## <a name="exceptions"></a><span data-ttu-id="1264f-113">Exceptions</span><span class="sxs-lookup"><span data-stu-id="1264f-113">Exceptions</span></span>

|<span data-ttu-id="1264f-114">Exception</span><span class="sxs-lookup"><span data-stu-id="1264f-114">Exception</span></span>|<span data-ttu-id="1264f-115">Condition</span><span class="sxs-lookup"><span data-stu-id="1264f-115">Condition</span></span>|
|---------------|---------------|
|<xref:System.NotSupportedException>|<span data-ttu-id="1264f-116">Le flux à convertir ne prend pas en charge la recherche.</span><span class="sxs-lookup"><span data-stu-id="1264f-116">The stream to convert does not support seeking.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1264f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1264f-117">Remarks</span></span>

<span data-ttu-id="1264f-118">Cette méthode d'extension est disponible uniquement lorsque vous développez des applications Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1264f-118">This extension method is available only when you develop Windows Store apps.</span></span> <span data-ttu-id="1264f-119">Cette méthode offre un moyen pratique de travailler avec des flux dans les applications Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1264f-119">This method provides a convenient way of working with streams in Windows Store apps.</span></span> <span data-ttu-id="1264f-120">Le flux .NET Framework à convertir doit prendre en charge la recherche.</span><span class="sxs-lookup"><span data-stu-id="1264f-120">The .NET Framework stream you want to convert must support seeking.</span></span> <span data-ttu-id="1264f-121">Pour plus d'informations, voir la méthode <xref:System.IO.Stream.Seek%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="1264f-121">For more information, see the <xref:System.IO.Stream.Seek%2A?displayProperty=nameWithType> method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1264f-122">Cette API est prise en charge dans le .NET Framework 4.5.1 et versions ultérieures, mais pas dans la version 4.5.</span><span class="sxs-lookup"><span data-stu-id="1264f-122">This API is supported in the .NET Framework 4.5.1 and later versions, but not in version 4.5.</span></span>

## <a name="version-information"></a><span data-ttu-id="1264f-123">Informations sur la version</span><span class="sxs-lookup"><span data-stu-id="1264f-123">Version Information</span></span>

<span data-ttu-id="1264f-124">**.NET pour les applications du Windows Store**</span><span class="sxs-lookup"><span data-stu-id="1264f-124">**.NET for Windows Store apps**</span></span>

<span data-ttu-id="1264f-125">Pris en charge dans : {0}, {1} Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1264f-125">Supported in: Windows 8.1</span></span>

## <a name="see-also"></a><span data-ttu-id="1264f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1264f-126">See also</span></span>

- [<span data-ttu-id="1264f-127">Guide pratique pour effectuer une conversion entre les flux du .NET Framework et les flux Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="1264f-127">How to: Convert Between .NET Framework Streams and Windows Runtime Streams</span></span>](../io/how-to-convert-between-dotnet-streams-and-winrt-streams.md)
