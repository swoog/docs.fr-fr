---
title: -codepage (Visual Basic)
ms.date: 03/09/2018
helpviewer_keywords:
- -codepage compiler option [Visual Basic]
- codepage compiler option [Visual Basic]
- -codepage compiler option [Visual Basic]
ms.assetid: be36ec33-6800-4505-838c-4124564f5cc9
ms.openlocfilehash: fda75383435fdff718d1d50bc8583afc9858e7e2
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2018
ms.locfileid: "46490476"
---
# <a name="-codepage-visual-basic"></a><span data-ttu-id="21601-102">-codepage (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="21601-102">-codepage (Visual Basic)</span></span>
<span data-ttu-id="21601-103">Spécifie la page de codes à utiliser pour tous les fichiers de code source inclus dans la compilation.</span><span class="sxs-lookup"><span data-stu-id="21601-103">Specifies the code page to use for all source-code files in the compilation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="21601-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21601-104">Syntax</span></span>  
  
```  
-codepage:id  
```  
  
## <a name="arguments"></a><span data-ttu-id="21601-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="21601-105">Arguments</span></span>  
  
|<span data-ttu-id="21601-106">Terme</span><span class="sxs-lookup"><span data-stu-id="21601-106">Term</span></span>|<span data-ttu-id="21601-107">Définition</span><span class="sxs-lookup"><span data-stu-id="21601-107">Definition</span></span>|  
|---|---|  
|`id`|<span data-ttu-id="21601-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="21601-108">Required.</span></span> <span data-ttu-id="21601-109">Le compilateur utilise la page de codes spécifiée par `id` pour interpréter l’encodage des fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="21601-109">The compiler uses the code page specified by `id` to interpret the encoding of the source files.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="21601-110">Notes</span><span class="sxs-lookup"><span data-stu-id="21601-110">Remarks</span></span>  
 <span data-ttu-id="21601-111">Pour compiler le code source enregistré avec un encodage spécifique, vous pouvez utiliser `-codepage` pour spécifier la page de codes doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="21601-111">To compile source code saved with a specific encoding, you can use `-codepage` to specify which code page should be used.</span></span> <span data-ttu-id="21601-112">Le `-codepage` option s’applique à tous les fichiers de code source dans votre compilation.</span><span class="sxs-lookup"><span data-stu-id="21601-112">The `-codepage` option applies to all source-code files in your compilation.</span></span> <span data-ttu-id="21601-113">Pour plus d’informations, consultez [encodage de caractères dans le .NET Framework](../../../standard/base-types/character-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="21601-113">For more information, see [Character Encoding in the .NET Framework](../../../standard/base-types/character-encoding.md).</span></span>  
  
 <span data-ttu-id="21601-114">Le `-codepage` option n’est pas nécessaire si les fichiers de code source ont été enregistrés à l’aide de la page de codes ANSI actuelle, Unicode ou UTF-8 avec une signature.</span><span class="sxs-lookup"><span data-stu-id="21601-114">The `-codepage` option is not needed if the source-code files were saved using the current ANSI code page, Unicode, or UTF-8 with a signature.</span></span> <span data-ttu-id="21601-115">Visual Studio enregistre tous les fichiers de code source avec la page de codes ANSI actuelle par défaut, à moins que l’utilisateur spécifie un autre encodage dans la **Encoding** boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="21601-115">Visual Studio saves all source-code files with the current ANSI code page by default, unless the user specifies another encoding in the **Encoding** dialog box.</span></span> <span data-ttu-id="21601-116">Visual Studio utilise le **Encoding** boîte de dialogue pour ouvrir des fichiers de code source enregistrés avec une page de codes différente.</span><span class="sxs-lookup"><span data-stu-id="21601-116">Visual Studio uses the **Encoding** dialog box to open source-code files saved with a different code page.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="21601-117">Le `-codepage` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="21601-117">The `-codepage` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="21601-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21601-118">See also</span></span>

- [<span data-ttu-id="21601-119">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="21601-119">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
