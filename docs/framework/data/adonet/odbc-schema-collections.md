---
title: Collections de schémas ODBC
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: ffe80120ceffbe29c0a117cf1194860c5782be8c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772045"
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="4bdd5-102">Collections de schémas ODBC</span><span class="sxs-lookup"><span data-stu-id="4bdd5-102">ODBC Schema Collections</span></span>

<span data-ttu-id="4bdd5-103">Cette section traite de la prise en charge des collections de schémas pour les pilotes ODBC Microsoft SQL Server, Oracle et Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="4bdd5-103">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>

## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="4bdd5-104">Pilote Microsoft SQL Server ODBC</span><span class="sxs-lookup"><span data-stu-id="4bdd5-104">Microsoft SQL Server ODBC Driver</span></span>

<span data-ttu-id="4bdd5-105">Le pilote ODBC de Microsoft SQL Server prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="4bdd5-105">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>

- <span data-ttu-id="4bdd5-106">Tables</span><span class="sxs-lookup"><span data-stu-id="4bdd5-106">Tables</span></span>

- <span data-ttu-id="4bdd5-107">Index</span><span class="sxs-lookup"><span data-stu-id="4bdd5-107">Indexes</span></span>

- <span data-ttu-id="4bdd5-108">Colonnes</span><span class="sxs-lookup"><span data-stu-id="4bdd5-108">Columns</span></span>

- <span data-ttu-id="4bdd5-109">Procédures</span><span class="sxs-lookup"><span data-stu-id="4bdd5-109">Procedures</span></span>

- <span data-ttu-id="4bdd5-110">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="4bdd5-110">ProcedureColumns</span></span>

- <span data-ttu-id="4bdd5-111">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="4bdd5-111">ProcedureParameters</span></span>

- <span data-ttu-id="4bdd5-112">Affichages</span><span class="sxs-lookup"><span data-stu-id="4bdd5-112">Views</span></span>

### <a name="tables-and-views"></a><span data-ttu-id="4bdd5-113">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="4bdd5-113">Tables and Views</span></span>

|<span data-ttu-id="4bdd5-114">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-114">ColumnName</span></span>|<span data-ttu-id="4bdd5-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="4bdd5-115">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="4bdd5-116">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="4bdd5-116">TABLE_CAT</span></span>|<span data-ttu-id="4bdd5-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-117">String</span></span>|
|<span data-ttu-id="4bdd5-118">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="4bdd5-118">TABLE_SCHEM</span></span>|<span data-ttu-id="4bdd5-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-119">String</span></span>|
|<span data-ttu-id="4bdd5-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-120">TABLE_NAME</span></span>|<span data-ttu-id="4bdd5-121">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-121">String</span></span>|
|<span data-ttu-id="4bdd5-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-122">TABLE_TYPE</span></span>|<span data-ttu-id="4bdd5-123">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-123">String</span></span>|
|<span data-ttu-id="4bdd5-124">REMARKS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-124">REMARKS</span></span>|<span data-ttu-id="4bdd5-125">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-125">String</span></span>|

### <a name="indexes"></a><span data-ttu-id="4bdd5-126">Index</span><span class="sxs-lookup"><span data-stu-id="4bdd5-126">Indexes</span></span>

|<span data-ttu-id="4bdd5-127">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-127">ColumnName</span></span>|<span data-ttu-id="4bdd5-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="4bdd5-128">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="4bdd5-129">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="4bdd5-129">TABLE_CAT</span></span>|<span data-ttu-id="4bdd5-130">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-130">String</span></span>|
|<span data-ttu-id="4bdd5-131">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="4bdd5-131">TABLE_SCHEM</span></span>|<span data-ttu-id="4bdd5-132">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-132">String</span></span>|
|<span data-ttu-id="4bdd5-133">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-133">TABLE_NAME</span></span>|<span data-ttu-id="4bdd5-134">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-134">String</span></span>|
|<span data-ttu-id="4bdd5-135">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-135">NON_UNIQUE</span></span>|<span data-ttu-id="4bdd5-136">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-136">Int16</span></span>|
|<span data-ttu-id="4bdd5-137">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-137">INDEX_QUALIFIER</span></span>|<span data-ttu-id="4bdd5-138">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-138">String</span></span>|
|<span data-ttu-id="4bdd5-139">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-139">INDEX_NAME</span></span>|<span data-ttu-id="4bdd5-140">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-140">String</span></span>|
|<span data-ttu-id="4bdd5-141">TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-141">TYPE</span></span>|<span data-ttu-id="4bdd5-142">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-142">Int16</span></span>|
|<span data-ttu-id="4bdd5-143">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="4bdd5-143">ORDINAL_POSITION</span></span>|<span data-ttu-id="4bdd5-144">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-144">Int16</span></span>|
|<span data-ttu-id="4bdd5-145">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-145">COLUMN_NAME</span></span>|<span data-ttu-id="4bdd5-146">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-146">String</span></span>|
|<span data-ttu-id="4bdd5-147">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="4bdd5-147">ASC_OR_DESC</span></span>|<span data-ttu-id="4bdd5-148">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-148">String</span></span>|
|<span data-ttu-id="4bdd5-149">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="4bdd5-149">CARDINALITY</span></span>|<span data-ttu-id="4bdd5-150">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-150">Int32</span></span>|
|<span data-ttu-id="4bdd5-151">PAGES</span><span class="sxs-lookup"><span data-stu-id="4bdd5-151">PAGES</span></span>|<span data-ttu-id="4bdd5-152">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-152">Int32</span></span>|
|<span data-ttu-id="4bdd5-153">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="4bdd5-153">FILTER_CONDITION</span></span>|<span data-ttu-id="4bdd5-154">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-154">String</span></span>|
|<span data-ttu-id="4bdd5-155">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4bdd5-155">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="4bdd5-156">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-156">String</span></span>|
|<span data-ttu-id="4bdd5-157">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-157">SS_DATA_TYPE</span></span>|<span data-ttu-id="4bdd5-158">Byte</span><span class="sxs-lookup"><span data-stu-id="4bdd5-158">Byte</span></span>|

