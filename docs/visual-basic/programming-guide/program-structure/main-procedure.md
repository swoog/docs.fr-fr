---
title: Procédure Main dans Visual Basic
ms.date: 07/20/2015
f1_keywords:
- vb.Main
helpviewer_keywords:
- Main procedure
- Main method [Visual Basic]
- main function
ms.assetid: f0db283e-f283-4464-b521-b90858cc1b44
ms.openlocfilehash: a1eebc3d384d2efef050672a9c589b14559977f5
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64648754"
---
# <a name="main-procedure-in-visual-basic"></a><span data-ttu-id="b02bf-102">Procédure Main dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b02bf-102">Main Procedure in Visual Basic</span></span>
<span data-ttu-id="b02bf-103">Toutes les applications Visual Basic doivent contenir une procédure appelée `Main`.</span><span class="sxs-lookup"><span data-stu-id="b02bf-103">Every Visual Basic application must contain a procedure called `Main`.</span></span> <span data-ttu-id="b02bf-104">Cette procédure sert de point de départ et contrôle général de votre application.</span><span class="sxs-lookup"><span data-stu-id="b02bf-104">This procedure serves as the starting point and overall control for your application.</span></span> <span data-ttu-id="b02bf-105">Le .NET Framework appelle votre `Main` procédure lorsqu’il a chargé votre application et est prêt à passer le contrôle.</span><span class="sxs-lookup"><span data-stu-id="b02bf-105">The .NET Framework calls your `Main` procedure when it has loaded your application and is ready to pass control to it.</span></span> <span data-ttu-id="b02bf-106">Sauf si vous créez une application Windows Forms, vous devez écrire le `Main` procédure pour les applications qui s’exécutent sur leurs propres.</span><span class="sxs-lookup"><span data-stu-id="b02bf-106">Unless you are creating a Windows Forms application, you must write the `Main` procedure for applications that run on their own.</span></span>  
  
 <span data-ttu-id="b02bf-107">`Main` contient le code qui s’exécute en premier.</span><span class="sxs-lookup"><span data-stu-id="b02bf-107">`Main` contains the code that runs first.</span></span> <span data-ttu-id="b02bf-108">Dans `Main`, vous pouvez déterminer quelle forme doit d’abord être chargé au démarrage du programme, savoir si une copie de votre application est déjà en cours d’exécution sur le système, définir un ensemble de variables pour votre application ou ouvrir une base de données requis par l’application.</span><span class="sxs-lookup"><span data-stu-id="b02bf-108">In `Main`, you can determine which form is to be loaded first when the program starts, find out if a copy of your application is already running on the system, establish a set of variables for your application, or open a database that the application requires.</span></span>  
  
## <a name="requirements-for-the-main-procedure"></a><span data-ttu-id="b02bf-109">Configuration requise pour la procédure principale</span><span class="sxs-lookup"><span data-stu-id="b02bf-109">Requirements for the Main Procedure</span></span>  
 <span data-ttu-id="b02bf-110">Un fichier qui s’exécute sur sa propre (généralement avec l’extension .exe) doit contenir un `Main` procédure.</span><span class="sxs-lookup"><span data-stu-id="b02bf-110">A file that runs on its own (usually with extension .exe) must contain a `Main` procedure.</span></span> <span data-ttu-id="b02bf-111">Une bibliothèque (par exemple avec l’extension .dll) ne s’exécute pas son propre et ne nécessite pas un `Main` procédure.</span><span class="sxs-lookup"><span data-stu-id="b02bf-111">A library (for example with extension .dll) does not run on its own and does not require a `Main` procedure.</span></span> <span data-ttu-id="b02bf-112">La configuration requise pour les différents types de projets que vous pouvez créer est les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b02bf-112">The requirements for the different types of projects you can create are as follows:</span></span>  
  
- <span data-ttu-id="b02bf-113">Applications console s’exécutent leurs propres, et vous devez fournir au moins un `Main` procédure.</span><span class="sxs-lookup"><span data-stu-id="b02bf-113">Console applications run on their own, and you must supply at least one `Main` procedure.</span></span> <span data-ttu-id="b02bf-114">.</span><span class="sxs-lookup"><span data-stu-id="b02bf-114">.</span></span>  
  
