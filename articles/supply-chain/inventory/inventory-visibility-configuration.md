---
title: Skilgreina Inventory Visibility
description: Þessi grein lýsir því hvernig á að stilla birgðasýnileika.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 915382c14cc9ba89b9d543cfd668a94cecbc0a55
ms.sourcegitcommit: 4f987aad3ff65fe021057ac9d7d6922fb74f980e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/14/2022
ms.locfileid: "9764867"
---
# <a name="configure-inventory-visibility"></a>Skilgreina Inventory Visibility

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að stilla Birgðasýnileika með því að nota Birgðasýnileikaforritið í Power Apps.

## <a name="introduction"></a><a name="introduction"></a>Kynning

Áður en þú byrjar að vinna með Birgðasýnileika verður þú að ljúka eftirfarandi uppsetningu eins og lýst er í þessari grein:

- [Skilgreining gagnagjafa](#data-source-configuration)
- [Skilgreining þáttunar](#partition-configuration)
- [Skilgreining á stigveldi atriðaskráar](#index-configuration)
- [Skilgreining frátekningar (valfrjálst)](#reservation-configuration)
- [Dæmi um sjálfgefna skilgreiningu](#default-configuration-sample)

## <a name="prerequisites"></a>Forkröfur

Áður en hafist er handa skal setja upp innbót birgðasýnileika eins og lýst er í [Setja upp sýnileika birgða](inventory-visibility-setup.md).

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>Skilgreiningasíða forrits birgðasýnileika

Í Power Apps hjápar síðan **Skilgreining** [Birgðasýnileikaforrits](inventory-visibility-power-platform.md) til við að setja upp lagerskilgreiningu og skilgreiningu mjúkrar frátekningar. Eftir að viðbótin hefur verið sett upp inniheldur sjálfgefna stillingin gildið frá Microsoft Dynamics 365 Supply Chain Management (`fno` gagnagjafinn). Hægt er að fara yfir sjálfgefnu stillingarnar. Byggt á viðskiptaþörfum þínum og þörfum birgðabókunar ytra kerfisins geturðu auk þess breytt skilgreiningunni til að staðla leiðina sem hægt er að bóka, skipuleggja og senda fyrirspurn á birgðabreytingar í hinum ýmsu kerfum. Hlutarnir sem eftir eru í þessari grein útskýra hvernig á að nota hvern hluta af **Stillingar** síðu.

Þegar skilgreiningunni er lokið skal ganga úr skugga um að velja **Uppfæra skilgreiningu** í forritinu.

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Virkja eiginleika birgðasýnileika í Power Apps eiginleikastjórnun

Innbót birgðasýnileika bætir ýmsum nýjum eiginleika við Power Apps uppsetninguna þína. Sjálfgefið er slökkt á þessum eiginleikum. Til að nota þá skaltu opna **Stillingar** síðu og síðan á **Eiginleikastjórnun** flipann, kveiktu á eftirfarandi eiginleikum eftir þörfum.

| Heiti eiginleikastjórnunar | Lýsing |
|---|---|
| *OnHandReservation* | Þessi eiginleiki gerir þér kleift að búa til pantanir, neyta bókana og/eða afpanta tiltekið birgðamagn með því að nota Birgðasýnileika. Frekari upplýsingar er að finna í [Frátekningar birgðasýnileika](inventory-visibility-reservations.md). |
| *OnHandMostSpecificBackgroundService* | Þessi eiginleiki veitir birgðayfirlit fyrir vörur, ásamt öllum víddum. Gögn birgðasamantektar verða samstillt reglulega úr birgðasýnileika. Sjálfgefin samstillingartíðni er einu sinni á 15 mínútna fresti og hægt er að stilla hana allt að einu sinni á 5 mínútna fresti. Fyrir frekari upplýsingar, sjá [Birgðayfirlit](inventory-visibility-power-platform.md#inventory-summary). |
| *onHandIndexQueryPreloadBackgroundService* | Þessi eiginleiki gerir það mögulegt að forhlaða birgðasýnileika fyrirspurnum fyrir hendi til að setja saman birgðalista með forvöldum víddum. Sjálfgefin samstillingartíðni er einu sinni á 15 mínútna fresti. Fyrir frekari upplýsingar, sjá [Forhlaða straumlínulagaða fyrirspurn](inventory-visibility-power-platform.md#preload-streamlined-onhand-query). |
| *OnhandChangeSchedule* | Þessi valfrjálsi eiginleiki gerir kleift að breyta áætluninni við höndina og aðgerðum sem hægt er að lofa (ATP). Fyrir frekari upplýsingar, sjá [Birgðasýnileiki fyrirliggjandi breytingaráætlun og hægt að lofa](inventory-visibility-available-to-promise.md). |
| *Úthlutun* | Þessi valfrjálsi eiginleiki gerir birgðasýnileika kleift að hafa birgðavörn (hringgirðingar) og yfirsölustýringu. Fyrir frekari upplýsingar, sjá [Birgðasýnileiki birgðaúthlutun](inventory-visibility-allocation.md). |
| *Virkja vörur vöruhúss í birgðasýnileika* | Þessi valfrjálsi eiginleiki gerir Birgðasýnileika kleift að styðja við hluti sem eru virkjaðir fyrir vöruhússtjórnunarferli (WMS). Fyrir frekari upplýsingar, sjá [Stuðningur við birgðasýnileika fyrir WMS hluti](inventory-visibility-whs-support.md). |

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Finna endastöð þjónustu

Ef þú veist ekki réttan birgðasýnileikaþjónustuendapunkt skaltu opna **Stillingar** síðu inn Power Apps, og veldu síðan **Sýna þjónustuupplýsingar** í efra hægra horninu. Síðan mun sýna rétta endastöð þjónustu. Þú getur líka fundið endapunktinn í Microsoft Dynamics Lífsferilsþjónusta, eins og lýst er í [Finndu endapunktinn í samræmi við Lifecycle Services umhverfið þitt](inventory-visibility-api.md#endpoint-lcs).

> [!NOTE]
> Notkun á röngum endapunkti getur valdið misheppnuðu uppsetningu birgðasýnileika og villum þegar birgðakeðjustjórnun er samstillt við birgðasýnileika. Ef þú ert ekki viss um hver endapunkturinn þinn er skaltu hafa samband við kerfisstjórann þinn. Vefslóðir endapunkta nota eftirfarandi snið:
>
> `https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Skilgreining gagnagjafa

Hver gagnagjafi táknar kerfi sem gögnin þín koma úr. Dæmi um heiti gagnagjafa innihalda`fno` (sem samsvarar Supply Chain Management) og`pos` (sem þýðir "sölustaður"). Supply Chain Management er sjálfgefið sett upp sem sjálfgefinn gagnagjafi (`fno`) í birgðasýnileika.

> [!NOTE]
> The`fno` gagnagjafinn er frátekinn fyrir Supply Chain Management. Ef birgðasýnileikaviðbótin þín er samþætt við Supply Chain Management umhverfi mælum við með því að þú eyðir ekki stillingum sem tengjast`fno` í gagnaveitunni.

Til að bæta við gagnagjafa skal fylgja þessum skrefum.

1. Skráðu þig inn í Power Apps umhverfið og opnaðu **Birgðasýnileika**.
1. Opnaðu síðuna **Skilgreining**.
1. Á **Uppruni gagna** flipa, veldu **Ný gagnaheimild** til að bæta við gagnagjafa (til dæmis`ecommerce` eða annað þýðingarmikið auðkenni gagnagjafa).

> [!NOTE]
> Þegar þú bætir við gagnagjafa skaltu ganga úr skugga um að staðfesta heiti gagnagjafans, efnislegar mælingar og víddarvarpanir áður en þú uppfærir skilgreininguna fyrir þjónustu birgðasýnileika. Þú getur ekki breytt þessum stillingum eftir að þú hefur valið **Uppfæra skilgreiningu**.

Skilgreining gagnagjafa inniheldur eftirfarandi hluta:

- Víddir (vörpun víddar)
- Efnislegar mælingar
- Reiknaðar mælingar

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Víddir (vörpun víddar)

Tilgangur víddarskilgreiningar er að staðla samþættingu margra kerfa fyrir bókun tilvika og fyrirspurna samkvæmt víddarsamsetningum. Birgðasýnileiki býður upp á lista yfir grunnvíddir sem hægt er að varpa úr víddunum í gagnagjafann þinn. Þrjátíu og þrjár víddir eru í boði fyrir kortlagningu.

- Ef þú ert að nota Supply Chain Management sem einn af gagnagjafanum þínum, eru 13 víddir þegar varpaðar á Supply Chain Management staðlaðar víddir sjálfgefið. Hinar 12 stærðirnar (`inventDimension1` í gegnum`inventDimension12`) eru einnig varpaðar á sérsniðnar víddir í Supply Chain Management. Hinar átta víddir (`ExtendedDimension1` í gegnum`ExtendedDimension8`) eru útbreiddar víddir sem hægt er að varpa til ytri gagnagjafa.
- Ef þú notar ekki Supply Chain Management sem einn af gagnagjöfum þínum getur þú varpað víddunum eins og þér sýnist. Eftirfarandi tafla sýnir heildarlista yfir tiltækar víddir.

> [!NOTE]
> Ef þú notar Supply Chain Management og breytir sjálfgefnum víddarvörpum á milli Supply Chain Management og Birgðasýnileika, mun breytta víddin ekki samstilla gögn. Þess vegna, ef víddin þín er ekki á sjálfgefna víddarlistanum og þú ert að nota utanaðkomandi gagnagjafa, mælum við með að þú notir`ExtendedDimension1` í gegnum`ExtendedDimension8` til að gera kortlagningu.

| Tegund víddar | Grunnvídd |
|---|---|
| Afurð | `ColorId` |
| Afurð | `SizeId` |
| Afurð | `StyleId` |
| Afurð | `ConfigId` |
| Rakning | `BatchId` |
| Rakning | `SerialId` |
| Staður | `LocationId` |
| Staður | `SiteId` |
| Birgðastaða | `StatusId` |
| Miðast við vöruhús | `WMSLocationId` |
| Miðast við vöruhús | `WMSPalletId` |
| Miðast við vöruhús | `LicensePlateId` |
| Aðrir | `VersionId` |
| Birgðir (sérstillt) | `InventDimension1` til og með `InventDimension12` |
| Viðbót | `ExtendedDimension1` til og með `ExtendedDimension8` |
| System | `Empty` |

> [!NOTE]
> Víddargerðirnar sem taldar eru upp í töflunni á undan eru aðeins til viðmiðunar. Þú þarft ekki að skilgreina þær í birgðasýnileika.
>
> Birgðavíddir (sérsniðnar) gætu verið fráteknar fyrir birgðakeðjustjórnun. Í því tilviki skaltu nota útvíkkuðu mál í staðinn.

Ytri kerfi geta fengið aðgang að birgðasýnileika í gegnum RESTful API. Fyrir samþættinguna gerir birgðasýnileiki þér kleift að skilgreina *ytri gagnagjafa* og vörpunina úr *ytri víddum* í *grunnvíddir*. Hér er dæmi um víddarkortatöflu.

| Ytri vídd | Grunnvídd |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Með því að stilla víddarvörpun er hægt að senda ytri víddir beint í birgðasýnileika. Birgðasýnileiki umbreytir þá sjálfkrafa ytri víddum í grunnvíddir.

Til að bæta við víddarvörpunum skal fylgja þessum skrefum.

1. Skráðu þig inn í Power Apps umhverfið og opnaðu **Birgðasýnileika**.
1. Opnaðu síðuna **Skilgreining**.
1. Á **Uppruni gagna** flipanum, veldu gagnagjafann þar sem þú vilt gera víddarvörpunina. Síðan, í **Víddarkortlagningar** kafla, veldu **Bæta við** til að bæta við víddarkortum.

    ![Vörpun vídda bætt við](media/inventory-visibility-dimension-mapping.png "Vörpun vídda bætt við")

1. Í reitnum **Heiti víddar** skal tilgreina upprunavíddina.
1. Í reitnum **Til grunnvíddar** skal velja víddina í birgðasýnileika sem á að varpa.
1. Veldu **Vista**.

Til dæmis hefur þú nú þegar búið til gagnagjafa sem er nefndur`ecommerce`, og það inniheldur vörulitavídd. Í þessu tilviki, til að gera kortlagningu, geturðu fyrst bætt við`ProductColor` til **Víddarheiti** sviði í`ecommerce` gagnagjafa og veldu síðan`ColorId` í **Til grunnvídd** sviði.

### <a name="physical-measures"></a><a name="data-source-configuration-physical-measures"></a>Efnislegar mælingar

Þegar gagnagjafi bókar birgðabreytingu í birgðasýnileika bókar hann þá breytingu með því að nota *efnislegar mælingar*. Efnislegar mælingar breyta magninu og endurspegla birgðastöðuna. Þú getur skilgreint þínar eigin líkamlegu ráðstafanir út frá þörfum þínum. Hægt er að byggja fyrirspurnir á efnislegum mælingum.

Birgðasýnileiki veitir lista yfir sjálfgefnar líkamlegar mælingar sem eru kortlagðar á Supply Chain Management (þ`fno` gagnagjafa). Þessar sjálfgefnu efnislegu mælingar eru teknar úr birgðafærslustöðum á síðunni **Lagerlisti** í Supply Chain Management (**Birgðastjórnun \> Fyrirspurnir og skýrslur \> Lagerlisti**). Eftirfarandi tafla sýnir dæmi um efnislegar mælieiningar.

| Heiti efnislegrar mælieiningar | lýsing |
|---|---|
| `NotSpecified` | Ótilgreint |
| `Arrived` | Komið |
| `AvailOrdered` | Pantað magn til ráðstöfunar |
| `AvailPhysical` | Efnislegt magn til ráðstöfunar |
| `Deducted` | Frádregið |
| `OnOrder` | OnOrder |
| `Ordered` | Raðað |
| `PhysicalInvent` | Efnislegar birgðir |
| `Picked` | Tekið til |
| `PostedQty` | Bókað magn |
| `QuotationIssue` | Úthreyfing tilboðs |
| `QuotationReceipt` | Innhreyfing tilboðs |
| `Received` | Móttekið |
| `Registered` | Skráð |
| `ReservOrdered` | Pantað frátekið |
| `ReservPhysical` | Efnislegt magn frátekið |

Ef gagnagjafinn þinn er Supply Chain Management þarftu ekki að endurskapa sjálfgefna líkamlegar mælingar. Fyrir ytri gagnagjafa þarftu hinsvegar að búa til nýjar efnislegar mælingar með því að fylgja þessum skrefum.

1. Skráðu þig inn í Power Apps umhverfið og opnaðu **Birgðasýnileika**.
1. Opnaðu síðuna **Skilgreining**.
1. Á **Uppruni gagna** flipanum, veldu gagnagjafann til að bæta líkamlegum mælingum við (til dæmis`ecommerce` gagnagjafa). Síðan, í **Líkamlegar ráðstafanir** kafla, veldu **Bæta við**, og tilgreindu heiti mælikvarða (til dæmis,`Returned` ef þú vilt skrá skilað magn í þessum gagnagjafa í Birgðasýnileika). Vista breytingarnar.

### <a name="calculated-measures"></a>Reiknaðar mælingar

Þú getur notað birgðasýnileika til að senda fyrirspurn á bæði efnislegar mælingar birgða og *sérstilltar reiknaðar mælingar*. Reiknaðar mælingar bjóða upp á sérstillta reikniformúlu sem samanstendur af samsetningu efnislegra mælieininga. Þessi virkni gerir þér kleift að skilgreina safn efnislegra mælieininga sem verður bætt við og/eða safn efnislegra mælieininga sem verða dregnar frá, til að búa til sérstillta mælingu.

> [!IMPORTANT]
> Reiknaður mælikvarði er samsetning líkamlegra mælikvarða. Formúla hennar getur aðeins innihaldið líkamlegar mælingar án afrita, ekki reiknaðar mælikvarða.

Stillingin gerir þér kleift að skilgreina sett af reiknuðum mælikvarðaformúlum sem innihalda breytingar á samlagningu eða frádrátt til að fá heildaruppsafnað úttaksmagn.

Til að setja upp sérstillta reiknaða mælingu skal fylgja þessum skrefum.

1. Skráðu þig inn í Power Apps umhverfið og opnaðu **Birgðasýnileika**.
1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Reiknuð mæling** skal velja **Ný reiknuð mæling** til að bæta við reiknaðri mælingu.
1. Stilltu eftirfarandi reiti fyrir nýju reiknaða mælinguna:

    - **Nýtt reiknað málsheiti** – Sláðu inn heiti reiknaðs mælingar.
    - **Uppruni gagna** – Veldu gagnauppsprettu til að taka með nýja útreiknaða mælinguna í. Fyrirspurnarkerfið er gagnagjafi.

1. Veldu **Bæta við** til að bæta við breytingum við nýja reiknaða mælinguna.
1. Stilltu eftirfarandi reiti fyrir nýja breytimanninn:

    - **Breytir** - Veldu tegund breytinga (*Viðbót* eða *Frádráttur*).
    - **Uppruni gagna** – Veldu gagnagjafann þar sem mælikvarðinn sem gefur breytigildið á að finnast.
    - **Mæla** – Veldu heiti mælingar (frá völdum gagnagjafa) sem gefur upp gildi fyrir breytileikann.

1. Endurtaktu skref 5 til 6 þar til þú hefur bætt við öllum nauðsynlegum breytingum og lokið formúlunni fyrir útreiknaðan mælikvarða.
1. Veldu **Vista**.

Til dæmis starfar tískufyrirtæki á þremur gagnaveitum:

- `pos`– Samsvarar verslunarrásinni.
- `fno`– Samsvarar aðfangakeðjustjórnun.
- `ecommerce`– Samsvarar vefrásinni þinni.

Án reiknaðra mælikvarða, þegar þú biður um vöru D0002 (skápur) undir stað 1, vöruhús 11 og a`ColorID` víddargildi af`Red`, gætirðu fengið eftirfarandi fyrirspurnarniðurstöðu, sem sýnir birgðamagn undir hverri forstilltri efnislegri mælingu. Hins vegar hefur þú ekki sýnilegt heildarmagn sem er tiltækt fyrir pöntunarmagn á milli gagnagjafanna þinna.

```json
[
    {
        "productId": "D0002",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "ecommerce": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

Þú stillir þá reiknaða mælingu sem heitir `MyCustomAvailableforReservation` eins og sýnt er í eftirfarandi töflu. Þessi reiknaða mæling verður notuð af notkunarkerfinu.

| Notkunarkerfi | Reiknuð mæling | Gagnaveita | Efnisleg mæling | Reiknigerð |
|---|---|---|---|---|
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `received` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `scheduled` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `issued` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `reserved` | `Subtraction` |

Þegar þessi reikniformúla er notuð, mun nýja niðurstaða fyrirspurnar fela í sér sérstilltu mælinguna.

```json
[
    {
        "productId": "D0002",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "ecommerce": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CrossChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Úttakið `MyCustomAvailableforReservation`, samkvæmt reiknistillingunni í sérstilltum mælingum, er 100 + 50 – 10 + 80 – 20 + 90 + 30 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Skilgreining þáttunar

Eins og er samanstendur skiptingin af tveimur grunnvíddum (`SiteId` og`LocationId`) sem gefa til kynna hvernig gögnunum er dreift. Aðgerðir undir sama skipting geta skilað meiri afköstum með lægri kostnaði. Eftirfarandi tafla sýnir sjálfgefna skiptingarstillingu sem Inventory Visibility Add-in veitir.

| Grunnvídd | Stigveldi |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

Lausnin inniheldur þessa skiptingarstillingu sjálfgefið. Þess vegna, *þú þarft ekki að skilgreina það sjálfur*.

> [!IMPORTANT]
> Ekki sérsníða sjálfgefna skiptinguna. Ef þú eyðir því eða breytir því er líklegt að þú valdi óvæntri villu.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Skilgreining á stigveldi atriðaskráar

Oftast verður fyrirspurn um lagerbirgðir ekki eingöngu á hæsta stigi „samtölu“. Í staðinn gætirðu líka viljað sjá niðurstöður sem eru teknar saman út frá birgðavíddum.

Birgðasýnileiki veitir sveigjanleika með því að leyfa þér að setja upp *vísitölur* til að bæta árangur fyrirspurna þinna. Þessar atriðaskrár byggja á vídd eða samsetningu vídda. Atriðaskrá samanstendur af *stilltu númeri*, *vídd* og *stigveldu* eins og er skilgreint í eftirfarandi töflu.

| Nafn | lýsing |
|---|---|
| Stilla númer | Víddir sem tilheyra sama safni (atriðaskrá) verða flokkaðar saman og þeim verður úthlutað sama stillta númerinu. |
| Vídd | Grunnvíddir sem niðurstaða fyrirspurnar er lögð saman á. |
| Stigveldi | Stigveldið gerir þér kleift að auka afköst tiltekinna samsetninga víddar þegar þau eru notuð í færibreytum síu og hópa eftir fyrirspurnum. Til dæmis, ef þú setur upp víddarmengi með stigveldisröð af`(ColorId, SizeId, StyleId)`, þá getur kerfið afgreitt fyrirspurnir sem tengjast fjórvíddarsamsetningum hraðar. Fyrsta samsetningin er tóm, önnur er `(ColorId)`, þriðja er `(ColorId, SizeId)` og fjórða er `(ColorId, SizeId, StyleId)`. Aðrar samsetningar verða ekki hraðar. Síur eru ekki takmarkaðar af röð en verða að vera innan þessara stærða ef þú vilt bæta árangur þeirra. Frekari upplýsingar er að finna í dæminu sem fylgir. |

Til að setja upp atriðaskrá afurðastigveldis skal fylgja þessum skrefum.

1. Skráðu þig inn í Power Apps umhverfið og opnaðu **Birgðasýnileika**.
1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Atriðaskrá afurðastigveldis**, í hlutanum **Vörpun vídda**, skal velja **Bæta við** til að bæta við vörpunum vídda.
1. Listi yfir atriðaskrár er sjálfgefið gefinn upp. Til að breyta núverandi atriðaskrá skal velja **Breyta** eða **Bæta við** í hlutanum fyrir viðeigandi atriðaskrá. Til að búa til nýja atriðaskrá skal velja **Nýtt safn atriðaskráar**. Fyrir hverja línu í hverju safni atriðaskráar, í reitnum **Vídd**, skal velja úr listanum yfir grunnvíddir. Gildi fyrir eftirfarandi reiti eru sjálfkrafa búin til:

    - **Stilla númer** – Víddir sem tilheyra sama flokknum (atriðaskrá) verða flokkaðar saman og þeim verður úthlutað sama stillta númerinu.
    - **Stigveldi** – Stigveldið eykur frammistöðu tiltekinna samsetninga víddar þegar þær eru notaðar í færibreytum síu og hópa eftir fyrirspurnum.

> [!TIP]
> Hér eru nokkur ráð til að hafa í huga þegar þú setur upp vísitölustigveldið þitt:
>
> - Grunnvíddir sem eru skilgreindar í skiptingarstillingunni ættu ekki að vera skilgreindar í vísitölustillingum. Ef grunnvídd er skilgreind aftur í vísitölustillingunni muntu ekki geta spurt eftir þessari vísitölu.
> - Ef þú þarft aðeins að spyrjast fyrir um birgðahald sem er safnað saman af öllum víddarsamsetningum skaltu setja upp eina vísitölu sem inniheldur grunnvíddina `Empty`.

### <a name="example"></a>Dæmi

Þessi hluti býður upp á dæmi sem sýnir hvernig stigveldið virkar.

Eftirfarandi tafla sýnir lista yfir tiltækar birgðir fyrir þetta dæmi.

| Atriði | ColorId | SizeId | StyleId | Magn |
|---|---|---|---|---|
| D0002 | Svart | Lítill | Breitt | 1 |
| D0002 | Svart | Lítill | Venjulegt | 2 |
| D0002 | Svart | Stór | Breitt | 3 |
| D0002 | Svart | Stór | Venjulegt | 4 |
| D0002 | Rautt | Lítill | Breitt | 5 |
| D0002 | Rautt | Lítill | Venjulegt | 6 |
| D0002 | Rautt | Stór | Venjulegt | 7 |

Eftirfarandi tafla sýnir hvernig stigveldi atriðaskráar er sett upp.

| Stilla númer | Vídd | Stigveldi |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Atriðaskráin gerir þér kleift að senda fyrirspurn á lagerbirgðirnar á eftirfarandi hátt:

- `()` – Flokkað eftir öllum

    - D0002, 28

- `(ColorId)` – flokkað eftir `ColorId`

    - D0002, svartur, 10
    - D0002, Rauður, 18

- `(ColorId, SizeId)` – Flokkað eftir samsetningu `ColorId` og `SizeId`

    - D0002, svartur, lítill, 3
    - D0002, svartur, stór, 7
    - D0002, Rauður, Lítill, 11
    - D0002, Rauður, Stór, 7

- `(ColorId, SizeId, StyleId)` – Flokkað eftir samsetningu `ColorId`, `StyleId` og `SizeId`

    - D0002, svartur, lítill, breiður, 1
    - D0002, svartur, lítill, venjulegur, 2
    - D0002, svartur, stór, breiður, 3
    - D0002, svartur, stór, venjulegur, 4
    - D0002, rauður, lítill, breiður, 5
    - D0002, Rauður, Lítill, Venjulegur, 6
    - D0002, Rauður, Stór, Venjulegur, 7

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Skilgreining frátekningar (valfrjálst)

Skilgreining bókunar er nauðsynleg ef þú vilt nota eiginleika mjúkrar frátekningar. Skilgreiningin samanstendur af tveimur grunnþáttum:

- Mjúk frátekningarvörpum
- Mjúkt frátekningarstigveldi

### <a name="soft-reservation-mapping"></a>Mjúk frátekningarvörpum

Þegar þú gerir frátekningu gætir þú viljað vita hvort lagerbirgðir séu tiltækar núna fyrir frátekningu. Staðfestingin er tengd við reiknaða mælingu sem stendur fyrir reikniformúlu sem er samsetning efnislegra mælieininga.

Með því að setja upp vörpun úr efnislegri mælingu í reiknaða mælingu gerir þú þjónustu birgðasýnileika kleift að sjálfkrafa staðfesta stöðu frátekningar samkvæmt efnislegu mælingunni.

Áður en þú setur upp þessa kortlagningu verður að skilgreina efnislegar mælingar, reiknaðar mælikvarða og gagnagjafa þeirra á **Uppruni gagna** og **Reiknaður mælikvarði** flipa á **Stillingar** síðu inn Power Apps (eins og lýst er fyrr í þessari grein).

Til að skilgreina vörpun mjúkrar frátekningar skal fylgja þessum skrefum.

1. Skilgreindu efnislega mælingu sem þjónar hlutverki mælingar mjúkrar frátekningar (til dæmis `SoftReservPhysical`).
1. Í flipanum **Reiknuð mæling** á síðunni **Skilgreining** skal skilgreina reiknuðu mælinguna *má taka frá* (AFR) sem inniheldur reikniformúlu AFR sem ætlunin er að varpa í efnislega mælingu. Til dæmis væri hægt að setja upp `AvailableToReserve` (í boði fyrir frátekningu) þannig að það sé varpað í fyrir skilgreiningu `SoftReservPhysical` efnislegrar mælingu. Á þennan hátt er hægt að sjá hvaða magn sem er með `SoftReservPhysical` birgðastöðuna verður í boði fyrir frátekningu. Eftirfarandi tafla sýnir AFR-reikniformúluna.

    | Reiknigerð | Gagnaveita | Efnisleg mæling |
    |---|---|---|
    | samlagning | `fno` | `AvailPhysical` |
    | samlagning | `pos` | `Inbound` |
    | Frádráttur | `pos` | `Outbound` |
    | Frádráttur | `iv` | `SoftReservPhysical` |

    Við mælum með því að þú setjir upp reiknaða mælingu þannig að hún innihaldi efnislega mælingu sem mæling frátekningar byggir á. Þannig mun magn reiknaðrar mælingar verða fyrir áhrifum af magni frátekningarmælingar. Í þessu dæmi ætti því `AvailableToReserve` reiknuð mæling `iv` gagnagjafans að innihalda `SoftReservPhysical` efnislega mælingu frá `iv` sem þátt.

1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Vörpun mjúkrar frátekningar** skal setja upp vörpunina úr efnislegu mælingunni í reiknaða mælingu. Í fyrra dæminu er hægt að nota eftirfarandi stillingar til að varpa `AvailableToReserve` í fyrri skilgreiningu `SoftReservPhysical` efnislegrar mælingar.

    | Gagnagjafi efnislegrar mælingar | Efnisleg mæling | Í boði fyrir gagnagjafa frátekningar | Í boði fyrir reiknaða mælingu frátekningar |
    |---|---|---|---|
    | `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > Ef þú getur ekki breytt flipanum **Vörpun mjúkrar frátekningar** gætir þú þurft að kveikja á eiginleikanum *OnHandReservation* í flipanum **Eiginleikastjórnun**.

Nú, þegar þú gerir frátekningu á `SoftReservPhysical`, mun birgðasýnileiki sjálfkrafa finna `AvailableToReserve` og tengda reikniformúlu til að staðfesta frátekninguna.

Þú getur til dæmis verið með eftirfarandi lagerbirgðir í birgðasýnileika.

```json
{
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservPhysical": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

Í þessu tilviki gildir eftirfarandi útreikningur:

`AvailableToReserve` = `fno.availphysical` + `pos.inbound`–`pos.outbound` –`iv.SoftReservPhysical`  
= 70 + 50 – 20 – 90  
= 10

Því ef þú reynir að gera fyrirvara á`iv.SoftReservPhysical`, og magnið er minna en eða jafnt og`AvailableToReserve` (10), mun mjúka fyrirvarabeiðnin ná fram að ganga.

> [!NOTE]
> Þegar þú kallar á API frátekningu er hægt að stjórna staðfestingu frátekningar með því að tilgreina Boolean `ifCheckAvailForReserv` færibreytu í meginmáli beiðninnar. Verðmæti á`True` þýðir að staðfestingin er nauðsynleg, en gildið á`False` þýðir að staðfestingin er ekki nauðsynleg (þó að þú gætir endað með neikvætt`AvailableToReserve` magn, kerfið mun samt leyfa þér að mjúkan varasjóð). Sjálfgefið gildi er `True`.

### <a name="soft-reservation-hierarchy"></a>Mjúkt frátekningarstigveldi

Frátekningarstigveldið útskýrir röð vídda sem þarf að tilgreina þegar frátekningar eru gerðar. Það virkar á sama hátt og stigveldi fyrir atriðaskrá afurðar virkar fyrir lagerfyrirspurnir.

Frátekningarstigveldið er óháð stigveldi atriðaskráar. Þetta sjálfstæði gerir þér kleift að innleiða flokkastjórnun þar sem notendur sundurliðað víddirnar í smáatriði til að tilgreina kröfurnar við að gera nákvæmari frátekningar. Mjúka frátekningastigveldið ætti að innihalda `SiteId` og `LocationId` sem þætti vegna þess að þeir setja saman skilgreiningu þáttunarinnar. Þegar frátekningin er gerð þarftu að tilgreina þáttun fyrir afurðina.

Hér er dæmi um mjúkt pöntunarstigveldi.

| Grunnvídd | Stigveldi |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

Í þessu dæmi er hægt að gera frátekningu í eftirfarandi víddarröðum. Tilgreina verður þáttun fyrir afurðina þegar þú gerir frátekningu. Þess vegna er grunnstigveldið sem þú getur notað er `(SiteId, LocationId)`.

- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Gild víddarröð ætti að fylgja nákvæmlega frátekningastigveldinu, vídd eftir vídd. Til dæmis er stigveldisröðin `(SiteId, LocationId, SizeId)` ekki gild því það vantar `ColorId`.

## <a name="available-to-promise-configuration-optional"></a>Í boði til að lofa stillingum (valfrjálst)

Þú getur sett upp birgðasýnileika til að gera þér kleift að skipuleggja framtíðar breytingar á hendi og reikna út magn sem er tiltækt til að lofa (ATP). ATP er magn vöru sem er tiltækt og hægt er að lofa viðskiptavinum á næsta tímabili. Notkun þessa útreiknings getur aukið getu þína til að uppfylla pöntunina til muna. Til að nota þennan eiginleika verður þú að virkja hann á **Eiginleikastjórnun** flipann og settu hann síðan upp á **ATP stilling** flipa. Fyrir frekari upplýsingar, sjá [Birgðasýnileiki fyrirliggjandi breytingaráætlanir og hægt að lofa](inventory-visibility-available-to-promise.md).

## <a name="complete-and-update-the-configuration"></a>Ljúka við og uppfæra skilgreininguna

Þegar þú hefur lokið við skilgreininguna þarftu að gera allar breytingarnar í birgðasýnileika. Fylgdu þessum skrefum til að framfylgja breytingunum.

1. Í Power Apps, á **Stillingar** síðu, veldu **Uppfærðu stillingar** í efra hægra horninu. 
1. Kerfið biður um innskráningarskilríki. Sláðu inn eftirfarandi gildi:

    - **Biðlarakenni** – Forritsauðkenni Azure sem þú bjóst til fyrir birgðasýnileika.
    - **Leigjandakenni** – Azure-leigjandakennið þitt.
    - **Leynilykill biðlara** – Leynilykill forrits í Azure sem þú bjóst til fyrir birgðasýnileika.

    Fyrir frekari upplýsingar um þessi skilríki og hvernig á að finna þau, sjá [Settu upp og settu upp Birgðasýnileika](inventory-visibility-setup.md).

    > [!IMPORTANT]
    > Vertu viss um að sannreyna heiti gagnagjafans, efnislegar mælingar og víddarvörp áður en þú uppfærir stillinguna. Þú munt ekki geta breytt þessum stillingum eftir að þú hefur uppfært þær.

1. Eftir innskráningu skaltu velja **Uppfærðu stillingar** aftur. Kerfið beitir stillingunum þínum og sýnir hvað hefur breyst.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Dæmi um sjálfgefna skilgreiningu

Á upphafsstigi setur birgðasýnileiki upp sjálfgefna skilgreiningu, sem er útskýrð hér. Hægt er að breyta þessari skilgreiningu eftir þörfum.

### <a name="data-source-configuration"></a>Skilgreining gagnagjafa

#### <a name="configuration-of-the-iv-data-source"></a>Skilgreining iv gagnagjafans

Í þessum kafla er lýst hvernig `iv` gagnagjafinn er skilgreindur.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Líkamlegar ráðstafanir stilltar fyrir „iv“ gagnagjafann

Eftirfarandi efnislegar mælingar eru skilgreindar fyrir `iv` gagnagjafann:

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>Reiknuð mæling OrderedTotal

Reiknuð mæling `OrderedTotal` er skilgreind fyrir `iv` gagnagjafann eins og sýnt er í eftirfarandi töflu.

| Reiknigerð | Gagnaveita | Efnisleg mæling |
|---|---|---|
| samlagning | `fno` | `Ordered` |
| samlagning | `fno` | `Arrived` |
| samlagning | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>Reiknuð mæling OnHand

Reiknuð mæling `OnHand` er skilgreind fyrir `iv` gagnagjafann eins og sýnt er í eftirfarandi töflu.

| Reiknigerð | Gagnaveita | Efnisleg mæling |
|---|---|---|
| samlagning | `fno` | `PhysicalInvent` |
| samlagning | `iom` | `OnHand` |
| samlagning | `erp` | `Unrestricted` |
| samlagning | `erp` | `QualityInspection` |
| samlagning | `pos` | `PosInbound` |
| Frádráttur | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>Reiknuð mæling ReservedTotal

Reiknuð mæling `ReservedTotal` er skilgreind fyrir `iv` gagnagjafann eins og sýnt er í eftirfarandi töflu.

| Reiknigerð | Gagnaveita | Efnisleg mæling |
|---|---|---|
| samlagning | `fno` | `ReservPhysical` |
| samlagning | `fno` | `ReservOrdered` |
| samlagning | `iv` | `SoftReservPhysical` |
| samlagning | `iv` | `SoftReservOrdered` |
| samlagning | `iv` | `ReservPhysical` |
| samlagning | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>Reiknuð mæling SoftReserved

Reiknuð mæling `SoftReserved` er skilgreind fyrir `iv` gagnagjafann eins og sýnt er í eftirfarandi töflu.

| Reiknigerð | Gagnaveita | Efnisleg mæling |
|---|---|---|
| samlagning | `iv` | `SoftReservPhysical` |
| samlagning | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>Reiknuð mæling HardReserved

Reiknuð mæling `HardReserved` er skilgreind fyrir `iv` gagnagjafann eins og sýnt er í eftirfarandi töflu.

| Reiknigerð | Gagnaveita | Efnisleg mæling |
|---|---|---|
| samlagning | `fno` | `ReservPhysical` |
| samlagning | `fno` | `ReservOrdered` |
| samlagning | `iv` | `ReservPhysical` |
| samlagning | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>Reiknuð mæling OpenOrder

Reiknuð mæling `OpenOrder` er skilgreind fyrir `iv` gagnagjafann eins og sýnt er í eftirfarandi töflu.

| Reiknigerð | Gagnaveita | Efnisleg mæling |
|---|---|---|
| samlagning | `fno` | `OnOrder` |
| samlagning | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>Reiknuð mæling OnHandAvailable

Reiknuð mæling `OnHandAvailable` er skilgreind fyrir `iv` gagnagjafann eins og sýnt er í eftirfarandi töflu.

| Reiknigerð | Gagnaveita | Efnisleg mæling |
|---|---|---|
| samlagning | `fno` | `PhysicalInvent` |
| samlagning | `iom` | `OnHand` |
| samlagning | `erp` | `Unrestricted` |
| samlagning | `erp` | `QualityInspection` |
| samlagning | `pos` | `PosInbound` |
| Frádráttur | `fno` | `ReservPhysical` |
| Frádráttur | `iv` | `SoftReservPhysical` |
| Frádráttur | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>Tiltæk reiknuð mæling ToReserve

Reiknuð mæling `AvailableToReserve` er skilgreind fyrir `iv` gagnagjafann eins og sýnt er í eftirfarandi töflu.

| Reiknigerð | Gagnaveita | Efnisleg mæling |
|---|---|---|
| samlagning | `fno` | `PhysicalInvent` |
| samlagning | `iom` | `OnHand` |
| samlagning | `erp` | `Unrestricted` |
| samlagning | `erp` | `QualityInspection` |
| samlagning | `pos` | `PosInbound` |
| samlagning | `fno` | `Ordered` |
| samlagning | `fno` | `Arrived` |
| samlagning | `iv` | `Ordered` |
| Frádráttur | `fno` | `ReservPhysical` |
| Frádráttur | `fno` | `ReservOrdered` |
| Frádráttur | `iv` | `SoftReservPhysical` |
| Frádráttur | `iv` | `SoftReservOrdered` |
| Frádráttur | `iv` | `ReservPhysical` |
| Frádráttur | `iv` | `ReservOrdered` |
| Frádráttur | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>Reiknuð mæling InventorySupply

Reiknuð mæling `InventorySupply` er skilgreind fyrir `iv` gagnagjafann eins og sýnt er í eftirfarandi töflu.

| Reiknigerð | Gagnaveita | Efnisleg mæling |
|---|---|---|
| samlagning | `fno` | `Ordered` |
| samlagning | `fno` | `Arrived` |
| samlagning | `iv` | `Ordered` |
| samlagning | `fno` | `PhysicalInvent` |
| samlagning | `iom` | `OnHand` |
| samlagning | `erp` | `Unrestricted` |
| samlagning | `erp` | `QualityInspection` |
| samlagning | `pos` | `PosInbound` |
| Frádráttur | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>Reiknuð mæling InventoryDemand

Reiknuð mæling `InventoryDemand` er skilgreind fyrir `iv` gagnagjafann eins og sýnt er í eftirfarandi töflu.

| Reiknigerð | Gagnaveita | Efnisleg mæling |
|---|---|---|
| samlagning | `fno` | `OnOrder` |
| samlagning | `iom` | `OnOrder` |
| samlagning | `iv` | `SoftReservPhysical` |
| samlagning | `iv` | `SoftReservOrdered` |
| Viðbót | `fno` | `ReservPhysical` |
| Viðbót | `fno` | `ReservOrdered` |
| Viðbót | `iv` | `ReservPhysical` |
| Viðbót | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>Stilling „fno“ gagnagjafans

Í þessum kafla er lýst hvernig `fno` gagnagjafinn er skilgreindur.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Víddarkortanir fyrir „fno“ gagnagjafann

Vörpun vídda sem er sýnd í eftirfarandi töflu er skilgreind fyrir `fno` gagnagjafann.

| Ytri vídd | Grunnvídd |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Líkamlegar ráðstafanir stilltar fyrir „fno“ gagnagjafann

Eftirfarandi efnislegar mælingar eru skilgreindar fyrir `fno` gagnagjafann:

- `Arrived`
- `PhysicalInvent`
- `ReservPhysical`
- `onorder`
- `notspecified`
- `availordered`
- `availphysical`
- `picked`
- `postedqty`
- `quotationreceipt`
- `received`
- `ordered`
- `ReservOrdered`

#### <a name="configuration-of-the-pos-data-source"></a>Stilling „pos“ gagnagjafans

Í þessum kafla er lýst hvernig gagnagjafinn `pos` er skilgreindur.

##### <a name="physical-measures-for-the-pos-data-source"></a>Líkamlegar mælingar fyrir „pos“ gagnagjafann

Eftirfarandi efnislegar mælingar eru skilgreindar fyrir `pos` gagnagjafann:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>Reiknuð mæling AvailQuantity

Reiknuð mæling `AvailQuantity` er skilgreind fyrir `pos` gagnagjafann eins og sýnt er í eftirfarandi töflu.

| Reiknigerð | Gagnaveita | Efnisleg mæling |
|---|---|---|
| Viðbót | `fno` | `AvailPhysical` |
| Viðbót | `pos` | `PosInbound` |
| Frádráttur | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>Stilling "iom" gagnagjafans

Eftirfarandi efnislegar mælingar eru skilgreindar fyrir `iom` (snjalla pantanastjórnun) gagnagjafann:

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>Stilling „erp“ gagnagjafans

Eftirfarandi efnislegar mælingar eru skilgreindar fyrir `erp` (skipulagsáætlun fyrirtækis) gagnagjafann:

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>Skilgreining þáttunar

Eftirfarandi tafla sýnir skilgreiningu sjálfgefnar þáttunar.

| Grunnvídd | Stigveldi |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>Skilgreining atriðaskrár

Eftirfarandi tafla sýnir skilgreiningu sjálfgefinnar atriðaskráar.

| Stilla númer | Vídd | Stigveldi |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>Skilgreining frátekningar

Þessi hluti lýsir sjálfgefinni skilgreiningu frátekningar.

#### <a name="reservation-mapping"></a>Vörpun frátekningar

Eftirfarandi tafla sýnir sjálfgefna frátekningarvörpun.

| Gagnagjafi efnislegrar mælingar | Efnisleg mæling | Í boði fyrir gagnagjafa frátekningar | Í boði fyrir reiknaða mælingu frátekningar |
|---|---|---|---|
| `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Frátekningarstigveldi

Eftirfarandi tafla sýnir sjálfgefið frátekningarstigveldi.

| Grunnvídd | Stigveldi |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
