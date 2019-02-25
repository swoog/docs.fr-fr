---
title: Marshaling des types – .NET
description: Découvrez comment .NET marshale vos types en une représentation native.
author: jkoritzinsky
ms.author: jekoritz
ms.date: 01/18/2019
ms.openlocfilehash: 2c62581d34e77f208b7764f955dfa37613615ee4
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "56411390"
---
# <a name="type-marshalling"></a><span data-ttu-id="dceca-103">Marshaling de types</span><span class="sxs-lookup"><span data-stu-id="dceca-103">Type marshalling</span></span>

<span data-ttu-id="dceca-104">Le **marshaling** est le processus qui consiste à transformer les types quand ils doivent naviguer entre du code managé et du code natif.</span><span class="sxs-lookup"><span data-stu-id="dceca-104">**Marshalling** is the process of transforming types when they need to cross between managed and native code.</span></span>

<span data-ttu-id="dceca-105">La raison pour laquelle le marshaling est nécessaire est que les types diffèrent entre le code managé et le code non managé.</span><span class="sxs-lookup"><span data-stu-id="dceca-105">Marshalling is needed because the types in the managed and unmanaged code are different.</span></span> <span data-ttu-id="dceca-106">Dans le code managé, par exemple, vous avez un élément `String`, tandis que dans le monde non managé, les chaînes peuvent être Unicode (« larges »), non-Unicode, terminées par Null, ASCII, etc. Par défaut, le sous-système P/Invoke tente de prendre la bonne décision en fonction du comportement par défaut, décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="dceca-106">In managed code, for instance, you have a `String`, while in the unmanaged world strings can be Unicode ("wide"), non-Unicode, null-terminated, ASCII, etc. By default, the P/Invoke subsystem tries to do the right thing based on the default behavior, described on this article.</span></span> <span data-ttu-id="dceca-107">Toutefois, dans les cas où vous avez besoin de plus de contrôle, vous pouvez employer l’attribut [MarshalAs](xref:System.Runtime.InteropServices.MarshalAsAttribute) pour spécifier le type attendu du côté du code non managé.</span><span class="sxs-lookup"><span data-stu-id="dceca-107">However, for those situations where you need extra control, you can employ the [MarshalAs](xref:System.Runtime.InteropServices.MarshalAsAttribute) attribute to specify what is the expected type on the unmanaged side.</span></span> <span data-ttu-id="dceca-108">Par exemple, pour que la chaîne soit envoyée sous forme de chaîne ANSI terminée par Null, vous pouvez procéder ainsi :</span><span class="sxs-lookup"><span data-stu-id="dceca-108">For instance, if you want the string to be sent as a null-terminated ANSI string, you could do it like this:</span></span>

```csharp
[DllImport("somenativelibrary.dll")]
static extern int MethodA([MarshalAs(UnmanagedType.LPStr)] string parameter);
```

## <a name="default-rules-for-marshalling-common-types"></a><span data-ttu-id="dceca-109">Règles par défaut de marshaling des types courants</span><span class="sxs-lookup"><span data-stu-id="dceca-109">Default rules for marshalling common types</span></span>

<span data-ttu-id="dceca-110">En règle générale, le runtime tente de prendre la bonne décision en matière de marshaling, c’est-à-dire celle qui demande le moins de travail de votre part.</span><span class="sxs-lookup"><span data-stu-id="dceca-110">Generally, the runtime tries to do the "right thing" when marshalling to require the least amount of work from you.</span></span> <span data-ttu-id="dceca-111">Les tableaux suivants indiquent comment chaque type est marshalé par défaut lorsqu’il est utilisé dans un paramètre ou un champ.</span><span class="sxs-lookup"><span data-stu-id="dceca-111">The following tables describe how each type is marshalled by default when used in a parameter or field.</span></span> <span data-ttu-id="dceca-112">Les types de caractères et d’entiers de longueur fixe C99/C ++11 garantissent que le tableau suivant est correct pour toutes les plateformes.</span><span class="sxs-lookup"><span data-stu-id="dceca-112">The C99/C++11 fixed-width integer and character types are used to ensure that the following table is correct for all platforms.</span></span> <span data-ttu-id="dceca-113">Vous pouvez utiliser n’importe quel type natif ayant les mêmes exigence d’alignement et de taille que ces types.</span><span class="sxs-lookup"><span data-stu-id="dceca-113">You can use any native type that has the same alignment and size requirements as these types.</span></span>

