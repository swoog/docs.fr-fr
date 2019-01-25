---
title: Conception de paramètres
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- member design guidelines [.NET Framework], parameters
- members [.NET Framework], parameters
- names [.NET Framework], parameters
- parameters, design guidelines
- reserved parameters
ms.assetid: 3f33bf46-4a7b-43b3-bb78-1ffebe0dcfa6
author: KrzysztofCwalina
ms.openlocfilehash: 5a0f6e0fab5d0f2fe8574e348fc6b8ae726eeb99
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54617211"
---
# <a name="parameter-design"></a>Conception de paramètres
Cette section fournit des indications générales sur la conception de paramètres, y compris les sections contenant des instructions pour la vérification des arguments. En outre, vous devez consulter les instructions décrites dans [d’affectation de noms de paramètres](../../../docs/standard/design-guidelines/naming-parameters.md).  
  
 **✓ DO** utiliser le type de paramètre moins dérivé qui fournit les fonctionnalités requises par le membre.  
  
 Par exemple, supposons que vous souhaitez concevoir une méthode qui énumère une collection et imprime chaque élément dans la console. Une telle méthode doit prendre <xref:System.Collections.IEnumerable> comme paramètre, pas <xref:System.Collections.ArrayList> ou <xref:System.Collections.IList>, par exemple.  
  
 **X DO NOT** utiliser des paramètres réservés.  
  
 Si plus d’entrée à un membre est nécessaire dans une version ultérieure, une nouvelle surcharge peut être ajoutée.  
  
 **X DO NOT** ont exposés publiquement de méthodes qui prennent des pointeurs, des tableaux de pointeurs ou des tableaux multidimensionnels en tant que paramètres.  
  
 Pointeurs et les tableaux multidimensionnels sont relativement difficiles à utiliser correctement. Dans presque tous les cas, l’API peuvent être repensées pour éviter de prendre ces types en tant que paramètres.  
  
 **✓ DO** placer tous les `out` paramètres après toute la valeur et `ref` paramètres (à l’exclusion des tableaux de paramètres), même si cela aboutit à une incohérence dans le paramètre de classement entre les surcharges (consultez [membre La surcharge](../../../docs/standard/design-guidelines/member-overloading.md)).  
  
 Le `out` paramètres peuvent être considérés comme valeurs de retour supplémentaires et regroupant les rend plus facile à comprendre la signature de méthode.  
  
 **✓ DO** cohérente dans les paramètres d’affectation de noms lors de la substitution de membres ou de l’implémentation des membres d’interface.  
  
 La relation entre les méthodes est mieux communique.  
  
### <a name="choosing-between-enum-and-boolean-parameters"></a>Choix entre Enum et des paramètres booléens  
 **✓ DO** utiliser les énumérations si un membre possède deux ou plusieurs paramètres booléens.  
  
 **X DO NOT** utiliser des valeurs booléennes, sauf si vous êtes absolument sûr, il y aura jamais besoin de plus de deux valeurs.  
  
 Enums donner à la place pour l’ajout ultérieur de valeurs, mais vous devez être conscient de toutes les implications de l’ajout de valeurs aux énumérations, qui sont décrites dans [conception d’énumérations](../../../docs/standard/design-guidelines/enum.md).  
  
 **✓ CONSIDER** à l’aide de valeurs booléennes pour les paramètres du constructeur qui sont des valeurs de deux États réellement et sont uniquement utilisées pour initialiser les propriétés booléennes.  
  
