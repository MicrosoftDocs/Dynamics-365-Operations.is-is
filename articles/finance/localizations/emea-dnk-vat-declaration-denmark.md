---
title: VSK-skýrsla (Danmörk)
description: Í þessari grein er lýst hvernig á að setja upp og búa til virðisaukaskattsskýrslu fyrir Danmörku.
author: AdamTrukawka
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: a47b2b98d86daf50876c783f879362ec1addb579
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272141"
---
# <a name="vat-declaration-denmark"></a>VSK-skýrsla (Danmörk)

[!include [banner](../includes/banner.md)]

Í þessari grein er lýst hvernig virðisaukaskattsskýrsla er sett upp í Danmörku og hún forskoðuð í Microsoft Excel.

Til að búa skýrsluna til sjálfkrafa þarf fyrst að búa til nógu marga VSK-kóða til að halda sérstakt VSK-bókhald fyrir hvern glugga í VSK-skýrslunni. Auk þess, í forritstengdum færibreytum rafræns skýrslugerðarsniðs fyrir VSK-skýrsluna, skal tengja VSK-kóða við uppflettiniðurstöður fyrir gluggana í VSK-skýrslunni.

Fyrir Danmörku þarf að grunnstilla **Uppfletting í skýrslureit**. Frekari upplýsingar um hvernig á að setja upp forritstengdar færibreytur er að finna í hlutanum [Setja upp færibreytur tiltekins forrits fyrir reiti VSK-skýrslu](#set-up-application-specific-parameters) síðar í þessari grein.

Í eftirfarandi töflu sýnir dálkurinn „Niðurstaða uppflettingar“ niðurstöðuna sem er forstillt fyrir tiltekna línu VSK-skýrslu á VSK-skýrslusniðinu. Notaðu þessar upplýsingar til að tengja VSK-kóða við niðurstöðu uppflettingar á réttan hátt og síðan við línuna í VSK-skýrslunni.

### <a name="vat-declaration-overview"></a>Yfirlit VSK-skýrslu

VSK-skýrsla í Danmörku inniheldur eftirfarandi upplýsingar.

**VAT til greiðslu**

| Lýsing                                                  | Skattstofn/skattupphæð | Niðurstaða uppflettingar/Alls                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Útskattur                                                   | Skattupphæð          | **OutputVAT**</br> **DomesticVATUseTax** (einnig gefið upp í glugganum „Innskattur“)                                                                                                                                                                                                                                                                       |
| VSK af vörum o.s.frv. keypt erlendis                           | Skattupphæð          | **PurchaseGoodsAbroad**</br>**PurchaseGoodsAbroadUseTax** (einnig gefið upp í glugganum „Innskattur“)</br>**PurchaseGoodsEU** (Skattstofninn er gefinn upp í „Gluggi A - kaup á vörum.“)</br>**PurchaseGoodsEUUseTax** (Skattupphæðin er einnig gefin upp í glugganum „Innskattur“. Skattstofninn er gefinn upp í „Gluggi A - kaup á vörum.“)                   |
| VSK af þjónustu sem keypt er erlendis og kann að falla undir bakfærð gjöld | Skattupphæð          | **PurchaseServicesAbroad**</br> **PurchaseServicesAbroadUseTax** (einnig gefið upp í glugganum „Innskattur“)</br>**PurchaseServicesEU** (Skattstofninn er gefinn upp í „Gluggi A - kaup á þjónustu.“)</br>**PurchaseServicesEUUseTax** (Skattupphæðin er einnig gefin upp í glugganum „Innskattur“. Skattstofninn er gefinn upp í „Gluggi A - kaup á þjónustu.“) |
| Samtala viðskiptaskuldar                                                | Skattupphæð          | Samtala fyrri þriggja glugganna                                                                                                                                                                                                                                                                                                            |

**Frádráttur**

| Lýsing                                                                               | Skattstofn/skattupphæð | Niðurstaða uppflettingar/Alls                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Innskattur                                                                                 | Skattupphæð          | **InputVAT**</br> **DomesticVATUseTax** (einnig gefið upp í glugganum „Útskattur“)</br>**PurchaseGoodsAbroadUseTax** (einnig gefið upp í „VSK af vörum o.s.frv. keypt erlendis“ gluggi)</br>**PurchaseServicesAbroadUseTax** (einnig í „VSK af þjónustu sem keypt er erlendis og kann að falla undir bakfærð gjöld“ reitnum)</br>**PurchaseGoodsEUUseTax** (einnig gefið upp í „VSK af vörum o.s.frv. keypt erlendis“ gluggi)</br> **PurchaseServicesEUUseTax** (einnig í „VSK af þjónustu sem keypt er erlendis og kann að falla undir bakfærð gjöld“ reitnum) |
| Gjald fyrir olíu og fljótandi jarðolíugas                                                                  | Skattupphæð          | **OilGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Gjald fyrir jarðgas og veitugas                                                             | Skattupphæð          | **NaturalTownGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Kolefnisgjald                                                                               | Skattupphæð          | **CarbonDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| CO2Duty                                                                                   | Skattupphæð          | **CO2Duty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Vatnsgjald                                                                              | Skattupphæð          | **WaterCharge**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Samtals frádráttur                                                                          | Skattupphæð          | Samtala fyrri sex glugga                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Heildarupphæð gjalda (plústala = ganga frá greiðslu, mínustala = fá endurgreiðslu) | Skattupphæð          | „Samtala viðskiptaskuldar“ – „Heildarfrádráttur“                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

**Viðbótarupplýsingar**

| Lýsing                                                                                                                                                                                                                                | Skattstofn/skattupphæð | Niðurstaða uppflettingar/Alls                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-------------------------------------------------|
| Gluggi A – Vörukaup. Virði vörukaupa innan ESB án VSK.                                                                                                                                                   | Skattstofn            | **PurchaseGoodsEU PurchaseGoodsEUUseTax**       |
| Gluggi A – Kaup á þjónustu. Virði kaupa á þjónustu innan ESB án VSK.                                                                                                                                             | Skattstofn            | **PurchaseServicesEU PurchaseServicesEUUseTax** |
| Gluggi B - framboð á vörum - sem gefa skal upp í „ESB-sala án VSK“/DK VIES. Virðið án VSK á vöruframboði innan ESB                                                                                                           | Skattstofn            | **SalesGoodsEU**                                |
| Gluggi B - birgðir - sem ekki á að gefa upp í „ESB-sala án VSK“/DK VIES. Virði tiltekinna aðfanga innan ESB án VSK, t.d. uppsetningar, samsetningar, fjarsölu og nýrra flutningsleiða til óskattskyldra aðila. | Skattstofn            | **SalesInstallationAssemblyEtcEU**              |
| Gluggi B – Framboð á þjónustu. Virði framboðs á þjónustu innan ESB án VSK sem kaupandi ber ábyrgð á að greiða VSK af sem bakfært gjald – verður einnig að tilkynna til „EU-sales without VAT“/DK VIES.                          | Skattstofn            | **SalesServicesEU**                             |
| Gluggi C – aðrar birgðir. Virði annarra vara og þjónustu sem veitt er án VSK í Danmörku til annarra aðildarríkja Evrópusambandsins og þriðju landa eða svæða.                                     | Skattstofn            | **OtherSuppliesWithoutVAT**                     |

#### <a name="purchase-reverse-charge-vat"></a>Innkaup, bakfærður VSK

Ef þú grunnstillir VSK-kóða til að bóka bakfærðan VSK á innleið með því að nota neysluskatt skaltu tengja VSK-kóðana við niðurstöðu uppflettingar í **Uppfletting í skýrslureit** sem inniheldur „UseTax“ í heitinu.

Annars er hægt að grunnstilla tvo aðskilda VSK-kóða: einn fyrir VSK til greiðslu og annan fyrir VSK-frádrátt. Síðan skal tengja hvern kóða við samsvarandi niðurstöður uppflettingar á **Uppfletting í skýrslureit**.

Fyrir skattskyld kaup innan ESB skal til dæmis grunnstilla VSK-kóðann **UT_S_EU** með neysluskatti og tengja hann við uppflettiniðurstöðuna **PurchaseGoodsEUUseTax** í **Uppfletting í skýrslureit**. Í þessu tilviki koma skattupphæðir sem nota VSK-kóðann **UT_S_EU** fram í gluggunum „VSK af vörum o.s.frv. keypt erlendis“ og „Innskattur“. Skattstofnar eru gefnir upp í „Gluggi A - kaup á vörum.“

Einnig getur þú stillt tvo VSK-kóða:

- **VAT_S_EU**, sem er með -25 prósent skatt
- **InVAT_S_EU**, sem er með 25 prósent skatt

Kóðana tengir þú svo við niðurstöður uppflettingar í **Uppfletting í skýrslureit** á eftirfarandi hátt:

- Tengdu **VAT_S_EU** við uppflettiniðurstöðuna **PurchaseGoodsEU**.
- Tengdu **VAT_S_EU** við uppflettiniðurstöðuna **InputVAT**.

Í þessu tilviki koma upphæðir sem nota VSK-kóðann **VAT_S_EU** fram í glugganum „VSK af vörum o.s.frv. keypt erlendis“ og „Gluggi A – kaup á vörum.“ Upphæðir sem nota VSK-kóðann **InVAT_S_EU** koma fram í glugganum „Innskattur“.

Frekari upplýsingar um hvernig á að grunnstilla bakfærðan VSK er að finna í [Bakfærð gjöld](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Skilgreina kerfisfæribreytur

Til að búa til VSK-skýrsla þarf að skilgreina VSK-númerið.

1. Fara í **Fyrirtækisstjórnun** > **Fyrirtæki** > **Lögaðilar**.
2. Veldu lögaðilann og veldu síðan **Skráningarkenni**.
3. Veldu eða búðu til aðsetrið í Danmörku og síðan í flýtiflipanum **Skráningarkenni** skaltu velja **Bæta við**.
4. Í reitnum **Skráningargerð** skal velja skráningargerðina sem tilheyrir Danmörku og sem notar skráningarflokkinn **VSK-nr.**.
5. Í reitinn **Skráningarnúmer** skal færa inn skattnúmerið.
6. Í flipanum **Almennt**, í reitinn **Gildistími**, skal færa inn dagsetningu þegar númerið tekur gildi.

Frekari upplýsingar um hvernig á að setja upp skráningarflokka og skráningargerðir er að finna í [Skráningarkenni](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-preview-for-denmark"></a>Setja upp forskoðun VSK-skýrslu fyrir Danmörku

### <a name="import-er-configurations"></a>Flytja inn rafræn skýrslugerð grunnstillingar

Opnaðu vinnusvæðið **Rafræn skýrslugerð** og flyttu inn rafræna skýrslugerðarsniðið **VSK-skýrsla í Excel (DK)**.

Frekari upplýsingar er að finna í [Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters"></a>Setja upp færibreytur tiltekins forrits fyrir VSK-skýrslureiti

> [!NOTE]
> Mælt er með að eiginleikinn **Nota sértækar færibreytur fyrir forrit úr fyrri útgáfum ER-sniða** á vinnusvæðinu **Eiginleikastjórnun** sé virkjaður. Þegar þessi eiginleiki er virkjaður verða færibreytur sem eru grunnstilltar fyrir fyrri útgáfu af rafrænu skýrslugerðarsniði sjálfkrafa virkar fyrir síðari útgáfu af sama sniði. Ef þessi eiginleiki er ekki virkur verður þú að grunnstilla færibreytur tiltekins forrits sérstaklega fyrir hverja útgáfu af sniði. Eiginleikinn **Nota sértækar færibreytur fyrir forrit úr fyrri útgáfum ER-sniða** er í boði á vinnusvæðinu **Eiginleikastjórnun** frá og með útgáfu 10.0.23 af Finance. Frekari upplýsingar um hvernig á að setja upp færibreytur á rafrænu skýrslugerðarsniði fyrir hvern lögaðila er að finna í [Setja upp færibreytur á sniði rafrænnar skýrslugerðar fyrir hvern lögaðila](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Til að búa sjálfkrafa til VSK-skýrslu skaltu tengja VSK-kóða í forritinu og fletta upp niðurstöðum í skilgreiningu rafrænnar skýrslugerðar.

Fylgdu þessum skrefum til að skilgreina hvaða VSK-kóðar búa til hvaða glugga í VSK-skýrslunni.

1. Farið í **Vinnusvæði** > **Rafræn skýrslugerð**, og veljið **Skilgreiningar skýrslugerðar**.
2. Veldu skilgreininguna **VSK-skýrsla í Excel (DK)** og veldu síðan **Skilgreiningar \> Uppsetning á færibreytum tiltekins forrits**.
3. Á síðunni **Færibreytur tiltekins forrits**, í flýtiflipanum **Uppflettingar**, skal velja **Uppfletting í skýrslureit**.
4. Í flýtiflipanum **Skilyrði** skal stilla eftirfarandi reiti til að tengja VSK-kóða og skýrslureiti.

    | Svæði                  | Lýsing                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Niðurstaða uppflettingar          | Veljið gildi skýrslureitarins. Frekari upplýsingar um gildin og úthlutun þeirra í línum VSK-skýrslu er að finna í hlutanum [Yfirlit VSK-skýrslu](#vat-declaration-overview) fyrr í þessari grein.                                                                                               |
    | Skattkóði               | Veldu VSK-kóðann sem á að tengja við skýrslureitinn. Bókaðar skattfærslur sem nota valinn VSK-kóða verður safnað í viðeigandi skýrsluglugga. Mælt er með að aðskilja VSK-kóðana á þann hátt að einn VSK-kóði búi til upphæðir í aðeins einum skýrsluglugga. |
    | Flokkari færslna | Ef þú bjóst til nógu marga VSK-kóða til að ákvarða skýrsluglugga skaltu velja **\*Ekki autt\***. Ef þú bjóst ekki til nógu marka VSK-kóða þannig að einn VSK-kóði búi til upphæðir í aðeins einum skýrsluglugga er hægt að setja upp færsluflokkara. Eftirfarandi færsluflokkarar eru í boði:</br>-   **Innkaup**</br>-   **PurchaseExempt** (skattfrjáls kaup)</br>-   **PurchaseReverseCharge**(innskattur af bakfærslu innkaupa)</br>-   **Sala**</br>-   **SalesExempt** (skattfrjáls sala)</br>-   **SalesReverseCharge** (gjaldfallinn skattur úr bakfærðu gjaldi kaupa eða sölu)</br>-   **Nota skatt**. </br>Fyrir hvern færsluflokkara er flokkari fyrir kreditnótuna líka í boði. Til dæmis er einn þessara flokkara **PurchaseCreditNote** (innkaupakreditnóta).</br>Gættu þess að stofna tvær línur fyrir hvern VSK-kóða: eina sem er með gildi færsluflokkara og eina sem er með færsluflokkara fyrir gildi kreditnótu. |


    > [!NOTE]
    > Tengdu alla VSK-kóða við niðurstöður uppflettingar. Ef einhverjir VSK-kóðar mynda ekki gildi í VSK-skýrslunni skal tengja þá við uppflettiniðurstöðuna **Annað**.

    ![Síða sértækra færibreyta fyrir forrit.](media/7db74920fad66a0db7fad60758698cc0.png)


5. Í reitnum **Staða** skal breyta gildinu í **Lokið**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Setja upp snið VSK-skýrslu til að forskoða upphæðir í Excel

1. Á vinnusvæðinu **Eiginleikastjórnun** skal finna og velja **Skýrslur fyrir snið VSK-yfirlits** eiginleiki á listanum og síðan velja **Virkja núna**.
2. Opnið **Fjárhagur** > **Uppsetning**  >  **Færibreytur fyrir fjárhag**.
3. Í flipanum **Virðisaukaskattur**, í hlutanum **Valkostir skatts**, í reitnum **Sniðsvörpun VSK-skýrslu**, skal velja ER-sniðið **VSK-skýrsla Excel (DK)**.

   Þetta snið er prentað þegar skýrslan **Gefa upp virðisaukaskatt fyrir jöfnunartímabil** er keyrð. Það er einnig prentað þegar **Prenta** er valið á síðunni **VSK-greiðslur**.

4. Á síðunni **Skattayfirvöld** skal velja skattayfirvöld og síðan í reitnum **Útlit skýrslu** skal velja **Sjálfgefið**.

Ef VSK-skýrsla er skilgreind í lögaðila sem er með [margar VSK-skráningar](emea-reporting-for-multiple-vat-registrations.md) skal fylgja þessum skrefum.

1. Opnið **Fjárhagur** \> **Uppsetning** \> **Færibreytur fyrir fjárhag**.
2. Í flipanum **Virðisaukaskattur**, í flýtiflipanum **Rafræn skýrslugerð fyrir lönd/svæði**, í línunni fyrir **DNK**, skal velja rafræna skýrslugerðarsniðið **VSK-skýrsla í Excel (DK)**.

## <a name="set-up-electronic-messages"></a>Setja upp rafræn skilaboð

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Sækja og flytja inn gagnapakkann sem er með dæmastillingar fyrir rafræn skilaboð

Gagnapakkinn inniheldur stillingar rafrænna skilaboða sem eru notaðar til að forskoða VSK-skýrsluna í Excel. Þú getur notað þessar stillingar eða búið til þínar eigin. Frekari upplýsingar um hvernig á að vinna með rafræn skilaboð og búa til sínar eigin stillingar er að finna í [Rafræn skilaboð](../general-ledger/electronic-messaging.md).

1. Í [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2), í samnýttu eignasafni, skal velja **Gagnapakka** sem eignagerð og sækja svo **DK VSK-skýrslupakka**. Skráin sem sótt var heitir **DK VAT Statement package.zip**.
2. Í Finance, á vinnusvæðinu **Gagnastjórnun** skal velja **Innflutningur**.
3. Í flýtiflipann **Flytja inn**, í reitinn **Heiti hóps**, skal færa inn heiti fyrir verkið.
4. Á flýtiflipanum **Valdar einingar** skal velja **Bæta við skrá**.
5. Í svarglugganum **Bæta við skrá** skal staðfesta að reiturinn **Snið upprunagagna** sé stilltur á **Pakki**, velja **Hlaða upp og bæta við** og velja svo zip-skrána sem var sótt áður.
6. Veljið **Loka**.
7. Þegar gagnaeiningunum er hlaðið upp skal á aðgerðasvæðinu velja **Flytja inn**.
8. Opnaðu **Skattur** > **Fyrirspurnir og skýrslur** > **Rafræn skilaboð** > **Rafræn skilaboð** og staðfesta vinnslu rafrænna skilaboða sem flutt voru inn (**DK VSK-skýrsla**).

### <a name="configure-electronic-messages"></a>Skilgreina rafræn skilaboð

1. Opnið **Skattur**  >  **Uppsetning**  >  **Rafræn skilaboð**  >  **Fylla út færsluaðgerðir**.
2. Veldu línuna fyrir **DK Fylla út færslur VSK-skila** og síðan velja **Breyta fyrirspurn**.
3. Notaðu síuna til að tilgreina jöfnunartímabil sem á að hafa með í skýrslunni.
4. Ef tilkynna þarf skattfærslur frá öðrum jöfnunartímabilum í annarri skýrslu skal búa til nýja aðgerð fyrir **Fylla út færslur** og velja viðeigandi jöfnunartímabil.

## <a name="preview-the-vat-declaration-in-excel"></a>Forskoða VSK-skýrsluna í Excel

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a><a name="preview-vat-excel"></a>Forskoða VSK-skýrsluna í Excel úr „Gefa upp virðisaukaskatt“ fyrir reglubundið verk jöfnunartímabils

1. Opna **Skattur** > **Reglubundin verkefni** > **Skattframtöl** > **Virðisaukaskattur** > **Virðisaukaskattsskýrsla fyrir jöfnunartímabil**.
2. Veljið gildi í reitnum **Jöfnunartímabil**.
3. Í reitnum **Útgáfa VSK-greiðslu** skal velja eitt eftirfarandi gilda:

    - **Upprunalegt**: Búðu til skýrslu fyrir VSK-færslur upprunalegrar VSK-greiðslu eða áður en VSK-greiðslan er mynduð.
    - **Leiðréttingar**: Búðu til skýrslu fyrir VSK-færslur fyrir allar komandi VSK-greiðslur fyrir tímabilið.
    - **Heildarlisti**: Búðu til skýrslu fyrir allar VSK-færslur fyrir tímabilið, þ.m.t. upprunalegt og allar leiðréttingar.

4. Í reitnum **Frá dagsetningu** velurðu upphafsdagsetningu skýrslutímabilsins.
5. Veldu **Í lagi** og farðu yfir Excel-skýrsluna.

### <a name="settle-and-post-sales-tax"></a>Jafna og bóka virðisaukaskatt

1. Farið í **Skattur** > **Reglubundin verkefni** > **Skattskýrslur** > **Virðisaukaskattur** > **Jafna og bóka VSK**.
2. Veljið gildi í reitnum **Jöfnunartímabil**.
3. Í reitnum **Útgáfa VSK-greiðslu** skal velja eitt eftirfarandi gilda:

    - **Upprunalegt**: Búðu til upprunalega VSK-greiðslu fyrir jöfnunartímabilið.
    - **Nýjustu leiðréttingar**: Búðu til leiðréttingu á VSK-greiðslur eftir að upprunaleg VSK-greiðsla fyrir jöfnunartímabilið var búin til.

4. Í reitnum **Frá dagsetningu** velurðu upphafsdagsetningu skýrslutímabilsins.
5. Veldu **Í lagi**.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Forskoða VSK-skýrsluna í Excel úr VSK-greiðslu

1. Opnaðu **Skattur** > **Fyrirspurnir og skýrslur** > **Fyrirspurnir um virðisaukaskatt** > **Greiðslur virðisaukaskatts** og veldu greiðslulínu virðisaukaskatts.
2. Veldu **Prenta skýrslu** og veldu síðan **Í lagi**.
3. Farðu yfir Excel-skrána sem er búin til fyrir valda VSK-greiðslulínu.

> [!NOTE]
> Skýrslan er aðeins gerð fyrir valda línu VSK-greiðslunnar. Ef þú verður til dæmis að búa til leiðréttingarskýrslu sem inniheldur allar leiðréttingar fyrir tímabilið eða staðgengilsskýrslu sem inniheldur upprunaleg gögn og allar leiðréttingar skaltu nota reglubundna verkið **Gefa upp virðisaukaskatt fyrir jöfnunartímabil**.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Búa til VSK-skýrslu úr rafrænum skilaboðum

Þegar þú notar rafræn skilaboð til að búa til skýrsluna geturðu safnað skattgögnum frá mörgum lögaðilum. Frekari upplýsingar er að finna í hlutanum [Keyra VSK-skýrslu fyrir marga lögaðila](#run-vat-declaration) síðar í þessari grein.

Eftirfarandi ferli á við um dæmi um vinnslu rafrænna skilaboða sem þú fluttir inn fyrr úr LCS samnýttu eignasafni.

1. Opnið **Skattur \> Fyrirspurnir og skýrslur \> Rafræn skilaboð \> Rafræn skilaboð**.
2. Veljið **DK VSK-skýrsla** í vinstra svæðinu.
3. Í flýtiflipanum **Skilaboð** skal velja **Nýtt** og síðan í svarglugganum **Keyra vinnslu** skal velja **Í lagi**.
4. Veldu skilaboðalínuna sem er búin til, sláðu inn lýsingu og tilgreindu svo upphafs- og lokadagsetningar fyrir skýrsluna.

   > [!NOTE]
   > Skref 5 til 7 eru valfrjáls.

5. Valfrjálst: Í flýtiflipanum **Skilaboð** skal velja **Safna gögnum** og velja síðan **Í lagi**. VSK-greiðslurnar sem voru gerðar áður er bætt við skilaboðin. Frekari upplýsingar er að finna í hlutanum [Jafna og bóka virðisaukaskatt](#settle-and-post-sales-tax) fyrr í þessari grein. Ef þú sleppir þessu skrefi geturðu samt búið til VSK-skýrslu með því að nota reitinn **Útgáfa skattskýrslu** í svarglugganum **Skýrsla**.
6. Valfrjálst: Í flýtiflipanum **Skilaboðaatriði** skal yfirfara VSK-greiðslur sem fluttar eru til vinnslu. Allar VSK-greiðslur á völdu tímabili sem voru ekki hafðar með í neinum öðrum skilaboðum sömu vinnslunnar eru sjálfgefið hafðar með.
7. Valfrjálst: Veldu **Upprunalegt skjal** til að yfirfara VSK-greiðslur eða veldu **Eyða** til að útiloka VSK-greiðslur frá vinnslu. Ef þú sleppir þessu skrefi geturðu samt búið til VSK-skýrslu með því að nota reitinn **Útgáfa skattskýrslu** í svarglugganum **Skýrsla**.
8. Í flýtiflipanum **Skilaboð** skal velja **Uppfæra stöðu**. Í svarglugganum **Uppfæra stöðu** skal velja **Tilbúið til myndunar** og síðan velja **Í lagi**. Staðfestu að stöðu skilaboðanna sé breytt í **Tilbúin til að mynda**.
9. Veldu **Búa til skýrslu**. Til að forskoða upphæðir VSK-skýrslu skal í svarglugganum **Keyra vinnslu** velja **Forskoða skýrslu** og síðan velja **Í lagi**.
10. Í svarglugganum **Færibreytur rafrænnar skýrslugerðar** skal stilla reitina eins og lýst er í hlutanum [Forskoða VSK-skýrsluna í Excel úr „Gefa upp virðisaukaskatt“ fyrir reglubundið verk jöfnunartímabils](#preview-vat-excel) fyrr í þessari grein og síðan velja **Í lagi**.
11. Veljið hnappinn **Viðhengi** (bréfaklemmutákn) efst í hægra horni síðunnar og veljið svo **Opna** til að opna skrána. Farið yfir upphæðirnar í Excel skjalinu.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-vat-declaration"></a>Keyra VSK-skýrslu fyrir marga lögaðila

Til að nota sniðin til að gefa upp VSK-skýrsluna fyrir hóp af lögaðilum þarf fyrst að setja upp forritstengdar færibreytur rafræna skýrslugerðarsniðanna fyrir VSK-kóða frá öllum nauðsynlegum lögaðilum.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Setja upp rafræn skilaboð til að safna skattgögnum frá nokkrum lögaðilum

Fylgdu þessum skrefum til að setja upp rafræn skilaboð til að safna gögnum frá mörgum lögaðilum.

1. Opnið **Vinnusvæði** > **Eiginleikastjórnun**.
2. Finndu og veldu eiginleikann **Fyrirspurnir milli fyrirtækja fyrir fyllingu færsluaðgerða** í listanum og veldu síðan **Virkja núna**.
3. Opnið **Skattur**  >  **Uppsetning**  >  **Rafræn skilaboð**  >  **Fylla út færsluaðgerðir**.
4. Á síðunni **Fylla út færsluaðgerð** skal velja línuna fyrir **DK Fylla út VSK-skilafærslu**.

   Í hnitanetinu **Uppsetning gagnagjafa** er nýr reitur fyrir **Fyrirtæki** í boði. Fyrir fyrirliggjandi færslur sýnir þessi reitur auðkenni núverandi lögaðila.

5. Í hnitanetinu **Uppsetning gagnagjafa** skal bæta við línu fyrir hvern aukalegan lögaðila sem á að vera í skýrslugjöfinni. Fyrir hverja nýja línu skal stilla eftirfarandi reiti:

    | Svæði                  | Lýsing                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Nafn                   | Sláðu inn gildi sem hjálpar þér að skilja hvaðan þessi færsla kemur. Sláðu til dæmis inn **VSK-greiðsla dótturfyrirtækis 1**. |
    | Gerð skilaboðaatriðis      | Veljið **VSK-endurgreiðslu**. Þetta gildi er eina gildið sem er í boði fyrir allar færslunar.                                    |
    | Lykilgerð           | Velja **Allt**                                                                                                               |
    | Aðaltöfluheiti      | Tilgreinið **TaxReportVoucher** fyrir allar færslurnar.                                                                             |
    | Reitur skjalnúmers  | Tilgreinið **Fylgiskjal** fyrir allar færslurnar.                                                                                      |
    | Dagsetningarreitur skjals    | Tilgreina **TransDate** fyrir allar færslur.                                                                                    |
    | Reikningsreitur skjals | Tilgreinið **TaxPeriod** fyrir allar færslurnar.                                                                                    |
    | Fyrirtæki                | Veljið auðkenni lögaðilans.                                                                                            |
    | Fyrirspurn notanda             | Þessi gátreitur er valinn sjálfkrafa þegar þú skilgreinir skilyrði með því að velja **Breyta fyrirspurn**.                                 |

6. Fyrir hverja nýja línu skal velja **Breyta fyrirspurn** og tilgreina tengt jöfnunartímabil sem á við um lögaðilann sem er tilgreindur í reitnum **Fyrirtæki** í línunni.

Þegar uppsetningunni er lokið safnar aðgerðin **Safna gögnum** á síðunni **Rafræn skilaboð** VSK-greiðslum frá öllum lögaðilum sem eru skilgreindir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
