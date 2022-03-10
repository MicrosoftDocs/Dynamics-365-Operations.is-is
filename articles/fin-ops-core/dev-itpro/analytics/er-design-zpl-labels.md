---
title: Hannaðu nýja ER lausn til að prenta ZPL merki
description: Þetta efni útskýrir hvernig á að hanna nýja rafræna skýrslugerð (ER) lausn til að prenta Zebra Programming Language (ZPL) merki.
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 8e5fb1515d4bdf36c22f617b6bfd2fa3ce3efa36
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/05/2022
ms.locfileid: "8389144"
---
# <a name="design-a-new-er-solution-to-print-zpl-labels"></a>Hannaðu nýja ER lausn til að prenta ZPL merki

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig notandi í hlutverki kerfisstjóra, rafrænnar skýrslugerðaraðila eða rafrænnar skýrslugerðarráðgjafa getur stillt færibreytur [Rafræn skýrslugerð (ER)](general-electronic-reporting.md) ramma, hanna nauðsynlega ER [stillingar](general-electronic-reporting.md#Configuration) af nýrri ER lausn til að fá aðgang að gögnum vöruhúsastjórnunarkerfisins og búa til sérsniðna vöruhúsastaðsetningarmerki á Zebra Programming Language (ZPL) II sniði. Hægt er að ljúka skrefunum í **USRT** fyrirtækinu.

## <a name="business-scenario"></a>Sviðsmynd fyrirtækis

Þú ert fulltrúi fyrirtækis sem innleiddi vöruhúsastjórnun í Microsoft Dynamics 365 Finance. Sérhver vöruhús verður að vera merkt með sjálflímandi miða sem inniheldur strikamerki. Starfsmenn vöruhúsa munu nota handfesta strikamerkjalesara til að skanna strikamerkin.

Allar vöruhúsastöðvar hafa verið merktar innan umfangs aðgerða fyrir ræsingu. Hins vegar verður þú einnig að geta prentað merki vöruhúsastaðsetningar ef óskað er eftir því ef núverandi merki skemmast eða vöruhúsahillur eru endurstilltar. Með því að nota nýlega útgefinn ER-virkni geturðu stillt nýja ER-lausn sem gerir umsjónarmanni vöruhúss kleift að prenta merki beint á hitamerkjaprentara.

## <a name="configure-the-er-framework"></a>Skilgreina ramma rafrænnar skýrslugerðar

Fylgdu skrefunum í [Skilgreina ramma rafrænnar skýrslugerðar](er-quick-start2-customize-report.md#ConfigureFramework) til að setja upp lágmarksfjölda af færibreytum rafrænnar skýrslugerðar. Þú verður að ljúka þessari uppsetningu áður en þú byrjar að nota ER ramma til að hanna nýja ER lausn.

## <a name="design-a-domain-specific-data-model"></a>Hanna gagnalíkan fyrir sérstakt lén

Búðu til nýja ER uppsetningu sem inniheldur a [gagnalíkan](er-overview-components.md#data-model-component) hluti fyrir Vöruhússtjórnunarlénið. Þetta gagnalíkan verður notað sem gagnagjafi síðar, þegar þú hannar ER snið til að búa til vöruhúsastaðsetningarmerki.

### <a name="import-a-data-model-configuration"></a>Flytja inn gagnalíkanstillingu

Fylgdu þessum skrefum til að flytja inn nauðsynlegt gagnalíkan úr XML skrá sem er útveguð af Microsoft. Að öðrum kosti geturðu búið til þitt eigið gagnalíkan eins og lýst er í næsta kafla.

1. Sækja [Vöruhús model.version.1.xml](https://download.microsoft.com/download/9/f/1/9f136e9b-bf5f-403a-b089-a2b2ed1da2ba/Warehouse-model.version.1.xml) skrá og vistaðu hana á tölvunni þinni.
2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.
4. Á **Stillingar** síðu, á aðgerðarrúðunni, veldu **Skipti** \> **Hlaða úr XML skrá**.
5. Veldu **Skoðaðu**, og finndu síðan og veldu **Vöruhús model.version.1.xml** skrá.
6. Veljið **Í lagi** til að flytja inn skilgreininguna.

![Innflutt ER gagnalíkanstilling á síðunni Stillingar.](./media/er-design-zpl-labels-imported-model.png)

### <a name="create-a-data-model-configuration"></a>Búðu til gagnalíkanstillingu

Í stað þess að flytja inn gagnalíkanskrána sem Microsoft útvegaði, geturðu búið til gagnalíkan frá grunni. Fyrir dæmi sem sýnir hvernig á að klára þetta verkefni, sjá [Búðu til nýja gagnalíkanstillingu](er-quick-start1-new-solution.md#DesignDataModel).

### <a name="review-the-data-model"></a>Skoðaðu gagnalíkanið

Þú getur skoðað breytanlega útgáfu af stillta gagnalíkaninu á **Hönnuður gagnalíkana** síðu.

![Uppbygging ER gagnalíkans á síðunni Gagnalíkanahönnuður.](./media/er-design-zpl-labels-model.png)

## <a name="design-a-model-mapping-for-the-configured-data-model"></a>Hanna líkanavörpun fyrir skilgreint gagnalíkan

Sem notandi í hlutverki þróunaraðila rafrænna skýrslna verður þú að búa til nýja ER-stillingu sem inniheldur a [módelkortlagningu](er-overview-components.md#model-mapping-component) hluti fyrir vöruhúsgagnalíkanið. Þessi hluti útfærir stillt gagnalíkan fyrir Dynamics 365 Finance og er sérstakt fyrir það app. Þú verður að stilla það til að tilgreina forritshlutina sem verða notaðir til að fylla út stillta gagnalíkanið með forritsgögnum á keyrslutíma. Til að klára þetta verkefni verður þú að skilja hvernig gagnaskipulag vöruhúsastjórnunarviðskiptaléns er útfært í Finance.

### <a name="import-a-model-mapping-configuration"></a>Flytja inn líkanakortastillingar

Fylgdu þessum skrefum til að flytja inn nauðsynlega líkanavörpun úr XML-skrá sem er útveguð af Microsoft. Að öðrum kosti geturðu búið til þína eigin líkanakortlagningu eins og lýst er í næsta kafla.

1. Sækja [Vöruhúslíkanakortlagning.version.1.1.xml](https://download.microsoft.com/download/1/c/c/1cc94d28-3d90-4ffd-a118-77d6c322904f/Warehouse-model-mapping.version.1.1.xml) skrá og vistaðu hana á tölvunni þinni.
2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.
4. Á **Stillingar** síðu, á aðgerðarrúðunni, veldu **Skipti** \> **Hlaða úr XML skrá**.
5. Veldu **Skoðaðu**, og finndu síðan og veldu **Vöruhúslíkanakortlagning.version.1.1.xml** skrá.
6. Veljið **Í lagi** til að flytja inn skilgreininguna.

![Innflutt ER líkanskortstillingar á síðunni Stillingar.](./media/er-design-zpl-labels-imported-mapping.png)

### <a name="create-a-model-mapping-configuration"></a>Búðu til líkanskortstillingu

Í stað þess að flytja inn líkanakortaskrána sem Microsoft útvegaði, geturðu búið til líkanakortlagningu frá grunni. Fyrir dæmi sem sýnir hvernig á að klára þetta verkefni, sjá [Búðu til nýja gerð kortlagningarstillingar](er-quick-start1-new-solution.md#CreateModelMapping).

### <a name="review-the-model-mapping"></a>Fara yfir líkanavörpun

Þú getur skoðað breytanlega útgáfu af stilltu líkanavörpunni á **Módelkortahönnuður** síðu.

![Uppbygging ER líkanakortlagningar á hönnuðarsíðu líkanakortlagningar.](./media/er-design-zpl-labels-mapping.png)

## <a name="design-a-format"></a>Setja upp snið

Sem notandi í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar þarf að stofna nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur [sniðs](er-overview-components.md#format-component) hluta. Til að stilla þennan íhlut muntu nota ZPL II kóða til að tilgreina útlit vöruhúsastaðsetningarmerkisins.

### <a name="import-a-format-configuration"></a>Flytja inn sniðstillingu

Fylgdu þessum skrefum til að flytja inn áskilið snið úr XML skrá sem er útveguð af Microsoft. Að öðrum kosti geturðu búið til þitt eigið snið eins og lýst er í næsta kafla.

1. Sækja [Staðsetningarmerki vöruhúss.version.1.1.xml](https://download.microsoft.com/download/5/7/5/5758b551-69a5-45bd-a2b2-21c3db73a6fc/Warehouse-location-labels.version.1.1.xml) skrá og vistaðu hana á tölvunni þinni.
2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar skýrslugerðar**.
4. Á **Stillingar** síðu, á aðgerðarrúðunni, veldu **Skipti** \> **Hlaða úr XML skrá**.
5. Veldu **Skoðaðu**, og finndu síðan og veldu **Staðsetningarmerki vöruhúss.version.1.1.xml** skrá.
6. Veljið **Í lagi** til að flytja inn skilgreininguna.

![Innflutt ER-sniðsstilling á síðunni Stillingar.](./media/er-design-zpl-labels-imported-format.png)

### <a name="create-a-format-configuration"></a>Stofna skilgreiningu sniðs

Í stað þess að flytja inn sniðskrána sem Microsoft útvegaði geturðu búið til snið frá grunni. Fyrir dæmi sem sýnir hvernig á að klára þetta verkefni, sjá [Búðu til nýja sniðstillingu](er-quick-start1-new-solution.md#FormatCreate).

### <a name="review-the-format"></a>Yfirfara snið

Þú getur skoðað breytanlega útgáfu af stilltu sniðinu á **Sniðhönnuður** síðu.

![Uppbygging ER sniðsins á síðunni Format designer.](./media/er-design-zpl-labels-format.png)

The`model.Location.Label` gagnagjafi á þessu sniði er stilltur til að búa til merki sem innihalda eftirfarandi upplýsingar:

- Vöruhústitillinn sem texti
- Vöruhússtitillinn sem strikamerki
- Staðsetningarheitið
- Vartölur

Á **Formúluhönnuður** síðu fyrir gagnagjafann, ER formúlan sem er notuð til að búa til merki inniheldur a`CONCATENATE` aðgerð sem sameinar upplýsingarnar í viðkomandi skipulagi.

![Formúla fyrir gagnagjafann á Formúlahönnuðarsíðunni.](./media/er-design-zpl-labels-review-formula.png)

> [!TIP]
> Útlit merkimiða er hannað þannig að staðsetningartitillinn og ávísunarstafirnir eru samræmdir í miðju merkimiðans. Hins vegar styður ZPL II ekki miðjastillingu fyrir strikamerki. Þess vegna er formúlan af`model.Location.Warehouse.Alignment` gagnagjafi er notaður til að samræma strikamerkið í miðju merkimiðans. Þessi formúla reiknar út vinstri hliðrun strikamerkisins, byggt á fjölda stafa í heiti vöruhússins.

## <a name="prepare-your-environment-for-previewing-generated-labels"></a>Undirbúðu umhverfið þitt til að forskoða mynduð merki

Eftirfarandi dæmi notar prentarahermiforrit fyrir ZPL merki til að sýna sýnishorn af mynduðum merkimiðum á skjánum. Fylgdu þessum skrefum til að virkja þennan valkost.

1. Bætið við [Prentari](er-destination-type-print.md) ER áfangastaður fyrir **Staðsetningarmerki vöruhúss** ER sniði, og stilltu það til að senda mynduð merki frá Finance til [Document routing agent (DRA)](install-document-routing-agent.md).
2. Settu upp og stilltu DRA til að beina mynduðum merkimiðum frá Finance til staðbundins prentara sem er aðgengilegur frá núverandi vinnustöð.
3. Bættu við staðbundnum prentara fyrir núverandi vinnustöð og stilltu hann til að senda mynduð merki frá DRA yfir í prentarahermiforrit.
4. Settu upp prentarahermiforrit sem framlengingu á Chrome vefvafranum og stilltu það þannig að það sendi mynduð merki frá staðbundnum prentara yfir í vefþjónustu sem mun birta mynduð merki og skila þeim í prentarahermi til forskoðunar.

<table>
<tbody>
<tr align="center">
<td>
<p>Finance</p>
<p>Skýrsla ER</p>
<p>Viðtökustaður prentara</p>
</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from Finance to the DRA."></td>
<td>Umboðsmaður skjalaleiðar</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from the DRA to a local printer."></td>
<td>Staðbundinn prentari</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from a local printer to a printer emulator."></td>
<td>Hermi prentara</td>
<td><img src="./media/er-design-zpl-labels-flow2.png" alt="Data flow direction: from a printer emulator to a rendering web service and then back to the printer emulator."></td>
<td>Að veita vefþjónustu</td>
</td>
</tr>
</tbody>
</table>

### <a name="install-and-configure-a-printer-emulator-application"></a>Settu upp og stilltu prentarahermiforrit

Bættu prentarahermiforriti fyrir ZPL flutningsvélina við Chrome vefvafrann þinn. Þetta dæmi notar [Zpl prentari](https://chrome.google.com/webstore/detail/zpl-printer/phoidlklenidapnijkabnfdgmadlcmjo) keppinautur sem er byggður á [Labelary ZPL vefþjónusta](http://labelary.com/service.html). Prenthermiforritið mun senda mynduð merki á ZPL sniði frá staðbundnum prentara til vefþjónustunnar og skila síðan merkimiðum sem PDF eða PNG skrám til forskoðunar.

1. Finndu og veldu prentarahermiforritið sem þú vilt nota í Chrome vefversluninni. Veldu síðan **Bæta við Chrome** til að bæta því við Chrome vafrann þinn.

    ![Bætir prentarahermiforritinu við Chrome vefvafra frá Chrome vefverslun.](./media/er-design-zpl-labels-add-app.png)

2. Veldu **Ræstu app** til að keyra prentarahermiforritið úr Chrome vefvafranum.

    ![Keyrir prentarahermiforritið úr Chrome vafranum.](./media/er-design-zpl-labels-run-app.png)

3. Stilltu forritið sem er í gangi:

    1. Slökktu á forritinu.
    2. Í prentarastillingunum skaltu stilla gestgjafann á **127.0.0.1**.
    3. Stilltu portið á **9100**.

        ![Stillir prentarahermiforritið.](./media/er-design-zpl-labels-configure-app.png)

    4. Kveiktu aftur á forritinu. Þú ættir að fá skilaboð sem segja að prentarinn hafi verið ræstur á tilgreindum hýsil og tengi.

        ![Kveikt aftur á prentarahermiforriti.](./media/er-design-zpl-labels-turn-on-app.png)

> [!NOTE]
> Þar sem prentarahermiforritið sem er notað í þessu dæmi byggir á vefþjónustu til að birta merkimiða, vertu viss um að öryggisstillingarnar þínar leyfi þér að hafa samskipti við þjónustuna. Að öðrum kosti mun forritið ekki fá birtu merkimiðana og engin forskoðun á þeim merkimiðum verður tiltæk.

### <a name="add-and-configure-a-local-printer"></a>Bættu við og stilltu staðbundinn prentara

[Bættu við nýjum staðbundnum prentara](https://support.microsoft.com/windows/install-a-printer-in-windows-10-cc0724cf-793e-3542-d1ff-727e4978638b) sem núverandi tæki getur notað til að senda mynduð merki frá DRA til prentarahermiforritsins.

1. Í Windows, veldu **Byrjaðu** \> **Stillingar** \> **Tæki** \> **Prentarar\& skanna**.
2. Veldu **Prentarar\& stillingar skanna**.
3. Fyrir **Bættu við prentara eða skanna**, veldu **Bæta við tæki**.
4. Fyrir **Prentarinn sem ég vil er ekki á listanum**, veldu **Bættu við handvirkt**.
5. Í **Finndu prentara með öðrum valkostum** reit, veldu **Bættu við staðbundnum prentara eða netprentara með handvirkum stillingum**.
6. Í **Veldu prentaratengi** reit, veldu **Búðu til nýja höfn**, og fylgdu síðan þessum skrefum:

    1. Í **Tegund hafnar** reit, veldu **Staðlað TCP/IP tengi**.
    2. Í **Hostnafn eða IP-tala** reit, slá inn **127.0.0.1**.
    3. Í **Heiti hafnar** reit, slá inn **ZPL**.
    4. Bíddu þar til **Greinir TCP/IP tengi** aðgerð er lokið.
    5. Í **Gerð tækis** reit, veldu **Sérsniðin**, og veldu síðan **Stillingar**.
    6. Gakktu úr skugga um að eftirfarandi tengistillingar séu tilgreindar:

        - **Heiti hafnar:** ZPL
        - **Nafn prentara eða IP-tala:** 127.0.0.1
        - **Bókun:** Hrátt
        - **Gáttarnúmer:** 9100

7. Í **Settu upp prentarann** reit, veldu **Almennt / aðeins texti**.
8. Í **Nafn prentara** reit, slá inn **ZebraPrinter**.

![Bætir við staðbundnum prentara fyrir núverandi tæki.](./media/er-design-zpl-labels-configure-printer.png)

### <a name="install-and-configure-the-dra"></a>Settu upp og stilltu DRA

Undirbúðu DRA til að senda mynduð merki frá Finance yfir í stilltan staðbundinn prentara.

1. [Settu upp DRA](install-document-routing-agent.md#install-the-document-routing-agent).
2. [Stilltu DRA](install-document-routing-agent.md#configure-the-document-routing-agent).
3. [Skráðu staðbundna prentara](install-document-routing-agent.md#register-network-printers) í DRA.
4. [Virkjaðu staðbundna prentara](install-document-routing-agent.md#administer-network-printers) í þínu fjármálaumhverfi.

![Undirbýr DRA til að prenta mynduð merki.](./media/er-design-zpl-labels-configure-dra.png)

### <a name="configure-the-er-destination"></a>Skilgreina áfangastað Rafræn skýrslugerðar

Undirbúðu ER áfangastað til að senda mynduð merki frá Fjármálum til DRA.

1. Fara á **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Viðtökustaður rafrænnar skýrslugerðar**.
2. Á **Áfangastaður rafrænnar skýrslugerðar** síðu, á aðgerðarrúðunni, veldu **Nýtt**.
3. Í **Tilvísun** reit, veldu **Staðsetningarmerki vöruhúss**.
4. Í flýtiflipanum **Viðtökustaður skráar** skal velja **Nýr**.
5. Í **Nafn** reit, slá inn **Merki**.
6. Í **Heiti skráarhluta** reit, veldu **Skýrsla**.
7. Veldu **Stillingar**.
8. Í **Stillingar áfangastaðar** valmynd, á **Prentari** flipann, stilltu **Virkt** valmöguleika til **Já**.
9. Í **Nafn prentara** reit, veldu **ZebraPrinter**.
10. Í **Tegund skjalaleiðar** reit, veldu **ZPL**.
11. Veldu **Í lagi**.

![Stilling á áfangastað fyrir ER fyrir snið vöruhúsastaðsetningarmerkja á áfangasíðu rafrænnar skýrslugerðar.](./media/er-design-zpl-labels-configure-destination.png)

## <a name="review-warehouse-locations"></a>Skoðaðu staðsetningu vöruhúsa

1. Fara til **Vöruhússtjórnun** \> **Uppsetning** \> **Vöruhús** \> **Staðsetningar**.
2. Á **Staðsetningar** síðu, síaðu til að skoða aðeins staðsetningar sem hafa gildi í **Athugaðu tölustafi** sviði.

![Farið yfir staðsetningar vöruhúsa á síðunni Staðsetningar.](./media/er-design-zpl-labels-review-locations.png)

## <a name="print-warehouse-location-labels"></a>Prentaðu staðsetningarmerki vöruhúss

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á **Stillingar** síðu, í stillingartrénu, stækkaðu **Vöruhús módel**, og veldu **Staðsetningarmerki vöruhúss**.
3. Í aðgerðarúðunni skal velja **Keyra**.
4. Í **Rafræn skýrslufæribreytur** valmynd, á **Skrár til að hafa með** flipa, veldu **Sía**.
5. Á **Svið** flipa, finndu línuna þar sem **Tafla** reiturinn er stilltur á **Staðsetningar** og **Field** reiturinn er stilltur á **Staðsetning**. Í **Viðmið** reit, slá inn **LPE virkt**.
6. Veldu **Í lagi**.
7. Veldu **Í lagi**. Merki er búinn til og sýndur á forskoðunarsíðunni í prenthermiforritinu.

![Skoðaðu myndaðan merkimiða á forskoðunarsíðu Zpl Printer emulator forritsins.](./media/er-design-zpl-labels-preview-label.png)

## <a name="modify-the-layout-of-a-label"></a>Breyttu útliti merkimiða

Þú getur breytt núverandi útliti vöruhúsastaðsetningarmerkinga. Eftirfarandi dæmi sýnir hvernig á að breyta útlitinu þannig að myndaðir merkimiðar innihaldi auðkenni staðsetningarsniðs.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Stilltu **Notaðu áfangastaði fyrir stöðu drög**[ER notendafæribreyta](electronic-reporting-destinations.md#applicability) til **Já**.
3. Á **Stillingar** síðu, í stillingartrénu, stækkaðu **Vöruhús módel**, og veldu **Staðsetningarmerki vöruhúss**.
4. Veljið **Hönnuður**.
5. Á **Sniðhönnuður** síðu, á **Kortlagning** flipann, veldu`model.Location.Label` gagnagjafa.
6. Í **Eiginleikar gagnagjafa** valmynd, veldu **Breyta** \> **Breyta formúlu**.
7. Á **Formúluhönnuður** síðu, í **Formúla** reit, skoðaðu ER formúluna sem er notuð til að búa til merki.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^XZ")
    ```

8. Uppfærðu formúluna til að bæta auðkenni staðsetningarprófíls við mynduð merki.

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
12. Í **Rafræn skýrslufæribreytur** valmynd, á **Skrár til að hafa með** flipa, veldu **Sía**.
13. Á **Svið** flipa, finndu línuna þar sem **Tafla** reiturinn er stilltur á **Staðsetningar** og **Field** reiturinn er stilltur á **Staðsetning**. Í **Viðmið** reit, slá inn **Bay**.
14. Veldu **Í lagi**.
15. Veldu **Í lagi**. Merki er búinn til og sýndur á forskoðunarsíðunni í prenthermiforritinu.

![Farið yfir myndað merki sem inniheldur auðkenni staðsetningarprófíls á forskoðunarsíðu Zpl Printer hermiforritsins.](./media/er-design-zpl-labels-preview-label2.png)

## <a name="encoding"></a>Dulritun

> [!NOTE]
> Þú verður að samstilla kóðunarstillingu **Sameiginlegt\\ Skrá** hluti af breytanlegu ER sniði og viðeigandi stillingu á hönnuðu merkimiðanum. Verðmæti **[Kóðun](er-suppress-bom-characters.md)** sviði á **Sameiginlegt\\ Skrá** hluti ætti ekki að stangast á við ZPL skipun sem er notuð til að stjórna kóðun merkisins (td`^CI` skipun). ER staðfestir ekki að þessar stillingar séu samstilltar.

## <a name="additional-resources"></a>Frekari upplýsingar

[Viðtökustaður prentara](er-destination-type-print.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
