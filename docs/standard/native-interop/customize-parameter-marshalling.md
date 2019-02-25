---
title: Personnaliser le marshaling des paramètres – .NET
description: Découvrez comment personnaliser la façon dont .NET marshale vos paramètres en une représentation native.
author: jkoritzinsky
ms.author: jekoritz
ms.date: 01/18/2019
ms.openlocfilehash: 7821da546e0ed0ab5fa97d00a638aa5cc1a3089c
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "56411385"
---
# <a name="customizing-parameter-marshalling"></a><span data-ttu-id="3245e-103">Personnaliser le marshaling des paramètres</span><span class="sxs-lookup"><span data-stu-id="3245e-103">Customizing parameter marshalling</span></span>

<span data-ttu-id="3245e-104">Si le comportement de marshaling des paramètres par défaut du runtime .NET ne vous convient pas, vous pouvez utiliser l’attribut <xref:System.Runtime.InteropServices.MarshalAsAttribute?displayProperty=nameWithType> pour le personnaliser.</span><span class="sxs-lookup"><span data-stu-id="3245e-104">When the .NET runtime's default parameter marshalling behavior doesn't do what you want, use can use the <xref:System.Runtime.InteropServices.MarshalAsAttribute?displayProperty=nameWithType> attribute to customize how your parameters are marshaled.</span></span>

## <a name="customizing-string-parameters"></a><span data-ttu-id="3245e-105">Personnaliser des paramètres de chaîne</span><span class="sxs-lookup"><span data-stu-id="3245e-105">Customizing string parameters</span></span>

<span data-ttu-id="3245e-106">.NET propose tout un éventail de formats pour le marshaling des chaînes.</span><span class="sxs-lookup"><span data-stu-id="3245e-106">.NET has a variety of formats for marshalling strings.</span></span> <span data-ttu-id="3245e-107">Ces méthodes sont divisées en deux sections distinctes : les chaînes de style C et les chaînes orientées Windows.</span><span class="sxs-lookup"><span data-stu-id="3245e-107">These methods are split into distinct sections on C-style strings and Windows-centric string formats.</span></span>

### <a name="c-style-strings"></a><span data-ttu-id="3245e-108">Chaînes de style C</span><span class="sxs-lookup"><span data-stu-id="3245e-108">C-Style strings</span></span>

<span data-ttu-id="3245e-109">Chacun de ces formats transmet une chaîne se terminant par Null au code natif.</span><span class="sxs-lookup"><span data-stu-id="3245e-109">Each of these formats passes a null-terminated string to native code.</span></span> <span data-ttu-id="3245e-110">Ils diffèrent par l’encodage de la chaîne native.</span><span class="sxs-lookup"><span data-stu-id="3245e-110">They differ by the encoding of the native string.</span></span>

| <span data-ttu-id="3245e-111">Valeur`System.Runtime.InteropServices.UnmanagedType` </span><span class="sxs-lookup"><span data-stu-id="3245e-111">`System.Runtime.InteropServices.UnmanagedType` value</span></span> | <span data-ttu-id="3245e-112">Encodage</span><span class="sxs-lookup"><span data-stu-id="3245e-112">Encoding</span></span> |
|------------------------------------------------------|----------|
| <span data-ttu-id="3245e-113">LPStr</span><span class="sxs-lookup"><span data-stu-id="3245e-113">LPStr</span></span> | <span data-ttu-id="3245e-114">ANSI</span><span class="sxs-lookup"><span data-stu-id="3245e-114">ANSI</span></span> |
| <span data-ttu-id="3245e-115">LPUTF8Str</span><span class="sxs-lookup"><span data-stu-id="3245e-115">LPUTF8Str</span></span> | <span data-ttu-id="3245e-116">UTF-8</span><span class="sxs-lookup"><span data-stu-id="3245e-116">UTF-8</span></span> | 
| <span data-ttu-id="3245e-117">LPWStr</span><span class="sxs-lookup"><span data-stu-id="3245e-117">LPWStr</span></span> | <span data-ttu-id="3245e-118">UTF-16</span><span class="sxs-lookup"><span data-stu-id="3245e-118">UTF-16</span></span> |