### <a name="validating-arguments"></a>Validation d’Arguments  
 **✓ DO** valider les arguments passés aux membres publics, protégés ou implémentées explicitement. Lever <xref:System.ArgumentException?displayProperty=nameWithType>, ou une de ses sous-classes, si la validation échoue.  
  
 Notez que la validation réelle ne doit pas nécessairement se produire dans le membre public ou protégé lui-même. Il peut se produire à un niveau inférieur dans une routine privé ou interne. Le point à retenir est que toute la surface exposée aux utilisateurs finaux vérifie les arguments.  
  
 **✓ DO** lever <xref:System.ArgumentNullException> si un argument null est passé et le membre ne prend pas en charge les arguments null.  
  
 **✓ DO** valider les paramètres d’énumération.  
  
 Ne supposez pas arguments enum seront dans la plage définie par l’énumération. Le CLR permet la conversion de toute valeur entière en une valeur enum même si la valeur n’est pas définie dans l’énumération.  
  
 **X DO NOT** utiliser <xref:System.Enum.IsDefined%2A?displayProperty=nameWithType> pour la plage enum vérifie.  
  
 **✓ DO** Sachez que les arguments mutables peuvent ont été modifiés après leur validation.  
  
 Si le membre est sensible à la sécurité, vous êtes invités à effectuer une copie puis valider et traiter l’argument.  
  
### <a name="parameter-passing"></a>Passage de paramètres  
 Du point de vue d’un concepteur de framework, il existe trois principaux groupes de paramètres : paramètres, par valeur `ref` paramètres, et `out` paramètres.  
  
 Lorsqu’un argument est passé à un paramètre par valeur, le membre reçoit une copie de l’argument réel passé. Si l’argument est un type valeur, une copie de l’argument est placée sur la pile. Si l’argument est un type référence, une copie de la référence est placée sur la pile. Langages CLR plus populaires, tels que c#, VB.NET et C++, default pour le passage de paramètres par valeur.  
  
 Quand un argument est passé via un `ref` paramètre, le membre reçoit une référence à l’argument réel passé. Si l’argument est un type valeur, une référence à l’argument est placée sur la pile. Si l’argument est un type référence, une référence à la référence est placée sur la pile. `Ref` paramètres peuvent être utilisés pour que le membre de modifier les arguments passés par l’appelant.  
  
 `Out` les paramètres sont similaires à `ref` paramètres, avec quelques petites différences. Le paramètre est considéré comme initialement non attribués et ne peut pas être lu dans le corps du membre avant lui est attribuée une valeur. En outre, le paramètre a à assigner une valeur avant le retour du membre.  
  
 **X AVOID** à l’aide de `out` ou `ref` paramètres.  
  
 À l’aide de `out` ou `ref` paramètres nécessite une certaine expérience des pointeurs, de comprendre la différence entre les types valeur et types référence et gestion de méthodes impliquant plusieurs valeurs de retour. En outre, la différence entre `out` et `ref` paramètres n’est pas généralement peu comprise. Les architectes de Framework conception destiné à une audience générale ne doivent pas s’attendre aux utilisateurs de maîtrisent l’utilisation des `out` ou `ref` paramètres.  
  
 **X DO NOT** passage de types référence par référence.  
  
 Il existe quelques rares exceptions à la règle, comme une méthode qui peut être utilisée pour échanger des références.  
  
### <a name="members-with-variable-number-of-parameters"></a>Membres avec un nombre Variable de paramètres  
 Les membres qui peuvent prendre un nombre variable d’arguments sont exprimées en fournissant un paramètre de tableau. Par exemple, <xref:System.String> fournit la méthode suivante :  
  
```  
public class String {  
    public static string Format(string format, object[] parameters);  
}  
```  
  
 Un utilisateur peut ensuite appeler la <xref:System.String.Format%2A?displayProperty=nameWithType> méthode, comme suit :  
  
 `String.Format("File {0} not found in {1}",new object[]{filename,directory});`  
  
 Ajout du mot clé c# params à un paramètre de tableau modifie le paramètre à un paramètre de tableau params ce que l'on appelle et fournit un raccourci à la création d’un tableau temporaire.  
  