### <a name="columns"></a><span data-ttu-id="4bdd5-159">Colonnes</span><span class="sxs-lookup"><span data-stu-id="4bdd5-159">Columns</span></span>

|<span data-ttu-id="4bdd5-160">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-160">ColumnName</span></span>|<span data-ttu-id="4bdd5-161">Type de données</span><span class="sxs-lookup"><span data-stu-id="4bdd5-161">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="4bdd5-162">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="4bdd5-162">TABLE_CAT</span></span>|<span data-ttu-id="4bdd5-163">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-163">String</span></span>|
|<span data-ttu-id="4bdd5-164">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="4bdd5-164">TABLE_SCHEM</span></span>|<span data-ttu-id="4bdd5-165">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-165">String</span></span>|
|<span data-ttu-id="4bdd5-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-166">TABLE_NAME</span></span>|<span data-ttu-id="4bdd5-167">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-167">String</span></span>|
|<span data-ttu-id="4bdd5-168">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-168">COLUMN_NAME</span></span>|<span data-ttu-id="4bdd5-169">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-169">String</span></span>|
|<span data-ttu-id="4bdd5-170">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-170">DATA_TYPE</span></span>|<span data-ttu-id="4bdd5-171">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-171">Int16</span></span>|
|<span data-ttu-id="4bdd5-172">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-172">TYPE_NAME</span></span>|<span data-ttu-id="4bdd5-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-173">String</span></span>|
|<span data-ttu-id="4bdd5-174">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-174">COLUMN_SIZE</span></span>|<span data-ttu-id="4bdd5-175">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-175">Int32</span></span>|
|<span data-ttu-id="4bdd5-176">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="4bdd5-176">BUFFER_LENGTH</span></span>|<span data-ttu-id="4bdd5-177">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-177">Int32</span></span>|
|<span data-ttu-id="4bdd5-178">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-178">DECIMAL_DIGITS</span></span>|<span data-ttu-id="4bdd5-179">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-179">Int16</span></span>|
|<span data-ttu-id="4bdd5-180">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="4bdd5-180">NUM_PREC_RADIX</span></span>|<span data-ttu-id="4bdd5-181">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-181">Int16</span></span>|
|<span data-ttu-id="4bdd5-182">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-182">NULLABLE</span></span>|<span data-ttu-id="4bdd5-183">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-183">Int16</span></span>|
|<span data-ttu-id="4bdd5-184">REMARKS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-184">REMARKS</span></span>|<span data-ttu-id="4bdd5-185">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-185">String</span></span>|
|<span data-ttu-id="4bdd5-186">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="4bdd5-186">COLUMN_DEF</span></span>|<span data-ttu-id="4bdd5-187">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-187">String</span></span>|
|<span data-ttu-id="4bdd5-188">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-188">SQL_DATA_TYPE</span></span>|<span data-ttu-id="4bdd5-189">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-189">Int16</span></span>|
|<span data-ttu-id="4bdd5-190">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="4bdd5-190">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="4bdd5-191">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-191">Int16</span></span>|
|<span data-ttu-id="4bdd5-192">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="4bdd5-192">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="4bdd5-193">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-193">Int32</span></span>|
|<span data-ttu-id="4bdd5-194">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="4bdd5-194">ORDINAL_POSITION</span></span>|<span data-ttu-id="4bdd5-195">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-195">Int32</span></span>|
|<span data-ttu-id="4bdd5-196">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-196">IS_NULLABLE</span></span>|<span data-ttu-id="4bdd5-197">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-197">String</span></span>|
|<span data-ttu-id="4bdd5-198">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4bdd5-198">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="4bdd5-199">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-199">String</span></span>|
|<span data-ttu-id="4bdd5-200">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4bdd5-200">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="4bdd5-201">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-201">String</span></span>|
|<span data-ttu-id="4bdd5-202">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-202">SS_DATA_TYPE</span></span>|<span data-ttu-id="4bdd5-203">Byte</span><span class="sxs-lookup"><span data-stu-id="4bdd5-203">Byte</span></span>|

### <a name="procedures"></a><span data-ttu-id="4bdd5-204">Procédures</span><span class="sxs-lookup"><span data-stu-id="4bdd5-204">Procedures</span></span>

|<span data-ttu-id="4bdd5-205">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-205">ColumnName</span></span>|<span data-ttu-id="4bdd5-206">Type de données</span><span class="sxs-lookup"><span data-stu-id="4bdd5-206">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="4bdd5-207">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="4bdd5-207">PROCEDURE_CAT</span></span>|<span data-ttu-id="4bdd5-208">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-208">String</span></span>|
|<span data-ttu-id="4bdd5-209">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="4bdd5-209">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="4bdd5-210">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-210">String</span></span>|
|<span data-ttu-id="4bdd5-211">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-211">PROCEDURE_NAME</span></span>|<span data-ttu-id="4bdd5-212">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-212">String</span></span>|
|<span data-ttu-id="4bdd5-213">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-213">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="4bdd5-214">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-214">Int32</span></span>|
|<span data-ttu-id="4bdd5-215">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-215">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="4bdd5-216">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-216">Int32</span></span>|
|<span data-ttu-id="4bdd5-217">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-217">NUM_RESULT_SETS</span></span>|<span data-ttu-id="4bdd5-218">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-218">Int32</span></span>|
|<span data-ttu-id="4bdd5-219">REMARKS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-219">REMARKS</span></span>|<span data-ttu-id="4bdd5-220">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-220">String</span></span>|
|<span data-ttu-id="4bdd5-221">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-221">PROCEDURE_TYPE</span></span>|<span data-ttu-id="4bdd5-222">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-222">Int16</span></span>|

