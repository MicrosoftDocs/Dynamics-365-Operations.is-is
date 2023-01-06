---
title: Hanna nýja rafræna skýrslugerðarlausn til að prenta ZPL-merki
description: Í þessari grein er útskýrt hvernig á að hanna nýja rafræna skýrslugerðarlausn til að prenta merki Zebra-forritunarmáls (ZPL).
author: kfend
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: 10.0.26
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 7ef83cf4822ca129af3ca01fa6ddd05219fee0d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271764"
---
# <a name="design-a-new-er-solution-to-print-zpl-labels"></a>Hanna nýja rafræna skýrslugerðarlausn til að prenta ZPL-merki

[!include [banner](../includes/banner.md)]


Þessi grein útskýrir hvernig notandi í hlutverki kerfisstjóra, hönnuðar rafrænnar skýrslugerðar eða hagnýts ráðgjafa rafrænnar skýrslugerðar getur skilgreint færibreytur fyrir ramma [rafrænnar skýrslugerðar](general-electronic-reporting.md), hannað nauðsynlegar [skilgreiningar](general-electronic-reporting.md#Configuration) rafrænnar skýrslugerðar fyrir nýja lausn rafrænnar skýrslugerðar til að fá aðgang vöruhúsakerfinu og útbúið sérsniðna merkimiða vöruhúsastaðsetningar ZPL II-sniði. Hægt er að ljúka skrefunum í **USRT** fyrirtækinu.

## <a name="business-scenario"></a>Sviðsmynd fyrirtækis

Þú ert fulltrúi fyrirtækis sem innleiddi vöruhúsakerfi í Microsoft Dynamics 365 Finance. Allir vöruhúsastaðsetningar verða að vera merktar með límmiða með strikamerki. Starfsmenn vöruhúss munu nota strikamerkjalesara til að skanna strikamerkin.

Allar vöruhúsastaðsetningar hafa verið merktar í umfangi aðgerða fyrir keyrslu. Samt sem áður þarftu einnig að geta prentað merki vöruhúsastaðsetninga eftir þörfum ef núverandi merki skemmast eða hillum vöruhúss er endurraðað. Með því að nota nýlega útgefna virkni rafrænnar skýrslugerðar er hægt að skilgreina nýja lausn rafrænnar skýrslugerðar sem gerir umsjónarmanni vöruhúss kleift að prenta merki beint á prentara sem prentar thermal-merkimiða.

## <a name="configure-the-er-framework"></a>Skilgreina ramma rafrænnar skýrslugerðar

Fylgdu skrefunum í [Skilgreina ramma rafrænnar skýrslugerðar](er-quick-start2-customize-report.md#ConfigureFramework) til að setja upp lágmarksfjölda af færibreytum rafrænnar skýrslugerðar. Þú verður að ljúka þessari uppsetningu áður en þú byrjar að nota ramma rafrænnar skýrslugerðar til að hanna nýja lausn rafrænnar skýrslugerðar.

## <a name="design-a-domain-specific-data-model"></a>Hanna gagnalíkan fyrir sérstakt lén

Stofna nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur [gagnalíkansíhlut](er-overview-components.md#data-model-component) fyrir lén vöruhúsakerfisins. Þetta gagnalíkan verður seinna notað sem gagnagjafi þegar hannað er snið rafrænnar skýrslugerðar til að búa til merkimiða fyrir staðsetningu vöruhúss.

### <a name="import-a-data-model-configuration"></a>Flytja inn skilgreiningu gagnalíkans

Fylgdu eftirfarandi skrefum til að flytja inn nauðsynlegt gagnalíkan úr XML-skrá sem Microsoft lætur í té. Þú getur einnig búið til þitt eigið gagnalíkan eins og lýst er í næsta hluta.

1. Sæktu skrána [Warehouse model.version.1.xml](https://download.microsoft.com/download/9/f/1/9f136e9b-bf5f-403a-b089-a2b2ed1da2ba/Warehouse-model.version.1.xml) og vistaðu hana á staðbundinni tölvu.
2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.
4. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, skal velja **Skipta út**\>**Hlaða úr XML-skrá**.
5. Veljið **Fletta** og finnið síðan og veljið skrána **Warehouse model.version.1.xml**.
6. Veljið **Í lagi** til að flytja inn skilgreininguna.

![Innflutt skilgreining gagnalíkans rafrænnar skýrslugerðar á skilgreiningasíðunni.](./media/er-design-zpl-labels-imported-model.png)

### <a name="create-a-data-model-configuration"></a>Stofnaðu nýja skilgreiningu gagnalíkans

Í stað þess að flytja inn gagnalíkanaskrá frá Microsoft geturðu búið til gagnalíkan frá grunni. Dæmi sem sýnir hvernig á að ljúka þessu verki er að finna í [Stofna nýjan skilgreiningu gagnalíkans](er-quick-start1-new-solution.md#DesignDataModel).

### <a name="review-the-data-model"></a>Fara yfir gagnalíkanið

Hægt er að skoða breytanlega útgáfu af skilgreindu gagnalíkani á síðunni **Hönnuður gagnalíkans**.

![Uppbygging gagnalíkans rafrænnar skýrslugerðar á síðu hönnuðar gagnalíkansins.](./media/er-design-zpl-labels-model.png)

## <a name="design-a-model-mapping-for-the-configured-data-model"></a>Hanna líkanavörpun fyrir skilgreint gagnalíkan

Sem notandi í hönnunarhlutverki rafrænnar skýrslugerðar þarf að stofna nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur íhlut [líkanavörpunar](er-overview-components.md#model-mapping-component) fyrir vöruhússgagnalíkanið. Þessi hluti innleiðir skilgreinda gagnalíkanið fyrir Dynamics 365 Finance og er einungis notað í því forriti. Skilgreining er nauðsynleg til að tilgreina hugbúnaðarhluti sem þarf að nota til að fylla út skilgreint gagnalíkan með forritsgögnum við keyrslu. Til að ljúka þessu verki verður þú að skilja hvernig gagnauppbygging fyrir viðskiptalén vöruhúsakerfis er útfærð í Finance.

### <a name="import-a-model-mapping-configuration"></a>Flytja inn skilgreiningar líkanavörpunar

Fylgdu þessum skrefum til að flytja inn nauðsynlega vörpun líkans úr XML-skrá sem Microsoft lætur í té. Einnig er hægt að búa til sína eigin líkanavörpun eins og lýst er í næsta hluta.

1. Sækið skrána [Warehouse model mapping.version.1.1.xml](https://download.microsoft.com/download/1/c/c/1cc94d28-3d90-4ffd-a118-77d6c322904f/Warehouse-model-mapping.version.1.1.xml) og vistið hana á staðbundinni tölvu.
2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.
4. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, skal velja **Skipta út**\>**Hlaða úr XML-skrá**.
5. Veljið **Fletta** og finnið síðan og veljið skrána **Warehouse model mapping.version.1.1.xml**.
6. Veljið **Í lagi** til að flytja inn skilgreininguna.

![Innflutt skilgreining vörpunar líkans rafrænnar skýrslugerðar á skilgreiningasíðunni.](./media/er-design-zpl-labels-imported-mapping.png)

### <a name="create-a-model-mapping-configuration"></a>Stofna skilgreiningu líkanavörpunar

Í stað þess að flytja inn skrá líkanavörpunar frá Microsoft er hægt að búa til líkanavörpun frá grunni. Dæmi sem sýnir hvernig á að ljúka þessu verki er að finna í [Stofna nýja skilgreiningu líkanavörpunar](er-quick-start1-new-solution.md#CreateModelMapping).

### <a name="review-the-model-mapping"></a>Fara yfir líkanavörpun

Hægt er að skoða breytanlega stöðu skilgreindrar líkanavörpunar á síðunni **Hönnuður líkanavörpunar**.

![Skipan vörpunar líkans rafrænnar skýrslugerð á síðunni Hönnuður líkanavörpunar.](./media/er-design-zpl-labels-mapping.png)

## <a name="design-a-format"></a>Setja upp snið

Sem notandi í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar þarf að stofna nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur [sniðs](er-overview-components.md#format-component) hluta. Til að skilgreina þennan þátt þarf að nota ZPL II kóða til að tilgreina útlitið á merki vöruhúsastaðsetningar.

### <a name="import-a-format-configuration"></a>Flytja inn skilgreiningu sniðs

Fylgdu þessum skrefum til að flytja inn áskilið snið úr XML skrá sem Microsoft lætur í té. Einnig er hægt að búa til sitt eigið snið eins og lýst er í næsta hluta.

1. Sækið skrána [Warehouse location labels.version.1.1.xml](https://download.microsoft.com/download/5/7/5/5758b551-69a5-45bd-a2b2-21c3db73a6fc/Warehouse-location-labels.version.1.1.xml) og vistið hana á staðbundinni tölvu.
2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.
4. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, skal velja **Skipta út**\>**Hlaða úr XML-skrá**.
5. Veljið **Fletta** og finnið síðan og veljið skrána **Warehouse location labels.version.1.1.xml**.
6. Veljið **Í lagi** til að flytja inn skilgreininguna.

![Innflutt skilgreining sniðs rafrænnar skýrslugerðar á skilgreiningasíðunni.](./media/er-design-zpl-labels-imported-format.png)

### <a name="create-a-format-configuration"></a>Stofna skilgreiningu sniðs

Í stað þess að flytja inn sniðsskrá frá Microsoft er hægt að búa til eigið snið frá grunni. Dæmi sem sýnir hvernig á að ljúka þessu verki er að finna í [Stofna nýja skilgreiningu á sniði](er-quick-start1-new-solution.md#FormatCreate).

### <a name="review-the-format"></a>Yfirfara snið

Hægt er að skoða breytanlega útgáfu af skilgreinda sniðinu á síðunni **Sniðshönnuður**.

![Skipan rafræns skýrslugerðarsniðs á sniðshönnunarsíðunni.](./media/er-design-zpl-labels-format.png)

Gagnagjafi `model.Location.Label` þessa sniðs er skilgreindur til að búa til merki sem innihalda eftirfarandi upplýsingar:

- Titill vöruhúss sem texti
- Titill vöruhúss sem strikamerki
- Staðsetningarreiturinn
- Vartölur

Á síðunni **Formúluhönnuður** fyrir gagnagjafann inniheldur formúla rafrænnar skýrslugerðar, sem notuð er til að búa til merki, `CONCATENATE` virkni sem sameinar upplýsingar í æskilegu útliti.

![Formúla fyrir gagnagjafann á síðu Formúluhönnuðar.](./media/er-design-zpl-labels-review-formula.png)

> [!TIP]
> Útlit merkisins er hannað þannig að titill staðsetningar og vartölur eru fyrir miðju merkisins. ZPL II styður hins vegar ekki miðjustillingu fyrir strikamerki. Þess vegna er formúla `model.Location.Warehouse.Alignment` gagnagjafans notuð til að miðjujafna strikamerkið á merkinu. Þessi formúla reiknar vinstri hliðrun strikamerkisins út frá fjölda stafa í titli vöruhússins.

## <a name="prepare-your-environment-for-previewing-generated-labels"></a>Gerðu umhverfi þitt klárt fyrir forskoðun á merkjum

Eftirfarandi dæmi notar hermiforrit prentara fyrir ZPL-merki til að sýna forskoðun á mynduðum merkjum á skjánum. Fylgdu þessum skrefum til að virkja þennan valkost.

1. Bæta við viðtökustað rafrænnar skýrslugerðar [Prentari](er-destination-type-print.md) fyrir snið rafrænnar skýrslugerðar **Merkimiði staðsetningar vöruhúss** og skilgreina það til að senda myndaða merkimiða frá Finance til [Document Routing Agent (DRA)](install-document-routing-agent.md).
2. Settu upp og skilgreindu DRA til að leiða mynduð merki úr Finance til staðbundins prentara sem er aðgengilegur frá núverandi vinnustöð.
3. Bættu við staðbundnum prentara fyrir núverandi vinnustöð og skilgreina hann þannig að hann skili merkingum sem eru búnar til í DRA prentarahermiforrit.
4. Settu upp hermiforrit prentara sem viðbót við Chrome-vafrann og skilgreindu það til að flytja mynduð merki úr staðbundnum prentara til vefþjónustu sem mun myndþýða mynduð merki og skila þeim til prentarahermis til forskoðunar.

<table>
<tbody>
<tr align="center">
<td>
<p>Finance</p>
<p>Rafræn skýrsla</p>
<p>Viðtökustaður prentara</p>
</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from Finance to the DRA."></td>
<td>Document Routing Agent</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from the DRA to a local printer."></td>
<td>Staðbundinn prentari</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from a local printer to a printer emulator."></td>
<td>Prentarahermir</td>
<td><img src="./media/er-design-zpl-labels-flow2.png" alt="Data flow direction: from a printer emulator to a rendering web service and then back to the printer emulator."></td>
<td>Myndþýðingarvefþjónusta</td>
</td>
</tr>
</tbody>
</table>

### <a name="install-and-configure-a-printer-emulator-application"></a>Setja upp og skilgreina prentarahermisforrit

Bæta við prentarahermiforriti fyrir ZPL-myndþýðingarvélina í Chrome-vafrann. Þetta dæmi notar hermi [Zpl-prentara](https://chrome.google.com/webstore/detail/zpl-printer/phoidlklenidapnijkabnfdgmadlcmjo) sem byggir á [Labelary ZPL vefþjónustunni](http://labelary.com/service.html). Hermiforrit prentara mun flytja mynduð merki á ZPL-sniði frá staðbundnum prentara til vefþjónustu og síðan skila merkjum sem PDF- eða PNG-skrá til forskoðunar.

1. Finndu og veldu hermiforrit prentunar sem þú vilt nota í Chrome-vefversluninni. Veldu síðan **Bæta við Chrome** til að bæta því við Chrome vafrann.

    ![Að bæta prentarahermiforritinu við Chrome vafrann úr Chrome vefversluninni.](./media/er-design-zpl-labels-add-app.png)

2. Veldu **Ræsa forrit** til að keyra hermiforrit prentunar úr Chrome-vafranum.

    ![Keyrsla prentarahermiforritsins úr Chrome-vefvafranum.](./media/er-design-zpl-labels-run-app.png)

3. Skilgreina forritið sem keyrir:

    1. Slökkvið á forritinu.
    2. Stillið á hýsilinn á **127.0.0.1** stillingum prentarans.
    3. Stillið tengið á **9100**.

        ![Skilgreining á prentarahermiforritinu.](./media/er-design-zpl-labels-configure-app.png)

    4. Kveikið aftur á forritinu. Þú ættir að fá skilaboð um að prentarinn hafi verið ræstur á tilgreindum hýsli og gátt.

        ![Kveikt er aftur á prentarahermiforritinu.](./media/er-design-zpl-labels-turn-on-app.png)

> [!NOTE]
> Þar sem hermiforrit prentunar sem notað er í þessu dæmi treystir á vefþjónustu til að myndþýða merki skaltu ganga úr skugga um að öryggisstillingarnar þínar leyfi þér að eiga samskipti við þjónustuna. Annars mun forritið ekki fá myndþýtt merki og ekki verður boðið upp á forskoðun á þeim.

### <a name="add-and-configure-a-local-printer"></a>Bæta við og skilgreina staðbundinn prentara

[Bætið við nýjum staðbundnum prentara](https://support.microsoft.com/windows/install-a-printer-in-windows-10-cc0724cf-793e-3542-d1ff-727e4978638b) sem núverandi tæki getur notað til að senda merkingar frá DRA í prentarahermiforritið.

1. Í Windows skaltu velja **Byrja** \> **Stillingar** \> **Tæki** \> **Prentarar \& skannar**.
2. Veldu **Stillingar prentara \& skanna**.
3. Fyrir **Bæta við prentara eða skanna** skal velja **Bæta við tæki**.
4. Veljið **Bæta við** handvirkt fyrir **Prentarinn sem ég vil er ekki á listanum**.
5. Í reitnum **Finna prentara eftir öðrum valkostum** skal velja **Bæta staðbundnum prentara eða netprentara við handvirkar stillingar**.
6. Í reitnum **Velja prentaragátt** skal velja **Búa til nýja gátt** og síðan fylgja þessum skrefum:

    1. Í reitnum **Gerð tengis** skal velja **Hefðbundið TCP/IP-tengi**.
    2. Í reitinn **Heiti hýsils eða IP-tala** sláðu inn **127.0.0.1**.
    3. Í reitinn **Heiti tengis** skal færa inn **ZPL**.
    4. Bíddu þar til aðgerðinni **Greinir TCP/IP-tengi** er lokið.
    5. Í reitnum **Tegund tækis** skaltu velja **Sérsniðið** og velja síðan **Stillingar**.
    6. Ganga þarf úr skugga um að eftirfarandi tengistillingar séu tilgreindar:

        - **Heiti gáttar:** ZPL
        - **Heiti eða IP- tala prentara:** 127.0.0.1
        - **Samskiptareglur:** Raw
        - **Númer gáttar:** 9100

7. Í reitnum **Setja upp rekil prentarans** skal velja **Almennt / Texti eingöngu**.
8. Í reitinn **Heiti prentara** skal færa inn **ZebraPrinter**.

![Bæti við staðbundnum prentara fyrir núverandi tæki.](./media/er-design-zpl-labels-configure-printer.png)

### <a name="install-and-configure-the-dra"></a>Uppsetning og skilgreining DRA

Búðu DRA undir að flytja mynduð merki úr Finance til skilgreinds staðbundins prentara.

1. [Setja upp DRA](install-document-routing-agent.md#install-the-document-routing-agent).
2. [Skilgreina DRA](install-document-routing-agent.md#configure-the-document-routing-agent)
3. [Skráðu prentarann á staðnum](install-document-routing-agent.md#register-network-printers) í DRA.
4. [Virkja staðbundinn prentara](install-document-routing-agent.md#administer-network-printers) í Finance-umhverfinu þínu.

![Útbúa DRA til að prenta myndaða merkimiða.](./media/er-design-zpl-labels-configure-dra.png)

### <a name="configure-the-er-destination"></a>Skilgreina áfangastað Rafræn skýrslugerðar

Búðu endastað rafrænnar skýrslugerðar undir að flytja mynduð merki úr Finance til DRA.

1. Fara á **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Viðtökustaður rafrænnar skýrslugerðar**.
2. Á síðunni **Áfangastaður fyrir rafræna skýrslugerð**, á aðgerðasvæðinu, skal velja **Nýr**.
3. Í reitnum **Tilvísun** skal velja **Merkimiðar staðsetningar vöruhúss**.
4. Í flýtiflipanum **Viðtökustaður skráar** skal velja **Nýr**.
5. Í reitinn **Heiti** skal færa inn **Merkimiðar**.
6. Í reitnum **Heiti skráaríhlutar** skal velja **Skýrsla**.
7. Veldu **Stillingar**.
8. Í svarglugganum **Stillingar viðtökustaðar** í flipanum **Prentari** skal stilla valkostinn **Virkjað** á **Já**.
9. Í reitinn **Heiti prentara** velurðu **ZebraPrinter**.
10. Í reitnum **Skjalaleiðargerð** skal velja **ZPL**.
11. Veldu **Í lagi**.

![Skilgreining viðtökustað rafrænnar skýrslugerðar fyrir merkimiðasnið staðsetningar vöruhúss á viðtökusíðu rafrænnar skýrslugerðar.](./media/er-design-zpl-labels-configure-destination.png)

## <a name="review-warehouse-locations"></a>Fara yfir staðsetningar vöruhúsa

1. Opnaðu **Vöruhúsakerfi** \> **Uppsetning** \> **Vöruhús** \> **Staðsetningar**.
2. Á síðunni **Staðsetningar** skal sía til að skoða aðeins staðsetningar sem eru með gildi í reitnum **Vartölur**.

![Yfirfara staðsetningar vöruhúsa á síðunni Staðsetningar.](./media/er-design-zpl-labels-review-locations.png)

## <a name="print-warehouse-location-labels"></a>Prenta merkimiða staðsetningar vöruhúsa

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu, skal stækka **Vöruhússlíkan** og velja **Merkimiðar staðsetningar vöruhúss**.
3. Í aðgerðarúðunni skal velja **Keyra**.
4. Í svarglugganum **Færibreytur rafrænnar skýrslugerðar** á flipanum **Færslur til að taka með** skal velja **Sía**.
5. Á flipanum **Svið**, skal finna línuna þar sem reiturinn **Tafla** er stillt á **Staðsetningar** og reiturinn **Reitur** er stilltur á **Staðsetning**. Í reitinn **Skilyrði** skal færa inn **LPEnabled**.
6. Veldu **Í lagi**.
7. Veldu **Í lagi**. Merkimiði er búinn til og sýndur á forskoðunarsíðunni í prentarahermiforritinu.

![Farið yfir myndað merki á forskoðunarsíðunni fyrir hermiforrit Zpl-prentara.](./media/er-design-zpl-labels-preview-label.png)

## <a name="modify-the-layout-of-a-label"></a>Breyta útliti merkimiða

Hægt er að breyta núverandi útliti á staðsetningarmerkingum vöruhúss. Eftirfarandi dæmi sýnir hvernig á að breyta útliti þannig að mynduð merki innihalda auðkenni staðsetningarforstillingar.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Stilltu **Nota áfangastaði fyrir drög** [notandafæribreytu rafrænnar skýrslugerðar](electronic-reporting-destinations.md#applicability) á **Já**.
3. Á síðunni **Skilgreiningar**, í skilgreiningatrénu, skal stækka **Vöruhússlíkan** og velja **Merkimiðar staðsetningar vöruhúss**.
4. Veljið **Hönnuður**.
5. Á síðunni **Sniðshönnuður**, í flipanum **Vörpun**, skal velja `model.Location.Label`-gagnagjafann.
6. Í svarglugganum **Eiginleikar gagnagjafa** skal velja **Breyta** \> **Breyta formúlu**.
7. Á síðunni **Formúluhönnuður**, í reitnum **Formúla**, skal fara yfir formúlu rafrænnar skýrslugerðar sem notuð er til að mynda merkin.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^XZ")
    ```

8. Uppfærðu formúluna til að bæta auðkenni staðsetningarsniðs við tilkomnar merkingar.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^CF0,40,40^FO0,240^FB800,1,0,C,0^FD",@.ProfileID,"\&^FS",CrLf,
    "^XZ")
    ```

9. Veldu **Vista**.
10. Veldu **Í lagi**.
11. Í aðgerðarúðunni skal velja **Keyra**.
12. Í svarglugganum **Færibreytur rafrænnar skýrslugerðar** á flipanum **Færslur til að taka með** skal velja **Sía**.
13. Á flipanum **Svið**, skal finna línuna þar sem reiturinn **Tafla** er stillt á **Staðsetningar** og reiturinn **Reitur** er stilltur á **Staðsetning**. Í reitinn **Skilyrði** skal færa inn **Bay**.
14. Veldu **Í lagi**.
15. Veldu **Í lagi**. Merkimiði er búinn til og sýndur á forskoðunarsíðunni í prentarahermiforritinu.

![Farið yfir myndað merki sem inniheldur auðkenni staðsetningarforstillingar á forskoðunarsíðu hermiforrits Zpl-prentara.](./media/er-design-zpl-labels-preview-label2.png)

## <a name="encoding"></a>Kóðun

> [!NOTE]
> Samstilla verður kóðunarstillingu fyrir þáttinn **Almennt\\Skrá** fyrir breytanlegt snið rafrænnar skýrslugerðar og viðeigandi stillingu hannaðs merkis. Gildið í reitnum **[Kóðun](er-suppress-bom-characters.md)** fyrir þáttinn **Almennt\\Skrá** á ekki að vera í mótsögn við ZPL-skipun sem notuð er til að stýra kóðun merkisins (til dæmis `^CI` skipunin). Rafræn skýrslugerð staðfestir ekki að þessar stillingar séu samstilltar.

## <a name="additional-resources"></a>Frekari upplýsingar

[Viðtökustaður prentara](er-destination-type-print.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
