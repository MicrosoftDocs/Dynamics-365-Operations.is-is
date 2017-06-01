---
title: "Samstarf með lánardrottnum í gegnum gátt lánardrottins"
description: "Þetta efnisatriði útskýrt hvernig innkaupastjórar geta notað Gátt lánardrottins til að vinna með ytri lánardrottnum meðan á staðfestingarvinnslu innkaupapöntunar stendur. Upplýsingarnar gildir aðeins um 2016 Febrúar &amp; 2016 Maí útgáfum Dynamics AX."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ef47cd32d78ea28496c014ed4537008159a05691
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="collaborate-with-vendors-by-using-the-vendor-portal"></a>Samstarf með lánardrottnum í gegnum gátt lánardrottins

[!include[banner](../includes/banner.md)]


Þetta efnisatriði útskýrt hvernig innkaupastjórar geta notað Gátt lánardrottins til að vinna með ytri lánardrottnum meðan á staðfestingarvinnslu innkaupapöntunar stendur. Upplýsingarnar gildir aðeins um 2016 Febrúar &amp; 2016 Maí útgáfum Dynamics AX.

Upplýsingarnar í þessu efnisatriði gildir aðeins um 2016 Febrúar og 2016 Maí útgáfum Dynamics AX. Virknin gátt Lánardrottins hefur verið skipt út fyrir virknina aukið samstarf lánardrottna í Dynamics 365 for Operations útgáfa 1611. Nánari upplýsingar um uppsetningu öryggis fyrir samstarf lánardrottna sjá [Uppsetning og viðhald samstarfs lánardrottna](vendor-collaboration-work-external-vendors.md).  

Gátt Lánardrottins er hönnuð fyrir lánardrottna sem ekki hafa rafræn gagnaskipti (EDI) samþætt við Microsoft Dynamics AX til að skiptast á upplýsingum um innkaupapöntun (PO). Gáttin leyfir innkaupastjórum að senda innkaupapöntun til lánardrottins og fá svarið Staðfest eða Hafnað beint í Dynamics AX.  

Mögulegt er að skilgreina ferli svo staðfesting frá lánardrottni staðfesti sjálfkrafa pöntun. Þetta þýðir að eftirfylgni er aðeins stundum þörf, þegar pöntun er hafnað eða ef staðfesting lánardrottins er skráð sem svar en staða Innkaupapöntunar er ekki uppfærð í **Staðfest** vegna vandamáls í staðfestingarferli.

## <a name="po-confirmation-and-rejection"></a>Staðfesting og höfnun Innkaupapöntunar.
Innkaupapantanir eru undirbúnar í Dynamics AX. Þegar Innkaupapöntun sem hefur stöðuna **Samþykkt**, skal senda hana til lánardrottins með því að mynda staðfestingarbeiðni. Ef óskað er að beina athygli lánardrottins að nýrri innkaupapöntun er einnig hægt að senda Innkaupapöntunina með tölvupósti með því að nota prentstjórnunarkerfið. Innkaupapöntun birtist í gátt Lánardrottins með valkost fyrir lánardrottna til að staðfesta eða hafna henni. Lánardrottinn getur líka bætt við athugasemdum til að gefa upplýsingar, eins og breytingar á Innkaupapöntun.  

Í gátt Lánardrottins getur lánardrottinn séð pöntunarlínur. Þessar línur sýna upplýsingar eins og ytri afurðarnúmer, víddir, upplýsingar um verð, magn, dagsetningu afhendingar, og afhendingaraðsetur. Lánardrottinn getur myndað skýrslu sem sýnir upplýsingar innkaupapöntunar og einnig heildarverð. Gjöld sem eiga við lánardrottin birtast ef lánardrottinn smellir á **Gjöld** hnappinn í haus eða línum. Lánardrottna geta flytja inn upplýsingar um Innkaupapöntun í sína eigin kerfið með því að nota í **Útflutning í Excel** virkni.  

Taflan hér að neðan sýnir dæmigerð upplýsingaskipti, eftir því hvernig lánardrottinn svarar þegar þú sendir innkaupapöntun til staðfestingar.