### <a name="procedurecolumns"></a><span data-ttu-id="4bdd5-223">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="4bdd5-223">ProcedureColumns</span></span>

|<span data-ttu-id="4bdd5-224">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-224">ColumnName</span></span>|<span data-ttu-id="4bdd5-225">Type de données</span><span class="sxs-lookup"><span data-stu-id="4bdd5-225">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="4bdd5-226">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="4bdd5-226">PROCEDURE_CAT</span></span>|<span data-ttu-id="4bdd5-227">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-227">String</span></span>|
|<span data-ttu-id="4bdd5-228">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="4bdd5-228">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="4bdd5-229">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-229">String</span></span>|
|<span data-ttu-id="4bdd5-230">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-230">PROCEDURE_NAME</span></span>|<span data-ttu-id="4bdd5-231">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-231">String</span></span>|
|<span data-ttu-id="4bdd5-232">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-232">COLUMN_NAME</span></span>|<span data-ttu-id="4bdd5-233">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-233">String</span></span>|
|<span data-ttu-id="4bdd5-234">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-234">COLUMN_TYPE</span></span>|<span data-ttu-id="4bdd5-235">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-235">Int16</span></span>|
|<span data-ttu-id="4bdd5-236">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-236">DATA_TYPE</span></span>|<span data-ttu-id="4bdd5-237">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-237">Int16</span></span>|
|<span data-ttu-id="4bdd5-238">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-238">TYPE_NAME</span></span>|<span data-ttu-id="4bdd5-239">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-239">String</span></span>|
|<span data-ttu-id="4bdd5-240">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-240">COLUMN_SIZE</span></span>|<span data-ttu-id="4bdd5-241">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-241">Int32</span></span>|
|<span data-ttu-id="4bdd5-242">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="4bdd5-242">BUFFER_LENGTH</span></span>|<span data-ttu-id="4bdd5-243">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-243">Int32</span></span>|
|<span data-ttu-id="4bdd5-244">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-244">DECIMAL_DIGITS</span></span>|<span data-ttu-id="4bdd5-245">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-245">Int16</span></span>|
|<span data-ttu-id="4bdd5-246">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="4bdd5-246">NUM_PREC_RADIX</span></span>|<span data-ttu-id="4bdd5-247">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-247">Int16</span></span>|
|<span data-ttu-id="4bdd5-248">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-248">NULLABLE</span></span>|<span data-ttu-id="4bdd5-249">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-249">Int16</span></span>|
|<span data-ttu-id="4bdd5-250">REMARKS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-250">REMARKS</span></span>|<span data-ttu-id="4bdd5-251">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-251">String</span></span>|
|<span data-ttu-id="4bdd5-252">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="4bdd5-252">COLUMN_DEF</span></span>|<span data-ttu-id="4bdd5-253">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-253">String</span></span>|
|<span data-ttu-id="4bdd5-254">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-254">SQL_DATA_TYPE</span></span>|<span data-ttu-id="4bdd5-255">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-255">Int16</span></span>|
|<span data-ttu-id="4bdd5-256">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="4bdd5-256">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="4bdd5-257">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-257">Int16</span></span>|
|<span data-ttu-id="4bdd5-258">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="4bdd5-258">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="4bdd5-259">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-259">Int32</span></span>|
|<span data-ttu-id="4bdd5-260">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="4bdd5-260">ORDINAL_POSITION</span></span>|<span data-ttu-id="4bdd5-261">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-261">Int32</span></span>|
|<span data-ttu-id="4bdd5-262">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-262">IS_NULLABLE</span></span>|<span data-ttu-id="4bdd5-263">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-263">String</span></span>|
|<span data-ttu-id="4bdd5-264">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4bdd5-264">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="4bdd5-265">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-265">String</span></span>|
|<span data-ttu-id="4bdd5-266">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4bdd5-266">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="4bdd5-267">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-267">String</span></span>|
|<span data-ttu-id="4bdd5-268">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-268">SS_DATA_TYPE</span></span>|<span data-ttu-id="4bdd5-269">Byte</span><span class="sxs-lookup"><span data-stu-id="4bdd5-269">Byte</span></span>|

### <a name="procedureparameters"></a><span data-ttu-id="4bdd5-270">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="4bdd5-270">ProcedureParameters</span></span>

