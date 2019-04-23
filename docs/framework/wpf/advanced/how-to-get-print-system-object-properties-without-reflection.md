---
title: 'Procédure : Obtenir les propriétés de l’objet de système d’impression sans réflexion'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- PrintSystemObject [WPF], getting properties
ms.assetid: 43560f28-183d-41c1-b9d1-de7c2552273e
ms.openlocfilehash: bb906dafd98e75708764b5f0f009900719f6a475
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59335197"
---
# <a name="how-to-get-print-system-object-properties-without-reflection"></a><span data-ttu-id="56aa8-102">Procédure : Obtenir les propriétés de l’objet de système d’impression sans réflexion</span><span class="sxs-lookup"><span data-stu-id="56aa8-102">How to: Get Print System Object Properties Without Reflection</span></span>
<span data-ttu-id="56aa8-103">À l’aide de la réflexion pour détailler les propriétés (et les types de ces propriétés) sur un objet peut ralentir les performances de l’application.</span><span class="sxs-lookup"><span data-stu-id="56aa8-103">Using reflection to itemize the properties (and the types of those properties) on an object can slow application performance.</span></span> <span data-ttu-id="56aa8-104">Le <xref:System.Printing.IndexedProperties> espace de noms fournit un moyen d’obtenir ces informations à l’aide de la réflexion.</span><span class="sxs-lookup"><span data-stu-id="56aa8-104">The <xref:System.Printing.IndexedProperties> namespace provides a means to getting this information with using reflection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="56aa8-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="56aa8-105">Example</span></span>  
 <span data-ttu-id="56aa8-106">Voici les étapes pour y parvenir.</span><span class="sxs-lookup"><span data-stu-id="56aa8-106">The steps for doing this are as follows.</span></span>  
  
1. <span data-ttu-id="56aa8-107">Créez une instance du type.</span><span class="sxs-lookup"><span data-stu-id="56aa8-107">Create an instance of the type.</span></span> <span data-ttu-id="56aa8-108">Dans l’exemple ci-dessous, le type est le <xref:System.Printing.PrintQueue> type qui est fourni avec Microsoft .NET Framework, mais un code presque identique doit fonctionner pour les types que vous dérivez de <xref:System.Printing.PrintSystemObject>.</span><span class="sxs-lookup"><span data-stu-id="56aa8-108">In the example below, the type is the <xref:System.Printing.PrintQueue> type that ships with Microsoft .NET Framework, but nearly identical code should work for types that you derive from <xref:System.Printing.PrintSystemObject>.</span></span>  
  
2. <span data-ttu-id="56aa8-109">Créer un <xref:System.Printing.IndexedProperties.PrintPropertyDictionary> à partir du type <xref:System.Printing.PrintSystemObject.PropertiesCollection%2A>.</span><span class="sxs-lookup"><span data-stu-id="56aa8-109">Create a <xref:System.Printing.IndexedProperties.PrintPropertyDictionary> from the type's <xref:System.Printing.PrintSystemObject.PropertiesCollection%2A>.</span></span> <span data-ttu-id="56aa8-110">Le <xref:System.Collections.DictionaryEntry.Value%2A> propriété de chaque entrée dans ce dictionnaire est un objet d’un des types dérivés de <xref:System.Printing.IndexedProperties.PrintProperty>.</span><span class="sxs-lookup"><span data-stu-id="56aa8-110">The <xref:System.Collections.DictionaryEntry.Value%2A> property of each entry in this dictionary is an object of one of the types derived from <xref:System.Printing.IndexedProperties.PrintProperty>.</span></span>  
  
3. <span data-ttu-id="56aa8-111">Énumérer les membres du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="56aa8-111">Enumerate the members of the dictionary.</span></span> <span data-ttu-id="56aa8-112">Pour chacun d’eux, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="56aa8-112">For each of them, do the following.</span></span>  
  
4. <span data-ttu-id="56aa8-113">Cast haut de la valeur de chaque entrée à <xref:System.Printing.IndexedProperties.PrintProperty> et utilisez-le pour créer un <xref:System.Printing.IndexedProperties.PrintProperty> objet.</span><span class="sxs-lookup"><span data-stu-id="56aa8-113">Up-cast the value of each entry to <xref:System.Printing.IndexedProperties.PrintProperty> and use it to create a <xref:System.Printing.IndexedProperties.PrintProperty> object.</span></span>  
  
5. <span data-ttu-id="56aa8-114">Obtenir le type de la <xref:System.Printing.IndexedProperties.PrintProperty.Value%2A> de chacune de la <xref:System.Printing.IndexedProperties.PrintProperty> objet.</span><span class="sxs-lookup"><span data-stu-id="56aa8-114">Get the type of the <xref:System.Printing.IndexedProperties.PrintProperty.Value%2A> of each of the <xref:System.Printing.IndexedProperties.PrintProperty> object.</span></span>  
  
 [!code-csharp[GetPrintObjectPropertyTypesWithoutReflection#ShowPropertyTypesWithoutReflection](~/samples/snippets/csharp/VS_Snippets_Wpf/GetPrintObjectPropertyTypesWithoutReflection/CSharp/Program.cs#showpropertytypeswithoutreflection)]
 [!code-vb[GetPrintObjectPropertyTypesWithoutReflection#ShowPropertyTypesWithoutReflection](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GetPrintObjectPropertyTypesWithoutReflection/visualbasic/program.vb#showpropertytypeswithoutreflection)]  
  
## <a name="see-also"></a><span data-ttu-id="56aa8-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56aa8-115">See also</span></span>

- <xref:System.Printing.IndexedProperties.PrintProperty>
- <xref:System.Printing.PrintSystemObject>
- <xref:System.Printing.IndexedProperties>
- <xref:System.Printing.IndexedProperties.PrintPropertyDictionary>
- <xref:System.Printing.LocalPrintServer>
- <xref:System.Printing.PrintQueue>
- <xref:System.Collections.DictionaryEntry>
- [<span data-ttu-id="56aa8-116">Documents dans WPF</span><span class="sxs-lookup"><span data-stu-id="56aa8-116">Documents in WPF</span></span>](documents-in-wpf.md)
- [<span data-ttu-id="56aa8-117">Vue d’ensemble de l’impression</span><span class="sxs-lookup"><span data-stu-id="56aa8-117">Printing Overview</span></span>](printing-overview.md)
