---
title: Stjórnun líftíma skilgreiningar fyrir rafræna skýrslugerð
description: Þessi grein lýsir hvernig eigi að stjórna lífsferli skilgreininga Rafrænnar skýrslugerðar (ER) fyrir Dynamics 365 Finance.
author: kfend
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 0209679c9882d87edab68d043fba9e7b3400a2a2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337264"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Stjórnun líftíma skilgreiningar fyrir rafræna skýrslugerð

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig eigi að stjórna lífsferli [Rafræn skýrslugerð](general-electronic-reporting.md) (ER) [stillingum](general-electronic-reporting.md#Configuration) fyrir Dynamics 365 Finance.

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
Mælt er með að hanna ER skilgreiningar í þróunarumhverfi sem aðskilið tilvik af fjármála- og reksturs fyrir eftirfarandi ER málefni:

- Notendur í hlutverkum annaðhvort **Þróunaraðila rafrænnar skýrslugerðar** eða **Hagnýts ráðgjafa vegna rafrænnar skýrslugerðar** geta breytt stillingum og keyrt þær vegna prófunar. Það getur valdið köllun eftir aðferðum flokka og töflum sem geta hugsanlega verið skaðleg fyrir viðskiptagögn og árangur af notkun tilviks.
- Köllun eftir aðferðum flokka og tafla sem ER gagnagjafa fyrir ER skilgreiningar eru ekki takmarkaðar af aðgangsstað og skráðu efni fyrirtækis. Því geta notendur sem eru í hlutverkum **Þróunaraðila rafrænnar skýrslugerðar** eða **Hagnýts ráðgjafa vegna rafrænnar skýrslugerðar** fengið aðgang að viðkvæmum gögnum fyrirtækis.

Skilgreiningar rafrænar skýrslugerðar sem eru hannaðar í þróunarumhverfi má [hlaða upp](#data-persistence-consideration) í prófunarumhverfi fyrir skilgreiningarmat (rétt samþætting vinnslu, nákvæmni niðurstaða og afköst) og gæðatryggingu, til dæmis réttmæti aðgangsheimilda sem eru knúin af hlutverkum, aðskilnaður á skyldum o.s.frv.. Hægt er að nota eiginleika til að skiptast á skilgreiningum rafrænnar skýrslugerðar í þessum tilgangi. Sannreyndar skilgreiningar rafrænnar skýrslugerðar er hægt að hlaða upp í LCS til að deila þeim með áskrifendum þjónustu eða [flytja inn](#data-persistence-consideration) í vinnsluumhverfi til innri nota.

![Lífsferill skilgreiningar rafrænnar skýrslugerðar.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>Taka til greina varanleika gagna

Hægt er að [flytja inn](tasks/er-import-configuration-lifecycle-services.md) hverja mismunandi útgáfu fyrir sig af [skilgreiningu](general-electronic-reporting.md#Configuration) rafrænnar skýrslugerðar í tilvikið þitt af Finance. Þegar ný útgáfa af skilgreiningu rafrænnar skýrslugerðar er flutt inn stjórnar kerfið innihaldi útgáfudraga fyrir þessa skilgreiningu:

- Þegar innflutt útgáfa er lægri en hæsta útgáfa þessarar skilgreiningar í núverandi tilviki af Finance mun innihald útgáfudraga þessarar skilgreiningar haldast óbreytt.
- Þegar innflutt útgáfa er hærri en önnur útgáfa þessarar skilgreiningar í núverandi tilviki af Finance verður innihald innfluttu útgáfunnar afritað í útgáfudrög þessarar skilgreiningar til að gera þér kleift að halda áfram að breyta síðustu loknu útgáfu.

Ef þessi skilgreining er í eigu [skilgreiningarveitunnar](general-electronic-reporting.md#Provider) sem er virkjuð sem stendur, verða útgáfudrög þessarar skilgreiningar sýnileg þér í flýtiflipanum **Útgáfur** á síðunni **Skilgreiningar** (**Fyrirtækisstjórnun** > **Rafræn skýrslugerð** > **Skilgreiningar**). Hægt er að velja útgáfudrög skilgreiningarinnar og [breyta](er-quick-start2-customize-report.md#ConfigureDerivedFormat) innihaldi hennar með því að nota viðeigandi hönnuð rafrænnar skýrslugerðar. Þegar þú hefur breytt útgáfudrögum fyrir skilgreiningu rafrænnar skýrslugerðar mun innihald þeirra ekki lengur passa við innihald hæstu útgáfu þessarar skilgreiningar í núverandi tilviki af Finance. Til að koma í veg fyrir að breytingarnar tapist birtir kerfið villu um að innflutningurinn geti ekki haldið áfram vegna þess að útgáfa þessarar skilgreiningar er hærri en hæsta útgáfa þessarar skilgreiningar í núverandi tilviki af Finance. Þegar þetta gerist, til dæmis með sniðsskilgreiningunni **X**, birtist villan **Snið af útgáfu „X“ er ekki lokið**.

Til að afturkalla breytingarnar sem þú kynntir í útgáfudrögum skal velja hæstu loknu eða deildu útgáfu af skilgreiningu rafrænnar skýrslugerðar í Finance í flýtiflipanum **Útgáfur** og síðan velja valkostinn **Sækja þessa útgáfu**. Innihald valinnar útgáfu er afritað í útgáfudrögin.

## <a name="applicability-consideration"></a>Önnur atriði varðandi gildissvið

Þegar ný útgáfa af rafrænni skýrslugerð er hönnuð er hægt að skilgreina hversu [háð](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) hún er öðrum hugbúnaðarhlutum. Þetta skref er hugsað sem skilyrði fyrir stjórnun niðurhals á þessari útgáfu grunnstillinga frá Rafræn skýrslugerð geymsla eða ytri XML-skrá og allri frekari notkun á þessari útgáfu. Þegar þú reynir að flytja inn nýja útgáfu af ER-stillingu notar kerfið stilltar skilyrði til að stjórna því hvort hægt sé að flytja inn útgáfuna.

Í sumum tilfellum gætir þú þurft að velja að kerfið hunsi stillt skilyrði þegar þú flytur inn nýjar útgáfur af skilgreiningum rafrænnar skýrslugerðar. Til að láta kerfið hunsa skilyrði meðan á innflutningi stendur skal fylgja þessum skrefum.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
3. Stillið **Sleppa forsendukönnun á uppfærslum og útgáfu vöru við innflutning** valkostinn á **Já**.

    > [!NOTE]
    > Þessi breyta er notendasértæk og fyrirtækjasértæk.

## <a name="dependencies-on-other-components"></a>Tengsl við aðra íhluti

Hægt er að stilla skilgreiningar rafrænnar skýrslugerðar sem [háðar](er-download-configurations-global-repo.md#import-filtered-configurations) öðrum skilgreiningum. Til dæmis er hægt að [flytja inn](er-download-configurations-global-repo.md) skilgreiningu [gagnalíkans](er-overview-components.md#data-model-component) fyrir rafræna skýrslugerð úr altæku geymslunni í [Microsoft Regulatory Configuration Services (RCS)](../../../finance/localizations/rcs-overview.md) eða tilvik af Dynamics 365 Finance og síðan búa til nýja skilgreining fyrir [snið](er-overview-components.md#format-component) rafrænnar skýrslugerðar sem er [afleidd](er-quick-start2-customize-report.md#DeriveProvidedFormat) úr innfluttri skilgreiningu á gagnalíkani rafrænnar skýrslugerðar. Afleidd skilgreining rafræns skýrslugerðarsniðs mun vera háð skilgreiningu á grunngagnalíkani rafrænnar skýrslugerðar.

![Afleidd skilgreining sniðs rafrænnar skýrslugerðar á skilgreiningasíðunni.](./media/ger-configuration-lifecycle-img1.png)

Þegar þú hefur lokið við að hanna sniðið geturðu breytt stöðu á upphaflegri útgáfu af skilgreiningu rafræns skýrslugerðarsniðs úr **Drögum** í **Lokið**. Síðan er hægt að deila lokinni útgáfu af skilgreiningu rafræns skýrslugerðarsniðs með því að [gefa hana út](../../../finance/localizations/rcs-global-repo-upload.md) til altæku geymslunnar. Næst er hægt að opna altæku geymsluna úr hvaða tilviki af RCS eða Finance í skýinu. Síðan er hægt að flytja inn allar útgáfur af skilgreiningu rafrænnar skýrslugerðar sem á við um forritið úr altæku geymslunni og í það forrit.

![Birt skilgreining sniðs rafrænnar skýrslugerðar á síðunni Skilgreiningageymsla.](./media/ger-configuration-lifecycle-img2.png)

Byggt á tengslum skilgreiningarinnar, þegar þú velur skilgreiningu rafræns skýrslugerðarsniðs í altæku geymslunni til að flytja hana inn í nýlega uppsett tilvik af RCS eða Finance, verður skilgreining á grunngagnalíkani rafrænnar skýrslugerðar sjálfkrafa fundin í altæku geymslunni og flutt inn með valdri skilgreiningu rafræns skýrslugerðarsniðs sem grunnskilgreining.

Einnig er hægt að flytja útgáfu af skilgreiningu rafræns skýrslugerðarsniðs út úr núverandi tilviki af RCS eða Finance og geyma hana staðbundið sem XML-skrá.

![Að flytja út útgáfu af skilgreiningu rafræns skýrslugerðarsniðs sem XML á skilgreiningarsíðunni.](./media/ger-configuration-lifecycle-img3.png)

Í Finance-útgáfum **á undan útgáfu 10.0.29**, þegar þú reynir að flytja útgáfu af skilgreiningu rafræns skýrslugerðarsniðs úr þeirri XML-skrá eða úr einhverri geymslu annarri en altæku geymslunni og inn í nýlega uppsett tilvik af RCS eða Finance sem inniheldur ekki neinar skilgreiningar rafrænnar skýrslugerðar verður eftirfarandi undantekning birt til að láta vita að ekki sé hægt að sækja grunnskilgreininguna:

> Óleystar tilvísanir sem eftir eru<br>
Ekki er hægt að stofna tilvísun hlutarins „\<imported configuration name\>“ í „Grunnur“ (\<globally unique identifier of the missed base configuration\>,\<version of the missed base configuration\>)

![Innflutningur útgáfu skilgreiningar sniðs rafrænnar skýrslugerðar á síðu skilgreiningageymslu.](./media/ger-configuration-lifecycle-img4.gif)

Í útgáfu **10.0.29 og síðar**, þegar þú reynir að sama innflutning á skilgreiningu, ef grunnskilgreining finnst ekki í núverandi forritstilviki eða í upprunageymslu sem verið er að nota (ef það á við), mun rammi rafrænnar skýrslugerðar sjálfkrafa reyna að finna heitið á grunnskilgreiningu sem vantar í skyndiminni altæku geymslunnar. Hann mun síðan sýna heitið og altækt einkvæmt kennimerki (GUID) á grunnskilgreiningunni sem vantar í texta undantekningarinnar sem var birt.

> Óleystar tilvísanir sem eftir eru<br>
Ekki er hægt að stofna tilvísun hlutarins „\<imported configuration name\>“ í „Grunnur“ (\<name of the missed base configuration\> \<globally unique identifier of the missed base configuration\>,\<version of the missed base configuration\>)

![Undantekning á síðu skilgreiningageymslu þegar grunnskilgreining finnst ekki.](./media/ger-configuration-lifecycle-img5.png)

Hægt er að nota uppgefið heiti til að finna grunnskilgreininguna og flytja hana síðan inn handvirkt.

> [!NOTE]
> Þessi nýi valkostur virkar aðeins þegar að minnsta kosti einn notandi hefur þegar skráð sig inn í altæku geymsluna með því að nota síðuna [Skilgreiningageymslur](er-download-configurations-global-repo.md#open-configurations-repository) eða einn af [uppflettireitum](er-extended-format-lookup.md) altæku geymslunnar í núverandi tilviki af Finance og þegar efni altæku geymslunnar hefur verið vista í skyndiminni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Skilgreina hversu mikil áhrif skilgreiningar rafrænnar skýrslugerðar hafa á aðra hluta](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

