---
title: Vulnérabilités de minutage avec déchiffrement symétrique en mode CBC à l’aide de la marge intérieure
description: Apprenez à détecter et atténuer les vulnérabilités de minutage avec déchiffrement symétrique sur le mode Cipher Block Chaining (CBC) à l’aide de la marge intérieure.
ms.date: 06/12/2018
author: blowdart
ms.author: mairaw
ms.openlocfilehash: 6d16b6849bfd4744f1828cda38a537f842243c1d
ms.sourcegitcommit: f513a91160b3fec289dd06646d0d6f81f8fcf910
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46288379"
---
# <a name="timing-vulnerabilities-with-cbc-mode-symmetric-decryption-using-padding"></a><span data-ttu-id="9f060-103">Vulnérabilités de minutage avec déchiffrement symétrique en mode CBC à l’aide de la marge intérieure</span><span class="sxs-lookup"><span data-stu-id="9f060-103">Timing vulnerabilities with CBC-mode symmetric decryption using padding</span></span>

<span data-ttu-id="9f060-104">Microsoft est convaincu qu’il n’est plus sûr déchiffrer les données chiffrées avec le mode Cipher Block Chaining (CBC) de chiffrement symétrique lors de la marge intérieure vérifiable a été appliqué sans d’abord vérifié que l’intégrité du texte chiffré, à l’exception de très spécifique circonstances.</span><span class="sxs-lookup"><span data-stu-id="9f060-104">Microsoft believes that it's no longer safe to decrypt data encrypted with the Cipher-Block-Chaining (CBC) mode of symmetric encryption when verifiable padding has been applied without first ensuring the integrity of the ciphertext, except for very specific circumstances.</span></span> <span data-ttu-id="9f060-105">Cette opinion est basée sur les recherches sur le chiffrement connus.</span><span class="sxs-lookup"><span data-stu-id="9f060-105">This judgement is based on currently known cryptographic research.</span></span> 

## <a name="introduction"></a><span data-ttu-id="9f060-106">Introduction</span><span class="sxs-lookup"><span data-stu-id="9f060-106">Introduction</span></span>

<span data-ttu-id="9f060-107">Une attaque d’oracle de remplissage est un type d’attaque sur les données chiffrées qui permet à un attaquant déchiffrer le contenu des données, sans connaître la clé.</span><span class="sxs-lookup"><span data-stu-id="9f060-107">A padding oracle attack is a type of attack against encrypted data that allows the attacker to decrypt the contents of the data, without knowing the key.</span></span>

<span data-ttu-id="9f060-108">Oracle fait référence à un « savoir » qui donne une personne malveillante d’informations sur si l’action qu’ils exécutent est correcte ou non.</span><span class="sxs-lookup"><span data-stu-id="9f060-108">An oracle refers to a "tell" which gives an attacker information about whether the action they're executing is correct or not.</span></span> <span data-ttu-id="9f060-109">Imaginez un plateau de jeu ou une carte de jeu avec un enfant.</span><span class="sxs-lookup"><span data-stu-id="9f060-109">Imagine playing a board or card game with a child.</span></span> <span data-ttu-id="9f060-110">Lorsque sa face s’allume avec un sourire volumineux, car elle pense qu’elle est sur le point d’effectuer un mouvement bon, ce qui est oracle.</span><span class="sxs-lookup"><span data-stu-id="9f060-110">When her face lights up with a big smile because she thinks she's about to make a good move, that's an oracle.</span></span> <span data-ttu-id="9f060-111">Vous, en tant que l’adversaire, pourrez utiliser cette oracle pour bien planifier votre prochain déplacement.</span><span class="sxs-lookup"><span data-stu-id="9f060-111">You, as the opponent, can use this oracle to plan your next move appropriately.</span></span>

<span data-ttu-id="9f060-112">Marge intérieure est un terme de chiffrement spécifique.</span><span class="sxs-lookup"><span data-stu-id="9f060-112">Padding is a specific cryptographic term.</span></span> <span data-ttu-id="9f060-113">Certains chiffrements qui sont les algorithmes utilisés pour chiffrer vos données, travailler sur des blocs de données où chaque bloc est de taille fixe.</span><span class="sxs-lookup"><span data-stu-id="9f060-113">Some ciphers, which are the algorithms used to encrypt your data, work on blocks of data where each block is a fixed size.</span></span> <span data-ttu-id="9f060-114">Si les données que vous souhaitez chiffrer n’est pas la bonne taille pour remplir les blocs, vos données sont complétées jusqu'à ce que c’est le cas.</span><span class="sxs-lookup"><span data-stu-id="9f060-114">If the data you want to encrypt isn't the right size to fill the blocks, your data is padded until it does.</span></span> <span data-ttu-id="9f060-115">Différentes formes de la marge intérieure nécessitent ce remplissage soit toujours présents, même si l’entrée d’origine était de la taille appropriée.</span><span class="sxs-lookup"><span data-stu-id="9f060-115">Many forms of padding require that padding to always be present, even if the original input was of the right size.</span></span> <span data-ttu-id="9f060-116">Ainsi, la marge intérieure à toujours être supprimés lors de déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="9f060-116">This allows the padding to always be safely removed upon decryption.</span></span>

<span data-ttu-id="9f060-117">Assembler les deux tâches, une implémentation logicielle avec une marge intérieure d’oracle révèle si les données déchiffrées ont remplissage valide.</span><span class="sxs-lookup"><span data-stu-id="9f060-117">Putting the two things together, a software implementation with a padding oracle reveals whether decrypted data has valid padding.</span></span> <span data-ttu-id="9f060-118">Oracle peut être quelque chose d’aussi simple que retournant une valeur qui indique « Remplissage non valide » ou quelque chose de plus compliqué à prendre une heure sensiblement différente pour traiter un bloc valide par opposition à un bloc non valide.</span><span class="sxs-lookup"><span data-stu-id="9f060-118">The oracle could be something as simple as returning a value that says "Invalid padding" or something more complicated like taking a measurably different time to process a valid block as opposed to an invalid block.</span></span>

<span data-ttu-id="9f060-119">Les chiffrements par bloc ont une autre propriété, appelée le mode, qui détermine la relation de données dans le premier bloc de données dans le deuxième bloc, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="9f060-119">Block-based ciphers have another property, called the mode, which determines the relationship of data in the first block to the data in the second block, and so on.</span></span> <span data-ttu-id="9f060-120">Un des modes plus couramment utilisées est CBC.</span><span class="sxs-lookup"><span data-stu-id="9f060-120">One of the most commonly used modes is CBC.</span></span> <span data-ttu-id="9f060-121">CBC introduit un bloc aléatoire initial, connu en tant que le vecteur d’initialisation (IV) et combine le bloc précédent avec le résultat du chiffrement statique pour le rendre telles que le chiffrement du message même avec la même clé ne produire toujours la même sortie chiffrée.</span><span class="sxs-lookup"><span data-stu-id="9f060-121">CBC introduces an initial random block, known as the Initialization Vector (IV), and combines the previous block with the result of static encryption to make it such that encrypting the same message with the same key doesn't always produce the same encrypted output.</span></span>

<span data-ttu-id="9f060-122">Une personne malveillante peut utiliser une oracle de remplissage, en association avec la structure des données de CBC, pour envoyer des messages légèrement modifiés pour le code qui expose l’oracle et envoyer des données jusqu'à ce que l’oracle lui indiquant les données sont correctes.</span><span class="sxs-lookup"><span data-stu-id="9f060-122">An attacker can use a padding oracle, in combination with how CBC data is structured, to send slightly changed messages to the code that exposes the oracle, and keep sending data until the oracle tells them the data is correct.</span></span> <span data-ttu-id="9f060-123">À partir de cette réponse, l’attaquant peut déchiffrer le message octet par octet.</span><span class="sxs-lookup"><span data-stu-id="9f060-123">From this response, the attacker can decrypt the message byte by byte.</span></span>

<span data-ttu-id="9f060-124">Réseaux informatiques modernes sont de ce type haute qualité qu’une personne malveillante peut détecter très petite (inférieure à 0,1 ms) les différences dans l’exécution de temps sur des systèmes distants.</span><span class="sxs-lookup"><span data-stu-id="9f060-124">Modern computer networks are of such high quality that an attacker can detect very small (less than 0.1 ms) differences in execution time on remote systems.</span></span> <span data-ttu-id="9f060-125">Les applications qui sont en supposant que le déchiffrement réussi ne peut se produire lorsque les données n’a pas été falsifiées peuvent être vulnérables aux attaques à partir d’outils sont conçus pour observer les différences de déchiffrement ayant réussi ou échoué.</span><span class="sxs-lookup"><span data-stu-id="9f060-125">Applications that are assuming that a successful decryption can only happen when the data wasn't tampered with may be vulnerable to attack from tools that are designed to observe differences in successful and unsuccessful decryption.</span></span> <span data-ttu-id="9f060-126">Cette différence de minutage peut être plus importante dans certains langages ou des bibliothèques que d’autres, il est désormais croire qu’il s’agit d’une menace pratique pour tous les langages et bibliothèques lors de la réponse de l’application aux défaillances est pris en compte.</span><span class="sxs-lookup"><span data-stu-id="9f060-126">While this timing difference may be more significant in some languages or libraries than others, it's now believed that this is a practical threat for all languages and libraries when the application's response to failure is taken into account.</span></span>