<span data-ttu-id="3245e-119">Le format <xref:System.Runtime.InteropServices.UnmanagedType.VBByRefStr?displayProperty=nameWithType> est légèrement différent.</span><span class="sxs-lookup"><span data-stu-id="3245e-119">The <xref:System.Runtime.InteropServices.UnmanagedType.VBByRefStr?displayProperty=nameWithType> format is slightly different.</span></span> <span data-ttu-id="3245e-120">Comme `LPWStr`, il marshale la chaîne en une chaîne de style C native encodée en UTF-16.</span><span class="sxs-lookup"><span data-stu-id="3245e-120">Like `LPWStr`, it marshals the string to a native C-style string encoded in UTF-16.</span></span> <span data-ttu-id="3245e-121">Toutefois, la signature managée vous fait passer la chaîne en référence ; la signature native correspondante prend la chaîne en valeur.</span><span class="sxs-lookup"><span data-stu-id="3245e-121">However, the managed signature has you pass in the string by reference and the matching native signature takes the string by value.</span></span> <span data-ttu-id="3245e-122">Cette distinction permet d’utiliser une API native qui prend une chaîne en valeur et la modifie sur place sans qu’il soit nécessaire d’utiliser de `StringBuilder`.</span><span class="sxs-lookup"><span data-stu-id="3245e-122">This distinction allows you to use a native API that takes a string by value and modifies it in-place without having to use a `StringBuilder`.</span></span> <span data-ttu-id="3245e-123">Nous vous déconseillons d’utiliser manuellement ce format, dans la mesure où il risque de provoquer une confusion entre les signatures native et managée.</span><span class="sxs-lookup"><span data-stu-id="3245e-123">We recommend against manually using this format since it's prone to cause confusion with the mismatching native and managed signatures.</span></span>

### <a name="windows-centric-string-formats"></a><span data-ttu-id="3245e-124">Formats de chaînes orientées Windows</span><span class="sxs-lookup"><span data-stu-id="3245e-124">Windows-centric string formats</span></span>

<span data-ttu-id="3245e-125">En interagissant avec des interfaces COM ou OLE, vous remarquerez sûrement que les fonctions natives prennent des chaînes comme arguments `BSTR`.</span><span class="sxs-lookup"><span data-stu-id="3245e-125">When interacting with COM or OLE interfaces, you'll likely find that the native functions take strings as `BSTR` arguments.</span></span> <span data-ttu-id="3245e-126">Vous pouvez utiliser le type non managé <xref:System.Runtime.InteropServices.UnmanagedType.BStr?displayProperty=nameWithType> pour marshaler une chaîne comme `BSTR`.</span><span class="sxs-lookup"><span data-stu-id="3245e-126">You can use the <xref:System.Runtime.InteropServices.UnmanagedType.BStr?displayProperty=nameWithType> unmanaged type to marshal a string as a `BSTR`.</span></span>

<span data-ttu-id="3245e-127">Si vous communiquez avec des API WinRT, vous pouvez utiliser le format <xref:System.Runtime.InteropServices.UnmanagedType.HString?displayProperty=nameWithType> pour marshaler une chaîne comme `HSTRING`.</span><span class="sxs-lookup"><span data-stu-id="3245e-127">If you're interacting with WinRT APIs, you can use the <xref:System.Runtime.InteropServices.UnmanagedType.HString?displayProperty=nameWithType> format to marshal a string as an `HSTRING`.</span></span>

## <a name="customizing-array-parameters"></a><span data-ttu-id="3245e-128">Personnaliser des paramètres de tableau</span><span class="sxs-lookup"><span data-stu-id="3245e-128">Customizing array parameters</span></span>

