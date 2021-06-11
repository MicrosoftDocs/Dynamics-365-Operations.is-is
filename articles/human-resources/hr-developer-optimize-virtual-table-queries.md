---
title: Fínstilla Dataverse sýndartöflufyrirspurnir
description: Fínstilla og úrræðaleita afköst á fyrirspurnum um Dataverse sýndartöflur
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66fb9f2b50079b5eb4eb16da17b8a473d687d354
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054909"
---
# <a name="optimize-dataverse-virtual-table-queries"></a><span data-ttu-id="5d465-103">Fínstilla Dataverse sýndartöflufyrirspurnir</span><span class="sxs-lookup"><span data-stu-id="5d465-103">Optimize Dataverse virtual table queries</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="5d465-104">Úthreyfing</span><span class="sxs-lookup"><span data-stu-id="5d465-104">Issue</span></span>

### <a name="overview"></a><span data-ttu-id="5d465-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="5d465-105">Overview</span></span>

<span data-ttu-id="5d465-106">Þegar Dataverse sýndartöflur eru notaðar til að þróa samþættingar og aðrar gagnatengingar við Dynamics 365 Human Resources geta komið upp vandamál með afköst vegna fyrirspurna um sýndartöflurnar.</span><span class="sxs-lookup"><span data-stu-id="5d465-106">When using Dataverse virtual tables to develop integrations and other data connections with Dynamics 365 Human Resources, you can experience performance issues with queries against the virtual tables.</span></span> <span data-ttu-id="5d465-107">Hæg fyrirspurnarkeyrsla getur gerst í ýmsum biðlurum eða viðmótum.</span><span class="sxs-lookup"><span data-stu-id="5d465-107">The slow query execution can occur across various clients or interfaces.</span></span> <span data-ttu-id="5d465-108">Til dæmis gæti vandamálið komið upp við eftirfarandi aðstæður:</span><span class="sxs-lookup"><span data-stu-id="5d465-108">For example, you may experience the issue in the following circumstances:</span></span>

- <span data-ttu-id="5d465-109">Þegar spurst er fyrir um sýndartöflu í gegnum Dataverse vef API</span><span class="sxs-lookup"><span data-stu-id="5d465-109">When querying a virtual table through the Dataverse Web API</span></span>
- <span data-ttu-id="5d465-110">Þegar Power App er búið til gegn sýndartöflu</span><span class="sxs-lookup"><span data-stu-id="5d465-110">When creating a Power App against a virtual table</span></span>
- <span data-ttu-id="5d465-111">Þegar byggð er Power BI skýrsla í sýndartöflu</span><span class="sxs-lookup"><span data-stu-id="5d465-111">When building a Power BI report on a virtual table</span></span>

<span data-ttu-id="5d465-112">Vandamál með afköst geta komið upp í öllum þessum viðmótum.</span><span class="sxs-lookup"><span data-stu-id="5d465-112">All these interfaces have the potential to surface the performance issue.</span></span>

<span data-ttu-id="5d465-113">Ein orsök á hægum afköstum með Dataverse sýndartöflur fyrir Human Resources er dálkar framandlykla í sýndartöflunni sem tengist [skoðunareiginleikum](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) töflunnar.</span><span class="sxs-lookup"><span data-stu-id="5d465-113">One cause of slow performance with Dataverse virtual tables for Human Resources is the foreign key columns of the virtual table related to the table's [navigation properties](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span></span> <span data-ttu-id="5d465-114">Þegar skoðunareiginleikar eru búnir til fyrir sýndartöflu er dálki framandlykils sjálfkrafa bætt við töfluna til að sýna gildi lykilsins fyrir tengdan dálk lykils í sýndartöflunni.</span><span class="sxs-lookup"><span data-stu-id="5d465-114">When navigation properties are created for a virtual table, a foreign key column is automatically added to the table to represent the value of the key for the related virtual table's key column.</span></span> <span data-ttu-id="5d465-115">Til dæmis er **_mshr_fk_person_id_value** dálkinum bætt við **mshr_hcmworkerbaseentity** eininguna með framandlyklinum úr **mshr_dirpersonentity** einingunni.</span><span class="sxs-lookup"><span data-stu-id="5d465-115">For example, the **_mshr_fk_person_id_value** column is added to the **mshr_hcmworkerbaseentity** entity with the foreign key property from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="5d465-116">Vegna þess hvernig gildum fyrir þessa dálka framandlykla er viðhaldið í töflu, getur það að sækja gildin haft neikvæð áhrif á afköst fyrirspurnar um sýndartöfluna.</span><span class="sxs-lookup"><span data-stu-id="5d465-116">Because of how the values for these foreign key columns are maintained in a table, fetching the values can have a negative impact on the performance of a query against the virtual table.</span></span>

