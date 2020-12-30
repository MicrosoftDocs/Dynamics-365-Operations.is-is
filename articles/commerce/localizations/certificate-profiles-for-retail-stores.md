---
title: Notandaskilgreint vottorðssnið fyrir smásöluverslanir
description: Í þessu efnisatriði er að finna yfirlit yfir hvernig vottorð eru notuð í smásöluverslunum.
author: josaw
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 75edc1b683c4ea6c2bac8e509e6f6da8c56c5e6a
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665248"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Notandaskilgreint vottorðssnið fyrir smásöluverslanir

[!include [banner](../includes/banner.md)]


## <a name="overview"></a>Yfirlit

Í þessu efnisatriði er að finna yfirlit yfir vottorðssnið sem eru í boði í Microsoft Dynamics 365 Commerce. Þessi virkni stækkar eiginleikann [Stjórna leynilyklum fyrir smásölurásir](../dev-itpro/manage-secrets.md) með því að bæta við stuðningi fyrir staðbundin vottorð.

Á meðan sölustaður er keyrður án nettengingar, er ekki hægt að fá aðgang að vottorðum sem eru geymd í lyklageymslunni. Nota ætti staðbundna vottorðið í staðinn. Eftirfarandi möguleikar eru studdir:

- Notkun staðbundinna vottorða í varaaðstæðum
- Notkun staðbundinna vottorða án lyklageymslu (t.d. í uppsetningu innanhúss)
- Stigvaxandi uppfærsla vottorða þar sem sumar verslanir og afgreiðslustöðvar nota nýja útgáfu vottorðsins, en aðrar verslanir og afgreiðslustöðvar halda áfram að nota fyrri útgáfuna

Með virkni vottorðssniðsins er hægt að tilgreina sjálfgefið vottorð og stilla röðina þannig að leitað sé í vottorðum í sama vottorðssniðinu. Þessi virkni býður einnig upp á svipaða uppsetningaraðferð fyrir staðbundin vottorð og lykilgeymsluvottorð. Hægt er að bæta við fyrirtækisstillingum fyrir vottorð, en einkvæmt auðkenni milli fyrirtækja fyrir hvert vottorð er hægt að nota í Commerce-rásum.

### <a name="scenarios"></a>Sviðsmyndir

Virkni vottorðssniðsins styður eftirfarandi aðstæður í Commerce-rásum:

- Notið staðbundið vottorð í varaaðstæðum lyklageymslu. Hér eru nokkur dæmi um þessar varaaðstæður:

    - Lyklageymsla er ekki aðgengileg.
    - Vottorð finnst ekki í lyklageymslu.
    - Sölustaður keyrir án nettengingar.

- Notið staðbundin vottorð, en án þess að geyma þau í lyklageymslu (til dæmis í uppsetningu innanhúss).
- Gerið stigvaxandi uppfærslu á vottorðum þar sem ný útgáfa vottorðsins er aðeins notað í verslunum eða afgreiðslustöðvum þar sem nýja útgáfan er þegar tiltæk.
- Notið sama vottorðið í mörgum fyrirtækjum.

## <a name="set-up-certificate-profiles"></a>Setja upp vottorðssnið

Eftirfarandi ferli lýsir hvernig setja á upp vottorðssnið. Áður en vottorðssnið er notað í Commerce-rásum skal fylgja þessum skrefum til að skilgreina stillingarnar.

1. Á vinnusvæðinu **Eiginleikastjórnun** skal kveikja á eiginleikanum **Notandaskilgreind vottorðssnið fyrir smásöluverslanir**.
2. Opnið **Kerfisstjórnun \> Uppsetning \> Vottorðssnið**.
3. Stofnið færslu og stillið reitina **Vottorðssnið**, **Heiti** og **Lýsing** fyrir hana.

    > [!NOTE]
    > Vottorðssniðið er einkvæmt kennimerki vottorðs í öllum þáttum fyrirtækja og Commerce.

3. Í flipanum **Lögaðilar** skal bæta við línu og velja lögaðilann (fyrirtækið) sem á að nota núverandi vottorðssnið fyrir. Ef nota á vottorðssniðið fyrir marga lögaðila skal endurtaka þetta skref til að bæta við línu fyrir hvern viðbótarlögaðila.
4. Veljið **Stillingar** til að opna síðuna **Stillingar vottorðssniðs** þar sem hægt er að færa inn sérstakar stillingar fyrirtækis fyrir vottorðssniðið.

### <a name="certificate-profile-settings"></a>Vottorðssniðsstillingar

Þegar **Stillingar** eru valdar fyrir línur vottorðssniðs, birtist síðan **Stillingar vottorðssniðs**. Á þessari síðu er hægt að tilgreina hvaða vottorð er hægt að nota þegar kallað er á núverandi vottorðssnið í Commerce-rásum. Einnig er hægt að tilgreina röðina sem leita ætti að vottorðum í.

> [!NOTE]
> Reiturinn **Forgangur** er stilltur sjálfkrafa. Gildið **1** táknar hæsta forgang. Þegar nýrri línu er bætt við síðuna **Stillingar vottorðssniðs**, er forgangur hennar stilltur á töluna sem er einum hærri en forgangur fyrri línu. Til að breyta forgangi tiltekinnar línu skal velja línuna og velja síðan annaðhvort **Færa upp** til að auka forgang eða **Færa niður** til að færa niður forgangsröðina.