<span data-ttu-id="dceca-114">La première table décrit les correspondances de différents types pour lesquels le marshaling P/Invoke et le marshaling des champs sont identiques.</span><span class="sxs-lookup"><span data-stu-id="dceca-114">This first table describes the mappings for various types for whom the marshalling is the same for both P/Invoke and field marshalling.</span></span>

| <span data-ttu-id="dceca-115">Type .NET</span><span class="sxs-lookup"><span data-stu-id="dceca-115">.NET Type</span></span> | <span data-ttu-id="dceca-116">Type natif</span><span class="sxs-lookup"><span data-stu-id="dceca-116">Native Type</span></span>  |
|-----------|-------------------------|
| `byte`    | `uint8_t`               |
| `sbyte`   | `int8_t`                |
| `short`   | `int16_t`               |
| `ushort`  | `uint16_t`              |
| `int`     | `int32_t`               |
| `uint`    | `uint32_t`              |
| `long`    | `int64_t`               |
| `ulong`   | `uint64_t`              |
| `char`    | <span data-ttu-id="dceca-117">`char` ou `char16_t` selon le `CharSet` de P/Invoke ou de la structure.</span><span class="sxs-lookup"><span data-stu-id="dceca-117">Either `char` or `char16_t` depending on the `CharSet` of the P/Invoke or structure.</span></span> <span data-ttu-id="dceca-118">Voir la [documentation charset](/.charset.md).</span><span class="sxs-lookup"><span data-stu-id="dceca-118">See the [charset documentation](/.charset.md).</span></span> |
| `string`  | <span data-ttu-id="dceca-119">`char*` ou `char16_t*` selon le `CharSet` de P/Invoke ou de la structure.</span><span class="sxs-lookup"><span data-stu-id="dceca-119">Either `char*` or `char16_t*` depending on the `CharSet` of the P/Invoke or structure.</span></span> <span data-ttu-id="dceca-120">Voir la [documentation charset](/.charset.md).</span><span class="sxs-lookup"><span data-stu-id="dceca-120">See the [charset documentation](/.charset.md).</span></span> |
| `System.IntPtr` | `intptr_t`        |
| `System.UIntPtr` | `uintptr_t`      |
| <span data-ttu-id="dceca-121">Types pointeur .NET (p. ex.,</span><span class="sxs-lookup"><span data-stu-id="dceca-121">.NET Pointer types (ex.</span></span> <span data-ttu-id="dceca-122">`void*`)</span><span class="sxs-lookup"><span data-stu-id="dceca-122">`void*`)</span></span>  | `void*` |
| <span data-ttu-id="dceca-123">Type dérivé de `System.Runtime.InteropServices.SafeHandle`</span><span class="sxs-lookup"><span data-stu-id="dceca-123">Type derived from `System.Runtime.InteropServices.SafeHandle`</span></span> | `void*` |
| <span data-ttu-id="dceca-124">Type dérivé de `System.Runtime.InteropServices.CriticalHandle`</span><span class="sxs-lookup"><span data-stu-id="dceca-124">Type derived from `System.Runtime.InteropServices.CriticalHandle`</span></span> | `void*`          |
| `bool`    | <span data-ttu-id="dceca-125">Type `BOOL` Win32</span><span class="sxs-lookup"><span data-stu-id="dceca-125">Win32 `BOOL` type</span></span>       |
| `decimal` | <span data-ttu-id="dceca-126">Struct `DECIMAL` COM</span><span class="sxs-lookup"><span data-stu-id="dceca-126">COM `DECIMAL` struct</span></span> |
| <span data-ttu-id="dceca-127">Délégué .NET</span><span class="sxs-lookup"><span data-stu-id="dceca-127">.NET Delegate</span></span> | <span data-ttu-id="dceca-128">Pointeur de fonction natif</span><span class="sxs-lookup"><span data-stu-id="dceca-128">Native function pointer</span></span> |
| `System.DateTime` | <span data-ttu-id="dceca-129">Type `DATE` Win32</span><span class="sxs-lookup"><span data-stu-id="dceca-129">Win32 `DATE` type</span></span> |
| `System.Guid` | <span data-ttu-id="dceca-130">Type `GUID` Win32</span><span class="sxs-lookup"><span data-stu-id="dceca-130">Win32 `GUID` type</span></span> |