- <span data-ttu-id="b02bf-115">Applications Windows Forms s’exécutent sur leurs propres.</span><span class="sxs-lookup"><span data-stu-id="b02bf-115">Windows Forms applications run on their own.</span></span> <span data-ttu-id="b02bf-116">Toutefois, le compilateur Visual Basic génère automatiquement un `Main` procédure telle une application et vous n’avez pas besoin d’écrire un.</span><span class="sxs-lookup"><span data-stu-id="b02bf-116">However, the Visual Basic compiler automatically generates a `Main` procedure in such an application, and you do not need to write one.</span></span>  
  
- <span data-ttu-id="b02bf-117">Bibliothèques de classes ne nécessitent pas une `Main` procédure.</span><span class="sxs-lookup"><span data-stu-id="b02bf-117">Class libraries do not require a `Main` procedure.</span></span> <span data-ttu-id="b02bf-118">Ceux-ci incluent des bibliothèques de contrôles Windows et les bibliothèques de contrôles Web.</span><span class="sxs-lookup"><span data-stu-id="b02bf-118">These include Windows Control Libraries and Web Control Libraries.</span></span> <span data-ttu-id="b02bf-119">Applications Web sont déployées en tant que bibliothèques de classes.</span><span class="sxs-lookup"><span data-stu-id="b02bf-119">Web applications are deployed as class libraries.</span></span>  
  
## <a name="declaring-the-main-procedure"></a><span data-ttu-id="b02bf-120">Déclaration de la procédure principale</span><span class="sxs-lookup"><span data-stu-id="b02bf-120">Declaring the Main Procedure</span></span>  
 <span data-ttu-id="b02bf-121">Il existe quatre façons de déclarer la `Main` procédure.</span><span class="sxs-lookup"><span data-stu-id="b02bf-121">There are four ways to declare the `Main` procedure.</span></span> <span data-ttu-id="b02bf-122">Il peut accepter des arguments ou non, et elle peut retourner une valeur ou non.</span><span class="sxs-lookup"><span data-stu-id="b02bf-122">It can take arguments or not, and it can return a value or not.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b02bf-123">Si vous déclarez `Main` dans une classe, vous devez utiliser le `Shared` mot clé.</span><span class="sxs-lookup"><span data-stu-id="b02bf-123">If you declare `Main` in a class, you must use the `Shared` keyword.</span></span> <span data-ttu-id="b02bf-124">Dans un module, `Main` pas nécessairement être `Shared`.</span><span class="sxs-lookup"><span data-stu-id="b02bf-124">In a module, `Main` does not need to be `Shared`.</span></span>  
  
- <span data-ttu-id="b02bf-125">La façon la plus simple consiste à déclarer un `Sub` procédure qui ne pas accepter des arguments ou retourner une valeur.</span><span class="sxs-lookup"><span data-stu-id="b02bf-125">The simplest way is to declare a `Sub` procedure that does not take arguments or return a value.</span></span>  
  
    ```  
    Module mainModule  
        Sub Main()  
            MsgBox("The Main procedure is starting the application.")  
            ' Insert call to appropriate starting place in your code.  
            MsgBox("The application is terminating.")  
        End Sub  
    End Module  
    ```  
  
- <span data-ttu-id="b02bf-126">`Main` peut également retourner un `Integer` valeur, que le système d’exploitation utilise comme le code de sortie de votre programme.</span><span class="sxs-lookup"><span data-stu-id="b02bf-126">`Main` can also return an `Integer` value, which the operating system uses as the exit code for your program.</span></span> <span data-ttu-id="b02bf-127">Autres programmes peuvent tester ce code en examinant la valeur ERRORLEVEL de Windows.</span><span class="sxs-lookup"><span data-stu-id="b02bf-127">Other programs can test this code by examining the Windows ERRORLEVEL value.</span></span> <span data-ttu-id="b02bf-128">Pour retourner un code de sortie, vous devez déclarer `Main` comme un `Function` procédure au lieu d’un `Sub` procédure.</span><span class="sxs-lookup"><span data-stu-id="b02bf-128">To return an exit code, you must declare `Main` as a `Function` procedure instead of a `Sub` procedure.</span></span>  
  
    ```  
    Module mainModule  
        Function Main() As Integer  
            MsgBox("The Main procedure is starting the application.")  
            Dim returnValue As Integer = 0  
            ' Insert call to appropriate starting place in your code.  
            ' On return, assign appropriate value to returnValue.  
            ' 0 usually means successful completion.  
            MsgBox("The application is terminating with error level " &  
                 CStr(returnValue) & ".")  
            Return returnValue  
        End Function  
    End Module  
    ```  
  
