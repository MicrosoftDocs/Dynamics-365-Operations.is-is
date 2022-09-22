---
title: Notandaskilgreint vottorðssnið fyrir smásöluverslanir
description: Þessi grein veitir yfirlit yfir vottorðasniðin sem eru fáanleg í Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: v-chgriffin
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.search.industry: Retail
ms.search.form: RetailFormLayout, RetailParameters
ms.openlocfilehash: 5baf043a43210d819b605546089e981c86922ca9
ms.sourcegitcommit: 4f28f262cfb8f047cb5c0070261aa0748835e74b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/21/2022
ms.locfileid: "9558438"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Notandaskilgreint vottorðssnið fyrir smásöluverslanir

[!include [banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir vottorðasniðin sem eru fáanleg í Microsoft Dynamics 365 Commerce. Þessi virkni stækkar eiginleikann [Stjórna leynilyklum fyrir smásölurásir](../dev-itpro/manage-secrets.md) með því að bæta við stuðningi fyrir staðbundin vottorð.

Á meðan sölustaðurinn (POS) er í gangi í ótengdum ham hefur hann ekki aðgang að skírteinunum sem eru geymd í Microsoft Azure Lyklahólf. Nota ætti staðbundna vottorðið í staðinn. Eftirfarandi möguleikar eru studdir:

- Notkun staðbundinna skírteina í Key Vault varatilvikum
- Notkun staðbundinna skírteina án Key Vault (til dæmis í uppsetningu á staðnum)
- Stigvaxandi uppfærsla vottorða þar sem sumar verslanir og afgreiðslustöðvar nota nýja útgáfu vottorðsins, en aðrar verslanir og afgreiðslustöðvar halda áfram að nota fyrri útgáfuna

Með virkni vottorðssniðsins er hægt að tilgreina sjálfgefið vottorð og stilla röðina þannig að leitað sé í vottorðum í sama vottorðssniðinu. Þessi virkni býður einnig upp á svipaða uppsetningaraðferð fyrir staðbundin vottorð og lykilgeymsluvottorð. Hægt er að bæta við fyrirtækisstillingum fyrir vottorð, en einkvæmt auðkenni milli fyrirtækja fyrir hvert vottorð er hægt að nota í Commerce-rásum.

### <a name="scenarios"></a>Sviðsmyndir

Virkni vottorðssniðsins styður eftirfarandi aðstæður í Commerce-rásum:

- Notaðu staðbundið vottorð í Key Vault varatilvikum. Hér eru nokkur dæmi um þessar varaaðstæður:

    - Lyklageymsla er ekki aðgengileg.
    - Vottorð finnst ekki í lyklageymslu.
    - Sölustaður keyrir án nettengingar.

- Notaðu staðbundin vottorð, en án þess að geyma þau í Key Vault (til dæmis í uppsetningu á staðnum).
- Gerið stigvaxandi uppfærslu á vottorðum þar sem ný útgáfa vottorðsins er aðeins notað í verslunum eða afgreiðslustöðvum þar sem nýja útgáfan er þegar tiltæk.
- Notið sama vottorðið í mörgum fyrirtækjum.

## <a name="set-up-certificate-profiles"></a>Setja upp vottorðssnið

Eftirfarandi ferli lýsir hvernig setja á upp vottorðssnið.

### <a name="set-up-key-vault"></a>Settu upp Key Vault

Ljúka verður eftirfarandi skrefum áður en hægt er að nota stafrænt skilríki sem er geymt í Key Vault.

1. Búðu til Key Vault geymslureikning. Við mælum með því að þú setjir geymslureikninginn á sama landfræðilega svæði og Commerce Scale Unit.
1. Hladdu upp stafræna vottorðinu á Key Vault geymslureikninginn.
1. Leyfðu Application Object Server (AOS) forritinu til að lesa leyndarmál frá Key Vault geymslureikningnum.

Fyrir frekari upplýsingar um hvernig á að vinna með Key Vault, sjá [Byrjaðu með Azure Key Vault](/azure/key-vault/key-vault-get-started).

### <a name="set-up-system-parameters"></a>Setja upp kerfisfæribreytur

Áður en þú stillir vottorðasnið í viðskiptarásum verður þú að virkja Commerce til að nota bæði vottorð sem eru geymd í Key Vault og vottorðssnið.

Til að setja upp kerfisfæribreytur í höfuðstöðvum Commerce skaltu fylgja þessum skrefum.

1. Á **Kerfisbreytur** síðu, stilltu **Notaðu háþróaða vottorðaverslun** valmöguleika til **Já**.
1. Á vinnusvæðinu **Eiginleikastjórnun** skal kveikja á eiginleikanum **Notandaskilgreind vottorðssnið fyrir smásöluverslanir**.

### <a name="set-up-key-vault-parameters"></a>Settu upp færibreytur Key Vault

Á **Helstu færibreytur Vault** síðu, verður þú að tilgreina eftirfarandi færibreytur til að fá aðgang að Key Vault geymslunni:

- **Nafn** og **Lýsing** – Nafn og lýsing á Key Vault geymslureikningnum.
- **Vefslóð lykilhólfs** – Vefslóð Key Vault geymslureikningsins.
- **Key Vault viðskiptavinur** – Gagnvirkt auðkenni viðskiptavinarins Azure Active Directory (Azure AD) forrit sem er tengt við Key Vault geymslureikninginn í auðkenningarskyni. Þessi viðskiptavinur ætti að hafa aðgang til að lesa leyndarmál af geymslureikningnum.
- **Key Vault leynilykill** – Leynilykill sem er tengdur við Azure AD forrit sem er notað til auðkenningar í Key Vault geymslureikningnum.
- **Nafn**, **·**, og **Leynileg tilvísun** – Nafn, lýsing og leynileg tilvísun skírteinisins.

Fyrir frekari upplýsingar, sjá [Settu upp Azure Key Vault biðlarann](../../finance/localizations/setting-up-azure-key-vault-client.md).

### <a name="configure-a-certificate-profile"></a>Stilltu vottorðssnið

Til að stilla vottorðssnið í höfuðstöðvum Commerce skaltu fylgja þessum skrefum.

1. Opnið **Kerfisstjórnun \> Uppsetning \> Vottorðssnið**.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að búa til færslu.
1. Sláðu inn gildi í **Vottorðsprófíll**, **·**, og **Lýsing** sviðum.

    > [!NOTE]
    > Vottorðssniðið er einkvæmt kennimerki vottorðs í öllum þáttum fyrirtækja og Commerce.

1. Á **Lögaðilar** Flýtiflipi, veldu **Bæta við** til að bæta við línu.
1. Undir **Lögaðili**, veldu lögaðilann (fyrirtækið) sem núverandi vottorðssnið ætti að nota fyrir.

    Ef nota ætti vottorðssniðið fyrir marga lögaðila, endurtakið skref 4 og 5 til að bæta við línu fyrir hvern viðbótar lögaðila.

1. Veljið **Stillingar** til að opna síðuna **Stillingar vottorðssniðs** þar sem hægt er að færa inn sérstakar stillingar fyrirtækis fyrir vottorðssniðið. Tilgreindu hvaða vottorð er hægt að nota þegar núverandi vottorðssnið er kallað í viðskiptarásum. Bættu við eins mörgum vottorðum og þú þarft og settu forgangsröðun fyrir þau. Ef skírteini sem hefur meiri forgang er ekki tiltækt verður næsta vottorð notað, byggt á forgangi. Fyrir frekari upplýsingar, sjá [Verkflæði: Leita að vottorðum í Commerce runtime](#workflow-searching-certificates-in-the-commerce-runtime) kafla.

    > [!NOTE]
    > Reiturinn **Forgangur** er stilltur sjálfkrafa. Gildið **1** táknar hæsta forgang. Þegar nýrri línu er bætt við síðuna **Stillingar vottorðssniðs**, er forgangur hennar stilltur á töluna sem er einum hærri en forgangur fyrri línu. Til að breyta forgangi tiltekinnar línu skal velja línuna og velja síðan annaðhvort **Færa upp** til að auka forgang eða **Færa niður** til að færa niður forgangsröðina.

1. Þegar þú bætir við nýrri línu á **Stillingar vottorðssniðs** síðu, stilltu eftirfarandi reiti:

    - **Gerð staðsetningar** – Veljið staðsetningu þar sem vottorð er geymt. Þessi reitur er með tvö möguleg gildi: **Staðbundið vottorð** og **Lyklageymsla**.
    - **Vottorð lyklageymslu** - Þessi reitur er áskilinn ef reiturinn **Gerð staðsetningar** er stilltur á **Lyklageymsla**. Notið hann til að tilgreina leynilykil vottorðs í lyklageymslu.
    - **Heiti verslunar** – Þessi reitur er valfrjáls og er aðeins aðgengilegur ef reiturinn **Gerð staðsetningar** er stilltur á **Staðbundið vottorð**. Notið hann til að tilgreina sjálfgefið heiti verslunar sem á að nota til að leita að staðbundnum vottorðum.
    - **Staðsetning verslunar** – Þessi reitur er valfrjáls og er aðeins aðgengilegur ef reiturinn **Gerð staðsetningar** er stilltur á **Staðbundið vottorð**. Notið hann til að tilgreina sjálfgefna staðsetningu verslunar sem á að nota til að leita að staðbundnum vottorðum.

        > [!NOTE]
        > Sjálfgefnu heiti verslunar og sjálfgefinni staðsetningu verslunar er bætt við til að einfalda ferlið við að leita að staðbundnum vottorðum í Commerce Runtime. X509StoreProvider er með lista yfir möppur þar sem vottorð eru geymd. Ef sjálfgefið verslunarheiti og sjálfgefin staðsetning verslunar eru ekki tilgreind, reynir X509StoreProvider að finna vottorð í hinum möppunum á listanum. Fyrir frekari upplýsingar um tiltæk gildi fyrir heiti verslunar og staðsetningu verslunar, sjá [StoreName Enum](/dotnet/api/system.security.cryptography.x509certificates.storename) og [StoreLocation Enum](//dotnet/api/system.security.cryptography.x509certificates.storelocation).

    - **Þumalfingursprent** – Þessi reitur er nauðsynlegur og er aðeins tiltækur ef þú stillir á **Staðsetningargerð** sviði til **Staðbundið vottorð**. Notið hann til að tilgreina fingrafar vottorðs.

        > [!IMPORTANT]
        > Þú verður að tryggja að notandinn sem keyrir forritið sem þarf að nota staðbundið vottorð (til dæmis Modern POS í ótengdri stillingu) hafi að minnsta kosti skrifvarinn aðgang að einkalyklinum vottorðsins.

    - **Athugasemdir** – Þetta svæði er valfrjálst og gerir notendum kleift að færa inn athugasemdir.

## <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Verkflæði: Leita að vottorðum í Commerce Runtime

Hér er grunnverkflæðið sem er notað til að leita að vottorði þegar kallað er á vottorðssnið í Commerce Runtime.

1. Kerfið segir til um hvort vottorðssniðið sé með fyrirtækisstillingar fyrir núverandi lögaðila.
1. Kerfið reynir að finna vottorð með því að nota gildin á síðunni **Stillingar vottorðssniðs** fyrir línuna þar sem reiturinn **Forgangur** er stilltur á **1**.

    - Ef reiturinn **Gerð staðsetningar** er stilltur á **Lyklageymsla** er gildið í reitnum **Leynilykill vottorðs í lyklageymslu** notað til að leita að vottorðinu á síðunni **Færibreytur lyklageymslu**. Síðan er leitað í vottorðinu í lyklageymslunni.
    - Ef reiturinn **Gerð staðsetningar** er stilltur á **Staðbundið vottorð** leitar X509StoreProvider fyrst að vottorðinu með því að nota sjálfgefið heiti og staðsetningu verslunar, ef þessar færibreytur eru tilgreindar. Það leitar síðan í öllum öðrum möppum á listanum sínum yfir möppur.

1. Ef vottorðið finnst ekki er ferlið endurtekið fyrir línuna þar sem reiturinn **Forgangur** er stilltur á **2** og svo framvegis.

> [!NOTE]
> Ef vottorðssniðið er með engar stillingar fyrir núverandi lögaðila, eða ef vottorðaleitin skilar ekki árangri fyrir allar línur á síðunni **Stillingar vottorðssniðs**, finnst vottorðið ekki.

### <a name="caching-the-results-of-certificate-searches"></a>Niðurstöður vottorðaleitar vistaðar í skyndiminni

Niðurstöður vottorðaleitar eru vistaðar í skyndiminni. Sjálfgefinn gildistími fyrir vistun í skyndiminni er ein klukkustund. Hins vegar er hægt að sérstilla þennan tíma og stilla hann á allt að 24 klst.

## <a name="gradual-update"></a>Stigvaxandi uppfærsla

Ef ný útgáfa af vottorðinu er kynnt til sögunnar, en ekki hægt að uppfæra hana í öllum verslunum á sama tíma, gerir virkni vottorðssniðsins vottorðinu kleift að uppfærast í áföngum.

1. Finnið vottorðssnið og línuna sem á að uppfæra og veljið síðan **Stillingar**.
1. Bætið við línu og tilgreinið stillingar sem tengjast nýjustu útgáfu vottorðsins.
1. Hækkið gildi **Forgangs** fyrir nýju línuna. Notið hnappinn **Færa upp** til að færa línuna þannig að hún sé fyrir ofan línuna fyrir fyrri útgáfu af sama vottorðinu.
> [!NOTE]
> Í Commerce Runtime verður fyrst kallað á nýju útgáfu vottorðsins. Ef vottorðið hefur ekki verið uppfært enn sem komið er í tiltekinni verslun er afgreiðslustöð, verður kallað á fyrri útgáfuna.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