<span data-ttu-id="dceca-131">Certaines catégories ont des valeurs par défaut différentes pour le marshaling comme paramètre ou comme structure.</span><span class="sxs-lookup"><span data-stu-id="dceca-131">A few categories of marshalling have different defaults if you're marshalling as a parameter or structure.</span></span>

| <span data-ttu-id="dceca-132">Type .NET</span><span class="sxs-lookup"><span data-stu-id="dceca-132">.NET Type</span></span> | <span data-ttu-id="dceca-133">Type natif (paramètre)</span><span class="sxs-lookup"><span data-stu-id="dceca-133">Native Type (Parameter)</span></span> | <span data-ttu-id="dceca-134">Type natif (champ)</span><span class="sxs-lookup"><span data-stu-id="dceca-134">Native Type (Field)</span></span> |
|-----------|-------------------------|---------------------|
| <span data-ttu-id="dceca-135">Tableau .NET</span><span class="sxs-lookup"><span data-stu-id="dceca-135">.NET array</span></span> | <span data-ttu-id="dceca-136">Pointeur vers le début d’un tableau de représentations natives des éléments du tableau</span><span class="sxs-lookup"><span data-stu-id="dceca-136">A pointer to the start of an array of native representations of the array elements.</span></span> | <span data-ttu-id="dceca-137">Non autorisé sans attribut `[MarshalAs]`</span><span class="sxs-lookup"><span data-stu-id="dceca-137">Not allowed without a `[MarshalAs]` attribute</span></span>|
| <span data-ttu-id="dceca-138">Classe avec `LayoutKind` de `Sequential` ou de `Explicit`</span><span class="sxs-lookup"><span data-stu-id="dceca-138">A class with a `LayoutKind` of `Sequential` or `Explicit`</span></span> | <span data-ttu-id="dceca-139">Pointeur vers la représentation native de la classe</span><span class="sxs-lookup"><span data-stu-id="dceca-139">A pointer to the native representation of the class</span></span> | <span data-ttu-id="dceca-140">Représentation native de la classe</span><span class="sxs-lookup"><span data-stu-id="dceca-140">The native representation of the class</span></span> |

<span data-ttu-id="dceca-141">Le tableau suivant présente les règles de marshaling par défaut propres à Windows.</span><span class="sxs-lookup"><span data-stu-id="dceca-141">The following table includes the default marshalling rules that are Windows-only.</span></span> <span data-ttu-id="dceca-142">Sur les autres plateformes, il n’est pas possible de marshaler ces types.</span><span class="sxs-lookup"><span data-stu-id="dceca-142">On non-Windows platforms, you cannot marshal these types.</span></span>

