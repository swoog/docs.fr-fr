---
title: -preferreduilang (Options du compilateur C#)
ms.date: 07/20/2015
f1_keywords:
- /preferreduilang
helpviewer_keywords:
- preferreduilang compiler option [C#]
- /preferreduilang compiler option [C#]
- -preferreduilang compiler option [C#]
ms.assetid: 68b2462f-6778-48d7-8052-62805fe8e02c
ms.openlocfilehash: a1fbbb8415e5e3405f039489aa071b0624065a9d
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43530141"
---
# <a name="-preferreduilang-c-compiler-options"></a><span data-ttu-id="56190-102">-preferreduilang (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="56190-102">-preferreduilang (C# Compiler Options)</span></span>
<span data-ttu-id="56190-103">L’option de compilateur `-preferreduilang` vous permet de spécifier la langue dans laquelle le compilateur C# affiche la sortie, comme les messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="56190-103">By using the `-preferreduilang` compiler option, you can specify the language in which the C# compiler displays output, such as error messages.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="56190-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56190-104">Syntax</span></span>  
  
```console  
-preferreduilang: language  
```  
  
## <a name="arguments"></a><span data-ttu-id="56190-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="56190-105">Arguments</span></span>  
 `language`  
 <span data-ttu-id="56190-106">Le [nom de la langue](/windows/desktop/Intl/language-names) à utiliser pour la sortie du compilateur.</span><span class="sxs-lookup"><span data-stu-id="56190-106">The [language name](/windows/desktop/Intl/language-names) of the language to use for compiler output.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="56190-107">Notes</span><span class="sxs-lookup"><span data-stu-id="56190-107">Remarks</span></span>  
 <span data-ttu-id="56190-108">Vous pouvez utiliser l’option de compilateur `-preferreduilang` pour spécifier la langue que le compilateur C# doit utiliser pour les messages d’erreur et d’autres types de sortie de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="56190-108">You can use the `-preferreduilang` compiler option to specify the language that you want the C# compiler to use for error messages and other command-line output.</span></span> <span data-ttu-id="56190-109">Si le module linguistique de la langue n’est pas installé, le paramètre de langue du système d’exploitation est utilisé et aucune erreur n’est signalée.</span><span class="sxs-lookup"><span data-stu-id="56190-109">If the language pack for the language is not installed, the language setting of the operating system is used instead, and no error is reported.</span></span>  
  
```csharp  
csc.exe -preferreduilang:ja-JP  
```  
  
## <a name="requirements"></a><span data-ttu-id="56190-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56190-110">Requirements</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="56190-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56190-111">See Also</span></span>

- [<span data-ttu-id="56190-112">Options du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="56190-112">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)
