---
title: Stjórnun á lífsferli grunnstillingar fyrir rafræna skýrslugerð
description: Þetta efnisatriði lýsir hvernig á að stjórna lífsferli skilgreininga rafrænnar skýrslugerðar (ER) fyrir Dynamics 365 Finance.
author: NickSelin
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52aba53b5323a9c6c4331cd8de7e932bb9c3547e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893202"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Stjórnun líftíma skilgreiningar fyrir rafræna skýrslugerð

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að stjórna lífsferli skilgreininga rafrænnar skýrslugerðar (ER) fyrir Dynamics 365 Finance.

## <a name="overview"></a>Yfirlit

Rafræn skýrslugerð (ER) er kerfi til að styðja lögboðin og landsértæk rafræn skjöl. Almennt hefur ER möguleikann á að framkvæma eftirfarandi verkefni fyrir stakt rafrænt skjal. Frekari upplýsingar eru í [Yfirlit yfir rafræna skýrslugerð (ER)](general-electronic-reporting.md).

- Að hanna sniðmát fyrir rafrænt skjal:

    - Auðkenna áskilinn uppruna gagna sem má setja fram í þessu fylgiskjali:

        - Undirliggjandi gögn, t.d. gagnatöflur, gagnaeiningar og flokkar.
        - Ferlistengdir eiginleikar, t.d. dagsetning og tími keyrslu og tímabelti.
        - Innsláttarfæribreytur notanda, tilgreindar af notanda á keyrslutíma.

    - Skilgreina þarf nauðsynlegar einingar skjals sem og grannfræði þess til að tilgreina snið endanlegs skjals.
    - Skilgreina þarf æskilegt flæði gagna frá völdum gagnagjafa til skilgreindra eininga skjals (í gegnum tengingar gagnagjafa við sniðsþætti skjals) og tilgreina rök vinnslustjórnunar.

- Gera sniðmát tiltækt þannig að hægt er að nota það í öðrum tilvikum:

    - Umbreyta sniðmáti skjals sem var stofnað yfir í ER skilgreiningu og flytja afbrigði úr núverandi forritstilviki sem xml-pakka sem hægt er að geyma annaðhvort staðbundið eða í Lifecycle Services (LCS).
    - Umbreyta skilgreiningu ER í skjalasniðmát forrits.
    - Flytja inn xml-pakka sem geymdur er annað hvort staðbundið eða í LCS yfir í gildandi tilvik.

- Sérsníða sniðmát rafræna skjalsins:

    - Flytja sniðmát úr LCS yfir í núverandi tilvik sem ER-skilgreiningu.
    - Hanna sérsniðna útgáfu ER skilgreiningar og halda tilvísun í grunnútgáfu hennar.

- Samþætta sniðmát við tiltekið viðskiptaferli, þannig að það sé tiltækt í forritinu:

    - Skilgreina stillingar þannig að forritið byrjar að nota ER-skilgreiningu með því að vísa í þá skilgreiningu í færibreytu sem er í tengslum við vinnslu. Til dæmis vísa í skilgreiningu rafrænnar skýrslugerðar í tilteknum greiðslumáta fyrir viðskiptaskuldir til að mynda rafræn greiðsluskilaboð fyrir úrvinnslu reikninga.

- Nota sniðmát í tilteknu viðskiptaferli:

    - Keyra skilgreiningu rafrænnar skýrslugerðar í tilteknu viðskiptaferli. Til dæmis til að mynda skilaboð rafrænnar greiðslu fyrir úrvinnslu reikninga þegar greiðslumáti sem vísar til skilgreiningar rafrænnar skýrslugerðar er valinn.

## <a name="concepts"></a>Hugtök
Eftirfarandi hlutverk og tengdar aðgerðir tengjast lífsferli skilgreiningar rafrænnar skýrslugerðar.

| Hlutverk                                       | Verkþættir                                                      | lýsing |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar | Stofna og stjórna íhlutum ER (líkön og snið).           | Viðskiptaaðili sem hannar sértæk gagnalíkön rafrænnar skýrslugerðar fyrir tiltekin svið hannar áskilin sniðmát fyrir rafræn skjöl og tengir þau saman á viðeigandi hátt. |
| Þróunaraðili rafrænnar skýrslulausnar             | Stofnar og stjórnar vörpunum gagnalíkana.                          | Sérfræðingur sem velur viðeigandi Finance gagnagjafa og tengir þá við lénasértæk ER gagnalíkön. |
| Yfirmaður bókhalds                      | Skilgreinir stillingar á ferlum sem vísa til ER gervinga. | Til dæmis hlutverkið **Yfirmaður bókhalds** sem leyfir að nota stillingar skilgreiningar rafrænnar skýrslugerðar fyrir tiltekinn greiðslumáta viðskiptaskulda til að geta búið til rafræn greiðsluskilaboð fyrir úrvinnslu reikninga. |
| Starfsmaður viðskiptaskuldagreiðslna            | Notar ER gervinga í tilteknu viðskiptaferli.                | Til dæmis hlutverk **Starfsmanns viðskiptaskuldagreiðslna** sem leyfir að mynda rafræn greiðsluskilaboð fyrir úrvinnslu reikninga, byggt á sniði rafrænnar skýrslugerðar sem er skilgreint fyrir tiltekinn greiðslumáta. |