| <span data-ttu-id="dceca-143">Type .NET</span><span class="sxs-lookup"><span data-stu-id="dceca-143">.NET Type</span></span> | <span data-ttu-id="dceca-144">Type natif (paramètre)</span><span class="sxs-lookup"><span data-stu-id="dceca-144">Native Type (Parameter)</span></span> | <span data-ttu-id="dceca-145">Type natif (champ)</span><span class="sxs-lookup"><span data-stu-id="dceca-145">Native Type (Field)</span></span> |
|-----------|-------------------------|---------------------|
| `object`  | `VARIANT`               | `IUnknown*`         |
| `System.Array` | <span data-ttu-id="dceca-146">Interface COM</span><span class="sxs-lookup"><span data-stu-id="dceca-146">COM interface</span></span> | <span data-ttu-id="dceca-147">Non autorisé sans attribut `[MarshalAs]`</span><span class="sxs-lookup"><span data-stu-id="dceca-147">Not allowed without a `[MarshalAs]` attribute</span></span> |
| `System.ArgIterator` | `va_list` | <span data-ttu-id="dceca-148">Non autorisé</span><span class="sxs-lookup"><span data-stu-id="dceca-148">Not allowed</span></span> |
| `System.Collections.IEnumerator` | `IEnumVARIANT*` | <span data-ttu-id="dceca-149">Non autorisé</span><span class="sxs-lookup"><span data-stu-id="dceca-149">Not allowed</span></span> |
| `System.Collections.IEnumerable` | `IDispatch*` | <span data-ttu-id="dceca-150">Non autorisé</span><span class="sxs-lookup"><span data-stu-id="dceca-150">Not allowed</span></span> |
| `System.DateTimeOffset` | <span data-ttu-id="dceca-151">`int64_t` représentant le nombre de cycles depuis le 1er janvier 1601 à minuit</span><span class="sxs-lookup"><span data-stu-id="dceca-151">`int64_t` representing the number of ticks since midnight on January 1, 1601</span></span> || <span data-ttu-id="dceca-152">`int64_t` représentant le nombre de cycles depuis le 1er janvier 1601 à minuit</span><span class="sxs-lookup"><span data-stu-id="dceca-152">`int64_t` representing the number of ticks since midnight on January 1, 1601</span></span> |

<span data-ttu-id="dceca-153">Certains types ne peuvent être marshalés que comme paramètres, et non comme champs</span><span class="sxs-lookup"><span data-stu-id="dceca-153">Some types can only be marshalled as parameters and not as fields.</span></span> <span data-ttu-id="dceca-154">:</span><span class="sxs-lookup"><span data-stu-id="dceca-154">These types are listed in the following table:</span></span>

| <span data-ttu-id="dceca-155">Type .NET</span><span class="sxs-lookup"><span data-stu-id="dceca-155">.NET Type</span></span> | <span data-ttu-id="dceca-156">Type natif (paramètre uniquement)</span><span class="sxs-lookup"><span data-stu-id="dceca-156">Native Type (Parameter Only)</span></span> |
|-----------|------------------------------|
| `System.Text.StringBuilder` | <span data-ttu-id="dceca-157">`char*` ou `char16_t*` selon le `CharSet` de P/Invoke.</span><span class="sxs-lookup"><span data-stu-id="dceca-157">Either `char*` or `char16_t*` depending on the `CharSet` of the P/Invoke.</span></span>  <span data-ttu-id="dceca-158">Voir la [documentation charset](/.charset.md).</span><span class="sxs-lookup"><span data-stu-id="dceca-158">See the [charset documentation](/.charset.md).</span></span> |
| `System.ArgIterator` | <span data-ttu-id="dceca-159">`va_list` (sur Windows x86/x64/arm64 uniquement)</span><span class="sxs-lookup"><span data-stu-id="dceca-159">`va_list` (on Windows x86/x64/arm64 only)</span></span> |
| `System.Runtime.InteropServices.ArrayWithOffset` | `void*` |
| `System.Runtime.InteropServices.HandleRef` | `void*` |

<span data-ttu-id="dceca-160">Si ces valeurs par défaut ne vous conviennent pas tout à fait, vous pouvez personnaliser la façon dont les paramètres sont marshalés.</span><span class="sxs-lookup"><span data-stu-id="dceca-160">If these defaults don't do exactly what you want, you can customize how parameters are marshalled.</span></span> <span data-ttu-id="dceca-161">L’article [Marshaling des paramètres](customize-parameter-marshalling.md) explique comment faire, pour différents types de paramètres.</span><span class="sxs-lookup"><span data-stu-id="dceca-161">The [parameter marshalling](customize-parameter-marshalling.md) article walks you through how to customize how different parameter types are marshalled.</span></span>

## <a name="marshalling-classes-and-structs"></a><span data-ttu-id="dceca-162">Marshaling de classes et de structures</span><span class="sxs-lookup"><span data-stu-id="dceca-162">Marshalling classes and structs</span></span>

