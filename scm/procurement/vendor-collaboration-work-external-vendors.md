---
title: "Samvinnusvæði lánardrottins með ytri lánardrottna"
description: "Þetta efnisatriði lýsir því hvernig innkaupastjórum geta unnið með ytri lánardrottinn til að skiptast á upplýsingar um innkaupapantanir og vörusendingabirgðir."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: d585ae0716a4bd9c3531e8639cd7c6b3cab780ac
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-with-external-vendors"></a>Samvinnusvæði lánardrottins með ytri lánardrottna

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir því hvernig innkaupastjórum geta unnið með ytri lánardrottinn til að skiptast á upplýsingar um innkaupapantanir og vörusendingabirgðir.

**Samvinnusvæði lánardrottins** kerfiseining er beint að lánardrottnum sem ekki hafa samþættingu rafrænna gagnaskipta (EDI) við Microsoft Dynamics 365 for Operations. Það leyfir lánardrottna til að vinna með innkaupapöntun, reikninga, og upplýsingar um vörusendingabirgðir. Þetta efnisatriði lýsir því hvernig er hægt vinna vandræðalaust með ytri lánardrottna sem eru að nota viðmótið samstarf lánardrottna til að vinna með að vinna með Innkaupapanganir og vörusendingabirgðir. Það lýst einnig hvernig á að virkja tiltekinn lánardrottinn til að nota samstarf lánardrottna og hvernig á að skilgreina þær upplýsingar sem allir lánardrottnar geta séð þegar þeir svara Innkaupapöntun. Fyrir frekari upplýsingar um hvaða ytri lánardrottnum geta gert viðmót fyrir samstarf lánardrottna , sjá [samstarf lánardrottna við viðskiptavini](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Sjá frekari upplýsingar um hvernig lánardrottnum geta notað samstarf lánardrottna í reikningsfærslu ferli, sjá [vinnusvæði reikningsfærslu fyrir samstarf lánardrottna](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace). Fyrir upplýsingar um hvernig á að gera ráðstafanir fyrir nýja notendur samstarfs lánardrottna, sjá [Stjórna notendum samstarfs lánardrottna](manage-vendor-collaboration-users.md).

## <a name="define-the-information-shown-to-vendors-when-they-respond-to-pos"></a>Tilgreina upplýsingar sem eru sýnd fyrir lánardrottnum þegar þeir svara innkaupapöntunum.
Þegar lánardrottna svara Innkaupapöntun sem þú sendir þeim, sjá þeir svarglugga þar sem þau þurfa að staðfesta að þeir vilja samþykkja, hafna eða samþykkja Innkaupapöntun með breytingum. Þær upplýsingar sem þarf að sýna lánardrottins á þeim tímapunkti getur verið sértæk fyrir þitt fyrirtækið, svo hægt er að tilgreina textann sem birtist á hverja þrjár staðfestingarboðum. Til dæmis, gæti texti upplýst lánardrottinn um næsta skref í ferlinu, eða um skilmála.  

Til að tilgreina textann sem birtist í svari IP:

1.  Opnaðu **Upplýsingar fyrir lánardrottna sem svara IP** síðuna.
2.  Veljið eina af eftirtöldum gerðum svars:
3.  Smella á **Breyta.**
4.  Færið inn upplýsingar sem óskað er eftir að lánardrottna sjá á **upplýsingaboð** reitnum.

Stofna aðskilin skilaboð með viðeigandi tungumálakóða ef nauðsynlegt er að bæta við skilaboðum á fleiri en eitt tungumál. Lánardrottinn birtast skilaboð á tungumálinu sem þær nota.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Stilla valkosti fyrir samstarf lánardrottins fyrir ákveðinn lánardrottinn
Almennar stillingar fyrir samstarf lánardrottins í Dynamics 365 for Operations eru skilgreind af kerfisstjóra. T.d. þær ákvarða hvaða öryggishlutverk eru tiltækar fyrir öllum lánardrottnum sem vinna með þér. Einnig eru sumum stillingum geta verið mismunandi fyrir hvern lánadrottnalykil og ætti að stilla þær:

-   Virkja samstarf lánardrottna
-   Ákveða hvort lánardrottinn á að sjá verðupplýsingar.

### <a name="enable-vendor-collaboration"></a>Virkja samstarf lánardrottna

Áður en hægt er að stofna notendareikningar ytri lánardrottins, þarf að skilgreina lánardrottnalykilinn sem leyfir þeim að nota samstarf lánardrottna. Til að gera þetta skal stilla **virkjun samstarfs** svæðið virkt á **Almennt** flipanum á **Lánardrottna** síðu. Tveir valkostir sem hægt er að velja eru:

-   **Virk (Innkaupapöntun er staðfest sjálfkrafa) **- innkaupapantanir eru sjálfkrafa staðfestar þegar lánardrottinn tekur á móti þeim án breytinga.
-   **Virk (Innkaupapöntun er ekki sjálfvirkt-staðfest) **- innkaupapantanir þarf að vera handvirkt staðfest af fyrirtæki þitt eftir að lánardrottni hefur samþykkt þau.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>Ákveða hvort lánardrottinn sjái verðupplýsingar.

Ef óskað er að sýna upplýsingar um verð eins og einingarverðið, afslætti og gjöld gegnum viðmót samstarfsins, þarf að stilla **verð/upphæð innkaupapöntunar** valkostinn á **Já** á lánardrottnalykilinn. Þessi valkostur er tiltæk á **Sjálfgildi innkaupapantana** flipanum.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>Unnið með IP þegar notað er samstarf lánardrottna
### <a name="sending-a-po-to-the-vendor"></a>Senda IP til lánardrottins

Innkaupapantanir eru undirbúnar í Dynamics 365 for Operations. Þegar Innkaupapöntunin hefur stöðuna **Samþykkt**, er hún send til lánardrottna með því að nota **Senda til staðfestingar ** aðgerðina á síðunni **Innkaupapöntun**. Staða Innkaupapöntunar Breytist í **í Ytri Yfirferð**. Eftir að Innkaupapöntunin hefur verið send lánardrottni er hægt að sjá það á **Innkaupapantanir fyrir yfirferð** síðu í viðmóti fyrir samstarf lánardrottna, þar sem þær geta samþykkja, hafna eða leggja til breytingar á pöntun. Lánardrottinn getur líka bætt við athugasemdum til að gefa upplýsingar, eins og breytingar á Innkaupapöntun. Ef óskað er að beina athygli lánardrottins að nýrri innkaupapöntun er einnig hægt að senda Innkaupapöntunina með tölvupósti með því að nota prentstjórnunarkerfið.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>Staðfesting og móttöku Innkaupapöntunar af lánardrottinn

Þegar lánardrottinn hefur samþykkt innkaupapöntun má staðfesta sjálfvirkt IP eða það gæti þurft að staðfesta handvirkt. Það veltur á hvort reiturinn **Virkjun Lánardrottins **er stillt á **Virkt (Innkaupapöntun er staðfest sjálfkrafa)** fyrir lánardrottinn, eða á **Virkt (Innkaupapöntunar er ekki staðfest sjálfkrafa)**.  

Taflan hér að neðan sýnir dæmigerð upplýsingaskipti, eftir því hvernig lánardrottinn svarar þegar þú sendir innkaupapöntun til staðfestingar.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Svar lánardrottins</strong></td>
<td><strong>Niðurstaða</strong></td>
</tr>
<tr class="even">
<td>Lánardrottinn <strong>samþykkir</strong> pöntun. Dynamics 365 for Operations er stillt á að staðfesta sjálfvirkt Innkaupapöntun þegar lánardrottinn staðfestir.</td>
<td>Staða pöntunar er uppfærð í <strong>Staðfest</strong>. Ef eitthvað kemur í veg fyrir að pöntun sé uppfærð, þá verður svar lánardrottins enn skráð sem <strong>samþykkt</strong> en innkaupapöntunin er áfram í stöðunni <strong>Í ytri yfirferð</strong>.</td>
</tr>
<tr class="odd">
<td>Lánardrottinn <strong>samþykkir</strong> pöntun. Dynamics 365 for Operations er ekki stillt á að staðfesta sjálfvirkt Innkaupapöntun þegar lánardrottinn staðfestir.</td>
<td>Svar lánardrottins er skráð sem <strong>samþykkt</strong> en innkaupapöntunin er áfram í stöðunni <strong>Í ytri yfirferð</strong>.</td>
</tr>
<tr class="even">
<td>Lánardrottinn <strong>hafnar </strong> pöntun.</td>
<td>Svar lánardrottins er skráð sem <strong>Hafnað</strong> og innkaupapöntunin er áfram í stöðunni <strong>Í ytri yfirferð</strong>. Höfnunin er móttekin með athugasemd lánardrottna.</td>
</tr>
<tr class="odd">
<td>Lánardrottinn <strong>samþykkir pöntunina með breytinum</strong>. Stungið er upp á breytingum á stigi línunnar. Mögulegt er að samþykkja eða hafna einstakar línur. Öðrum mögulegt breytingar eru m.a.:
<ul>
<li>Breyta dagsetningum eða magn.</li>
<li>Skipta upp línum fyrir mismunandi afhendingardaga eða magn.</li>
<li>Nota staðgengilsvöru.</li>
</ul>
Upplýsingar um Verð og gjöld geta ekki verið breytt af lánardrottinn. Hægt að gera tillögur fyrir breytingum á þeim með athugasemdir.</td>
<td>Svar lánardrottins er skráð sem <strong>Samþykkt með breytingum</strong> <strong></strong> og innkaupapöntunin er áfram í stöðunni <strong>Í ytri yfirferð</strong>.</td>
</tr>
</tbody>
</table>

Hægt er að nota vinnusvæðið **Undirbúningur** ** innkaupapöntunar** til að fylgjast með hvaða innkaupapöntun lánardrottinn hefur svarað. Þetta vinnusvæði inniheldur tvo lista sem innihalda innkaupapantanir með stöðuna **í Ytri Yfirferð**:

-   Í ytri yfirferð krefst aðgerða.
-   Í ytri yfirferð og bíður svars lánardrottins.

### <a name="changing-a-po"></a>Breyta Innkaupapöntun

Þegar breyta þarf Innkaupapöntun sem er þegar búið að svara er hægt að senda nýja útgáfu Innkaupapöntunar til lánardrottins. Ný Innkaupapöntun verður með viðskeyti til að gefa til kynna að það sé breytt útgáfa af Innkaupapöntun sem var áður í gangi. Í **staðfestingarsögu innkaupapantana lánardrottins ** síðu getur þú og lánardrottnana að rekja sögu hverja pöntun. Áður staðfesta útgáfa Innkaupapöntunarinnar mun vera í lista yfir staðfestar Innkaupapantanir þar til ný Innkaupapöntun hefur verið staðfest.

### <a name="cancelling-a-po"></a>Hætt við Innkaupapöntun

Þegar hætt er við Innkaupapöntun er stöðu breytt í **Samþykkt**. Þú þarft að senda Innkaupapöntunina aftur til lánardrottins í gegnum Gátt lánardrottins þannig að lánardrottinn get staðfest eða hafnað ógildingunni. Eftir að ógildingin er staðfest birtist Innkaupapöntunin í lista lánardrottins yfir staðfestar Innkaupapantanir sem **Hætt við**.

### <a name="adding-attachments-to-a-po"></a>Bætir viðhengjum við IP

Hægt að bæta við viðhengi eins og skrár, myndir og athugasemdir við Innkaupapöntun með því að nota skjalstjórnunarkerfið. Viðhengi sem hengd eru við með takmörkuninni af gerðinni **Ytri** verður sýnilegt lánardrottins þegar Innkaupapöntunin er send til þeirra.

## <a name="purchase-order-statuses-and-versions"></a>Staða innkaupapöntunar og Útgáfur
Þessi kafli lýsir mismunandi stöðum sem Innkaupapöntun getur haft fram að þeim tíma þegar það er staðfest, og á hvaða tímapunkti nýjar útgáfur Innkaupapöntunin gerðar tiltækar til lánardrottins. Þarna er munur á, allt eftir því hvort þú notar breytingastjórnun fyrir innkaupapöntun. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Útgáfur og stöður ef þú notar ekki breytingastjórnun

Taflan hér að neðan sýnir dæmi um breytingar á stöðu og útgáfum sem Innkaupapöntun gæti farið í gegnum.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aðgerð**                                                               | **Staða og útgáfa**                                                                                                                                       |
| Upprunaleg útgáfa af Innkaupapöntuninni er stofnuð í Dynamics 365 for Operations. | Staðan er  **Samþykkt**.                                                                                                                                  |
| Innkaupapöntunin er send á lánardrottins.                                            | Útgáfa er skráð í viðmót samstarfs lánardrottna og stöðunni er breytt í **Í Ytri Yfirferð**.                                          |
| Lánardrottinn sendir inn **Samþykkt með breytingum** svarið.                  | Staðan er enn **í Ytri yfirferð**.                                                                                                                  |
| Þú gerir einhverjar breytingar sem lánardrottinn biður um.                  | Stöðu breytt í **Samþykkt**.                                                                                                                        |
| Þú sendir nýja útgáfu af Innkaupapöntuninni lánardrottins.                        | Ný útgáfa er skráð í viðmót samstarfs lánardrottna og stöðunni er breytt í **Í Ytri Yfirferð**.                                      |
| Lánardrottinn samþykkir nýju útgáfuna af IP.                            | Staðan er enn **í Ytri Yfirferð **nema lánardrottnalykill er skilgreindur til að stilla sjálfkrafa Innkaupapöntun á stöðuna **Staðfest** þegar þeir samþykkja það. |

Lánardrottnar þurfa ekki að staðfesta Innkaupapöntun í viðmóti fyrir samstarf lánardrottna. Þeir geta einnig sent skilaboð í tölvupósti eða tilkynnt samþykki Innkaupapöntunarinnar gegnum aðrar rásir. Síðan er hægt að staðfesta pöntunina handvirkt í Dynamics 365 for Operations. Ef þú gerir þetta berst viðvörun um að verið er að staðfesta pöntun jafnvel þótt að það er ekkert svar frá lánardrottni. Innkaupapöntunin birtist síðan í staðfestingarsögu sem opin staðfest pöntun sem hefur ekki svör. Lánardrottinn hefur ekki lengur valkost til að staðfesta eða hafna innkaupapöntun.  

**Athugasemd:** Sú útgáfa Innkaupapöntunar sem er tiltæk við önnur ferli í Dynamics 365 for Operations er alltaf síðasta útgáfa, jafnvel þó að sú útgáfa hafi ekki enn verið skráð í viðmóti fyrir samstarf lánardrottna.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Útgáfur og stöður ef þú notar breytingastjórnun

Ef breytingastjórnun er virkjuð fyrir Innkaupapöntun, fer Innkaupapöntunin í gegnum samþykktarverkflæði til að komast í stöðuna **Samþykkt**. Þetta ferli er ekki sýnilegt lánardrottni.  

Taflan hér að neðan sýnir dæmi um breytingar á stöðu og útgáfu sem Innkaupapöntun gæti farið í gegnum þegar breytingastjórnun er virkjuð. Útgáfan er skráð þegar Innkaupapöntunin er samþykkt, ekki þegar Innkaupapöntunin er send til lánardrottins eða staðfest.

|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aðgerð**                                                                                                    | **Staða og útgáfa**                                                                                                                                                                                                                                                                                                                                                                      |
| Upprunaleg útgáfa af Innkaupapöntuninni er stofnuð í Dynamics 365 for Operations.                                      | Staðan er **Drög**.                                                                                                                                                                                                                                                                                                                                                                    |
| Innkaupapöntunin er send í samþykktarferli. (Þetta er innra ferli sem lánardrottinn er ekki hluti af.) | Stöðunni er breytt úr **Drög** til **í Yfirferð** til **Samþykki** ef Innkaupapöntuninni er ekki hafnað meðan á samþykktarferlinu stendur. Samþykkt innkaupapöntun er skráð sem útgáfa.                                                                                                                                                                                                                     |
| Innkaupapöntunin er send á lánardrottins.                                                                                  | Útgáfa er skráð í viðmót samstarfs lánardrottna og stöðunni er breytt í **Í Ytri Yfirferð**.                                                                                                                                                                                                                                                                       |
| Þú gerir einhverjar breytingar sem lánardrottinn biður um.                                                       | Stöðu er breytt aftur í **Drög**.                                                                                                                                                                                                                                                                                                                                                    |
| Innkaupapöntunin er send aftur í samþykktarferlið.                                                            | Stöðunni er breytt úr **Drög** til **í Yfirferð** til **Samþykki** ef Innkaupapöntuninni er ekki hafnað meðan á samþykktarferlinu stendur. Einnig er hægt að skilgreina kerfið þannig að tilteknar breytingar á reitum krefjast ekki endursamþykktar. Í þessu tilfelli fer staðan fyrst í **Drög** og er sjálfkrafa uppfærð í **Samþykkt**. Samþykkta Innkaupapöntunin er skráð sem ný útgáfa. |
| Þú sendir nýja útgáfu af Innkaupapöntuninni lánardrottins.                                                             | Ný útgáfa er skráð í viðmót samstarfs lánardrottna og stöðunni er breytt í **Í Ytri Yfirferð**.                                                                                                                                                                                                                                                                   |
| Lánardrottinn samþykkir nýju útgáfuna.                                                                | Stöðu er breytt í **Staðfest**, annað hvort sjálfvirkt eða þegar svarið kemur frá lánardrottni og síðan er Innkaupapöntunin staðfest.                                                                                                                                                                                                                                                     |

## <a name="share-information-about-consignment-inventory"></a>Deila upplýsingum um vörusendingabirgðir
Ef verið er að nota vörusendingabirgðir, geta lánardrottna notað viðmót fyrir samstarf lánardrottna til að skoða upplýsingar um eftirfarandi síður:

-   **Innkaupapantanir sem notar vörusendingabirgðir** - innkaupapantanir fyrir vörusendingabirgðir eru myndaðar þegar eignarhaldi á birgðum er breytt frá lánardrottninum til fyrirtækis. Innhreyfingarskjal afurða er bókaðar samtímis. Þessum innkaupapantanir vörusendinga birtast aðeins á **Innkaupapantanir sem nota vörusendingabirgðir** síðuna. Þær eru ekki teknar með í **Allar staðfestar innkaupapantanir** síðuna í á **samstarf lánardrottna** kerfiseiningu.
-   **Afurðir sem er tekið við úr vörusendingabirgðum** - Þessi síða inniheldur lista yfir allar færslur þar sem eignarhald afurða hefur verið flutt frá lánardrottni til fyrirtækis. Lánardrottnar geta nota þessar upplýsingar til að reikningsfæra á viðskiptavininn.
-   **Vörusendingarbirgðir á lager ** - Þessi síða sýnir vörusendingabirgðir á lager í eigu lánardrottins sem hefur verið móttekið í vöruhúsi þínu.