| Gerð svars                                                                                                  | Niðurstaða                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lánardrottinn staðfestir pöntun. Kerfið er stillt á að staðfesta sjálfvirkt Innkaupapöntun þegar lánardrottinn staðfestir.    | Staða pöntunar er uppfærð í **Staðfest**. Ef eitthvað kemur í veg fyrir að pöntun sé uppfærð, þá verður svar lánardrottins enn skráð sem **Staðfest** en innkaupapöntunin er áfram í stöðunni **Í ytri yfirferð**.                                                                       |
| Lánardrottinn staðfestir pöntun. Kerfið er ekki stillt á að staðfesta sjálfvirkt Innkaupapöntun þegar lánardrottinn staðfestir. | Svar lánardrottins er skráð sem **Staðfest** en innkaupapöntunin er áfram í stöðunni **Í ytri yfirferð**.                                                                                                                                                                                      |
| Lánardrottinn hafnar pöntun.                                                                                     | Svar lánardrottins er skráð sem **Hafnað** og innkaupapöntunin er áfram í stöðunni **Í ytri yfirferð**. Höfnunin er móttekin með ástæðu og tillögu um breytingu, svo sem aðra afhendingardagsetningu. Innkaupapöntun er uppfærð og ný útgáfa send til staðfestingar. |

## <a name="changes-to-a-po"></a>Breytingar á innkaupapöntun
Þegar breyta þarf Innkaupapöntun sem er þegar búið að staðfesta er hægt að senda nýja Innkaupapöntun til lánardrottins í gegnum Gátt lánardrottins. Ný Innkaupapöntun verður með viðskeyti til að gefa til kynna að það sé breytt útgáfa af Innkaupapöntun sem var áður í gangi. Gátt Lánardrottins gerir lánardrottnum kleift að rekja sögu hverjar pöntunar. Áður staðfesta útgáfa Innkaupapöntunarinnar mun vera í lista yfir staðfestar Innkaupapantanir þar til ný Innkaupapöntun hefur verið staðfest.  

Þegar hætt er við Innkaupapöntun er stöðu breytt aftur í **Samþykkt**. Þú þarft að senda Innkaupapöntunina aftur til lánardrottins í gegnum Gátt lánardrottins þannig að lánardrottinn get staðfest eða hafnað ógildingunni. Eftir að ógildingin er staðfest birtist Innkaupapöntunin í lista lánardrottins yfir staðfestar Innkaupapantanir sem **Hætt við**.

## <a name="versions-status-transitions-and-change-management"></a>Útgáfur, stöðubreytingar og stjórnun breytinga
Þegar Innkaupapöntun er send til lánardrottins er hún er skráð í kerfinu sem tiltekin útgáfa innkaupapöntunar og staðan breytist úr **Samþykkt** í **Í Ytri Yfirferð**. Ef Innkaupapöntuninni er breytt síðar er ný útgáfa af Innkaupapöntuninni stofnuð og staðan breytist aftur í **Samþykkt** (eða í **Drög** ef breytingastjórnun er virkjuð).  

Taflan hér að neðan sýnir dæmi um breytingar á stöðu og útgáfum sem Innkaupapöntun gæti farið í gegnum.

| Aðgerð                                                   | Staða og útgáfa                                                                                    |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Upprunaleg útgáfa af Innkaupapöntuninni er stofnuð í Dynamics AX. | Staðan er  **Samþykkt**.                                                                           |
| Innkaupapöntunin er send á Gátt lánardrottins.                     | Útgáfa er skráð í Gátt lánardrottins og stöðunni er breytt í **Í Ytri Yfirferð**.    |
| Þú gerir einhverjar breytingar sem lánardrottinn biður um.  | Stöðu breytt aftur í **Samþykkt**.                                                            |
| Þú sendir nýja útgáfu af Innkaupapöntuninni á Gátt lánardrottins. | Ný útgáfa er skráð í Gátt lánardrottins og stöðunni er breytt í **Í Ytri Yfirferð**. |
| Lánardrottinn samþykkir nýju útgáfuna.           | Stöðu er breytt aftur í **Samþykkt**.                                                                |

Til að sjá útgáfur af Innkaupapöntunum sem hafa verið sendar lánardrottni og svör hans, farið í **Færslubækur** &gt; **Staðfestingarbeiðnir** úr innkaupapöntuninni.  

Pantanir sem hafa verið sendar til lánardrottins til svars og hafa stöðuna **Í ytri Yfirferð** birtast annað hvort í listanum **Innkaupapantanir sem eru sendar í Gátt lánardrottins, beðið eftir svari** eða í listanum **Innkaupapantanir sendar í Gátt lánardrottins, svar krefst aðgerða**. Þegar pöntun er breytt sem hefur verið send til lánadrottna, svo að staðan breytist aftur í **Samþykkt**, birtist hún ekki lengur í þessum listum. Til að sjá hvort það hafa áður komið svör frá lánardrottni er smellt á **Færslubækur** &gt; **Staðfestingarbeiðnir**.  