|<span data-ttu-id="4bdd5-271">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-271">ColumnName</span></span>|<span data-ttu-id="4bdd5-272">Type de données</span><span class="sxs-lookup"><span data-stu-id="4bdd5-272">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="4bdd5-273">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="4bdd5-273">PROCEDURE_CAT</span></span>|<span data-ttu-id="4bdd5-274">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-274">String</span></span>|
|<span data-ttu-id="4bdd5-275">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="4bdd5-275">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="4bdd5-276">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-276">String</span></span>|
|<span data-ttu-id="4bdd5-277">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-277">PROCEDURE_NAME</span></span>|<span data-ttu-id="4bdd5-278">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-278">String</span></span>|
|<span data-ttu-id="4bdd5-279">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-279">COLUMN_NAME</span></span>|<span data-ttu-id="4bdd5-280">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-280">String</span></span>|
|<span data-ttu-id="4bdd5-281">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-281">COLUMN_TYPE</span></span>|<span data-ttu-id="4bdd5-282">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-282">Int16</span></span>|
|<span data-ttu-id="4bdd5-283">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-283">DATA_TYPE</span></span>|<span data-ttu-id="4bdd5-284">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-284">Int16</span></span>|
|<span data-ttu-id="4bdd5-285">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-285">TYPE_NAME</span></span>|<span data-ttu-id="4bdd5-286">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-286">String</span></span>|
|<span data-ttu-id="4bdd5-287">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-287">COLUMN_SIZE</span></span>|<span data-ttu-id="4bdd5-288">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-288">Int32</span></span>|
|<span data-ttu-id="4bdd5-289">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="4bdd5-289">BUFFER_LENGTH</span></span>|<span data-ttu-id="4bdd5-290">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-290">Int32</span></span>|
|<span data-ttu-id="4bdd5-291">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-291">DECIMAL_DIGITS</span></span>|<span data-ttu-id="4bdd5-292">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-292">Int16</span></span>|
|<span data-ttu-id="4bdd5-293">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="4bdd5-293">NUM_PREC_RADIX</span></span>|<span data-ttu-id="4bdd5-294">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-294">Int16</span></span>|
|<span data-ttu-id="4bdd5-295">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-295">NULLABLE</span></span>|<span data-ttu-id="4bdd5-296">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-296">Int16</span></span>|
|<span data-ttu-id="4bdd5-297">REMARKS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-297">REMARKS</span></span>|<span data-ttu-id="4bdd5-298">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-298">String</span></span>|
|<span data-ttu-id="4bdd5-299">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="4bdd5-299">COLUMN_DEF</span></span>|<span data-ttu-id="4bdd5-300">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-300">String</span></span>|
|<span data-ttu-id="4bdd5-301">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-301">SQL_DATA_TYPE</span></span>|<span data-ttu-id="4bdd5-302">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-302">Int16</span></span>|
|<span data-ttu-id="4bdd5-303">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="4bdd5-303">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="4bdd5-304">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-304">Int16</span></span>|
|<span data-ttu-id="4bdd5-305">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="4bdd5-305">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="4bdd5-306">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-306">Int32</span></span>|
|<span data-ttu-id="4bdd5-307">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="4bdd5-307">ORDINAL_POSITION</span></span>|<span data-ttu-id="4bdd5-308">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-308">Int32</span></span>|
|<span data-ttu-id="4bdd5-309">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-309">IS_NULLABLE</span></span>|<span data-ttu-id="4bdd5-310">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-310">String</span></span>|
|<span data-ttu-id="4bdd5-311">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4bdd5-311">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="4bdd5-312">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-312">String</span></span>|
|<span data-ttu-id="4bdd5-313">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4bdd5-313">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="4bdd5-314">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-314">String</span></span>|
|<span data-ttu-id="4bdd5-315">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-315">SS_DATA_TYPE</span></span>|<span data-ttu-id="4bdd5-316">Byte</span><span class="sxs-lookup"><span data-stu-id="4bdd5-316">Byte</span></span>|

## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="4bdd5-317">Pilote Microsoft Oracle ODBC</span><span class="sxs-lookup"><span data-stu-id="4bdd5-317">Microsoft Oracle ODBC Driver</span></span>

<span data-ttu-id="4bdd5-318">Le pilote Microsoft SQL Server Oracle ODBC prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="4bdd5-318">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>

- <span data-ttu-id="4bdd5-319">Tables</span><span class="sxs-lookup"><span data-stu-id="4bdd5-319">Tables</span></span>

- <span data-ttu-id="4bdd5-320">Colonnes</span><span class="sxs-lookup"><span data-stu-id="4bdd5-320">Columns</span></span>

- <span data-ttu-id="4bdd5-321">Procédures</span><span class="sxs-lookup"><span data-stu-id="4bdd5-321">Procedures</span></span>

- <span data-ttu-id="4bdd5-322">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="4bdd5-322">ProcedureColumns</span></span>

- <span data-ttu-id="4bdd5-323">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="4bdd5-323">ProcedureParameters</span></span>

- <span data-ttu-id="4bdd5-324">Affichages</span><span class="sxs-lookup"><span data-stu-id="4bdd5-324">Views</span></span>

- <span data-ttu-id="4bdd5-325">Index</span><span class="sxs-lookup"><span data-stu-id="4bdd5-325">Indexes</span></span>

### <a name="tables-and-views"></a><span data-ttu-id="4bdd5-326">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="4bdd5-326">Tables and Views</span></span>

|<span data-ttu-id="4bdd5-327">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-327">ColumnName</span></span>|<span data-ttu-id="4bdd5-328">Type de données</span><span class="sxs-lookup"><span data-stu-id="4bdd5-328">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="4bdd5-329">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-329">TABLE_QUALIFIER</span></span>|<span data-ttu-id="4bdd5-330">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-330">String</span></span>|
|<span data-ttu-id="4bdd5-331">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-331">TABLE_OWNER</span></span>|<span data-ttu-id="4bdd5-332">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-332">String</span></span>|
|<span data-ttu-id="4bdd5-333">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-333">TABLE_NAME</span></span>|<span data-ttu-id="4bdd5-334">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-334">String</span></span>|
|<span data-ttu-id="4bdd5-335">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-335">TABLE_TYPE</span></span>|<span data-ttu-id="4bdd5-336">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-336">String</span></span>|
|<span data-ttu-id="4bdd5-337">REMARKS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-337">REMARKS</span></span>|<span data-ttu-id="4bdd5-338">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-338">String</span></span>|

