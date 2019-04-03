---
title: Comment les informations de culture affectent les chaînes dans Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- locale [Visual Basic], effect on strings
- strings [Visual Basic], locale dependence
ms.assetid: c4664444-ee0d-47bf-bef1-eaa3c54bdd7f
ms.openlocfilehash: d3c7ae9da9c18e53da393928e34dcfbf04fc891c
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58834619"
---
# <a name="how-culture-affects-strings-in-visual-basic"></a>Comment les informations de culture affectent les chaînes dans Visual Basic
Cette page d’aide décrit comment Visual Basic utilise les informations de culture pour effectuer des comparaisons et les conversions de chaînes.  
  
## <a name="when-to-use-culture-specific-strings"></a>Quand utiliser des chaînes spécifiques à la Culture  
 En règle générale, vous devez utiliser des chaînes spécifiques à la culture pour toutes les données présentées à lire à partir d’utilisateurs et utiliser les chaînes de culture dite indifférente pour les données internes de votre application.  
  
 Par exemple, si votre application demande aux utilisateurs d’entrer une date sous forme de chaîne, il doit attendre les utilisateurs à mettre en forme les chaînes en fonction de leur culture et l’application doit convertir la chaîne de manière appropriée. Si votre application présente ensuite cette date dans son interface utilisateur, elle doit le présenter dans la culture de l’utilisateur.  
  
 Toutefois, si l’application télécharge la date sur un serveur central, il doit mettre en forme la chaîne en fonction d’une culture spécifique, afin d’éviter toute confusion entre les formats de date potentiellement différents.  
  
## <a name="culture-sensitive-functions"></a>Fonctions de la culture  
 Toutes les fonctions de conversion de chaînes Visual Basic (à l’exception de la `Str` et `Val` fonctions) utilisent les informations de culture de l’application pour vous assurer que les conversions et les comparaisons sont appropriés pour la culture de l’application utilisateur.  
  
 La clé à l’aide de fonctions de conversion de chaînes dans les applications qui s’exécutent sur des ordinateurs avec des paramètres de culture différent est de comprendre les fonctions qui utilisent un paramètre de culture spécifique, et qui utilisent le paramètre de culture actuel. Notez que les paramètres de culture de l’application sont, par défaut, héritées à partir des paramètres de culture du système d’exploitation. Pour plus d’informations, consultez <xref:Microsoft.VisualBasic.Strings.Asc%2A>, <xref:Microsoft.VisualBasic.Strings.AscW%2A>, <xref:Microsoft.VisualBasic.Strings.Chr%2A>, <xref:Microsoft.VisualBasic.Strings.ChrW%2A>, <xref:Microsoft.VisualBasic.Strings.Format%2A>, <xref:Microsoft.VisualBasic.Conversion.Hex%2A>, <xref:Microsoft.VisualBasic.Conversion.Oct%2A>, et [les fonctions de Conversion de Type](../../../../visual-basic/language-reference/functions/type-conversion-functions.md).  
  
 Le `Str` (convertit les nombres en chaînes) et `Val` les fonctions (convertit des chaînes en nombres) n’utilisent pas les informations de culture de l’application lors de la conversion entre chaînes et des nombres. Au lieu de cela, ils ne reconnaissent que le point (.) comme séparateur décimal valide. Les culture prenant en charge les analogues de ces fonctions sont les suivantes :  
  
-   **Conversions qui utilisent la culture actuelle.** Le `CStr` et `Format` fonctions convertissent un nombre en une chaîne et le `CDbl` et `CInt` fonctions convertissent une chaîne en un nombre.  
  
-   **Conversions qui utilisent une culture spécifique.** Chaque objet number a un `ToString(IFormatProvider)` méthode qui convertit un nombre en une chaîne, et un `Parse(String, IFormatProvider)` méthode qui convertit une chaîne en un nombre. Par exemple, le `Double` type fournit le <xref:System.Double.ToString%28System.IFormatProvider%29> et <xref:System.Double.Parse%28System.String%2CSystem.IFormatProvider%29> méthodes.  
  
 Pour plus d’informations, consultez <xref:Microsoft.VisualBasic.Conversion.Str%2A> et <xref:Microsoft.VisualBasic.Conversion.Val%2A>.  
  
