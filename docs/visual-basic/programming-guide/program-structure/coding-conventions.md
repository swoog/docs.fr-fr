---
title: Conventions de codage Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- coding conventions [Visual Basic], Visual Basic
- examples [Visual Basic], coding conventions
- Visual Basic code, conventions
ms.assetid: c1df130b-fec6-49a5-becf-0a7e494a1d0f
ms.openlocfilehash: f73648888b28c349104a70e78c29eb208d438b78
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58814560"
---
# <a name="visual-basic-coding-conventions"></a><span data-ttu-id="b5063-102">Conventions de codage Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b5063-102">Visual Basic Coding Conventions</span></span>
<span data-ttu-id="b5063-103">Microsoft développe des exemples et la documentation qui suivent les instructions de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="b5063-103">Microsoft develops samples and documentation that follow the guidelines in this topic.</span></span> <span data-ttu-id="b5063-104">Si vous suivez les mêmes conventions de codage, vous pouvez profiter des avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="b5063-104">If you follow the same coding conventions, you may gain the following benefits:</span></span>  
  
-   <span data-ttu-id="b5063-105">Votre code aura une apparence cohérente, afin que les lecteurs puissent mieux se concentrer sur le contenu, pas de disposition.</span><span class="sxs-lookup"><span data-stu-id="b5063-105">Your code will have a consistent look, so that readers can better focus on content, not layout.</span></span>  
  
-   <span data-ttu-id="b5063-106">Les lecteurs comprennent votre code plus rapidement, car ils peuvent faire des hypothèses selon leur expérience précédente.</span><span class="sxs-lookup"><span data-stu-id="b5063-106">Readers understand your code more quickly because they can make assumptions based on previous experience.</span></span>  
  
-   <span data-ttu-id="b5063-107">Vous pouvez copier, modifier et gérer le code plus facilement.</span><span class="sxs-lookup"><span data-stu-id="b5063-107">You can copy, change, and maintain the code more easily.</span></span>  
  
-   <span data-ttu-id="b5063-108">Vous assurer que votre code illustre les « meilleures pratiques » pour Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b5063-108">You help ensure that your code demonstrates "best practices" for Visual Basic.</span></span>  
  
## <a name="naming-conventions"></a><span data-ttu-id="b5063-109">Conventions d'affectation de noms</span><span class="sxs-lookup"><span data-stu-id="b5063-109">Naming Conventions</span></span>  
  
-   <span data-ttu-id="b5063-110">Pour plus d’informations sur les règles d’affectation de noms, consultez [instructions de dénomination de](../../../standard/design-guidelines/naming-guidelines.md) rubrique.</span><span class="sxs-lookup"><span data-stu-id="b5063-110">For information about naming guidelines, see [Naming Guidelines](../../../standard/design-guidelines/naming-guidelines.md) topic.</span></span>  
  
-   <span data-ttu-id="b5063-111">N’utilisez pas « Mon » ou « my » en tant que partie d’un nom de variable.</span><span class="sxs-lookup"><span data-stu-id="b5063-111">Do not use "My" or "my" as part of a variable name.</span></span> <span data-ttu-id="b5063-112">Cette pratique peut créer une confusion avec les `My` objets.</span><span class="sxs-lookup"><span data-stu-id="b5063-112">This practice creates confusion with the `My` objects.</span></span>  
  
-   <span data-ttu-id="b5063-113">Il est inutile de modifier les noms des objets dans le code généré automatiquement pour les rendre conformes aux indications.</span><span class="sxs-lookup"><span data-stu-id="b5063-113">You do not have to change the names of objects in auto-generated code to make them fit the guidelines.</span></span>  
  
## <a name="layout-conventions"></a><span data-ttu-id="b5063-114">Conventions de disposition</span><span class="sxs-lookup"><span data-stu-id="b5063-114">Layout Conventions</span></span>  
  