### <a name="columns"></a><span data-ttu-id="4bdd5-339">Colonnes</span><span class="sxs-lookup"><span data-stu-id="4bdd5-339">Columns</span></span>

|<span data-ttu-id="4bdd5-340">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-340">ColumnName</span></span>|<span data-ttu-id="4bdd5-341">Type de données</span><span class="sxs-lookup"><span data-stu-id="4bdd5-341">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="4bdd5-342">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-342">TABLE_QUALIFIER</span></span>|<span data-ttu-id="4bdd5-343">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-343">String</span></span>|
|<span data-ttu-id="4bdd5-344">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-344">TABLE_OWNER</span></span>|<span data-ttu-id="4bdd5-345">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-345">String</span></span>|
|<span data-ttu-id="4bdd5-346">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-346">TABLE_NAME</span></span>|<span data-ttu-id="4bdd5-347">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-347">String</span></span>|
|<span data-ttu-id="4bdd5-348">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-348">COLUMN_NAME</span></span>|<span data-ttu-id="4bdd5-349">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-349">String</span></span>|
|<span data-ttu-id="4bdd5-350">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-350">DATA_TYPE</span></span>|<span data-ttu-id="4bdd5-351">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-351">Int16</span></span>|
|<span data-ttu-id="4bdd5-352">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-352">TYPE_NAME</span></span>|<span data-ttu-id="4bdd5-353">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-353">String</span></span>|
|<span data-ttu-id="4bdd5-354">PRECISION</span><span class="sxs-lookup"><span data-stu-id="4bdd5-354">PRECISION</span></span>|<span data-ttu-id="4bdd5-355">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-355">Int32</span></span>|
|<span data-ttu-id="4bdd5-356">LENGTH</span><span class="sxs-lookup"><span data-stu-id="4bdd5-356">LENGTH</span></span>|<span data-ttu-id="4bdd5-357">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-357">Int32</span></span>|
|<span data-ttu-id="4bdd5-358">SCALE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-358">SCALE</span></span>|<span data-ttu-id="4bdd5-359">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-359">Int16</span></span>|
|<span data-ttu-id="4bdd5-360">RADIX</span><span class="sxs-lookup"><span data-stu-id="4bdd5-360">RADIX</span></span>|<span data-ttu-id="4bdd5-361">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-361">Int16</span></span>|
|<span data-ttu-id="4bdd5-362">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-362">NULLABLE</span></span>|<span data-ttu-id="4bdd5-363">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-363">Int16</span></span>|
|<span data-ttu-id="4bdd5-364">REMARKS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-364">REMARKS</span></span>|<span data-ttu-id="4bdd5-365">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-365">String</span></span>|
|<span data-ttu-id="4bdd5-366">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="4bdd5-366">ORDINAL_POSITION</span></span>|<span data-ttu-id="4bdd5-367">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-367">Int32</span></span>|

### <a name="procedures"></a><span data-ttu-id="4bdd5-368">Procédures</span><span class="sxs-lookup"><span data-stu-id="4bdd5-368">Procedures</span></span>

|<span data-ttu-id="4bdd5-369">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-369">ColumnName</span></span>|<span data-ttu-id="4bdd5-370">Type de données</span><span class="sxs-lookup"><span data-stu-id="4bdd5-370">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="4bdd5-371">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-371">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="4bdd5-372">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-372">String</span></span>|
|<span data-ttu-id="4bdd5-373">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-373">PROCEDURE_OWNER</span></span>|<span data-ttu-id="4bdd5-374">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-374">String</span></span>|
|<span data-ttu-id="4bdd5-375">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-375">PROCEDURE_NAME</span></span>|<span data-ttu-id="4bdd5-376">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-376">String</span></span>|
|<span data-ttu-id="4bdd5-377">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-377">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="4bdd5-378">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-378">Int16</span></span>|
|<span data-ttu-id="4bdd5-379">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-379">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="4bdd5-380">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-380">Int16</span></span>|
|<span data-ttu-id="4bdd5-381">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-381">NUM_RESULT_SETS</span></span>|<span data-ttu-id="4bdd5-382">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-382">Int16</span></span>|
|<span data-ttu-id="4bdd5-383">REMARKS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-383">REMARKS</span></span>|<span data-ttu-id="4bdd5-384">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-384">String</span></span>|
|<span data-ttu-id="4bdd5-385">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-385">PROCEDURE_TYPE</span></span>|<span data-ttu-id="4bdd5-386">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-386">Int16</span></span>|

### <a name="procedurecolumns"></a><span data-ttu-id="4bdd5-387">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="4bdd5-387">ProcedureColumns</span></span>

