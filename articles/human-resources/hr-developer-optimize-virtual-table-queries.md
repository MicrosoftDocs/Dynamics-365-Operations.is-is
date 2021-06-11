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
# <a name="optimize-dataverse-virtual-table-queries"></a>Fínstilla Dataverse sýndartöflufyrirspurnir

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a>Úthreyfing

### <a name="overview"></a>Yfirlit

Þegar Dataverse sýndartöflur eru notaðar til að þróa samþættingar og aðrar gagnatengingar við Dynamics 365 Human Resources geta komið upp vandamál með afköst vegna fyrirspurna um sýndartöflurnar. Hæg fyrirspurnarkeyrsla getur gerst í ýmsum biðlurum eða viðmótum. Til dæmis gæti vandamálið komið upp við eftirfarandi aðstæður:

- Þegar spurst er fyrir um sýndartöflu í gegnum Dataverse vef API
- Þegar Power App er búið til gegn sýndartöflu
- Þegar byggð er Power BI skýrsla í sýndartöflu

Vandamál með afköst geta komið upp í öllum þessum viðmótum.

Ein orsök á hægum afköstum með Dataverse sýndartöflur fyrir Human Resources er dálkar framandlykla í sýndartöflunni sem tengist [skoðunareiginleikum](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) töflunnar. Þegar skoðunareiginleikar eru búnir til fyrir sýndartöflu er dálki framandlykils sjálfkrafa bætt við töfluna til að sýna gildi lykilsins fyrir tengdan dálk lykils í sýndartöflunni. Til dæmis er **_mshr_fk_person_id_value** dálkinum bætt við **mshr_hcmworkerbaseentity** eininguna með framandlyklinum úr **mshr_dirpersonentity** einingunni. Vegna þess hvernig gildum fyrir þessa dálka framandlykla er viðhaldið í töflu, getur það að sækja gildin haft neikvæð áhrif á afköst fyrirspurnar um sýndartöfluna.

### <a name="potential-symptoms"></a>Möguleg einkenni

Dæmi þar sem þú gætir séð þessi áhrif er í fyrirspurnum gegn starfsmanninum (**mshr_hcmworkerentity**) eða einingu grunnstarfskrafts (**mshr_hcmworkerbaseentity**). Frammistöðuvandamál gætu birtst á nokkra mismunandi vegu:

- **Hæg fyrirspurnarkeyrsla**: Fyrirspurn vegna sýndartöflu gæti skilað eðlilegum niðurstöðum en tekið lengri tíma en vanalega að ljúka keyrslu fyrirspurnarinnar.
- **Fyrirspurnin rann út á tíma**: Þessi fyrirspurn gæti runnið út á tíma og skilað eftirfarandi villu: „Náð var í merki til að kalla á Finance and Operations, en Finance and Operations skilaði villu af gerðinni InternalServerError.“
- **Óvænt villa**: Fyrirspurnin gæti skilað villu af gerðinni 400 með eftirfarandi skilaboðum: „Óvænt villa kom upp.“

  ![Villugerð 400 á HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType400.png)

