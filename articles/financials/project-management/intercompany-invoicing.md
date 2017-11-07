---
title: "reikningsfærsla innan samstæðu"
description: "Þessi grein veitir upplýsingar og dæmi um reikningsfærslu innan samstæðu fyrir verk í Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfu."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0e6eb4cb0192da40b4d064d955feb75b91f87bbb
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="intercompany-invoicing"></a>Reikningsfærsla innan samstæðu

[!include[banner](../includes/banner.md)]


Þessi grein veitir upplýsingar og dæmi um reikningsfærslu innan samstæðu fyrir verk í Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfu.

Fyrirtæki þitt gætu haft margar deildir, dótturfyrirtæki og annarra lögaðila sem flytja afurðir og þjónustu milli sín fyrir verk. Lögaðili sem sem veitir þessi þjónustu eða afurðir kallast *lögaðili sem lánar* og lögaðilann sem fær þjónustuna eða vörurnar er kallað *lögaðili sem fær lánað*. 

Eftirfarandi skýringarmynd sýnir í dæmigerðum aðstæðum þar sem tveir lögaðilar deila SI FR (lögaðili sem fær lánað) og SI USA (Lögaðili sem er lánveitandi) tilföngum fyrir verk sem skal afhenda til viðskiptavinar A. Fyrir þessar aðstæður er SI FR samningsbundið til að afhenda vinnu til viðskiptavinarins A. 

