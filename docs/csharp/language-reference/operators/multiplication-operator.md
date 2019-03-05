---
title: '* opérateur - Référence C#'
ms.custom: seodec18
ms.date: 02/26/2019
f1_keywords:
- '*_CSharpKeyword'
helpviewer_keywords:
- multiplication operator (*) [C#]
- '* operator [C#]'
ms.assetid: abd9a5f0-9b24-431e-971a-09ee1c45c50e
ms.openlocfilehash: a5e120d26614f1e38cc2f2db02949552140b594e
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56977342"
---
# <a name="-operator-c-reference"></a>*, opérateur (référence C#)

L’opérateur `*` est pris en charge sous deux formes : un opérateur d’indirection de pointeur unaire et un opérateur de multiplication binaire.

## <a name="pointer-indirection-operator"></a>Opérateur d’indirection de pointeur

Utilisez l’opérateur `*` unaire pour récupérer la variable vers laquelle pointe un opérande de type pointeur. Pour plus d’informations, voir [Guide pratique : Récupérer la valeur d’une variable de pointeur](../../programming-guide/unsafe-code-pointers/how-to-obtain-the-value-of-a-pointer-variable.md).

L’opérateur d’indirection de pointeur `*` réclame un contexte [unsafe](../keywords/unsafe.md).

## <a name="multiplication-operator"></a>Opérateur de multiplication

Pour les types numériques, l’opérateur `*` calcule le produit de ses opérandes :

[!code-csharp-interactive[multiplication](~/samples/snippets/csharp/language-reference/operators/MultiplicationExamples.cs#Multiply)]

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) un opérateur `*` binaire. En cas de surcharge d’un opérateur `*` binaire, [l’opérateur d’assignation de multiplication](multiplication-assignment-operator.md) `*=` est aussi implicitement surchargé.

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, voir les sections [Indirection de pointeur](~/_csharplang/spec/unsafe-code.md#pointer-indirection) et [Opérateur de multiplication](~/_csharplang/spec/expressions.md#multiplication-operator) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
- [Types de pointeur](../../programming-guide/unsafe-code-pointers/pointer-types.md)