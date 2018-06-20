---
title: Vulnérabilités de temporisation avec le déchiffrement symétrique en mode CBC à l’aide du remplissage
description: Découvrez comment détecter et atténuer les vulnérabilités de minutage avec déchiffrement symétrique sur le mode Cipher Block Chaining (CBC) à l’aide du remplissage.
ms.date: 06/12/2018
author: blowdart
ms.author: mairaw
ms.openlocfilehash: 26f4d19f591ac02d792bebbd648e90b07d84de56
ms.sourcegitcommit: 6bc4efca63e526ce6f2d257fa870f01f8c459ae4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2018
ms.locfileid: "36208685"
---
# <a name="timing-vulnerabilities-with-cbc-mode-symmetric-decryption-using-padding"></a>Vulnérabilités de temporisation avec le déchiffrement symétrique en mode CBC à l’aide du remplissage

Microsoft estime qu’il n’est plus sûr déchiffrer les données chiffrées avec le mode Cipher Block Chaining (CBC) de chiffrement symétrique lorsque vérifiable remplissage a été appliqué sans première vérification de l’intégrité du texte chiffré, à l’exception de très spécifique les circonstances. Cette décision est basée sur les recherches connus sur le chiffrement. 

## <a name="introduction"></a>Introduction

Une attaque d’oracle de remplissage est un type d’attaque contre les données chiffrées qui permet à la personne malveillante déchiffrer le contenu des données, sans connaître la clé.

Oracle fait référence à un « en savoir » qui donne une personne malveillante d’informations que l’action qu’ils l’exécution est correcte ou non. Imaginez la lecture d’un tableau ou une carte de jeu avec un enfant. Lorsque son face allume avec un grand sourire, car elle pense qu’il est sur le point d’effectuer un mouvement bon, ce qui est d’oracle. Vous, en tant que l’adversaire, pourrez utiliser cette oracle pour planifier votre prochain déplacement correctement.

Le remplissage est un terme de chiffrement spécifique. Des chiffrements qui sont les algorithmes utilisés pour chiffrer vos données, fonctionnent sur des blocs de données où chaque bloc est de taille fixe. Si les données que vous souhaitez chiffrer n’est pas la bonne taille pour remplir les blocs, vos données sont complétées jusqu'à ce qu’il effectue. De nombreux formulaires de remplissage nécessitent ce remplissage soit toujours présent, même si l’entrée d’origine était la taille appropriée. Ainsi, la marge intérieure à toujours être supprimée sans risque sur le déchiffrement.

Assembler les deux tâches, une implémentation logicielle avec un remplissage d’oracle révèle si les données déchiffrées ont remplissage valid. Oracle peut être simplement retourner une valeur qui indique « Remplissage non valide » ou plus complexe à prendre une heure sensiblement différente pour traiter un bloc valide, par opposition à un bloc non valide.

Le chiffrement par bloc par une autre propriété, appelée le mode qui détermine la relation de données dans le premier bloc de données dans le deuxième bloc, et ainsi de suite. Un des modes couramment utilisées est CBC. CBC introduit un bloc aléatoire initial, connu en tant que le vecteur d’initialisation (IV) et associe le bloc précédent le résultat d’un chiffrement statique pour le rendre telle que le chiffrement du message de même avec la même clé ne produire toujours le même résultat crypté.

Une personne malveillante peut utiliser une marge intérieure oracle, en association avec la structure des données de CBC, pour envoyer des messages légèrement modifiés pour le code qui expose l’oracle et conserver envoi de données jusqu'à ce qu’oracle leur indique les données sont correctes. À partir de cette réponse, l’attaquant peut déchiffrer le message octet par octet.

Réseaux d’ordinateurs modernes sont d’une qualité élevée qu’un attaquant peut détecter très faible (inférieure à 0,1 ms) les différences dans l’exécution de temps sur les systèmes distants. Les applications qui sont en supposant que le déchiffrement réussi ne peut se produire lorsque les données n’a pas été falsifiées peuvent être vulnérables aux attaques à partir d’outils sont conçus pour observer les différences de déchiffrement réussi et ayant échoué. Cette différence de minuterie peut être plus importante dans certaines langues ou des bibliothèques que d’autres, il est désormais croire qu’il s’agit d’une menace pratique pour tous les langages et les bibliothèques lors de la réponse de l’application à la défaillance est pris en compte.