[![Dæmi um reikningsfærslu innan samstæðu](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Markmiðið er að gera kostnaðarstýringu , tekjuskráningu, skatta og flutningsverð fyrir verkfærslur innan samstæðu í Dynamics AX sveigjanlegri og öflugri. Þar að auki er eftirfarandi geta í boði:

-   Stofna reikninga viðskiptavina gagnvart verk í lögaðili sem fær lánað með því að nota vinnukort innan samstæðu, útgjöld og reikningar í lögaðila sem lánar.
-   Styðja skattaútreikninga og óbeinan kostnað.
-   Fresta tekjuskráningu hjá lögaðili sem lánar og þegar lögaðili sem fær lánað á að viðurkenna kostnaðinn.
-   Safna upp tekjum fyrir verk í vinnslu (VÍV) í lögaðilanum sem lánar.
-   Setja upp flutningsverð sem geta byggt á mismunandi verðflokkar. Hér eru nokkur dæmi:
    -   **Magn** – upphæðin sem færð er inn í á **Verðlagning** reitnum er raunverulegur kostnaður á magn eða einingu.
    -   **Upphæð gjalda** -  verð/kostnaður á færslu plús upphæð gjalda sem þú færðir inn í reitnum **verðlagning**
    -   **Gjaldaprósenta** -  Flutningsverð er verð/kostnaður á færslu margfaldað með gjaldprósentu sem þú færðir inn í reitnum **verðlagning**.
    -   **Prósenta af söluverði** – prósentu af söluverðinu sem er flutt í lögaðilanum sem lánar.
    -   **Upphæð fyrir neðan söluverð** – upphæðin sem er lögaðili sem fær lánað heldur eftir af söluverðinu fyrir flutning í lögaðilanum sem lánar.
    -   **Framlegðarhlutfall** – númerið sem færð er inn í á **Verðlagning** er framlegðarhlutfall sem er sýnd sem prósenta af söluverði.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Dæmi 1: Setja upp færibreytur fyrir reikningsfærsla innan samstæðu
Í þessu dæmi er USSI lögaðili sem lánar, og tilföng hennar eru að skrá tíma gagnvart lögaðila sem lánar, FRSI, sem á samninginn við endanlegan viðskiptavin. Vinnustundur og útgjöld sem USSI starfsmenn skýra frá má taka með í reikningi sem FRSI myndar. Þar að auki er til staðar þriðji uppruni færslna sem geta komið frá lögaðilanum sem lánar (USSI í þessu dæmi) þegar hún veitir samnýtta þjónustu lánardrottna fyrir dótturfyrirtæki (til dæmis FRSI) og sendir síðan þann kostnað á verkefni innan þeirra dótturfyrirtækjum. Öllum samsvarandi reikningsskjölum og skattaútreikningum er lokið af Finance and Operations. 

Í þessu dæmi verður FRSI að vera viðskiptavinur USSI lögaðila, og USSI verður að vera lánardrottins í FRSI-lögaðila . Síðan er hægt að setja upp tengsl innan samstæðu milli tveggja lögaðila. Eftirfarandi ferli sýnir hvernig á að setja upp færibreytur þannig að bæði lögaðila geta taka þátt í reikningsfærslu innan samstæðu .

1.  Setja upp FRSI sem viðskiptavin í USSI lögaðila, og setja upp USSI sem lánardrottinn í FRSI-lögaðila. Það eru þrír komustaðir fyrir skref sem þarf fyrir þetta verk.
    | Skref | Aðgangsstaður                                                                       | lýsing   |
    |------|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Lista fyrir    | Í USSI smellið á **Viðskiptakröfur** &gt; **Viðskiptavinir** &gt; **Allir viðskiptavinir**. | Búa til nýja færslu viðskiptavinar fyrir FRSI og veljið viðskiptavinaflokkur.                                                                                                                                                                                                                           |
    | B    | Í FRSI, smellið á **Viðskiptaskuldir** &gt; **Lánardrottnar** &gt; **Allir lánardrottnar**.        | Búa til nýja færslu lánardrottins fyrir USSI, og veljið svo lánardrottnaflokkur                                                                                                                                                                                                                               |
    | K    | Í FRSI, Opna færslu lánardrottins sem nýverið var stofnuð.                            | Í Aðgerðasvæði, á flipanum **Almennt** í flokknum **Uppsetning** er smellt á **sinnan samstæðu**. Á á **Innan samstæðu** á síðunni á **viðskiptasamningur** flipanum, skal stilla sleðann **Virkt** til **Já**. Í **fyrirtæki Viðskiptavinar** reitnum skal velja færslu viðskiptavinar sem var stofnaður í skrefi A. |

2.  Smellið á **Verkefnastjórnun og bókhald** &gt; **Uppsetning** &gt; **færibreytur verkefnastjórnunar og bókhalds**, og smellið svo á flipann **innan samstæðu**. Aðferðin sem þú notar til að setja upp færibreytur fer eftir því hvort þú ert lögaðili sem fær lánað eða lögaðili sem lánar.
    -   Ef þú ert lögaðili sem fær lánað, skal velja innkaupategund sem á að nota til að jafna reikninga lánardrottins, sem eru myndaðar sjálfkrafa.
    -   Ef þú ert lögaðili sem lánar, fyrir hvern lögaðila sem fær lánað, veldu sjálfgefna verktegund fyrir hverja færslugerð. Verktegundir eru notaðar fyrir skattskilgreiningu þegar tegund reikningsfærslna í samstæðufærslum eru eingöngu til hjá lögaðili sem fær lánað. Hægt er að velja að safna upp tekjum fyrir færslur fyrir samstæðufærslur. Þessi uppsöfnun er gert þegar færslur eru bókaðar, og það er síðan bakfærðar þegar samstæðureikningur er bókaður.

3.  Smellið á **Verkefnastjórnun og bókhald** &gt; **Uppsetning** &gt; **Verð** &gt; **Flutningsverð**.
4.  Velja gjaldmiðil, færslugerð og verðlíkan innanhússverðs. Gjaldmiðill sem notaður er á reikningi er sá gjaldmiðill sem skilgreindur er í færslu viðskiptavinar fyrir lögaðili sem fær lánað í lögaðilanum sem lánar. Gjaldmiðill er notaður til að jafna færslur í töflu innanhússverðs.
5.  Smellt er á **Fjárhagur** &gt; **Uppsetning bókunar** &gt; **Samstæðulyklar** og sett upp vensl fyrir USSI og FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Dæmi 2: Stofnað og bókað vinnukort innan samstæðu
USSI, lögaðilanum sem lánar, verður að stofna og bóka vinnukort fyrir verk úr FRSI, lögaðili sem fær lánað. Það eru tveir komustaðir fyrir skref sem þarf fyrir þetta verk.

| Skref | Aðgangsstaður                                                                       | lýsing                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lista fyrir    | **Verkefnastjórnun og bókhald** &gt; **Vinnukort** &gt; **Öll vinnukort** | Stofna nýtt vinnukort Í línu vinnukorts í á **lögaðila** svæðinu, veljið **FRSI**. Í því **Verkkenni** svæðinu, veljið verkið í FRSI . Færið inn vinnustundir fyrir hvern dag vikunnar |
| B    | Síðan **vinnukort**                                                                | Eftir að verkflæðið keyrir, skal bóka vinnukort, og skrá niður fylgiskjalsnúmer.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Dæmi 3: Stofnað og bókað lánardrottinsreikningur innan samstæðu
USSI, lögaðilanum sem lánar, verður að stofna og bóka lánardrottinsreikningur innan samstæðu fyrir verk úr FRSI, lögaðili sem fær lánað. Þessi reikningur lánardrottins sýnir útselda vinnu og kostnað sem var framkvæmdur af lánardrottnar sem sem fá borgað frá USSI. Það eru tveir komustaðir fyrir skref sem þarf fyrir þetta verk.

| Þrep | Aðgangsstaður                                                                                      | lýsing                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lista fyrir    | **Viðskiptaskuldir** &gt; **Reikningar** &gt; **Opna reikning lánardrottins** &gt; **nýr reikningur lánardrottins** | Stofna nýjan reikning lánardrottins og færa inn þjónustu sem voru keypt fyrir hönd verkefnis á vegum FRSI.                                                                                                                                                                                  |
| B    | Síðan **reikning lánardrottins**.                                                                      | Færið inn lína sem standa fyrir útselda þjónustu fyrir hönd FRSI. Á **Línuupplýsingar** flýtiflipi, á **Verks** flipanum fyrir reikningslínu á **fyrirtæki Verkefnis** reit, skal færa inn **FRSI**. Færið inn verkefni og samsvarandi upplýsingar. Bóka síðan reikningur lánardrottins |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Dæmi 4: Stofnað og bókað samstæðureikningur
USSI, lögaðilanum sem lánar, verður að stofna og bóka samstæðureikningur. Það eru tveir komustaðir fyrir skref sem þarf fyrir þetta verk.

| Skref | Aðgangsstaður                                                                                             | lýsing                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Lista fyrir    | **Verkefnastjórnun og bókhald** &gt; **Verkreikningar** &gt; **samstæðureikningur viðskiptavinar**.  | Smellið á **Nýtt** til að opna í **Stofna samstæðureikning** síðu.                                                                                  |
| B    | **Verkefnastjórnun og bókhald** &gt; **Verkreikningar** &gt; **samstæðureikningar viðskiptavinar**. | Á við **Stofna samstæðureikning** síðunni skal færa inn lögaðila, tilgreina færsluna sem á að taka með og smellið síðan á **Leit**. |
| K    | **Verkefnastjórnun og bókhald** &gt; **Verkreikningar** &gt; **samstæðureikningar viðskiptavinar**. | Velja færslur til að reikningsfæra eða smellið á **Velja allt** til að reikningsfæra allar færslur í listanum og smellið síðan á **í lagi**.                  |
| D    | Síðan **samstæðureikningur**                                                                       | Reikningstillaga samstæðuviðskiptavinar er sýnd.                                                                                             |
| E    | Síðan **samstæðureikningur**                                                                       | Smella  **bóka.**                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Dæmi 5: Bóka reikning lánardrottins og reikningsfæra á viðskiptavininn
Þegar lögaðilanum sem lánar, USSI, bókar samstæðureikningur viðskiptavinar, er samsvarandi reikningur lánardrottins í bið stofnuð í lögaðili sem fær lánað, FRSI. Eftir að þessum reikningi lánardrottins er bókaður, reikningsfærir FRSI einnig viðskiptavin verks fyrir vinnustundir sem USSI færði inn. Það eru þrír komustaðir fyrir skref sem þarf fyrir þetta verk.

| Þrep | Aðgangsstaður                                                                                        | lýsing                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Lista fyrir    | **Viðskiptaskuldir** &gt; **Reikningar** &gt; **Reikningar frá lánardrottni í bið**                            | Skoða reikning til að staðfesta að gildi vinnukorts eru teknar með og bóka síðan reikning lánardrottins.                  |
| B    | **Verkefnastjórnun og bókhald** &gt; **Verkreikningar** &gt; **Tillögur um verkreikning** | Búa til nýja verkreikning fyrir verkið, og staðfesta að tímafærslur sem voru bókaðar birtast.            |
| K    | Síðan **verkreikningur**                                                                       | Velja verkreikning, og smellið síðan á **Skoða upplýsingar** til að yfirfara kostnað og upphæð sölu. Bóka síðan reikninginn. |


Nánari upplýsingar er að finna í [Skilgreina reikningagerð fyrir verk innan samstæðu](tasks/configure-intercompany-project-invoicing.md)