|<span data-ttu-id="4bdd5-388">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-388">ColumnName</span></span>|<span data-ttu-id="4bdd5-389">Type de données</span><span class="sxs-lookup"><span data-stu-id="4bdd5-389">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="4bdd5-390">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-390">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="4bdd5-391">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-391">String</span></span>|
|<span data-ttu-id="4bdd5-392">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-392">PROCEDURE_OWNER</span></span>|<span data-ttu-id="4bdd5-393">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-393">String</span></span>|
|<span data-ttu-id="4bdd5-394">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-394">PROCEDURE_NAME</span></span>|<span data-ttu-id="4bdd5-395">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-395">String</span></span>|
|<span data-ttu-id="4bdd5-396">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-396">COLUMN_NAME</span></span>|<span data-ttu-id="4bdd5-397">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-397">String</span></span>|
|<span data-ttu-id="4bdd5-398">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-398">COLUMN_TYPE</span></span>|<span data-ttu-id="4bdd5-399">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-399">Int16</span></span>|
|<span data-ttu-id="4bdd5-400">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-400">DATA_TYPE</span></span>|<span data-ttu-id="4bdd5-401">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-401">Int16</span></span>|
|<span data-ttu-id="4bdd5-402">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-402">TYPE_NAME</span></span>|<span data-ttu-id="4bdd5-403">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-403">String</span></span>|
|<span data-ttu-id="4bdd5-404">PRECISION</span><span class="sxs-lookup"><span data-stu-id="4bdd5-404">PRECISION</span></span>|<span data-ttu-id="4bdd5-405">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-405">Int32</span></span>|
|<span data-ttu-id="4bdd5-406">LENGTH</span><span class="sxs-lookup"><span data-stu-id="4bdd5-406">LENGTH</span></span>|<span data-ttu-id="4bdd5-407">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-407">Int32</span></span>|
|<span data-ttu-id="4bdd5-408">SCALE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-408">SCALE</span></span>|<span data-ttu-id="4bdd5-409">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-409">Int16</span></span>|
|<span data-ttu-id="4bdd5-410">RADIX</span><span class="sxs-lookup"><span data-stu-id="4bdd5-410">RADIX</span></span>|<span data-ttu-id="4bdd5-411">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-411">Int16</span></span>|
|<span data-ttu-id="4bdd5-412">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-412">NULLABLE</span></span>|<span data-ttu-id="4bdd5-413">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-413">Int16</span></span>|
|<span data-ttu-id="4bdd5-414">REMARKS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-414">REMARKS</span></span>|<span data-ttu-id="4bdd5-415">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-415">String</span></span>|
|<span data-ttu-id="4bdd5-416">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="4bdd5-416">OVERLOAD</span></span>|<span data-ttu-id="4bdd5-417">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-417">Int32</span></span>|
|<span data-ttu-id="4bdd5-418">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="4bdd5-418">ORDINAL_POSITION</span></span>|<span data-ttu-id="4bdd5-419">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-419">Int32</span></span>|

## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="4bdd5-420">Pilote Microsoft Jet ODBC</span><span class="sxs-lookup"><span data-stu-id="4bdd5-420">Microsoft Jet ODBC Driver</span></span>

<span data-ttu-id="4bdd5-421">Le pilote Microsoft Jet ODBC prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="4bdd5-421">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>

- <span data-ttu-id="4bdd5-422">Tables</span><span class="sxs-lookup"><span data-stu-id="4bdd5-422">Tables</span></span>

- <span data-ttu-id="4bdd5-423">Index</span><span class="sxs-lookup"><span data-stu-id="4bdd5-423">Indexes</span></span>

- <span data-ttu-id="4bdd5-424">Colonnes</span><span class="sxs-lookup"><span data-stu-id="4bdd5-424">Columns</span></span>

- <span data-ttu-id="4bdd5-425">Procédures</span><span class="sxs-lookup"><span data-stu-id="4bdd5-425">Procedures</span></span>

- <span data-ttu-id="4bdd5-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="4bdd5-426">ProcedureColumns</span></span>

- <span data-ttu-id="4bdd5-427">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="4bdd5-427">ProcedureParameters</span></span>

- <span data-ttu-id="4bdd5-428">Affichages</span><span class="sxs-lookup"><span data-stu-id="4bdd5-428">Views</span></span>

### <a name="tables-and-views"></a><span data-ttu-id="4bdd5-429">Tables et vues</span><span class="sxs-lookup"><span data-stu-id="4bdd5-429">Tables and Views</span></span>

|<span data-ttu-id="4bdd5-430">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-430">ColumnName</span></span>|<span data-ttu-id="4bdd5-431">Type de données</span><span class="sxs-lookup"><span data-stu-id="4bdd5-431">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="4bdd5-432">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-432">TABLE_QUALIFIER</span></span>|<span data-ttu-id="4bdd5-433">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-433">String</span></span>|
|<span data-ttu-id="4bdd5-434">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-434">TABLE_OWNER</span></span>|<span data-ttu-id="4bdd5-435">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-435">String</span></span>|
|<span data-ttu-id="4bdd5-436">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-436">TABLE_NAME</span></span>|<span data-ttu-id="4bdd5-437">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-437">String</span></span>|
|<span data-ttu-id="4bdd5-438">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-438">TABLE_TYPE</span></span>|<span data-ttu-id="4bdd5-439">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-439">String</span></span>|
|<span data-ttu-id="4bdd5-440">REMARKS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-440">REMARKS</span></span>|<span data-ttu-id="4bdd5-441">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-441">String</span></span>|

### <a name="columns"></a><span data-ttu-id="4bdd5-442">Colonnes</span><span class="sxs-lookup"><span data-stu-id="4bdd5-442">Columns</span></span>