Þegar nýrri línu er bætt við síðuna **Stillingar vottorðssniðs** skal stilla eftirfarandi reiti:

- **Gerð staðsetningar** – Veljið staðsetningu þar sem vottorð er geymt. Þessi reitur er með tvö möguleg gildi: **Staðbundið vottorð** og **Lyklageymsla**.
- **Vottorð lyklageymslu** - Þessi reitur er áskilinn ef reiturinn **Gerð staðsetningar** er stilltur á **Lyklageymsla**. Notið hann til að tilgreina leynilykil vottorðs í lyklageymslu.

    > [!NOTE]
    > Áður en vottorð lyklageymslu er notað í vottorðssniðum, skal fyrst hlaða upp vottorði í lyklageymsluna og fylgja leiðbeiningunum í [Setja upp biðlara Azure-lyklageymslu](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client).

- **Heiti verslunar** – Þessi reitur er valfrjáls og er aðeins aðgengilegur ef reiturinn **Gerð staðsetningar** er stilltur á **Staðbundið vottorð**. Notið hann til að tilgreina sjálfgefið heiti verslunar sem á að nota til að leita að staðbundnum vottorðum.
- **Staðsetning verslunar** – Þessi reitur er valfrjáls og er aðeins aðgengilegur ef reiturinn **Gerð staðsetningar** er stilltur á **Staðbundið vottorð**. Notið hann til að tilgreina sjálfgefna staðsetningu verslunar sem á að nota til að leita að staðbundnum vottorðum.

    > [!NOTE]
    > Sjálfgefnu heiti verslunar og sjálfgefinni staðsetningu verslunar er bætt við til að einfalda ferlið við að leita að staðbundnum vottorðum í Commerce Runtime. X509StoreProvider er með lista yfir möppur þar sem vottorð eru geymd. Ef sjálfgefið heiti verslunar og sjálfgefin staðsetning verslunar eru ekki tilgreind reynir X509StoreProvider að finna vottorð í öðrum möppum í listanum sínum.

- **Fingrafar** – Þessi reitur er áskilinn og aðeins aðgengilegur ef reiturinn **Gerð staðsetningar** er stilltur á **Staðbundið vottorð**. Notið hann til að tilgreina fingrafar vottorðs.
- **Athugasemdir** – Þetta svæði er valfrjálst og gerir notendum kleift að færa inn athugasemdir.

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Verkflæði: Leita að vottorðum í Commerce Runtime

Hér er grunnverkflæðið sem er notað til að leita að vottorði þegar kallað er á vottorðssnið í Commerce Runtime.

1. Kerfið segir til um hvort vottorðssniðið sé með fyrirtækisstillingar fyrir núverandi lögaðila.
1. Kerfið reynir að finna vottorð með því að nota gildin á síðunni **Stillingar vottorðssniðs** fyrir línuna þar sem reiturinn **Forgangur** er stilltur á **1**.

    - Ef reiturinn **Gerð staðsetningar** er stilltur á **Lyklageymsla** er gildið í reitnum **Leynilykill vottorðs í lyklageymslu** notað til að leita að vottorðinu á síðunni **Færibreytur lyklageymslu**. Síðan er leitað í vottorðinu í lyklageymslunni.
    - Ef reiturinn **Gerð staðsetningar** er stilltur á **Staðbundið vottorð** leitar X509StoreProvider fyrst að vottorðinu með því að nota sjálfgefið heiti og staðsetningu verslunar, ef þessar færibreytur eru tilgreindar. Það leitar síðan í öllum öðrum möppum á listanum sínum yfir möppur.

1. Ef vottorðið finnst ekki er ferlið endurtekið fyrir línuna þar sem reiturinn **Forgangur** er stilltur á **2** og svo framvegis.

> [!NOTE]
> Ef vottorðssniðið er með engar stillingar fyrir núverandi lögaðila, eða ef vottorðaleitin skilar ekki árangri fyrir allar línur á síðunni **Stillingar vottorðssniðs**, finnst vottorðið ekki.

#### <a name="caching-the-results-of-certificate-searches"></a>Niðurstöður vottorðaleitar vistaðar í skyndiminni

Niðurstöður vottorðaleitar eru vistaðar í skyndiminni. Sjálfgefinn gildistími fyrir vistun í skyndiminni er ein klukkustund. Hins vegar er hægt að sérstilla þennan tíma og stilla hann á allt að 24 klst.

### <a name="gradual-update"></a>Stigvaxandi uppfærsla

Ef ný útgáfa af vottorðinu er kynnt til sögunnar, en ekki hægt að uppfæra hana í öllum verslunum á sama tíma, gerir virkni vottorðssniðsins vottorðinu kleift að uppfærast í áföngum.

1. Finnið vottorðssnið og línuna sem á að uppfæra og veljið síðan **Stillingar**.
1. Bætið við línu og tilgreinið stillingar sem tengjast nýjustu útgáfu vottorðsins.
1. Hækkið gildi **Forgangs** fyrir nýju línuna. Notið hnappinn **Færa upp** til að færa línuna þannig að hún sé fyrir ofan línuna fyrir fyrri útgáfu af sama vottorðinu.

> [!NOTE]
> Í Commerce Runtime verður fyrst kallað á nýju útgáfu vottorðsins. Ef vottorðið hefur ekki verið uppfært enn sem komið er í tiltekinni verslun er afgreiðslustöð, verður kallað á fyrri útgáfuna.