### <a name="potential-symptoms"></a><span data-ttu-id="5d465-117">Möguleg einkenni</span><span class="sxs-lookup"><span data-stu-id="5d465-117">Potential symptoms</span></span>

<span data-ttu-id="5d465-118">Dæmi þar sem þú gætir séð þessi áhrif er í fyrirspurnum gegn starfsmanninum (**mshr_hcmworkerentity**) eða einingu grunnstarfskrafts (**mshr_hcmworkerbaseentity**).</span><span class="sxs-lookup"><span data-stu-id="5d465-118">An example where you may see this impact is in queries against the Worker (**mshr_hcmworkerentity**) or Base worker (**mshr_hcmworkerbaseentity**) entity.</span></span> <span data-ttu-id="5d465-119">Frammistöðuvandamál gætu birtst á nokkra mismunandi vegu:</span><span class="sxs-lookup"><span data-stu-id="5d465-119">You may see the performance issue manifest itself in a few different ways:</span></span>

- <span data-ttu-id="5d465-120">**Hæg fyrirspurnarkeyrsla**: Fyrirspurn vegna sýndartöflu gæti skilað eðlilegum niðurstöðum en tekið lengri tíma en vanalega að ljúka keyrslu fyrirspurnarinnar.</span><span class="sxs-lookup"><span data-stu-id="5d465-120">**Slow query execution**: The query against the virtual table may return the expected results, but take longer than expected to complete execution of the query.</span></span>
- <span data-ttu-id="5d465-121">**Fyrirspurnin rann út á tíma**: Þessi fyrirspurn gæti runnið út á tíma og skilað eftirfarandi villu: „Náð var í merki til að kalla á Finance and Operations, en Finance and Operations skilaði villu af gerðinni InternalServerError.“</span><span class="sxs-lookup"><span data-stu-id="5d465-121">**Query timeout**: The query may time out and return the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type InternalServerError."</span></span>
- <span data-ttu-id="5d465-122">**Óvænt villa**: Fyrirspurnin gæti skilað villu af gerðinni 400 með eftirfarandi skilaboðum: „Óvænt villa kom upp.“</span><span class="sxs-lookup"><span data-stu-id="5d465-122">**Unexpected error**: The query may return an error type 400 with the following message: "An unexpected error occurred."</span></span>

  ![Villugerð 400 á HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType400.png)