|<span data-ttu-id="4bdd5-443">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-443">ColumnName</span></span>|<span data-ttu-id="4bdd5-444">Type de données</span><span class="sxs-lookup"><span data-stu-id="4bdd5-444">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="4bdd5-445">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-445">TABLE_QUALIFIER</span></span>|<span data-ttu-id="4bdd5-446">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-446">String</span></span>|
|<span data-ttu-id="4bdd5-447">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-447">TABLE_OWNER</span></span>|<span data-ttu-id="4bdd5-448">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-448">String</span></span>|
|<span data-ttu-id="4bdd5-449">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-449">TABLE_NAME</span></span>|<span data-ttu-id="4bdd5-450">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-450">String</span></span>|
|<span data-ttu-id="4bdd5-451">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-451">COLUMN_NAME</span></span>|<span data-ttu-id="4bdd5-452">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-452">String</span></span>|
|<span data-ttu-id="4bdd5-453">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-453">DATA_TYPE</span></span>|<span data-ttu-id="4bdd5-454">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-454">Int16</span></span>|
|<span data-ttu-id="4bdd5-455">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-455">TYPE_NAME</span></span>|<span data-ttu-id="4bdd5-456">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-456">String</span></span>|
|<span data-ttu-id="4bdd5-457">PRECISION</span><span class="sxs-lookup"><span data-stu-id="4bdd5-457">PRECISION</span></span>|<span data-ttu-id="4bdd5-458">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-458">Int32</span></span>|
|<span data-ttu-id="4bdd5-459">LENGTH</span><span class="sxs-lookup"><span data-stu-id="4bdd5-459">LENGTH</span></span>|<span data-ttu-id="4bdd5-460">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-460">Int32</span></span>|
|<span data-ttu-id="4bdd5-461">SCALE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-461">SCALE</span></span>|<span data-ttu-id="4bdd5-462">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-462">Int16</span></span>|
|<span data-ttu-id="4bdd5-463">RADIX</span><span class="sxs-lookup"><span data-stu-id="4bdd5-463">RADIX</span></span>|<span data-ttu-id="4bdd5-464">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-464">Int16</span></span>|
|<span data-ttu-id="4bdd5-465">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-465">NULLABLE</span></span>|<span data-ttu-id="4bdd5-466">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-466">Int16</span></span>|
|<span data-ttu-id="4bdd5-467">REMARKS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-467">REMARKS</span></span>|<span data-ttu-id="4bdd5-468">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-468">String</span></span>|
|<span data-ttu-id="4bdd5-469">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="4bdd5-469">ORDINAL_POSITION</span></span>|<span data-ttu-id="4bdd5-470">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-470">Int32</span></span>|

### <a name="procedures"></a><span data-ttu-id="4bdd5-471">Procédures</span><span class="sxs-lookup"><span data-stu-id="4bdd5-471">Procedures</span></span>

|<span data-ttu-id="4bdd5-472">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-472">ColumnName</span></span>|<span data-ttu-id="4bdd5-473">Type de données</span><span class="sxs-lookup"><span data-stu-id="4bdd5-473">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="4bdd5-474">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-474">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="4bdd5-475">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-475">String</span></span>|
|<span data-ttu-id="4bdd5-476">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-476">PROCEDURE_OWNER</span></span>|<span data-ttu-id="4bdd5-477">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-477">String</span></span>|
|<span data-ttu-id="4bdd5-478">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-478">PROCEDURE_NAME</span></span>|<span data-ttu-id="4bdd5-479">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-479">String</span></span>|
|<span data-ttu-id="4bdd5-480">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-480">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="4bdd5-481">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-481">Int16</span></span>|
|<span data-ttu-id="4bdd5-482">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-482">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="4bdd5-483">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-483">Int16</span></span>|
|<span data-ttu-id="4bdd5-484">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-484">NUM_RESULT_SETS</span></span>|<span data-ttu-id="4bdd5-485">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-485">Int16</span></span>|
|<span data-ttu-id="4bdd5-486">REMARKS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-486">REMARKS</span></span>|<span data-ttu-id="4bdd5-487">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-487">String</span></span>|
|<span data-ttu-id="4bdd5-488">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-488">PROCEDURE_TYPE</span></span>|<span data-ttu-id="4bdd5-489">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-489">Int16</span></span>|

### <a name="procedurecolumns"></a><span data-ttu-id="4bdd5-490">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="4bdd5-490">ProcedureColumns</span></span>

|<span data-ttu-id="4bdd5-491">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-491">ColumnName</span></span>|<span data-ttu-id="4bdd5-492">Type de données</span><span class="sxs-lookup"><span data-stu-id="4bdd5-492">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="4bdd5-493">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-493">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="4bdd5-494">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-494">String</span></span>|
|<span data-ttu-id="4bdd5-495">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="4bdd5-495">PROCEDURE_OWNER</span></span>|<span data-ttu-id="4bdd5-496">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-496">String</span></span>|
|<span data-ttu-id="4bdd5-497">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-497">PROCEDURE_NAME</span></span>|<span data-ttu-id="4bdd5-498">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-498">String</span></span>|
|<span data-ttu-id="4bdd5-499">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-499">COLUMN_NAME</span></span>|<span data-ttu-id="4bdd5-500">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-500">String</span></span>|
|<span data-ttu-id="4bdd5-501">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-501">COLUMN_TYPE</span></span>|<span data-ttu-id="4bdd5-502">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-502">Int16</span></span>|
|<span data-ttu-id="4bdd5-503">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-503">DATA_TYPE</span></span>|<span data-ttu-id="4bdd5-504">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-504">Int16</span></span>|
|<span data-ttu-id="4bdd5-505">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-505">TYPE_NAME</span></span>|<span data-ttu-id="4bdd5-506">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-506">String</span></span>|
|<span data-ttu-id="4bdd5-507">PRECISION</span><span class="sxs-lookup"><span data-stu-id="4bdd5-507">PRECISION</span></span>|<span data-ttu-id="4bdd5-508">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-508">Int32</span></span>|
|<span data-ttu-id="4bdd5-509">LENGTH</span><span class="sxs-lookup"><span data-stu-id="4bdd5-509">LENGTH</span></span>|<span data-ttu-id="4bdd5-510">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-510">Int32</span></span>|
|<span data-ttu-id="4bdd5-511">SCALE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-511">SCALE</span></span>|<span data-ttu-id="4bdd5-512">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-512">Int16</span></span>|
|<span data-ttu-id="4bdd5-513">RADIX</span><span class="sxs-lookup"><span data-stu-id="4bdd5-513">RADIX</span></span>|<span data-ttu-id="4bdd5-514">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-514">Int16</span></span>|
|<span data-ttu-id="4bdd5-515">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-515">NULLABLE</span></span>|<span data-ttu-id="4bdd5-516">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-516">Int16</span></span>|
|<span data-ttu-id="4bdd5-517">REMARKS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-517">REMARKS</span></span>|<span data-ttu-id="4bdd5-518">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-518">String</span></span>|
|<span data-ttu-id="4bdd5-519">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="4bdd5-519">OVERLOAD</span></span>|<span data-ttu-id="4bdd5-520">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-520">Int32</span></span>|
|<span data-ttu-id="4bdd5-521">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="4bdd5-521">ORDINAL_POSITION</span></span>|<span data-ttu-id="4bdd5-522">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-522">Int32</span></span>|

