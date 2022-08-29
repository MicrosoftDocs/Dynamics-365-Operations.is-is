---
title: Hanna segðir rafrænnar skýrslugerðar til að kalla á aðferðir forritaflokka
description: Þessi grein lýsir því hvernig á að endurnýta núverandi forritsrökfræði í rafrænum skýrslustillingum með því að kalla á nauðsynlegar aðferðir forritaflokka.
author: kfend
ms.date: 11/02/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21c24cee15e9a0fd11838b5b8fd816e4aaed9a93
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267843"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>Hanna segðir rafrænnar skýrslugerðar til að kalla á aðferðir forritaflokka

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir því hvernig á að endurnýta núverandi forritsrökfræði í [Rafræn skýrslugerð (ER)](../general-electronic-reporting.md) stillingar með því að kalla á nauðsynlegar aðferðir forritaflokka í ER tjáningum. Gildi röksemda fyrir að kalla flokka er hægt að skilgreina á breytilegan hátt á keyrslutíma. Til dæmis geta gildi byggt á upplýsingum í þáttunarskjalinu til að tryggja réttmæti þess.

Fyrir dæmið í þessari grein munt þú hanna ferli sem flokkar innkomnar bankayfirlit fyrir uppfærslu forritsgagna. Þú munt fá bankayfirlit sem berast sem textaskrár (.txt) sem innihalda IBAN-kóða (International Bank Account Number). Sem hluti af innflutningsferli bankayfirlita verður þú að sannreyna réttmæti IBAN kóðans með því að nota rökfræðina sem þegar er tiltæk.

## <a name="prerequisites"></a>Forkröfur

Verklagsreglurnar í þessari grein eru ætlaðar notendum sem hafa verið úthlutað **Kerfisstjóri** eða **Framkvæmdaraðili rafrænna skýrslugerðar** hlutverki.

Hægt er að ljúka verklagsreglunum með því að nota hvaða gagnasett sem er.

