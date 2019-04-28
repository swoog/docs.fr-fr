---
title: Dépannage des tableaux (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- troubleshooting arrays
- arrays [Visual Basic], initialization errors
- troubleshooting Visual Basic, arrays
- arrays [Visual Basic], compilation errors
- arrays [Visual Basic], declaration errors
- arrays [Visual Basic], troubleshooting
ms.assetid: f4e971c7-c0a4-4ed7-a77a-8d71039f266f
ms.openlocfilehash: 2b051d22fe3d331626f2e181c008043e576b7526
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61908126"
---
# <a name="troubleshooting-arrays-visual-basic"></a>Dépannage des tableaux (Visual Basic)
Cette page répertorie certains problèmes courants qui peuvent se produire lorsque vous travaillez avec des tableaux.  
  
## <a name="compilation-errors-declaring-and-initializing-an-array"></a>Déclaration et initialisation d’un tableau d’erreurs de compilation  
 Erreurs de compilation peuvent se produire à partir de la méconnaissance des relations entre les règles de déclaration, la création et initialisation des tableaux. Les causes les plus courantes d’erreurs sont les suivantes :  
  
- En fournissant un [nouvel opérateur](../../../../visual-basic/language-reference/operators/new-operator.md) clause après avoir spécifié les longueurs de dimensions dans la déclaration de variable de tableau. Les lignes de code suivantes illustrent des déclarations non valides de ce type.  
  
     `Dim INVALIDsingleDimByteArray(2) As Byte = New Byte()`  
  
     `Dim INVALIDtwoDimShortArray(1, 1) As Short = New Short(,)`  
  
     `Dim INVALIDjaggedByteArray(1)() As Byte = New Byte()()`  
  
- Spécification de longueurs de dimensions plus longtemps que le tableau de niveau supérieur d’un tableau en escalier. La ligne de code suivant montre une déclaration non valide de ce type.  
  
     `Dim INVALIDjaggedByteArray(1)(1) As Byte`  
  
- En omettant le `New` mot clé lorsque vous spécifiez les valeurs d’élément. La ligne de code suivant montre une déclaration non valide de ce type.  
  
     `Dim INVALIDoneDimShortArray() As Short = Short() {0, 1, 2, 3}`  
  
- En fournissant un `New` clause sans accolades (`{}`). Les lignes de code suivantes illustrent des déclarations non valides de ce type.  
  
     `Dim INVALIDsingleDimByteArray() As Byte = New Byte()`  
  
     `Dim INVALIDsingleDimByteArray() As Byte = New Byte(2)`  
  
     `Dim INVALIDtwoDimShortArray(,) As Short = New Short(,)`  
  
     `Dim INVALIDtwoDimShortArray(,) As Short = New Short(1, 1)`  
  
## <a name="accessing-an-array-out-of-bounds"></a>L’accès à un tableau hors limites  
 Le processus d’initialisation d’un tableau assigne une limite supérieure et inférieure à chaque dimension. Chaque accès à un élément du tableau doit spécifier un index valide, ou un indice, pour chaque dimension. Si un index est inférieur à sa limite inférieure ou au-dessus de sa limite supérieure, une <xref:System.IndexOutOfRangeException> résultats de l’exception. Le compilateur ne peut pas détecter une telle erreur, donc une erreur se produit au moment de l’exécution.  
  
### <a name="determining-bounds"></a>Détermination des limites  
 Si un autre composant passe un tableau à votre code, par exemple en tant qu’argument de procédure, vous ne connaissez pas la taille de ce tableau ou les longueurs de ses dimensions. Vous devez toujours déterminer la limite supérieure de chaque dimension d’un tableau avant de tenter d’accéder aux éléments. Si le groupe a été créé par des moyens autres que Visual Basic `New` clause, la limite inférieure peut avoir une valeur différente de 0, et il est plus sûre déterminer ce inférieure.  
  
### <a name="specifying-the-dimension"></a>Spécification de la Dimension  
 Lorsque vous déterminez les limites d’un tableau multidimensionnel, veillez à vous spécifiez comment la dimension. Le `dimension` paramètres de le <xref:System.Array.GetLowerBound%2A> et <xref:System.Array.GetUpperBound%2A> méthodes sont basés sur 0, lors de la `Rank` paramètres de Visual Basic <xref:Microsoft.VisualBasic.Information.LBound%2A> et <xref:Microsoft.VisualBasic.Information.UBound%2A> fonctions sont de base 1.  
  
## <a name="see-also"></a>Voir aussi

- [Tableaux](../../../../visual-basic/programming-guide/language-features/arrays/index.md)
- [Guide pratique pour Initialiser une Variable tableau en Visual Basic](../../../../visual-basic/programming-guide/language-features/arrays/how-to-initialize-an-array-variable.md)