Lánardrottnar þurfa ekki að staðfesta Innkaupapöntun í Gátt lánardrottins. Þeir geta einnig sent skilaboð í tölvupósti eða tilkynnt samþykki Innkaupapöntunarinnar gegnum aðrar rásir. Síðan er hægt að staðfesta pöntunina handvirkt í Dynamics AX. Í þessu tilfelli berst viðvörun um að verið er að staðfesta pöntun jafnvel þótt að það er ekkert svar frá lánardrottni. Innkaupapöntunin birtist síðan í staðfestingarsögu í Gátt lánardrottins sem opin staðfest pöntun sem hefur ekki svör. Til viðbótar við þetta hefur lánardrottinn ekki lengur valkost til að staðfesta eða hafna innkaupapöntun.  

**Athugasemd:** Sú útgáfa Innkaupapöntunar sem er tiltæk við önnur ferli í Dynamics AX er alltaf síðasta útgáfa, jafnvel þó að sú útgáfa hafi ekki enn verið skráð.

### <a name="change-management"></a>breytingastjórnun

Ef kveikt hefur verið á breytingastjórnun fyrir Innkaupapöntun, fer Innkaupapöntunin í gegnum samþykktarverkflæði til að komast í stöðuna **Samþykkt**. Þetta ferli er ekki sýnilegt lánardrottni.  

Þegar kveikt hefur verið á breytingastjórnun fyrir Innkaupapöntun, er útgáfan skráð þegar Innkaupapöntunin er samþykkt, ekki þegar Innkaupapöntunin er send til lánardrottins eða staðfest.  

Taflan hér að neðan sýnir dæmi um breytingar á stöðu og útgáfu sem Innkaupapöntun gæti farið í gegnum þegar breytingastjórnun er virkjuð.

| Aðgerð                                                                                                        | Staða og útgáfa                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Upprunaleg útgáfa af Innkaupapöntuninni er stofnuð í Dynamics AX.                                                      | Staðan er **Drög**.                                                                                                                                                                                                                                                                                                                                                                    |
| Innkaupapöntunin er send í samþykktarferli. (Þetta er innra ferli sem lánardrottinn er ekki hluti af.) | Stöðunni er breytt úr **Drög** til **Í Yfirferð** til **Samþykki** ef Innkaupapöntuninni er ekki hafnað meðan á samþykktarferlinu stendur. Samþykkt innkaupapöntun er skráð sem útgáfa.                                                                                                                                                                                                                     |
| Innkaupapöntunin er send á gátt Lánardrottins                                                                           | Útgáfa er skráð í Gátt lánardrottins og stöðu er breytt í **Í Ytri Yfirferð**.                                                                                                                                                                                                                                                                                        |
| Þú gerir einhverjar breytingar sem lánardrottinn biður um.                                                       | Stöðu er breytt aftur í **Drög**.                                                                                                                                                                                                                                                                                                                                                    |
| Innkaupapöntunin er send aftur í samþykktarferlið.                                                            | Stöðunni er breytt úr **Drög** til **í Yfirferð** til **Samþykki** ef Innkaupapöntuninni er ekki hafnað meðan á samþykktarferlinu stendur. Einnig er hægt að skilgreina kerfið þannig að breytingar krefjast ekki endursamþykktar. Í þessu tilfelli fer staðan fyrst í **Drög** og er sjálfkrafa uppfærð í **Samþykkt**. Samþykkta Innkaupapöntunin er skráð sem ný útgáfa. |
| Þú sendir nýja útgáfu af Innkaupapöntuninni á Gátt lánardrottins.                                                      | Nýja útgáfan er skráð í Gátt lánardrottins og stöðu er breytt í **Í Ytri Yfirferð**.                                                                                                                                                                                                                                                                                    |
| Lánardrottinn samþykkir nýju útgáfuna.                                                                | Stöðu er breytt í **Staðfest**, annað hvort sjálfvirkt eða þegar svarið kemur frá lánardrottni og síðan er Innkaupapöntunin staðfest.                                                                                                                                                                                                                                                     |
<a name="see-also"></a>Sjá einnig
--------

[Skilgreining öryggis fyrir Notendur samstarfs lánardrottna ](configure-security-vendor-portal-users.md)

[Vinnusvæði fyrir reikningsfærslur fyrir samstarf lánardrottna](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace)