<span data-ttu-id="9f060-127">Cette attaque s’appuie sur la possibilité de modifier les données chiffrées et testez le résultat avec oracle.</span><span class="sxs-lookup"><span data-stu-id="9f060-127">This attack relies on the ability to change the encrypted data and test the result with the oracle.</span></span> <span data-ttu-id="9f060-128">La seule façon d’atténuer entièrement l’attaque consiste à détecter les modifications apportées aux données chiffrées et refuse d’effectuer des actions sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="9f060-128">The only way to fully mitigate the attack is to detect changes to the encrypted data and refuse to perform any actions on it.</span></span> <span data-ttu-id="9f060-129">Pour ce faire, le standard consiste à créer une signature pour les données et valider la signature avant que toutes les opérations sont effectuées.</span><span class="sxs-lookup"><span data-stu-id="9f060-129">The standard way to do this is to create a signature for the data and validate that signature before any operations are performed.</span></span> <span data-ttu-id="9f060-130">La signature doit être vérifiable, il ne peut pas être créé par l’attaquant, sinon ils seraient modifier les données chiffrées, puis calculer une nouvelle signature basée sur les données modifiées.</span><span class="sxs-lookup"><span data-stu-id="9f060-130">The signature must be verifiable, it cannot be created by the attacker, otherwise they'd change the encrypted data, then compute a new signature based on the changed data.</span></span> <span data-ttu-id="9f060-131">Un type courant de la signature appropriée est appelé un code d’authentification de message de hachage à clé (HMAC).</span><span class="sxs-lookup"><span data-stu-id="9f060-131">One common type of appropriate signature is known as a keyed-hash message authentication code (HMAC).</span></span> <span data-ttu-id="9f060-132">Un HMAC diffère d’une somme de contrôle dans la mesure où il prend une clé secrète, connu uniquement à la personne produisant le code HMAC et à la personne validant.</span><span class="sxs-lookup"><span data-stu-id="9f060-132">An HMAC differs from a checksum in that it takes a secret key, known only to the person producing the HMAC and to the person validating it.</span></span> <span data-ttu-id="9f060-133">Sans la possession de la clé, vous ne peuvent pas produire un code HMAC correct.</span><span class="sxs-lookup"><span data-stu-id="9f060-133">Without possession of the key, you can't produce a correct HMAC.</span></span> <span data-ttu-id="9f060-134">Lorsque vous recevez vos données, vous prendre les données chiffrées, calculer indépendamment le HMAC à l’aide de la clé secrète vous et le partage de l’expéditeur, puis compare le HMAC ils vous avons envoyé par rapport à celle calculé.</span><span class="sxs-lookup"><span data-stu-id="9f060-134">When you receive your data, you'd take the encrypted data, independently compute the HMAC using the secret key you and the sender share, then compare the HMAC they sent against the one you computed.</span></span> <span data-ttu-id="9f060-135">Cette comparaison doit être temps constant, sinon vous avez ajouté un autre oracle détectable, ce qui permet un autre type d’attaque.</span><span class="sxs-lookup"><span data-stu-id="9f060-135">This comparison must be constant time, otherwise you've added another detectable oracle, allowing a different type of attack.</span></span>

<span data-ttu-id="9f060-136">En résumé, pour utiliser complété les chiffrements par bloc CBC en toute sécurité, vous devez les combiner avec un code HMAC (ou une autre vérification de l’intégrité des données) que vous validez à l’aide d’une comparaison de temps constant avant d’essayer de déchiffrer les données.</span><span class="sxs-lookup"><span data-stu-id="9f060-136">In summary, to use padded CBC block ciphers safely, you must combine them with an HMAC (or another data integrity check) that you validate using a constant time comparison before trying to decrypt the data.</span></span> <span data-ttu-id="9f060-137">Étant donné que tous les messages modifiés prennent le même volume de temps pour produire une réponse, l’attaque est empêchée.</span><span class="sxs-lookup"><span data-stu-id="9f060-137">Since all altered messages take the same amount time to produce a response, the attack is prevented.</span></span>

## <a name="who-is-vulnerable"></a><span data-ttu-id="9f060-138">Qui est vulnérable</span><span class="sxs-lookup"><span data-stu-id="9f060-138">Who is vulnerable</span></span>

<span data-ttu-id="9f060-139">Cette vulnérabilité s’applique aux applications gérées et natives qui effectuent leur propre chiffrement et le déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="9f060-139">This vulnerability applies to both managed and native applications that are performing their own encryption and decryption.</span></span> <span data-ttu-id="9f060-140">Cela inclut, par exemple :</span><span class="sxs-lookup"><span data-stu-id="9f060-140">This includes, for example:</span></span>

- <span data-ttu-id="9f060-141">Une application qui chiffre un cookie pour le déchiffrement ultérieure sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="9f060-141">An application that encrypts a cookie for later decryption on the server.</span></span>
- <span data-ttu-id="9f060-142">Une application de base de données qui offre la possibilité aux utilisateurs d’insérer des données dans une table dont les colonnes sont déchiffrées.</span><span class="sxs-lookup"><span data-stu-id="9f060-142">A database application that provides the ability for users to insert data into a table whose columns are later decrypted.</span></span>
- <span data-ttu-id="9f060-143">Une application de transfert de données qui s’appuie sur le chiffrement à l’aide d’une clé partagée pour protéger les données en transit.</span><span class="sxs-lookup"><span data-stu-id="9f060-143">A data transfer application that relies on encryption using a shared key to protect the data in transit.</span></span>
- <span data-ttu-id="9f060-144">Une application qui chiffre et déchiffre les messages « interne » le tunnel TLS.</span><span class="sxs-lookup"><span data-stu-id="9f060-144">An application that encrypts and decrypts messages "inside" the TLS tunnel.</span></span>

<span data-ttu-id="9f060-145">Notez qu’à l’aide de TLS seul ne peut pas protéger dans ces scénarios.</span><span class="sxs-lookup"><span data-stu-id="9f060-145">Note that using TLS alone may not protect you in these scenarios.</span></span>

<span data-ttu-id="9f060-146">Une application vulnérable :</span><span class="sxs-lookup"><span data-stu-id="9f060-146">A vulnerable application:</span></span>

- <span data-ttu-id="9f060-147">Déchiffre les données à l’aide du mode de chiffrement CBC avec un mode de remplissage vérifiable, tels que PKCS #7 ou ANSI X.923.</span><span class="sxs-lookup"><span data-stu-id="9f060-147">Decrypts data using the CBC cipher mode with a verifiable padding mode, such as PKCS#7 or ANSI X.923.</span></span>
- <span data-ttu-id="9f060-148">Exécute le déchiffrement sans avoir effectué une vérification de l’intégrité des données (via un MAC ou une signature numérique asymétrique).</span><span class="sxs-lookup"><span data-stu-id="9f060-148">Performs the decryption without having performed a data integrity check (via a MAC or an asymmetric digital signature).</span></span>

