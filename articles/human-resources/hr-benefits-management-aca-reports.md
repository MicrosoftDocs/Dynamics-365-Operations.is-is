---
title: Búa til tilkynningar um Affordable Care Act í fríðindastjórnun
description: Þetta efnisatriði lýsir því hvernig fríðindastjórnun rekur upplýsingar sem er greint frá á eyðublaði 1095-B og eyðublaði 1095-C fyrir vinnuveitandaumboð Affordable Care Act (ACA).
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 79bd8e02aeac1be94e735373740cf9508f494a06
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065994"
---
# <a name="generate-aca-reports-in-benefits-management"></a>Búa til ACA-tilkynningar í fríðindastjórnun


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Fríðindastjórnun rekur upplýsingar sem er greint frá á eyðublaði 1095-B og eyðublaði 1095-C fyrir vinnuveitandaumboð Affordable Care Act (ACA). Rétt eins og möguleiki ACA-skýrslugerðar í gamla vinnusvæðinu **Fríðindi**, á þessi virkni aðeins við um lögaðila í Bandaríkjunum.

Til að nota þessa virkni þarf fyrst að kveikja á **Ítarleg fríðindastjórnun**. Frekari upplýsingar, þar á meðal mikilvæg skilyrði fríðindastjórnunar, er að finna í [Virkja eða óvirkja fríðindastjórnun](hr-admin-manage-features.md#enable-or-disable-benefits-management).

> [!IMPORTANT]
> Aðeins er hægt að nota ACA-tilkynningu frá annaðhvort vinnusvæðinu **Fríðindastjórnun** eða gamla vinnusvæðinu **Fríðindi**, en ekki báðum. Til dæmis ef skipt er yfir í fríðindastjórnun er ACA-tilkynning aðeins í boði á vinnusvæðinu **Fríðindastjórnun**, en ekki gamla vinnusvæðinu **Fríðindi**.
>
> Ef skipt er í fríðindastjórnun á miðju skráningarári verður að skilgreina á réttan hátt starfsmannagögn fyrir allt árið í fríðindastjórnun. Þannig er gengið úr skugga um að nákvæmar upplýsingar tilkynningar komi fram fyrir allt árið.

## <a name="getting-started"></a>Hafist handa

Til að rekja upplýsingar fyrir 1095-eyðublöð skal fyrst stofna einn eða fleiri Affordable Care-tryggingaflokka. Þessir flokkar sýna eftirfarandi upplýsingar:

- Tryggingatilboð sem starfsmanni var útvegað
- Hlutdeild starfsmanns í lægstu mánaðarlegu greiðslu iðgjalds, ef kostnaðurinn er fyrir ofan fátæktarmörk
- Örugga höfnin sem er notuð af starfsmanni, ef á við

Affordable Care-tryggingaflokkar auðvelda þér að stjórna þessum upplýsingum fyrir margar starfsmannsfærslur sem eru með sömu skilyrðin. Auðveldlega er hægt að úthluta flokkum á einn eða fleiri starfsmenn.

### <a name="create-or-edit-an-affordable-care-coverage-group"></a>Búa til eða breyta Affordable Care-tryggingaflokk

1. Á vinnusvæðinu **Fríðindastjórnun** skal velja **Affordable Care-tryggingaflokk**.

    ![Val á Affordable Care-tryggingaflokk.](./media/hr-benefits-management-aca-coverage-group.png)

2. Velja skal **Nýr** til að stofna nýjan Affordable Care-tryggingaflokk eða **Breyta** til að breyta fyrirliggjandi flokki.

    ![Að velja nýtt eða breytt.](./media/hr-benefits-management-aca-new.png)

3. Stilltu eftirfarandi reiti.

    | Svæði | lýsing |
    |---|---|
    | Nafn | Færa inn heiti fyrir hópinn. |
    | lýsing | Færa inn lýsingu á flokknum. |
    | Tryggingatilboð | Tryggingin sem boðin er starfsmanni, maka og skjólstæðinga. |
    | Kostnaðarhlutdeild starfsmanns | Upphæðin sem starfsmaður ber ábyrgð á. |
    | Viðeigandi hluti 4980H um örugga höfn | 4980H fyrir örugga höfn eða afléttingarkóði umbreytingar. |
    | Upphafsmánuður áætlunar | Veljið almanaksmánuðinn þegar ár fríðindaáætlunar hefst. |
    | Flokkur gildir frá | Fyrsta gilda dagsetning þessarar færslu. |
    | Flokkur gildir | Síðasta gilda dagsetning þessarar færslu. Ef engin lokadagsetning er til staðar skal slá inn **Aldrei**. |

    ![Stofnun þekjuflokks.](./media/hr-benefits-management-aca-new-group.png)

4. Veldu **Vista**.

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a>Úthluta mörgum starfsmönnum á Affordable Care-tryggingaflokk

1. Á vinnusvæðinu **Fríðindastjórnun** skal velja **Affordable Care-tryggingaflokk**.
2. Veljið flokkinn sem úthluta á starfsmönnum í.
3. Veljið **Fjöldaúthlutun**.

    ![Fjöldaúthlutun valin.](./media/hr-benefits-management-aca-mass-assignment.png)

4. Veljið starfsmenn af listanum og veljið síðan **Úthluta**.

    ![Völdum starfsmönnum úthlutað í flokk.](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a>Vinna með margar útgáfur af tryggingarmöguleikum

Hægt er að viðhalda mörgum útgáfum í hvaða tryggingaflokki sem er. Þegar eitthvað breytist í fyrirtækinu eða fríðindin sem boðið er upp á er hægt að halda upplýsingum um flokkinn uppfærðum án þess að þurfa að stofna nýjan flokk og endurúthluta starfsmönnum í hann.

Þegar búið er að stofna Affordable Care-tryggingaflokka er hægt að úthluta mörgum starfsmönnum í hann í einu. Einnig er hægt að úthluta einum starfsmanni í einu í flokkana og gefa upp hvort ACA-upplýsingar eru raktar og tilkynntar.

Ef ekki þarf að rekja og tilkynna ACA-upplýsingar fyrir starfsmann, er hægt að stilla valkostinn **Tilkynna tryggingu** á **Nei**. Til dæmis gætu verið starfsmenn í hlutastarfi sem þurfa ekki ACA-tilkynningu.

### <a name="override-default-values-for-an-employee"></a>Hnekkja sjálfgefnum gildum fyrir starfsmann

Fyrir starfsmenn sem er úthlutað í Affordable Care-tryggingaflokk er hægt að breyta eftirfarandi valkostum fyrir hvaða mánuð sem er sem þarf önnur gildi:

- Tryggingatilboð
- Kostnaðarhlutdeild starfsmanns
- Viðeigandi hluti 4980H um örugga höfn

> [!NOTE]
> Fyrir ACA-tilkynningar 2020 þarf að tilkynna bæði póstnúmer vinnustaðar og heimilis á eyðublað 1095-C. Gildin eru sjálfkrafa fyllt út í samræmi við núgildandi virkar staðsetningar. Ef önnur hvor staðsetningin var önnur einhvern hluta ársins þarf að hnekkja gildinu. Aðeins er fyllt út í reitinn **Póstnúmer** (lína 17) á tilkynningu 1095-C ef kóðinn **Tryggingatilboð** inniheldur **1L** til **1Q** eins og eftirfarandi:
>
> - **1L, 1M eða 1N:** Póstnúmer aðalaðseturs
> - **1O, 1P, 1Q:** Póstnúmer aðalvinnustaðar

Til að færa inn undantekningar fyrir gildi Affordable Care-tryggingaflokks skal fylgja þessum skrefum.

1. Á vinnusvæðinu **Starfsmannastjórnun** skal velja **Tenglar** og síðan velja **Starfsmenn**.
2. Veljið starfsmanninn í listanum.
3. Í flipanum **Starf**, í hlutanum **Frekari upplýsingar**, skal velja **Affordable Care-trygging**.

    ![Valkostum breytt fyrir einn starfsmann.](./media/hr-benefits-management-aca-change-single-employee.png)

4. Veljið **Breyta**.
5. Fyrir hvern mánuð sem krefst breytinga skal velja gátreitinn **Hnekkja sjálfgildi** og síðan breyta hinum gildunum eftir þörfum.

    ![Sjálfgefnum gildum hnekkt.](./media/hr-benefits-management-aca-override-default.png)

6. Veldu **Vista**.

## <a name="report-health-care-coverage"></a>Tilkynna heilbrigðistryggingu

Fylgjast verður með sjálftryggðri heilbrigðistryggingu sem vinnuveitandi greiðir fyrir starfsmenn í fullu starfi og hlutastarfi. Hafið með hvern starfsmann auk skjólstæðinga hans á eyðublaði 1095-C fyrir mánuðina sem þeir eru tryggðir.

Til að gefa til kynna hvort tilkynna verður fríðindaáætlun skal fylgja þessum skrefum.

1. Á vinnusvæðinu **Fríðindastjórnun** skal velja **Fríðindaáætlanir**.
2. Veljið fríðindaáætlunina sem á að tilkynna.
3. Veljið **Breyta**.
4. Stillið valkostinn **Tilkynningarskylt samkvæmt Affordable Care Act** á **Já**.

    ![Sjúkratrygging tilkynnt.](./media/hr-benefits-management-aca-report-coverage.png)

5. Veldu **Vista**.

Ef starfsmaður velur heilbrigðistryggingu fyrir skjólstæðing er tryggingartímabil skjólstæðingsins ákvarðað af dagsetningunni þegar hann var skráður eða fjarlægður. Tryggingadagsetningar fyrir skjólstæðing eru sjálfkrafa reiknaðar út frá tímabilinu þegar skjólstæðingurinn var tryggður og virkur í áætlun á skráningarárinu.

## <a name="generate-1095-b-and-1095-c-forms"></a>Búa til eyðublöð 1095-B og 1095-C

Hægt er að búa til eyðublöðin ACA 1095-B og 1095-C og síðan dreifa þeim til allra starfsmanna þinna. Einnig er hægt að búa rafrænt til eyðublöð 1095-C og samsvarandi 1094-C skilaskrár til að senda á bandarísk skattyfirvöld (IRS).

1. Á vinnusvæðinu **Fríðindastjórnun** skal velja **Eyðublað ACA 1095-B** eða **Eyðublað ACA 1095-C**.
2. Breytið færibreytum eins og krafist er og veljið svo **Í lagi**.

    > [!NOTE]
    > Ef eyðublað 1095-C er prentað fyrir fleiri en 500 starfsmenn, færðu fleiri en eina PDF-skrá afhenta. Mælt er með því að auka gildið í reitnum **Hámarksstærð skráar í megabætum** á síðunni **Færibreytur skjalastjórnunar** í **150**. (Til að opna þessa síðu á fljótlegan hátt skal nota leitarsvæðið á yfirlitsstikunni.)
    >
    > ![Hámarksstærð skráar breytt.](./media/hr-benefits-management-aca-maximum-file-size.png)

3. Til að athuga stöðu skýrslnanna og skoða þær skal nota leitarsvæðið á yfirlitsstikunni til að opna síðuna **Rafræn skýrslugerðarvinnsla**.

    ![Leitað að síðu rafrænnar skýrslugerðarvinnslu.](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. Veljið skýrslurnar sem á að skoða og veljið síðan **Sýna skrár**.

    ![Skrár sýndar.](./media/hr-benefits-management-aca-show-files.png)

5. Veljið **Opna**.

    ![Skrá opnuð.](./media/hr-benefits-management-aca-open-file.png)

6. Úr tilkynningastikunni sem birtist neðst í vafraglugganum skal opna zip-skrána og síðan velja skýrsluna. Hægt er að skoða eða prenta út PDF-skrána.

    ![Sýnishorn af eyðublaði 1095-C.](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a>Skoða upplýsingar um ACA-tryggingu

Síðan **Affordable Care-trygging fyrir starfsmann** sýnir eftirfarandi upplýsingar:

- Starfsmenn sem úthlutað er í hvern tryggingaflokk
- Starfsmenn sem þurfa ekki að vera í skýrslu
- Óúthlutaða starfsmenn

Til að skoða þessar upplýsingar skal fylgja þessum skrefum.

1. Á vinnusvæðinu **Fríðindastjórnun** skal velja **Affordable Care-trygging fyrir starfsmann**.
2. Í reitnum **Heiti flokks** skal velja flokk.

    ![ACA-trygging skoðuð.](./media/hr-benefits-management-aca-view-coverage.png)

Ef einhverjum sjálfgefnum gildum úr Affordable Care-tryggingaflokknum hefur verið hnekkt, birtist stjarna við hliðina á gildinu sem var breytt. Ef gildin fyrir alla 12 mánuðina eru þau sömu og hefur ekki verið hnekkt birtist gildið í dálknum **Allir 12 mánuðirnir**.

Hægt er að skoða starfsmenn sem eru merktir sem ekki ACA-tilkynningaskyldir og þurfa ekki eyðublað 1095-C. Í reitnum **Sía eftir** skal velja **Er ekki ACA-tilkynningaskylt**.

Hægt er að skoða starfsmenn sem ekki er búið að úthluta í flokk eða er úthlutað í útrunninn flokk. Í **Sía eftir** skal velja **Óúthlutaður eða útrunninn flokkur**.

### <a name="export-to-excel"></a>Flytja út í Excel

Til að flytja út einhvern listanna í Microsoft Excel skal fylgja þessum skrefum.

1. Veljið hnappinn **Opna í Microsoft Office**.
2. Veljið **Bráðabirgðatafla HCM Human Resources til notkunar innanhúss**.
3. Veljið **Hlaða niður**.

### <a name="view-aca-reportable-dependents"></a>Skoða skjólstæðinga sem eru ACA-tilkynningaskyldir

Ef þarf að tilkynna tryggða einstaklinga vegna þess að þú býður upp á sjálfstryggða tryggingu, er hægt að skoða skjólstæðinga sem eru tryggðir undir fríðindaáætlunum sem eru merktar sem **ACA-tilkynningaskylt**. Á aðgerðasvæðinu skal velja **Skoða tryggingar skjólstæðinga**.

![Tryggingar skjólstæðinga skoðaðar.](./media/hr-benefits-management-aca-view-dependent-coverage.png)

Upplýsingar um tryggingu skjólstæðinga starfsmanns eru sýndar.

![Tryggingar skjólstæðinga.](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> Síðan sýnir aðeins fríðindaáætlanir sem eru merktar sem **ACA-tilkynningaskyldar**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
