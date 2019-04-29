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
ms.openlocfilehash: 642ca16142bdfe78a40ddf4e6a3a79ce6a8a4985
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61938747"
---
# <a name="xamlname-grammar"></a>XamlName, grammaire
XamlName, grammaire est une syntaxe spécifique qui est définie dans la spécification du langage XAML [MS-XAML], qui est reproduite ici par commodité.  
  
## <a name="from-the-xaml-specification"></a>À partir de la spécification de XAML  
 La spécification [MS-XAML] définit la grammaire XamlName pour identifier le jeu d’identificateurs symboliques légaux utilisé pour les types et les propriétés.  
  
 Valeurs de chaîne qui sont de type que XamlName doivent se conformer à la grammaire suivante :  
  
```  
XamlName ::= NameStartChar ( NameChar )*   
NameStartChar ::= LetterCharacter | '_'   
NameChar ::= NameStartChar | DecimalDigit | CombiningCharacter   
LetterCharacter ::= UnicodeLu | UnicodeLl | UnicodeLo | UnicodeLt | UnicodeNl   
DecimalDigit ::= UnicodeNd   
CombiningCharacter ::= UnicodeMn | UnicodeMc  
```  
  
 Ce qui suppose que les valeurs suivantes de la catégorie générale tel que défini dans la base de données de caractères Unicode  
  
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
  
 XAML définit une deuxième grammaire, DottedXamlName, qui est utilisé pour la propriété et événement qualifiés des références et également pour les membres attachés. Pour plus d’informations, consultez <xref:System.Windows.DependencyProperty> et [vue d’ensemble de XAML (WPF)](../wpf/advanced/xaml-overview-wpf.md).  
  
 Valeurs de chaîne qui sont de type que DottedXamlName doivent se conformer à la grammaire suivante :  
  
```  
DottedXamlName ::= XamlName '.' XamlName  
```  
  
## <a name="remarks"></a>Notes  
 Pour la spécification complète, consultez [ \[MS-XAML\]](https://go.microsoft.com/fwlink/?LinkId=114525).