Til að ljúka þeim verður þú að hlaða niður og vista eftirfarandi skrá: [SampleIncomingMessage.txt](https://download.microsoft.com/download/8/0/a/80adbc89-f23c-46d9-9241-e0f19125c04b/SampleIncomingMessage.txt).

Í þessari grein muntu búa til nauðsynlegar ER stillingar fyrir Litware, Inc. sýnishornsfyrirtækið. Þess vegna, áður en þú lýkur aðferðunum í þessari grein, verður þú að fylgja þessum skrefum.

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á **Staðsetningarstillingar** síðu, staðfestu að stillingarveitan fyrir **Litware, Inc.** sýnishornsfyrirtæki er tiltækt og merkt sem virkt. Ef þú sérð ekki þessa stillingarveitu verður þú fyrst að ljúka skrefunum í [Búðu til stillingaveitur og merktu þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-a-new-er-model-configuration"></a>Flytja inn nýja grunnstillingu líkans í Rafræn skýrslugerð

1. Á **Staðsetningarstillingar** síðu, í **Stillingarveitur** kafla, veldu flísina fyrir **Microsoft** uppsetningarveitu.
2. Veldu **Geymslur**.
3. Á **Staðsetningargeymslur** síðu, veldu **Sýna síur**.
4. Til að velja alþjóðlega geymsluskrá skaltu bæta við a **Nafn** síunarreitur.
5. Í **Nafn** reit, slá inn **Alþjóðlegt**. Veldu síðan **inniheldur** síunarstjóri.
6. Veljið **Bæta við**.
7. Veldu **[Opið](../er-download-configurations-global-repo.md#open-configurations-repository)** til að skoða listann yfir ER stillingar í valinni geymslu.
8. Á **Stillingargeymsla** síðu, í stillingartrénu, veldu **Greiðslulíkan**.
9. Á **Útgáfur** Flýtiflipi, ef **Flytja inn** hnappur er tiltækur, veldu hann og veldu síðan **Já**.

    Ef **Flytja inn** hnappurinn er ekki tiltækur, þú hefur þegar flutt inn valda útgáfu af **Greiðslulíkan** ER stillingar.

10. Lokaðu **Stillingargeymsla** síðu og lokaðu síðan **Staðsetningargeymslur** síðu.

## <a name="add-a-new-er-format-configuration"></a>Bæta við nýrri grunnstillingu sniðs í Rafræn skýrslugerð

Bæta við nýju sniði fyrir rafræna skýrslugerð til að þátta bankayfirlit á innleið á TXT-sniði.

1. Á **Staðsetningarstillingar** síðu, veldu **Skýrslustillingar** flísar.
2. Á **Stillingar** síðu, í stillingartrénu í vinstri glugganum, veldu **Greiðslulíkan**.
3. Veljið **Stofna skilgreiningu**. 
4. Í fellilistanum skaltu fylgja þessum skrefum:

    1. Í svæðinu **Nýtt** skal færa inn **Snið byggir á gagnalíkani PaymentModel**,
    2. Í **Nafn** reit, slá inn **Innflutningssnið bankayfirlits (sýnishorn)**.
    3. Í **Styður gagnainnflutning** reit, veldu **Já**.
    4. Veldu **Búðu til stillingar** til að klára að búa til stillinguna.

## <a name="design-the-er-format-configuration--format"></a>Hannaðu ER snið stillingu - Format

Hannaðu ER snið sem táknar væntanlega uppbyggingu ytri skráar á TXT sniði.

1. Fyrir **Innflutningssnið bankayfirlits (sýnishorn)** sniðstillingu sem þú bættir við skaltu velja **Hönnuður**.
2. Á **Sniðhönnuður** síðu, í sniðbyggingartrénu í vinstri glugganum, veldu **Bæta við rót**.
3. Í svarglugganum sem kemur upp skal fylgja þessum skrefum:

    1. Í trénu, veldu **Texti\\ Röð** að bæta við a **Röð** sniði hluti.
    2. Í **Nafn** reit, slá inn **Rót**.
    3. Í **Sérstakar** reit, veldu **Ný lína - Windows (CR LF)**. Byggt á þessari stillingu verður hver lína í þáttunarskránni talin sérstök skrá.
    4. Veldu **Í lagi**.

4. Veljið **Bæta við**.
5. Í svarglugganum sem kemur upp skal fylgja þessum skrefum:

    1. Í trénu, veldu **Texti\\ Röð**.
    2. Í **Nafn** reit, slá inn **Raðir**.
    3. Í reitnum **Margfeldi** skaltu velja **Einn margir**. Byggt á þessari stillingu mun búast við að að minnsta kosti ein lína sé til staðar í þáttunarskránni.
    4. Veldu **Í lagi**.

6. Í trénu, veldu **Rót\\ Raðir**, og veldu síðan **Bæta við röð**.
7. Í svarglugganum sem kemur upp skal fylgja þessum skrefum:

    1. Í **Nafn** reit, slá inn **Fields**.
    2. Í **Margföldun** reit, veldu **Nákvæmlega einn**.
    3. Veldu **Í lagi**.

8. Í trénu, veldu **Rót\\ Raðir\\ Fields**, og veldu síðan **Bæta við**.
9. Í svarglugganum sem kemur upp skal fylgja þessum skrefum:

    1. Í trénu, veldu **Texti\\ Strengur**.
    2. Í **Nafn** reit, slá inn **IBAN**.
    3. Veldu **Í lagi**.

10. Veldu **Vista**.

Stillingin er nú sett upp þannig að hver lína í þáttunarskránni inniheldur aðeins IBAN kóðann.

![Innflutningssnið bankayfirlits (sýnishorn) sniðsstillingar á síðunni Sniðshönnuður.](../media/design-expressions-app-class-er-01.png)

## <a name="design-the-er-format-configuration--mapping-to-a-data-model"></a>Hannaðu uppsetningu ER sniðs - Kortlagning á gagnalíkan

Hannaðu kortlagningu ER sniðs sem notar upplýsingar úr þáttunarskránni til að fylla út gagnalíkan.

1. Á **Sniðhönnuður** síðu, á aðgerðarrúðunni, veldu **Korta snið að líkani**.
2. Á **Líkan til kortlagningar gagnagjafa** síðu, á aðgerðarrúðunni, veldu **Nýtt**.
3. Í **Skilgreining** reit, veldu **BankToCustomerDebitCreditNotificationInitiation**.
4. Í **Nafn** reit, slá inn **Kortlagning á gagnalíkan**.
5. Veldu **Vista**.
6. Veljið **Hönnuður**.
7. Á **Módelkortahönnuður** síðu, í **Tegundir gagnagjafa** tré, veldu **Dynamics 365 for Operations\\ bekk**.
8. Í **Uppsprettur gagna** kafla, veldu **Bæta við rót** til að bæta við gagnagjafa sem kallar á núverandi forritsrökfræði fyrir staðfestingu IBAN kóða.
9. Í svarglugganum sem kemur upp skal fylgja þessum skrefum:

    1. Í **Nafn** reit, slá inn **Athugaðu\_ kóða**.
    2. Í **bekk** reit, sláðu inn eða veldu **ISO7064**.
    3. Veldu **Í lagi**.

10. Í **Tegundir gagnagjafa** tré, fylgdu þessum skrefum:

    1. Stækkaðu **sniði** gagnagjafa.
    2. Stækkaðu **sniði\\ Rót: Röð (rót)**.
    3. Stækkaðu **sniði\\ Rót: Röð (rót)\\ Raðir: Röð 1..\* (Raðir)**.
    4. Stækkaðu **sniði\\ Rót: Röð (rót)\\ Raðir: Röð 1..\* (Raðir)\\ Reitir: Röð 1..1 (reitir)**.

11. Í **Gagnalíkan** tré, fylgdu þessum skrefum:

    1. Stækkaðu **Greiðslur** sviði gagnalíkans.
    2. Stækkaðu **Greiðslur\\ Kröfuhafareikningur (Creditor Account)**.
    3. Stækkaðu **Greiðslur\\ Kröfuhafareikningur (Creditor Account)\\ Auðkenning**.
    4. Stækkaðu **Greiðslur\\ Kröfuhafareikningur (Creditor Account)\\ Auðkenning\\ IBAN**.

12. Fylgdu þessum skrefum til að binda íhluti á stillta sniðinu við reiti gagnalíkana:

    1. Veldu **sniði\\ Rót: Röð (rót)\\ Raðir: Röð 1..\* (Raðir)**.
    2. Veldu **Greiðslur**.
    3. Veldu **Binda**. Miðað við þessa stillingu verður hver lína í þáttunarskránni talin ein greiðsla.
    4. Veldu **sniði\\ Rót: Röð (rót)\\ Raðir: Röð 1..\* (Raðir)\\ Reitir: Röð 1..1 (reitir)\\ IBAN: String(IBAN)**.
    5. Veldu **Greiðslur\\ Kröfuhafareikningur (Creditor Account)\\ Auðkenning\\ IBAN**.
    6. Veldu **Binda**. Byggt á þessari stillingu er **IBAN** reit gagnalíkans verður fyllt út með gildinu úr þáttunarskránni.

    ![Binding sniðíhluta við reiti gagnalíkana á síðunni Hönnuðir líkanakorta.](../media/design-expressions-app-class-er-02.png)

13. Á **Staðfestingar** flipanum skaltu fylgja þessum skrefum til að bæta við a [löggildingu](../general-electronic-reporting-formula-designer.md#Validation) regla sem sýnir villuboð fyrir hvaða línu sem er í þáttunarskránni sem inniheldur ógildan IBAN kóða:

    1. Veldu **Nýtt**, og veldu síðan **Breyta ástandi**.
    2. Á **Formúluhönnuður** síðu, í **Uppruni gagna** tré, stækkaðu **Athugaðu\_ kóða** gagnaveita sem táknar **ISO7064** umsóknarflokki til að skoða tiltækar aðferðir þessa flokks.
    3. Veldu **Athugaðu\_ kóða\\ verifyMOD1271\_ 36**.
    4. Veldu **Bæta við gagnagjafa**.
    5. Í **Formúla** reit, sláðu inn eftirfarandi [tjáningu](../general-electronic-reporting-formula-designer.md#Binding) :**Athugaðu\_ codes.verifyMOD1271\_ 36(snið.Root.Rows.Fields.IBAN)**.
    6. Veljið **Vista** og lokið síðan skjámyndinni.
    7. Veldu **Breyta skilaboðum**.
    8. Á **Formúluhönnuður** síðu, í **Formúla** reit, slá inn **CONCATENATE("Ógildur IBAN kóði fannst:&nbsp; ", format.Root.Rows.Fields.IBAN)**.
    9. Veljið **Vista** og lokið síðan skjámyndinni.

    Byggt á þessum stillingum mun staðfestingarskilyrðið koma aftur *[RANGT](../er-formula-supported-data-types-primitive.md#boolean)* fyrir ógildan IBAN kóða með því að hringja í núverandi **verifyMOD1271\_ 36** aðferð við **ISO7064** umsóknarflokkur. Athugaðu að gildi IBAN kóðans er virkt skilgreint á keyrslutíma sem rök köllunaraðferðarinnar, byggt á innihaldi þáttunartextaskráarinnar.

    ![Staðfestingarregla á síðunni Hönnuður líkanakortlagningar.](../media/design-expressions-app-class-er-03.png)

14. Veldu **Vista**.
15. Lokaðu **Módelkortahönnuður** síðu og lokaðu síðan **Líkan til kortlagningar gagnagjafa** síðu.

## <a name="run-the-format-mapping"></a>Keyra vörpun sniðs

Í prófunarskyni skaltu keyra sniðkortlagninguna með því að nota SampleIncomingMessage.txt skrána sem þú sóttir áðan. Mynduð framleiðsla mun innihalda gögn sem eru flutt inn úr völdu textaskránni og flutt í sérsniðna gagnalíkanið meðan á raunverulegum innflutningi stendur.

1. Á **Líkan til kortlagningar gagnagjafa** síðu, veldu **Hlaupa**.
2. Á **Rafræn skýrslufæribreytur** síðu, veldu **Skoðaðu**, flettu að **SampleIncomingMessage.txt** skrána sem þú halaðir niður og veldu hana.
3. Veldu **Í lagi**.
4. Taktu eftir því að **Líkan til kortlagningar gagnagjafa** síða sýnir villuboð um ógildan IBAN kóða.

    ![Niðurstaðan af því að keyra sniðvörpunina á Vörpun líkan til gagnaveitu.](../media/design-expressions-app-class-er-04.png)

5. Farið yfir úttak í XML-sniði, sem stendur fyrir gögn sem hafa verið innflutt úr valinni skrá og tengd við gagnalíkan. Taktu eftir að aðeins þrjár línur af innfluttu textaskránni voru unnar án villna. IBAN kóðann á netinu 4 er ekki gildur og var sleppt.

    ![XML úttak.](../media/design-expressions-app-class-er-05.png)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
