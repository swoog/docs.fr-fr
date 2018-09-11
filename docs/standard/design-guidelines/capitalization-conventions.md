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
ms.openlocfilehash: 070fc69728c2cb38e465dab9f6f591a77a857531
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44274257"
---
# <a name="capitalization-conventions"></a><span data-ttu-id="6c123-102">Conventions de mise en majuscules</span><span class="sxs-lookup"><span data-stu-id="6c123-102">Capitalization Conventions</span></span>
<span data-ttu-id="6c123-103">Les lignes directrices de ce chapitre présentent une méthode simple d'utilisation des cas qui, lorsqu'ils sont appliqués de façon uniforme, rendent les identificateurs pour les types, les membres et les paramètres faciles à lire.</span><span class="sxs-lookup"><span data-stu-id="6c123-103">The guidelines in this chapter lay out a simple method for using case that, when applied consistently, make identifiers for types, members, and parameters easy to read.</span></span>  
  
## <a name="capitalization-rules-for-identifiers"></a><span data-ttu-id="6c123-104">Règles de casse des identificateurs</span><span class="sxs-lookup"><span data-stu-id="6c123-104">Capitalization Rules for Identifiers</span></span>  
 <span data-ttu-id="6c123-105">Afin de distinguer les mots dans un identificateur, il faut y mettre en majuscule la première lettre de chaque mot.</span><span class="sxs-lookup"><span data-stu-id="6c123-105">To differentiate words in an identifier, capitalize the first letter of each word in the identifier.</span></span> <span data-ttu-id="6c123-106">N’utilisez pas de traits de soulignement pour différencier des mots, ni ailleurs à cette fin dans les identificateurs.</span><span class="sxs-lookup"><span data-stu-id="6c123-106">Do not use underscores to differentiate words, or for that matter, anywhere in identifiers.</span></span> <span data-ttu-id="6c123-107">Il existe deux façons appropriées d’utiliser des majuscules pour les identificateurs, en fonction de son utilisation :</span><span class="sxs-lookup"><span data-stu-id="6c123-107">There are two appropriate ways to capitalize identifiers, depending on the use of the identifier:</span></span>  
  
-   <span data-ttu-id="6c123-108">Casse Pascal</span><span class="sxs-lookup"><span data-stu-id="6c123-108">PascalCasing</span></span>  
  
-   <span data-ttu-id="6c123-109">casseCamel</span><span class="sxs-lookup"><span data-stu-id="6c123-109">camelCasing</span></span>  
  
 <span data-ttu-id="6c123-110">La convention CassePascal, utilisée pour tous les identificateurs à l’exception des noms de paramètres, met en majuscule le premier caractère de chaque mot (y compris les acronymes d’une longueur de deux lettres), comme indiqué dans les exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="6c123-110">The PascalCasing convention, used for all identifiers except parameter names, capitalizes the first character of each word (including acronyms over two letters in length), as shown in the following examples:</span></span>  
  
 `PropertyDescriptor`  
 `HtmlTag`  
  
 <span data-ttu-id="6c123-111">Un cas particulier concerne des acronymes de deux lettres dans lequel les deux lettres sont en majuscules, comme indiqué dans l’identificateur suivant :</span><span class="sxs-lookup"><span data-stu-id="6c123-111">A special case is made for two-letter acronyms in which both letters are capitalized, as shown in the following identifier:</span></span>  
  
 `IOStream`  
  
 <span data-ttu-id="6c123-112">La convention casseCamel, utilisée uniquement pour les noms de paramètres, met en majuscule le premier caractère de chaque mot, sauf le premier mot, comme indiqué dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="6c123-112">The camelCasing convention, used only for parameter names, capitalizes the first character of each word except the first word, as shown in the following examples.</span></span> <span data-ttu-id="6c123-113">Comme le montre également l’exemple, les acronymes de deux lettres qui sont au début d’un identificateur à casse mixte sont tout en minuscules.</span><span class="sxs-lookup"><span data-stu-id="6c123-113">As the example also shows, two-letter acronyms that begin a camel-cased identifier are both lowercase.</span></span>  
  
 `propertyDescriptor`  
 `ioStream`  
 `htmlTag`  
  
 <span data-ttu-id="6c123-114">**✓ UTILISEZ** la convention CassePascal pour tous les noms de membres, de types et d’espaces de noms publics constitué de plusieurs mots.</span><span class="sxs-lookup"><span data-stu-id="6c123-114">**✓ DO** use PascalCasing for all public member, type, and namespace names consisting of multiple words.</span></span>  
  
 <span data-ttu-id="6c123-115">**✓ UTILISEZ** la convention casseCamel pour les noms de paramètre.</span><span class="sxs-lookup"><span data-stu-id="6c123-115">**✓ DO** use camelCasing for parameter names.</span></span>  
  
 <span data-ttu-id="6c123-116">Le tableau suivant décrit les règles de mise en majuscules pour différents types d’identificateurs.</span><span class="sxs-lookup"><span data-stu-id="6c123-116">The following table describes the capitalization rules for different types of identifiers.</span></span>  
  