Cette attaque s’appuie sur la possibilité de modifier les données chiffrées et de tester le résultat avec oracle. La seule façon entièrement atténuer l’attaque consiste à détecter les modifications apportées aux données chiffrées et refuse d’effectuer des actions sur celui-ci. Pour ce faire, la standard consiste à créer une signature pour les données et valider la signature avant que toutes les opérations sont effectuées. La signature doit être vérifiable, il ne peut pas être créé par la personne malveillante, sinon ils seraient modifier les données chiffrées, puis calculer une nouvelle signature basée sur les données modifiées. Un type courant de la signature appropriée est appelé un code d’authentification de message de hachage à clé (HMAC). Un code HMAC diffère une somme de contrôle dans la mesure où il prend une clé secrète, connu uniquement à la personne produisant le code HMAC et à la personne sa validation. Sans la possession de la clé, vous ne peut pas produire un code HMAC correct. Lorsque vous recevez vos données, vous serait prendre les données chiffrées, indépendamment de calcul du code HMAC à l’aide de la clé secrète vous et le partage de l’expéditeur, puis compare le HMAC ils envoyés par rapport à celle calculé. Cette comparaison doit être temps constant, sinon vous avez ajouté un autre oracle détectable, ce qui permet un autre type d’attaque.

En résumé, pour utiliser complété le chiffrement par blocs CBC en toute sécurité, vous devez les combiner avec un code HMAC (ou un autre contrôle d’intégrité de données) que vous validez à l’aide d’une comparaison de temps avant d’essayer de déchiffrer les données. Étant donné que tous les messages modifiées de temps la même quantité pour produire une réponse, l’attaque est bloqué.

## <a name="who-is-vulnerable"></a>Qui est vulnérable

Cette vulnérabilité s’applique aux applications gérées et natives qui effectuent leur propre chiffrement et le déchiffrement. Cela inclut, par exemple :

- Une application qui chiffre un cookie pour le déchiffrement de version ultérieure sur le serveur.
- Une application de base de données qui offre la possibilité aux utilisateurs d’insérer des données dans une table dont les colonnes sont déchiffrées.
- Une application de transfert de données qui s’appuie sur le chiffrement à l’aide d’une clé partagée pour protéger les données en transit.
- Une application qui chiffre et déchiffre les messages « à l’intérieur » du tunnel TLS.

Notez qu’à l’aide de TLS seul ne peut pas protéger dans ces scénarios.

Une application vulnérable :

- Déchiffre les données à l’aide du mode de chiffrement CBC avec un mode de remplissage vérifiable, tels que PKCS #7 ou ANSI X.923.
- Effectue le déchiffrement sans avoir effectué une vérification de l’intégrité des données (via un MAC ou une signature numérique asymétrique).