- <span data-ttu-id="5d465-124">**Takmörkun**: Fyrirspurnin kann að ofnota tilföng netþjóns og orðið fyrir takmörkunum.</span><span class="sxs-lookup"><span data-stu-id="5d465-124">**Throttling**: The query may overuse server resources, and become subject to throttling.</span></span> <span data-ttu-id="5d465-125">Í slíku tilfelli skilar fyrirspurnin eftirfarandi villu: „Náð var í merki til að kalla á Finance and Operations, en Finance and Operations skilaði villu af gerðinni 429.“</span><span class="sxs-lookup"><span data-stu-id="5d465-125">In this case, the query returns the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type 429."</span></span> <span data-ttu-id="5d465-126">Frekari upplýsingar um takmörkun í Human Resources er að finna í [Algengar spurningar um takmörkun](./hr-admin-integration-throttling-faq.md).</span><span class="sxs-lookup"><span data-stu-id="5d465-126">For more information in throttling in Human Resources, see [Throttling FAQ](./hr-admin-integration-throttling-faq.md).</span></span>

  ![Villugerð 429 á HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a><span data-ttu-id="5d465-128">Upplausn</span><span class="sxs-lookup"><span data-stu-id="5d465-128">Resolution</span></span>

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a><span data-ttu-id="5d465-129">Takmarka dálkafjölda í gagnafyrirspurninni</span><span class="sxs-lookup"><span data-stu-id="5d465-129">Limit the number of columns included in your data query</span></span>

<span data-ttu-id="5d465-130">Með sýndartöflum er ein sú aðferð sem hefur mestan möguleika á að bæta afköst fyrirspurnar er að takmarka fjölda dálka sem valdir eru í fyrirspurninni.</span><span class="sxs-lookup"><span data-stu-id="5d465-130">With virtual tables, one of the methods with the greatest potential to improve query performance is to limit the number of columns selected in the query.</span></span> <span data-ttu-id="5d465-131">Almennar leiðbeiningar um fínstillingu á afköstum fyrirspurnar er að takmarka dálkana sem skilað er í fyrirspurninni niður í þá eiginleika sem á þarf að halda.</span><span class="sxs-lookup"><span data-stu-id="5d465-131">The general guidance for optimizing query performance is to limit the columns returned in your query to only those properties that you need.</span></span> <span data-ttu-id="5d465-132">Þetta á sérstaklega við um dálka framandlykla í sýndartöflum.</span><span class="sxs-lookup"><span data-stu-id="5d465-132">This is particularly true with the foreign key columns on virtual tables.</span></span> <span data-ttu-id="5d465-133">Ef þú þarft ekki gildin í dálkum framandlykla fyrir samþættinguna eða skýrsluna, þá skaltu skipuleggja fyrirspurnina þannig að hún velji aðeins dálkana sem á þarf að halda og sleppir dálkum framandlykla.</span><span class="sxs-lookup"><span data-stu-id="5d465-133">If you don't need the values in the foreign key columns for your integration or report, then structure the query to select only the columns you need, excluding the foreign key columns.</span></span>

#### <a name="selecting-columns-in-an-odata-query"></a><span data-ttu-id="5d465-134">Dálkar valdir í OData-fyrirspurn</span><span class="sxs-lookup"><span data-stu-id="5d465-134">Selecting columns in an OData query</span></span>

<span data-ttu-id="5d465-135">Þegar fyrirspurn er send á sýndartöflu í gegnum Dataverse vef API er hægt að takmarka fjölda dálka sem hafðir eru með í fyrirspurninni með því að nota valkostinn **$select** í kerfisfyrirspurn og skilgreina dálkana þar sem þarf að skila niðurstöðum.</span><span class="sxs-lookup"><span data-stu-id="5d465-135">When querying a virtual table through the Dataverse Web API, you can limit the number of columns included in the query by using the **$select** system query option, and define the columns for which you need results returned.</span></span> <span data-ttu-id="5d465-136">Til að hámarka árangur skaltu útiloka dálka framandlykla (þá með **_mshr_FK_** forskeytið) úr fyrirspurninni.</span><span class="sxs-lookup"><span data-stu-id="5d465-136">To maximize performance, exclude foreign key columns (those with the **_mshr_FK_** prefix) from the query.</span></span>

<span data-ttu-id="5d465-137">Til dæmis mun eftirfarandi fyrirspurn gagnvart einingunni **mshr_hcmworkerbaseentity** aðeins taka með dálkana sem hafðir eru með í fyrirspurnarmöguleika **$select**, þar sem gildum framandlykla er sleppt.</span><span class="sxs-lookup"><span data-stu-id="5d465-137">For example, the following query against the **mshr_hcmworkerbaseentity** entity will include only the columns included in the **$select** query option clause, excluding foreign key values.</span></span> <span data-ttu-id="5d465-138">Þetta gefur umtalsvert betri afköst í fyrirspurn sem tekur með alla dálka töflu.</span><span class="sxs-lookup"><span data-stu-id="5d465-138">This provides significant improvements in performance over a query that includes all table columns.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="5d465-139">Tillagan um að takmarka fjölda dálka sem eru valdir á einnig við þegar fyrirspurnarmöguleikinn **$expand** er notaður til að stækka fyrirspurnina yfir í tengdar sýndartöflur í gegnum skoðunareiginleika.</span><span class="sxs-lookup"><span data-stu-id="5d465-139">The recommendation to limit the number of columns selected also applies when using the **$expand** query option to expand the query to related virtual tables through navigation properties.</span></span> <span data-ttu-id="5d465-140">Eftirfarandi fyrirspurn inniheldur t.d. dálka úr einingunni **mshr_hcmworkerbaseentity** með stækkuðum dálkum úr einingunni **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="5d465-140">For example, the following query includes columns from the **mshr_hcmworkerbaseentity** entity with expanded columns from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="5d465-141">Athugið að fyrirspurnarmöguleikinn **$select** er einnig hafður með í fyrirspurnarmöguleikanum **$expand**.</span><span class="sxs-lookup"><span data-stu-id="5d465-141">Note that the **$select** query option is also included in the **$expand** query option clause.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="5d465-142">Þegar þessi aðferð er notuð til að sækja gögn með fyrirspurnarmöguleikanum **$select** í klausu fyrirspurnarmöguleikans **$expand** sjást yfirleitt enn betri afköst þegar skoðunareiginleikinn á milli eininganna er margt í eitt vensl.</span><span class="sxs-lookup"><span data-stu-id="5d465-142">When using this method of retrieving data with the **$select** query option in the **$expand** query option clause, you will typically see greater performance improvements when the navigation property between the entities is a many-to-one relationship.</span></span> <span data-ttu-id="5d465-143">Ekki er víst að þú sjáir sömu styttingu á tíma fyrirspurnarkeyrslu þegar eitt í margt vensl eru stækkuð.</span><span class="sxs-lookup"><span data-stu-id="5d465-143">You may not see the same decrease in query execution time when expanding a one-to-many relationship.</span></span> <span data-ttu-id="5d465-144">Frekari upplýsingar um skilgreiningu vensla fyrir Dataverse sýndartöflur er að finna í [Töfluvensl](/powerapps/maker/data-platform/create-edit-entity-relationships).</span><span class="sxs-lookup"><span data-stu-id="5d465-144">For more information on relationship definition for Dataverse virtual tables, see [Table relationships](/powerapps/maker/data-platform/create-edit-entity-relationships).</span></span>

<span data-ttu-id="5d465-145">Frekari upplýsingar um notkun á fyrirspurnarmöguleikum **$select** og **$expand** í kerfinum í Dataverse vef API er að finna í [Sækja tengdar færslueiningar með fyrirspurn](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span><span class="sxs-lookup"><span data-stu-id="5d465-145">For more information on using the **$select** and **$expand** system query options in the Dataverse Web API, see [Retrieve related entity records with a query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span></span>

#### <a name="selecting-columns-in-power-bi"></a><span data-ttu-id="5d465-146">Velja dálka í Power BI</span><span class="sxs-lookup"><span data-stu-id="5d465-146">Selecting columns in Power BI</span></span>

<span data-ttu-id="5d465-147">Ef þú finnur fyrir einhverjum af áðurnefndum vísbendingum um hæga keyrslu þegar Power BI skýrsla er sett saman gagnvart Dataverse sýndartöflu, er hægt að bæta afköstin með því að sleppa dálkum framandlykla úr dálkunum sem valdir eru úr töflunni fyrir skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="5d465-147">If you experience any of the aforementioned indications of slow performance when building a Power BI report against a Dataverse virtual table, you can improve the performance by excluding foreign key columns from the columns selected from the table for the report.</span></span> <span data-ttu-id="5d465-148">Til dæmis ef þú notar Power BI Desktop til að búa til skýrslu gagnvart einingunni **mshr_hcmworkerbaseentity**, geturðu notað eftirfarandi skref til að velja dálkana sem á að hafa með í skýrslufyrirspurninni.</span><span class="sxs-lookup"><span data-stu-id="5d465-148">For example, if you are using Power BI Desktop to create a report against the **mshr_hcmworkerbaseentity** entity, you can use the following steps to select the columns you want included in the report query.</span></span>

1. <span data-ttu-id="5d465-149">Í Power BI Desktop skal velja **Fleiri...** úr fellilistanum **Sækja gögn** á aðgerðarborðanum.</span><span class="sxs-lookup"><span data-stu-id="5d465-149">In Power BI Desktop, select **More...** from the **Get data** drop-down list on the action ribbon.</span></span>
2. <span data-ttu-id="5d465-150">Í glugganum **Sækja gögn** skal slá inn **Common Data Service** í leitarreitinn, velja **Common Data Service** tengilinn og velja **Tengja**.</span><span class="sxs-lookup"><span data-stu-id="5d465-150">In the **Get Data** window, enter **Common Data Service** in the search box, select the **Common Data Service** connector, and select **Connect**.</span></span>
3. <span data-ttu-id="5d465-151">Í reitinn **Vefslóð þjóns** í Common Data Service-glugganum skal slá inn URI fyrirtækisins fyrir Dataverse-umhverfið og velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5d465-151">In the **Server Url** field of the Common Data Service window, enter the organization URI for your Dataverse environment, and select **OK**.</span></span>
  
   ![Sláðu inn URI fyrir Dataverse umhverfið þitt](./media/PowerBIDataverseURLSetup.png)
  
4. <span data-ttu-id="5d465-153">Í skoðunarglugganum skal stækka hnútinn **Einingar**.</span><span class="sxs-lookup"><span data-stu-id="5d465-153">In the Navigator window, expand the **Entities** node.</span></span>
5. <span data-ttu-id="5d465-154">Í leitarreitnum skal færa inn **mshr_hcmworkerbaseentity** og velja eininguna.</span><span class="sxs-lookup"><span data-stu-id="5d465-154">In the search box, enter **mshr_hcmworkerbaseentity**, and select the entity.</span></span>
6. <span data-ttu-id="5d465-155">Veldu **Umbreyta gögnum**.</span><span class="sxs-lookup"><span data-stu-id="5d465-155">Select **Transform Data**.</span></span>
7. <span data-ttu-id="5d465-156">Í glugga Power Query-ritils skal velja **Ítarlegur ritill**.</span><span class="sxs-lookup"><span data-stu-id="5d465-156">In the Power Query Editor window, select **Advanced Editor**.</span></span>
8. <span data-ttu-id="5d465-157">Í glugganum **Ítarlegur ritill** skal uppfæra fyrirspurnina þannig að hún líti út eins og hér að neðan, bæta við eða fjarlægja dálka úr fylkinu eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="5d465-157">In the **Advanced Editor** window, update the query to look like the below, adding or removing any columns to the array as needed.</span></span>

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Uppfæra fyrirspurnina í ítarlegum ritli fyrir Power Query-ritil](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. <span data-ttu-id="5d465-159">Velja **Ekkert**.</span><span class="sxs-lookup"><span data-stu-id="5d465-159">Select **Done**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="5d465-160">Ef villa kom upp áður af gerðinni 429 vegna fyrirspurnarinnar á undan uppfærslu, þarf hugsanlega að bíða eftir tímabili endurtilrauna áður en fyrirspurnin er endurhlaðin til að ljúka henni.</span><span class="sxs-lookup"><span data-stu-id="5d465-160">If you previously received an error of type 429 from the query prior to updating, you may need to wait for the retry period prior to refreshing the query for it to complete successully.</span></span>

10. <span data-ttu-id="5d465-161">Smellið á **Loka og nota** á aðgerðarborða Power Query-ritils.</span><span class="sxs-lookup"><span data-stu-id="5d465-161">Click **Close & Apply** on the Power Query Editor action ribbon.</span></span>

<span data-ttu-id="5d465-162">Þá verður hægt að setja saman Power BI-skýrsluna vegna dálkanna sem valdir eru í sýndartöflunni.</span><span class="sxs-lookup"><span data-stu-id="5d465-162">You're then able to begin building your Power BI report against the columns selected from the virtual table.</span></span>

#### <a name="selecting-columns-in-power-apps"></a><span data-ttu-id="5d465-163">Velja dálka í Power Apps</span><span class="sxs-lookup"><span data-stu-id="5d465-163">Selecting columns in Power Apps</span></span>

<span data-ttu-id="5d465-164">Svipað og Dataverse vef API fyrirspurnir og Power BI, er hægt að auka afköst fyrirspurnar fyrir Power Apps sem byggir á Dataverse sýndartöflum með því að sleppa dálkum tengdra taflna í forritinu.</span><span class="sxs-lookup"><span data-stu-id="5d465-164">Similar to Dataverse Web API queries and Power BI, you can improve query performance for Power Apps based on Dataverse virtual tables by excluding columns of related tables from your app.</span></span> <span data-ttu-id="5d465-165">Ef einhverjir dálkar úr tengdri töflu hafa verið hafðir með á síðu, þá mun vefslóð beiðni sem var stofnuð til að sækja gögnin hafa með eiginleika framandlykla tengdrar töflu.</span><span class="sxs-lookup"><span data-stu-id="5d465-165">If any columns from a related table have been included on a page, then the request URL constructed to fetch the data will include foreign key properties of the related table.</span></span> <span data-ttu-id="5d465-166">Þetta, eins og í dæmunum um [Dálkar valdir í OData-fyrirspurn](#selecting-columns-in-power-apps) að ofan, minnkar afköst vegna fleiri uppflettinga á gögnum.</span><span class="sxs-lookup"><span data-stu-id="5d465-166">This, as in the examples of [Selecting columns in an OData Query](#selecting-columns-in-power-apps) above, reduces performance by causing additional data lookups.</span></span>

<span data-ttu-id="5d465-167">Til að komast fram hjá þessu er hægt að staðfesta að engir gagnareitir úr tengdum töflum hafi verið hafðir með í neinu gagnasniði Power App.</span><span class="sxs-lookup"><span data-stu-id="5d465-167">To work around this, you can validate that no data fields from related tables have been included on any data form of your Power App.</span></span>

1. <span data-ttu-id="5d465-168">Á svæði trjáyfirlits skal velja gagnasniðið fyrir skjámyndina.</span><span class="sxs-lookup"><span data-stu-id="5d465-168">In the Tree view pane, select the data form for the screen.</span></span>
2. <span data-ttu-id="5d465-169">Á svæðinu **Eiginleikar** skal velja **Breyta** í eiginleikanum **Reitir**.</span><span class="sxs-lookup"><span data-stu-id="5d465-169">In the **Properties** pane, select **Edit** on the **Fields** property.</span></span>
3. <span data-ttu-id="5d465-170">Á svæðinu **Gögn** skal staðfesta að engir völdu reitanna séu reitir sýndartöflu gagnaveitunnar.</span><span class="sxs-lookup"><span data-stu-id="5d465-170">In the **Data** pane, verify that none of the selected fields are fields of the virtual table of the data source.</span></span>

<span data-ttu-id="5d465-171">Ef til dæmis einn af gagnareitunum, sem hafðir eru með á síðu í forritinu, vísar í aðra töflu á borð við **ThisItem.Worker.Name**, þar sem **Starfsmaður** er tengda taflan, er möguleiki á minnkuðum afköstum þegar gögnin eru sótt.</span><span class="sxs-lookup"><span data-stu-id="5d465-171">For example, if one of the data fields included on a page in the app references another table, such as **ThisItem.Worker.Name**, where **Worker** is the related table, there is a potential for reduced performance in fetching the data.</span></span>

<span data-ttu-id="5d465-172">Hægt er að nota [Power Apps Fylgjast með](/powerapps/maker/monitor-overview) til að tryggja að aðeins dálkarnir sem þú þarft séu teknir með í fyrirspurnina til að sækja gögnin fyrir Power App.</span><span class="sxs-lookup"><span data-stu-id="5d465-172">You can use the [Power Apps Monitor](/powerapps/maker/monitor-overview) to ensure that only the columns you need are being included in the query to get the data for the Power App.</span></span> <span data-ttu-id="5d465-173">Hægt er að skoða vefslóðina sem smíðuð er fyrir getRows-aðgerðina til að tryggja að dálkarnir sem valdir hafa verið fyrir forritið verði ákjósanlegir til að sækja gögnin.</span><span class="sxs-lookup"><span data-stu-id="5d465-173">You can view the URL constructed for the getRows operation to ensure the columns you have selected for your app will be optimal for retrieving the data.</span></span>

![Nota Power Apps eftirfylgni til að greina getData-aðgerðina](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a><span data-ttu-id="5d465-175">Sía gagnafyrirspurnina</span><span class="sxs-lookup"><span data-stu-id="5d465-175">Filtering the data query</span></span>

<span data-ttu-id="5d465-176">Önnur aðferð til að bæta afköst fyrirspurnarkeyrslu er að takmarka fjölda færslna sem er skilað í fyrirspurnarniðurstöðunum.</span><span class="sxs-lookup"><span data-stu-id="5d465-176">Another method for improving query execution performance is to limit the number of records returned in the query results.</span></span> <span data-ttu-id="5d465-177">Hægt er að gera þetta með því að sía niðurstöðurnar til að tryggja að þú sért aðeins að taka á móti þeim færslum sem þú þarft.</span><span class="sxs-lookup"><span data-stu-id="5d465-177">You can do this by filtering the results to ensure that you are only receiving the records you need.</span></span>

<span data-ttu-id="5d465-178">Sjá [Síuniðurstöður](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) fyrir frekari upplýsingar um síun fyrirspurnargagna.</span><span class="sxs-lookup"><span data-stu-id="5d465-178">See [Filter results](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for more information on filtering query data.</span></span>

### <a name="limiting-the-page-size-of-the-query"></a><span data-ttu-id="5d465-179">Takmarka blaðsíðustærð fyrirspurnar</span><span class="sxs-lookup"><span data-stu-id="5d465-179">Limiting the page size of the query</span></span>

<span data-ttu-id="5d465-180">Ef unnið er með stór gagnasöfn er hægt að skipta niðurstöðum fyrirspurnar niður á margar síður með því að bæta `odata.maxpagesize` kjörstillingarhausnum við gagnafyrirspurnir.</span><span class="sxs-lookup"><span data-stu-id="5d465-180">If you're working with large data sets, you can divide query results into multiple pages by adding the `odata.maxpagesize` preference header to data queries.</span></span>

<span data-ttu-id="5d465-181">Frekari upplýsingar um síðuskiptingu er að finna í [Tilgreina fjölda eininga sem á að skila á síðu](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span><span class="sxs-lookup"><span data-stu-id="5d465-181">For more information on paging, see [Specify the number of entities to return in a page](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span></span>

## <a name="see-also"></a><span data-ttu-id="5d465-182">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5d465-182">See also</span></span>

- [<span data-ttu-id="5d465-183">Skilgreina Dataverse-sýndartöflur</span><span class="sxs-lookup"><span data-stu-id="5d465-183">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)
- [<span data-ttu-id="5d465-184">Algengar spurningar um sýndartöflur Human Resources</span><span class="sxs-lookup"><span data-stu-id="5d465-184">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)
- [<span data-ttu-id="5d465-185">Algengar spurningar um takmörkun</span><span class="sxs-lookup"><span data-stu-id="5d465-185">Throttling FAQ</span></span>](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]