<span data-ttu-id="9f060-149">Cela s’applique également aux applications reposant sur les abstractions par-dessus ces primitives, telles que la structure de EnvelopedData Cryptographic Message Syntax (PKCS #7/CMS).</span><span class="sxs-lookup"><span data-stu-id="9f060-149">This also applies to applications built on top of abstractions over top of these primitives, such as the Cryptographic Message Syntax (PKCS#7/CMS) EnvelopedData structure.</span></span>

## <a name="related-areas-of-concern"></a><span data-ttu-id="9f060-150">Domaines de préoccupation connexes</span><span class="sxs-lookup"><span data-stu-id="9f060-150">Related areas of concern</span></span>

<span data-ttu-id="9f060-151">Research a conduit Microsoft à se préoccuper davantage de messages de CBC sont complétées par ISO 10126-équivalent de remplissage lorsque le message a une structure de pied de page connu ou prévisibles.</span><span class="sxs-lookup"><span data-stu-id="9f060-151">Research has led Microsoft to be further concerned about CBC messages that are padded with ISO 10126-equivalent padding when the message has a well-known or predictable footer structure.</span></span> <span data-ttu-id="9f060-152">Par exemple, le contenu préparé conformément aux règles de W3C XML Encryption Syntax et de la recommandation de traitement (xmlenc, EncryptedXml).</span><span class="sxs-lookup"><span data-stu-id="9f060-152">For example, content prepared under the rules of the W3C XML Encryption Syntax and Processing Recommendation (xmlenc, EncryptedXml).</span></span> <span data-ttu-id="9f060-153">Tandis que les recommandations du W3C pour signer le message, puis chiffrer a été considérée comme appropriée en temps, Microsoft recommande toujours fait encrypt-then-sign.</span><span class="sxs-lookup"><span data-stu-id="9f060-153">While the W3C guidance to sign the message then encrypt was considered appropriate at the time, Microsoft now recommends always doing encrypt-then-sign.</span></span>

<span data-ttu-id="9f060-154">Les développeurs d’applications doivent toujours être conscients de la vérification de la mise en application d’une clé de signature asymétrique, car il n’existe aucune relation d’approbation inhérente entre une clé asymétrique et un message arbitraire.</span><span class="sxs-lookup"><span data-stu-id="9f060-154">Application developers should always be mindful of verifying the applicability of an asymmetric signature key, as there's no inherent trust relationship between an asymmetric key and an arbitrary message.</span></span>

## <a name="details"></a><span data-ttu-id="9f060-155">Détails</span><span class="sxs-lookup"><span data-stu-id="9f060-155">Details</span></span>

<span data-ttu-id="9f060-156">Historiquement, il a été consensus qu’il est important de chiffrer et authentifier des données importantes, à l’aide de moyens par exemple, les signatures HMAC ou RSA.</span><span class="sxs-lookup"><span data-stu-id="9f060-156">Historically, there has been consensus that it's important to both encrypt and authenticate important data, using means such as HMAC or RSA signatures.</span></span> <span data-ttu-id="9f060-157">Toutefois, il a été moins des conseils éclairés concernant la procédure pour séquencer les opérations de chiffrement et d’authentification.</span><span class="sxs-lookup"><span data-stu-id="9f060-157">However, there has been less clear guidance as to how to sequence the encryption and authentication operations.</span></span> <span data-ttu-id="9f060-158">En raison de la vulnérabilité décrites dans cet article, les conseils de Microsoft est désormais à toujours utiliser le paradigme « encrypt-then-sign ».</span><span class="sxs-lookup"><span data-stu-id="9f060-158">Due to the vulnerability detailed in this article, Microsoft's guidance is now to always use the "encrypt-then-sign" paradigm.</span></span> <span data-ttu-id="9f060-159">Autrement dit, tout d’abord chiffrer des données à l’aide d’une clé symétrique, puis un MAC ou signature asymétrique de calcul sur le texte chiffré (données chiffrées).</span><span class="sxs-lookup"><span data-stu-id="9f060-159">That is, first encrypt data using a symmetric key, then compute a MAC or asymmetric signature over the ciphertext (encrypted data).</span></span> <span data-ttu-id="9f060-160">Lors du déchiffrage des données, effectuer l’inverse.</span><span class="sxs-lookup"><span data-stu-id="9f060-160">When decrypting data, perform the reverse.</span></span> <span data-ttu-id="9f060-161">Tout d’abord, vérifiez le MAC ou la signature du texte chiffré, puis le déchiffrer.</span><span class="sxs-lookup"><span data-stu-id="9f060-161">First, confirm the MAC or signature of the ciphertext, then decrypt it.</span></span>

<span data-ttu-id="9f060-162">Une classe de vulnérabilités appelé « remplissage oracle attaques » ont été identifiés existe depuis plus de 10 ans.</span><span class="sxs-lookup"><span data-stu-id="9f060-162">A class of vulnerabilities known as "padding oracle attacks" have been known to exist for over 10 years.</span></span> <span data-ttu-id="9f060-163">Ces vulnérabilités permettent à une personne malveillante de déchiffrer les données chiffrées par bloc symétriques algorithmes, tels que AES et 3DES, à l’aide de tentatives de ne plus de 4 096 par bloc de données.</span><span class="sxs-lookup"><span data-stu-id="9f060-163">These vulnerabilities allow an attacker to decrypt data encrypted by symmetric block algorithms, such as AES and 3DES, using no more than 4096 attempts per block of data.</span></span> <span data-ttu-id="9f060-164">Assurez-vous de supprimer ces vulnérabilités utilisation du fait que les chiffrements par bloc les plus fréquemment utilisés avec des données de remplissage vérifiable à la fin.</span><span class="sxs-lookup"><span data-stu-id="9f060-164">These vulnerabilities make use of the fact that block ciphers are most frequently used with verifiable padding data at the end.</span></span> <span data-ttu-id="9f060-165">Il a été trouvé si une personne malveillante peut falsifier le texte chiffré et déterminer si les risques de falsification a entraîné une erreur dans le format de la marge intérieure à la fin, l’attaquant peut déchiffrer les données.</span><span class="sxs-lookup"><span data-stu-id="9f060-165">It was found that if an attacker can tamper with ciphertext and find out whether the tampering caused an error in the format of the padding at the end, the attacker can decrypt the data.</span></span>

<span data-ttu-id="9f060-166">Initialement, les attaques pratiques étaient basés sur les services qui retournent les codes d’erreur différents en fonction de remplissage intervenue valide, telle que la vulnérabilité ASP.NET [MS10-070](https://technet.microsoft.com/library/security/ms10-070.aspx).</span><span class="sxs-lookup"><span data-stu-id="9f060-166">Initially, practical attacks were based on services that would return different error codes based on whether padding was valid, such as the ASP.NET vulnerability [MS10-070](https://technet.microsoft.com/library/security/ms10-070.aspx).</span></span> <span data-ttu-id="9f060-167">Toutefois, Microsoft estime maintenant qu’il est pratique de mener des attaques similaires à l’aide uniquement les différences de minutage entre le traitement de remplissage valide et non valide.</span><span class="sxs-lookup"><span data-stu-id="9f060-167">However, Microsoft now believes that it's practical to conduct similar attacks using only the differences in timing between processing valid and invalid padding.</span></span>

<span data-ttu-id="9f060-168">Condition que le schéma de chiffrement utilise une signature et que la vérification de signature est effectuée avec un runtime fixe pour une longueur donnée de données (quel que soit le contenu), l’intégrité des données peut être vérifiée sans émettre de toutes les informations à un attaquant via un [canal latéral](https://en.wikipedia.org/wiki/Side-channel_attack).</span><span class="sxs-lookup"><span data-stu-id="9f060-168">Provided that the encryption scheme employs a signature and that the signature verification is performed with a fixed runtime for a given length of data (irrespective of the contents), the data integrity can be verified without emitting any information to an attacker via a [side channel](https://en.wikipedia.org/wiki/Side-channel_attack).</span></span> <span data-ttu-id="9f060-169">Étant donné que la vérification d’intégrité rejette les messages falsifiés, la menace d’oracle de remplissage est atténuée.</span><span class="sxs-lookup"><span data-stu-id="9f060-169">Since the integrity check rejects any tampered messages, the padding oracle threat is mitigated.</span></span>

## <a name="guidance"></a><span data-ttu-id="9f060-170">Conseils</span><span class="sxs-lookup"><span data-stu-id="9f060-170">Guidance</span></span>

<span data-ttu-id="9f060-171">Tout d’abord, Microsoft recommande que les données ayant la confidentialité doivent être transmises sur sécurité TLS (Transport Layer), le successeur de couche SSL (Secure Sockets).</span><span class="sxs-lookup"><span data-stu-id="9f060-171">First and foremost, Microsoft recommends that any data that has confidentiality needs be transmitted over Transport Layer Security (TLS), the successor to Secure Sockets Layer (SSL).</span></span>

<span data-ttu-id="9f060-172">Ensuite, analysez votre application :</span><span class="sxs-lookup"><span data-stu-id="9f060-172">Next, analyze your application to:</span></span>

- <span data-ttu-id="9f060-173">Comprendre et avec précision quelles chiffrement que vous effectuez le chiffrement est fourni par les plateformes et les API que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="9f060-173">Understand precisely what encryption you're performing and what encryption is being provided by the platforms and APIs you're using.</span></span>
- <span data-ttu-id="9f060-174">Être certain que chaque utilisation au niveau de chaque couche de symétrique [algorithme de chiffrement par bloc](https://en.wikipedia.org/wiki/Block_cipher#Notable_block_ciphers), tel que AES et 3DES, en mode CBC incorporer l’utilisation d’une vérification de l’intégrité des données à la clé de secret (une signature asymétrique, un code HMAC, ou pour modifier le mode de chiffrement à un [authentifié chiffrement](https://en.wikipedia.org/wiki/Authenticated_encryption) mode (AE) telles que GCM ou CCM).</span><span class="sxs-lookup"><span data-stu-id="9f060-174">Be certain that each usage at each layer of a symmetric [block cipher algorithm](https://en.wikipedia.org/wiki/Block_cipher#Notable_block_ciphers), such as AES and 3DES, in CBC mode incorporate the use of a secret-keyed data integrity check (an asymmetric signature, an HMAC, or to change the cipher mode to an [authenticated encryption](https://en.wikipedia.org/wiki/Authenticated_encryption) (AE) mode such as GCM or CCM).</span></span>

<span data-ttu-id="9f060-175">En fonction de la recherche en cours, il est de croire que lorsque les étapes de l’authentification et le chiffrement sont effectuées indépendamment pour les modes non AE de chiffrement, l’authentification le texte chiffré (encrypt-then-sign) est la meilleure option générale.</span><span class="sxs-lookup"><span data-stu-id="9f060-175">Based on the current research, it's generally believed that when the authentication and encryption steps are performed independently for non-AE modes of encryption, authenticating the ciphertext (encrypt-then-sign) is the best general option.</span></span> <span data-ttu-id="9f060-176">Toutefois, il n’existe aucune réponse correcte uniformisée au chiffrement et cette généralisation n’est pas aussi bonne qualité qu’orienté conseils à partir d’un cryptographe Professionnel.</span><span class="sxs-lookup"><span data-stu-id="9f060-176">However, there's no one-size-fits-all correct answer to cryptography and this generalization isn't as good as directed advice from a professional cryptographer.</span></span>

<span data-ttu-id="9f060-177">Les applications qui ne peuvent pas modifier leur format de messagerie mais effectuer un déchiffrement CBC non authentifié sont invitées à tentez d’incorporer des solutions d’atténuation telles que :</span><span class="sxs-lookup"><span data-stu-id="9f060-177">Applications that are unable to change their messaging format but perform unauthenticated CBC decryption are encouraged to try to incorporate mitigations such as:</span></span>

- <span data-ttu-id="9f060-178">Déchiffrer sans autoriser le déchiffreur vérifier ou supprimer le remplissage :</span><span class="sxs-lookup"><span data-stu-id="9f060-178">Decrypt without allowing the decryptor to verify or remove padding:</span></span>
  - <span data-ttu-id="9f060-179">Tout remplissage a été appliqué doit toujours être supprimés ou ignorés, que vous déplacez le fardeau dans votre application.</span><span class="sxs-lookup"><span data-stu-id="9f060-179">Any padding that was applied still needs to be removed or ignored, you're moving the burden into your application.</span></span>
  - <span data-ttu-id="9f060-180">L’avantage est que la vérification de la marge intérieure et la suppression peuvent être incorporés dans une autre logique de vérification de données application.</span><span class="sxs-lookup"><span data-stu-id="9f060-180">The benefit is that the padding verification and removal can be incorporated into other application data verification logic.</span></span> <span data-ttu-id="9f060-181">Si la vérification de la marge intérieure et la vérification des données peuvent être effectuées en temps constant, la menace est réduite.</span><span class="sxs-lookup"><span data-stu-id="9f060-181">If the padding verification and data verification can be done in constant time, the threat is reduced.</span></span>
  - <span data-ttu-id="9f060-182">Étant donné que l’interprétation de la marge intérieure change la longueur du message perçue, il peut toujours être émises à partir de cette approche des informations de minutage.</span><span class="sxs-lookup"><span data-stu-id="9f060-182">Since the interpretation of the padding changes the perceived message length, there may still be timing information emitted from this approach.</span></span>
- <span data-ttu-id="9f060-183">Modifiez le mode de remplissage de déchiffrement ISO10126 :</span><span class="sxs-lookup"><span data-stu-id="9f060-183">Change the decryption padding mode to ISO10126:</span></span>
  - <span data-ttu-id="9f060-184">Remplissage de déchiffrement ISO10126 est compatible avec remplissage de chiffrement PKCS7 et remplissage ANSIX923.</span><span class="sxs-lookup"><span data-stu-id="9f060-184">ISO10126 decryption padding is compatible with both PKCS7 encryption padding and ANSIX923 encryption padding.</span></span>
  - <span data-ttu-id="9f060-185">Modification du mode réduit les connaissances d’oracle de remplissage à 1 octet au lieu de l’intégralité du bloc.</span><span class="sxs-lookup"><span data-stu-id="9f060-185">Changing the mode reduces the padding oracle knowledge to 1 byte instead of the entire block.</span></span> <span data-ttu-id="9f060-186">Toutefois, si le contenu a un pied de page bien connu, tels que d’un élément XML, de fermeture attaques connexes peuvent continuer attaquer le reste du message.</span><span class="sxs-lookup"><span data-stu-id="9f060-186">However, if the content has a well-known footer, such as a closing XML element, related attacks can continue to attack the rest of the message.</span></span>
  - <span data-ttu-id="9f060-187">Cela n’empêche également pas récupération en texte clair dans les situations où l’attaquant peut forcer le même texte en clair à chiffrer plusieurs fois avec un décalage de message différent.</span><span class="sxs-lookup"><span data-stu-id="9f060-187">This also doesn't prevent plaintext recovery in situations where the attacker can coerce the same plaintext to be encrypted multiple times with a different message offset.</span></span>
- <span data-ttu-id="9f060-188">L’évaluation d’un appel de déchiffrement à mouiller le signal de minutage de la grille :</span><span class="sxs-lookup"><span data-stu-id="9f060-188">Gate the evaluation of a decryption call to dampen the timing signal:</span></span>
  - <span data-ttu-id="9f060-189">Le calcul de la durée de conservation doit avoir un minimum dépassant la quantité maximale de temps que l’opération de déchiffrement serait nécessaire pour n’importe quel segment de données qui contient le remplissage.</span><span class="sxs-lookup"><span data-stu-id="9f060-189">The computation of hold time must have a minimum in excess of the maximum amount of time the decryption operation would take for any data segment that contains padding.</span></span>
  - <span data-ttu-id="9f060-190">Calculs de temps doivent être effectuées selon les instructions de [l’acquisition des horodatages haute résolution](https://msdn.microsoft.com/library/windows/desktop/dn55340.aspx), ne pas à l’aide <xref:System.Environment.TickCount?displayProperty=nameWithType> (susceptibles d’être roll-over/dépassement de capacité) ou la soustraction de deux horodatages système (susceptibles d’être modifiés de NTP erreurs).</span><span class="sxs-lookup"><span data-stu-id="9f060-190">Time computations should be done according to the guidance in [Acquiring high-resolution time stamps](https://msdn.microsoft.com/library/windows/desktop/dn55340.aspx), not by using <xref:System.Environment.TickCount?displayProperty=nameWithType> (subject to roll-over/overflow) or subtracting two system timestamps (subject to NTP adjustment errors).</span></span>
  - <span data-ttu-id="9f060-191">Calculs de temps doivent être qui inclut l’opération de déchiffrement, y compris toutes les exceptions potentielles dans géré ou des applications C++, pas seulement complétées à la fin.</span><span class="sxs-lookup"><span data-stu-id="9f060-191">Time computations must be inclusive of the decryption operation including all potential exceptions in managed or C++ applications, not just padded onto the end.</span></span>
  - <span data-ttu-id="9f060-192">Si la réussite ou l’échec a encore été déterminé, la porte de minutage doit renvoient une erreur lorsqu’il arrive à expiration.</span><span class="sxs-lookup"><span data-stu-id="9f060-192">If success or failure has been determined yet, the timing gate needs to return failure when it expires.</span></span>
- <span data-ttu-id="9f060-193">Les services qui effectuent de déchiffrement non authentifié doivent avoir en place pour détecter qu’un flux de messages « non valides » est venue par le biais du contrôle.</span><span class="sxs-lookup"><span data-stu-id="9f060-193">Services that are performing unauthenticated decryption should have monitoring in place to detect that a flood of "invalid" messages has come through.</span></span>
  - <span data-ttu-id="9f060-194">N’oubliez pas que ce signal comporte des faux positifs (données endommagées légitimement) et faux négatifs (répartir l’attaque sur une période suffisamment longue pour échapper à la détection).</span><span class="sxs-lookup"><span data-stu-id="9f060-194">Bear in mind that this signal carries both false positives (legitimately corrupted data) and false negatives (spreading out the attack over a sufficiently long time to evade detection).</span></span>

## <a name="finding-vulnerable-code---native-applications"></a><span data-ttu-id="9f060-195">Recherche de code vulnérable - applications natives</span><span class="sxs-lookup"><span data-stu-id="9f060-195">Finding vulnerable code - native applications</span></span>

<span data-ttu-id="9f060-196">Pour les programmes basées sur la cryptographie Windows : bibliothèque de Next Generation (CNG) :</span><span class="sxs-lookup"><span data-stu-id="9f060-196">For programs built against the Windows Cryptography: Next Generation (CNG) library:</span></span>

- <span data-ttu-id="9f060-197">L’appel de déchiffrement concerne [BCryptDecrypt](/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt), en spécifiant le `BCRYPT_BLOCK_PADDING` indicateur.</span><span class="sxs-lookup"><span data-stu-id="9f060-197">The decryption call is to [BCryptDecrypt](/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt), specifying the `BCRYPT_BLOCK_PADDING` flag.</span></span>
- <span data-ttu-id="9f060-198">Le handle de clé a été initialisé en appelant [BCryptSetProperty](/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsetproperty) avec [BCRYPT_CHAINING_MODE](https://msdn.microsoft.com/library/windows/desktop/aa376211.aspx#BCRYPT_CHAINING_MODE) défini sur `BCRYPT_CHAIN_MODE_CBC`.</span><span class="sxs-lookup"><span data-stu-id="9f060-198">The key handle has been initialized by calling [BCryptSetProperty](/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsetproperty) with [BCRYPT_CHAINING_MODE](https://msdn.microsoft.com/library/windows/desktop/aa376211.aspx#BCRYPT_CHAINING_MODE) set to `BCRYPT_CHAIN_MODE_CBC`.</span></span>
  - <span data-ttu-id="9f060-199">Dans la mesure où `BCRYPT_CHAIN_MODE_CBC` est la valeur par défaut, affectée code a ne peut-être pas attribué la valeur de `BCRYPT_CHAINING_MODE`.</span><span class="sxs-lookup"><span data-stu-id="9f060-199">Since `BCRYPT_CHAIN_MODE_CBC` is the default, affected code may not have assigned any value for `BCRYPT_CHAINING_MODE`.</span></span>

<span data-ttu-id="9f060-200">Pour les programmes développés à l’API de chiffrement Windows plus anciens :</span><span class="sxs-lookup"><span data-stu-id="9f060-200">For programs built against the older Windows Cryptographic API:</span></span>

- <span data-ttu-id="9f060-201">L’appel de déchiffrement concerne [CryptDecrypt](/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecrypt) avec `Final=TRUE`.</span><span class="sxs-lookup"><span data-stu-id="9f060-201">The decryption call is to [CryptDecrypt](/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecrypt) with `Final=TRUE`.</span></span>
- <span data-ttu-id="9f060-202">Le handle de clé a été initialisé en appelant [CryptSetKeyParam](/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyparam) avec [KP_MODE](https://msdn.microsoft.com/library/windows/desktop/aa379949.aspx#KP_MODE) défini sur `CRYPT_MODE_CBC`.</span><span class="sxs-lookup"><span data-stu-id="9f060-202">The key handle has been initialized by calling [CryptSetKeyParam](/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyparam) with [KP_MODE](https://msdn.microsoft.com/library/windows/desktop/aa379949.aspx#KP_MODE) set to `CRYPT_MODE_CBC`.</span></span>
  - <span data-ttu-id="9f060-203">Dans la mesure où `CRYPT_MODE_CBC` est la valeur par défaut, affectée code a ne peut-être pas attribué la valeur de `KP_MODE`.</span><span class="sxs-lookup"><span data-stu-id="9f060-203">Since `CRYPT_MODE_CBC` is the default, affected code may not have assigned any value for `KP_MODE`.</span></span>

## <a name="finding-vulnerable-code---managed-applications"></a><span data-ttu-id="9f060-204">Code vulnérable recherche - applications managées</span><span class="sxs-lookup"><span data-stu-id="9f060-204">Finding vulnerable code - managed applications</span></span>

- <span data-ttu-id="9f060-205">L’appel de déchiffrement concerne le <xref:System.Security.Cryptography.SymmetricAlgorithm.CreateDecryptor> ou <xref:System.Security.Cryptography.SymmetricAlgorithm.CreateDecryptor(System.Byte[],System.Byte[])> méthodes sur <xref:System.Security.Cryptography.SymmetricAlgorithm?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="9f060-205">The decryption call is to the <xref:System.Security.Cryptography.SymmetricAlgorithm.CreateDecryptor> or <xref:System.Security.Cryptography.SymmetricAlgorithm.CreateDecryptor(System.Byte[],System.Byte[])> methods on <xref:System.Security.Cryptography.SymmetricAlgorithm?displayProperty=nameWithType>.</span></span>
  - <span data-ttu-id="9f060-206">Cela inclut les types dérivés suivants dans le .NET, mais peut également inclure les types de fournisseurs tiers :</span><span class="sxs-lookup"><span data-stu-id="9f060-206">This includes the following derived types within the .NET, but may also include third-party types:</span></span>
    - <xref:System.Security.Cryptography.Aes>
    - <xref:System.Security.Cryptography.AesCng>
    - <xref:System.Security.Cryptography.AesCryptoServiceProvider>
    - <xref:System.Security.Cryptography.AesManaged>
    - <xref:System.Security.Cryptography.DES>
    - <xref:System.Security.Cryptography.DESCryptoServiceProvider>
    - <xref:System.Security.Cryptography.RC2>
    - <xref:System.Security.Cryptography.RC2CryptoServiceProvider>
    - <xref:System.Security.Cryptography.Rijndael>
    - <xref:System.Security.Cryptography.RijndaelManaged>
    - <xref:System.Security.Cryptography.TripleDES>
    - <xref:System.Security.Cryptography.TripleDESCng>
    - <xref:System.Security.Cryptography.TripleDESCryptoServiceProvider>
- <span data-ttu-id="9f060-207">Le <xref:System.Security.Cryptography.SymmetricAlgorithm.Padding?displayProperty=nameWithType> propriété a été définie sur <xref:System.Security.Cryptography.PaddingMode.PKCS7?displayProperty=nameWithType>, <xref:System.Security.Cryptography.PaddingMode.ANSIX923?displayProperty=nameWithType>, ou <xref:System.Security.Cryptography.PaddingMode.ISO10126?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="9f060-207">The <xref:System.Security.Cryptography.SymmetricAlgorithm.Padding?displayProperty=nameWithType> property was set to <xref:System.Security.Cryptography.PaddingMode.PKCS7?displayProperty=nameWithType>, <xref:System.Security.Cryptography.PaddingMode.ANSIX923?displayProperty=nameWithType>, or <xref:System.Security.Cryptography.PaddingMode.ISO10126?displayProperty=nameWithType>.</span></span>
  - <span data-ttu-id="9f060-208">Dans la mesure où <xref:System.Security.Cryptography.PaddingMode.PKCS7?displayProperty=nameWithType> est la valeur par défaut, affectée code ne peut jamais avoir attribué la <xref:System.Security.Cryptography.SymmetricAlgorithm.Padding?displayProperty=nameWithType> propriété.</span><span class="sxs-lookup"><span data-stu-id="9f060-208">Since <xref:System.Security.Cryptography.PaddingMode.PKCS7?displayProperty=nameWithType> is the default, affected code may never have assigned the <xref:System.Security.Cryptography.SymmetricAlgorithm.Padding?displayProperty=nameWithType> property.</span></span>
- <span data-ttu-id="9f060-209">Le <xref:System.Security.Cryptography.SymmetricAlgorithm.Mode?displayProperty=nameWithType> a la valeur de propriété <xref:System.Security.Cryptography.CipherMode.CBC?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="9f060-209">The <xref:System.Security.Cryptography.SymmetricAlgorithm.Mode?displayProperty=nameWithType> property was set to <xref:System.Security.Cryptography.CipherMode.CBC?displayProperty=nameWithType></span></span>
  - <span data-ttu-id="9f060-210">Dans la mesure où <xref:System.Security.Cryptography.CipherMode.CBC?displayProperty=nameWithType> est la valeur par défaut, affectée code ne peut jamais avoir attribué la <xref:System.Security.Cryptography.SymmetricAlgorithm.Mode?displayProperty=nameWithType> propriété.</span><span class="sxs-lookup"><span data-stu-id="9f060-210">Since <xref:System.Security.Cryptography.CipherMode.CBC?displayProperty=nameWithType> is the default, affected code may never have assigned the <xref:System.Security.Cryptography.SymmetricAlgorithm.Mode?displayProperty=nameWithType> property.</span></span>

## <a name="finding-vulnerable-code---cryptographic-message-syntax"></a><span data-ttu-id="9f060-211">Recherche de code vulnérable - syntaxe de message de chiffrement</span><span class="sxs-lookup"><span data-stu-id="9f060-211">Finding vulnerable code - cryptographic message syntax</span></span>

<span data-ttu-id="9f060-212">Un message CMS EnvelopedData non authentifié dont le contenu chiffré utilise le mode CBC AES (2.16.840.1.101.3.4.1.2, 2.16.840.1.101.3.4.1.22, 2.16.840.1.101.3.4.1.42), DES (1.3.14.3.2.7), 3DES (1.2.840.113549.3.7) ou RC2 (1.2.840.113549.3.2) est vulnérable, ainsi que des messages à l’aide de n’importe quel autres algorithmes de chiffrement par bloc en mode CBC.</span><span class="sxs-lookup"><span data-stu-id="9f060-212">An unauthenticated CMS EnvelopedData message whose encrypted content uses the CBC mode of AES (2.16.840.1.101.3.4.1.2, 2.16.840.1.101.3.4.1.22, 2.16.840.1.101.3.4.1.42), DES (1.3.14.3.2.7), 3DES (1.2.840.113549.3.7) or RC2 (1.2.840.113549.3.2) is vulnerable, as well as messages using any other block cipher algorithms in CBC mode.</span></span>

<span data-ttu-id="9f060-213">Tandis que les chiffrements de flux ne sont pas sensibles à cette vulnérabilité, Microsoft vous recommande de toujours authentifier les données au fil de l’inspection de la valeur ContentEncryptionAlgorithm.</span><span class="sxs-lookup"><span data-stu-id="9f060-213">While stream ciphers aren't susceptible to this particular vulnerability, Microsoft recommends always authenticating the data over inspecting the ContentEncryptionAlgorithm value.</span></span>

<span data-ttu-id="9f060-214">Pour les applications managées, un EnvelopedData CMS blob peut être détecté comme n’importe quelle valeur passée à <xref:System.Security.Cryptography.Pkcs.EnvelopedCms.Decode(System.Byte[])?displayProperty=fullName>.</span><span class="sxs-lookup"><span data-stu-id="9f060-214">For managed applications, a CMS EnvelopedData blob can be detected as any value that is passed to <xref:System.Security.Cryptography.Pkcs.EnvelopedCms.Decode(System.Byte[])?displayProperty=fullName>.</span></span>

<span data-ttu-id="9f060-215">Pour les applications natives, un objet blob CMS EnvelopedData peut être détecté en tant que la valeur fournie pour un handle CMS via [CryptMsgUpdate](/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgupdate) dont résultant [CMSG_TYPE_PARAM](/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetparam) est `CMSG_ENVELOPED` et/ou le handle CMS est envoyées ultérieurement un `CMSG_CTRL_DECRYPT` instruction via [CryptMsgControl](/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol).</span><span class="sxs-lookup"><span data-stu-id="9f060-215">For native applications, a CMS EnvelopedData blob can be detected as any value provided to a CMS handle via [CryptMsgUpdate](/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgupdate) whose resulting [CMSG_TYPE_PARAM](/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetparam) is `CMSG_ENVELOPED` and/or the CMS handle is later sent a `CMSG_CTRL_DECRYPT` instruction via [CryptMsgControl](/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol).</span></span>

## <a name="vulnerable-code-example---managed"></a><span data-ttu-id="9f060-216">Exemple de code vulnérable - géré</span><span class="sxs-lookup"><span data-stu-id="9f060-216">Vulnerable code example - managed</span></span>

<span data-ttu-id="9f060-217">Cette méthode lit un cookie et la déchiffre et aucune vérification de l’intégrité des données est visible.</span><span class="sxs-lookup"><span data-stu-id="9f060-217">This method reads a cookie and decrypts it and no data integrity check is visible.</span></span> <span data-ttu-id="9f060-218">Par conséquent, le contenu d’un cookie qui est lu par cette méthode peut être attaqué par l’utilisateur qui les ont reçues, ou par n’importe quel agresseur a obtenu la valeur du cookie chiffré.</span><span class="sxs-lookup"><span data-stu-id="9f060-218">Therefore, the contents of a cookie that is read by this method can be attacked by the user who received it, or by any attacker who has obtained the encrypted cookie value.</span></span>

```csharp
private byte[] DecryptCookie(string cookieName)
{
    HttpCookie cookie = Request.Cookies[cookieName];

    if (cookie == null)
    {
        return null;
    }

    using (ICryptoTransform decryptor = _aes.CreateDecryptor())
    using (MemoryStream memoryStream = new MemoryStream())
    using (CryptoStream cryptoStream =
        new CryptoStream(memoryStream, decryptor, CryptoStreamMode.Write))
    {
        byte[] readCookie = Convert.FromBase64String(cookie.Value);
        cryptoStream.Write(readCookie, 0, readCookie.Length);
        cryptoStream.FlushFinalBlock();
        return memoryStream.ToArray();
    }
}
```

## <a name="example-code-following-recommended-practices---managed"></a><span data-ttu-id="9f060-219">Exemple suivant de code recommandées - géré</span><span class="sxs-lookup"><span data-stu-id="9f060-219">Example code following recommended practices - managed</span></span>

<span data-ttu-id="9f060-220">L’exemple de code suivant utilise un format de message non standard de</span><span class="sxs-lookup"><span data-stu-id="9f060-220">The following sample code uses a non-standard message format of</span></span>

`cipher_algorithm_id || hmac_algorithm_id || hmac_tag || iv || ciphertext`

<span data-ttu-id="9f060-221">où les `cipher_algorithm_id` et `hmac_algorithm_id` identificateurs d’algorithme sont des représentations de (non standard) local de l’application de ces algorithmes.</span><span class="sxs-lookup"><span data-stu-id="9f060-221">where the `cipher_algorithm_id` and `hmac_algorithm_id` algorithm identifiers are application-local (non-standard) representations of those algorithms.</span></span> <span data-ttu-id="9f060-222">Ces identificateurs peuvent être judicieux dans d’autres parties de votre protocole de messagerie existant et non comme un flux d’octets concaténée strict.</span><span class="sxs-lookup"><span data-stu-id="9f060-222">These identifiers may make sense in other parts of your existing messaging protocol instead of as a bare concatenated bytestream.</span></span>

<span data-ttu-id="9f060-223">Cet exemple utilise également une clé principale unique pour dériver une clé de chiffrement et une clé HMAC.</span><span class="sxs-lookup"><span data-stu-id="9f060-223">This example also uses a single master key to derive both an encryption key and an HMAC key.</span></span> <span data-ttu-id="9f060-224">Ceci est fourni à la fois comme une commodité pour l’activation d’une application indexé séparément dans une application de clés en double et à encourager la conservation des valeurs d’autre que les deux clés.</span><span class="sxs-lookup"><span data-stu-id="9f060-224">This is provided both as a convenience for turning a singly-keyed application into a dual-keyed application, and to encourage keeping the two keys as different values.</span></span> <span data-ttu-id="9f060-225">Elle garantit davantage que la clé HMAC et la clé de chiffrement ne peut pas tirer parti de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="9f060-225">It further guarantees that the HMAC key and encryption key can't get out of synchronization.</span></span>

<span data-ttu-id="9f060-226">Cet exemple n’accepte pas un <xref:System.IO.Stream> pour le chiffrement ou déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="9f060-226">This sample doesn't accept a <xref:System.IO.Stream> for either encryption or decryption.</span></span> <span data-ttu-id="9f060-227">Une étape du fait de format de données actuelle chiffrer difficile, car le `hmac_tag` valeur précède le texte chiffré.</span><span class="sxs-lookup"><span data-stu-id="9f060-227">The current data format makes one-pass encrypt difficult because the `hmac_tag` value precedes the ciphertext.</span></span> <span data-ttu-id="9f060-228">Toutefois, ce format a été choisi, car il conserve tous les éléments de taille fixe au début pour conserver la plus simple de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="9f060-228">However, this format was chosen because it keeps all of the fixed-size elements at the beginning to keep the parser simpler.</span></span> <span data-ttu-id="9f060-229">Avec ce format de données, une seule passe decrypt est possible, même si un implémenteur est imminente pour appeler GetHashAndReset et vérifier le résultat avant d’appeler TransformFinalBlock.</span><span class="sxs-lookup"><span data-stu-id="9f060-229">With this data format, one-pass decrypt is possible, though an implementer is cautioned to call GetHashAndReset and verify the result before calling TransformFinalBlock.</span></span> <span data-ttu-id="9f060-230">Si le chiffrement de diffusion en continu est important, un autre mode AE peut être requis.</span><span class="sxs-lookup"><span data-stu-id="9f060-230">If streaming encryption is important, then a different AE mode may be required.</span></span>

```csharp
// ==++==
//
//   Copyright (c) Microsoft Corporation.  All rights reserved.
//
//   Shared under the terms of the Microsoft Public License,
//   https://opensource.org/licenses/MS-PL
//
// ==--==

using System;
using System.Diagnostics;
using System.IO;
using System.Runtime.CompilerServices;
using System.Security.Cryptography;

namespace Microsoft.Examples.Cryptography
{
    public enum AeCipher : byte
    {
        Unknown,
        Aes256CbcPkcs7,
    }

    public enum AeMac : byte
    {
        Unknown,
        HMACSHA256,
        HMACSHA384,
    }

    /// <summary>
    /// Provides extension methods to make HashAlgorithm look like .NET Core's
    /// IncrementalHash
    /// </summary>
    internal static class IncrementalHashExtensions
    {
        public static void AppendData(this HashAlgorithm hash, byte[] data)
        {
            hash.TransformBlock(data, 0, data.Length, null, 0);
        }

        public static void AppendData(
            this HashAlgorithm hash,
            byte[] data,
            int offset,
            int length)
        {
            hash.TransformBlock(data, offset, length, null, 0);
        }

        public static byte[] GetHashAndReset(this HashAlgorithm hash)
        {
            hash.TransformFinalBlock(Array.Empty<byte>(), 0, 0);
            return hash.Hash;
        }
    }

    public static partial class AuthenticatedEncryption
    {
        /// <summary>
        /// Use <paramref name="masterKey"/> to derive two keys (one cipher, one HMAC)
        /// to provide authenticated encryption for <paramref name="message"/>.
        /// </summary>
        /// <param name="masterKey">The master key from which other keys derive.</param>
        /// <param name="message">The message to encrypt</param>
        /// <returns>
        /// A concatenation of
        /// [cipher algorithm+chainmode+padding][mac algorithm][authtag][IV][ciphertext],
        /// suitable to be passed to <see cref="Decrypt"/>.
        /// </returns>
        /// <remarks>
        /// <paramref name="masterKey"/> should be a 128-bit (or bigger) value generated
        /// by a secure random number generator, such as the one returned from
        /// <see cref="RandomNumberGenerator.Create()"/>.
        /// This implementation chooses to block deficient inputs by length, but does not
        /// make any attempt at discerning the randomness of the key.
        ///
        /// If the master key is being input by a prompt (like a password/passphrase)
        /// then it should be properly turned into keying material via a Key Derivation
        /// Function like PBKDF2, represented by Rfc2898DeriveBytes. A 'password' should
        /// never be simply turned to bytes via an Encoding class and used as a key.
        /// </remarks>
        public static byte[] Encrypt(byte[] masterKey, byte[] message)
        {
            if (masterKey == null)
                throw new ArgumentNullException(nameof(masterKey));
            if (masterKey.Length < 16)
                throw new ArgumentOutOfRangeException(
                    nameof(masterKey),
                    "Master Key must be at least 128 bits (16 bytes)");
            if (message == null)
                throw new ArgumentNullException(nameof(message));

            // First, choose an encryption scheme.
            AeCipher aeCipher = AeCipher.Aes256CbcPkcs7;

            // Second, choose an authentication (message integrity) scheme.
            //
            // In this example we use the master key length to change from HMACSHA256 to
            // HMACSHA384, but that is completely arbitrary. This mostly represents a
            // "cryptographic needs change over time" scenario.
            AeMac aeMac = masterKey.Length < 48 ? AeMac.HMACSHA256 : AeMac.HMACSHA384;

            // It's good to be able to identify what choices were made when a message was
            // encrypted, so that the message can later be decrypted. This allows for
            // future versions to add support for new encryption schemes, but still be
            // able to read old data. A practice known as "cryptographic agility".
            //
            // This is similar in practice to PKCS#7 messaging, but this uses a
            // private-scoped byte rather than a public-scoped Object IDentifier (OID).
            // Please note that the scheme in this example adheres to no particular
            // standard, and is unlikely to survive to a more complete implementation in
            // the .NET Framework.
            //
            // You may be well-served by prepending a version number byte to this
            // message, but may want to avoid the value 0x30 (the leading byte value for
            // DER-encoded structures such as X.509 certificates and PKCS#7 messages).
            byte[] algorithmChoices = { (byte)aeCipher, (byte)aeMac };
            byte[] iv;
            byte[] cipherText;
            byte[] tag;

            // Using our algorithm choices, open an HMAC (as an authentication tag
            // generator) and a SymmetricAlgorithm which use different keys each derived
            // from the same master key.
            //
            // A custom implementation may very well have distinctly managed secret keys
            // for the MAC and cipher, this example merely demonstrates the master to
            // derived key methodology to encourage key separation from the MAC and
            // cipher keys.
            using (HMAC tagGenerator = GetMac(aeMac, masterKey))
            {
                using (SymmetricAlgorithm cipher = GetCipher(aeCipher, masterKey))
                using (ICryptoTransform encryptor = cipher.CreateEncryptor())
                {
                    // Since no IV was provided, a random one has been generated
                    // during the call to CreateEncryptor.
                    //
                    // But note that it only does the auto-generation once. If the cipher
                    // object were used again, a call to GenerateIV would have been
                    // required.
                    iv = cipher.IV;

                    cipherText = Transform(encryptor, message, 0, message.Length);
                }

                // The IV and ciphertest both need to be included in the MAC to prevent
                // tampering.
                //
                // By including the algorithm identifiers, we have technically moved from
                // simple Authenticated Encryption (AE) to Authenticated Encryption with
                // Additional Data (AEAD). By including the algorithm identifiers in the
                // MAC, it becomes harder for an attacker to change them as an attempt to
                // perform a downgrade attack.
                //
                // If you've added a data format version field, it can also be included
                // in the MAC to further inhibit an attacker's options for confusing the
                // data processor into believing the tampered message is valid.
                tagGenerator.AppendData(algorithmChoices);
                tagGenerator.AppendData(iv);
                tagGenerator.AppendData(cipherText);
                tag = tagGenerator.GetHashAndReset();
            }

            // Build the final result as the concatenation of everything except the keys.
            int totalLength =
                algorithmChoices.Length +
                tag.Length +
                iv.Length +
                cipherText.Length;

            byte[] output = new byte[totalLength];
            int outputOffset = 0;

            Append(algorithmChoices, output, ref outputOffset);
            Append(tag, output, ref outputOffset);
            Append(iv, output, ref outputOffset);
            Append(cipherText, output, ref outputOffset);

            Debug.Assert(outputOffset == output.Length);
            return output;
        }

        /// <summary>
        /// Reads a message produced by <see cref="Encrypt"/> after verifying it hasn't
        /// been tampered with.
        /// </summary>
        /// <param name="masterKey">The master key from which other keys derive.</param>
        /// <param name="cipherText">
        /// The output of <see cref="Encrypt"/>: a concatenation of a cipher ID, mac ID,
        /// authTag, IV, and cipherText.
        /// </param>
        /// <returns>The decrypted content.</returns>
        /// <exception cref="ArgumentNullException">
        /// <paramref name="masterKey"/> is <c>null</c>.
        /// </exception>
        /// <exception cref="ArgumentNullException">
        /// <paramref name="cipherText"/> is <c>null</c>.
        /// </exception>
        /// <exception cref="CryptographicException">
        /// <paramref name="cipherText"/> identifies unknown algorithms, is not long
        /// enough, fails a data integrity check, or fails to decrypt.
        /// </exception>
        /// <remarks>
        /// <paramref name="masterKey"/> should be a 128-bit (or larger) value
        /// generated by a secure random number generator, such as the one returned from
        /// <see cref="RandomNumberGenerator.Create()"/>. This implementation chooses to
        /// block deficient inputs by length, but doesn't make any attempt at
        /// discerning the randomness of the key.
        ///
        /// If the master key is being input by a prompt (like a password/passphrase),
        /// then it should be properly turned into keying material via a Key Derivation
        /// Function like PBKDF2, represented by Rfc2898DeriveBytes. A 'password' should
        /// never be simply turned to bytes via an Encoding class and used as a key.
        /// </remarks>
        public static byte[] Decrypt(byte[] masterKey, byte[] cipherText)
        {
            // This example continues the .NET practice of throwing exceptions for
            // failures. If you consider message tampering to be normal (and thus
            // "not exceptional") behavior, you may like the signature
            // bool Decrypt(byte[] messageKey, byte[] cipherText, out byte[] message)
            // better.
            if (masterKey == null)
                throw new ArgumentNullException(nameof(masterKey));
            if (masterKey.Length < 16)
                throw new ArgumentOutOfRangeException(
                    nameof(masterKey),
                    "Master Key must be at least 128 bits (16 bytes)");
            if (cipherText == null)
                throw new ArgumentNullException(nameof(cipherText));

            // The format of this message is assumed to be public, so there's no harm in
            // saying ahead of time that the message makes no sense.
            if (cipherText.Length < 2)
            {
                throw new CryptographicException();
            }

            // Use the message algorithm headers to determine what cipher algorithm and
            // MAC algorithm are going to be used. Since the same Key Derivation
            // Functions (KDFs) are being used in Decrypt as Encrypt, the keys are also
            // the same.
            AeCipher aeCipher = (AeCipher)cipherText[0];
            AeMac aeMac = (AeMac)cipherText[1];

            using (SymmetricAlgorithm cipher = GetCipher(aeCipher, masterKey))
            using (HMAC tagGenerator = GetMac(aeMac, masterKey))
            {
                int blockSizeInBytes = cipher.BlockSize / 8;
                int tagSizeInBytes = tagGenerator.HashSize / 8;
                int headerSizeInBytes = 2;
                int tagOffset = headerSizeInBytes;
                int ivOffset = tagOffset + tagSizeInBytes;
                int cipherTextOffset = ivOffset + blockSizeInBytes;
                int cipherTextLength = cipherText.Length - cipherTextOffset;
                int minLen = cipherTextOffset + blockSizeInBytes;

                // Again, the minimum length is still assumed to be public knowledge,
                // nothing has leaked out yet. The minimum length couldn't just be calculated
                // without reading the header.
                if (cipherText.Length < minLen)
                {
                    throw new CryptographicException();
                }

                // It's very important that the MAC be calculated and verified before
                // proceeding to decrypt the ciphertext, as this prevents any sort of
                // information leaking out to an attacker.
                //
                // Don't include the tag in the calculation, though.

                // First, everything before the tag (the cipher and MAC algorithm ids)
                tagGenerator.AppendData(cipherText, 0, tagOffset);

                // Skip the data before the tag and the tag, then read everything that
                // remains.
                tagGenerator.AppendData(
                    cipherText,
                    tagOffset + tagSizeInBytes,
                    cipherText.Length - tagSizeInBytes - tagOffset);

                byte[] generatedTag = tagGenerator.GetHashAndReset();

                // The time it took to get to this point has so far been a function only
                // of the length of the data, or of non-encrypted values (e.g. it could
                // take longer to prepare the *key* for the HMACSHA384 MAC than the
                // HMACSHA256 MAC, but the algorithm choice wasn't a secret).
                //
                // If the verification of the authentication tag aborts as soon as a
                // difference is found in the byte arrays then your program may be
                // acting as a timing oracle which helps an attacker to brute-force the
                // right answer for the MAC. So, it's very important that every possible
                // "no" (2^256-1 of them for HMACSHA256) be evaluated in as close to the
                // same amount of time as possible. For this, we call CryptographicEquals
                if (!CryptographicEquals(
                    generatedTag,
                    0,
                    cipherText,
                    tagOffset,
                    tagSizeInBytes))
                {
                    // Assuming every tampered message (of the same length) took the same
                    // amount of time to process, we can now safely say
                    // "this data makes no sense" without giving anything away.
                    throw new CryptographicException();
                }

                // Restore the IV into the symmetricAlgorithm instance.
                byte[] iv = new byte[blockSizeInBytes];
                Buffer.BlockCopy(cipherText, ivOffset, iv, 0, iv.Length);
                cipher.IV = iv;

                using (ICryptoTransform decryptor = cipher.CreateDecryptor())
                {
                    return Transform(
                        decryptor,
                        cipherText,
                        cipherTextOffset,
                        cipherTextLength);
                }
            }
        }

        private static byte[] Transform(
            ICryptoTransform transform,
            byte[] input,
            int inputOffset,
            int inputLength)
        {
            // Many of the implementations of ICryptoTransform report true for
            // CanTransformMultipleBlocks, and when the entire message is available in
            // one shot this saves on the allocation of the CryptoStream and the
            // intermediate structures it needs to properly chunk the message into blocks
            // (since the underlying stream won't always return the number of bytes
            // needed).
            if (transform.CanTransformMultipleBlocks)
            {
                return transform.TransformFinalBlock(input, inputOffset, inputLength);
            }

            // If our transform couldn't do multiple blocks at once, let CryptoStream
            // handle the chunking.
            using (MemoryStream messageStream = new MemoryStream())
            using (CryptoStream cryptoStream =
                new CryptoStream(messageStream, transform, CryptoStreamMode.Write))
            {
                cryptoStream.Write(input, inputOffset, inputLength);
                cryptoStream.FlushFinalBlock();
                return messageStream.ToArray();
            }
        }

        /// <summary>
        /// Open a properly configured <see cref="SymmetricAlgorithm"/> conforming to the
        /// scheme identified by <paramref name="aeCipher"/>.
        /// </summary>
        /// <param name="aeCipher">The cipher mode to open.</param>
        /// <param name="masterKey">The master key from which other keys derive.</param>
        /// <returns>
        /// A SymmetricAlgorithm object with the right key, cipher mode, and padding
        /// mode; or <c>null</c> on unknown algorithms.
        /// </returns>
        private static SymmetricAlgorithm GetCipher(AeCipher aeCipher, byte[] masterKey)
        {
            SymmetricAlgorithm symmetricAlgorithm;

            switch (aeCipher)
            {
                case AeCipher.Aes256CbcPkcs7:
                    symmetricAlgorithm = Aes.Create();
                    // While 256-bit, CBC, and PKCS7 are all the default values for these
                    // properties, being explicit helps comprehension more than it hurts
                    // performance.
                    symmetricAlgorithm.KeySize = 256;
                    symmetricAlgorithm.Mode = CipherMode.CBC;
                    symmetricAlgorithm.Padding = PaddingMode.PKCS7;
                    break;
                default:
                    // An algorithm we don't understand
                    throw new CryptographicException();
            }

            // Instead of using the master key directly, derive a key for our chosen
            // HMAC algorithm based upon the master key.
            //
            // Since none of the symmetric encryption algorithms currently in .NET
            // support key sizes greater than 256-bit, we can use HMACSHA256 with
            // NIST SP 800-108 5.1 (Counter Mode KDF) to derive a value that is
            // no smaller than the key size, then Array.Resize to trim it down as
            // needed.

            using (HMAC hmac = new HMACSHA256(masterKey))
            {
                // i=1, Label=ASCII(cipher)
                byte[] cipherKey = hmac.ComputeHash(
                    new byte[] { 1, 99, 105, 112, 104, 101, 114 });

                // Resize the array to the desired keysize. KeySize is in bits,
                // and Array.Resize wants the length in bytes.
                Array.Resize(ref cipherKey, symmetricAlgorithm.KeySize / 8);

                symmetricAlgorithm.Key = cipherKey;
            }

            return symmetricAlgorithm;
        }

        /// <summary>
        /// Open a properly configured <see cref="HMAC"/> conforming to the scheme
        /// identified by <paramref name="aeMac"/>.
        /// </summary>
        /// <param name="aeMac">The message authentication mode to open.</param>
        /// <param name="masterKey">The master key from which other keys derive.</param>
        /// <returns>
        /// An HMAC object with the proper key, or <c>null</c> on unknown algorithms.
        /// </returns>
        private static HMAC GetMac(AeMac aeMac, byte[] masterKey)
        {
            HMAC hmac;

            switch (aeMac)
            {
                case AeMac.HMACSHA256:
                    hmac = new HMACSHA256();
                    break;
                case AeMac.HMACSHA384:
                    hmac = new HMACSHA384();
                    break;
                default:
                    // An algorithm we don't understand
                    throw new CryptographicException();
            }

            // Instead of using the master key directly, derive a key for our chosen
            // HMAC algorithm based upon the master key.
            // Since the output size of the HMAC is the same as the ideal key size for
            // the HMAC, we can use the master key over a fixed input once to perform
            // NIST SP 800-108 5.1 (Counter Mode KDF):
            hmac.Key = masterKey;

            // i=1, Context=ASCII(MAC)
            byte[] newKey = hmac.ComputeHash(new byte[] { 1, 77, 65, 67 });

            hmac.Key = newKey;
            return hmac;
        }

        // A simple helper method to ensure that the offset (writePos) always moves
        // forward with new data.
        private static void Append(byte[] newData, byte[] combinedData, ref int writePos)
        {
            Buffer.BlockCopy(newData, 0, combinedData, writePos, newData.Length);
            writePos += newData.Length;
        }

        /// <summary>
        /// Compare the contents of two arrays in an amount of time which is only
        /// dependent on <paramref name="length"/>.
        /// </summary>
        /// <param name="a">An array to compare to <paramref name="b"/>.</param>
        /// <param name="aOffset">
        /// The starting position within <paramref name="a"/> for comparison.
        /// </param>
        /// <param name="b">An array to compare to <paramref name="a"/>.</param>
        /// <param name="bOffset">
        /// The starting position within <paramref name="b"/> for comparison.
        /// </param>
        /// <param name="length">
        /// The number of bytes to compare between <paramref name="a"/> and
        /// <paramref name="b"/>.</param>
        /// <returns>
        /// <c>true</c> if both <paramref name="a"/> and <paramref name="b"/> have
        /// sufficient length for the comparison and all of the applicable values are the
        /// same in both arrays; <c>false</c> otherwise.
        /// </returns>
        /// <remarks>
        /// An "insufficient data" <c>false</c> response can happen early, but otherwise
        /// a <c>true</c> or <c>false</c> response take the same amount of time.
        /// </remarks>
        [MethodImpl(MethodImplOptions.NoInlining | MethodImplOptions.NoOptimization)]
        private static bool CryptographicEquals(
            byte[] a,
            int aOffset,
            byte[] b,
            int bOffset,
            int length)
        {
            Debug.Assert(a != null);
            Debug.Assert(b != null);
            Debug.Assert(length >= 0);

            int result = 0;

            if (a.Length - aOffset < length || b.Length - bOffset < length)
            {
                return false;
            }

            unchecked
            {
                for (int i = 0; i < length; i++)
                {
                    // Bitwise-OR of subtraction has been found to have the most
                    // stable execution time.
                    //
                    // This cannot overflow because bytes are 1 byte in length, and
                    // result is 4 bytes.
                    // The OR propagates all set bytes, so the differences are only
                    // present in the lowest byte.
                    result = result | (a[i + aOffset] - b[i + bOffset]);
                }
            }

            return result == 0;
        }
    }
}
```
