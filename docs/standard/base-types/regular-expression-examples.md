---
title: Exemples d'expressions régulières
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- regular expressions [.NET Framework], examples
- regular expressions [.NET Framework]
- strings [.NET Framework], regular expressions
ms.assetid: e9fd53f2-ed56-4b09-b2ea-e9bc9d65e6d6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8fb58f8e7a1fef711de28534fbe53dfc9d7084ac
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="regular-expression-examples"></a><span data-ttu-id="e25ff-102">Exemples d'expressions régulières</span><span class="sxs-lookup"><span data-stu-id="e25ff-102">Regular Expression Examples</span></span>
<span data-ttu-id="e25ff-103">Cette section contient des exemples de code qui illustrent l’utilisation des expressions régulières dans des applications courantes.</span><span class="sxs-lookup"><span data-stu-id="e25ff-103">This section contains code examples that illustrate the use of regular expressions in common applications.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e25ff-104">L’espace de noms <xref:System.Web.RegularExpressions> contient un nombre d’objets d’expression régulière qui implémentent des modèles d’expression régulière prédéfinis pour l’analyse de chaînes provenant de documents HTML, XML et ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="e25ff-104">The <xref:System.Web.RegularExpressions> namespace contains a number of regular expression objects that implement predefined regular expression patterns for parsing strings from HTML, XML, and ASP.NET documents.</span></span> <span data-ttu-id="e25ff-105">Par exemple, la classe <xref:System.Web.RegularExpressions.TagRegex> identifie les balises de début d’une chaîne, tandis que la classe <xref:System.Web.RegularExpressions.CommentRegex> identifie les commentaires ASP.NET d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="e25ff-105">For example, the <xref:System.Web.RegularExpressions.TagRegex> class identifies start tags in a string and the <xref:System.Web.RegularExpressions.CommentRegex> class identifies ASP.NET comments in a string.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="e25ff-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e25ff-106">In This Section</span></span>  
 [<span data-ttu-id="e25ff-107">Exemple : recherche de valeurs HREF</span><span class="sxs-lookup"><span data-stu-id="e25ff-107">Example: Scanning for HREFs</span></span>](../../../docs/standard/base-types/regular-expression-example-scanning-for-hrefs.md)  
 <span data-ttu-id="e25ff-108">Fournit un exemple qui recherche une chaîne d’entrée et imprime toutes les valeurs href="…" et leurs emplacements dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="e25ff-108">Provides an example that searches an input string and prints out all the href="…" values and their locations in the string.</span></span>  
  
 [<span data-ttu-id="e25ff-109">Exemple : modification des formats de date</span><span class="sxs-lookup"><span data-stu-id="e25ff-109">Example: Changing Date Formats</span></span>](../../../docs/standard/base-types/regular-expression-example-changing-date-formats.md)  
 <span data-ttu-id="e25ff-110">Fournit un exemple qui remplace les dates au format mm/jj/aa par des dates au format jj-mm-aa.</span><span class="sxs-lookup"><span data-stu-id="e25ff-110">Provides an example that replaces dates in the form mm/dd/yy with dates in the form dd-mm-yy.</span></span>  
  
 [<span data-ttu-id="e25ff-111">Guide pratique pour extraire un protocole et un numéro de port d’une URL</span><span class="sxs-lookup"><span data-stu-id="e25ff-111">How to: Extract a Protocol and Port Number from a URL</span></span>](../../../docs/standard/base-types/how-to-extract-a-protocol-and-port-number-from-a-url.md)  
 <span data-ttu-id="e25ff-112">Fournit un exemple qui extrait un protocole et un numéro de port d’une chaîne qui contient une URL.</span><span class="sxs-lookup"><span data-stu-id="e25ff-112">Provides an example that extracts a protocol and port number from a string that contains a URL.</span></span> <span data-ttu-id="e25ff-113">Par exemple, « http://www.contoso.com:8080/letters/readme.html » retourne « http:8080 ».</span><span class="sxs-lookup"><span data-stu-id="e25ff-113">For example, "http://www.contoso.com:8080/letters/readme.html" returns "http:8080".</span></span>  
  
 [<span data-ttu-id="e25ff-114">Guide pratique pour supprimer des caractères non valides d’une chaîne</span><span class="sxs-lookup"><span data-stu-id="e25ff-114">How to: Strip Invalid Characters from a String</span></span>](../../../docs/standard/base-types/how-to-strip-invalid-characters-from-a-string.md)  
 <span data-ttu-id="e25ff-115">Fournit un exemple qui supprime les caractères non alphanumériques et non valides d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="e25ff-115">Provides an example that strips invalid non-alphanumeric characters from a string.</span></span>  
  
 [<span data-ttu-id="e25ff-116">Guide pratique pour vérifier que des chaînes sont dans un format d’adresse e-mail valide</span><span class="sxs-lookup"><span data-stu-id="e25ff-116">How to: Verify that Strings Are in Valid Email Format</span></span>](../../../docs/standard/base-types/how-to-verify-that-strings-are-in-valid-email-format.md)  
 <span data-ttu-id="e25ff-117">Fournit un exemple que vous pouvez utiliser pour vérifier qu’une chaîne est dans un format d’e-mail valide.</span><span class="sxs-lookup"><span data-stu-id="e25ff-117">Provides an example that you can use to verify that a string is in valid email format.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="e25ff-118">Référence</span><span class="sxs-lookup"><span data-stu-id="e25ff-118">Reference</span></span>  
 <xref:System.Text.RegularExpressions>  
 <span data-ttu-id="e25ff-119">Fournit des informations de référence sur les bibliothèques de classes pour l’espace de noms **System.Text.RegularExpressions** .NET.</span><span class="sxs-lookup"><span data-stu-id="e25ff-119">Provides class library reference information for the .NET **System.Text.RegularExpressions** namespace.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="e25ff-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e25ff-120">Related Sections</span></span>  
 [<span data-ttu-id="e25ff-121">Expressions régulières .NET</span><span class="sxs-lookup"><span data-stu-id="e25ff-121">.NET Regular Expressions</span></span>](../../../docs/standard/base-types/regular-expressions.md)  
 <span data-ttu-id="e25ff-122">Fournit une vue d’ensemble de l’aspect du langage de programmation des expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="e25ff-122">Provides an overview of the programming language aspect of regular expressions.</span></span>  
  
 [<span data-ttu-id="e25ff-123">Modèle objet d’expression régulière</span><span class="sxs-lookup"><span data-stu-id="e25ff-123">The Regular Expression Object Model</span></span>](../../../docs/standard/base-types/the-regular-expression-object-model.md)  
 <span data-ttu-id="e25ff-124">Décrit les classes d’expression régulière contenues dans l’espace de noms `System.Text.RegularExpression` et fournit des exemples de leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="e25ff-124">Describes the regular expression classes contained in the `System.Text.RegularExpression` namespace and provides examples of their use.</span></span>  
  
 [<span data-ttu-id="e25ff-125">Comportement détaillé des expressions régulières</span><span class="sxs-lookup"><span data-stu-id="e25ff-125">Details of Regular Expression Behavior</span></span>](../../../docs/standard/base-types/details-of-regular-expression-behavior.md)  
 <span data-ttu-id="e25ff-126">Fournit des informations sur les fonctionnalités et le comportement des expressions régulières .NET.</span><span class="sxs-lookup"><span data-stu-id="e25ff-126">Provides information about the capabilities and behavior of .NET regular expressions.</span></span>  
  
 [<span data-ttu-id="e25ff-127">Langage des expressions régulières - Aide-mémoire</span><span class="sxs-lookup"><span data-stu-id="e25ff-127">Regular Expression Language - Quick Reference</span></span>](../../../docs/standard/base-types/regular-expression-language-quick-reference.md)  
 <span data-ttu-id="e25ff-128">Fournit des informations sur le jeu de caractères, d'opérateurs et de constructions permettant de définir des expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="e25ff-128">Provides information on the set of characters, operators, and constructs that you can use to define regular expressions.</span></span>
