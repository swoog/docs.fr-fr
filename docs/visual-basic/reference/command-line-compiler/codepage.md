---
title: -codepage (Visual Basic)
ms.date: 03/09/2018
helpviewer_keywords:
- -codepage compiler option [Visual Basic]
- codepage compiler option [Visual Basic]
- -codepage compiler option [Visual Basic]
ms.assetid: be36ec33-6800-4505-838c-4124564f5cc9
ms.openlocfilehash: fda75383435fdff718d1d50bc8583afc9858e7e2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61944701"
---
# <a name="-codepage-visual-basic"></a><span data-ttu-id="dad26-102">-codepage (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="dad26-102">-codepage (Visual Basic)</span></span>
<span data-ttu-id="dad26-103">Spécifie la page de codes à utiliser pour tous les fichiers de code source inclus dans la compilation.</span><span class="sxs-lookup"><span data-stu-id="dad26-103">Specifies the code page to use for all source-code files in the compilation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dad26-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dad26-104">Syntax</span></span>  
  
```  
-codepage:id  
```  
  
## <a name="arguments"></a><span data-ttu-id="dad26-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="dad26-105">Arguments</span></span>  
  
|<span data-ttu-id="dad26-106">Terme</span><span class="sxs-lookup"><span data-stu-id="dad26-106">Term</span></span>|<span data-ttu-id="dad26-107">Définition</span><span class="sxs-lookup"><span data-stu-id="dad26-107">Definition</span></span>|  
|---|---|  
|`id`|<span data-ttu-id="dad26-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dad26-108">Required.</span></span> <span data-ttu-id="dad26-109">Le compilateur utilise la page de codes spécifiée par `id` pour interpréter l’encodage des fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="dad26-109">The compiler uses the code page specified by `id` to interpret the encoding of the source files.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="dad26-110">Notes</span><span class="sxs-lookup"><span data-stu-id="dad26-110">Remarks</span></span>  
 <span data-ttu-id="dad26-111">Pour compiler le code source enregistré avec un encodage spécifique, vous pouvez utiliser `-codepage` pour spécifier la page de codes doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="dad26-111">To compile source code saved with a specific encoding, you can use `-codepage` to specify which code page should be used.</span></span> <span data-ttu-id="dad26-112">Le `-codepage` option s’applique à tous les fichiers de code source dans votre compilation.</span><span class="sxs-lookup"><span data-stu-id="dad26-112">The `-codepage` option applies to all source-code files in your compilation.</span></span> <span data-ttu-id="dad26-113">Pour plus d’informations, consultez [encodage de caractères dans le .NET Framework](../../../standard/base-types/character-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="dad26-113">For more information, see [Character Encoding in the .NET Framework](../../../standard/base-types/character-encoding.md).</span></span>  
  
 <span data-ttu-id="dad26-114">Le `-codepage` option n’est pas nécessaire si les fichiers de code source ont été enregistrés à l’aide de la page de codes ANSI actuelle, Unicode ou UTF-8 avec une signature.</span><span class="sxs-lookup"><span data-stu-id="dad26-114">The `-codepage` option is not needed if the source-code files were saved using the current ANSI code page, Unicode, or UTF-8 with a signature.</span></span> <span data-ttu-id="dad26-115">Visual Studio enregistre tous les fichiers de code source avec la page de codes ANSI actuelle par défaut, à moins que l’utilisateur spécifie un autre encodage dans la **Encoding** boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="dad26-115">Visual Studio saves all source-code files with the current ANSI code page by default, unless the user specifies another encoding in the **Encoding** dialog box.</span></span> <span data-ttu-id="dad26-116">Visual Studio utilise le **Encoding** boîte de dialogue pour ouvrir des fichiers de code source enregistrés avec une page de codes différente.</span><span class="sxs-lookup"><span data-stu-id="dad26-116">Visual Studio uses the **Encoding** dialog box to open source-code files saved with a different code page.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="dad26-117">Le `-codepage` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="dad26-117">The `-codepage` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dad26-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dad26-118">See also</span></span>

- [<span data-ttu-id="dad26-119">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="dad26-119">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
