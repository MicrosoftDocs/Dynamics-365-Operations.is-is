---
title: Stofna og uppfæra tímabil afhendingar til viðskiptavinar
description: Þessi grein lýsir því hvernig á að búa til, stilla og uppfæra afhendingartíma viðskiptavina í höfuðstöðvum Commerce.
author: anupamar-ms
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.openlocfilehash: a135f592225e4b388b5c9fdaa5fe23e60baf0185
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882234"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a>Stofna og uppfæra tímabil afhendingar til viðskiptavinar

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir því hvernig á að búa til, stilla og uppfæra afhendingartíma viðskiptavina í höfuðstöðvum Commerce.

Tímahólfsaðgerðin býður smásölum upp á leið til að skilgreina tímahólf fyrir vörur þar sem kveikt er á afhendingarmátanum fyrir sótta pöntun viðskiptavinar. Tímahólf gera smásölum kleift að skilgreina dagsetningar og tímasetningar þegar hægt er að sækja pöntun í verslun. Einnig er hægt að skilgreina fjölda pantana sem hægt er að sækja á tilteknu tímabili. Á þennan hátt geta smásalar takmarkað fjölda pantana sem hægt verður að sækja á tilteknum degi og tíma. Útkoman er betri gæðaþjónusta fyrir viðskiptavinina.

> [!NOTE]
> Þessi eiginleiki er tiltækur í Microsoft Dynamics 365 Commerce útgáfum 10.0.15 og nýrri.

Eftirfarandi mynd sýnir dæmi um val á tímahólfi í greiðsluferli rafrænna viðskipta.

