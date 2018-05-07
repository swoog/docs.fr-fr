---
title: Vs de base zéro. Accès d’une chaîne de base en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], indexing
ms.assetid: 0ed39f35-d68e-421d-ae14-460a5c0373b8
ms.openlocfilehash: a0a42f72d94adf1c10865374017fa61e833df40f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="zero-based-vs-one-based-string-access-in-visual-basic"></a>Vs de base zéro. Accès d’une chaîne de base en Visual Basic
Cette rubrique compare la façon dont Visual Basic et [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] fournissent l’accès aux caractères dans une chaîne. Le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] fournit toujours un accès de base zéro pour les caractères dans une chaîne, alors que Visual Basic fournit un accès de base zéro et basé sur un, selon la fonction.  
  
## <a name="one-based"></a>Basé sur un  
 Pour obtenir un exemple d’une fonction Visual Basic basé sur un, envisagez la `Mid` (fonction). Il prend un argument qui indique la position de caractère à laquelle la sous-chaîne démarrera, en commençant à la position 1. Le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] <xref:System.String.Substring%2A?displayProperty=nameWithType> méthode prend un index du caractère dans la chaîne à laquelle la sous-chaîne doit démarrer, en commençant à la position 0. Par conséquent, si vous avez une chaîne « ABCDE », les caractères sont numérotés 1,2,3,4,5 pour la `Mid` (fonction), mais 0,1,2,3,4 pour une utilisation avec le <xref:System.String.Substring%2A?displayProperty=nameWithType> (méthode).  
  
## <a name="zero-based"></a>Base zéro  
 Pour obtenir un exemple d’une fonction Visual Basic de base zéro, envisagez la `Split` (fonction). Il fractionne une chaîne et retourne un tableau contenant les sous-chaînes. Le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] <xref:System.String.Split%2A?displayProperty=nameWithType> méthode également fractionne une chaîne et retourne un tableau contenant les sous-chaînes. Étant donné que la `Split` (fonction) et <xref:System.String.Split%2A> retour de la méthode [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] tableaux, ils doivent être de base zéro.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.Strings.Mid%2A>  
 <xref:Microsoft.VisualBasic.Strings.Split%2A>  
 <xref:System.String.Substring%2A>  
 <xref:System.String.Split%2A>  
 [Introduction aux chaînes en Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)