Cela s’applique également aux applications reposant sur les abstractions au-dessus de ces primitives, tels que la structure de DonnéesEnveloppées Cryptographic Message Syntax (PKCS #7/CMS).

## <a name="related-areas-of-concern"></a>Zones posant problème connexes

Research a conduit Microsoft plus concernées sur les messages CBC sont complétées avec équivalent ISO 10126 remplissage lorsque le message a une structure de pied de page connus ou prévisibles. Par exemple, le contenu préparé selon les règles de la syntaxe du chiffrement XML W3C et la recommandation de traitement (xmlenc EncryptedXml). Bien que les recommandations du W3C pour signer le message, puis chiffrer a été considéré comme appropriée en temps, Microsoft maintenant recommande toujours signer puis chiffrer.

Les développeurs d’applications doivent toujours être conscients de vérification de la mise en application d’une clé de signature asymétrique, car il n’existe aucune relation d’approbation inhérente entre une clé asymétrique et un message arbitraire.

## <a name="details"></a>Détails

Historiquement, il a été consensus qu’il est important de chiffrer et authentifier des données importantes, à l’aide de moyens tels que les signatures HMAC ou RSA. Toutefois, il a été inférieur des indications précises sur la procédure pour séquencer les opérations de chiffrement et d’authentification. En raison de la vulnérabilité détaillée dans cet article, les conseils de Microsoft est désormais à toujours utiliser le paradigme « encrypt-then-sign ». Autrement dit, chiffrer les données à l’aide d’une clé symétrique avant le calcul de signature asymétrique MAC sur le texte chiffré (données chiffrées). Lors du déchiffrement des données, effectuer l’inverse. Tout d’abord, vérifiez l’adresse MAC ou signature du texte chiffré, puis le déchiffrer.

Une classe de vulnérabilités appelé « remplissage oracle attaques » ont été identifiés existe depuis plus de 10 ans. Ces vulnérabilités permettent une personne malveillante de déchiffrer les données chiffrées par les algorithmes symétrique, tel que AES et 3DES, à l’aide de 4096 pas plus de tentatives par bloc de données. Ces vulnérabilités rendre l’utilisation du fait que les chiffrements par bloc les plus fréquemment utilisés avec des données de remplissage vérifiable à la fin. Il a été constaté que si une personne malveillante peut falsifier le texte chiffré et savoir si la falsification a provoqué une erreur dans le format de la marge intérieure à la fin, la personne malveillante peut déchiffrer les données.

Au départ, attaques pratiques étaient basées sur les services qui doit retourner des codes d’erreur différents selon si le remplissage était valide, telle que la vulnérabilité dans ASP.NET [MS10-070](https://technet.microsoft.com/library/security/ms10-070.aspx). Toutefois, Microsoft estime maintenant qu’il est possible d’effectuer des attaques similaires à l’aide uniquement les différences dans la synchronisation entre le traitement de remplissage valide et non valide.

Si le schéma de chiffrement utilise une signature et vérification de la signature est effectué avec un runtime fixe pour une période donnée de données (quel que soit le contenu), l’intégrité des données peuvent être vérifié sans l’émission de toutes les informations à un intrus via un [canal latéral](https://en.wikipedia.org/wiki/Side-channel_attack). Étant donné que le contrôle d’intégrité rejette les messages falsifiés, la remplissage une menace pour oracle est atténuée.

## <a name="guidance"></a>Conseils

Tout d’abord, Microsoft recommande que les données ayant la confidentialité doivent être transmises sur sécurité TLS (Transport Layer), le successeur de couche SSL (Secure Sockets).

Ensuite, analyser votre application pour :

- Comprendre précisément quelles chiffrement que vous effectuez et le chiffrement est fourni par les plateformes et les API que vous utilisez.
- Être certain que chaque utilisation au niveau de chaque couche d’un [algorithme de chiffrement en bloc](https://en.wikipedia.org/wiki/Block_cipher#Notable_block_ciphers), tel que AES et 3DES, en mode CBC incorporer l’utilisation d’une vérification de l’intégrité des données secret (une signature asymétrique, un code HMAC, ou pour modifier le mode de chiffrement pour un [authentifié chiffrement](https://en.wikipedia.org/wiki/Authenticated_encryption) mode (AE) comme GCM ou CCM).

En fonction de la recherche en cours, il est généralement considérée comme que lorsque les opérations de chiffrement et d’authentification sont effectuées indépendamment pour les modes non AE de chiffrement, l’authentification le texte chiffré (encrypt-then-sign) est la meilleure option générale. Toutefois, aucune réponse conséquente correct pour le chiffrement et cette généralisation n’est pas aussi bonne qualité que dirigée conseils à partir d’un cryptographe Professionnel.

Les applications qui ne peuvent pas modifier leur format de messagerie mais effectuer un déchiffrement CBC non authentifié sont invitées pour tenter d’intégrer les solutions d’atténuation tels que :

- Déchiffrer sans autoriser le déchiffreur vérifier ou supprimer des marges intérieures :
  - Tout remplissage a été appliqué doive toujours être supprimées ou ignorées, vous déplacez la charge dans votre application.
  - L’avantage est que la vérification de la marge intérieure et la suppression peuvent être incorporés dans une autre logique de vérification de données application. Si la vérification de la marge intérieure et la vérification des données peuvent être effectuées dans le temps, la menace est réduite.
  - Étant donné que l’interprétation de la marge intérieure change la longueur du message ne soit perçu, peut-être encore être émises à partir de cette approche des informations de minutage.
- Modifiez le mode de remplissage de déchiffrement ISO10126 :
  - Remplissage de déchiffrement ISO10126 est compatible avec remplissage PKCS7 et remplissage de chiffrement ANSIX923.
  - Modification du mode permet de réduire la base de connaissances oracle remplissage à 1 octet, au lieu de l’intégralité du bloc. Toutefois, si le contenu a un pied de page bien connu, par exemple un élément XML de fermeture attaques associées peuvent continuer attaquer le reste du message.
  - Cela n’également empêche la récupération en texte clair dans les situations où la personne malveillante peut forcer le même texte en clair pour être chiffré plusieurs fois avec un décalage de message différent.
- Portail de l’évaluation d’un appel de déchiffrement à mouiller le signal de synchronisation :
  - Le calcul du temps d’attente doit avoir un minimum dépassant la quantité maximale de temps que l’opération de déchiffrement faudrait pour n’importe quel segment de données qui contient le remplissage.
  - Calculs de temps doivent être effectuées selon les instructions de [lors de l’acquisition des horodatages haute résolution](https://msdn.microsoft.com/library/windows/desktop/dn55340.aspx), ne pas à l’aide de <xref:System.Environment.TickCount?displayProperty=nameWithType> (sujet à la restauration sur/dépassement) ou la soustraction de deux horodatages système (susceptibles d’être modifiés de NTP erreurs).
  - Calculs de temps doivent être qui inclut l’opération de déchiffrement, y compris toutes les exceptions éventuelles dans géré ou des applications C++, pas seulement complétées à la fin.
  - Si la réussite ou l’échec a encore été déterminé, la porte de la minuterie doit renvoient une erreur lors de son expiration.
- Les services qui exécutent le déchiffrement non authentifié doivent avoir en place pour détecter qu’un flux excessif de messages « non valides » n’a rien par le biais du contrôle.
  - N’oubliez pas que ce signal comporte des faux positifs (données en toute légitimité endommagées) et des faux négatifs (propagation de l’attaque sur une période suffisamment longue pour échapper à la détection).

## <a name="finding-vulnerable-code---native-applications"></a>Recherche de code vulnérable - applications natives

Pour les programmes basés sur la cryptographie Windows : bibliothèque de génération (CNG) :

- L’appel de déchiffrement concerne [BCryptDecrypt](https://msdn.microsoft.com/library/windows/desktop/aa375391.aspx), en spécifiant le `BCRYPT_BLOCK_PADDING` indicateur.
- Le handle de clé a été initialisé en appelant [BCryptSetProperty](https://msdn.microsoft.com/library/windows/desktop/aa375504.aspx) avec [BCRYPT_CHAINING_MODE](https://msdn.microsoft.com/library/windows/desktop/aa376211.aspx#BCRYPT_CHAINING_MODE) la valeur `BCRYPT_CHAIN_MODE_CBC`.
  - Étant donné que `BCRYPT_CHAIN_MODE_CBC` est la valeur par défaut, affectée code avez ne peut-être pas affecté la valeur de `BCRYPT_CHAINING_MODE`.

Pour les programmes basés sur l’API de chiffrement Windows plus anciens :

- L’appel de déchiffrement concerne [CryptDecrypt](https://msdn.microsoft.com/library/windows/desktop/aa379913.aspx) avec `Final=TRUE`.
- Le handle de clé a été initialisé en appelant [CryptSetKeyParam](https://msdn.microsoft.com/library/windows/desktop/aa380272.aspx) avec [KP_MODE](https://msdn.microsoft.com/library/windows/desktop/aa379949.aspx#KP_MODE) la valeur `CRYPT_MODE_CBC`.
  - Étant donné que `CRYPT_MODE_CBC` est la valeur par défaut, affectée code avez ne peut-être pas affecté la valeur de `KP_MODE`.

## <a name="finding-vulnerable-code---managed-applications"></a>Code vulnérable recherche - applications managées

- L’appel de déchiffrement concerne le <xref:System.Security.Cryptography.SymmetricAlgorithm.CreateDecryptor> ou <xref:System.Security.Cryptography.SymmetricAlgorithm.CreateDecryptor(System.Byte[],System.Byte[])> méthodes sur <xref:System.Security.Cryptography.SymmetricAlgorithm?displayProperty=nameWithType>.
  - Cela inclut les types dérivés suivants dans .NET, mais peut-être également inclure des types tiers :
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
- Le <xref:System.Security.Cryptography.SymmetricAlgorithm.Padding?displayProperty=nameWithType> a pris la valeur de propriété <xref:System.Security.Cryptography.PaddingMode.PKCS7?displayProperty=nameWithType>, <xref:System.Security.Cryptography.PaddingMode.ANSIX923?displayProperty=nameWithType>, ou <xref:System.Security.Cryptography.PaddingMode.ISO10126?displayProperty=nameWithType>.
  - Étant donné que <xref:System.Security.Cryptography.PaddingMode.PKCS7?displayProperty=nameWithType> est la valeur par défaut, affectée code ne peut jamais avoir affecté le <xref:System.Security.Cryptography.SymmetricAlgorithm.Padding?displayProperty=nameWithType> propriété.
- Le <xref:System.Security.Cryptography.SymmetricAlgorithm.Mode?displayProperty=nameWithType> a pris la valeur de propriété <xref:System.Security.Cryptography.CipherMode.CBC?displayProperty=nameWithType>
  - Étant donné que <xref:System.Security.Cryptography.CipherMode.CBC?displayProperty=nameWithType> est la valeur par défaut, affectée code ne peut jamais avoir affecté le <xref:System.Security.Cryptography.SymmetricAlgorithm.Mode?displayProperty=nameWithType> propriété.

## <a name="finding-vulnerable-code---cryptographic-message-syntax"></a>Recherche de code vulnérable - syntaxe de message

Un message CMS DonnéesEnveloppées non authentifié dont le contenu chiffré utilise le mode CBC AES (2.16.840.1.101.3.4.1.2, 2.16.840.1.101.3.4.1.22, 2.16.840.1.101.3.4.1.42), DES (1.3.14.3.2.7), 3DES (1.2.840.113549.3.7) ou RC2 (1.2.840.113549.3.2) est vulnérables, ainsi que des messages à l’aide de toutes les autres algorithmes de chiffrement par bloc en mode CBC.

Tandis que les chiffrements de flux ne sont pas sensibles à cette vulnérabilité, Microsoft vous recommande de toujours authentifier les données sur l’inspection de la valeur ContentEncryptionAlgorithm.

Pour les applications managées, un DonnéesEnveloppées CMS blob peut être détecté comme n’importe quelle valeur est passée à <xref:System.Security.Cryptography.Pkcs.EnvelopedCms.Decode(System.Byte[])?displayProperty=fullName>.

Pour les applications natives, un objet blob CMS DonnéesEnveloppées peut être détecté en tant que la valeur fournie pour un handle CMS via [CryptMsgUpdate](https://msdn.microsoft.com/library/windows/desktop/aa380231.aspx) dont résultant [CMSG_TYPE_PARAM](https://msdn.microsoft.com/library/windows/desktop/aa380227.aspx) est `CMSG_ENVELOPED` et/ou le handle CMS est envoyées ultérieurement un `CMSG_CTRL_DECRYPT` instruction via [CryptMsgControl](https://msdn.microsoft.com/library/windows/desktop/aa380220.aspx).

## <a name="vulnerable-code-example---managed"></a>Exemple de code vulnérable - géré

Cette méthode lit un cookie et la déchiffre et aucune vérification de l’intégrité des données n’est visible. Par conséquent, le contenu d’un cookie qui est lu par cette méthode peut être attaqué par l’utilisateur qui a reçu ou par un pirate a obtenu la valeur de cookie chiffré.

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

## <a name="example-code-following-recommended-practices---managed"></a>Exemple suivant de code pratiques - géré

L’exemple de code suivant utilise un format de message non standard de

`cipher_algorithm_id || hmac_algorithm_id || hmac_tag || iv || ciphertext`

où les `cipher_algorithm_id` et `hmac_algorithm_id` identificateurs d’algorithme sont des représentations de (non standard) local de l’application de ces algorithmes. Ces identificateurs peuvent être judicieuse dans d’autres parties de votre protocole de messagerie existant et non comme un flux d’octets concaténée nu.

Cet exemple utilise également une clé principale unique pour dériver une clé de chiffrement et une clé HMAC. Cela est dû à la fois pour des raisons pratiques permettant d’activer une application séparément indexés dans une application de clés en double et visant à encourager la conservation des valeurs d’autre que les deux clés. Plus, elle garantit que la clé HMAC et la clé de chiffrement ne peuvent pas tirer parti de synchronisation.

Cet exemple n’accepte pas un <xref:System.IO.Stream> pour le chiffrement ou le déchiffrement. Une étape du fait de format de données en cours chiffrer difficile, car le `hmac_tag` valeur précède le texte chiffré. Toutefois, ce format a été choisi car il conserve tous les éléments de taille fixe au début de conserver la plus simple de l’analyseur. Avec ce format de données, une seule passe decrypt est possible, si un implémenteur est indispensable pour appeler GetHashAndReset et avant d’appeler TransformFinalBlock de vérifier le résultat. Si le chiffrement de diffusion en continu est important, un autre mode AE peut être requis.

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
