---
title: Instructions d’utilisation
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- class library design guidelines [.NET Framework], usage guidelines
ms.assetid: 42215ffa-a099-4a26-b14e-fb2bdb6f95b7
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7bd54a2325c9721ad17943ba663e7ec0c300632e
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/25/2018
ms.locfileid: "42925074"
---
# <a name="usage-guidelines"></a><span data-ttu-id="6b107-102">Instructions d’utilisation</span><span class="sxs-lookup"><span data-stu-id="6b107-102">Usage guidelines</span></span>

<span data-ttu-id="6b107-103">Cette section contient des instructions sur l’utilisation de types courants dans les API accessible publiquement.</span><span class="sxs-lookup"><span data-stu-id="6b107-103">This section contains guidelines for using common types in publicly accessible APIs.</span></span> <span data-ttu-id="6b107-104">Il porte sur l’utilisation directe de types de Framework (par exemple, les attributs de sérialisation) et de la surcharge des opérateurs courants intégrés.</span><span class="sxs-lookup"><span data-stu-id="6b107-104">It deals with direct usage of built-in Framework types (e.g., serialization attributes) and overloading common operators.</span></span>
  
<span data-ttu-id="6b107-105">Le <xref:System.IDisposable?displayProperty=nameWithType> interface n’est pas couverte dans cette section, mais est abordée dans le [modèle Dispose](../../../docs/standard/design-guidelines/dispose-pattern.md) section.</span><span class="sxs-lookup"><span data-stu-id="6b107-105">The <xref:System.IDisposable?displayProperty=nameWithType> interface is not covered in this section, but is discussed in the [Dispose Pattern](../../../docs/standard/design-guidelines/dispose-pattern.md) section.</span></span>

> [!NOTE]
> <span data-ttu-id="6b107-106">Pour les instructions et informations supplémentaires sur les autres commun, les types intégrés .NET Framework, consultez les rubriques de référence pour les éléments suivants : <xref:System.DateTime?displayProperty=nameWithType>, <xref:System.DateTimeOffset?displayProperty=nameWithType>, <xref:System.ICloneable?displayProperty=nameWithType>, <xref:System.IComparable%601?displayProperty=nameWithType>, <xref:System.IEquatable%601?displayProperty=nameWithType>, <xref:System.Nullable%601?displayProperty=nameWithType>, <xref:System.Object?displayProperty=nameWithType> , <xref:System.Uri?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="6b107-106">For guidelines and additional information about about other common, built-in .NET Framework types, see the reference topics for the following: <xref:System.DateTime?displayProperty=nameWithType>, <xref:System.DateTimeOffset?displayProperty=nameWithType>, <xref:System.ICloneable?displayProperty=nameWithType>, <xref:System.IComparable%601?displayProperty=nameWithType>, <xref:System.IEquatable%601?displayProperty=nameWithType>, <xref:System.Nullable%601?displayProperty=nameWithType>, <xref:System.Object?displayProperty=nameWithType>, <xref:System.Uri?displayProperty=nameWithType>.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6b107-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="6b107-107">In this section</span></span>

[<span data-ttu-id="6b107-108">Tableaux</span><span class="sxs-lookup"><span data-stu-id="6b107-108">Arrays</span></span>](arrays.md)  
[<span data-ttu-id="6b107-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="6b107-109">Attributes</span></span>](attributes.md)  
[<span data-ttu-id="6b107-110">Collections</span><span class="sxs-lookup"><span data-stu-id="6b107-110">Collections</span></span>](guidelines-for-collections.md)  
[<span data-ttu-id="6b107-111">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="6b107-111">Serialization</span></span>](serialization.md)  
[<span data-ttu-id="6b107-112">System.Xml, utilisation</span><span class="sxs-lookup"><span data-stu-id="6b107-112">System.Xml Usage</span></span>](system-xml-usage.md)  
[<span data-ttu-id="6b107-113">Opérateurs d’égalité</span><span class="sxs-lookup"><span data-stu-id="6b107-113">Equality Operators</span></span>](equality-operators.md)  

<span data-ttu-id="6b107-114">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="6b107-114">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

<span data-ttu-id="6b107-115">*Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="6b107-115">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6b107-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b107-116">See also</span></span>

[<span data-ttu-id="6b107-117">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="6b107-117">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
