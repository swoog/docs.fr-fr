---
title: volatile (référence C#)
ms.date: 07/20/2015
f1_keywords:
- volatile_CSharpKeyword
- volatile
helpviewer_keywords:
- volatile keyword [C#]
ms.assetid: 78089bc7-7b38-4cfd-9e49-87ac036af009
ms.openlocfilehash: be7e081b18702710c00b5b86a9bc152800f0cf3d
ms.sourcegitcommit: fe02afbc39e78afd78cc6050e4a9c12a75f579f8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43253165"
---
# <a name="volatile-c-reference"></a>volatile (référence C#)
Le mot clé `volatile` indique qu’un champ peut être modifié par plusieurs threads qui s’exécutent simultanément. Les champs qui sont déclarés `volatile` ne sont pas soumis aux optimisations du compilateur qui supposent l’accès par un seul thread. Ces restrictions garantissent que tous les threads observent les écritures volatiles effectuées par un autre thread dans l’ordre dans lequel elles ont été effectuées. Rien ne garantit que les écritures volatiles présentent un ordre total unique, tel que le voient tous les threads d’exécution.  
  
 Le modificateur `volatile` est généralement utilisé pour un champ auquel accèdent plusieurs threads sans utiliser l’instruction [lock](../../../csharp/language-reference/keywords/lock-statement.md) pour sérialiser l’accès.  
  
 Le mot clé `volatile` peut être appliqué aux champs des types suivants :  
  
-   Types référence.  
  
-   Types pointeur (dans un contexte unsafe). Notez que, même si le pointeur lui-même peut être volatile, l’objet sur lequel il pointe ne le peut pas. En d’autres termes, vous ne pouvez pas déclarer un pointeur vers un objet volatile.  
  
-   Types tels que sbyte, byte, short, ushort, int, uint, char, float et bool.  
  
-   Type enum avec l’un des types de base suivants : byte, sbyte, short, ushort, int ou uint.  
  
-   Paramètres de type générique connus comme des types référence.  
  
-   Voir <xref:System.IntPtr> et <xref:System.UIntPtr>.  
  
 Le mot clé volatile ne peut s’appliquer qu’aux champs d’une classe ou d’une structure. Les variables locales ne peuvent pas être déclarées `volatile`.  
  
## <a name="example"></a>Exemple  
 L’exemple ci-dessous montre comment déclarer une variable de champ public comme `volatile`.  
  
 [!code-csharp[csrefKeywordsModifiers#24](../../../csharp/language-reference/keywords/codesnippet/CSharp/volatile_1.cs)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment il est possible de créer un thread auxiliaire ou de travail et de l’utiliser pour effectuer le traitement en parallèle avec le thread principal. Pour obtenir des informations générales sur le multithreading, consultez [Threading managé](../../../standard/threading/index.md) et [Threading (C#)](../../programming-guide/concepts/threading/index.md).  
  
 [!code-csharp[csProgGuideThreading#1](../../../csharp/language-reference/keywords/codesnippet/CSharp/volatile_2.cs)]  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Mots clés C#](../../../csharp/language-reference/keywords/index.md)  
- [Modificateurs](../../../csharp/language-reference/keywords/modifiers.md)
