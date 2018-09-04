---
title: XamlName, grammaire
ms.date: 03/30/2017
helpviewer_keywords:
- DottedXamlName grammar [XAML Services]
- grammar [XAML Services], DottedXamlName
- grammar [XAML Services], XamlName
- names in XAML [XAML Services]
- XamlName grammar [XAML Services]
ms.assetid: 11e4cada-41d2-494d-9531-0d3df4dfcbe3
ms.openlocfilehash: 2a934316517047da6b6aec8e88026024b9a25f65
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43514799"
---
# <a name="xamlname-grammar"></a><span data-ttu-id="7ed5a-102">XamlName, grammaire</span><span class="sxs-lookup"><span data-stu-id="7ed5a-102">XamlName Grammar</span></span>
<span data-ttu-id="7ed5a-103">XamlName, grammaire est une syntaxe spécifique qui est définie dans la spécification du langage XAML [MS-XAML], qui est reproduite ici par commodité.</span><span class="sxs-lookup"><span data-stu-id="7ed5a-103">XamlName Grammar is a specific grammar that is defined in the XAML language specification [MS-XAML], which is reproduced here for convenience.</span></span>  
  
## <a name="from-the-xaml-specification"></a><span data-ttu-id="7ed5a-104">À partir de la spécification de XAML</span><span class="sxs-lookup"><span data-stu-id="7ed5a-104">From the XAML Specification</span></span>  
 <span data-ttu-id="7ed5a-105">La spécification [MS-XAML] définit la grammaire XamlName pour identifier le jeu d’identificateurs symboliques légaux utilisé pour les types et les propriétés.</span><span class="sxs-lookup"><span data-stu-id="7ed5a-105">The [MS-XAML] specification defines the grammar XamlName to identify the set of legal symbolic identifiers used for types and properties.</span></span>  
  
 <span data-ttu-id="7ed5a-106">Valeurs de chaîne qui sont de type que XamlName doivent se conformer à la grammaire suivante :</span><span class="sxs-lookup"><span data-stu-id="7ed5a-106">String values that are of type XamlName must conform to the following grammar:</span></span>  
  
```  
XamlName ::= NameStartChar ( NameChar )*   
NameStartChar ::= LetterCharacter | '_'   
NameChar ::= NameStartChar | DecimalDigit | CombiningCharacter   
LetterCharacter ::= UnicodeLu | UnicodeLl | UnicodeLo | UnicodeLt | UnicodeNl   
DecimalDigit ::= UnicodeNd   
CombiningCharacter ::= UnicodeMn | UnicodeMc  
```  
  
 <span data-ttu-id="7ed5a-107">Ce qui suppose que les valeurs suivantes de la catégorie générale tel que défini dans la base de données de caractères Unicode</span><span class="sxs-lookup"><span data-stu-id="7ed5a-107">Which assumes the following general category values as defined in the Unicode Character Database</span></span>  
  
```  
Lu  
Letter, Uppercase  
Ll  
Letter, Lowercase  
Lt  
Letter, Titlecase  
Lm  
Letter, Modifier  
Lo  
Letter, Other  
Mn  
Mark, Non-Spacing  
Mc  
Mark, Spacing Combining  
Nd  
Number, Decimal  
Nl  
Number, Letter  
```  
  
 <span data-ttu-id="7ed5a-108">XAML définit une deuxième grammaire, DottedXamlName, qui est utilisé pour la propriété et événement qualifiés des références et également pour les membres attachés.</span><span class="sxs-lookup"><span data-stu-id="7ed5a-108">XAML defines a second grammar, DottedXamlName, that is used for property and event qualified references, and also for attached members.</span></span> <span data-ttu-id="7ed5a-109">Pour plus d’informations, consultez <xref:System.Windows.DependencyProperty> et [vue d’ensemble de XAML (WPF)](../../../docs/framework/wpf/advanced/xaml-overview-wpf.md).</span><span class="sxs-lookup"><span data-stu-id="7ed5a-109">For more information, see <xref:System.Windows.DependencyProperty> and [XAML Overview (WPF)](../../../docs/framework/wpf/advanced/xaml-overview-wpf.md).</span></span>  
  
 <span data-ttu-id="7ed5a-110">Valeurs de chaîne qui sont de type que DottedXamlName doivent se conformer à la grammaire suivante :</span><span class="sxs-lookup"><span data-stu-id="7ed5a-110">String values that are of type DottedXamlName must conform to the following grammar:</span></span>  
  
```  
DottedXamlName ::= XamlName '.' XamlName  
```  
  
## <a name="remarks"></a><span data-ttu-id="7ed5a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7ed5a-111">Remarks</span></span>  
 <span data-ttu-id="7ed5a-112">Pour la spécification complète, consultez [ \[MS-XAML\]](https://go.microsoft.com/fwlink/?LinkId=114525).</span><span class="sxs-lookup"><span data-stu-id="7ed5a-112">For the complete specification, see [\[MS-XAML\]](https://go.microsoft.com/fwlink/?LinkId=114525).</span></span>
