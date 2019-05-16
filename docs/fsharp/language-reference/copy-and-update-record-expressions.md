---
title: Copie et mise à jour des expressions d’enregistrement
description: Découvrez comment écrire une « copie et mise à jour enregistrement expression » qui copie un existant, ces mises à jour spécifié de champs et retourne l’enregistrement mis à jour.
author: ChrSteinert
ms.date: 06/04/2016
ms.openlocfilehash: 7657b0295c9437890baea258295f9e9ab10073dd
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65645580"
---
# <a name="copy-and-update-record-expressions"></a><span data-ttu-id="dd1cc-103">Copie et mise à jour des expressions d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="dd1cc-103">Copy and Update Record Expressions</span></span>

<span data-ttu-id="dd1cc-104">Un *copier et mettre à jour d’expression d’enregistrement* est une expression qui copie un enregistrement existant, met à jour les champs spécifiés et retourne l’enregistrement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="dd1cc-104">A *copy and update record expression* is an expression that copies an existing record, updates specified fields, and returns the updated record.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd1cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd1cc-105">Syntax</span></span>

```fsharp
{ record-name with
    updated-member-definitions }
```

## <a name="remarks"></a><span data-ttu-id="dd1cc-106">Notes</span><span class="sxs-lookup"><span data-stu-id="dd1cc-106">Remarks</span></span>

<span data-ttu-id="dd1cc-107">Les enregistrements sont immuables par défaut, pour qu’il n’y a aucune mise à jour un enregistrement existant possible.</span><span class="sxs-lookup"><span data-stu-id="dd1cc-107">Records are immutable by default, so that there is no update to an existing record possible.</span></span> <span data-ttu-id="dd1cc-108">Pour créer un enregistrement mis à jour tous les champs d’un enregistrement devrait être spécifiés à nouveau.</span><span class="sxs-lookup"><span data-stu-id="dd1cc-108">To create an updated record all the fields of a record would have to be specified again.</span></span> <span data-ttu-id="dd1cc-109">Pour simplifier cette tâche un *copier et mettre à jour d’expression d’enregistrement* peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="dd1cc-109">To simplify this task a *copy and update record expression* can be used.</span></span> <span data-ttu-id="dd1cc-110">Cette expression prend un enregistrement existant, crée un nouveau du même type à l’aide des champs spécifiés à partir de l’expression et le champ manquant spécifié par l’expression.</span><span class="sxs-lookup"><span data-stu-id="dd1cc-110">This expression takes an existing record, creates a new one of the same type by using specified fields from the expression and the missing field specified by the expression.</span></span>
<span data-ttu-id="dd1cc-111">Cela peut être utile lorsque vous devez copier un enregistrement existant et éventuellement modifier certaines valeurs de champ.</span><span class="sxs-lookup"><span data-stu-id="dd1cc-111">This can be useful when you have to copy an existing record, and possibly change some of the field values.</span></span>

<span data-ttu-id="dd1cc-112">Prenez par exemple un enregistrement qui vient d’être créé.</span><span class="sxs-lookup"><span data-stu-id="dd1cc-112">Take for instance a newly created record.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1905.fs)]

<span data-ttu-id="dd1cc-113">Si vous deviez mettre à jour uniquement sur le champ de cet enregistrement, vous pouvez utiliser la *copier et mettre à jour d’expression d’enregistrement* comme suit :</span><span class="sxs-lookup"><span data-stu-id="dd1cc-113">If you were to update only on field of that record you could use the *copy and update record expression* like the following:</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1906.fs)]

## <a name="see-also"></a><span data-ttu-id="dd1cc-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd1cc-114">See also</span></span>

- [<span data-ttu-id="dd1cc-115">Enregistrements</span><span class="sxs-lookup"><span data-stu-id="dd1cc-115">Records</span></span>](records.md)
- [<span data-ttu-id="dd1cc-116">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="dd1cc-116">F# Language Reference</span></span>](index.md)
