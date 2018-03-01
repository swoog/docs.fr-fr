---
title: "Analyse de chaînes dans .NET"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- parsing strings, about parsing strings
- IFormatProvider interface, parsing strings
- base types, parsing strings
- Parse method
- parsing strings
ms.assetid: 5e758b41-db93-456b-8999-99b7304b090d
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 9c2193dd1b1f3c0478efb5fc9c2b80250ef1878f
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="parsing-strings-in-net"></a><span data-ttu-id="86976-102">Analyse de chaînes dans .NET</span><span class="sxs-lookup"><span data-stu-id="86976-102">Parsing Strings in .NET</span></span>
<span data-ttu-id="86976-103">Une opération d’analyse convertit une chaîne qui représente un type de base .NET en ce type de base.</span><span class="sxs-lookup"><span data-stu-id="86976-103">A parsing operation converts a string that represents a .NET base type into that base type.</span></span> <span data-ttu-id="86976-104">Par exemple, une opération d'analyse permet de convertir une chaîne en nombre à virgule flottante ou en valeur de date et d'heure.</span><span class="sxs-lookup"><span data-stu-id="86976-104">For example, a parsing operation is used to convert a string to a floating-point number or to a date and time value.</span></span> <span data-ttu-id="86976-105">La méthode la plus couramment utilisée pour effectuer une opération d’analyse est la méthode `Parse`.</span><span class="sxs-lookup"><span data-stu-id="86976-105">The method most commonly used to perform a parsing operation is the `Parse` method.</span></span> <span data-ttu-id="86976-106">Étant donné que l’analyse est l’opération inverse de la mise en forme (qui consiste à convertir un type de base en sa représentation sous forme de chaîne), de nombreuses règles et conventions identiques s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="86976-106">Because parsing is the reverse operation of formatting (which involves converting a base type into its string representation), many of the same rules and conventions apply.</span></span> <span data-ttu-id="86976-107">Tout comme la mise en forme utilise un objet qui implémente l’interface <xref:System.IFormatProvider> pour fournir des informations de mise en forme dépendantes de la culture, l’analyse utilise un objet qui implémente l’interface <xref:System.IFormatProvider> pour déterminer comment interpréter une représentation sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="86976-107">Just as formatting uses an object that implements the <xref:System.IFormatProvider> interface to provide culture-sensitive formatting information, parsing also uses an object that implements the <xref:System.IFormatProvider> interface to determine how to interpret a string representation.</span></span> <span data-ttu-id="86976-108">Pour plus d’informations, consultez [Mise en forme des types](../../../docs/standard/base-types/formatting-types.md).</span><span class="sxs-lookup"><span data-stu-id="86976-108">For more information, see [Formatting Types](../../../docs/standard/base-types/formatting-types.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="86976-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="86976-109">In This Section</span></span>  
 [<span data-ttu-id="86976-110">Analyse de chaînes numériques</span><span class="sxs-lookup"><span data-stu-id="86976-110">Parsing Numeric Strings</span></span>](../../../docs/standard/base-types/parsing-numeric.md)  
 <span data-ttu-id="86976-111">Explique comment convertir des chaînes en types numériques .NET.</span><span class="sxs-lookup"><span data-stu-id="86976-111">Describes how to convert strings into .NET numeric types.</span></span>  
  
 [<span data-ttu-id="86976-112">Analyse de chaînes de date et d’heure</span><span class="sxs-lookup"><span data-stu-id="86976-112">Parsing Date and Time Strings</span></span>](../../../docs/standard/base-types/parsing-datetime.md)  
 <span data-ttu-id="86976-113">Explique comment convertir des chaînes en types **DateTime** .NET.</span><span class="sxs-lookup"><span data-stu-id="86976-113">Describes how to convert strings into .NET **DateTime** types.</span></span>  
  
 [<span data-ttu-id="86976-114">Analyse d’autres chaînes</span><span class="sxs-lookup"><span data-stu-id="86976-114">Parsing Other Strings</span></span>](../../../docs/standard/base-types/parsing-other.md)  
 <span data-ttu-id="86976-115">Explique comment convertir des chaînes en types **Char**, **Boolean** et **Enum**.</span><span class="sxs-lookup"><span data-stu-id="86976-115">Describes how to convert strings into **Char**, **Boolean**, and **Enum** types.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="86976-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="86976-116">Related Sections</span></span>  
 [<span data-ttu-id="86976-117">Mise en forme des types</span><span class="sxs-lookup"><span data-stu-id="86976-117">Formatting Types</span></span>](../../../docs/standard/base-types/formatting-types.md)  
 <span data-ttu-id="86976-118">Décrit les concepts de mise en forme de base, tels que les spécificateurs de format et les fournisseurs de format.</span><span class="sxs-lookup"><span data-stu-id="86976-118">Describes basic formatting concepts like format specifiers and format providers.</span></span>  
  
 [<span data-ttu-id="86976-119">Conversion de type dans .NET</span><span class="sxs-lookup"><span data-stu-id="86976-119">Type Conversion in .NET</span></span>](../../../docs/standard/base-types/type-conversion.md)  
 <span data-ttu-id="86976-120">Décrit comment convertir des types.</span><span class="sxs-lookup"><span data-stu-id="86976-120">Describes how to convert types.</span></span>  
  
 [<span data-ttu-id="86976-121">Types de base</span><span class="sxs-lookup"><span data-stu-id="86976-121">Base Types</span></span>](../../../docs/standard/base-types/index.md)  
 <span data-ttu-id="86976-122">Décrit les opérations courantes que vous pouvez effectuer sur les types de base .NET.</span><span class="sxs-lookup"><span data-stu-id="86976-122">Describes common operations that you can perform on .NET base types.</span></span>
