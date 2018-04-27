---
title: Structure de programme et conventions de codage (Visual Basic)
ms.custom: ''
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- coding conventions
- Visual Basic code, coding conventions
- coding conventions [Visual Basic], Visual Basic
- programs [Visual Basic], structure
- program structure [Visual Basic]
- naming conventions [Visual Basic], Visual Basic
- best practices [Visual Basic], coding conventions
- conventions [Visual Basic], Visual Basic coding
- Visual Basic code
- programming [Visual Basic], Visual Basic coding conventions
ms.assetid: dd9be76f-6944-4e78-ad72-0b6084a3fc13
caps.latest.revision: 21
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 9980a815d83b21214f1be441d641c3da38c1b541
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="program-structure-and-code-conventions-visual-basic"></a><span data-ttu-id="4bd71-102">Structure de programme et conventions de codage (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4bd71-102">Program Structure and Code Conventions (Visual Basic)</span></span>
<span data-ttu-id="4bd71-103">Cette section présente la structure de programme Visual Basic classique, offre un programme Visual Basic simple, « Hello, World » et décrit les conventions de code Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4bd71-103">This section introduces the typical Visual Basic program structure, provides a simple Visual Basic program, "Hello, World", and discusses Visual Basic code conventions.</span></span> <span data-ttu-id="4bd71-104">Conventions de code sont des suggestions qui reposent pas sur la logique d’un programme mais sur sa structure physique et son apparence.</span><span class="sxs-lookup"><span data-stu-id="4bd71-104">Code conventions are suggestions that focus not on a program's logic but on its physical structure and appearance.</span></span> <span data-ttu-id="4bd71-105">Suivant les rend plus faciles à lire, comprendre et gérer votre code.</span><span class="sxs-lookup"><span data-stu-id="4bd71-105">Following them makes your code easier to read, understand, and maintain.</span></span> <span data-ttu-id="4bd71-106">Conventions de code incluent, entre autres :</span><span class="sxs-lookup"><span data-stu-id="4bd71-106">Code conventions can include, among others:</span></span>  
  
-   <span data-ttu-id="4bd71-107">Formats normalisés pour l’étiquetage et les commentaires de code.</span><span class="sxs-lookup"><span data-stu-id="4bd71-107">Standardized formats for labeling and commenting code.</span></span>  
  
-   <span data-ttu-id="4bd71-108">Instructions pour l’espacement, la mise en forme et la mise en retrait du code.</span><span class="sxs-lookup"><span data-stu-id="4bd71-108">Guidelines for spacing, formatting, and indenting code.</span></span>  
  
-   <span data-ttu-id="4bd71-109">Conventions d’affectation de noms pour les objets, des variables et des procédures.</span><span class="sxs-lookup"><span data-stu-id="4bd71-109">Naming conventions for objects, variables, and procedures.</span></span>  
  
 <span data-ttu-id="4bd71-110">Les rubriques suivantes présentent un ensemble d’instructions de programmation pour les programmes Visual Basic, ainsi que des exemples d’utilisation appropriée.</span><span class="sxs-lookup"><span data-stu-id="4bd71-110">The following topics present a set of programming guidelines for Visual Basic programs, along with examples of good usage.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="4bd71-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="4bd71-111">In This Section</span></span>  
 [<span data-ttu-id="4bd71-112">Structure d’un programme Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4bd71-112">Structure of a Visual Basic Program</span></span>](../../../visual-basic/programming-guide/program-structure/structure-of-a-visual-basic-program.md)  
 <span data-ttu-id="4bd71-113">Fournit une vue d’ensemble des éléments qui composent un programme Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4bd71-113">Provides an overview of the elements that make up a Visual Basic program.</span></span>  
  
 [<span data-ttu-id="4bd71-114">Procédure Main dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4bd71-114">Main Procedure in Visual Basic</span></span>](../../../visual-basic/programming-guide/program-structure/main-procedure.md)  
 <span data-ttu-id="4bd71-115">Décrit la procédure qui sert le démarrage du point de contrôle général pour votre application.</span><span class="sxs-lookup"><span data-stu-id="4bd71-115">Discusses the procedure that serves as the starting point and overall control for your application.</span></span>  
  
 [<span data-ttu-id="4bd71-116">Références et l’instruction Imports</span><span class="sxs-lookup"><span data-stu-id="4bd71-116">References and the Imports Statement</span></span>](../../../visual-basic/programming-guide/program-structure/references-and-the-imports-statement.md)  
 <span data-ttu-id="4bd71-117">Explique comment référencer des objets dans d’autres assemblys.</span><span class="sxs-lookup"><span data-stu-id="4bd71-117">Discusses how to reference objects in other assemblies.</span></span>  
  
 [<span data-ttu-id="4bd71-118">Espaces de noms dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4bd71-118">Namespaces in Visual Basic</span></span>](../../../visual-basic/programming-guide/program-structure/namespaces.md)  
 <span data-ttu-id="4bd71-119">Décrit comment les espaces de noms organisent les objets dans les assemblys.</span><span class="sxs-lookup"><span data-stu-id="4bd71-119">Describes how namespaces organize objects within assemblies.</span></span>  
  
 [<span data-ttu-id="4bd71-120">Conventions d’affectation de noms de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4bd71-120">Visual Basic Naming Conventions</span></span>](../../../visual-basic/programming-guide/program-structure/naming-conventions.md)  
 <span data-ttu-id="4bd71-121">Comprend des instructions générales de nommer les procédures, de constantes, variables, arguments et objets.</span><span class="sxs-lookup"><span data-stu-id="4bd71-121">Includes general guidelines for naming procedures, constants, variables, arguments, and objects.</span></span>  
  
 [<span data-ttu-id="4bd71-122">Conventions de codage Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4bd71-122">Visual Basic Coding Conventions</span></span>](../../../visual-basic/programming-guide/program-structure/coding-conventions.md)  
 <span data-ttu-id="4bd71-123">Passe en revue les instructions utilisées pour le développement des exemples de cette documentation.</span><span class="sxs-lookup"><span data-stu-id="4bd71-123">Reviews the guidelines used in developing the samples in this documentation.</span></span>  
  
 [<span data-ttu-id="4bd71-124">Compilation conditionnelle</span><span class="sxs-lookup"><span data-stu-id="4bd71-124">Conditional Compilation</span></span>](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)  
 <span data-ttu-id="4bd71-125">Décrit comment compiler sélectivement des blocs de code spécifiques tout en demandant au compilateur d’ignorer d’autres.</span><span class="sxs-lookup"><span data-stu-id="4bd71-125">Describes how to compile particular blocks of code selectively while directing the compiler to ignore others.</span></span>  
  
 [<span data-ttu-id="4bd71-126">Guide pratique : diviser et combiner des instructions dans le code</span><span class="sxs-lookup"><span data-stu-id="4bd71-126">How to: Break and Combine Statements in Code</span></span>](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)  
 <span data-ttu-id="4bd71-127">Montre comment répartir les instructions longues sur plusieurs lignes et associer des instructions courtes sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="4bd71-127">Shows how to divide long statements into multiple lines and combine short statements on one line.</span></span>  
  
 [<span data-ttu-id="4bd71-128">Guide pratique : réduire et masquer des sections de code</span><span class="sxs-lookup"><span data-stu-id="4bd71-128">How to: Collapse and Hide Sections of Code</span></span>](../../../visual-basic/programming-guide/program-structure/how-to-collapse-and-hide-sections-of-code.md)  
 <span data-ttu-id="4bd71-129">Montre comment réduire et masquer des sections de code dans Visual Basic éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="4bd71-129">Shows how to collapse and hide sections of code in the Visual Basic code editor.</span></span>  
  
 [<span data-ttu-id="4bd71-130">Guide pratique : étiqueter des instructions</span><span class="sxs-lookup"><span data-stu-id="4bd71-130">How to: Label Statements</span></span>](../../../visual-basic/programming-guide/program-structure/how-to-label-statements.md)  
 <span data-ttu-id="4bd71-131">Montre comment marquer une ligne de code pour identifier pour une utilisation avec des instructions telles que `On Error Goto`.</span><span class="sxs-lookup"><span data-stu-id="4bd71-131">Shows how to mark a line of code to identify it for use with statements such as `On Error Goto`.</span></span>  
  
 [<span data-ttu-id="4bd71-132">Caractères spéciaux dans le code</span><span class="sxs-lookup"><span data-stu-id="4bd71-132">Special Characters in Code</span></span>](../../../visual-basic/programming-guide/program-structure/special-characters-in-code.md)  
 <span data-ttu-id="4bd71-133">Explique comment et où utiliser des caractères non numériques et non alphabétiques.</span><span class="sxs-lookup"><span data-stu-id="4bd71-133">Shows how and where to use non-numeric and non-alphabetic characters.</span></span>  
  
 [<span data-ttu-id="4bd71-134">Commentaires dans le code</span><span class="sxs-lookup"><span data-stu-id="4bd71-134">Comments in Code</span></span>](../../../visual-basic/programming-guide/program-structure/comments-in-code.md)  
 <span data-ttu-id="4bd71-135">Explique comment ajouter des commentaires descriptifs à votre code.</span><span class="sxs-lookup"><span data-stu-id="4bd71-135">Discusses how to add descriptive comments to your code.</span></span>  
  
 [<span data-ttu-id="4bd71-136">Utilisation des mots clés comme noms d’éléments dans le code</span><span class="sxs-lookup"><span data-stu-id="4bd71-136">Keywords as Element Names in Code</span></span>](../../../visual-basic/programming-guide/program-structure/keywords-as-element-names-in-code.md)  
 <span data-ttu-id="4bd71-137">Décrit comment utiliser des crochets (`[]`) pour délimiter les noms de variables qui sont également des mots clés Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4bd71-137">Describes how to use brackets (`[]`) to delimit variable names that are also Visual Basic keywords.</span></span>  
  
 [<span data-ttu-id="4bd71-138">Me, My, MyBase et MyClass</span><span class="sxs-lookup"><span data-stu-id="4bd71-138">Me, My, MyBase, and MyClass</span></span>](../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)  
 <span data-ttu-id="4bd71-139">Décrit les différentes façons de faire référence aux éléments d’un programme Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4bd71-139">Describes various ways to refer to elements of a Visual Basic program.</span></span>  
  
 [<span data-ttu-id="4bd71-140">Limitations de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4bd71-140">Visual Basic Limitations</span></span>](../../../visual-basic/programming-guide/program-structure/limitations.md)  
 <span data-ttu-id="4bd71-141">Traite de la suppression des limites connues du codage dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4bd71-141">Discusses the removal of known coding limits within Visual Basic.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="4bd71-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4bd71-142">Related Sections</span></span>  
 [<span data-ttu-id="4bd71-143">Conventions typographiques</span><span class="sxs-lookup"><span data-stu-id="4bd71-143">Typographic and Code Conventions</span></span>](../../../visual-basic/language-reference/typographic-and-code-conventions.md)  
 <span data-ttu-id="4bd71-144">Fournit les conventions de codage standard pour Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4bd71-144">Provides standard coding conventions for Visual Basic.</span></span>  
  
 [<span data-ttu-id="4bd71-145">Écriture de code</span><span class="sxs-lookup"><span data-stu-id="4bd71-145">Writing Code</span></span>](/visualstudio/ide/writing-code-in-the-code-and-text-editor)  
 <span data-ttu-id="4bd71-146">Décrit les fonctionnalités qui facilitent l’écriture et la gestion de votre code.</span><span class="sxs-lookup"><span data-stu-id="4bd71-146">Describes features that make it easier for you to write and manage your code.</span></span>
