---
title: Complexité des mots de passe lors de la validation (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- String data type [Visual Basic], validation
ms.assetid: 5d9a918f-6c1f-41a3-a019-b5c2b8ce0381
ms.openlocfilehash: fd1cfa8c3391861b87e8aec718b63287c1225263
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54733946"
---
# <a name="walkthrough-validating-that-passwords-are-complex-visual-basic"></a><span data-ttu-id="0ea02-102">Procédure pas à pas : Validation de mots de passe complexes (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0ea02-102">Walkthrough: Validating That Passwords Are Complex (Visual Basic)</span></span>
<span data-ttu-id="0ea02-103">Cette méthode vérifie certaines caractéristiques de mot de passe fort et met à jour un paramètre de chaîne avec des informations sur les vérifications le mot de passe échoue.</span><span class="sxs-lookup"><span data-stu-id="0ea02-103">This method checks for some strong-password characteristics and updates a string parameter with information about which checks the password fails.</span></span>  
  
 <span data-ttu-id="0ea02-104">Les mots de passe peuvent être utilisés dans un système sécurisé pour autoriser un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0ea02-104">Passwords can be used in a secure system to authorize a user.</span></span> <span data-ttu-id="0ea02-105">Toutefois, les mots de passe doivent être difficiles pour les utilisateurs non autorisés de deviner.</span><span class="sxs-lookup"><span data-stu-id="0ea02-105">However, the passwords must be difficult for unauthorized users to guess.</span></span> <span data-ttu-id="0ea02-106">Des attaquants peuvent utiliser un *attaque par dictionnaire* programme qui effectue une itération dans tous les mots dans un dictionnaire (ou plusieurs dictionnaires dans différentes langues) et teste si les mots en tant que mot de passe d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0ea02-106">Attackers can use a *dictionary attack* program, which iterates through all of the words in a dictionary (or multiple dictionaries in different languages) and tests whether any of the words work as a user's password.</span></span> <span data-ttu-id="0ea02-107">Mots de passe faibles tels que « Yankees » ou « Mustang » peuvent être devinés rapidement.</span><span class="sxs-lookup"><span data-stu-id="0ea02-107">Weak passwords such as "Yankees" or "Mustang" can be guessed quickly.</span></span> <span data-ttu-id="0ea02-108">Les mots de passe plus forts, tel que « ? Vous «L1N3vaFiNdMeyeP@sSWerd! », sont beaucoup moins susceptibles d’être devinée.</span><span class="sxs-lookup"><span data-stu-id="0ea02-108">Stronger passwords, such as "?You'L1N3vaFiNdMeyeP@sSWerd!", are much less likely to be guessed.</span></span> <span data-ttu-id="0ea02-109">Un système protégé par mot de passe doit garantir que les utilisateurs choisissent des mots de passe forts.</span><span class="sxs-lookup"><span data-stu-id="0ea02-109">A password-protected system should ensure that users choose strong passwords.</span></span>  
  
 <span data-ttu-id="0ea02-110">Un mot de passe fort est complexe (contenant un mélange de caractères majuscules, minuscules, numériques et spéciaux) et n’est pas un mot.</span><span class="sxs-lookup"><span data-stu-id="0ea02-110">A strong password is complex (containing a mixture of uppercase, lowercase, numeric, and special characters) and is not a word.</span></span> <span data-ttu-id="0ea02-111">Cet exemple montre comment vérifier la complexité.</span><span class="sxs-lookup"><span data-stu-id="0ea02-111">This example demonstrates how to verify complexity.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0ea02-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="0ea02-112">Example</span></span>  
  
### <a name="code"></a><span data-ttu-id="0ea02-113">Code</span><span class="sxs-lookup"><span data-stu-id="0ea02-113">Code</span></span>  
 [!code-vb[VbVbcnRegEx#1](../../../../visual-basic/programming-guide/language-features/strings/codesnippet/VisualBasic/walkthrough-validating-that-passwords-are-complex_1.vb)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="0ea02-114">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="0ea02-114">Compiling the Code</span></span>  
 <span data-ttu-id="0ea02-115">Appelez cette méthode en passant la chaîne qui contient ce mot de passe.</span><span class="sxs-lookup"><span data-stu-id="0ea02-115">Call this method by passing the string that contains that password.</span></span>  
  
 <span data-ttu-id="0ea02-116">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="0ea02-116">This example requires:</span></span>  
  
-   <span data-ttu-id="0ea02-117">Un accès aux membres de l’espace de noms <xref:System.Text.RegularExpressions>.</span><span class="sxs-lookup"><span data-stu-id="0ea02-117">Access to the members of the <xref:System.Text.RegularExpressions> namespace.</span></span> <span data-ttu-id="0ea02-118">Ajoutez une instruction `Imports` si vous n’utilisez pas de noms de membres qualifiés complets dans votre code.</span><span class="sxs-lookup"><span data-stu-id="0ea02-118">Add an `Imports` statement if you are not fully qualifying member names in your code.</span></span> <span data-ttu-id="0ea02-119">Pour plus d’informations, consultez [Instruction Imports (espace de noms et type .NET)](../../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md).</span><span class="sxs-lookup"><span data-stu-id="0ea02-119">For more information, see [Imports Statement (.NET Namespace and Type)](../../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md).</span></span>  
  
## <a name="security"></a><span data-ttu-id="0ea02-120">Sécurité</span><span class="sxs-lookup"><span data-stu-id="0ea02-120">Security</span></span>  
 <span data-ttu-id="0ea02-121">Si vous déplacez le mot de passe sur un réseau, vous devez utiliser une méthode sécurisée pour transférer des données.</span><span class="sxs-lookup"><span data-stu-id="0ea02-121">If you are moving the password across a network, you need to use a secure method for transferring data.</span></span> <span data-ttu-id="0ea02-122">Pour plus d’informations, consultez [ASP.NET Web Application Security](https://msdn.microsoft.com/library/330a99hc).</span><span class="sxs-lookup"><span data-stu-id="0ea02-122">For more information, see [ASP.NET Web Application Security](https://msdn.microsoft.com/library/330a99hc).</span></span>  
  
 <span data-ttu-id="0ea02-123">Vous pouvez améliorer la précision de la `ValidatePassword` fonction en ajoutant des contrôles de complexité supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="0ea02-123">You can improve the accuracy of the `ValidatePassword` function by adding additional complexity checks:</span></span>  
  
-   <span data-ttu-id="0ea02-124">Comparez le mot de passe et ses sous-chaînes contre le nom d’utilisateur, l’identificateur d’utilisateur et un dictionnaire défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="0ea02-124">Compare the password and its substrings against the user's name, user identifier, and an application-defined dictionary.</span></span> <span data-ttu-id="0ea02-125">En outre, considérez les caractères visuellement semblables comme équivalents lorsque vous effectuez des comparaisons.</span><span class="sxs-lookup"><span data-stu-id="0ea02-125">In addition, treat visually similar characters as equivalent when performing the comparisons.</span></span> <span data-ttu-id="0ea02-126">Par exemple, traiter les lettres « l » et « e » comme équivalentes aux chiffres « 1 » et « 3 ».</span><span class="sxs-lookup"><span data-stu-id="0ea02-126">For example, treat the letters "l" and "e" as equivalent to the numerals "1" and "3".</span></span>  
  
-   <span data-ttu-id="0ea02-127">S’il n'existe qu’un seul caractère en majuscule, assurez-vous qu’il n’est pas premier caractère du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="0ea02-127">If there is only one uppercase character, make sure it is not the password's first character.</span></span>  
  
-   <span data-ttu-id="0ea02-128">Assurez-vous que les deux derniers caractères du mot de passe sont des lettres.</span><span class="sxs-lookup"><span data-stu-id="0ea02-128">Make sure that the last two characters of the password are letter characters.</span></span>  
  
-   <span data-ttu-id="0ea02-129">N’autorisez pas les mots de passe dans lequel tous les symboles sont entrés à partir de la ligne du haut du clavier.</span><span class="sxs-lookup"><span data-stu-id="0ea02-129">Do not allow passwords in which all the symbols are entered from the keyboard's top row.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ea02-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ea02-130">See also</span></span>
- <xref:System.Text.RegularExpressions.Regex>
- [<span data-ttu-id="0ea02-131">Sécurité des applications web ASP.NET</span><span class="sxs-lookup"><span data-stu-id="0ea02-131">ASP.NET Web Application Security</span></span>](https://msdn.microsoft.com/library/330a99hc)
