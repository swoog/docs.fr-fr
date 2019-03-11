---
title: '##pragma warning - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '#pragma warning'
helpviewer_keywords:
- '#pragma warning [C#]'
ms.assetid: 723493d5-9753-4cec-babb-54e2b8eb36b6
ms.openlocfilehash: 0145df533572ff9d5004a653bb232a7ff60af5f1
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57495102"
---
# <a name="pragma-warning-c-reference"></a><span data-ttu-id="1e9ad-102">#pragma warning (référence C#)</span><span class="sxs-lookup"><span data-stu-id="1e9ad-102">#pragma warning (C# Reference)</span></span>
<span data-ttu-id="1e9ad-103">`#pragma warning` peut activer ou désactiver certains avertissements.</span><span class="sxs-lookup"><span data-stu-id="1e9ad-103">`#pragma warning` can enable or disable certain warnings.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1e9ad-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e9ad-104">Syntax</span></span>  
  
```csharp
#pragma warning disable warning-list  
#pragma warning restore warning-list  
```  
  
## <a name="parameters"></a><span data-ttu-id="1e9ad-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e9ad-105">Parameters</span></span>  
 `warning-list`  
 <span data-ttu-id="1e9ad-106">Liste de numéros d’avertissement séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="1e9ad-106">A comma-separated list of warning numbers.</span></span> <span data-ttu-id="1e9ad-107">Le préfixe « CS » est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1e9ad-107">The "CS" prefix is optional.</span></span>  
  
 <span data-ttu-id="1e9ad-108">Quand aucun numéro d’avertissement n’est spécifié, `disable` désactive tous les avertissements et `restore` active tous les avertissements.</span><span class="sxs-lookup"><span data-stu-id="1e9ad-108">When no warning numbers are specified, `disable` disables all warnings and `restore` enables all warnings.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1e9ad-109">Pour trouver les numéros d’avertissement dans Visual Studio, générez votre projet, puis recherchez les numéros d’avertissement dans la fenêtre **Sortie**.</span><span class="sxs-lookup"><span data-stu-id="1e9ad-109">To find warning numbers in Visual Studio, build your project and then look for the warning numbers in the **Output** window.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1e9ad-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="1e9ad-110">Example</span></span>  
  
```csharp
// pragma_warning.cs  
using System;  
  
#pragma warning disable 414, CS3021  
[CLSCompliant(false)]  
public class C  
{  
    int i = 1;  
    static void Main()  
    {  
    }  
}  
#pragma warning restore CS3021  
[CLSCompliant(false)]  // CS3021  
public class D  
{  
    int i = 1;  
    public static void F()  
    {  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="1e9ad-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e9ad-111">See also</span></span>

- [<span data-ttu-id="1e9ad-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="1e9ad-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="1e9ad-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="1e9ad-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="1e9ad-114">Directives de préprocesseur C#</span><span class="sxs-lookup"><span data-stu-id="1e9ad-114">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
- [<span data-ttu-id="1e9ad-115">Erreurs du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="1e9ad-115">C# Compiler Errors</span></span>](../../../csharp/language-reference/compiler-messages/index.md)
