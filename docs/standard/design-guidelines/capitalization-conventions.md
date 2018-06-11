---
title: Conventions de mise en majuscules
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- camel-case names [.NET Framework]
- class library design guidelines [.NET Framework], capitalization
- Pascal-case names [.NET Framework]
- case sensitivity, capitalization conventions
- names [.NET Framework], capitalization
ms.assetid: 4c4ea526-9203-486f-b72d-29d61c5b3c6d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7ef7913a2601c3a791cb028b4074ce37b9e9421b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="capitalization-conventions"></a>Conventions de mise en majuscules
Les lignes directrices de ce chapitre présentent une méthode simple d'utilisation des cas qui, lorsqu'ils sont appliqués de façon uniforme, rendent les identificateurs pour les types, les membres et les paramètres faciles à lire.
  
## <a name="capitalization-rules-for-identifiers"></a>Règles de casse des identificateurs  
Afin de distinguer des mots dans un identifiant, il faut mettre en majuscule la première lettre de chaque mot dans l’identifiant. N’utilisez pas de traits de soulignement pour différencier des mots, ainsi que n’importe où dans les identifiant. Il existe deux façons appropriés pour tirer profit des identificateurs, en fonction de l’utilisation de l’identificateur :  
  
-   Casse Pascal  
-   Casse Camel
  
 La convention de casse Pascal, utilisée pour tous les identificatiantss à l’exception des noms de paramètres, met en majuscule le premier caractère de chaque mot (y compris les acronymes sur les deux lettres longueur), comme indiqué dans les exemples suivants :  
  
 `PropertyDescriptor`  
 `HtmlTag`
  
 Un cas particulier concerne des acronymes de deux lettres correspondant à la fois des lettres sont en majuscules, comme indiqué dans l’identificateur suivant :  
  
 `IOStream`  
  
 La convention de casse Camel, utilisée uniquement pour les noms de paramètres, met en majuscule le premier caractère de chaque mot, sauf le premier mot, comme indiqué dans les exemples suivants.
  
 `propertyDescriptor`  
 `ioStream`  
 
 Comme dans l’exemple également, les acronymes de deux lettres qui commencent un identifiant à casse mixte sont en minuscules.  
 
 `htmlTag`  
  
 **✓ FAIRE** utiliser la Pascal Case pour tous les noms de membre, le type et espace de noms publics constitué de plusieurs mots.  
  
 **✓ FAIRE** utiliser la casse Camel pour les noms de paramètre.  
  
 Le tableau suivant décrit les règles de mise en majuscules pour différents types d’identificateurs.  
  
|Identificateur|Casse|Exemple|  
|----------------|------------|-------------|  
|Espace de noms|Pascal|`namespace System.Security { ... }`|  
|Type|Pascal|`public class StreamReader { ... }`|  
|Interface|Pascal|`public interface IEnumerable { ... }`|  
|Méthode|Pascal|`public class Object {` <br />  `public virtual string ToString();` <br /> `}`|  
|Propriété|Pascal|`public class String {` <br />  `public int Length { get; }` <br /> `}`|  
|Événement|Pascal|`public class Process {` <br />  `public event EventHandler Exited;` <br /> `}`|  
|Champ|Pascal|`public class MessageQueue {` <br />  `public static readonly TimeSpan` <br /> `InfiniteTimeout;` <br /> `}` <br /> `public struct UInt32 {` <br />  `public const Min = 0;` <br /> `}`|  
|Valeur d’énumération|Pascal|`public enum FileMode {` <br />  `Append,` <br />  `...` <br /> `}`|  
|Paramètre|Camel|`public class Convert {` <br />  `public static int ToInt32(string value);` <br /> `}`|  
  
## <a name="capitalizing-compound-words-and-common-terms"></a>Mise en majuscule de mots composés et les termes courants  
 La plupart des termes composés sont traités comme des mots isolés pour les besoins de mise en majuscules.  
  
 **X NE PAS FAIRE**  mettre une majuscule à chaque mot dans les mots composés dits fermés.
  
 Il s’agit de mots composés écrits comme un mot unique, comme point de terminaison. Les instructions de la casse, à des fins de traiter un mot composé fermé comme un mot unique. Utiliser un dictionnaire actuel pour déterminer si un mot composé est écrit dans une forme fermée.  
  
|Pascal|Camel|Pas|  
|------------|-----------|---------|  
|`BitFlag`|`bitFlag`|`Bitflag`|  
|`Callback`|`callback`|`CallBack`|  
|`Canceled`|`canceled`|`Cancelled`|  
|`DoNot`|`doNot`|`Don't`|  
|`Email`|`email`|`EMail`|  
|`Endpoint`|`endpoint`|`EndPoint`|  
|`FileName`|`fileName`|`Filename`|  
|`Gridline`|`gridline`|`GridLine`|  
|`Hashtable`|`hashtable`|`HashTable`|  
|`Id`|`id`|`ID`|  
|`Indexes`|`indexes`|`Indices`|  
|`LogOff`|`logOff`|`LogOut`|  
|`LogOn`|`logOn`|`LogIn`|  
|`Metadata`|`metadata`|`MetaData, metaData`|  
|`Multipanel`|`multipanel`|`MultiPanel`|  
|`Multiview`|`multiview`|`MultiView`|  
|`Namespace`|`namespace`|`NameSpace`|  
|`Ok`|`ok`|`OK`|  
|`Pi`|`pi`|`PI`|  
|`Placeholder`|`placeHolder`|`Placeholder`|  
|`SignIn`|`signIn`|`SignOn`|  
|`SignOut`|`signOut`|`SignOff`|  
|`UserName`|`userName`|`Username`|  
|`WhiteSpace`|`whiteSpace`|`Whitespace`|  
|`Writable`|`writable`|`Writeable`|  
  
## <a name="case-sensitivity"></a>Respect de la casse  
 Les langues qui peuvent s’exécuter sur le CLR ne sont pas requis pour prendre en charge le respect de la casse, bien que certains le fassent. Même si votre langue le supporte, d'autres langues qui pourraient accéder à votre framework ne le font pas. Les API qui sont accessibles de l'extérieur ne peuvent donc pas se fier uniquement à la casse pour distinguer deux noms dans le même contexte.
  
 **X NE PAS FAIRE** supposer que tous les langages de programmation sont sensibles à la casse. Ils ne le sont pas. Les noms ne peuvent pas différer d'un cas à l'autre.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimées avec l’autorisation de Pearson éducation, Inc. à partir de [règles de conception d’infrastructure : Conventions, idiomes et des modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi  
 [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)  
 [Directives de nommage](../../../docs/standard/design-guidelines/naming-guidelines.md)