- **Takmörkun**: Fyrirspurnin kann að ofnota tilföng netþjóns og orðið fyrir takmörkunum. Í slíku tilfelli skilar fyrirspurnin eftirfarandi villu: „Náð var í merki til að kalla á Finance and Operations, en Finance and Operations skilaði villu af gerðinni 429.“ Frekari upplýsingar um takmörkun í Human Resources er að finna í [Algengar spurningar um takmörkun](./hr-admin-integration-throttling-faq.md).

  ![Villugerð 429 á HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a>Upplausn

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a>Takmarka dálkafjölda í gagnafyrirspurninni

Með sýndartöflum er ein sú aðferð sem hefur mestan möguleika á að bæta afköst fyrirspurnar er að takmarka fjölda dálka sem valdir eru í fyrirspurninni. Almennar leiðbeiningar um fínstillingu á afköstum fyrirspurnar er að takmarka dálkana sem skilað er í fyrirspurninni niður í þá eiginleika sem á þarf að halda. Þetta á sérstaklega við um dálka framandlykla í sýndartöflum. Ef þú þarft ekki gildin í dálkum framandlykla fyrir samþættinguna eða skýrsluna, þá skaltu skipuleggja fyrirspurnina þannig að hún velji aðeins dálkana sem á þarf að halda og sleppir dálkum framandlykla.

#### <a name="selecting-columns-in-an-odata-query"></a>Dálkar valdir í OData-fyrirspurn

Þegar fyrirspurn er send á sýndartöflu í gegnum Dataverse vef API er hægt að takmarka fjölda dálka sem hafðir eru með í fyrirspurninni með því að nota valkostinn **$select** í kerfisfyrirspurn og skilgreina dálkana þar sem þarf að skila niðurstöðum. Til að hámarka árangur skaltu útiloka dálka framandlykla (þá með **_mshr_FK_** forskeytið) úr fyrirspurninni.

Til dæmis mun eftirfarandi fyrirspurn gagnvart einingunni **mshr_hcmworkerbaseentity** aðeins taka með dálkana sem hafðir eru með í fyrirspurnarmöguleika **$select**, þar sem gildum framandlykla er sleppt. Þetta gefur umtalsvert betri afköst í fyrirspurn sem tekur með alla dálka töflu.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Tillagan um að takmarka fjölda dálka sem eru valdir á einnig við þegar fyrirspurnarmöguleikinn **$expand** er notaður til að stækka fyrirspurnina yfir í tengdar sýndartöflur í gegnum skoðunareiginleika. Eftirfarandi fyrirspurn inniheldur t.d. dálka úr einingunni **mshr_hcmworkerbaseentity** með stækkuðum dálkum úr einingunni **mshr_dirpersonentity**. Athugið að fyrirspurnarmöguleikinn **$select** er einnig hafður með í fyrirspurnarmöguleikanum **$expand**.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Þegar þessi aðferð er notuð til að sækja gögn með fyrirspurnarmöguleikanum **$select** í klausu fyrirspurnarmöguleikans **$expand** sjást yfirleitt enn betri afköst þegar skoðunareiginleikinn á milli eininganna er margt í eitt vensl. Ekki er víst að þú sjáir sömu styttingu á tíma fyrirspurnarkeyrslu þegar eitt í margt vensl eru stækkuð. Frekari upplýsingar um skilgreiningu vensla fyrir Dataverse sýndartöflur er að finna í [Töfluvensl](/powerapps/maker/data-platform/create-edit-entity-relationships).

Frekari upplýsingar um notkun á fyrirspurnarmöguleikum **$select** og **$expand** í kerfinum í Dataverse vef API er að finna í [Sækja tengdar færslueiningar með fyrirspurn](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).

#### <a name="selecting-columns-in-power-bi"></a>Velja dálka í Power BI

Ef þú finnur fyrir einhverjum af áðurnefndum vísbendingum um hæga keyrslu þegar Power BI skýrsla er sett saman gagnvart Dataverse sýndartöflu, er hægt að bæta afköstin með því að sleppa dálkum framandlykla úr dálkunum sem valdir eru úr töflunni fyrir skýrsluna. Til dæmis ef þú notar Power BI Desktop til að búa til skýrslu gagnvart einingunni **mshr_hcmworkerbaseentity**, geturðu notað eftirfarandi skref til að velja dálkana sem á að hafa með í skýrslufyrirspurninni.

1. Í Power BI Desktop skal velja **Fleiri...** úr fellilistanum **Sækja gögn** á aðgerðarborðanum.
2. Í glugganum **Sækja gögn** skal slá inn **Common Data Service** í leitarreitinn, velja **Common Data Service** tengilinn og velja **Tengja**.
3. Í reitinn **Vefslóð þjóns** í Common Data Service-glugganum skal slá inn URI fyrirtækisins fyrir Dataverse-umhverfið og velja **Í lagi**.
  
   ![Sláðu inn URI fyrir Dataverse umhverfið þitt](./media/PowerBIDataverseURLSetup.png)
  
4. Í skoðunarglugganum skal stækka hnútinn **Einingar**.
5. Í leitarreitnum skal færa inn **mshr_hcmworkerbaseentity** og velja eininguna.
6. Veldu **Umbreyta gögnum**.
7. Í glugga Power Query-ritils skal velja **Ítarlegur ritill**.
8. Í glugganum **Ítarlegur ritill** skal uppfæra fyrirspurnina þannig að hún líti út eins og hér að neðan, bæta við eða fjarlægja dálka úr fylkinu eftir þörfum.

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

9. Velja **Ekkert**.

   > [!NOTE]
   > Ef villa kom upp áður af gerðinni 429 vegna fyrirspurnarinnar á undan uppfærslu, þarf hugsanlega að bíða eftir tímabili endurtilrauna áður en fyrirspurnin er endurhlaðin til að ljúka henni.

10. Smellið á **Loka og nota** á aðgerðarborða Power Query-ritils.

Þá verður hægt að setja saman Power BI-skýrsluna vegna dálkanna sem valdir eru í sýndartöflunni.

#### <a name="selecting-columns-in-power-apps"></a>Velja dálka í Power Apps

Svipað og Dataverse vef API fyrirspurnir og Power BI, er hægt að auka afköst fyrirspurnar fyrir Power Apps sem byggir á Dataverse sýndartöflum með því að sleppa dálkum tengdra taflna í forritinu. Ef einhverjir dálkar úr tengdri töflu hafa verið hafðir með á síðu, þá mun vefslóð beiðni sem var stofnuð til að sækja gögnin hafa með eiginleika framandlykla tengdrar töflu. Þetta, eins og í dæmunum um [Dálkar valdir í OData-fyrirspurn](#selecting-columns-in-power-apps) að ofan, minnkar afköst vegna fleiri uppflettinga á gögnum.

Til að komast fram hjá þessu er hægt að staðfesta að engir gagnareitir úr tengdum töflum hafi verið hafðir með í neinu gagnasniði Power App.

1. Á svæði trjáyfirlits skal velja gagnasniðið fyrir skjámyndina.
2. Á svæðinu **Eiginleikar** skal velja **Breyta** í eiginleikanum **Reitir**.
3. Á svæðinu **Gögn** skal staðfesta að engir völdu reitanna séu reitir sýndartöflu gagnaveitunnar.

Ef til dæmis einn af gagnareitunum, sem hafðir eru með á síðu í forritinu, vísar í aðra töflu á borð við **ThisItem.Worker.Name**, þar sem **Starfsmaður** er tengda taflan, er möguleiki á minnkuðum afköstum þegar gögnin eru sótt.

Hægt er að nota [Power Apps Fylgjast með](/powerapps/maker/monitor-overview) til að tryggja að aðeins dálkarnir sem þú þarft séu teknir með í fyrirspurnina til að sækja gögnin fyrir Power App. Hægt er að skoða vefslóðina sem smíðuð er fyrir getRows-aðgerðina til að tryggja að dálkarnir sem valdir hafa verið fyrir forritið verði ákjósanlegir til að sækja gögnin.

![Nota Power Apps eftirfylgni til að greina getData-aðgerðina](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a>Sía gagnafyrirspurnina

Önnur aðferð til að bæta afköst fyrirspurnarkeyrslu er að takmarka fjölda færslna sem er skilað í fyrirspurnarniðurstöðunum. Hægt er að gera þetta með því að sía niðurstöðurnar til að tryggja að þú sért aðeins að taka á móti þeim færslum sem þú þarft.

Sjá [Síuniðurstöður](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) fyrir frekari upplýsingar um síun fyrirspurnargagna.

### <a name="limiting-the-page-size-of-the-query"></a>Takmarka blaðsíðustærð fyrirspurnar

Ef unnið er með stór gagnasöfn er hægt að skipta niðurstöðum fyrirspurnar niður á margar síður með því að bæta `odata.maxpagesize` kjörstillingarhausnum við gagnafyrirspurnir.

Frekari upplýsingar um síðuskiptingu er að finna í [Tilgreina fjölda eininga sem á að skila á síðu](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).

## <a name="see-also"></a>Sjá einnig

- [Skilgreina Dataverse-sýndartöflur](hr-admin-integration-common-data-service-virtual-entities.md)
- [Algengar spurningar um sýndartöflur Human Resources](hr-admin-virtual-entity-faq.md)
- [Algengar spurningar um takmörkun](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]