|<span data-ttu-id="6c123-117">Identificateur</span><span class="sxs-lookup"><span data-stu-id="6c123-117">Identifier</span></span>|<span data-ttu-id="6c123-118">Casse</span><span class="sxs-lookup"><span data-stu-id="6c123-118">Casing</span></span>|<span data-ttu-id="6c123-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="6c123-119">Example</span></span>|  
|----------------|------------|-------------|  
|<span data-ttu-id="6c123-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6c123-120">Namespace</span></span>|<span data-ttu-id="6c123-121">Pascal</span><span class="sxs-lookup"><span data-stu-id="6c123-121">Pascal</span></span>|`namespace System.Security { ... }`|  
|<span data-ttu-id="6c123-122">Type</span><span class="sxs-lookup"><span data-stu-id="6c123-122">Type</span></span>|<span data-ttu-id="6c123-123">Pascal</span><span class="sxs-lookup"><span data-stu-id="6c123-123">Pascal</span></span>|`public class StreamReader { ... }`|  
|<span data-ttu-id="6c123-124">Interface</span><span class="sxs-lookup"><span data-stu-id="6c123-124">Interface</span></span>|<span data-ttu-id="6c123-125">Pascal</span><span class="sxs-lookup"><span data-stu-id="6c123-125">Pascal</span></span>|`public interface IEnumerable { ... }`|  
|<span data-ttu-id="6c123-126">Méthode</span><span class="sxs-lookup"><span data-stu-id="6c123-126">Method</span></span>|<span data-ttu-id="6c123-127">Pascal</span><span class="sxs-lookup"><span data-stu-id="6c123-127">Pascal</span></span>|`public class Object {` <br />  `public virtual string ToString();` <br /> `}`|  
|<span data-ttu-id="6c123-128">Propriété</span><span class="sxs-lookup"><span data-stu-id="6c123-128">Property</span></span>|<span data-ttu-id="6c123-129">Pascal</span><span class="sxs-lookup"><span data-stu-id="6c123-129">Pascal</span></span>|`public class String {` <br />  `public int Length { get; }` <br /> `}`|  
|<span data-ttu-id="6c123-130">Événement</span><span class="sxs-lookup"><span data-stu-id="6c123-130">Event</span></span>|<span data-ttu-id="6c123-131">Pascal</span><span class="sxs-lookup"><span data-stu-id="6c123-131">Pascal</span></span>|`public class Process {` <br />  `public event EventHandler Exited;` <br /> `}`|  
|<span data-ttu-id="6c123-132">Champ</span><span class="sxs-lookup"><span data-stu-id="6c123-132">Field</span></span>|<span data-ttu-id="6c123-133">Pascal</span><span class="sxs-lookup"><span data-stu-id="6c123-133">Pascal</span></span>|`public class MessageQueue {` <br />  `public static readonly TimeSpan` <br /> `InfiniteTimeout;` <br /> `}` <br /> `public struct UInt32 {` <br />  `public const Min = 0;` <br /> `}`|  
|<span data-ttu-id="6c123-134">Valeur enum</span><span class="sxs-lookup"><span data-stu-id="6c123-134">Enum value</span></span>|<span data-ttu-id="6c123-135">Pascal</span><span class="sxs-lookup"><span data-stu-id="6c123-135">Pascal</span></span>|`public enum FileMode {` <br />  `Append,` <br />  `...` <br /> `}`|  
|<span data-ttu-id="6c123-136">Paramètre</span><span class="sxs-lookup"><span data-stu-id="6c123-136">Parameter</span></span>|<span data-ttu-id="6c123-137">Camel</span><span class="sxs-lookup"><span data-stu-id="6c123-137">Camel</span></span>|`public class Convert {` <br />  `public static int ToInt32(string value);` <br /> `}`|  
  
