---
title: 'Procédure : Appeler une fonction Windows qui possède des Types non signés (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- Windows functions [Visual Basic], calling
- unsigned data types [Visual Basic]
- UShort data type [Visual Basic], using
- functions [Visual Basic], calling Windows functions
- ULong data type [Visual Basic], using
- UInteger data type [Visual Basic], using
- data types [Visual Basic], using
- unsigned types [Visual Basic]
- data types [Visual Basic], unsigned
- data types [Visual Basic], numeric
- unsigned types [Visual Basic], using
ms.assetid: c2c0e712-8dc2-43b9-b4c6-345fbb02e7ce
ms.openlocfilehash: e31bc2f9a0b20ce168004fa3ea2210d39a23761e
ms.sourcegitcommit: facefcacd7ae2e5645e463bc841df213c505ffd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2019
ms.locfileid: "55738615"
---
# <a name="how-to-call-a-windows-function-that-takes-unsigned-types-visual-basic"></a><span data-ttu-id="663df-102">Procédure : Appeler une fonction Windows qui possède des Types non signés (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="663df-102">How to: Call a Windows Function that Takes Unsigned Types (Visual Basic)</span></span>
<span data-ttu-id="663df-103">Si vous consommez une classe, un module ou une structure qui possède des membres de types d’entiers non signés, vous pouvez accéder à ces membres avec Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="663df-103">If you are consuming a class, module, or structure that has members of unsigned integer types, you can access these members with Visual Basic.</span></span>  
  
### <a name="to-call-a-windows-function-that-takes-an-unsigned-type"></a><span data-ttu-id="663df-104">Pour appeler une fonction Windows qui prend un type non signé</span><span class="sxs-lookup"><span data-stu-id="663df-104">To call a Windows function that takes an unsigned type</span></span>  
  
1.  <span data-ttu-id="663df-105">Utilisez un [instruction Declare](../../../visual-basic/language-reference/statements/declare-statement.md) pour indiquer à Visual Basic quelle bibliothèque contient la fonction, ce qui est son nom dans cette bibliothèque, sa séquence d’appel What ' s et comment convertir des chaînes lors de son appel.</span><span class="sxs-lookup"><span data-stu-id="663df-105">Use a [Declare Statement](../../../visual-basic/language-reference/statements/declare-statement.md) to tell Visual Basic which library holds the function, what its name is in that library, what its calling sequence is, and how to convert strings when calling it.</span></span>  
  
2.  <span data-ttu-id="663df-106">Dans le `Declare` instruction, utilisez `UInteger`, `ULong`, `UShort`, ou `Byte` selon le cas pour chaque paramètre avec un type non signé.</span><span class="sxs-lookup"><span data-stu-id="663df-106">In the `Declare` statement, use `UInteger`, `ULong`, `UShort`, or `Byte` as appropriate for each parameter with an unsigned type.</span></span>  
  
3.  <span data-ttu-id="663df-107">Consultez la documentation de la fonction Windows que vous appelez pour rechercher les noms et valeurs des constantes, qu'elle utilise.</span><span class="sxs-lookup"><span data-stu-id="663df-107">Consult the documentation for the Windows function you are calling to find the names and values of the constants it uses.</span></span> <span data-ttu-id="663df-108">Nombre d'entre elles sont définies dans le fichier WinUser.h.</span><span class="sxs-lookup"><span data-stu-id="663df-108">Many of these are defined in the WinUser.h file.</span></span>  
  
4.  <span data-ttu-id="663df-109">Déclarez les constantes nécessaires dans votre code.</span><span class="sxs-lookup"><span data-stu-id="663df-109">Declare the necessary constants in your code.</span></span> <span data-ttu-id="663df-110">Nombreuses constantes Windows sont des valeurs non signées de 32 bits, et vous devez déclarer ces `As UInteger`.</span><span class="sxs-lookup"><span data-stu-id="663df-110">Many Windows constants are 32-bit unsigned values, and you should declare these `As UInteger`.</span></span>  
  
