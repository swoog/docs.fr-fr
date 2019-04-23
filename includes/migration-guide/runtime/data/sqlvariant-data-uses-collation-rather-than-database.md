---
ms.openlocfilehash: e7a5a95a5d13f3396d396ad0d74a19a0efa3a967
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235273"
---
### <a name="sqlvariant-data-uses-sqlvariant-collation-rather-than-database-collation"></a><span data-ttu-id="56041-101">Les données Sql_variant utilisent le classement sql_variant plutôt que le classement de la base de données</span><span class="sxs-lookup"><span data-stu-id="56041-101">Sql_variant data uses sql_variant collation rather than database collation</span></span>

|   |   |
|---|---|
|<span data-ttu-id="56041-102">Détails</span><span class="sxs-lookup"><span data-stu-id="56041-102">Details</span></span>|<code>sql_variant</code> <span data-ttu-id="56041-103">Les données utilisent le classement <code>sql_variant</code> plutôt que le classement de la base de données.</span><span class="sxs-lookup"><span data-stu-id="56041-103">data uses <code>sql_variant</code> collation rather than database collation.</span></span>|
|<span data-ttu-id="56041-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="56041-104">Suggestion</span></span>|<span data-ttu-id="56041-105">Cette modification permet de répondre à une éventuelle altération de données si le classement de la base de données est différent du classement <code>sql_variant</code>.</span><span class="sxs-lookup"><span data-stu-id="56041-105">This change addresses possible data corruption if the database collation differs from the <code>sql_variant</code> collation.</span></span> <span data-ttu-id="56041-106">Les applications qui s'appuient sur les données endommagées peuvent éventuellement échouer.</span><span class="sxs-lookup"><span data-stu-id="56041-106">Applications that rely on the corrupted data may experience failure.</span></span>|
|<span data-ttu-id="56041-107">Portée</span><span class="sxs-lookup"><span data-stu-id="56041-107">Scope</span></span>|<span data-ttu-id="56041-108">Transparent</span><span class="sxs-lookup"><span data-stu-id="56041-108">Transparent</span></span>|
|<span data-ttu-id="56041-109">Version</span><span class="sxs-lookup"><span data-stu-id="56041-109">Version</span></span>|<span data-ttu-id="56041-110">4.5</span><span class="sxs-lookup"><span data-stu-id="56041-110">4.5</span></span>|
|<span data-ttu-id="56041-111">Type</span><span class="sxs-lookup"><span data-stu-id="56041-111">Type</span></span>|<span data-ttu-id="56041-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="56041-112">Runtime</span></span>|
