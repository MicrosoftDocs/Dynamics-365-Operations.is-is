---
title: Stjórnun líftíma skilgreiningar fyrir rafræna skýrslugerð
description: Þessi grein lýsir því hvernig á að stjórna líftíma rafrænna skýrslugerðar (ER) stillinga fyrir Dynamics 365 Finance.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337264"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Stjórnun líftíma skilgreiningar fyrir rafræna skýrslugerð

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að stjórna líftíma [Rafræn skýrslugerð](general-electronic-reporting.md) (ER) [stillingar](general-electronic-reporting.md#Configuration) fyrir Dynamics 365 Finance.

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
Af eftirfarandi ER-tengdum ástæðum mælum við með því að þú sért að hanna ER stillingar í þróunarumhverfinu, sem sérstakt dæmi um fjármál og rekstur:

- Notendur í hlutverkum annaðhvort **Þróunaraðila rafrænnar skýrslugerðar** eða **Hagnýts ráðgjafa vegna rafrænnar skýrslugerðar** geta breytt stillingum og keyrt þær vegna prófunar. Það getur valdið köllun eftir aðferðum flokka og töflum sem geta hugsanlega verið skaðleg fyrir viðskiptagögn og árangur af notkun tilviks.
- Köllun eftir aðferðum flokka og tafla sem ER gagnagjafa fyrir ER skilgreiningar eru ekki takmarkaðar af aðgangsstað og skráðu efni fyrirtækis. Því geta notendur sem eru í hlutverkum **Þróunaraðila rafrænnar skýrslugerðar** eða **Hagnýts ráðgjafa vegna rafrænnar skýrslugerðar** fengið aðgang að viðkvæmum gögnum fyrirtækis.

Skilgreiningar rafrænar skýrslugerðar sem eru hannaðar í þróunarumhverfi má [hlaða upp](#data-persistence-consideration) í prófunarumhverfi fyrir skilgreiningarmat (rétt samþætting vinnslu, nákvæmni niðurstaða og afköst) og gæðatryggingu, til dæmis réttmæti aðgangsheimilda sem eru knúin af hlutverkum, aðskilnaður á skyldum o.s.frv.. Hægt er að nota eiginleika til að skiptast á skilgreiningum rafrænnar skýrslugerðar í þessum tilgangi. Sannreyndar skilgreiningar rafrænnar skýrslugerðar er hægt að hlaða upp í LCS til að deila þeim með áskrifendum þjónustu eða [flytja inn](#data-persistence-consideration) í vinnsluumhverfi til innri nota.

![Lífsferill skilgreiningar rafrænnar skýrslugerðar.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>Taka til greina varanleika gagna

Þú getur hver fyrir sig [flytja inn](tasks/er-import-configuration-lifecycle-services.md) mismunandi útgáfur af bráðamóttöku [uppsetningu](general-electronic-reporting.md#Configuration) til þíns fjármálatilviks. Þegar ný útgáfa af skilgreiningu rafrænnar skýrslugerðar er flutt inn stjórnar kerfið innihaldi útgáfudraga fyrir þessa skilgreiningu:

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

## <a name="dependencies-on-other-components"></a>Ósjálfstæði á öðrum hlutum

Hægt er að stilla ER stillingar sem [háð](er-download-configurations-global-repo.md#import-filtered-configurations) á öðrum stillingum. Til dæmis getur þú [flytja inn](er-download-configurations-global-repo.md) bráðamóttöku [gagnalíkan](er-overview-components.md#data-model-component) stillingar frá alþjóðlegu geymslunni í þinn [Microsoft Regulatory Configuration Services (RCS)](../../../finance/localizations/rcs-overview.md) eða Dynamics 365 Finance tilvik, og stofnaðu síðan nýtt ER [sniði](er-overview-components.md#format-component) uppsetningu sem er [afleidd](er-quick-start2-customize-report.md#DeriveProvidedFormat) úr innfluttu ER gagnalíkanstillingunni. Afleidda ER-sniðsstillingin verður háð grunnstillingu ER-gagnalíkans.

![Afleidd ER-sniðsstilling á síðunni Stillingar.](./media/ger-configuration-lifecycle-img1.png)

Þegar þú hefur lokið við að hanna sniðið geturðu breytt stöðu upphafsútgáfu þinnar af uppsetningu ER sniðs frá **Drög** til **Lokið**. Þú getur síðan deilt fullgerðri útgáfu af ER sniðstillingunni með því að [útgáfu](../../../finance/localizations/rcs-global-repo-upload.md) það í alþjóðlegu geymsluna. Næst geturðu fengið aðgang að alþjóðlegu geymslunni frá hvaða RCS eða Finance skýjatilviki sem er. Þú getur síðan flutt inn hvaða ER stillingarútgáfu sem á við um forritið úr alþjóðlegu geymslunni í það forrit.

![Birt ER snið stillingar á síðu Stillingar geymslu.](./media/ger-configuration-lifecycle-img2.png)

Byggt á uppsetningarháðinni, þegar þú velur ER sniðsstillingu í alþjóðlegu geymslunni til að flytja hana inn í nýuppsett RCS eða Finance tilvik, er grunnstilling ER gagnalíkans sjálfkrafa að finna í alþjóðlegu geymslunni og er flutt inn ásamt völdu ER sniði stillingar sem grunnstillingar.

Þú getur líka flutt út ER snið stillingarútgáfuna þína úr núverandi RCS eða Finance tilvikinu þínu og geymt það á staðnum sem XML skrá.

![Flytja út ER snið stillingarútgáfu sem XML á Stillingar síðunni.](./media/ger-configuration-lifecycle-img3.png)

Í útgáfum af Finance **fyrir útgáfu 10.0.29**, þegar þú reynir að flytja inn ER-sniðsstillingarútgáfuna úr þeirri XML-skrá eða úr einhverri annarri geymslu en alþjóðlegu geymslunni í nýuppsett RCS- eða Finance-tilvik sem enn inniheldur engar ER-stillingar, verður eftirfarandi undantekning hent til að upplýsa þú að ekki sé hægt að fá grunnstillingu:

> Óleystar tilvísanir sem eftir eru<br>
Tilvísun hlutarins '\<imported configuration name\> ' við hlutinn 'Base' (\<globally unique identifier of the missed base configuration\>,\<version of the missed base configuration\>) er ekki hægt að staðfesta

![Flytja inn ER snið stillingarútgáfu á síðu Stillingar geymsla.](./media/ger-configuration-lifecycle-img4.gif)

Í útgáfu **10.0.29 og síðar**, þegar þú reynir að flytja inn sama stillingar, ef grunnstilling er ekki að finna í núverandi forritstilviki eða í frumgagnageymslunni sem þú ert að nota núna (ef við á), mun ER ramma sjálfkrafa reyna að finna nafn grunnstillingar sem vantar í skyndiminni Global repository. Það mun þá kynna nafn og alþjóðlegt einstakt auðkenni (GUID) grunnstillingar sem vantar í texta undantekningar sem er kastað.

> Óleystar tilvísanir sem eftir eru<br>
Tilvísun hlutarins '\<imported configuration name\> ' við hlutinn 'Base' (\<name of the missed base configuration\>\<globally unique identifier of the missed base configuration\>,\<version of the missed base configuration\>) er ekki hægt að staðfesta

![Undantekning á síðunni Configuration repository þegar grunnstillingin er ekki að finna.](./media/ger-configuration-lifecycle-img5.png)

Þú getur notað uppgefið nafn til að finna grunnstillinguna og síðan flutt hana inn handvirkt.

> [!NOTE]
> Þessi nýi valkostur virkar aðeins þegar að minnsta kosti einn notandi hefur þegar skráð sig inn á alþjóðlegu geymsluna með því að nota [Stillingargeymslur](er-download-configurations-global-repo.md#open-configurations-repository) síðu eða einni af alþjóðlegu geymslunni [horfðu upp](er-extended-format-lookup.md) reiti í núverandi Finance-tilviki og þegar innihald alþjóðlegu geymslunnar hefur verið í skyndiminni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Skilgreina hversu mikil áhrif skilgreiningar rafrænnar skýrslugerðar hafa á aðra hluta](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