## <a name="er-configuration-development-lifecycle"></a>Þróunarlífsferill ER skilgreiningar.
Af eftirfarandi ER-tengdum ástæðum er mælt með að hanna ER skilgreiningar í þróunarumhverfi sem aðskilið tilvik af Finance and Operations:

- Notendur í hlutverkum annaðhvort **Þróunaraðila rafrænnar skýrslugerðar** eða **Hagnýts ráðgjafa vegna rafrænnar skýrslugerðar** geta breytt stillingum og keyrt þær vegna prófunar. Það getur valdið köllun eftir aðferðum flokka og töflum sem geta hugsanlega verið skaðleg fyrir viðskiptagögn og árangur af notkun tilviks.
- Köllun eftir aðferðum flokka og tafla sem ER gagnagjafa fyrir ER skilgreiningar eru ekki takmarkaðar af aðgangsstað og skráðu efni fyrirtækis. Því geta notendur sem eru í hlutverkum **Þróunaraðila rafrænnar skýrslugerðar** eða **Hagnýts ráðgjafa vegna rafrænnar skýrslugerðar** fengið aðgang að viðkvæmum gögnum fyrirtækis.

Skilgreiningar rafrænar skýrslugerðar sem eru hannaðar í þróunarumhverfi má [hlaða upp](#data-persistence-consideration) í prófunarumhverfi fyrir skilgreiningarmat (rétt samþætting vinnslu, nákvæmni niðurstaða og afköst) og gæðatryggingu, til dæmis réttmæti aðgangsheimilda sem eru knúin af hlutverkum, aðskilnaður á skyldum o.s.frv.. Hægt er að nota eiginleika til að skiptast á skilgreiningum rafrænnar skýrslugerðar í þessum tilgangi. Sannreyndar skilgreiningar rafrænnar skýrslugerðar er hægt að hlaða upp í LCS til að deila þeim með áskrifendum þjónustu eða [flytja inn](#data-persistence-consideration) í vinnsluumhverfi til innri nota.

![Lífsferill skilgreiningar rafrænnar skýrslugerðar](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a><a name="data-persistence-consideration" />Taka til greina varanleika gagna

Hægt er að [flytja inn](tasks/er-import-configuration-lifecycle-services.md) hverja mismunandi [útgáfu](general-electronic-reporting.md#component-versioning) fyrir sig af [skilgreiningu](general-electronic-reporting.md#Configuration) rafrænnar skýrslugerðar í tilvikið þitt af Finance. Þegar ný útgáfa af skilgreiningu rafrænnar skýrslugerðar er flutt inn stjórnar kerfið innihaldi útgáfudraga fyrir þessa skilgreiningu:

   - Þegar innflutt útgáfa er lægri en hæsta útgáfa þessarar skilgreiningar í núverandi tilviki af Finance mun innihald útgáfudraga þessarar skilgreiningar haldast óbreytt.
   - Þegar innflutt útgáfa er hærri en önnur útgáfa þessarar skilgreiningar í núverandi tilviki af Finance verður innihald innfluttu útgáfunnar afritað í útgáfudrög þessarar skilgreiningar til að gera þér kleift að halda áfram að breyta síðustu loknu útgáfu.

Ef þessi skilgreining er í eigu [skilgreiningarveitunnar](general-electronic-reporting.md#Provider) sem er virkjuð sem stendur, verða útgáfudrög þessarar skilgreiningar sýnileg þér í flýtiflipanum **Útgáfur** á síðunni **Skilgreiningar** (**Fyrirtækisstjórnun** > **Rafræn skýrslugerð** > **Skilgreiningar**). Hægt er að velja útgáfudrög skilgreiningarinnar og [breyta](er-quick-start2-customize-report.md#ConfigureDerivedFormat) innihaldi hennar með því að nota viðeigandi hönnuð rafrænnar skýrslugerðar. Þegar þú hefur breytt útgáfudrögum fyrir skilgreiningu rafrænnar skýrslugerðar mun innihald þeirra ekki lengur passa við innihald hæstu útgáfu þessarar skilgreiningar í núverandi tilviki af Finance. Til að koma í veg fyrir að breytingarnar tapist birtir kerfið villu um að innflutningurinn geti ekki haldið áfram vegna þess að útgáfa þessarar skilgreiningar er hærri en hæsta útgáfa þessarar skilgreiningar í núverandi tilviki af Finance. Þegar þetta gerist, til dæmis með sniðsskilgreiningunni **X**, birtist villan **Snið af útgáfu „X“ er ekki lokið**.

Til að afturkalla breytingarnar sem þú kynntir í útgáfudrögum skal velja hæstu loknu eða deildu útgáfu af skilgreiningu rafrænnar skýrslugerðar í Finance í flýtiflipanum **Útgáfur** og síðan velja valkostinn **Sækja þessa útgáfu**. Innihald valinnar útgáfu er afritað í útgáfudrögin.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
