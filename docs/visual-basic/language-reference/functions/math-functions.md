---
title: Fonctions mathématiques (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- math functions, Visual Basic
- arithmetic operations, math functions
- math routines
- Atn function
ms.assetid: 4d2d82e7-6924-42fe-a4a7-b4dd5bebbd0c
ms.openlocfilehash: e5f87a8e367e8c9df65b979fea3781b42ee3ce83
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61801346"
---
# <a name="math-functions-visual-basic"></a>Fonctions mathématiques (Visual Basic)
Les méthodes de la <xref:System.Math?displayProperty=nameWithType> classe fournir trigonométriques, logarithmiques et d’autres fonctions mathématiques courantes.  
  
## <a name="remarks"></a>Notes  
 Le tableau suivant répertorie les méthodes de la <xref:System.Math?displayProperty=nameWithType> classe. Vous pouvez les utiliser dans un programme Visual Basic.  
  
|Méthode .NET|Description|  
|---------------------------|-----------------|  
|<xref:System.Math.Abs%2A>|Retourne la valeur absolue d'un nombre.|  
|<xref:System.Math.Acos%2A>|Retourne l'angle dont le cosinus est le nombre spécifié.|  
|<xref:System.Math.Asin%2A>|Retourne l'angle dont le sinus est le nombre spécifié.|  
|<xref:System.Math.Atan%2A>|Retourne l'angle dont la tangente est le nombre spécifié.|  
|<xref:System.Math.Atan2%2A>|Retourne l'angle dont la tangente est le quotient de deux nombres spécifiés.|  
|<xref:System.Math.BigMul%2A>|Retourne le produit intégral de deux nombres 32 bits.|  
|<xref:System.Math.Ceiling%2A>|Retourne la plus petite valeur intégrale qui est supérieure ou égale à spécifié `Decimal` ou `Double`.|  
|<xref:System.Math.Cos%2A>|Retourne le cosinus de l'angle spécifié.|  
|<xref:System.Math.Cosh%2A>|Retourne le cosinus hyperbolique de l'angle spécifié.|  
|<xref:System.Math.DivRem%2A>|Renvoie le quotient de deux entiers signés 32 bits ou 64 bits et retourne également le reste dans un paramètre de sortie.|  
|<xref:System.Math.Exp%2A>|Retourne e (la base des logarithmes naturels) élevé à la puissance spécifiée.|  
|<xref:System.Math.Floor%2A>|Retourne le plus grand entier inférieur ou égal à l’élément spécifié est `Decimal` ou `Double` nombre.|  
|<xref:System.Math.IEEERemainder%2A>|Retourne le reste de la division d’un nombre spécifié par un autre de nombre spécifié.|  
|<xref:System.Math.Log%2A>|Retourne le logarithme népérien (base e) d’un nombre spécifié ou le logarithme d’un nombre spécifié dans une base spécifiée.|  
|<xref:System.Math.Log10%2A>|Retourne le logarithme de base 10 d'un nombre spécifié.|  
|<xref:System.Math.Max%2A>|Retourne le plus grand de deux nombres.|  
|<xref:System.Math.Min%2A>|Retourne le plus petit de deux nombres.|  
|<xref:System.Math.Pow%2A>|Retourne un nombre spécifié élevé à la puissance spécifiée.|  
|<xref:System.Math.Round%2A>|Retourne un `Decimal` ou `Double` valeur arrondie à la valeur intégrale la plus proche ou à un nombre spécifié de chiffres fractionnaires.|  
|<xref:System.Math.Sign%2A>|Retourne un `Integer` valeur indiquant le signe d’un nombre.|  
|<xref:System.Math.Sin%2A>|Retourne le sinus de l'angle spécifié.|  
|<xref:System.Math.Sinh%2A>|Retourne le sinus hyperbolique de l'angle spécifié.|  
|<xref:System.Math.Sqrt%2A>|Retourne la racine carrée d'un nombre spécifié.|  
|<xref:System.Math.Tan%2A>|Retourne la tangente de l'angle spécifié.|  
|<xref:System.Math.Tanh%2A>|Retourne la tangente hyperbolique de l'angle spécifié.|  
|<xref:System.Math.Truncate%2A>|Calcule la partie entière d’une certaine `Decimal` ou `Double` nombre.|  
  
 Pour utiliser ces fonctions sans qualification, importez le <xref:System.Math?displayProperty=nameWithType> espace de noms dans votre projet en ajoutant le code suivant en haut de votre fichier source :  
  
```vb
Imports System.Math  
```  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le <xref:System.Math.Abs%2A> méthode de la <xref:System.Math> classe pour calculer la valeur absolue d’un nombre.  
  
```vb
' Returns 50.3.  
Dim MyNumber1 As Double = Math.Abs(50.3)  
' Returns 50.3.  
Dim MyNumber2 As Double = Math.Abs(-50.3)  
```  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le <xref:System.Math.Atan%2A> méthode de la <xref:System.Math> classe pour calculer la valeur de pi.  
  
```vb
Public Function GetPi() As Double  
    ' Calculate the value of pi.  
    Return 4.0 * Math.Atan(1.0)  
End Function  
```  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le <xref:System.Math.Cos%2A> méthode de la <xref:System.Math> classe pour retourner le cosinus d’un angle.  
  
```vb
Public Function Sec(ByVal angle As Double) As Double  
    ' Calculate the secant of angle, in radians.  
    Return 1.0 / Math.Cos(angle)  
End Function  
```  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le <xref:System.Math.Exp%2A> méthode de la <xref:System.Math> classe pour retourner la valeur e élevée à une puissance.  
  
```vb
Public Function Sinh(ByVal angle As Double) As Double  
    ' Calculate hyperbolic sine of an angle, in radians.  
    Return (Math.Exp(angle) - Math.Exp(-angle)) / 2.0  
End Function  
```  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le <xref:System.Math.Log%2A> méthode de la <xref:System.Math> classe pour retourner le logarithme naturel d’un nombre.  
  
```vb
Public Function Asinh(ByVal value As Double) As Double  
    ' Calculate inverse hyperbolic sine, in radians.  
    Return Math.Log(value + Math.Sqrt(value * value + 1.0))  
End Function  
```  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le <xref:System.Math.Round%2A> méthode de la <xref:System.Math> classe pour arrondir un nombre à l’entier le plus proche.  
  
```vb
' Returns 3.  
Dim MyVar2 As Double = Math.Round(2.8)  
```  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le <xref:System.Math.Sign%2A> méthode de la <xref:System.Math> classe pour déterminer le signe d’un nombre.  
  
```vb
' Returns 1.  
Dim MySign1 As Integer = Math.Sign(12)  
' Returns -1.  
Dim MySign2 As Integer = Math.Sign(-2.4)  
' Returns 0.  
Dim MySign3 As Integer = Math.Sign(0)  
```  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le <xref:System.Math.Sin%2A> méthode de la <xref:System.Math> classe pour retourner le sinus d’un angle.  
  
```vb
Public Function Csc(ByVal angle As Double) As Double  
    ' Calculate cosecant of an angle, in radians.  
    Return 1.0 / Math.Sin(angle)  
End Function  
```  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le <xref:System.Math.Sqrt%2A> méthode de la <xref:System.Math> classe pour calculer la racine carrée d’un nombre.  
  
```vb
' Returns 2.  
Dim MySqr1 As Double = Math.Sqrt(4)  
' Returns 4.79583152331272.  
Dim MySqr2 As Double = Math.Sqrt(23)  
' Returns 0.  
Dim MySqr3 As Double = Math.Sqrt(0)  
' Returns NaN (not a number).  
Dim MySqr4 As Double = Math.Sqrt(-4)  
```  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le <xref:System.Math.Tan%2A> méthode de la <xref:System.Math> classe pour retourner la tangente d’un angle.  
  
```vb
Public Function Ctan(ByVal angle As Double) As Double  
    ' Calculate cotangent of an angle, in radians.  
    Return 1.0 / Math.Tan(angle)  
End Function  
```  
  
## <a name="requirements"></a>Configuration requise  
 **Classe :** <xref:System.Math>  
  
 **Espace de noms :** <xref:System>  
  
 **Assembly :** mscorlib (dans mscorlib.dll)  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.VBMath.Rnd%2A>
- <xref:Microsoft.VisualBasic.VBMath.Randomize%2A>
- <xref:System.Double.NaN>
- [Fonctions mathématiques dérivées](../../../visual-basic/language-reference/keywords/derived-math-functions.md)
- [Opérateurs arithmétiques](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