<span data-ttu-id="3245e-129">.NET propose également plusieurs moyens de marshaler des paramètres de tableau.</span><span class="sxs-lookup"><span data-stu-id="3245e-129">.NET also provides you multiple ways to marshal array parameters.</span></span> <span data-ttu-id="3245e-130">Si vous appelez une API qui accepte un tableau de style C, utilisez le type non managé <xref:System.Runtime.InteropServices.UnmanagedType.LPArray?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="3245e-130">If you're calling an API that takes a C-style array, use the <xref:System.Runtime.InteropServices.UnmanagedType.LPArray?displayProperty=nameWithType> unmanaged type.</span></span> <span data-ttu-id="3245e-131">Si les valeurs du tableau exigent un marshaling personnalisé, vous pouvez pour cela utiliser le champ <xref:System.Runtime.InteropServices.MarshalAsAttribute.ArraySubType> sur l’attribut `[MarshalAs]`.</span><span class="sxs-lookup"><span data-stu-id="3245e-131">If the values in the array need customized marshalling, you can use the <xref:System.Runtime.InteropServices.MarshalAsAttribute.ArraySubType> field on the `[MarshalAs]` attribute for that.</span></span>

<span data-ttu-id="3245e-132">Si vous utilisez les API COM, vous devrez probablement marshaler vos paramètres de tableau comme `SAFEARRAY*`.</span><span class="sxs-lookup"><span data-stu-id="3245e-132">If you're using COM APIs, you'll likely have to marshal your array parameters as `SAFEARRAY*`s.</span></span> <span data-ttu-id="3245e-133">Pour cela, vous pouvez utiliser le type non managé <xref:System.Runtime.InteropServices.UnmanagedType.SafeArray?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="3245e-133">To do so, you can use the <xref:System.Runtime.InteropServices.UnmanagedType.SafeArray?displayProperty=nameWithType> unmanaged type.</span></span> <span data-ttu-id="3245e-134">Le type par défaut des éléments de `SAFEARRAY` est présenté dans la table [Personnaliser des champs `object`](./customize-struct-marshalling.md#marshalling-systemobjects).</span><span class="sxs-lookup"><span data-stu-id="3245e-134">The default type of the elements of the `SAFEARRAY` can be seen in the table on [customizing `object` fields](./customize-struct-marshalling.md#marshalling-systemobjects).</span></span> <span data-ttu-id="3245e-135">Vous pouvez utiliser les champs <xref:System.Runtime.InteropServices.MarshalAsAttribute.SafeArraySubType?displayProperty=nameWithType> et <xref:System.Runtime.InteropServices.MarshalAsAttribute.SafeArrayUserDefinedSubType?displayProperty=nameWithType> pour personnaliser précisément le type d’élément de `SAFEARRAY`.</span><span class="sxs-lookup"><span data-stu-id="3245e-135">You can use the <xref:System.Runtime.InteropServices.MarshalAsAttribute.SafeArraySubType?displayProperty=nameWithType> and <xref:System.Runtime.InteropServices.MarshalAsAttribute.SafeArrayUserDefinedSubType?displayProperty=nameWithType> fields to customize the exact element type of the `SAFEARRAY`.</span></span>

## <a name="customizing-boolean-or-decimal-parameters"></a><span data-ttu-id="3245e-136">Personnaliser des paramètres booléens ou décimaux</span><span class="sxs-lookup"><span data-stu-id="3245e-136">Customizing boolean or decimal parameters</span></span>

<span data-ttu-id="3245e-137">Pour plus d’informations sur le marshaling des paramètres booléens ou décimaux, voir [Personnaliser le marshaling des structures](customize-struct-marshalling.md).</span><span class="sxs-lookup"><span data-stu-id="3245e-137">For information on marshalling boolean or decimal parameters, see [Customizing structure marshalling](customize-struct-marshalling.md).</span></span>

## <a name="customizing-object-parameters-windows-only"></a><span data-ttu-id="3245e-138">Personnaliser des paramètres d’objet (Windows uniquement)</span><span class="sxs-lookup"><span data-stu-id="3245e-138">Customizing object parameters (Windows-only)</span></span>

<span data-ttu-id="3245e-139">Sous Windows, le runtime .NET propose plusieurs moyens de marshaler des paramètres d’objet en code natif.</span><span class="sxs-lookup"><span data-stu-id="3245e-139">On Windows, the .NET runtime provides a number of different ways to marshal object parameters to native code.</span></span>

### <a name="marshalling-as-specific-com-interfaces"></a><span data-ttu-id="3245e-140">Marshaling comme interfaces COM spécifiques</span><span class="sxs-lookup"><span data-stu-id="3245e-140">Marshalling as specific COM interfaces</span></span>

<span data-ttu-id="3245e-141">Si votre API accepte un pointeur vers un objet COM, vous pouvez utiliser l’un des formats `UnmanagedType` suivants sur un paramètre de type `object` pour indiquer à .NET de marshaler comme ces interfaces spécifiques :</span><span class="sxs-lookup"><span data-stu-id="3245e-141">If your API takes a pointer to a COM object, you can use any of the following `UnmanagedType` formats on an `object`-typed parameter to tell .NET to marshal as these specific interfaces:</span></span>

- `IUnknown`
- `IDispatch`
- `IInspectable`

<span data-ttu-id="3245e-142">En outre, si votre type est marqué `[ComVisible(true)]` ou que vous marshalez le type `object`, vous pouvez utiliser le format <xref:System.Runtime.InteropServices.UnmanagedType.Interface?displayProperty=nameWithType> pour marshaler votre objet comme wrapper appelable COM pour la vue COM de votre type.</span><span class="sxs-lookup"><span data-stu-id="3245e-142">Additionally, if your type is marked `[ComVisible(true)]` or you're marshalling the `object` type, you can use the <xref:System.Runtime.InteropServices.UnmanagedType.Interface?displayProperty=nameWithType> format to marshal your object as a COM callable wrapper for the COM view of your type.</span></span>

### <a name="marshalling-to-a-variant"></a><span data-ttu-id="3245e-143">Marshaling en `VARIANT`</span><span class="sxs-lookup"><span data-stu-id="3245e-143">Marshalling to a `VARIANT`</span></span>

<span data-ttu-id="3245e-144">Si votre API native accepte une `VARIANT` Win32, vous pouvez utiliser le format <xref:System.Runtime.InteropServices.UnmanagedType.Struct?displayProperty=nameWithType> sur votre `object` paramètre pour marshaler vos objets comme `VARIANT`.</span><span class="sxs-lookup"><span data-stu-id="3245e-144">If your native API takes a Win32 `VARIANT`, you can use the <xref:System.Runtime.InteropServices.UnmanagedType.Struct?displayProperty=nameWithType> format on your `object` parameter to marshal your objects as `VARIANT`s.</span></span> <span data-ttu-id="3245e-145">Pour connaître les correspondances entre les types .NET et les types `VARIANT`, voir la documentation [Personnaliser les champs `object`](customize-struct-marshalling.md#marshalling-systemobjects).</span><span class="sxs-lookup"><span data-stu-id="3245e-145">See the documentation on [customizing `object` fields](customize-struct-marshalling.md#marshalling-systemobjects) for a mapping between .NET types and `VARIANT` types.</span></span>

### <a name="custom-marshalers"></a><span data-ttu-id="3245e-146">Marshaleurs personnalisés</span><span class="sxs-lookup"><span data-stu-id="3245e-146">Custom marshalers</span></span>

<span data-ttu-id="3245e-147">Si vous voulez projeter une interface COM native dans un autre type managé, vous pouvez utiliser le format `UnmanagedType.CustomMarshaler` et une implémentation <xref:System.Runtime.InteropServices.ICustomMarshaler> pour fournir votre propre code de marshaling personnalisé.</span><span class="sxs-lookup"><span data-stu-id="3245e-147">If you want to project a native COM interface into a different managed type, you can use the `UnmanagedType.CustomMarshaler` format and an implementation of <xref:System.Runtime.InteropServices.ICustomMarshaler> to provide your own custom marshalling code.</span></span>