-   <span data-ttu-id="b5063-115">Insérez les tabulations en tant qu’espaces et utilisez la mise en retrait intelligente avec des retraits de quatre espaces.</span><span class="sxs-lookup"><span data-stu-id="b5063-115">Insert tabs as spaces, and use smart indenting with four-space indents.</span></span>  
  
-   <span data-ttu-id="b5063-116">Utilisez **code (Reformatage) de listing en mode Pretty** à remettre en forme votre code dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="b5063-116">Use **Pretty listing (reformatting) of code** to reformat your code in the code editor.</span></span> <span data-ttu-id="b5063-117">Pour plus d’informations, consultez [Options, éditeur de texte, base (Visual Basic)](/visualstudio/ide/reference/options-text-editor-basic-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="b5063-117">For more information, see [Options, Text Editor, Basic (Visual Basic)](/visualstudio/ide/reference/options-text-editor-basic-visual-basic).</span></span>  
  
-   <span data-ttu-id="b5063-118">Utiliser une seule instruction par ligne.</span><span class="sxs-lookup"><span data-stu-id="b5063-118">Use only one statement per line.</span></span> <span data-ttu-id="b5063-119">N’utilisez pas le caractère de séparation de ligne Visual Basic ( :)).</span><span class="sxs-lookup"><span data-stu-id="b5063-119">Don't use the Visual Basic line separator character (:).</span></span>  
  
-   <span data-ttu-id="b5063-120">Évitez d’utiliser le caractère de continuation de ligne explicite « _ » en faveur de la continuation de ligne implicite partout où le langage le permet.</span><span class="sxs-lookup"><span data-stu-id="b5063-120">Avoid using the explicit line continuation character "_" in favor of implicit line continuation wherever the language allows it.</span></span>  
  
-   <span data-ttu-id="b5063-121">Utiliser une seule déclaration par ligne.</span><span class="sxs-lookup"><span data-stu-id="b5063-121">Use only one declaration per line.</span></span>  
  
-   <span data-ttu-id="b5063-122">Si **code (Reformatage) de listing en mode Pretty** ne format des lignes de continuation automatiquement, manuellement mettre en retrait continuation lignes un taquet de tabulation.</span><span class="sxs-lookup"><span data-stu-id="b5063-122">If **Pretty listing (reformatting) of code** doesn't format continuation lines automatically, manually indent continuation lines one tab stop.</span></span> <span data-ttu-id="b5063-123">Toutefois, toujours aligner à gauche des éléments dans une liste.</span><span class="sxs-lookup"><span data-stu-id="b5063-123">However, always left-align items in a list.</span></span>  
  
    ```  
    a As Integer,  
    b As Integer  
    ```  
  
-   <span data-ttu-id="b5063-124">Ajoutez au moins une ligne vide entre les définitions de méthode et la propriété.</span><span class="sxs-lookup"><span data-stu-id="b5063-124">Add at least one blank line between method and property definitions.</span></span>  
  
## <a name="commenting-conventions"></a><span data-ttu-id="b5063-125">Conventions de commentaires</span><span class="sxs-lookup"><span data-stu-id="b5063-125">Commenting Conventions</span></span>  
  
-   <span data-ttu-id="b5063-126">Placez les commentaires sur une ligne distincte, et non à la fin d’une ligne de code.</span><span class="sxs-lookup"><span data-stu-id="b5063-126">Put comments on a separate line instead of at the end of a line of code.</span></span>  
  
-   <span data-ttu-id="b5063-127">Démarrer le texte de commentaire par une lettre majuscule et texte de commentaire de fin par un point.</span><span class="sxs-lookup"><span data-stu-id="b5063-127">Start comment text with an uppercase letter, and end comment text with a period.</span></span>  
  
