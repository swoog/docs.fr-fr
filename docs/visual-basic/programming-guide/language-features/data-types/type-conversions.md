---
title: Conversions de type en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- conversions [Visual Basic], type
- data types [Visual Basic], changing
- variables [Visual Basic], changing data type
- type conversion [Visual Basic]
- conversions [Visual Basic], data type
- changing data types [Visual Basic]
- data type conversion [Visual Basic]
ms.assetid: 1cdacd21-ba31-4b62-b5be-395e41eeaa17
ms.openlocfilehash: 026b2a250abfac0782feb0946bc50a94f504f7ed
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61663282"
---
# <a name="type-conversions-in-visual-basic"></a><span data-ttu-id="d257b-102">Conversions de type en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d257b-102">Type Conversions in Visual Basic</span></span>
<span data-ttu-id="d257b-103">Le processus de modification d’une valeur à partir d’un type de données à un autre type est appelé *conversion*.</span><span class="sxs-lookup"><span data-stu-id="d257b-103">The process of changing a value from one data type to another type is called *conversion*.</span></span> <span data-ttu-id="d257b-104">Les conversions sont soit *étendues* ou *restrictives*, en fonction de la capacité de données des types impliqués.</span><span class="sxs-lookup"><span data-stu-id="d257b-104">Conversions are either *widening* or *narrowing*, depending on the data capacities of the types involved.</span></span> <span data-ttu-id="d257b-105">Ils sont également *implicite* ou *explicite*, en fonction de la syntaxe dans le code source.</span><span class="sxs-lookup"><span data-stu-id="d257b-105">They are also *implicit* or *explicit*, depending on the syntax in the source code.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="d257b-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d257b-106">In This Section</span></span>  
 [<span data-ttu-id="d257b-107">Conversions étendues et restrictives</span><span class="sxs-lookup"><span data-stu-id="d257b-107">Widening and Narrowing Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)  
 <span data-ttu-id="d257b-108">Explique les conversions classées par indique si le type de destination peut contenir les données.</span><span class="sxs-lookup"><span data-stu-id="d257b-108">Explains conversions classified by whether the destination type can hold the data.</span></span>  
  
 [<span data-ttu-id="d257b-109">Conversions implicites et explicites</span><span class="sxs-lookup"><span data-stu-id="d257b-109">Implicit and Explicit Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)  
 <span data-ttu-id="d257b-110">Traite des conversions classifiées que Visual Basic effectue automatiquement.</span><span class="sxs-lookup"><span data-stu-id="d257b-110">Discusses conversions classified by whether Visual Basic performs them automatically.</span></span>  
  
 [<span data-ttu-id="d257b-111">Conversion entre des chaînes et d’autres types</span><span class="sxs-lookup"><span data-stu-id="d257b-111">Conversions Between Strings and Other Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/conversions-between-strings-and-other-types.md)  
 <span data-ttu-id="d257b-112">Décrit la conversion entre des chaînes et numériques, `Boolean`, ou les valeurs de date/heure.</span><span class="sxs-lookup"><span data-stu-id="d257b-112">Illustrates converting between strings and numeric, `Boolean`, or date/time values.</span></span>  
  
 [<span data-ttu-id="d257b-113">Guide pratique pour Convertir un objet en un autre Type dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d257b-113">How to: Convert an Object to Another Type in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/how-to-convert-an-object-to-another-type.md)  
 <span data-ttu-id="d257b-114">Montre comment convertir une `Object` variable en un autre type de données.</span><span class="sxs-lookup"><span data-stu-id="d257b-114">Shows how to convert an `Object` variable to any other data type.</span></span>  
  
 [<span data-ttu-id="d257b-115">Conversions de tableau</span><span class="sxs-lookup"><span data-stu-id="d257b-115">Array Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/array-conversions.md)  
 <span data-ttu-id="d257b-116">Vous guide dans le processus de conversion entre les tableaux de types de données différents.</span><span class="sxs-lookup"><span data-stu-id="d257b-116">Steps you through the process of converting between arrays of different data types.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="d257b-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d257b-117">Related Sections</span></span>  
 [<span data-ttu-id="d257b-118">Types de données</span><span class="sxs-lookup"><span data-stu-id="d257b-118">Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/index.md)  
 <span data-ttu-id="d257b-119">Introduit les types de données Visual Basic et décrit comment les utiliser.</span><span class="sxs-lookup"><span data-stu-id="d257b-119">Introduces the Visual Basic data types and describes how to use them.</span></span>  
  
 [<span data-ttu-id="d257b-120">Types de données</span><span class="sxs-lookup"><span data-stu-id="d257b-120">Data Types</span></span>](../../../../visual-basic/language-reference/data-types/index.md)  
 <span data-ttu-id="d257b-121">Répertorie les types de données élémentaires fournis par Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d257b-121">Lists the elementary data types supplied by Visual Basic.</span></span>  
  
 [<span data-ttu-id="d257b-122">Dépannage des types de données</span><span class="sxs-lookup"><span data-stu-id="d257b-122">Troubleshooting Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)  
 <span data-ttu-id="d257b-123">Décrit des problèmes courants qui peuvent survenir lorsque vous travaillez avec des types de données.</span><span class="sxs-lookup"><span data-stu-id="d257b-123">Discusses some common problems that can arise when working with data types.</span></span>
