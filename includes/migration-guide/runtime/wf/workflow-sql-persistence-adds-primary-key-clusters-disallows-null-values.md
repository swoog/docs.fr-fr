---
ms.openlocfilehash: 9e98d3bca645cf82bf4fe99160dd096b0e274ef7
ms.sourcegitcommit: 0aca6c5d166d7961a1e354c248495645b97a1dc5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2019
ms.locfileid: "58760417"
---
### <a name="workflow-sql-persistence-adds-primary-key-clusters-and-disallows-null-values-in-some-columns"></a><span data-ttu-id="40946-101">La persistance des workflows SQL ajoute des clusters de clé primaire et interdit les valeurs null dans certaines colonnes</span><span class="sxs-lookup"><span data-stu-id="40946-101">Workflow SQL persistence adds primary key clusters and disallows null values in some columns</span></span>

|   |   |
|---|---|
|<span data-ttu-id="40946-102">Détails</span><span class="sxs-lookup"><span data-stu-id="40946-102">Details</span></span>|<span data-ttu-id="40946-103">À compter de .NET Framework 4.7, les tables créées pour le magasin d’instances de workflow SQL par le script SqlWorkflowInstanceStoreSchema.sql utilisent des clés primaires en cluster.</span><span class="sxs-lookup"><span data-stu-id="40946-103">Starting with the .NET Framework 4.7, the tables created for the SQL Workflow Instance Store (SWIS) by the SqlWorkflowInstanceStoreSchema.sql script use clustered primary keys.</span></span> <span data-ttu-id="40946-104">Pour cette raison, les identités ne prennent pas en charge les valeurs <code>null</code>.</span><span class="sxs-lookup"><span data-stu-id="40946-104">Because of this, identities do not support <code>null</code> values.</span></span> <span data-ttu-id="40946-105">Le fonctionnement du magasin d’instances de workflow SQL n’est pas impacté par ce changement.</span><span class="sxs-lookup"><span data-stu-id="40946-105">The operation of SWIS is not impacted by this change.</span></span> <span data-ttu-id="40946-106">Les mises à jour ont été apportées pour prendre en charge la réplication transactionnelle de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="40946-106">The updates were made to support SQL Server Transactional Replication.</span></span>|
|<span data-ttu-id="40946-107">Suggestion</span><span class="sxs-lookup"><span data-stu-id="40946-107">Suggestion</span></span>|<span data-ttu-id="40946-108">Le fichier SQL SqlWorkflowInstanceStoreSchemaUpgrade.sql doit être appliqué aux installations existantes pour bénéficier de ce changement.</span><span class="sxs-lookup"><span data-stu-id="40946-108">The SQL file SqlWorkflowInstanceStoreSchemaUpgrade.sql must be applied to existing installations in order to experience this change.</span></span> <span data-ttu-id="40946-109">Les nouvelles installations de base de données ont automatiquement ce changement.</span><span class="sxs-lookup"><span data-stu-id="40946-109">New database installations will automatically have the change.</span></span>|
|<span data-ttu-id="40946-110">Portée</span><span class="sxs-lookup"><span data-stu-id="40946-110">Scope</span></span>|<span data-ttu-id="40946-111">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="40946-111">Edge</span></span>|
|<span data-ttu-id="40946-112">Version</span><span class="sxs-lookup"><span data-stu-id="40946-112">Version</span></span>|<span data-ttu-id="40946-113">4.7</span><span class="sxs-lookup"><span data-stu-id="40946-113">4.7</span></span>|
|<span data-ttu-id="40946-114">Type</span><span class="sxs-lookup"><span data-stu-id="40946-114">Type</span></span>|<span data-ttu-id="40946-115">Runtime</span><span class="sxs-lookup"><span data-stu-id="40946-115">Runtime</span></span>|

