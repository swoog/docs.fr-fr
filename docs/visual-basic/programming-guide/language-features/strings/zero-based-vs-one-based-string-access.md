---
title: Accès à une chaîne de base zéro et Accès d’une chaîne de base dans Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], indexing
ms.assetid: 0ed39f35-d68e-421d-ae14-460a5c0373b8
ms.openlocfilehash: a6ceb10d4a3cb9463551d8c85375ddbbb607ffdc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62024454"
---
# <a name="zero-based-vs-one-based-string-access-in-visual-basic"></a>Accès à une chaîne de base zéro et Accès d’une chaîne de base dans Visual Basic
Cette rubrique compare la façon dont Visual Basic et le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] fournir un accès aux caractères dans une chaîne. Le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] fournit toujours un accès de base zéro pour les caractères dans une chaîne, tandis que Visual Basic fournit l’accès de base zéro et un, en fonction de la fonction.  
  
## <a name="one-based"></a>Basé sur un  
 Pour obtenir un exemple d’une fonction Visual Basic basé sur 1, envisagez le `Mid` (fonction). Il accepte un argument qui indique la position de caractère à laquelle la sous-chaîne démarre, en commençant à la position 1. Le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] <xref:System.String.Substring%2A?displayProperty=nameWithType> méthode prend un index du caractère dans la chaîne à laquelle la sous-chaîne doit démarrer, en commençant à la position 0. Par conséquent, si vous avez une chaîne « ABCDE », les caractères individuels sont numérotés 1,2,3,4,5 pour une utilisation avec le `Mid` (fonction), mais 0,1,2,3,4 pour une utilisation avec le <xref:System.String.Substring%2A?displayProperty=nameWithType> (méthode).  
  
## <a name="zero-based"></a>Base zéro  
 Pour obtenir un exemple d’une fonction Visual Basic de base zéro, envisagez le `Split` (fonction). Il fractionne une chaîne et retourne un tableau contenant les sous-chaînes. Le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] <xref:System.String.Split%2A?displayProperty=nameWithType> méthode également fractionne une chaîne et retourne un tableau contenant les sous-chaînes. Étant donné que le `Split` (fonction) et <xref:System.String.Split%2A> retour de la méthode [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] tableaux, ils doivent être de base zéro.  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.Strings.Mid%2A>
- <xref:Microsoft.VisualBasic.Strings.Split%2A>
- <xref:System.String.Substring%2A>
- <xref:System.String.Split%2A>
- [Introduction aux chaînes en Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)