![Dæmi um val á tímahólfi í greiðsluferli rafrænna viðskipta.](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a>Eiginleikar tímahólfs

Tímahólf er sérstakt tímabil þegar viðskiptavinur getur valið að sækja pöntun frá tiltekinni verslun eða staðsetningu. Eiginleiki tímahólfsstjórnunar er aðeins í boði þegar afhendingarmáti sóttrar pöntunar viðskiptavinar er skilgreindur í Dynamics 365 Commerce.

Tímahólf er skilgreint með eftirfarandi eiginleikum:

- **Afhendingarmáti** – Tilgreinið afhendingarmáta sóttrar pöntunar sem tímahólfið á við um.
- **Lágmarksdagar** og **Hámarksdagar** – Tilgreinið fyrstu og síðustu dagsetningarnar sem hægt er að velja fyrir sótta pöntun miðað við dagsetninguna þegar pöntunin er gerð. 

    Eiginleikinn **Lágmarksdagar** tryggir að nægur tími er fyrir smásala til að ganga frá pöntuninni áður en hún er tilbúin til að verða sótt. Eiginleikinn **Hámarksdagar** tryggir að notendur geti ekki valið dagsetningu sem er of langt fram í tímann. Til dæmis, ef lágmarksgildið er stillt á **1**, og pöntun er gerð 20. september, er fyrsti dagurinn sem verður hægt að sækja pöntunina næsti gjaldgengi dagur (21. september). Á svipaðan hátt, með því að stilla hámarksgildi, er hægt að skilgreina hámarksfjölda daga sem hægt verður að sækja pöntunina. Þegar lágmarks- og hámarksgildin eru skilgreind geta notendur svæðisins séð og valið aðeins tiltekinn fjölda daga í greiðsluferlinu.

    Hægt er að stilla lágmarksgildið á tugagildi sem er minna en 1. Til dæmis ef hægt verður að sækja fjórum klukkustundum eftir að pöntun er gerð, skal stilla lágmarksgildið á **0,17** (= 4 ÷ 24, námundað upp í tvö aukasæti). Ef lágmarksgildið er hins vegar stillt á tugagildi sem eru hærra en 1, er það alltaf námundað í næstu heilu tölu. Til dæmis verður gildið **1,2** sléttað upp í **2**. Ef hámarksgildið er stillt á tugabrot er það á samma hátt alltaf sléttað. 

- **Upphafsdagsetning** og **Lokadagsetning** – Tilgreinið upphafs- og lokadagsetningar tímahólfsins. Hver tímafærsla er með upphafsdag og lokadag. Þess vegna er sveigjanleikinn til staðar til að bæta við mismunandi tímahólfum yfir árið (til dæmis það sem verður sótt á frídögum). Ef upphafs- og lokadagsetning tímahólfs er breytt eftir að pöntun er gerð munu breytingarnar ekki eiga við þá pöntun. Þegar upphafs- og lokadagsetningar eru skilgreindar þarf að taka tillit til dagsetninga þegar verslun er lokið (t.d. jóladag) og tryggja að tímahólf séu ekki skilgreind fyrir þessa daga.
- **Virkar klukkustundir afhendingar** – Tilgreinið tímabilið þegar leyft er að sækja. Til dæmis gæti afgreiðslutími verið á milli 14:00 og 17:00 hvern dag. Þessi eiginleiki gerir kleift að hafa afhendingartíma óháðan opnunartíma verslunar. Þar af leiðandi getur smásali skilgreint afhendingartíma sem hentar viðskiptaþörfum hans. Þegar virkur tími er skilgreindur fyrir sótta pöntun þarf að taka tillit til opnunartíma verslunar og ganga úr skugga um að afhendingartímar séu ekki skilgreindir fyrir tíma þegar verslunin er lokuð.

    > [!NOTE]
    > Skilgreina þarf tímana fyrir sótta pöntun úr verslun í tímabelti viðeigandi verslunar.

- **Tímabil tímahólfs** - Tilgreinið tímalengdina sem hægt verður að úthluta hverju tímahólfi. Til dæmis gæti tímalengd hvers tímahólfs verið stigvaxandi frá 15 mínútum, 30 mínútur, eða einni klukkustund. Ef gildi tímahólfs er 0 er tímahólfið í boði fyrir alla tímalengd milli upphafs- og lokatíma.
- **Hólf á tímabil** - Tilgreinið fjölda viðskiptavina eða pantanir sem hægt verður að afgreiða þegar er sótt í hverju tímabili tímahólfs. Til dæmis skal slá inn **1**, **2**, **3** eða aðrar heiltölur.
- **Virkir dagar** – Tilgreinið daga vikunnar þegar tímahólf afhendingar eru virk. Þessi eiginleiki gerir söluaðila kleift að skilgreina dagana þegar hann vill þjónusta pantanir sem verða sóttar.
- **Smásölurásir** - Tilgreinið smásölurásir. Hvert tímahólf er hægt að tengja við eina eða fleiri smásöluverslanir. Hægt er að stofna eina eða fleiri tímahólfsfærslur, allt eftir opnunartíma hverrar verslunar, og tengja við rásina. 

<!-- ![HQ Timeslot overview.](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

Aðeins er hægt að grunnstilla eitt tímasniðmát fyrir hverja rás. Þessar rásir innihalda verslanir á staðnum, símaver, farsíma og netverslunarsíður.

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a>Skilgreina eiginleika tímahólfsins í Commerce Headquarters

Tilgreina verður tímahólf fyrir hvern afhendingarmáta í Commerce Headquarters þannig að sá sölustaður og netverslunarrásir geta vísað á þá.

- Aðeins er hægt að tengja eitt sniðmát tímahólfs við hverja verslun eða rás.
- Hvert tímahólf sem er stofnað ætti að vera einkvæmt fyrir hvern afhendingarmáta í hverju sniðmáti.
- Þegar búið er að skilgreina eiginleika tímahólfsins, verður dagatal tímahólfsins gert aðgengilegt fyrir valdar verslanir eða hópa verslunar. Það verður líka sýnilegt á sölustaðnum til viðmiðunar.

Til að skilgreina eiginleika tímahólfsins í Commerce Headquarters skal fylgja þessum skrefum.

1. Farið í **Commerce** \> **Uppsetning rásar** \> **Tímahólf afhendingar í verslun**.
1. Velja skal **Nýtt** til að búa til nýtt sniðmát tímahólfs. Veldu sniðmátið í vinstri glugganum til að nota sniðmát sem fyrir er.
1. Færið inn gildi í reitina **Kenni tímahólfs** og **Lýsing**.
1. Í flýtiflipanum **Pöntun sótt - Tímastillingar** skal velja **Bæta við**.
1. Í svarglugganum **Pöntun sótt - Tímastillingar** skal skilgreina dagsetningabilið, afhendingarmátann, virkan tíma afhendingar, virka daga, tímabil tímahólfs, hólf á hvert tímabil og aðrar stillingar.

    Ef tímahólf eiga að vera óbreytt í ókominni framtíð skal stilla reitinn **Lokadagsetning** á **Aldrei**.

    > [!NOTE]
    > Hægt er að búa til mörg sniðmát en aðeins má tengja eitt sniðmát við eina rás eða verslun.

    ![Svargluggi fyrir Pöntun sótt - Tímastillingar.](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. Þegar þessu er lokið skal velja **Í lagi**.
1. Ef tímahólf yfir daginn eru breytileg skal búa til fleiri færslur í flýtiflipanum **Pöntun sótt - Tímastillingar** til að ganga úr skugga um að dagsetningar og tímar skarist ekki.
1. Í flýtiflipanum **Smásölurásir** skal velja **Bæta við** til að tengja sniðmát tímahólfs við verslanir eða rásir þar sem það verður notað.
1. Í svarglugganum **Veljið fyrirtækjahnúta** skal nota örvarhnappana til að velja (eða hreinsa valið á) verslanir, svæði og fyrirtæki sem sniðmátið á að tengjast.

    <!-- ![HQ Timeslot overview.](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. Þegar þessu er lokið skal velja **Í lagi**.
1. Á síðunni **Dreifingaráætlun** skal keyra verkin **1070** og **1135** til að samstilla gögn til rásanna.

## <a name="time-slot-selection-for-pos-orders"></a>Val tímahólfs fyrir pantanir sölustaðar

Á sölustaðnum, þegar pöntun eða pöntunarlína er auðkennd fyrir sótta pöntun, getur gjaldkeri valið verslun eða staðsetningu afhendingar og dagsetningu og tímahólf. Ef viðskiptavinur er með tínslupöntun fyrir aðra verslun getur gjaldkerinn valið dagsetningar þegar tínslan verður tiltæk í þeirri verslun. Uppfletting verslunarinnar mun veita tilvísun í dagsetningar og tíma verslana.

Eftirfarandi mynd sýnir dæmi um val á tímahólfi fyrir pöntun sölustaðar.

![Dæmi um val á tímahólfi fyrir sölustaðarpöntun.](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a>Val á tímahólfi fyrir pantanir rafrænna viðskipta

Upplýsingar um hvernig hægt er að gera val á tímahólfi aðgengilegt fyrir pantanir rafrænna viðskipta er að finna í [Upplýsingar um sótta pöntun](../pickup-info-module.md).

> [!NOTE]
> Notendur geta aðeins skoðað eða breytt tímahólfum sóttra pantana á greiðsluferlissíðu verslunarsvæðis ef upplýsingar um sótta pöntun hefur verið bætt við þá síðu. Ef greiðsluferlissíðan inniheldur ekki upplýsingaeiningu sóttrar pöntunar, verða pantanir gerðar án þess að leyfa notendum að tilgreina eða skoða upplýsingar um tímahólf.

Eftirfarandi mynd sýnir dæmi um rafræna pöntun þar sem tímahólf sóttrar pöntunar hefur verið valið.

![Dæmi um rafræna pöntun þar sem tímahólf sóttrar pöntunar hefur verið valið.](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="time-slot-selection-for-call-center-orders"></a>Val tímahólfs fyrir pantanir símavers

Í símaforriti símavers geta fulltrúar símavers valið móttökuverslunina eða staðsetningu, ásamt dagsetningu og tímahólf sem auðkenndt er á eftirfarandi mynd.

![Dæmi um pöntun símavers þar sem tímahólf hefur verið valið.](../dev-itpro/media/Curbside_timeslot_callcenter.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Eining fyrir afhendingarupplýsingar](../pickup-info-module.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]