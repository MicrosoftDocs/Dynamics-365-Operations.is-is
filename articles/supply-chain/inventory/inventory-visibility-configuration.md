---
title: Stilla sýnileika birgða
description: Þetta efnisatriði lýsir hvernig á að skilgreina birgðasýnileika.
author: yufeihuang
ms.date: 12/09/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 7e42c0b49a4083edd0e64551f4840bd74d412fc1
ms.sourcegitcommit: 1877696fa05d66b6f51996412cf19e3a6b2e18c6
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/20/2022
ms.locfileid: "8786839"
---
# <a name="configure-inventory-visibility"></a>Stilla sýnileika birgða

[!include [banner](../includes/banner.md)]


Þetta efnisatriði lýsir hvernig á að skilgreina birgðasýnileika með forriti birgðasýnileika í Power Apps.

## <a name="introduction"></a><a name="introduction"></a>Kynning

Áður en byrjað er að vinna með birgðasýnileika þarf að ljúka eftirfarandi skilgreiningu eins og lýst er í þessu efnisatriði:

- [Skilgreining gagnagjafa](#data-source-configuration)
- [Skilgreining þáttunar](#partition-configuration)
- [Skilgreining á stigveldi atriðaskráar](#index-configuration)
- [Skilgreining frátekningar (valfrjálst)](#reservation-configuration)
- [Dæmi um sjálfgefna skilgreiningu](#default-configuration-sample)

## <a name="prerequisites"></a>Forkröfur

Áður en hafist er handa skal setja upp innbót birgðasýnileika eins og lýst er í [Setja upp sýnileika birgða](inventory-visibility-setup.md).

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>Skilgreiningasíða forrits birgðasýnileika

Í Power Apps hjápar síðan **Skilgreining** [Birgðasýnileikaforrits](inventory-visibility-power-platform.md) til við að setja upp lagerskilgreiningu og skilgreiningu mjúkrar frátekningar. Eftir að viðbótin hefur verið sett upp inniheldur sjálfgefna stillingin gildið frá Microsoft Dynamics 365 Supply Chain Management (`fno` gagnagjafinn). Hægt er að fara yfir sjálfgefnu stillingarnar. Byggt á viðskiptaþörfum þínum og þörfum birgðabókunar ytra kerfisins geturðu auk þess breytt skilgreiningunni til að staðla leiðina sem hægt er að bóka, skipuleggja og senda fyrirspurn á birgðabreytingar í hinum ýmsu kerfum. Eftirstandandi hlutar þessa efnisatriðis útskýra hvernig á að nota hvern hluta **Skilgreiningarsíðunnar**.

Þegar skilgreiningunni er lokið skal ganga úr skugga um að velja **Uppfæra skilgreiningu** í forritinu.

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Virkja eiginleika birgðasýnileika í Power Apps eiginleikastjórnun

Innbót birgðasýnileika bætir ýmsum nýjum eiginleika við Power Apps uppsetninguna þína. Sjálfgefið er slökkt á þessum eiginleikum. Til að nota þá skaltu opna **Stillingar** síðu og síðan á **Eiginleikastjórnun** flipann, kveiktu á eftirfarandi eiginleikum eins og þú þarft.

| Heiti eiginleikastjórnunar | Lýsing |
|---|---|
| *OnHandReservation* | Þessi eiginleiki gerir þér kleift að búa til pantanir, neyta bókana og/eða afpanta tiltekið birgðamagn með því að nota Birgðasýnileika. Frekari upplýsingar er að finna í [Frátekningar birgðasýnileika](inventory-visibility-reservations.md). |
| *OnHandMostSpecificBackgroundService* | Þessi eiginleiki veitir birgðayfirlit fyrir vörur, ásamt öllum víddum. Gögn birgðasamantektar verða samstillt reglulega úr birgðasýnileika. Fyrir frekari upplýsingar, sjá [Birgðayfirlit](inventory-visibility-power-platform.md#inventory-summary). |
| *OnhandChangeSchedule* | Þessi valfrjálsi eiginleiki gerir kleift að breyta áætluninni við höndina og eiginleika sem hægt er að lofa (ATP). Fyrir frekari upplýsingar, sjá [Birgðasýnileiki fyrirliggjandi breytingaráætlun og hægt að lofa](inventory-visibility-available-to-promise.md). |
| *Virkja vörur vöruhúss í birgðasýnileika* | Þessi valfrjálsi eiginleiki gerir birgðasýnileika kleift að styðja við vörur sem eru virkjaðar fyrir háþróaða vöruhúsaferla (WHS vörur). Fyrir frekari upplýsingar, sjá [Stuðningur við birgðasýnileika fyrir WHS hluti](inventory-visibility-whs-support.md). |

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Finna endastöð þjónustu

Ef þú veist ekki rétta endastöð fyrir þjónustu birgðasýnileika skaltu opna síðuna **Skilgreining** í Power Apps og því næst velja **Sýna endastöð þjónustu** efst í hægra horninu. Síðan mun sýna rétta endastöð þjónustu.

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Skilgreining gagnagjafa

Hver gagnagjafi táknar kerfi sem gögnin þín koma úr. Dæmi um heiti gagnagjafa innihalda`fno` (sem þýðir "Dynamics 365 Finance and Operations forrit") og`pos` (sem þýðir "sölustaður"). Supply Chain Management er sjálfgefið sett upp sem sjálfgefinn gagnagjafi (`fno`) í birgðasýnileika.

> [!NOTE]
> The`fno` gagnauppspretta er frátekin fyrir Supply Chain Management. Ef birgðasýnileikaviðbótin þín er samþætt við Supply Chain Management umhverfi mælum við með að þú eyðir ekki stillingum sem tengjast`fno` í gagnaveitunni.

Til að bæta við gagnagjafa skal fylgja þessum skrefum.

1. Skráðu þig inn í Power Apps umhverfið og opnaðu **Birgðasýnileika**.
1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Gagnagjafi** skal velja **Nýr gagnagjafi** til að bæta við gagnagjafa.

> [!NOTE]
> Þegar þú bætir við gagnagjafa skaltu ganga úr skugga um að staðfesta heiti gagnagjafans, efnislegar mælingar og víddarvarpanir áður en þú uppfærir skilgreininguna fyrir þjónustu birgðasýnileika. Þú getur ekki breytt þessum stillingum eftir að þú hefur valið **Uppfæra skilgreiningu**.

Skilgreining gagnagjafa inniheldur eftirfarandi hluta:

- Víddir (vörpun víddar)
- Efnislegar mælingar
- Reiknaðar mælingar

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Víddir (vörpun víddar)

Tilgangur víddarskilgreiningar er að staðla samþættingu margra kerfa fyrir bókun tilvika og fyrirspurna samkvæmt víddarsamsetningum. Birgðasýnileiki býður upp á lista yfir grunnvíddir sem hægt er að varpa úr víddunum í gagnagjafann þinn. Þrjátíu og þrjár víddir eru í boði fyrir kortlagningu.

- Sjálfgefið notar þú Supply Chain Management sem einn af gagnagjöfunum þínum, 13 víddir eru varpaðar í staðlaðar víddir Supply Chain Management. Tólf öðrum víddum (`inventDimension1` til `inventDimension12`) er varpað í sérstilltar víddir í Supply Chain Management. Eftirstandandi átta víddir eru útvíkkaðar víddir sem hægt er að varpa í ytri gagnagjafa.
- Ef þú notar ekki Supply Chain Management sem einn af gagnagjöfum þínum getur þú varpað víddunum eins og þér sýnist. Eftirfarandi tafla sýnir heildarlista yfir tiltækar víddir.

> [!NOTE]
> Ef víddin þín er ekki á lista yfir sjálfgefnar víddir og þú ert að nota ytri gagnagjafa mælum við með að þú notir `ExtendedDimension1` til `ExtendedDimension8` til að gera vörpunina.

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
> Víddargerðirnar sem eru sýndar í töflunni hér á undan eru aðeins tilvísandi. Þú þarft ekki að skilgreina þær í birgðasýnileika.
>
> Birgðavíddir (sérstilltar) kunna að vera fráteknar fyrir Supply Chain Management. Í því tilviki er hægt að nota útvíkkaðar víddir í staðinn.

Ytri kerfi geta fengið aðgang að birgðasýnileika í gegnum RESTful API. Fyrir samþættinguna gerir birgðasýnileiki þér kleift að skilgreina _ytri gagnagjafa_ og vörpunina úr _ytri víddum_ í _grunnvíddir_. Hér er dæmi um töflu víddarvörpunar.

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
1. Í flipanum **Gagnagjafi**, í hlutanum **Vörpun vídda**, skal velja **Bæta við** til að bæta við vörpunum vídda.
    ![Vörpun vídda bætt við](media/inventory-visibility-dimension-mapping.png "Vörpun vídda bætt við")

1. Í reitnum **Heiti víddar** skal tilgreina upprunavíddina.
1. Í reitnum **Til grunnvíddar** skal velja víddina í birgðasýnileika sem á að varpa.
1. Veldu **Vista**.

Ef til dæmis gagnagjafinn þinn inniheldur litavídd afurðar getur þú varpað hennir í `ColorId` grunnvíddina til að bæta við `ProductColor` sérstilltri vídd í `exterchannel` gagnagjafanum. Henni er síðan varpað í `ColorId` grunnvíddina.

### <a name="physical-measures"></a><a name="data-source-configuration-physical-measures"></a>Efnislegar mælingar

Þegar gagnagjafi bókar birgðabreytingu í birgðasýnileika bókar hann þá breytingu með því að nota *efnislegar mælingar*. Efnislegar mælingar breyta magninu og endurspegla birgðastöðuna. Þú getur skilgreint þínar eigin efnislegu mælingar samkvæmt þínum kröfum. Hægt er að byggja fyrirspurnir á efnislegum mælingum.

Birgðasýnileiki veitir lista yfir sjálfgefnar efnislegar mælingar sem eru tengdar við Supply Chain Management (`fno` gagnagjafann). Þessar sjálfgefnu efnislegu mælingar eru teknar úr birgðafærslustöðum á síðunni **Lagerlisti** í Supply Chain Management (**Birgðastjórnun \> Fyrirspurnir og skýrslur \> Lagerlisti**). Eftirfarandi tafla sýnir dæmi um efnislegar mælieiningar.

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

Ef gagnagjafinn er Supply Chain Management þarftu ekki að búa aftur til sjálfgefnar efnislegar mælingar. Fyrir ytri gagnagjafa þarftu hinsvegar að búa til nýjar efnislegar mælingar með því að fylgja þessum skrefum.

1. Skráðu þig inn í Power Apps umhverfið og opnaðu **Birgðasýnileika**.
1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Gagnagjafi**, í hlutanum **Efnislegar mælingar**, skal velja **Bæta við**, tilgreina heiti upprunamælingar og vista breytingarnar.

### <a name="calculated-measures"></a>Reiknaðar mælingar

Þú getur notað birgðasýnileika til að senda fyrirspurn á bæði efnislegar mælingar birgða og *sérstilltar reiknaðar mælingar*. Reiknaðar mælingar bjóða upp á sérstillta reikniformúlu sem samanstendur af samsetningu efnislegra mælieininga. Þessi virkni gerir þér kleift að skilgreina safn efnislegra mælieininga sem verður bætt við og/eða safn efnislegra mælieininga sem verða dregnar frá, til að búa til sérstillta mælingu.

> [!IMPORTANT]
> Reiknaður mælikvarði er samsetning líkamlegra mælikvarða. Formúla hennar getur aðeins innihaldið líkamlegar mælingar án afrita, ekki reiknaðar mælikvarða.

Stillingin gerir þér kleift að skilgreina safn af breytilyklum sem er bætt við eða dregnir frá til að fá samtals uppsafnað magn úttaks.

Til að setja upp sérstillta reiknaða mælingu skal fylgja þessum skrefum.

1. Skráðu þig inn í Power Apps umhverfið og opnaðu **Birgðasýnileika**.
1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Reiknuð mæling** skal velja **Ný reiknuð mæling** til að bæta við reiknaðri mælingu.
1. Stilltu eftirfarandi reiti fyrir nýju útreiknuðu mælinguna:

    - **Nýtt útreiknað málsheiti** – Sláðu inn heiti reiknaðs mælingar.
    - **Uppspretta gagna** – Veldu gagnagjafann sem tengist nýja breytinum. Fyrirspurnarkerfið er gagnagjafi.

1. Veldu **Bæta við** til að bæta við breytu við nýja reiknaða mælinguna.
1. Stilltu eftirfarandi reiti fyrir nýja breytimanninn:

    - **Breytir** – Veldu breytigerð (*Viðbót* eða *Frádráttur*).
    - **Uppspretta gagna** – Veldu gagnagjafann þar sem mælikvarðinn sem gefur breytigildið á að finnast.
    - **Mæla** – Veldu heiti mælingar (frá völdum gagnagjafa) sem gefur upp gildi fyrir breytimann.

1. Endurtaktu skref 5 til 6 þar til þú hefur bætt við öllum nauðsynlegum breytingum.
1. Veldu **Vista**.

Þú gætir til dæmis verið með eftirfarandi niðurstöður fyrirspurnar.

```json
[
    {
        "productId": "T-shirt",
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
            "externalchannel": {
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
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

Þegar þessi reikniformúla er notuð, mun nýja niðurstaða fyrirspurnar fela í sér sérstilltu mælinguna.

```json
[
    {
        "productId": "T-shirt",
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
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
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

Lausnin inniheldur þessa skiptingastillingu sjálfgefið. Þess vegna, *þú þarft ekki að skilgreina það sjálfur*.

> [!IMPORTANT]
> Ekki sérsníða sjálfgefna skiptinguna. Ef þú eyðir því eða breytir því er líklegt að þú valdi óvæntri villu.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Skilgreining á stigveldi atriðaskráar

Oftast verður fyrirspurn um lagerbirgðir ekki eingöngu á hæsta stigi „samtölu“. Í staðinn gætirðu líka viljað sjá niðurstöður sem eru teknar saman út frá birgðavíddum.

Birgðavíddir bjóða upp á sveigjanleika með því að leyfa þér að setja upp _atriðaskrár_. Þessar atriðaskrár byggja á vídd eða samsetningu vídda. Atriðaskrá samanstendur af *stilltu númeri*, *vídd* og *stigveldu* eins og er skilgreint í eftirfarandi töflu.

| Nafn | lýsing |
|---|---|
| Stilla númer | Víddir sem tilheyra sama safni (atriðaskrá) verða flokkaðar saman og þeim verður úthlutað sama stillta númerinu. |
| Vídd | Grunnvíddir sem niðurstaða fyrirspurnar er lögð saman á. |
| Stigveldi | Stigveldið er notað til að skilgreina studdar víddarsamsetningar sem hægt er að senda fyrirspurn á. Til dæmis er sett um víddasamstæða sem er með stigveldisröðina `(ColorId, SizeId, StyleId)`. Í þessu tilfelli styður kerfið fyrirspurnir um fjórar víddarsamsetningar. Fyrsta samsetningin er tóm, önnur er `(ColorId)`, þriðja er `(ColorId, SizeId)` og fjórða er `(ColorId, SizeId, StyleId)`. Aðrar samsetningar eru ekki studdar. Frekari upplýsingar er að finna í dæminu sem fylgir. |

Til að setja upp atriðaskrá afurðastigveldis skal fylgja þessum skrefum.

1. Skráðu þig inn í Power Apps umhverfið og opnaðu **Birgðasýnileika**.
1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Atriðaskrá afurðastigveldis**, í hlutanum **Vörpun vídda**, skal velja **Bæta við** til að bæta við vörpunum vídda.
1. Listi yfir atriðaskrár er sjálfgefið gefinn upp. Til að breyta núverandi atriðaskrá skal velja **Breyta** eða **Bæta við** í hlutanum fyrir viðeigandi atriðaskrá. Til að búa til nýja atriðaskrá skal velja **Nýtt safn atriðaskráar**. Fyrir hverja línu í hverju safni atriðaskráar, í reitnum **Vídd**, skal velja úr listanum yfir grunnvíddir. Gildi fyrir eftirfarandi reiti eru sjálfkrafa búin til:

    - **Stilla númer** – Víddir sem tilheyra sama flokknum (atriðaskrá) verða flokkaðar saman og þeim verður úthlutað sama stillta númerinu.
    - **Stigveldi** – Stigveldið er notað til að skilgreina studdar víddarsamsetningar sem hægt er að senda fyrirspurn á í víddaflokki (atriðaskrá). Ef til dæmis er settur upp víddaflokkur sem er með stigveldisröðina *Stíll*, *Litur* og *Stærð* styður kerfið niðurstöðu þriggja fyrirspurnarflokka. Fyrsti hópurinn er eingöngu stíll. Annar hópurinn er sambland af stíl og lit. Og þriðji hópurinn er sambland af stíl, lit og stærð. Aðrar samsetningar eru ekki studdar.

### <a name="example"></a>Dæmi

Þessi hluti býður upp á dæmi sem sýnir hvernig stigveldið virkar.

Eftirfarandi tafla sýnir lista yfir tiltækar birgðir fyrir þetta dæmi.

| vara | ColorId | SizeId | StyleId | Magn |
|---|---|---|---|---|
| Stuttermabolur | Svart | Lítill | Breitt | 1 |
| Stuttermabolur | Svart | Lítill | Venjulegt | 2 |
| Stuttermabolur | Svart | Stór | Breitt | 3 |
| Stuttermabolur | Svart | Stór | Venjulegt | 4 |
| Stuttermabolur | Rauður | Lítill | Breitt | 5 |
| Stuttermabolur | Rauður | Lítill | Venjulegt | 6 |
| Stuttermabolur | Rauður | Stór | Venjulegt | 7 |

Eftirfarandi tafla sýnir hvernig stigveldi atriðaskráar er sett upp.

| Stilla númer | Vídd | Stigveldi |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Atriðaskráin gerir þér kleift að senda fyrirspurn á lagerbirgðirnar á eftirfarandi hátt:

- `()` – Flokkað eftir öllum

    - Bolur, 28

- `(ColorId)` – flokkað eftir `ColorId`

    - Bolur, svartur, 10
    - Bolur, rauður, 18

- `(ColorId, SizeId)` – Flokkað eftir samsetningu `ColorId` og `SizeId`

    - Bolur, svartur, lítill, 3
    - Bolur, svartur, stór, 7
    - Bolur, rauður, lítill, 11
    - Bolur, rauður, stór, 7

- `(ColorId, SizeId, StyleId)` – Flokkað eftir samsetningu `ColorId`, `StyleId` og `SizeId`

    - Bolur, svartur, lítill, víður, 1
    - Bolur, svartur, lítill, venjulegur, 2
    - Bolur, svartur, stór, víður, 3
    - Bolur, svartur, stór, venjulegur, 4
    - Bolur, rauður, lítill, víður, 5
    - Bolur, rauður, lítill, venjulegur, 6
    - Bolur, rauður, stór, venjulegur, 7

> [!NOTE]
> Grunnvíddir sem eru skilgreindar í skilgreiningu þáttunar eiga ekki að vera skilgreindar í skilgreiningum atriðaskráar.
> 
> Ef þú verður að spyrjast eingöngu fyrir um birgðir sem eru teknar saman eftir öllum víddarsamsetningum, geturðu sett upp eina vísun sem inniheldur grunnvíddina `Empty`.

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Skilgreining frátekningar (valfrjálst)

Skilgreining bókunar er nauðsynleg ef þú vilt nota eiginleika mjúkrar frátekningar. Skilgreiningin samanstendur af tveimur grunnþáttum:

- Mjúk frátekningarvörpum
- Mjúkt frátekningarstigveldi

### <a name="soft-reservation-mapping"></a>Mjúk frátekningarvörpum

Þegar þú gerir frátekningu gætir þú viljað vita hvort lagerbirgðir séu tiltækar núna fyrir frátekningu. Staðfestingin er tengd við reiknaða mælingu sem stendur fyrir reikniformúlu sem er samsetning efnislegra mælieininga.

Með því að setja upp vörpun úr efnislegri mælingu í reiknaða mælingu gerir þú þjónustu birgðasýnileika kleift að sjálfkrafa staðfesta stöðu frátekningar samkvæmt efnislegu mælingunni.

Áður en þessi vörpun er sett upp þarf að skilgreina efnislegar mælingar, reiknaðar mælingar og gagnagjafa þeirra í flipunum **Gagnagjafi** og **Reiknuð mæling** á síðunni **Skilgreining** í Power Apps (eins og lýst er fyrr í þessu efnisatriði).

Til að skilgreina vörpun mjúkrar frátekningar skal fylgja þessum skrefum.

1. Skilgreindu efnislega mælingu sem þjónar hlutverki mælingar mjúkrar frátekningar (til dæmis `SoftReservOrdered`).
1. Í flipanum **Reiknuð mæling** á síðunni **Skilgreining** skal skilgreina reiknuðu mælinguna *má taka frá* (AFR) sem inniheldur reikniformúlu AFR sem ætlunin er að varpa í efnislega mælingu. Til dæmis væri hægt að setja upp `AvailableToReserve` (í boði fyrir frátekningu) þannig að það sé varpað í fyrir skilgreiningu `SoftReservOrdered` efnislegrar mælingu. Á þennan hátt er hægt að sjá hvaða magn sem er með `SoftReservOrdered` birgðastöðuna verður í boði fyrir frátekningu. Eftirfarandi tafla sýnir AFR-reikniformúluna.

    | Reiknigerð | Gagnaveita | Efnisleg mæling |
    |---|---|---|
    | samlagning | `fno` | `AvailPhysical` |
    | samlagning | `pos` | `Inbound` |
    | Frádráttur | `pos` | `Outbound` |
    | Frádráttur | `iv` | `SoftReservOrdered` |

    Við mælum með því að þú setjir upp reiknaða mælingu þannig að hún innihaldi efnislega mælingu sem mæling frátekningar byggir á. Þannig mun magn reiknaðrar mælingar verða fyrir áhrifum af magni frátekningarmælingar. Í þessu dæmi ætti því `AvailableToReserve` reiknuð mæling `iv` gagnagjafans að innihalda `SoftReservOrdered` efnislega mælingu frá `iv` sem þátt.

1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Vörpun mjúkrar frátekningar** skal setja upp vörpunina úr efnislegu mælingunni í reiknaða mælingu. Í fyrra dæminu er hægt að nota eftirfarandi stillingar til að varpa `AvailableToReserve` í fyrri skilgreiningu `SoftReservOrdered` efnislegrar mælingar.

    | Gagnagjafi efnislegrar mælingar | Efnisleg mæling | Í boði fyrir gagnagjafa frátekningar | Í boði fyrir reiknaða mælingu frátekningar |
    |---|---|---|---|
    | `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > Ef þú getur ekki breytt flipanum **Vörpun mjúkrar frátekningar** gætir þú þurft að kveikja á eiginleikanum *OnHandReservation* í flipanum **Eiginleikastjórnun**.

Nú, þegar þú gerir frátekningu á `SoftReservOrdered`, mun birgðasýnileiki sjálfkrafa finna `AvailableToReserve` og tengda reikniformúlu til að staðfesta frátekninguna.

Þú getur til dæmis verið með eftirfarandi lagerbirgðir í birgðasýnileika.

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
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

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
= 70 + 50 – 20 – 90  
= 10

Ef þú reynir þar af leiðandi að gera frátekningar á `iv.SoftReservOrdered` og magnið er minna en eða jafnt og `AvailableToReserve` (10) getur þú tekið frá.

> [!NOTE]
> Þegar þú kallar á API frátekningu er hægt að stjórna staðfestingu frátekningar með því að tilgreina Boolean `ifCheckAvailForReserv` færibreytu í meginmáli beiðninnar. Gildi `True` þýðir að staðfesting sé nauðsynleg og á móti merkir gildið `False` að staðfestingin er ekki nauðsynleg. Sjálfgefið gildi er `True`.

### <a name="soft-reservation-hierarchy"></a>Mjúkt frátekningarstigveldi

Frátekningarstigveldið útskýrir röð vídda sem þarf að tilgreina þegar frátekningar eru gerðar. Það virkar á sama hátt og stigveldi fyrir atriðaskrá afurðar virkar fyrir lagerfyrirspurnir.

Frátekningarstigveldið er óháð stigveldi atriðaskráar. Þetta sjálfstæði gerir þér kleift að innleiða flokkastjórnun þar sem notendur sundurliðað víddirnar í smáatriði til að tilgreina kröfurnar við að gera nákvæmari frátekningar. Mjúka frátekningastigveldið ætti að innihalda `SiteId` og `LocationId` sem þætti vegna þess að þeir setja saman skilgreiningu þáttunarinnar. Þegar frátekningin er gerð þarftu að tilgreina þáttun fyrir afurðina.

Hér er dæmi um mjúkt frátekningastigveldi.

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

Þegar þú hefur lokið við skilgreininguna þarftu að gera allar breytingarnar í birgðasýnileika. Til að koma á breytingum skaltu velja **Uppfæra skilgreiningu** efst í hægra horni síðunnar **Skilgreining** í Power Apps.

Í fyrsta sinn sem þú velur **Uppfæra skilgreiningu** óskar kerfið eftir innskráningarupplýsingunum þínum.

- **Biðlarakenni** – Forritsauðkenni Azure sem þú bjóst til fyrir birgðasýnileika.
- **Leigjandakenni** – Azure-leigjandakennið þitt.
- **Leynilykill biðlara** – Leynilykill forrits í Azure sem þú bjóst til fyrir birgðasýnileika.

Þegar þú hefur skráð þig inn er skilgreiningin uppfærð í þjónustu birgðasýnileika.

> [!NOTE]
> Gakktu úr skugga um að staðfesta heiti gagnagjafans, efnislegar mælingar og víddarvarpanir áður en þú uppfærir skilgreininguna fyrir þjónustu birgðasýnileika. Þú getur ekki breytt þessum stillingum eftir að þú hefur valið **Uppfæra skilgreiningu**.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Dæmi um sjálfgefna skilgreiningu

Á upphafsstigi setur birgðasýnileiki upp sjálfgefna skilgreiningu, sem er útskýrð hér. Hægt er að breyta þessari skilgreiningu eftir þörfum.

### <a name="data-source-configuration"></a>Skilgreining gagnagjafa

#### <a name="configuration-of-the-iv-data-source"></a>Skilgreining iv gagnagjafans

Í þessum kafla er lýst hvernig `iv` gagnagjafinn er skilgreindur.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Efnislegar mælingar skilgreindar fyrir iv gagnagjafann

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
| samlagning | `fno` | `ReservPhysical` |
| samlagning | `fno` | `ReservOrdered` |
| samlagning | `iv` | `ReservPhysical` |
| samlagning | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>Skilgreining fno gagnagjafa

Í þessum kafla er lýst hvernig `fno` gagnagjafinn er skilgreindur.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Vörpun vídda fyrir fno gagnagjafann

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

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Efnislegar mælingar skilgreindar fyrir fno gagnagjafann

Eftirfarandi efnislegar mælingar eru skilgreindar fyrir `fno` gagnagjafann:

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>Skilgreining pos gagnagjafans

Í þessum kafla er lýst hvernig gagnagjafinn `pos` er skilgreindur.

##### <a name="physical-measures-for-the-pos-data-source"></a>Efnislegar mælingar fyrir pos gagnagjafann

Eftirfarandi efnislegar mælingar eru skilgreindar fyrir `pos` gagnagjafann:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>Reiknuð mæling AvailQuantity

Reiknuð mæling `AvailQuantity` er skilgreind fyrir `pos` gagnagjafann eins og sýnt er í eftirfarandi töflu.

| Reiknigerð | Gagnaveita | Efnisleg mæling |
|---|---|---|
| samlagning | `fno` | `AvailPhysical` |
| samlagning | `pos` | `PosInbound` |
| Frádráttur | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>Skilgreining iom gagnagjafans

Eftirfarandi efnislegar mælingar eru skilgreindar fyrir `iom` (snjalla pantanastjórnun) gagnagjafann:

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>Skilgreining erp gagnagjafans

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
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Frátekningarstigveldi

Eftirfarandi tafla sýnir sjálfgefið frátekningarstigveldi.

| Grunnvídd | Stigveldi |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10 |
| `WMSPalletId` | 11 |
| `ConfigId` | 12 |
| `VersionId` | 13 |
| `CustomDimension1` | 14 |
| `CustomDimension2` | 15 |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