```  
public class String {  
    public static string Format(string format, params object[] parameters);  
}  
```  
  
 Cela permet à l’utilisateur d’appeler la méthode en passant les éléments du tableau directement dans la liste d’arguments.  
  
 `String.Format("File {0} not found in {1}",filename,directory);`  
  
 Notez que le mot clé params peut être ajouté uniquement au dernier paramètre dans la liste de paramètres.  
  
 **✓ CONSIDER** Ajout du mot clé params aux paramètres de tableau, si vous pensez que les utilisateurs finaux pour passer des tableaux avec un petit nombre d’éléments. S’il est prévu qu’un grand nombre d’éléments sera transmis en commun des scénarios, les utilisateurs sans doute ne passera pas ces éléments comme étant inline quand même, et par conséquent, le mot clé params n’est pas nécessaire.  
  
 **X AVOID** à l’aide de tableaux params si l’appelant est presque toujours avoir l’entrée dans un tableau.  
  
 Par exemple, les membres avec des paramètres de tableau d’octets seraient presque jamais être appelées en passant des octets individuels. Pour cette raison, les paramètres de tableau d’octets dans le .NET Framework n’utilisent pas le mot clé params.  
  
 **X DO NOT** utiliser des tableaux params si le tableau est modifié par le membre prenant le paramètre de tableau params.  
  
 En raison du fait que de nombreux compilateurs transforment les arguments pour le membre en un tableau temporaire sur le site d’appel, le tableau peut être un objet temporaire, et par conséquent, toute modification apportée à la baie seront perdues.  
  
 **✓ CONSIDER** à l’aide du mot clé params dans une surcharge simple, même si une surcharge plus complexe ne peut pas l’utiliser.  
  
 Demandez-vous si les utilisateurs importants ayant du tableau de paramètres dans une surcharge même si ce n’était pas dans toutes les surcharges.  
  
 **✓ DO** essayez des paramètres de commande pour le rendre possible d’utiliser le mot clé params.  
  
 **✓ CONSIDER** fournissant des surcharges spéciaux et les chemins de code pour les appels avec un petit nombre d’arguments dans les API très sensibles aux performances.  
  
 Cela rend possible pour éviter de créer des objets de tableau lors de l’API est appelée avec un petit nombre d’arguments. Les noms des paramètres du formulaire en prenant une forme au singulier du paramètre de tableau et en ajoutant un suffixe numérique.  
  
 Vous devez uniquement le faire si vous vous apprêtez à particulariser le chemin d’accès de l’ensemble du code, pas seulement créer un tableau et appelez la méthode plus générale.  
  
 **✓ DO** Sachez que la valeur null peut être passée comme un argument de tableau params.  
  
 Vous devez valider que le tableau n’est pas null avant le traitement.  
  
 **X DO NOT** utiliser le `varargs` méthodes en tant que les points de suspension.  
  
 Certains langages CLR, tels que C++, prennent en charge une autre convention pour passer des listes de paramètres de variable appelées `varargs` méthodes. La convention de ne doit pas servir dans les infrastructures, car il n'est pas conforme CLS.  
  
### <a name="pointer-parameters"></a>Paramètres de pointeur  
 En règle générale, les pointeurs ne doivent pas apparaître dans la surface d’exposition publique d’une infrastructure bien conçue du code managé. La plupart du temps, les pointeurs doivent être encapsulées. Toutefois, dans certains cas les pointeurs sont nécessaires pour des raisons de l’interopérabilité et l’utilisation des pointeurs dans ce cas est appropriée.  
  
 **✓ DO** offrent une alternative pour les membres qui prennent un argument de pointeur, étant donné que les pointeurs ne sont pas conformes CLS.  
  
 **X AVOID** effectuant l’argument coûteux, la vérification des arguments de pointeur.  
  
 **✓ DO** suivent les conventions de pointeur associé courantes lors de la conception de membres avec des pointeurs.  
  
 Par exemple, il n’est pas nécessaire de transmettre l’index de début, car l’opération arithmétique de pointeur simple peut être utilisé pour obtenir le même résultat.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Instructions de conception des membres](../../../docs/standard/design-guidelines/member.md)
- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
