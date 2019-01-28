---
title: -nostdlib (Options du compilateur C#)
ms.date: 07/20/2015
f1_keywords:
- /nostdlib
helpviewer_keywords:
- nostdlib compiler option [C#]
- -nostdlib compiler option [C#]
- /nostdlib compiler option [C#]
ms.assetid: ec197989-fa49-4725-a455-e06b551eb65f
ms.openlocfilehash: cf87d8d2ac4531142288a8637f7fbeb9139382ea
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54545827"
---
# <a name="-nostdlib-c-compiler-options"></a><span data-ttu-id="750fc-102">-nostdlib (Options du compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="750fc-102">-nostdlib (C# Compiler Options)</span></span>

<span data-ttu-id="750fc-103">**-nostdlib** empêche l’importation du fichier mscorlib.dll, qui définit l’espace de noms System tout entier.</span><span class="sxs-lookup"><span data-stu-id="750fc-103">**-nostdlib** prevents the import of mscorlib.dll, which defines the entire System namespace.</span></span>

## <a name="syntax"></a><span data-ttu-id="750fc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="750fc-104">Syntax</span></span>

```console
-nostdlib[+ | -]
```

## <a name="remarks"></a><span data-ttu-id="750fc-105">Notes</span><span class="sxs-lookup"><span data-stu-id="750fc-105">Remarks</span></span>

<span data-ttu-id="750fc-106">Utilisez cette option si vous souhaitez définir ou créer vos propres objets et espace de noms System.</span><span class="sxs-lookup"><span data-stu-id="750fc-106">Use this option if you want to define or create your own System namespace and objects.</span></span>

<span data-ttu-id="750fc-107">Si vous ne spécifiez pas **-nostdlib**, mscorlib.dll est importé dans votre programme (ce qui équivaut à spécifier **-nostdlib-**).</span><span class="sxs-lookup"><span data-stu-id="750fc-107">If you do not specify **-nostdlib**, mscorlib.dll is imported into your program (same as specifying **-nostdlib-**).</span></span> <span data-ttu-id="750fc-108">Les options **-nostdlib** et **-nostdlib+** sont équivalentes.</span><span class="sxs-lookup"><span data-stu-id="750fc-108">Specifying **-nostdlib** is the same as specifying **-nostdlib+**.</span></span>

### <a name="to-set-this-compiler-option-in-visual-studio"></a><span data-ttu-id="750fc-109">Pour définir cette option de compilateur dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="750fc-109">To set this compiler option in Visual Studio</span></span>

> [!NOTE]
> <span data-ttu-id="750fc-110">Les instructions suivantes s’appliquent uniquement à Visual Studio 2015 (et versions antérieures).</span><span class="sxs-lookup"><span data-stu-id="750fc-110">The following instructions apply to Visual Studio 2015 (and earlier versions) only.</span></span> <span data-ttu-id="750fc-111">La propriété de build **Ne pas référencer mscorlib.dll** n’existe pas dans Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="750fc-111">The **Do not reference mscorlib.dll** build property doesn't exist in Visual Studio 2017.</span></span>

1. <span data-ttu-id="750fc-112">Ouvrez la page **Propriétés** du projet.</span><span class="sxs-lookup"><span data-stu-id="750fc-112">Open the **Properties** page for the project.</span></span>

2. <span data-ttu-id="750fc-113">Cliquez sur la page de propriétés **Générer** .</span><span class="sxs-lookup"><span data-stu-id="750fc-113">Click the **Build** properties page.</span></span>

3. <span data-ttu-id="750fc-114">Cliquez sur le bouton **Avancées** .</span><span class="sxs-lookup"><span data-stu-id="750fc-114">Click the **Advanced** button.</span></span>

4. <span data-ttu-id="750fc-115">Modifiez la propriété **Ne pas référencer mscorlib.dll** .</span><span class="sxs-lookup"><span data-stu-id="750fc-115">Modify the **Do not reference mscorlib.dll** property.</span></span>

### <a name="to-set-this-compiler-option-programmatically"></a><span data-ttu-id="750fc-116">Pour définir cette option du compilateur par programmation</span><span class="sxs-lookup"><span data-stu-id="750fc-116">To set this compiler option programmatically</span></span>

<span data-ttu-id="750fc-117">Pour plus d’informations sur la définition de cette option du compilateur par programmation, consultez <xref:VSLangProj80.CSharpProjectConfigurationProperties3.NoStdLib%2A>.</span><span class="sxs-lookup"><span data-stu-id="750fc-117">For information on how to set this compiler option programmatically, see <xref:VSLangProj80.CSharpProjectConfigurationProperties3.NoStdLib%2A>.</span></span>

## <a name="see-also"></a><span data-ttu-id="750fc-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="750fc-118">See also</span></span>

- [<span data-ttu-id="750fc-119">Options du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="750fc-119">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)