-   <span data-ttu-id="b5063-128">Insérer un espace entre le délimiteur de commentaire (') et le texte du commentaire.</span><span class="sxs-lookup"><span data-stu-id="b5063-128">Insert one space between the comment delimiter (') and the comment text.</span></span>  
  
     [!code-vb[VbVbalrGuidelines#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#2)]  
  
-   <span data-ttu-id="b5063-129">N’entourez pas les commentaires avec des blocs d’astérisques mis en forme.</span><span class="sxs-lookup"><span data-stu-id="b5063-129">Do not surround comments with formatted blocks of asterisks.</span></span>  
  
## <a name="program-structure"></a><span data-ttu-id="b5063-130">Structure du programme</span><span class="sxs-lookup"><span data-stu-id="b5063-130">Program Structure</span></span>  
  
-   <span data-ttu-id="b5063-131">Lorsque vous utilisez le `Main` (méthode), utilisez la construction par défaut pour les nouvelles applications de console et `My` pour les arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="b5063-131">When you use the `Main` method, use the default construct for new console applications, and use `My` for command-line arguments.</span></span>  
  
     [!code-vb[VbVbalrGuidelines#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#3)]  
  
## <a name="language-guidelines"></a><span data-ttu-id="b5063-132">Directives du langage</span><span class="sxs-lookup"><span data-stu-id="b5063-132">Language Guidelines</span></span>  
  
### <a name="string-data-type"></a><span data-ttu-id="b5063-133">String, type de données</span><span class="sxs-lookup"><span data-stu-id="b5063-133">String Data Type</span></span>  
  
-   <span data-ttu-id="b5063-134">Pour concaténer des chaînes, utilisez une esperluette (&).</span><span class="sxs-lookup"><span data-stu-id="b5063-134">To concatenate strings, use an ampersand (&).</span></span>  
  
     [!code-vb[VbVbalrGuidelines#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#4)]  
  
-   <span data-ttu-id="b5063-135">Pour ajouter des chaînes dans des boucles, utilisez le <xref:System.Text.StringBuilder> objet.</span><span class="sxs-lookup"><span data-stu-id="b5063-135">To append strings in loops, use the <xref:System.Text.StringBuilder> object.</span></span>  
  
     [!code-vb[VbVbalrGuidelines#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#5)]  
  
### <a name="relaxed-delegates-in-event-handlers"></a><span data-ttu-id="b5063-136">Délégués souples dans les gestionnaires d’événements</span><span class="sxs-lookup"><span data-stu-id="b5063-136">Relaxed Delegates in Event Handlers</span></span>  
 <span data-ttu-id="b5063-137">Ne sont pas explicitement éligibles les arguments (objet et EventArgs) aux gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="b5063-137">Do not explicitly qualify the arguments (Object and EventArgs) to event handlers.</span></span> <span data-ttu-id="b5063-138">Si vous n’utilisez pas les arguments d’événement sont passés à un événement (par exemple, l’expéditeur en tant qu’objet, e pour EventArgs), utilisez les délégués simplifiés et omettez les arguments d’événement dans votre code :</span><span class="sxs-lookup"><span data-stu-id="b5063-138">If you are not using the event arguments that are passed to an event (for example, sender as Object, e as EventArgs), use relaxed delegates, and leave out the event arguments in your code:</span></span>  
  
 [!code-vb[VbVbalrGuidelines#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#7)]  
  
### <a name="unsigned-data-type"></a><span data-ttu-id="b5063-139">Type de données non signé</span><span class="sxs-lookup"><span data-stu-id="b5063-139">Unsigned Data Type</span></span>  
  
-   <span data-ttu-id="b5063-140">Utilisez `Integer` plutôt que des types non signés, sauf s’ils sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="b5063-140">Use `Integer` rather than unsigned types, except where they are necessary.</span></span>  
  
### <a name="arrays"></a><span data-ttu-id="b5063-141">Tableaux</span><span class="sxs-lookup"><span data-stu-id="b5063-141">Arrays</span></span>  
  
-   <span data-ttu-id="b5063-142">Utilisez la syntaxe concise lorsque vous initialisez des tableaux sur la ligne de déclaration.</span><span class="sxs-lookup"><span data-stu-id="b5063-142">Use the short syntax when you initialize arrays on the declaration line.</span></span> <span data-ttu-id="b5063-143">Par exemple, utilisez la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="b5063-143">For example, use the following syntax.</span></span>  
  
     [!code-vb[VbVbalrGuidelines#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#8)]  
  
     <span data-ttu-id="b5063-144">N’utilisez pas la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="b5063-144">Do not use the following syntax.</span></span>  
  
     [!code-vb[VbVbalrGuidelines#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#9)]  
  
-   <span data-ttu-id="b5063-145">Placez l’indicateur de tableau sur le type, et non sur la variable.</span><span class="sxs-lookup"><span data-stu-id="b5063-145">Put the array designator on the type, not on the variable.</span></span> <span data-ttu-id="b5063-146">Par exemple, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b5063-146">For example, use the following syntax:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#11)]  
  
     <span data-ttu-id="b5063-147">N’utilisez pas la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b5063-147">Do not use the following syntax:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#10)]  
  
-   <span data-ttu-id="b5063-148">Utilisez la syntaxe {} lorsque vous déclarez et initialisez des tableaux de types de base de données.</span><span class="sxs-lookup"><span data-stu-id="b5063-148">Use the { } syntax when you declare and initialize arrays of basic data types.</span></span> <span data-ttu-id="b5063-149">Par exemple, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b5063-149">For example, use the following syntax:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#12)]  
  
     <span data-ttu-id="b5063-150">N’utilisez pas la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b5063-150">Do not use the following syntax:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#13)]  
  
### <a name="use-the-with-keyword"></a><span data-ttu-id="b5063-151">Utilisez le mot clé</span><span class="sxs-lookup"><span data-stu-id="b5063-151">Use the With Keyword</span></span>  
 <span data-ttu-id="b5063-152">Lorsque vous effectuez une série d’appels à un objet, envisagez d’utiliser le `With` mot clé :</span><span class="sxs-lookup"><span data-stu-id="b5063-152">When you make a series of calls to one object, consider using the `With` keyword:</span></span>  
  
 [!code-vb[VbVbalrGuidelines#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#15)]  
  
### <a name="use-the-trycatch-and-using-statements-when-you-use-exception-handling"></a><span data-ttu-id="b5063-153">Utilisez les instructions Try... Catch et les instructions Using lorsque vous utilisez la gestion des exceptions</span><span class="sxs-lookup"><span data-stu-id="b5063-153">Use the Try...Catch and Using Statements when you use Exception Handling</span></span>  
 <span data-ttu-id="b5063-154">N’utilisez pas `On Error Goto`.</span><span class="sxs-lookup"><span data-stu-id="b5063-154">Do not use `On Error Goto`.</span></span>  
  
### <a name="use-the-isnot-keyword"></a><span data-ttu-id="b5063-155">Utilisez le mot clé IsNot</span><span class="sxs-lookup"><span data-stu-id="b5063-155">Use the IsNot Keyword</span></span>  
 <span data-ttu-id="b5063-156">Utilisez le `IsNot` mot clé au lieu de `Not...Is Nothing`.</span><span class="sxs-lookup"><span data-stu-id="b5063-156">Use the `IsNot` keyword instead of `Not...Is Nothing`.</span></span>  
  
### <a name="new-keyword"></a><span data-ttu-id="b5063-157">Nouveau mot clé</span><span class="sxs-lookup"><span data-stu-id="b5063-157">New Keyword</span></span>  
  
-   <span data-ttu-id="b5063-158">Utilisez l’instanciation courte.</span><span class="sxs-lookup"><span data-stu-id="b5063-158">Use short instantiation.</span></span> <span data-ttu-id="b5063-159">Par exemple, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b5063-159">For example, use the following syntax:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#21](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#21)]  
  
     <span data-ttu-id="b5063-160">La ligne précédente est équivalente à ceci :</span><span class="sxs-lookup"><span data-stu-id="b5063-160">The preceding line is equivalent to this:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#22](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#22)]  
  
-   <span data-ttu-id="b5063-161">Utilisez des initialiseurs d’objets pour les nouveaux objets au lieu du constructeur sans paramètre :</span><span class="sxs-lookup"><span data-stu-id="b5063-161">Use object initializers for new objects instead of the parameterless constructor:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#23)]  
  
### <a name="event-handling"></a><span data-ttu-id="b5063-162">Gestion des événements</span><span class="sxs-lookup"><span data-stu-id="b5063-162">Event Handling</span></span>  
  
-   <span data-ttu-id="b5063-163">Utilisez `Handles` plutôt que `AddHandler`:</span><span class="sxs-lookup"><span data-stu-id="b5063-163">Use `Handles` rather than `AddHandler`:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#24](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#24)]  
  
-   <span data-ttu-id="b5063-164">Utilisez `AddressOf`et n’instanciez pas le délégué explicitement :</span><span class="sxs-lookup"><span data-stu-id="b5063-164">Use `AddressOf`, and do not instantiate the delegate explicitly:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#25](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#25)]  
  
-   <span data-ttu-id="b5063-165">Lorsque vous définissez un événement, utilisez la syntaxe concise et laissez le compilateur définir le délégué :</span><span class="sxs-lookup"><span data-stu-id="b5063-165">When you define an event, use the short syntax, and let the compiler define the delegate:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#26](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#26)]  
  
-   <span data-ttu-id="b5063-166">Ne pas vérifier si un événement est `Nothing` (null) avant d’appeler le `RaiseEvent` (méthode).</span><span class="sxs-lookup"><span data-stu-id="b5063-166">Do not verify whether an event is `Nothing` (null) before you call the `RaiseEvent` method.</span></span> <span data-ttu-id="b5063-167">`RaiseEvent` vérifie les `Nothing` avant de déclencher l’événement.</span><span class="sxs-lookup"><span data-stu-id="b5063-167">`RaiseEvent` checks for `Nothing` before it raises the event.</span></span>  
  
### <a name="using-shared-members"></a><span data-ttu-id="b5063-168">À l’aide des membres partagés</span><span class="sxs-lookup"><span data-stu-id="b5063-168">Using Shared Members</span></span>  
 <span data-ttu-id="b5063-169">Appelez `Shared` membres en utilisant le nom de classe, pas à partir d’une variable d’instance.</span><span class="sxs-lookup"><span data-stu-id="b5063-169">Call `Shared` members by using the class name, not from an instance variable.</span></span>  
  
### <a name="use-xml-literals"></a><span data-ttu-id="b5063-170">Utiliser des littéraux XML</span><span class="sxs-lookup"><span data-stu-id="b5063-170">Use XML Literals</span></span>  
 <span data-ttu-id="b5063-171">Les littéraux XML simplifient les tâches les plus courantes que vous rencontrez lorsque vous utilisez XML (par exemple, charge, requête et transformation).</span><span class="sxs-lookup"><span data-stu-id="b5063-171">XML literals simplify the most common tasks that you encounter when you work with XML (for example, load, query, and transform).</span></span> <span data-ttu-id="b5063-172">Lorsque vous développez avec XML, suivez ces instructions :</span><span class="sxs-lookup"><span data-stu-id="b5063-172">When you develop with XML, follow these guidelines:</span></span>  
  
-   <span data-ttu-id="b5063-173">Utiliser des littéraux XML pour créer des documents XML et des fragments au lieu d’appeler directement les API XML.</span><span class="sxs-lookup"><span data-stu-id="b5063-173">Use XML literals to create XML documents and fragments instead of calling XML APIs directly.</span></span>  
  
-   <span data-ttu-id="b5063-174">Importez les espaces de noms XML au niveau du fichier ou du projet pour tirer parti des optimisations des performances des littéraux XML.</span><span class="sxs-lookup"><span data-stu-id="b5063-174">Import XML namespaces at the file or project level to take advantage of the performance optimizations for XML literals.</span></span>  
  
-   <span data-ttu-id="b5063-175">Utilisez les propriétés d’axe XML pour accéder aux éléments et attributs dans un document XML.</span><span class="sxs-lookup"><span data-stu-id="b5063-175">Use the XML axis properties to access elements and attributes in an XML document.</span></span>  
  
-   <span data-ttu-id="b5063-176">Utiliser des expressions incorporées pour inclure des valeurs et créer du code XML à partir de valeurs existantes au lieu d’utiliser des appels d’API tels que le `Add` méthode :</span><span class="sxs-lookup"><span data-stu-id="b5063-176">Use embedded expressions to include values and to create XML from existing values instead of using API calls such as the `Add` method:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#27)]  
  
### <a name="linq-queries"></a><span data-ttu-id="b5063-177">Requêtes LINQ</span><span class="sxs-lookup"><span data-stu-id="b5063-177">LINQ Queries</span></span>  
  
-   <span data-ttu-id="b5063-178">Utiliser des noms significatifs pour les variables de requête :</span><span class="sxs-lookup"><span data-stu-id="b5063-178">Use meaningful names for query variables:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#28)]  
  
-   <span data-ttu-id="b5063-179">Fournir des noms pour les éléments d’une requête pour vous assurer que les noms de propriété des types anonymes sont correctement capitalisés à l’aide de la casse Pascal casse :</span><span class="sxs-lookup"><span data-stu-id="b5063-179">Provide names for elements in a query to make sure that property names of anonymous types are correctly capitalized using Pascal casing:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#29](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#29)]  
  
-   <span data-ttu-id="b5063-180">Renommez les propriétés lorsque les noms de propriétés dans le résultat sont ambigus.</span><span class="sxs-lookup"><span data-stu-id="b5063-180">Rename properties when the property names in the result would be ambiguous.</span></span> <span data-ttu-id="b5063-181">Par exemple, si votre requête retourne un client nom et un ID de commande, renommez-les au lieu de les laisser au format `Name` et `ID` dans le résultat :</span><span class="sxs-lookup"><span data-stu-id="b5063-181">For example, if your query returns a customer name and an order ID, rename them instead of leaving them as `Name` and `ID` in the result:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#30](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#30)]  
  
-   <span data-ttu-id="b5063-182">Utiliser l’inférence de type dans la déclaration des variables de requête et des variables de portée :</span><span class="sxs-lookup"><span data-stu-id="b5063-182">Use type inference in the declaration of query variables and range variables:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#31](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#31)]  
  
-   <span data-ttu-id="b5063-183">Alignez les clauses de requête sous la `From` instruction :</span><span class="sxs-lookup"><span data-stu-id="b5063-183">Align query clauses under the `From` statement:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#32](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#32)]  
  
-   <span data-ttu-id="b5063-184">Utilisez `Where` clauses avant les autres clauses de requête afin que les clauses de requête ultérieures opèrent sur l’ensemble filtré de données :</span><span class="sxs-lookup"><span data-stu-id="b5063-184">Use `Where` clauses before other query clauses so that later query clauses operate on the filtered set of data:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#33](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#33)]  
  
-   <span data-ttu-id="b5063-185">Utilisez le `Join` clause pour définir explicitement une opération de jointure au lieu d’utiliser le `Where` clause définir implicitement une opération de jointure :</span><span class="sxs-lookup"><span data-stu-id="b5063-185">Use the `Join` clause to explicitly define a join operation instead of using the `Where` clause to implicitly define a join operation:</span></span>  
  
     [!code-vb[VbVbalrGuidelines#34](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#34)]  
  
## <a name="see-also"></a><span data-ttu-id="b5063-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5063-186">See also</span></span>

- [<span data-ttu-id="b5063-187">Instructions de codage sécurisé</span><span class="sxs-lookup"><span data-stu-id="b5063-187">Secure Coding Guidelines</span></span>](../../../standard/security/secure-coding-guidelines.md)