## <a name="capitalizing-compound-words-and-common-terms"></a><span data-ttu-id="6c123-138">Tirant partis de la casse des mots composés et les termes courants</span><span class="sxs-lookup"><span data-stu-id="6c123-138">Capitalizing Compound Words and Common Terms</span></span>  
 <span data-ttu-id="6c123-139">La plupart des termes composés sont considérés comme des termes uniques à des fins de mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="6c123-139">Most compound terms are treated as single words for purposes of capitalization.</span></span>  
  
 <span data-ttu-id="6c123-140">**X N’UTILISEZ PAS DE MAJUSCULE** au début de chaque mot dans les mots composés dits fermés.</span><span class="sxs-lookup"><span data-stu-id="6c123-140">**X DO NOT** capitalize each word in so-called closed-form compound words.</span></span>  
  
 <span data-ttu-id="6c123-141">Il s’agit des mots composés écrites sous la forme d’un mot unique, comme point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="6c123-141">These are compound words written as a single word, such as endpoint.</span></span> <span data-ttu-id="6c123-142">Pour les besoins de recommandations de la casse, traiter un fermeture mot composé comme un mot unique.</span><span class="sxs-lookup"><span data-stu-id="6c123-142">For the purpose of casing guidelines, treat a closed-form compound word as a single word.</span></span> <span data-ttu-id="6c123-143">Utiliser un dictionnaire en cours pour déterminer si un mot composé est écrit dans une forme fermée.</span><span class="sxs-lookup"><span data-stu-id="6c123-143">Use a current dictionary to determine if a compound word is written in closed form.</span></span>  
  
|<span data-ttu-id="6c123-144">Pascal</span><span class="sxs-lookup"><span data-stu-id="6c123-144">Pascal</span></span>|<span data-ttu-id="6c123-145">Camel</span><span class="sxs-lookup"><span data-stu-id="6c123-145">Camel</span></span>|<span data-ttu-id="6c123-146">Ne convient pas</span><span class="sxs-lookup"><span data-stu-id="6c123-146">Not</span></span>|  
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
|`Placeholder`|`placeholder`|`PlaceHolder`|  
|`SignIn`|`signIn`|`SignOn`|  
|`SignOut`|`signOut`|`SignOff`|  
|`UserName`|`userName`|`Username`|  
|`WhiteSpace`|`whiteSpace`|`Whitespace`|  
|`Writable`|`writable`|`Writeable`|  
  
## <a name="case-sensitivity"></a><span data-ttu-id="6c123-147">Respect de la casse</span><span class="sxs-lookup"><span data-stu-id="6c123-147">Case Sensitivity</span></span>  
 <span data-ttu-id="6c123-148">Les langages qui peuvent s’exécuter sur le CLR n’ont pas l’obligation de prendre en charge le respect de la casse, bien que certains le fassent.</span><span class="sxs-lookup"><span data-stu-id="6c123-148">Languages that can run on the CLR are not required to support case-sensitivity, although some do.</span></span> <span data-ttu-id="6c123-149">Même si votre langage le prend en charge, d'autres langages qui pourraient accéder à votre framework ne le font pas.</span><span class="sxs-lookup"><span data-stu-id="6c123-149">Even if your language supports it, other languages that might access your framework do not.</span></span> <span data-ttu-id="6c123-150">Les API qui sont accessibles de l'extérieur ne peuvent donc pas se fier uniquement à la casse pour distinguer deux noms dans le même contexte.</span><span class="sxs-lookup"><span data-stu-id="6c123-150">Any APIs that are externally accessible, therefore, cannot rely on case alone to distinguish between two names in the same context.</span></span>  
  
 <span data-ttu-id="6c123-151">**X NE SUPPOSEZ PAS** que tous les langages de programmation respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="6c123-151">**X DO NOT** assume that all programming languages are case sensitive.</span></span> <span data-ttu-id="6c123-152">Ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="6c123-152">They are not.</span></span> <span data-ttu-id="6c123-153">Les noms ne peuvent pas différer seulement par la casse.</span><span class="sxs-lookup"><span data-stu-id="6c123-153">Names cannot differ by case alone.</span></span>  
  
 <span data-ttu-id="6c123-154">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="6c123-154">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="6c123-155">*Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="6c123-155">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c123-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c123-156">See also</span></span>

- [<span data-ttu-id="6c123-157">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="6c123-157">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="6c123-158">Directives de nommage</span><span class="sxs-lookup"><span data-stu-id="6c123-158">Naming Guidelines</span></span>](../../../docs/standard/design-guidelines/naming-guidelines.md)