<span data-ttu-id="dceca-163">Un autre aspect du marshaling de types consiste à passer une structure à une méthode non managée.</span><span class="sxs-lookup"><span data-stu-id="dceca-163">Another aspect of type marshalling is how to pass in a struct to an unmanaged method.</span></span> <span data-ttu-id="dceca-164">Par exemple, certaines des méthodes non managées nécessitent une structure comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="dceca-164">For instance, some of the unmanaged methods require a struct as a parameter.</span></span> <span data-ttu-id="dceca-165">Il faut dans ce cas créer une classe ou un struct correspondant dans la partie managée de l’environnement pour l’utiliser comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="dceca-165">In these cases, you need to create a corresponding struct or a class in managed part of the world to use it as a parameter.</span></span> <span data-ttu-id="dceca-166">Toutefois, il ne suffit pas de définir la classe : il est également nécessaire d’indiquer au marshaleur comment mapper des champs de la classe au struct non managé.</span><span class="sxs-lookup"><span data-stu-id="dceca-166">However, just defining the class isn't enough, you also need to instruct the marshaler how to map fields in the class to the unmanaged struct.</span></span> <span data-ttu-id="dceca-167">C’est ici qu’intervient l’attribut `StructLayout`.</span><span class="sxs-lookup"><span data-stu-id="dceca-167">Here the `StructLayout` attribute becomes useful.</span></span>

```csharp
[DllImport("kernel32.dll")]
static extern void GetSystemTime(SystemTime systemTime);

[StructLayout(LayoutKind.Sequential)]
class SystemTime {
    public ushort Year;
    public ushort Month;
    public ushort DayOfWeek;
    public ushort Day;
    public ushort Hour;
    public ushort Minute;
    public ushort Second;
    public ushort Milsecond;
}

public static void Main(string[] args) {
    SystemTime st = new SystemTime();
    GetSystemTime(st);
    Console.WriteLine(st.Year);
}
```

<span data-ttu-id="dceca-168">Le code précédent illustre de manière simple les appels dans la fonction `GetSystemTime()`.</span><span class="sxs-lookup"><span data-stu-id="dceca-168">The previous code shows a simple example of calling into `GetSystemTime()` function.</span></span> <span data-ttu-id="dceca-169">L’élément digne d’intérêt se trouve sur la ligne 4.</span><span class="sxs-lookup"><span data-stu-id="dceca-169">The interesting bit is on line 4.</span></span> <span data-ttu-id="dceca-170">L’attribut spécifie que les champs de la classe doivent être mappés séquentiellement à la structure de l’autre côté (non managé).</span><span class="sxs-lookup"><span data-stu-id="dceca-170">The attribute specifies that the fields of the class should be mapped sequentially to the struct on the other (unmanaged) side.</span></span> <span data-ttu-id="dceca-171">Cela signifie que le nom des champs n’a pas d’importance ; seul leur ordre compte, car il doit correspondre au struct non managé, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="dceca-171">This means that the naming of the fields isn't important, only their order is important, as it needs to correspond to the unmanaged struct, shown in the following example:</span></span>

```c
typedef struct _SYSTEMTIME {
  WORD wYear;
  WORD wMonth;
  WORD wDayOfWeek;
  WORD wDay;
  WORD wHour;
  WORD wMinute;
  WORD wSecond;
  WORD wMilliseconds;
} SYSTEMTIME, *PSYSTEMTIME*;
```

<span data-ttu-id="dceca-172">Il est possible que le marshaling par défaut de votre structure ne vous convienne pas.</span><span class="sxs-lookup"><span data-stu-id="dceca-172">Sometimes the default marshalling for your structure doesn't do what you need.</span></span> <span data-ttu-id="dceca-173">L’article [Personnaliser le marshaling des structures](./customize-struct-marshalling.md) explique comment personnaliser la façon dont les structures sont marshalées.</span><span class="sxs-lookup"><span data-stu-id="dceca-173">The [Customizing structure marshalling](./customize-struct-marshalling.md) article teaches you how to customize how your structure is marshaled.</span></span>