- <span data-ttu-id="b02bf-129">`Main` peut également prendre un `String` tableau comme argument.</span><span class="sxs-lookup"><span data-stu-id="b02bf-129">`Main` can also take a `String` array as an argument.</span></span> <span data-ttu-id="b02bf-130">Chaque chaîne dans le tableau contient un des arguments de ligne de commande utilisées pour appeler votre programme.</span><span class="sxs-lookup"><span data-stu-id="b02bf-130">Each string in the array contains one of the command-line arguments used to invoke your program.</span></span> <span data-ttu-id="b02bf-131">Vous pouvez effectuer des actions différentes en fonction de leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="b02bf-131">You can take different actions depending on their values.</span></span>  
  
    ```  
    Module mainModule  
        Function Main(ByVal cmdArgs() As String) As Integer  
            MsgBox("The Main procedure is starting the application.")  
            Dim returnValue As Integer = 0  
            ' See if there are any arguments.  
            If cmdArgs.Length > 0 Then  
                For argNum As Integer = 0 To UBound(cmdArgs, 1)  
                    ' Insert code to examine cmdArgs(argNum) and take  
                    ' appropriate action based on its value.  
                Next argNum  
            End If  
            ' Insert call to appropriate starting place in your code.  
            ' On return, assign appropriate value to returnValue.  
            ' 0 usually means successful completion.  
            MsgBox("The application is terminating with error level " &  
                 CStr(returnValue) & ".")  
            Return returnValue  
        End Function  
    End Module  
    ```  
  
- <span data-ttu-id="b02bf-132">Vous pouvez déclarer `Main` à examiner les arguments de ligne de commande, mais pas retourner un code de sortie, comme suit.</span><span class="sxs-lookup"><span data-stu-id="b02bf-132">You can declare `Main` to examine the command-line arguments but not return an exit code, as follows.</span></span>  
  
    ```  
    Module mainModule  
        Sub Main(ByVal cmdArgs() As String)  
            MsgBox("The Main procedure is starting the application.")  
            Dim returnValue As Integer = 0  
            ' See if there are any arguments.  
            If cmdArgs.Length > 0 Then  
                For argNum As Integer = 0 To UBound(cmdArgs, 1)  
                    ' Insert code to examine cmdArgs(argNum) and take  
                    ' appropriate action based on its value.  
                Next argNum  
            End If  
            ' Insert call to appropriate starting place in your code.  
            MsgBox("The application is terminating.")  
        End Sub  
    End Module  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="b02bf-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b02bf-133">See also</span></span>

- <xref:Microsoft.VisualBasic.Interaction.MsgBox%2A>
- <xref:System.Array.Length%2A>
- <xref:Microsoft.VisualBasic.Information.UBound%2A>
- [<span data-ttu-id="b02bf-134">Structure d’un programme Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b02bf-134">Structure of a Visual Basic Program</span></span>](../../../visual-basic/programming-guide/program-structure/structure-of-a-visual-basic-program.md)
- [<span data-ttu-id="b02bf-135">/main</span><span class="sxs-lookup"><span data-stu-id="b02bf-135">/main</span></span>](../../../visual-basic/reference/command-line-compiler/main.md)
- [<span data-ttu-id="b02bf-136">Shared</span><span class="sxs-lookup"><span data-stu-id="b02bf-136">Shared</span></span>](../../../visual-basic/language-reference/modifiers/shared.md)
- [<span data-ttu-id="b02bf-137">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="b02bf-137">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)
- [<span data-ttu-id="b02bf-138">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="b02bf-138">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)
- [<span data-ttu-id="b02bf-139">Integer (type de données)</span><span class="sxs-lookup"><span data-stu-id="b02bf-139">Integer Data Type</span></span>](../../../visual-basic/language-reference/data-types/integer-data-type.md)
- [<span data-ttu-id="b02bf-140">String (type de données)</span><span class="sxs-lookup"><span data-stu-id="b02bf-140">String Data Type</span></span>](../../../visual-basic/language-reference/data-types/string-data-type.md)
