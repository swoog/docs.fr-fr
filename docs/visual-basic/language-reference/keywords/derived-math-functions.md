---
title: Fonctions mathématiques dérivées (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- arithmetic operations, derived math functions
- cosecant function
- arcsecant function
- arccotangent function
- functions [Visual Basic], derived math functions
- inverse functions
- math functions, derived
- derived math functions
- cotangent function
- angles
- secant function
- trigonometric functions
- logarithms
- arccosecant function
- hyperbolic functions
- arcsine function
- degrees
- arccosine function
ms.assetid: 63e449d8-9444-44fb-8db1-6d9cf346e2aa
ms.openlocfilehash: 87faa623f5b145eec8b88e350fce4171125324dc
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33596806"
---
# <a name="derived-math-functions-visual-basic"></a>Fonctions mathématiques dérivées (Visual Basic)
Le tableau suivant présente les fonctions mathématiques non intrinsèques qui peuvent être dérivées des fonctions mathématiques intrinsèques de le <xref:System.Math?displayProperty=nameWithType> objet. Vous pouvez accéder à des fonctions mathématiques intrinsèques en ajoutant `Imports System.Math` à votre projet ou un fichier.  
  
|Fonction|Équivalents|  
|--------------|-------------------------|  
|Sécante (Sec(x))|1 / COS (x)|  
|Cosécante (Csc(x))|1 / sin (x)|  
|Cotangente (Ctan(x))|1 / tan (x)|  
|Sinus inverse (Asin(x))|ATAN (x / Sqrt (-x * x + 1))|  
|Cosinus inverse (Acos(x))|ATAN (-x / Sqrt (-x * x + 1)) + 2 \* Atan(1)|  
|Sécante (Asec(x))|2 * Atan(1) – Atan(Sign(x) / Sqrt (x \* x-1))|  
|Cosécante inverse (Acsc(x))|ATAN(Sign(x) / Sqrt (x * x-1))|  
|Cotangente inverse (Acot(x))|2 * Atan(1) - ATAN (x)|  
|Sinus hyperbolique (Sinh(x))|(EXP (x) – Exp(-x)) / 2|  
|Cosinus hyperbolique (Cosh(x))|(EXP (x) + Exp(-x)) / 2|  
|Tangente hyperbolique (TANH|(EXP (x) – Exp(-x)) / (EXP (x) + Exp(-x))|  
|Sécante hyperbolique (Sech(x))|2 / (EXP (x) + Exp(-x))|  
|Cosécante hyperbolique (Csch(x))|2 / (EXP (x) – Exp(-x))|  
|Cotangente hyperbolique (Coth(x))|(EXP (x) + Exp(-x)) / (EXP (x) – Exp(-x))|  
|Sinus hyperbolique inverse (Asinh(x))|Journal (x + Sqrt (x * x + 1))|  
|Cosinus hyperbolique inverse (Acosh(x))|Journal (x + Sqrt (x * x-1))|  
|Tangente hyperbolique inverse (Atanh(x))|Journal ((1 + x) / (1 – x)) / 2|  
|Sécante hyperbolique inverse (AsecH(x))|Journal ((Sqrt (-x * x + 1) + 1) / x)|  
|Cosécante hyperbolique inverse (Acsch(x))|Log((Sign(x) * Sqrt (x \* x + 1) + 1) / x)|  
|Cotangente hyperbolique inverse (Acoth(x))|Journal ((x + 1) / (n-1)) / 2|  
  
## <a name="see-also"></a>Voir aussi  
 [Fonctions mathématiques](../../../visual-basic/language-reference/functions/math-functions.md)
