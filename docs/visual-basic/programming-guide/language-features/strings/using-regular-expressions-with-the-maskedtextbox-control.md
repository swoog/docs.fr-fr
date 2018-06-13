---
title: Utilisation d'expressions régulières avec le contrôle MaskedTextBox en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], regular expressions
- strings [Visual Basic], masked edit
ms.assetid: 2a048fb0-7053-487d-b2c5-ffa5e22ed6f9
ms.openlocfilehash: afc19ccf476317e8c30a1cc6964c64f1a59a0ff8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33655469"
---
# <a name="using-regular-expressions-with-the-maskedtextbox-control-in-visual-basic"></a>Utilisation d'expressions régulières avec le contrôle MaskedTextBox en Visual Basic
Cet exemple montre comment convertir des expressions régulières simples pour travailler avec les <xref:System.Windows.Forms.MaskedTextBox> contrôle.  
  
## <a name="description-of-the-masking-language"></a>Description du langage de masquage  
 La norme <xref:System.Windows.Forms.MaskedTextBox> le langage de masquage est basé sur celui utilisé par le `Masked Edit` contrôler dans Visual Basic 6.0 et doit être connu pour les utilisateurs de la migration à partir de cette plateforme.  
  
 Le <xref:System.Windows.Forms.MaskedTextBox.Mask%2A> propriété de la <xref:System.Windows.Forms.MaskedTextBox> contrôle spécifie le masque d’entrée à utiliser. Le masque doit être une chaîne composée d’un ou plusieurs des éléments de masques dans le tableau suivant.  
  
|Élément de masquage|Description|Élément d’expression régulière|  
|---------------------|-----------------|--------------------------------|  
|0|Tout chiffre compris entre 0 et 9. Entrée obligatoire.|\d|  
|9|Chiffre ou espace. Entrée facultative.|[\d] ?|  
|#|Chiffre ou espace. Entrée facultative. Si cette position est vide dans le masque, elle est restituée comme un espace. Signe plus (+) et moins (-), signes sont autorisés.|[\d+-] ?|  
|L|Lettre ASCII. Entrée obligatoire.|[a-zA-Z]|  
|?|Lettre ASCII. Entrée facultative.|[a-zA-Z] ?|  
|&|Caractère. Entrée obligatoire.|[\p{Ll}\p{Lu}\p{Lt}\p{Lm}\p{Lo}]|  
|C|Caractère. Entrée facultative.|[\p{Ll}\p{Lu}\p{Lt}\p{Lm}\p{Lo}] ?|  
|A|Alphanumérique. Entrée facultative.|\W|  
|.|Espace réservé décimal approprié à la culture.|Non disponible.|  
|,|Espace réservé aux milliers approprié à la culture.|Non disponible.|  
|:|Séparateur d’heure approprié à la culture.|Non disponible.|  
|/|Séparateur de date approprié à la culture.|Non disponible.|  
|$|Symbole de devise d’approprié à la culture.|Non disponible.|  
|\<|Convertit tous les caractères qui suivent en minuscules.|Non disponible.|  
|>|Convertit tous les caractères qui suivent en majuscules.|Non disponible.|  
|&#124;|Annule un décalage vers la précédente haut ou vers le bas.|Non disponible.|  
|\|Remplace un caractère de masque, transformant en un littéral. «\\\\» est la séquence d’échappement pour une barre oblique inverse.|\|  
|Tous les autres caractères.|Littéraux. Tous les éléments non-masque apparaîtra eux-mêmes dans <xref:System.Windows.Forms.MaskedTextBox>.|Tous les autres caractères.|  
  
 Le séparateur décimal (.) millièmes (,), ( :), date (/) et heure par défaut de symboles de devise ($) à l’affichage de ces symboles tel que défini par la culture de l’application. Vous pouvez les forcer à afficher les symboles d’une autre culture à l’aide de la <xref:System.Windows.Forms.MaskedTextBox.FormatProvider%2A> propriété.  
  
## <a name="regular-expressions-and-masks"></a>Expressions régulières et masques  
 Bien que vous pouvez utiliser des expressions régulières et masques pour valider l’entrée d’utilisateur, ils ne sont pas complètement équivalentes. Expressions régulières peuvent exprimer des modèles plus complexes que les masques, mais les masques peuvent exprimer les mêmes informations plus succinctement et dans un format culturellement pertinent.  
  
 Le tableau suivant compare quatre expressions régulières et le masque équivalent pour chacune.  
  
|Expression régulière|Masque|Notes|  
|------------------------|----------|-----------|  
|`\d{2}/\d{2}/\d{4}`|`00/00/0000`|Le `/` dans le masque est un séparateur de date logique, et elle apparaîtra à l’utilisateur en tant que séparateur de date approprié à la culture actuelle de l’application.|  
|`\d{2}-[A-Z][a-z]{2}-\d{4}`|`00->L<LL-0000`|Date (jour, abréviation du mois et année) au format américain dans lequel l’abréviation de trois lettres du mois est affichée par une lettre majuscule initiale suivie de deux lettres minuscules.|  
|`(\(\d{3}\)-)?\d{3}-d{4}`|`(999)-000-0000`|Numéro de téléphone aux États-Unis, indicatif régional facultatif. Si l’utilisateur ne souhaite pas entrer les caractères facultatifs, il peut entrer des espaces ou placer le pointeur de souris directement à la position représentée par le premier 0 dans le masque.|  
|`$\d{6}.00`|`$999,999.00`|Valeur monétaire comprise entre 0 et 999999. La devise, millième et caractères décimaux sont remplacés au moment de l’exécution par leurs équivalents spécifiques à la culture.|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.MaskedTextBox.Mask%2A>  
 <xref:System.Windows.Forms.MaskedTextBox>  
 [Validation de chaînes en Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/validating-strings.md)  
 [MaskedTextBox, contrôle](../../../../framework/winforms/controls/maskedtextbox-control-windows-forms.md)
