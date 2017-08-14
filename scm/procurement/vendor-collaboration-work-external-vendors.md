---
title: "Samvinnusvæði lánardrottins með ytri lánardrottna"
description: "Þetta efnisatriði lýsir því hvernig innkaupastjórum geta unnið með ytri lánardrottinn til að skiptast á upplýsingar um innkaupapantanir og vörusendingabirgðir."
author: BibiSp
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: cbd099403f48b502ca74bcb38ae12decedb8f2da
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---

# <a name="vendor-collaboration-with-external-vendors"></a>Samvinnusvæði lánardrottins með ytri lánardrottna

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir því hvernig innkaupastjórum geta unnið með ytri lánardrottinn til að skiptast á upplýsingar um innkaupapantanir og vörusendingabirgðir.

**Samvinnusvæði lánardrottins** kerfiseining er beint að lánardrottnum sem ekki hafa samþættingu rafrænna gagnaskipta (EDI) við Microsoft Dynamics 365 for Finance and Operations. Það leyfir lánardrottna til að vinna með innkaupapöntun, reikninga, og upplýsingar um vörusendingabirgðir. Þetta efnisatriði lýsir því hvernig er hægt vinna vandræðalaust með ytri lánardrottna sem eru að nota viðmótið samstarf lánardrottna til að vinna með að vinna með Innkaupapanganir og vörusendingabirgðir. Það lýst einnig hvernig á að virkja tiltekinn lánardrottinn til að nota samstarf lánardrottna og hvernig á að skilgreina þær upplýsingar sem allir lánardrottnar geta séð þegar þeir svara Innkaupapöntun. Fyrir frekari upplýsingar um hvaða ytri lánardrottnum geta gert viðmót fyrir samstarf lánardrottna , sjá [samstarf lánardrottna við viðskiptavini](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Sjá frekari upplýsingar um hvernig lánardrottnum geta notað samstarf lánardrottna í reikningsfærslu ferli, sjá [vinnusvæði reikningsfærslu fyrir samstarf lánardrottna](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace). Fyrir upplýsingar um hvernig á að gera ráðstafanir fyrir nýja notendur samstarfs lánardrottna, sjá [Stjórna notendum samstarfs lánardrottna](manage-vendor-collaboration-users.md).

Sjá frekari upplýsingar um hvernig lánardrottnum geta notað samstarf lánardrottna í reikningsfærslu ferli, sjá [vinnusvæði reikningsfærslu fyrir samstarf lánardrottna](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace). 

Fyrir upplýsingar um hvernig á að gera ráðstafanir fyrir nýja notendur samstarfs lánardrottna, sjá [Stjórna notendum samstarfs lánardrottna](manage-vendor-collaboration-users.md).

## <a name="define-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Tilgreina upplýsingar sem eru sýndar lánardrottnum þegar þeir svara innkaupapöntunum.
Þegar lánardrottnar svara Innkaupapöntun sem þú sendir þeim, sjá þeir skilaboðaglugga þar sem þeir verða að staðfesta að þeir vilji samþykkja, hafna eða samþykkja Innkaupapöntun með breytingum. Þar sem þær upplýsingar sem verður að sýna lánardrottni á þeim tímapunkti kunna að vera sértæk fyrir fyrirtækið er hægt að tilgreina textann sem birtist í hverju af þremur staðfestingarboðunum. Til dæmis, getur textinn upplýst lánardrottinn um næsta skref í ferlinu, eða um skilmála.  

Til að tilgreina textann sem birtist í svari IP:

1.  Opnaðu **Upplýsingar fyrir lánardrottna sem svara IP** síðuna.
2.  Veljið eina af eftirtöldum gerðum svars:
3.  Smellið á **Breyta**.
4.  Færið inn upplýsingar sem óskað er eftir að lánardrottna sjá á **upplýsingaboð** reitnum.

Stofnaðu aðskilin skilaboð og tilgreindu viðeigandi tungumálakóða fyrir hvert þeirra ef nauðsynlegt er að bæta við skilaboðum á fleiri en eitt tungumál. Lánardrottninum verða birt skilaboð á því tungumáli sem hann notar.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Stilla valkosti fyrir samstarf lánardrottins fyrir ákveðinn lánardrottinn
Almennar stillingar fyrir samstarf lánardrottins í Finance and Operations eru skilgreind af kerfisstjóra. T.d. mun stjórnandi ákvarða hvaða öryggishlutverk eru tiltæk fyrir alla lánardrottna sem vinna með þér. Einnig eru sumar stillingar sem geta verið mismunandi fyrir hvern lánadrottnalykil og ætti að stilla þær:
-   Virkja samstarf lánardrottna
-   Ákveða hvort lánardrottinn á að sjá verðupplýsingar.

### <a name="enable-vendor-collaboration"></a>Virkja samstarf lánardrottna

Áður en hægt er að stofna notendareikningar ytri lánardrottins, þarf að skilgreina lánardrottnalykilinn sem leyfir þeim að nota samstarf lánardrottna. Til að gera þetta skal stilla **virkjun samstarfs** svæðið virkt á **Almennt** flipanum á **Lánardrottna** síðu. Tveir valkostir sem hægt er að velja eru:

-   **Virk (Innkaupapöntun er staðfest sjálfkrafa)**- innkaupapantanir eru sjálfkrafa staðfestar þegar lánardrottinn tekur á móti þeim án breytinga.
-   **Virk (Innkaupapöntun er ekki sjálfvirkt-staðfest)**- innkaupapantanir þarf að vera handvirkt staðfest af fyrirtæki þitt eftir að lánardrottni hefur samþykkt þau.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>Ákveða hvort lánardrottinn sjái verðupplýsingar.

Ef óskað er að sýna upplýsingar um verð eins og einingarverðið, afslætti og gjöld gegnum viðmót samstarfsins, þarf að stilla **verð/upphæð innkaupapöntunar** valkostinn á **Já** á lánardrottnalykilinn. Þessi valkostur er tiltæk á **Sjálfgildi innkaupapantana** flipanum.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>Unnið með IP þegar notað er samstarf lánardrottna
### <a name="sending-a-po-to-the-vendor"></a>Senda IP til lánardrottins

Innkaupapantanir eru undirbúnar í Finance and Operations. Þegar Innkaupapöntunin hefur stöðuna **Samþykkt**, er hún senda til lánardrottna með því að nota **Senda til staðfestingar** aðgerðar á **Innkaupapöntun** síðuna. Staða Innkaupapöntunar Breytist í **í Ytri Yfirferð**. Þegar Innkaupapöntunin hefur verið send lánardrottni getur hann séð hana á síðunni **Innkaupapantanir til skoðunar** í viðmóti lánardrottnasamvinnu. Lánardrottinn getur síðan samþykkt pöntun, hafnað henni eða stungið upp breytingum á henni. Lánardrottinn getur líka bætt við athugasemdum til að gefa upplýsingar, eins og breytingar á Innkaupapöntun. Ef óskað er að beina athygli lánardrottins að nýrri innkaupapöntun er einnig hægt að senda Innkaupapöntunina með tölvupósti með því að nota prentstjórnunarkerfið.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>Staðfesting og móttöku Innkaupapöntunar af lánardrottinn

Þegar lánardrottinn hefur samþykkt innkaupapöntun má staðfesta sjálfvirkt IP eða það gæti þurft að staðfesta handvirkt. Það veltur á hvort reiturinn **Virkjun lánardrottins** er stilltur á **Virkt (Innkaupapöntun er staðfest sjálfkrafa)** fyrir lánardrottinn, eða á **Virkt (Innkaupapöntunar er ekki staðfest sjálfkrafa)**.  

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
<td>Lánardrottinn <strong>samþykkir</strong> pöntun. Finance and Operations er stillt á að staðfesta sjálfvirkt Innkaupapöntun þegar lánardrottinn staðfestir.</td>

<td>Staða pöntunar er uppfærð í <strong>Staðfest</strong>. Ef eitthvað kemur í veg fyrir að pöntun sé uppfærð, þá verður svar lánardrottins enn skráð sem <strong>samþykkt</strong> en innkaupapöntunin er áfram í stöðunni <strong>Í ytri yfirferð</strong>. 

Innkaupapöntunin sem var send til lánardrottins og er með stöðuna **Í ytri endurskoðun** uppfærist með staðfestar afhendingardagsetningar í línunum. Uppfærsla hefur nýja útgáfu sem verður sjálfkrafa uppfærð í stöðuna **Staðfest**. Þegar Innkaupapöntunin er staðfesta mun hún birtast í viðmóti samvinnu lánardrottna.</td>
</tr>
<tr class="odd">
<td>Lánardrottinn <strong>samþykkir</strong> pöntun. Finance and Operations er ekki stillt á að staðfesta sjálfvirkt Innkaupapöntun þegar lánardrottinn staðfestir.</td>
<td>Svar lánardrottins er skráð sem <strong>samþykkt</strong> en innkaupapöntunin er áfram í stöðunni <strong>Í ytri yfirferð</strong>.

Innkaupapöntunin sem var send til lánardrottins og er með stöðuna **Í ytri endurskoðun** uppfærist með staðfestar afhendingardagsetningar í línunum. Uppfærsla hefur nýja útgáfu sem verður sjálfkrafa stillt á **Í ytri endurskoðun**. Þú getur síðan staðfest innkaupapöntunina handvirkt.</td>

</tr>
<tr class="even">
<td>Lánardrottinn <strong>hafnar </strong> pöntun.</td>
<td>Svar lánardrottins er skráð sem <strong>Hafnað</strong> og innkaupapöntunin er áfram í stöðunni <strong>Í ytri yfirferð</strong>. Höfnunin er móttekin með athugasemd lánardrottins.</td>
</tr>
<tr class="odd">
<td>Lánardrottinn <strong>samþykkir pöntunina með breytinum</strong>. Stungið er upp á breytingum á stigi línunnar. Mögulegt er að samþykkja eða hafna einstakar línur. Öðrum mögulegt breytingar eru m.a.:
<ul>
<li>Breyta dagsetningum eða magn.</li>
<li>Skipta upp línum fyrir mismunandi afhendingardaga eða magn.</li>
<li>Nota staðgengilsvöru.</li>
</ul>
Upplýsingar um Verð og gjöld geta ekki verið breytt af lánardrottinn. Hægt að gera tillögur fyrir breytingum á þeim með athugasemdir.</td>
<td>Svar lánardrottins er skráð sem <strong>Samþykkt með breytingum</strong> og innkaupapöntunin er áfram í stöðunni <strong>Í ytri yfirferð</strong>. Stöðurnar sýna hvaða gerðir breytinga lánardrottinn hefur lagt til. Sjá kaflann hér að neðan um hvernig á að uppfæra IP þegar lánardrottinn leggur til breytingar fyrir upplýsingar um notkun á breytingunum. </td>
</tr>
</tbody>
</table>

Hægt er að nota vinnusvæðið **Undirbúningur** **innkaupapöntunar** til að fylgjast með hvaða innkaupapöntun lánardrottinn hefur svarað. Þetta vinnusvæði inniheldur tvo lista sem innihalda innkaupapantanir með stöðuna **í Ytri Yfirferð**:

-   Í ytri yfirferð krefst aðgerða.
-   Í ytri yfirferð og bíður svars lánardrottins.

### <a name="changing-a-po"></a>Breyta Innkaupapöntun

Til að breyta Innkaupapöntun sem er þegar búið að svara verður að senda nýja útgáfu Innkaupapöntunar til lánardrottins. Ný Innkaupapöntun verður með viðskeyti til að gefa til kynna að það sé breytt útgáfa af Innkaupapöntun sem var áður í gangi. Síðan **Staðfestingarsaga innkaupapantana lánardrottins** gerir þér og lánardrottnum kleift að rekja sögu hverja pöntun. Áður staðfest útgáfa Innkaupapöntunarinnar mun vera í lista yfir staðfestar Innkaupapantanir þar til ný Innkaupapöntun hefur verið staðfest.

### <a name="cancelling-a-po"></a>Hætt við Innkaupapöntun

Þegar hætt er við Innkaupapöntun er stöðu breytt í **Samþykkt**. Þú þarft að senda Innkaupapöntunina aftur til lánardrottins í gegnum Gátt lánardrottins þannig að lánardrottinn get staðfest eða hafnað ógildingunni. Eftir að ógildingin er staðfest birtist Innkaupapöntunin í lista lánardrottins yfir staðfestar Innkaupapantanir sem **Hætt við**.

### <a name="adding-attachments-to-a-po"></a>Bætir viðhengjum við IP

Hægt að bæta við viðhengjum eins og skrám, myndum og athugasemdum við Innkaupapöntun með því að nota skjalastjórnunarkerfið. Viðhengi við gerðina **Ytri** verða sýnileg lánardrottni þegar Innkaupapöntunin er send til þeirra.

## <a name="update-the-po-when-a-vendor-suggests-changes"></a>Innkaupapöntunin er uppfærð þegar lánardrottinn leggur til breytingar
Þegar lánardrottinn hefur svarað Innkaupapöntuninni og ráðlögðum breytingum er næsta skrefið að vinna svarið.
Ef **vinnusvæði undirbúnings innkaupapöntunar** í Í ytri endurskoðun krefst aðgerðalista, er hægt að auðkenna Innkaupapöntun sem lánardrottinn svaraði sem samþykkta með breytingunum. Ef Í ytri endurskoðun krefst aðgerðalista er einnig er hægt að fara í svar lánardrottins. Í svari getur lánardrottinn breytt eftirfarandi upplýsingum í haus.
 
-   Tilvísun lánardrottnaskjals
-   Afhendingarmáti
-   Afhendingarskilmálar
-   Staðfest dagsetning afhendingar

Lánardrottinn getur líka bætt við athugasemd eða viðhengi

Á línunum getur lánardrottinn breytt magni og afhendingardagsetningum, bætt við athugasemdum og viðhengjum, hafnað línu, skipt línu með annarri vöru sem er slegið inn sem texti og skipt línu upp í margar afhendingar. Eftir því hvaða breytingar lánardrottinn stingur upp á mun línustaðan hafa aðrar línustöður:
    
-   **Samþykkt með breytingum**
-   **Hafnað**
-   **Sett í staðinn** Í þessu tilfelli verður aukalínu bætt við sem hefur stöðuna **Staðgengill**.
-   **Staðfest** Skipt upp í áætlun Í þessu tilfelli verður að bæta fleiri línum við sem hafa stöðuna **Raða línum**.

Hafi lína engar breytingar er línustaðan **Samþykkt**.

Í svarinu er hægt að sjá áður nefndar línustöður sem tilgreina þær gerðir breytinga sem lánardrottinn gerði. Þar að auki birtast öll breytt svæði sem feitletruð til að hjálpa þér að bera kennsl á breytingarnar.

Hægt er að uppfæra Innkaupapöntun með því að smella á aðgerðina **Vinna uppfærslu á innkaupapöntun** í svarinu eða í einni línu í einu. Vísir, **Hefur uppfærsla á innkaupapöntun verið keyrð?**, í haus og línum gerir kleift að sjá hvort kerfið hefur keyrt hausinn eða línur til að uppfæra innkaupapöntunina með hugsanlegum breytingumm sem eru úr svarinu. Aðeins er hægt að keyra **Keyra uppfærslu innkaupapöntunar** einu sinni á hvern haus eða línu.

Ekki er hægt að uppfæra allar ráðlagðar breytingar í innkaupapöntun. Aðeins uppfærslur í haus og uppfærslur á dagsetningum og magni í línum geta verið uppfærðar sjálfkrafa í innkaupapöntun. Fyrir aðrar breytingar verður að uppfæra innkaupapöntunina handvirkt. Í þessu tilfelli sýnir **Hefur uppfærsla á innkaupapöntunni verið keyrð?** vísirinn **Handvirkar uppfærslur**. Dæmi um breytingu sem á að meðhöndla handvirkt væri þegar lánardrottinn leggur til að skipta línu niður í áætlun.

Lína með stöðuna **Samþykkt** hefur staðfesta afhendingardagsetningu sem verða uppfærðar í innkaupapöntuninni þegar framkvæma á **Keyra uppfærslu innkaupapöntunar**. Athugasemdir og viðhengi færast ekki sjálfkrafa í gildandi innkaupapöntun. Athugið að þegar gildandi innkaupapöntun er uppfærð í gegnum aðgerðina **Keyra uppfærslu á innkaupapöntun** verða viðskiptasamningar ekki endurmetnir í línum innkaupapöntunar.


## <a name="po-statuses-and-versions"></a>Staða og útgáfur innkaupapöntunar
Þessi hluti lýsir ýmsum stöðum sem Innkaupapöntun getur haft fram að þeim tíma þegar hún er staðfest. Hann lýsir einnig á hvaða tímapunkti nýjar útgáfur af innkaupapöntun eru til taks til lánardrottinn. Hegðunin er breytileg eftir því hvort notuð eru breytingarstjórnun fyrir innkaupapantanir. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Útgáfur og stöður ef þú notar ekki breytingastjórnun

Taflan hér að neðan sýnir dæmi um breytingar á stöðu og útgáfum sem Innkaupapöntun gæti farið í gegnum.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aðgerð**                                                               | **Staða og útgáfa**                                                                                                                                       |
| Upprunaleg útgáfa af Innkaupapöntuninni er stofnuð í Finance and Operations. | Staðan er  **Samþykkt**.                                                                                                                                  |
| Innkaupapöntunin er send á lánardrottins.                                            | Útgáfa er skráð í viðmót samstarfs lánardrottna og stöðunni er breytt í **Í Ytri Yfirferð**.                                          |
| Lánardrottinn sendir inn **Samþykkt með breytingum** svarið.                  | Staðan er enn **í Ytri yfirferð**.                                                                                                                  |
| Þú gerir einhverjar breytingar sem lánardrottinn biður um.                  | Stöðu breytt í **Samþykkt**.                                                                                                                        |
| Þú sendir nýja útgáfu af Innkaupapöntuninni lánardrottins.                        | Ný útgáfa er skráð í viðmót samstarfs lánardrottna og stöðunni er breytt í **Í Ytri Yfirferð**.                                      |
| Lánardrottinn samþykkir nýju útgáfuna af IP.                            | Staðan er enn **í Ytri Yfirferð** nema lánardrottnalykill er skilgreindur til að stilla sjálfkrafa Innkaupapöntun á stöðuna **Staðfest** þegar þeir samþykkja það. |


Lánardrottnar þurfa ekki að staðfesta Innkaupapöntun með því að nota viðmót fyrir samstarf lánardrottna. Þeir geta einnig sent skilaboð í tölvupósti eða tilkynnt samþykki Innkaupapöntunarinnar gegnum aðrar rásir. Síðan er hægt að staðfesta pöntunina handvirkt í Finance and Operations. Í þessu tilfelli berst viðvörun um að verið er að staðfesta pöntun jafnvel þótt að það er ekkert svar frá lánardrottni. Innkaupapöntunin birtist síðan í staðfestingarsögu sem opin staðfest pöntun sem hefur ekki svör. Lánardrottinn hefur ekki lengur valkost til að staðfesta eða hafna innkaupapöntun.  


>[!NOTE]
>Athugasemd: Sú útgáfa Innkaupapöntunar sem er tiltæk við önnur ferli í Finance and Operations er alltaf síðasta útgáfa, jafnvel þó að sú útgáfa hafi ekki enn verið skráð í viðmóti fyrir samstarf lánardrottna.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Útgáfur og stöður ef þú notar breytingastjórnun

Ef breytingastjórnun er virkjuð fyrir Innkaupapöntun, fer Innkaupapöntunin í gegnum samþykktarverkflæði til að komast í stöðuna **Samþykkt**. Þetta ferli er ekki sýnilegt lánardrottni.  

Taflan hér að neðan sýnir dæmi um breytingar á stöðu og útgáfu sem Innkaupapöntun gæti farið í gegnum þegar breytingastjórnun er virkjuð. Útgáfan er skráð þegar Innkaupapöntunin er samþykkt, ekki þegar Innkaupapöntunin er send til lánardrottins eða staðfest.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aðgerð**                                                               | **Staða og útgáfa**                                                                                                                                       |
| Upprunaleg útgáfa af Innkaupapöntuninni er stofnuð í Finance and Operations.      | Staðan er **Drög**.  |
| Innkaupapöntunin er send í samþykktarferli. (Samþykktarferlið er innra ferli sem lánardrottinn hefur ekki aðkomu að.)                                                           | Stöðunni er breytt úr **Drög** til **í Yfirferð** til **Samþykki** ef Innkaupapöntuninni er ekki hafnað meðan á samþykktarferlinu stendur. Samþykkt innkaupapöntun er skráð sem útgáfa.           | 
| Innkaupapöntunin er send á lánardrottins.                                                            | Útgáfa er skráð í viðmót samstarfs lánardrottna og stöðunni er breytt í **Í Ytri Yfirferð**.      |
| Þú gerir einhverjar breytingar sem lánardrottinn biður um, annaðhvort handvirkt eða með því að nota aðgerðina í svarinu til að uppfæra innkaupapöntunina.                                                            | Stöðu er breytt aftur í **Drög**.     |
|Innkaupapöntunin er send aftur í samþykktarferlið.                                                |  Stöðunni er breytt úr **Drög** til **í Yfirferð** til **Samþykki** ef Innkaupapöntuninni er ekki hafnað meðan á samþykktarferlinu stendur. Einnig er hægt að skilgreina kerfið þannig að tilteknar breytingar á reitum krefjast ekki endursamþykktar. Í þessu tilfelli fer staðan fyrst í **Drög** og er sjálfkrafa uppfærð í **Samþykkt**. Samþykkta Innkaupapöntunin er skráð sem ný útgáfa.                                         |
|Þú sendir nýja útgáfu af Innkaupapöntuninni lánardrottins.                                                |  Ný útgáfa er skráð í viðmót samstarfs lánardrottna og stöðunni er breytt í **Í Ytri Yfirferð**.                                         |
|Lánardrottinn samþykkir nýju útgáfuna.                                                |  Stöðu er breytt í **Staðfest**, annað hvort sjálfvirkt eða þegar svarið kemur frá lánardrottni og síðan er Innkaupapöntunin staðfest. |

## <a name="share-information-about-consignment-inventory"></a>Deila upplýsingum um vörusendingabirgðir
Ef verið er að nota vörusendingabirgðir, geta lánardrottna notað viðmót fyrir samstarf lánardrottna til að skoða upplýsingar um eftirfarandi síður:

-   **Innkaupapantanir sem notar vörusendingabirgðir** - innkaupapantanir fyrir vörusendingabirgðir eru myndaðar þegar eignarhaldi á birgðum er breytt frá lánardrottninum til fyrirtækis. Innhreyfingarskjal afurða er bókaðar samtímis. Þessum innkaupapantanir vörusendinga birtast aðeins á **Innkaupapantanir sem nota vörusendingabirgðir** síðuna. Þær eru ekki teknar með í **Allar staðfestar innkaupapantanir** síðuna í á **samstarf lánardrottna** kerfiseiningu.
-   **Afurðir sem er tekið við úr vörusendingabirgðum** - Þessi síða inniheldur lista yfir allar færslur þar sem eignarhald afurða hefur verið flutt frá lánardrottni til fyrirtækis. Lánardrottnar geta nota þessar upplýsingar til að reikningsfæra á viðskiptavininn.
-   **Vörusendingarbirgðir á lager** - Þessi síða sýnir vörusendingabirgðir á lager í eigu lánardrottins sem hefur verið móttekið í vöruhúsi þínu.





