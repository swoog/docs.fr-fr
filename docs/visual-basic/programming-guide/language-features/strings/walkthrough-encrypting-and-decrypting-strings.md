---
title: Chiffrement et déchiffrement de chaînes en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- encryption [Visual Basic], strings
- strings [Visual Basic], encrypting
- decryption [Visual Basic], strings
- strings [Visual Basic], decrypting
ms.assetid: 1f51e40a-2f88-43e2-a83e-28a0b5c0d6fd
ms.openlocfilehash: aaf8238a330ceb9e1cf4f9ff5892d1db1d951faa
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58826793"
---
# <a name="walkthrough-encrypting-and-decrypting-strings-in-visual-basic"></a><span data-ttu-id="9a025-102">Procédure pas à pas : Chiffrement et déchiffrement de chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9a025-102">Walkthrough: Encrypting and Decrypting Strings in Visual Basic</span></span>
<span data-ttu-id="9a025-103">Cette procédure pas à pas vous montre comment utiliser le <xref:System.Security.Cryptography.DESCryptoServiceProvider> classe pour chiffrer et déchiffrer des chaînes à l’aide de la version du fournisseur (CSP) de services de chiffrement de Triple Data Encryption Standard (<xref:System.Security.Cryptography.TripleDES>) algorithme.</span><span class="sxs-lookup"><span data-stu-id="9a025-103">This walkthrough shows you how to use the <xref:System.Security.Cryptography.DESCryptoServiceProvider> class to encrypt and decrypt strings using the cryptographic service provider (CSP) version of the Triple Data Encryption Standard (<xref:System.Security.Cryptography.TripleDES>) algorithm.</span></span> <span data-ttu-id="9a025-104">La première étape consiste à créer une classe wrapper simple qui encapsule l’algorithme 3DES et stocke les données chiffrées en tant qu’une chaîne codée en base 64.</span><span class="sxs-lookup"><span data-stu-id="9a025-104">The first step is to create a simple wrapper class that encapsulates the 3DES algorithm and stores the encrypted data as a base-64 encoded string.</span></span> <span data-ttu-id="9a025-105">Ensuite, ce wrapper est utilisé pour stocker en toute sécurité des données utilisateur privées dans un fichier texte accessible publiquement.</span><span class="sxs-lookup"><span data-stu-id="9a025-105">Then, that wrapper is used to securely store private user data in a publicly accessible text file.</span></span>  
  
 <span data-ttu-id="9a025-106">Vous pouvez utiliser le chiffrement pour protéger les secrets de l’utilisateur (par exemple, les mots de passe) et pour rendre les informations d’identification illisibles par les utilisateurs non autorisés.</span><span class="sxs-lookup"><span data-stu-id="9a025-106">You can use encryption to protect user secrets (for example, passwords) and to make credentials unreadable by unauthorized users.</span></span> <span data-ttu-id="9a025-107">Cela peut protéger l’identité d’un utilisateur autorisé son vol, qui protège les actifs de l’utilisateur et fournit la non répudiation.</span><span class="sxs-lookup"><span data-stu-id="9a025-107">This can protect an authorized user's identity from being stolen, which protects the user's assets and provides non-repudiation.</span></span> <span data-ttu-id="9a025-108">Le chiffrement peut également protéger les données d’un utilisateur d’accéder à des utilisateurs non autorisés.</span><span class="sxs-lookup"><span data-stu-id="9a025-108">Encryption can also protect a user's data from being accessed by unauthorized users.</span></span>  
  
 <span data-ttu-id="9a025-109">Pour plus d’informations, consultez [Services de cryptographie](../../../../standard/security/cryptographic-services.md).</span><span class="sxs-lookup"><span data-stu-id="9a025-109">For more information, see [Cryptographic Services](../../../../standard/security/cryptographic-services.md).</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="9a025-110">Les Rijndael (maintenant appelé Advanced Encryption Standard [AES]) et les algorithmes Triple Data Encryption Standard (3DES) fournissent une meilleure sécurité que DES car elles sont plus intensifs.</span><span class="sxs-lookup"><span data-stu-id="9a025-110">The Rijndael (now referred to as Advanced Encryption Standard [AES]) and Triple Data Encryption Standard (3DES) algorithms provide greater security than DES because they are more computationally intensive.</span></span> <span data-ttu-id="9a025-111">Pour plus d’informations, consultez <xref:System.Security.Cryptography.DES> et <xref:System.Security.Cryptography.Rijndael>.</span><span class="sxs-lookup"><span data-stu-id="9a025-111">For more information, see <xref:System.Security.Cryptography.DES> and <xref:System.Security.Cryptography.Rijndael>.</span></span>  
  
### <a name="to-create-the-encryption-wrapper"></a><span data-ttu-id="9a025-112">Pour créer le wrapper de chiffrement</span><span class="sxs-lookup"><span data-stu-id="9a025-112">To create the encryption wrapper</span></span>  
  
