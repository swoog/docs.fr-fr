---
title: Outil de recherche de clé privée (FindPrivateKey.exe)
ms.date: 09/11/2017
ms.assetid: b8846a95-3fcc-4e8c-b9c0-128d975a6307
ms.openlocfilehash: 8f156cbb2f4fad8d51e356bd4dee2d72d9397ffb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33498512"
---
# <a name="find-private-key-tool-findprivatekeyexe"></a><span data-ttu-id="52b14-102">Outil de recherche de clé privée (FindPrivateKey.exe)</span><span class="sxs-lookup"><span data-stu-id="52b14-102">Find Private Key Tool (FindPrivateKey.exe)</span></span>

<span data-ttu-id="52b14-103">Cet outil de ligne de commande peut être utilisé pour récupérer une clé privée provenant d'un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="52b14-103">This command-line tool can be used to retrieve a private key from a certificate store.</span></span> <span data-ttu-id="52b14-104">Par exemple, *FindPrivateKey.exe* peut être utilisé pour rechercher l’emplacement et le nom du fichier de clé privée associé à un certificat X.509 spécifique dans le magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="52b14-104">For example, *FindPrivateKey.exe* can be used to find the location and name of the private key file associated with a specific X.509 certificate in the certificate store.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52b14-105">L'outil FindPrivateKey est fourni à titre d'exemple WCF.</span><span class="sxs-lookup"><span data-stu-id="52b14-105">The FindPrivateKey tool is shipped as a WCF sample.</span></span> <span data-ttu-id="52b14-106">Pour plus d’informations sur où trouver l’exemple et comment le générer, consultez [FindPrivateKey](./samples/findprivatekey.md).</span><span class="sxs-lookup"><span data-stu-id="52b14-106">For more information about where to find the sample and how to build it, see [FindPrivateKey](./samples/findprivatekey.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="52b14-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52b14-107">Syntax</span></span>

```
FindPrivateKey<storeName> <storeLocation> [{ {-n <subjectName>} | {-t <thumbprint>} } [-f | -d | -a]]
```

## <a name="remarks"></a><span data-ttu-id="52b14-108">Notes</span><span class="sxs-lookup"><span data-stu-id="52b14-108">Remarks</span></span>

<span data-ttu-id="52b14-109">Les tables suivantes décrivent les arguments et les options qui peuvent être utilisés avec l’outil de recherche de clé privée Clé (FindPrivateKey.exe).</span><span class="sxs-lookup"><span data-stu-id="52b14-109">The following tables describe the arguments and the options that can be used with the Find Private Key tool (FindPrivateKey.exe).</span></span>

|<span data-ttu-id="52b14-110">Argument</span><span class="sxs-lookup"><span data-stu-id="52b14-110">Argument</span></span>|<span data-ttu-id="52b14-111">Description</span><span class="sxs-lookup"><span data-stu-id="52b14-111">Description</span></span>|
|--------------|-----------------|
|`storeName`|<span data-ttu-id="52b14-112">Nom du magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="52b14-112">Name of the certificate store.</span></span>|
|`storeLocation`|<span data-ttu-id="52b14-113">Emplacement du magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="52b14-113">The location of the certificate store.</span></span>|

|<span data-ttu-id="52b14-114">Option</span><span class="sxs-lookup"><span data-stu-id="52b14-114">Option</span></span>|<span data-ttu-id="52b14-115">Description</span><span class="sxs-lookup"><span data-stu-id="52b14-115">Description</span></span>|
|------------|-----------------|
|<span data-ttu-id="52b14-116">`/n <` *subjectName* `>`</span><span class="sxs-lookup"><span data-stu-id="52b14-116">`/n <` *subjectName* `>`</span></span>|<span data-ttu-id="52b14-117">Spécifie le nom du sujet du certificat.</span><span class="sxs-lookup"><span data-stu-id="52b14-117">Specifies the subject name of the certificate.</span></span>|
|<span data-ttu-id="52b14-118">`/t <` *empreinte numérique* `>`</span><span class="sxs-lookup"><span data-stu-id="52b14-118">`/t <` *thumbprint* `>`</span></span>|<span data-ttu-id="52b14-119">Spécifie l'empreinte numérique du certificat.</span><span class="sxs-lookup"><span data-stu-id="52b14-119">Specifies the thumbprint of the certificate.</span></span> <span data-ttu-id="52b14-120">Utilisez Certmgr.exe pour récupérer l'empreinte numérique du certificat.</span><span class="sxs-lookup"><span data-stu-id="52b14-120">Use Certmgr.exe to retrieve the thumbprint of the certificate.</span></span>|
|`/f`|<span data-ttu-id="52b14-121">Affiche le nom de fichier uniquement.</span><span class="sxs-lookup"><span data-stu-id="52b14-121">Outputs the file name only.</span></span>|
|`/d`|<span data-ttu-id="52b14-122">Affiche le répertoire uniquement.</span><span class="sxs-lookup"><span data-stu-id="52b14-122">Outputs the directory only.</span></span>|
|`/a`|<span data-ttu-id="52b14-123">Affiche le nom de fichier absolu.</span><span class="sxs-lookup"><span data-stu-id="52b14-123">Outputs the absolute file name.</span></span>|

## <a name="examples"></a><span data-ttu-id="52b14-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="52b14-124">Examples</span></span>

<span data-ttu-id="52b14-125">La commande suivante récupère la clé privée associée à John Doe :</span><span class="sxs-lookup"><span data-stu-id="52b14-125">The following command retrieves the private key for John Doe:</span></span>

```
FindPrivateKey My CurrentUser -n "CN=John Doe"
```

<span data-ttu-id="52b14-126">La commande suivante récupère la clé privée pour l’ordinateur local :</span><span class="sxs-lookup"><span data-stu-id="52b14-126">The following command retrieves the private key for the local machine:</span></span>

```
FindPrivateKey My LocalMachine -t "03 33 98 63 d0 47 e7 48 71 33 62 64 76 5c 4c 9d 42 1d 6b 52" –a
```