5.  <span data-ttu-id="663df-111">Appelez la fonction de façon normale.</span><span class="sxs-lookup"><span data-stu-id="663df-111">Call the function in the normal way.</span></span> <span data-ttu-id="663df-112">L’exemple suivant appelle la fonction Windows `MessageBox`, qui prend un argument d’entier non signé.</span><span class="sxs-lookup"><span data-stu-id="663df-112">The following example calls the Windows function `MessageBox`, which takes an unsigned integer argument.</span></span>  
  
    ```  
    Public Class windowsMessage  
        Private Declare Auto Function mb Lib "user32.dll" Alias "MessageBox" (  
            ByVal hWnd As Integer,   
            ByVal lpText As String,   
            ByVal lpCaption As String,   
            ByVal uType As UInteger) As Integer  
        Private Const MB_OK As UInteger = 0  
        Private Const MB_ICONEXCLAMATION As UInteger = &H30  
        Private Const IDOK As UInteger = 1  
        Private Const IDCLOSE As UInteger = 8  
        Private Const c As UInteger = MB_OK Or MB_ICONEXCLAMATION  
        Public Function messageThroughWindows() As String  
            Dim r As Integer = mb(0, "Click OK if you see this!",   
                "Windows API call", c)  
            Dim s As String = "Windows API MessageBox returned " &  
                 CStr(r)& vbCrLf & "(IDOK = " & CStr(IDOK) &  
                 ", IDCLOSE = " & CStr(IDCLOSE) & ")"  
            Return s  
        End Function  
    End Class  
    ```  
  
     <span data-ttu-id="663df-113">Vous pouvez tester la fonction `messageThroughWindows` avec le code suivant.</span><span class="sxs-lookup"><span data-stu-id="663df-113">You can test the function `messageThroughWindows` with the following code.</span></span>  
  
    ```  
    Public Sub consumeWindowsMessage()  
        Dim w As New windowsMessage  
        w.messageThroughWindows()  
    End Sub  
    ```  
  
    > [!CAUTION]
    >  <span data-ttu-id="663df-114">Le `UInteger`, `ULong`, `UShort`, et `SByte` les types de données ne sont pas dans le cadre de la [indépendance du langage et composants indépendants du langage](../../../standard/language-independence-and-language-independent-components.md) (CLS), le code conforme CLS ne peut pas consommer un composant qui les utilise.</span><span class="sxs-lookup"><span data-stu-id="663df-114">The `UInteger`, `ULong`, `UShort`, and `SByte` data types are not part of the [Language Independence and Language-Independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS), so CLS-compliant code cannot consume a component that uses them.</span></span>  
  
    > [!IMPORTANT]
    >  <span data-ttu-id="663df-115">Effectuer un appel au code non managé, telles que l’interface de programmation d’application Windows (API), expose votre code à des risques de sécurité potentiels.</span><span class="sxs-lookup"><span data-stu-id="663df-115">Making a call to unmanaged code, such as the Windows application programming interface (API), exposes your code to potential security risks.</span></span>  
  
    > [!IMPORTANT]
    >  <span data-ttu-id="663df-116">Appeler l’API Windows nécessite une autorisation de code non managé, ce qui peut affecter son exécution dans les situations de confiance partielle.</span><span class="sxs-lookup"><span data-stu-id="663df-116">Calling the Windows API requires unmanaged code permission, which might affect its execution in partial-trust situations.</span></span> <span data-ttu-id="663df-117">Pour plus d’informations, consultez <xref:System.Security.Permissions.SecurityPermission> et [autorisations d’accès de Code](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/h846e9b3(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="663df-117">For more information, see <xref:System.Security.Permissions.SecurityPermission> and [Code Access Permissions](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/h846e9b3(v=vs.100)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="663df-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="663df-118">See also</span></span>
- [<span data-ttu-id="663df-119">Types de données</span><span class="sxs-lookup"><span data-stu-id="663df-119">Data Types</span></span>](../../../visual-basic/language-reference/data-types/index.md)
- [<span data-ttu-id="663df-120">Integer (type de données)</span><span class="sxs-lookup"><span data-stu-id="663df-120">Integer Data Type</span></span>](../../../visual-basic/language-reference/data-types/integer-data-type.md)
- [<span data-ttu-id="663df-121">UInteger (type de données)</span><span class="sxs-lookup"><span data-stu-id="663df-121">UInteger Data Type</span></span>](../../../visual-basic/language-reference/data-types/uinteger-data-type.md)
- [<span data-ttu-id="663df-122">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="663df-122">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)
- [<span data-ttu-id="663df-123">Procédure pas à pas : Appel des API Windows</span><span class="sxs-lookup"><span data-stu-id="663df-123">Walkthrough: Calling Windows APIs</span></span>](../../../visual-basic/programming-guide/com-interop/walkthrough-calling-windows-apis.md)