## <a name="using-a-specific-culture"></a>À l’aide d’une Culture spécifique  
 Imaginez que vous développez une application qui envoie une date (sous formatée de chaîne) à un service Web. Dans ce cas, votre application doit utiliser une culture spécifique pour la conversion de chaîne. Pour illustrer pourquoi, observez le résultat de l’utilisation de la date <xref:System.DateTime.ToString> méthode : Si votre application utilise cette méthode pour mettre en forme la date du 4 juillet 2005, elle retourne « 7/4/2005 12:00:00 AM » lorsqu’il est exécuté avec la culture anglais des États-Unis (en-US), mais elle retourne « 04.07.2005 00:00:00 » lorsqu’il est exécuté avec la culture Allemand (de-DE).  
  
 Lorsque vous avez besoin effectuer une conversion de chaîne dans un format de culture spécifique, vous devez utiliser le `CultureInfo` classe qui est intégrée dans le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)]. Vous pouvez créer un nouveau `CultureInfo` objet pour une culture spécifique en passant le nom de la culture à le <xref:System.Globalization.CultureInfo.%23ctor%2A> constructeur. Les noms de culture prise en charge sont répertoriés dans le <xref:System.Globalization.CultureInfo> page d’aide de classe.  
  
 Vous pouvez également obtenir une instance de la *culture dite indifférente* à partir de la <xref:System.Globalization.CultureInfo.InvariantCulture%2A?displayProperty=nameWithType> propriété. La culture dite indifférente est basée sur la culture anglaise, mais il existe quelques différences. Par exemple, la culture dite indifférente spécifie une horloge de 24 heures au lieu d’une horloge de 12 heures.  
  
 Pour convertir une date à la chaîne de culture, passez le <xref:System.Globalization.CultureInfo> objet à l’objet date <xref:System.DateTime.ToString%28System.IFormatProvider%29> (méthode). Par exemple, le code suivant affiche « 07/04/2005 00:00:00 », indépendamment des paramètres de culture de l’application.  
  
 [!code-vb[VbVbalrConcepts#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrConcepts/VB/Class1.vb#1)]  
  
> [!NOTE]
>  Littéraux de date sont toujours interprétées selon la culture.  
  
## <a name="comparing-strings"></a>Comparaison de chaînes  
 Il existe deux situations importantes où les comparaisons de chaînes sont nécessaires :  
  
-   **Tri des données pour l’affichage à l’utilisateur.** Utilisez des opérations basée sur la culture actuelle, le tri de chaînes en conséquence.  
  
-   **Déterminer si deux chaînes interne de l’application correspondent exactement (en général pour des raisons de sécurité).** Utilisez les opérations qui ignorent la culture actuelle.  
  
 Vous pouvez effectuer les deux types de comparaisons avec Visual Basic <xref:Microsoft.VisualBasic.Strings.StrComp%2A> (fonction). Spécifiez le paramètre facultatif `Compare` argument pour contrôler le type de comparaison : `Text` pour la plupart des entrées et sorties `Binary` pour déterminer les correspondances exactes.  
  
 Le `StrComp` fonction retourne un entier qui indique la relation entre les deux chaînes comparées selon l’ordre de tri. Une valeur positive pour le résultat indique que la première chaîne est supérieure à la seconde chaîne. Un résultat négatif indique la première chaîne est plus petite et la valeur zéro indique l’égalité entre les chaînes.  
  
 [!code-vb[VbVbalrStrings#22](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class1.vb#22)]  
  
 Vous pouvez également utiliser le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] partenaire de la `StrComp` (fonction), le <xref:System.String.Compare%2A?displayProperty=nameWithType> (méthode). Il s’agit d’une méthode statique, la surcharge de la classe string de base. L’exemple suivant illustre comment cette méthode est utilisée :  
  
 [!code-vb[VbVbalrStrings#48](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#48)]  
  
 Pour un contrôle plus précis sur la façon dont les comparaisons sont effectuées, vous pouvez utiliser des surcharges supplémentaires de la <xref:System.String.Compare%2A> (méthode). Avec le <xref:System.String.Compare%2A?displayProperty=nameWithType> (méthode), vous pouvez utiliser le `comparisonType` argument pour spécifier le type de comparaison à utiliser.  
  
|Valeur pour `comparisonType` argument|Type de comparaison|Quand l'utiliser|  
|---|---|---|  
|`Ordinal`|Comparaison basée sur les octets de composant de chaînes.|Utilisez cette valeur lors de la comparaison : identificateurs respectant la casse, les paramètres de sécurité ou autres identificateurs non linguistiques où les octets doivent correspondre exactement.|  
|`OrdinalIgnoreCase`|Comparaison basée sur les octets de composant de chaînes.<br /><br /> `OrdinalIgnoreCase` utilise les informations de culture dite indifférente pour déterminer quand deux caractères diffèrent uniquement par la mise en majuscules.|Utilisez cette valeur lors de la comparaison : identificateurs de non-respect de la casse, les paramètres liés à la sécurité et les données stockées dans Windows.|  
|`CurrentCulture` ou `CurrentCultureIgnoreCase`|Comparaison basée sur l’interprétation des chaînes dans la culture actuelle.|Utilisez ces valeurs lors de la comparaison : données qui sont affichées à l’utilisateur, la plupart des entrées d’utilisateur et autres données qui nécessitent une interprétation linguistique.|  
|`InvariantCulture` ou `InvariantCultureIgnoreCase`|Comparaison basée sur l’interprétation des chaînes dans la culture dite indifférente.<br /><br /> Cela diffère la `Ordinal` et `OrdinalIgnoreCase`, car la culture dite indifférente traite les caractères en dehors de sa plage admise comme des caractères invariants équivalents.|Utilisez ces valeurs uniquement lors de la comparaison des données persistantes ou affichage des données linguistiquement pertinentes qui requiert un ordre de tri fixe.|  
  
### <a name="security-considerations"></a>Considérations relatives à la sécurité  
 Si votre application prend des décisions de sécurité en fonction du résultat d’une comparaison ou d’une opération de changement de casse, l’opération doit utiliser le <xref:System.String.Compare%2A?displayProperty=nameWithType> (méthode), puis transmettez `Ordinal` ou `OrdinalIgnoreCase` pour le `comparisonType` argument.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Globalization.CultureInfo>
- [Introduction aux chaînes en Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)
- [Fonctions de conversion de types](../../../../visual-basic/language-reference/functions/type-conversion-functions.md)