### <a name="procedureparameters"></a><span data-ttu-id="4bdd5-523">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="4bdd5-523">ProcedureParameters</span></span>

|<span data-ttu-id="4bdd5-524">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-524">ColumnName</span></span>|<span data-ttu-id="4bdd5-525">Type de données</span><span class="sxs-lookup"><span data-stu-id="4bdd5-525">DataType</span></span>|
|----------------|--------------|
|<span data-ttu-id="4bdd5-526">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="4bdd5-526">PROCEDURE_CAT</span></span>|<span data-ttu-id="4bdd5-527">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-527">String</span></span>|
|<span data-ttu-id="4bdd5-528">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="4bdd5-528">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="4bdd5-529">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-529">String</span></span>|
|<span data-ttu-id="4bdd5-530">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-530">PROCEDURE_NAME</span></span>|<span data-ttu-id="4bdd5-531">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-531">String</span></span>|
|<span data-ttu-id="4bdd5-532">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-532">COLUMN_NAME</span></span>|<span data-ttu-id="4bdd5-533">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-533">String</span></span>|
|<span data-ttu-id="4bdd5-534">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-534">COLUMN_TYPE</span></span>|<span data-ttu-id="4bdd5-535">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-535">Int16</span></span>|
|<span data-ttu-id="4bdd5-536">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-536">DATA_TYPE</span></span>|<span data-ttu-id="4bdd5-537">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-537">Int16</span></span>|
|<span data-ttu-id="4bdd5-538">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="4bdd5-538">TYPE_NAME</span></span>|<span data-ttu-id="4bdd5-539">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-539">String</span></span>|
|<span data-ttu-id="4bdd5-540">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-540">COLUMN_SIZE</span></span>|<span data-ttu-id="4bdd5-541">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-541">Int32</span></span>|
|<span data-ttu-id="4bdd5-542">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="4bdd5-542">BUFFER_LENGTH</span></span>|<span data-ttu-id="4bdd5-543">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-543">Int32</span></span>|
|<span data-ttu-id="4bdd5-544">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-544">DECIMAL_DIGITS</span></span>|<span data-ttu-id="4bdd5-545">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-545">Int16</span></span>|
|<span data-ttu-id="4bdd5-546">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="4bdd5-546">NUM_PREC_RADIX</span></span>|<span data-ttu-id="4bdd5-547">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-547">Int16</span></span>|
|<span data-ttu-id="4bdd5-548">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-548">NULLABLE</span></span>|<span data-ttu-id="4bdd5-549">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-549">Int16</span></span>|
|<span data-ttu-id="4bdd5-550">REMARKS</span><span class="sxs-lookup"><span data-stu-id="4bdd5-550">REMARKS</span></span>|<span data-ttu-id="4bdd5-551">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-551">String</span></span>|
|<span data-ttu-id="4bdd5-552">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="4bdd5-552">COLUMN_DEF</span></span>|<span data-ttu-id="4bdd5-553">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-553">String</span></span>|
|<span data-ttu-id="4bdd5-554">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-554">SQL_DATA_TYPE</span></span>|<span data-ttu-id="4bdd5-555">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-555">Int16</span></span>|
|<span data-ttu-id="4bdd5-556">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="4bdd5-556">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="4bdd5-557">Int16</span><span class="sxs-lookup"><span data-stu-id="4bdd5-557">Int16</span></span>|
|<span data-ttu-id="4bdd5-558">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="4bdd5-558">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="4bdd5-559">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-559">Int32</span></span>|
|<span data-ttu-id="4bdd5-560">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="4bdd5-560">ORDINAL_POSITION</span></span>|<span data-ttu-id="4bdd5-561">Int32</span><span class="sxs-lookup"><span data-stu-id="4bdd5-561">Int32</span></span>|
|<span data-ttu-id="4bdd5-562">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="4bdd5-562">IS_NULLABLE</span></span>|<span data-ttu-id="4bdd5-563">Chaîne</span><span class="sxs-lookup"><span data-stu-id="4bdd5-563">String</span></span>|

## <a name="see-also"></a><span data-ttu-id="4bdd5-564">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bdd5-564">See also</span></span>

- [<span data-ttu-id="4bdd5-565">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="4bdd5-565">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