1.  <span data-ttu-id="9a025-113">Créer la `Simple3Des` classe pour encapsuler les méthodes de chiffrement et le déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="9a025-113">Create the `Simple3Des` class to encapsulate the encryption and decryption methods.</span></span>  
  
     [!code-vb[VbVbalrStrings#38](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#38)]  
  
2.  <span data-ttu-id="9a025-114">Ajoutez une importation de l’espace de noms de chiffrement au début du fichier qui contient le `Simple3Des` classe.</span><span class="sxs-lookup"><span data-stu-id="9a025-114">Add an import of the cryptography namespace to the start of the file that contains the `Simple3Des` class.</span></span>  
  
     [!code-vb[VbVbalrStrings#77](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#77)]  
  
3.  <span data-ttu-id="9a025-115">Dans la `Simple3Des` classe, ajoutez un champ privé pour stocker le fournisseur de services de chiffrement 3DES.</span><span class="sxs-lookup"><span data-stu-id="9a025-115">In the `Simple3Des` class, add a private field to store the 3DES cryptographic service provider.</span></span>  
  
     [!code-vb[VbVbalrStrings#39](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#39)]  
  
4.  <span data-ttu-id="9a025-116">Ajoutez une méthode privée qui crée un tableau d’octets d’une longueur spécifiée à partir du hachage de la clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9a025-116">Add a private method that creates a byte array of a specified length from the hash of the specified key.</span></span>  
  
     [!code-vb[VbVbalrStrings#41](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#41)]  
  
5.  <span data-ttu-id="9a025-117">Ajoutez un constructeur pour initialiser le fournisseur de services de chiffrement 3DES.</span><span class="sxs-lookup"><span data-stu-id="9a025-117">Add a constructor to initialize the 3DES cryptographic service provider.</span></span>  
  
     <span data-ttu-id="9a025-118">Le `key` paramètre contrôle le `EncryptData` et `DecryptData` méthodes.</span><span class="sxs-lookup"><span data-stu-id="9a025-118">The `key` parameter controls the `EncryptData` and `DecryptData` methods.</span></span>  
  
     [!code-vb[VbVbalrStrings#40](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#40)]  
  
6.  <span data-ttu-id="9a025-119">Ajoutez une méthode publique qui chiffre une chaîne.</span><span class="sxs-lookup"><span data-stu-id="9a025-119">Add a public method that encrypts a string.</span></span>  
  
     [!code-vb[VbVbalrStrings#42](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#42)]  
  
7.  <span data-ttu-id="9a025-120">Ajoutez une méthode publique qui déchiffre une chaîne.</span><span class="sxs-lookup"><span data-stu-id="9a025-120">Add a public method that decrypts a string.</span></span>  
  
     [!code-vb[VbVbalrStrings#43](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#43)]  
  
     <span data-ttu-id="9a025-121">La classe wrapper peut maintenant être utilisée pour protéger les ressources de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9a025-121">The wrapper class can now be used to protect user assets.</span></span> <span data-ttu-id="9a025-122">Dans cet exemple, il est utilisé pour stocker en toute sécurité des données utilisateur privées dans un fichier texte accessible publiquement.</span><span class="sxs-lookup"><span data-stu-id="9a025-122">In this example, it is used to securely store private user data in a publicly accessible text file.</span></span>  
  
### <a name="to-test-the-encryption-wrapper"></a><span data-ttu-id="9a025-123">Pour tester le wrapper de chiffrement</span><span class="sxs-lookup"><span data-stu-id="9a025-123">To test the encryption wrapper</span></span>  
  
1.  <span data-ttu-id="9a025-124">Dans une classe distincte, ajoutez une méthode qui utilise le wrapper `EncryptData` méthode pour chiffrer une chaîne et l’écrire à l’utilisateur du dossier Mes Documents.</span><span class="sxs-lookup"><span data-stu-id="9a025-124">In a separate class, add a method that uses the wrapper's `EncryptData` method to encrypt a string and write it to the user's My Documents folder.</span></span>  
  
     [!code-vb[VbVbalrStrings#78](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#78)]  
  
2.  <span data-ttu-id="9a025-125">Ajouter une méthode qui lit la chaîne chiffrée à partir de l’utilisateur du dossier Mes Documents et déchiffre la chaîne avec le wrapper `DecryptData` (méthode).</span><span class="sxs-lookup"><span data-stu-id="9a025-125">Add a method that reads the encrypted string from the user's My Documents folder and decrypts the string with the wrapper's `DecryptData` method.</span></span>  
  
     [!code-vb[VbVbalrStrings#79](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class3.vb#79)]  
  
3.  <span data-ttu-id="9a025-126">Ajoutez le code d’interface utilisateur pour appeler le `TestEncoding` et `TestDecoding` méthodes.</span><span class="sxs-lookup"><span data-stu-id="9a025-126">Add user interface code to call the `TestEncoding` and `TestDecoding` methods.</span></span>  
  
4.  <span data-ttu-id="9a025-127">Exécutez l'application.</span><span class="sxs-lookup"><span data-stu-id="9a025-127">Run the application.</span></span>  
  
     <span data-ttu-id="9a025-128">Lorsque vous testez l’application, notez qu’il ne sera pas déchiffrer les données si vous fournissez le mot de passe incorrect.</span><span class="sxs-lookup"><span data-stu-id="9a025-128">When you test the application, notice that it will not decrypt the data if you provide the wrong password.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9a025-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a025-129">See also</span></span>

- <xref:System.Security.Cryptography>
- <xref:System.Security.Cryptography.DESCryptoServiceProvider>
- <xref:System.Security.Cryptography.DES>
- <xref:System.Security.Cryptography.TripleDES>
- <xref:System.Security.Cryptography.Rijndael>
- [<span data-ttu-id="9a025-130">Cryptographic Services</span><span class="sxs-lookup"><span data-stu-id="9a025-130">Cryptographic Services</span></span>](../../../../standard/security/cryptographic-services.md)
