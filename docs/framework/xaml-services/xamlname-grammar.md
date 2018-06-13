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
ms.openlocfilehash: 32fd7b7b952ebbc853e41c0a8276d1ab487e619f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33561889"
---
# <a name="xamlname-grammar"></a><span data-ttu-id="76936-102">XamlName, grammaire</span><span class="sxs-lookup"><span data-stu-id="76936-102">XamlName Grammar</span></span>
<span data-ttu-id="76936-103">XamlName, grammaire est une grammaire spécifique qui est définie dans la spécification du langage XAML [MS-XAML], reproduite ici par commodité.</span><span class="sxs-lookup"><span data-stu-id="76936-103">XamlName Grammar is a specific grammar that is defined in the XAML language specification [MS-XAML], which is reproduced here for convenience.</span></span>  
  
## <a name="from-the-xaml-specification"></a><span data-ttu-id="76936-104">À partir de la spécification de XAML</span><span class="sxs-lookup"><span data-stu-id="76936-104">From the XAML Specification</span></span>  
 <span data-ttu-id="76936-105">La spécification [MS-XAML] définit la grammaire XamlName pour identifier le jeu d’identificateurs symboliques légaux utilisé pour les types et propriétés.</span><span class="sxs-lookup"><span data-stu-id="76936-105">The [MS-XAML] specification defines the grammar XamlName to identify the set of legal symbolic identifiers used for types and properties.</span></span>  
  
 <span data-ttu-id="76936-106">Valeurs de chaîne qui sont de type que XamlName doivent se conformer à la grammaire suivante :</span><span class="sxs-lookup"><span data-stu-id="76936-106">String values that are of type XamlName must conform to the following grammar:</span></span>  
  
```  
XamlName ::= NameStartChar ( NameChar )*   
NameStartChar ::= LetterCharacter | '_'   
NameChar ::= NameStartChar | DecimalDigit | CombiningCharacter   
LetterCharacter ::= UnicodeLu | UnicodeLl | UnicodeLo | UnicodeLt | UnicodeNl   
DecimalDigit ::= UnicodeNd   
CombiningCharacter ::= UnicodeMn | UnicodeMc  
```  
  
 <span data-ttu-id="76936-107">Qui suppose que les valeurs de catégorie générale suivantes comme défini dans la base de données de caractères Unicode</span><span class="sxs-lookup"><span data-stu-id="76936-107">Which assumes the following general category values as defined in the Unicode Character Database</span></span>  
  
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
  
 <span data-ttu-id="76936-108">Code XAML définit une deuxième grammaire, DottedXamlName, qui est utilisé pour la propriété et événement références qualifiées et également pour les membres attachés.</span><span class="sxs-lookup"><span data-stu-id="76936-108">XAML defines a second grammar, DottedXamlName, that is used for property and event qualified references, and also for attached members.</span></span> <span data-ttu-id="76936-109">Pour plus d’informations, consultez <xref:System.Windows.DependencyProperty> et [vue d’ensemble du XAML (WPF)](../../../docs/framework/wpf/advanced/xaml-overview-wpf.md).</span><span class="sxs-lookup"><span data-stu-id="76936-109">For more information, see <xref:System.Windows.DependencyProperty> and [XAML Overview (WPF)](../../../docs/framework/wpf/advanced/xaml-overview-wpf.md).</span></span>  
  
 <span data-ttu-id="76936-110">Valeurs de chaîne qui sont de type que DottedXamlName doivent se conformer à la grammaire suivante :</span><span class="sxs-lookup"><span data-stu-id="76936-110">String values that are of type DottedXamlName must conform to the following grammar:</span></span>  
  
```  
DottedXamlName ::= XamlName '.' XamlName  
```  
  
## <a name="remarks"></a><span data-ttu-id="76936-111">Notes</span><span class="sxs-lookup"><span data-stu-id="76936-111">Remarks</span></span>  
 <span data-ttu-id="76936-112">Pour la spécification complète, consultez [ \[MS-XAML\]](http://go.microsoft.com/fwlink/?LinkId=114525).</span><span class="sxs-lookup"><span data-stu-id="76936-112">For the complete specification, see [\[MS-XAML\]](http://go.microsoft.com/fwlink/?LinkId=114525).</span></span>
