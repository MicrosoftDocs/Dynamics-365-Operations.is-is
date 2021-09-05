---
title: Forrit birgðasýnileika
description: Í þessu efnisatriði er lýst hvernig á að nota forrit birgðasýnileika.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: cc09dd82547ec42041889e9a96662cd17549a3ea
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345003"
---
# <a name="inventory-visibility-app"></a>Forrit birgðasýnileika

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er lýst hvernig á að nota forrit birgðasýnileika.

Birgðasýnileiki býður upp á líkanadrifið forrit fyrir myndræna framsetningu. Forritið inniheldur þrjár síður: **Skilgreining**, **Rekstrarsýnileiki** og **Birgðasamantekt**. Það er með eftirfarandi eiginleika:

- Það býður upp á notandaviðmót fyrir lagerskilgreiningu og skilgreiningu mjúkrar frátekningar.
- Það styður fyrirspurnir lagerbirgða í rauntíma í ýmsum víddarsamsetningum.
- Það býður upp á notendaviðmót fyrir bókun frátekningarbeiðna.
- Það býður upp á sérstillt yfirlit yfir lagerbirgðir fyrir afurðir með öllum víddum

## <a name="prerequisites"></a>Forkröfur

Áður en hafist er handa skal setja upp innbót birgðasýnileika eins og lýst er í [Setja upp sýnileika birgða](inventory-visibility-setup.md).

## <a name="configuration"></a><a name="configuration"></a>Grunnstilling

Síðan **Skilgreining** hjálpar þér að setja upp lagerskilgreiningu og skilgreiningu mjúkrar frátekningar. Eftir að viðbótin hefur verið sett upp inniheldur sjálfgefna stillingin gildið frá Microsoft Dynamics 365 Supply Chain Management (`fno` gagnagjafinn). Hægt er að fara yfir sjálfgefnu stillinguna. Byggt á viðskiptaþörfum þínum og þörfum birgðabókunar ytra kerfisins geturðu auk þess breytt skilgreiningunni í [Dataverse](/powerapps/maker/common-data-service/data-platform-intro) til að staðla leiðina sem hægt er að bóka, skipuleggja og senda fyrirspurn á birgðabreytingar í hinum ýmsu kerfum.

### <a name="define-data-sources"></a>Skilgreina gagnagjafa

Þú skilgreinir hvern *gagnagjafa* sem á að samþætta við birgðasýnileika. Birgðasýnileiki styður samþættingu við ýmsa gagnagjafa á borð við sölustaðarkerfið, Supply Chain Management og önnur ytri kerfi. Supply Chain Management er sjálfgefið sett upp sem sjálfgefinn gagnagjafi (`fno`) í birgðasýnileika.

Til að bæta við gagnagjafa skal fylgja þessum skrefum.

1. Skráðu þig inn í Power Apps umhverfið og opnaðu **Birgðasýnileika**.
1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Gagnagjafi** skal velja **Nýr gagnagjafi** til að bæta við gagnagjafa.

> [!NOTE]
> Þegar þú bætir við gagnagjafa skaltu ganga úr skugga um að staðfesta heiti gagnagjafans, efnislegar mælingar og víddarvarpanir áður en þú uppfærir skilgreininguna fyrir þjónustu birgðasýnileika. Þú getur ekki breytt þessum stillingum eftir að þú hefur valið **Uppfæra skilgreiningu**.

### <a name="set-up-dimension-mappings"></a>Setja upp varpanir vídda

Birgðasýnileiki býður upp á lista yfir grunnvíddir sem hægt er að varpa úr víddunum í gagnagjafann þinn. Þrjátíu og þrjár víddir eru í boði fyrir kortlagningu.

- Sjálfgefið notar þú Supply Chain Management sem einn af gagnagjöfunum þínum, 13 víddir eru varpaðar í staðlaðar víddir Supply Chain Management. Tólf öðrum víddum (`inventDimension1` til `inventDimension12`) er varpað í sérstilltar víddir í Supply Chain Management. Eftirstandandi átta víddir eru útvíkkaðar víddir sem hægt er að varpa í ytri gagnagjafa.
- Ef þú notar ekki Supply Chain Management sem einn af gagnagjöfum þínum getur þú varpað víddunum eins og þér sýnist. Eftirfarandi tafla sýnir heildarlista yfir tiltækar víddir.

> [!NOTE]
> Ef víddin þín er ekki á lista yfir sjálfgefnar víddir og þú ert að nota ytri gagnagjafa mælum við með að þú notir `ExtendedDimension1` til `ExtendedDimension8` til að gera vörpunina.

| Tegund víddar | Heiti víddar |
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
| Annað | `VersionId` |
| Birgðir (sérstillt) | `InventDimension1` til og með `InventDimension12` |
| Annað | `ExtendedDimension1` til og með `ExtendedDimension8` |

Til að bæta við víddarvörpunum skal fylgja þessum skrefum.

1. Skráðu þig inn í Power Apps umhverfið og opnaðu **Birgðasýnileika**.
1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Gagnagjafi**, í hlutanum **Vörpun vídda**, skal velja **Bæta við** til að bæta við vörpunum vídda.
1. Í reitnum **Heiti víddar** skal tilgreina upprunavíddina.
1. Í reitnum **Til grunnvíddar** skal velja víddina í birgðasýnileika sem á að varpa.
1. Veldu **Vista**.

![Vörpun vídda bætt við](media/inventory-visibility-dimension-mapping.png "Vörpun vídda bætt við")

Ef til dæmis gagnagjafinn þinn inniheldur litavídd afurðar getur þú varpað hennir í `ColorId` grunnvíddina til að bæta við `ProductColor` sérstilltri vídd í `exterchannel` gagnagjafanum. Henni er síðan varpað í `ColorId` grunnvíddina.

## <a name="create-a-physical-measure"></a>Búa til efnislega mælingu

Þegar gagnagjafi bókar birgðabreytingu í birgðasýnileika bókar hann þá breytingu með því að nota *efnislegar mælingar*. Efnislegar mælingar eru breytilyklar sem endurspegla samanteknar stöður birgðafærslna. Hægt er að byggja fyrirspurnir á efnislegum mælingum.

Birgðasýnileiki er með lista yfir sjálfgefnar efnislegar mælingar. Þessar sjálfgefnu efnislegu mælingar eru teknar úr birgðafærslustöðum á síðunni **Lagerlisti** í Supply Chain Management (**Birgðastjórnun \> Fyrirspurnir og skýrslur \> Lagerlisti**).

| Umbreytir | Nafn |
|---|---|
| `PhysicalInvent` | Birgðir |
| `ReservPhysical` | Efnislegt magn frátekið |
| `AvailPhysical` | Efnislegt magn til ráðstöfunar |
| `ReservOrdered` | Pantað frátekið |
| `PostedQty` | Bókað magn |
| `Deducted` | Frádregið |
| `Picked` | Tekið til |
| `Received` | Móttekið |
| `Registered` | Skráð |
| `Arrived` | Komið |
| `Ordered` | Raðað |
| `OnOrder` | Í pöntun |
| `QuotationReceipt` | Kvittun tilboðs |
| `QuotationIssue` | Úthreyfing tilboðs |

Ef gagnagjafinn er Supply Chain Management þarftu ekki að búa aftur til sjálfgefnar efnislegar mælingar. Fyrir ytri gagnagjafa þarftu hinsvegar að búa til nýjar efnislegar mælingar með því að fylgja þessum skrefum.

1. Skráðu þig inn í Power Apps umhverfið og opnaðu **Birgðasýnileika**.
1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Gagnagjafi**, í hlutanum **Efnislegar mælingar**, skal velja **Bæta við**, tilgreina heiti upprunamælingar og vista breytingarnar.

## <a name="define-the-product-hierarchy-index"></a>Skilgreina atriðaskrá afurðastigveldis

Með því að setja upp uppsafnaða víddaflokka getur þú notað birgðasýnileika til að senda fyrirspurn vegna lagerbirgðastöðu. Í birgðasýnileika er hver víddaflokkur þekktur sem *atriðaskrá*. Hver atriðaskrá samsvarar stilltu númeri. Þú getur ákveðið hvaða víddir verða notaðar til að setja upp atriðaskrána á grunni þess hvernig þú sendir fyrirspurn til birgðasýnileika.

Til að setja upp atriðaskrá afurðastigveldis skal fylgja þessum skrefum.

1. Skráðu þig inn í Power Apps umhverfið og opnaðu **Birgðasýnileika**.
1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Atriðaskrá afurðastigveldis**, í hlutanum **Vörpun vídda**, skal velja **Bæta við** til að bæta við vörpunum vídda.
1. Listi yfir atriðaskrár er sjálfgefið gefinn upp. Til að breyta núverandi atriðaskrá skal velja **Breyta** eða **Bæta við** í hlutanum fyrir viðeigandi atriðaskrá. Til að búa til nýja atriðaskrá skal velja **Nýtt safn atriðaskráar**. Fyrir hverja línu í hverju safni atriðaskráar, í reitnum **Vídd**, skal velja úr listanum yfir grunnvíddir. Gildi fyrir eftirfarandi reiti eru sjálfkrafa búin til:

    - **Stilla númer** – Víddir sem tilheyra sama flokknum (atriðaskrá) verða flokkaðar saman og þeim verður úthlutað sama stillta númerinu.
    - **Stigveldi** – Stigveldið er notað til að skilgreina studdar víddarsamsetningar sem hægt er að senda fyrirspurn á í víddaflokki (atriðaskrá). Ef til dæmis er settur upp víddaflokkur sem er með stigveldisröðina *Stíll*, *Litur* og *Stærð* styður kerfið niðurstöðu þriggja fyrirspurnarflokka. Fyrsti hópurinn er eingöngu stíll. Annar hópurinn er sambland af stíl og lit. Og þriðji hópurinn er sambland af stíl, lit og stærð. Aðrar samsetningar eru ekki studdar.

Frekari upplýsingar er að finna í [Skilgreining á stigveldi atriðaskráar](inventory-visibility-configuration.md#index-configuration).

### <a name="example"></a>Dæmi

Þessi hluti býður upp á dæmi sem sýnir hvernig stigveldið virkar. Eftirfarandi tafla sýnir lista yfir tiltækar birgðir fyrir þetta dæmi.

| vara | Stíll | Litur | Stærð | Magn |
|---|---|---|---|---|
| I0001 | Breitt | Svart | Lítill | 1 |
| I0001 | Breitt | Svart | Stór | 2 |
| I0001 | Breitt | Rauður | Lítill | 3 |
| I0001 | Venjulegt | Svart | Lítill | 4 |
| I0001 | Venjulegt | Svart | Stór | 5 |
| I0001 | Venjulegt | Rauður | Lítill | 6 |
| I0001 | Venjulegt | Rauður | Stór | 7 |

Eftirfarandi tafla sýnir hvernig stigveldi atriðaskráar er sett upp.

| Lykill | Stilla númer | Stigveldi |
|---|---|---|
| `StyleId` | 1 | 1 |
| `ColorId` | 1 | 2 |
| `SizeId` | 1 | 3 |

Byggt á fyrri stillingum er víddarsamsetningin fyrir fyrirspurn birgðasýnileika *Stíll*, *Litur* og *Stærð*. Uppsetning stigveldis gerir ytri kerfum kleift að senda fyrirspurn um lagerbirgðir á eftirfarandi hátt:

- `()` – Flokkað eftir öllum. Úttakið er:

    - I0001, 28

- `(StyleId)` – Flokka eftir stíl. Úttakið er:

    - I0001, Breiður, 6
    - I0001, Venjulegur, 22

- `(StyleId, ColorId)` – Flokkað eftir samsetningu stíls og litar. Úttakið er:

    - I0001, víður, svartur, 3
    - I0001, víður, rauður, 3
    - I0001, venjulegur, svartur, 9
    - I0001, venjulegur, rauður, 13

- `(StyleId, ColorId, SizeId)` – Flokkað eftir samsetningu stíls, litar og stærðar. Úttakið er:

    - I0001, breiður, svartur, lítill,1
    - I0001, Breiður, svartur, stór, 2
    - I0001, Breiður, Rauður, Lítill, 3
    - I0001, venjulegir, svartur, Lítill, 4
    - I0001, venjulegur, svartur, stór, 5
    - I0001, venjulegur, rauður, lítill, 6
    - I0001, venjulegur, rauður, stór, 7

## <a name="set-up-a-custom-calculated-measure"></a>Setja upp sérstillta reiknaða mælingu

Þú getur notað birgðasýnileika til að senda fyrirspurn á bæði efnislegar mælingar birgða og *sérstilltar reiknaðar mælingar*.

Stillingin gerir þér kleift að skilgreina safn af breytilyklum sem er bætt við eða dregnir frá til að fá samtals uppsafnað magn úttaks.

1. Skráðu þig inn í Power Apps umhverfið og opnaðu **Birgðasýnileika**.
1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Reiknuð mæling** skal velja **Ný reiknuð mæling** til að bæta við reiknaðri mælingu. Því næst skal stilla reitina eins og lýst er í eftirfarandi töflu.

    | Svæði | Virði |
    |---|---|
    | Heiti nýrrar reiknaðrar mælingar | Færðu inn heiti reiknaðrar mælingar. |
    | Gagnaveita | Fyrirspurnarkerfið er gagnagjafi. |
    | Breytir gagnagjafa | Færðu inn gagnagjafa breytilykilsins. |
    | Umbreytir | Færðu inn heiti breytilykils. |
    | Gerð breytilykils | Veldu gerð breytilykils (*Samlagning* eða *Frádráttur*). |

Eftirfarandi tafla sýnir dæmi um `MyCustomAvailableforReservation` sérstillta reiknaða mælingu. Frekari upplýsingar um þetta dæmi er að finna í [Skilgreining gagnagjafa](inventory-visibility-configuration.md#data-source-configuration).

| Gagnagjafi reiknaðrar mælingar | Reiknuð mæling | Breytir gagnagjafa | Umbreytir | Gerð breytilykils |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `Exteexterchannelrchannel` | `reserved` | `Subtraction` |

### <a name="set-up-a-soft-reservation-mapping"></a><a name="setup-reservation-mapping"></a>Uppsetning vörpunar fyrir mjúka frátekningu

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Áður en hægt er að breyta flipanum **Vörpun mjúkrar frátekningar** þarftu að kveikja á eiginleikanum *OnHandReservation* í flipanum **Eiginleikastjórnun**.

Með því að setja upp vörpun úr efnislegri mælingu í reiknaða mælingu gerir þú þjónustu birgðasýnileika kleift að sjálfkrafa staðfesta stöðu frátekningar samkvæmt efnislegu mælingunni.

Áður en þessi vörpun er sett upp þarf að skilgreina efnislegar mælingar, reiknaðar mælingar og gagnagjafa þeirra í flipunum **Gagnagjafi** og **Reiknuð mæling** á síðunni **Skilgreining** í Power Apps (eins og lýst er fyrr í þessu efnisatriði).

Til að skilgreina vörpun mjúkrar frátekningar skal fylgja þessum skrefum.

1. Skilgreindu efnislega mælingu sem þjónar hlutverki mælingar mjúkrar frátekningar (til dæmis `softreservordered`).
1. Í flipanum **Reiknuð mæling** á síðunni **Skilgreining** skal skilgreina reiknuðu mælinguna *má taka frá* (AFR) sem inniheldur reikniformúlu AFR sem ætlunin er að varpa í efnislega mælingu. Til dæmis væri hægt að setja upp `availforreserv` (í boði fyrir frátekningu) þannig að það sé varpað í fyrir skilgreiningu `softreservordered` efnislegrar mælingu. Á þennan hátt er hægt að sjá hvaða magn sem er með `softreservordered` birgðastöðuna verður í boði fyrir frátekningu. Eftirfarandi tafla sýnir AFR-reikniformúluna.

    | Umbreytir | Gagnaveita | Mæla |
    |---|---|---|
    | `Addition` | `fno` | `availphysical` |
    | `Addition` | `pos` | `inbound` |
    | `Subtraction` | `pos` | `outbound` |
    | `Subtraction` | `iv` | `softreservordered` |

1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Vörpun mjúkrar frátekningar** skal setja upp vörpunina úr efnislegu mælingunni í reiknaða mælingu. Í fyrra dæminu er hægt að nota eftirfarandi stillingar til að varpa `availforreserv` í fyrri skilgreiningu `softreservordered` efnislegrar mælingar.

    | Gagnagjafi efnislegrar mælingar | Efnisleg mæling | Í boði fyrir gagnagjafa frátekningar | Í boði fyrir reiknaða mælingu frátekningar |
    |---|---|---|---|
    | `iv` | `softreservordered` | `iv` | `availforreserv` |

### <a name="set-up-a-soft-reservation-hierarchy"></a><a name="setup-reservation-hierarchy"></a>Setja upp stigveldi mjúkrar frátekningar

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Áður en hægt er að breyta flipanum **Stigveldi mjúkrar frátekningar** þarftu að kveikja á eiginleikanum *OnHandReservation* í flipanum **Eiginleikastjórnun**.

Frátekningarstigveldið útskýrir röð vídda sem þarf að tilgreina þegar frátekningar eru gerðar. Það virkar á sama hátt og stigveldi fyrir atriðaskrá afurðar virkar fyrir lagerfyrirspurnir.

Frátekningarstigveldið getið verið öðruvísi en stigveldi fyrir atriðaskrá lagers. Þetta sjálfstæði gerir þér kleift að innleiða flokkastjórnun þar sem notendur sundurliðað víddirnar í smáatriði til að tilgreina kröfurnar við að gera nákvæmari frátekningar.

#### <a name="example"></a>Dæmi

Eftirfarandi frátekningastigveldi er sett upp í kerfinu þínu.

| Vídd | Stigveldi |
|---|---|
| `ColorId` | 1 |
| `SizeId ` | 2 |
| `StyleId` | 3 |

Með þessu frátekningastigveldi getur þú gert frátekningar í eftirfarandi víddaröðum:

- `()` – Engin vídd er gefin upp.
- `(ColorId)`
- `(ColorId, SizeId)`
- `(ColorId, SizeId, StyleId)`

Víddarröðin ætti að fylgja röð frátekningastigveldisins, vídd eftir vídd. Til dæmis eru frátekningar sem eru með `(ColorId, StyleId)` ekki leyfðar í þessu dæmi vegna þess að þessi röð er ekki skilgreind í frátekningastigveldinu.

### <a name="control-feature-management"></a><a name="feature-switch"></a>Stjórna eiginleikastjórnun

Innbót birgðasýnileika býður upp á eiginleika á borð við *OnHandReservation* og *OnHandMostSpecificBackgroundService*. Sjálfgefið er slökkt á þessum eiginleikum. Til að nota þá skal opna síðuna **Skilgreining** í Power Apps og því næst í flipanum **Eiginleikastjórnun** skal kveikja á þeim.

### <a name="complete-and-update-the-configuration"></a>Ljúka við og uppfæra skilgreininguna

Þegar þú hefur lokið við skilgreininguna þarftu að gera allar breytingarnar í birgðasýnileika. Til að koma á breytingum skaltu velja **Uppfæra skilgreiningu** efst í hægra horni síðunnar **Skilgreining** í Power Apps.

Í fyrsta sinn sem þú velur **Uppfæra skilgreiningu** óskar kerfið eftir innskráningarupplýsingunum þínum.

- **Biðlarakenni** – Forritsauðkenni Azure sem þú bjóst til fyrir birgðasýnileika.
- **Leigjandakenni** – Azure-leigjandakennið þitt.
- **Leynilykill biðlara** – Leynilykill forrits í Azure sem þú bjóst til fyrir birgðasýnileika.

Þegar þú hefur skráð þig inn er skilgreiningin uppfærð í þjónustu birgðasýnileika.

> [!NOTE]
> Gakktu úr skugga um að staðfesta heiti gagnagjafans, efnislegar mælingar og víddarvarpanir áður en þú uppfærir skilgreininguna fyrir þjónustu birgðasýnileika. Þú getur ekki breytt þessum stillingum eftir að þú hefur valið **Uppfæra skilgreiningu**.

### <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Finna endastöð þjónustu

Ef þú veist ekki rétta endastöð fyrir þjónustu birgðasýnileika skaltu opna síðuna **Skilgreining** í Power Apps og því næst velja **Sýna endastöð þjónustu** efst í hægra horninu. Síðan mun sýna rétta endastöð þjónustu.

## <a name="operational-visibility"></a>Rekstrarsýnileiki

Síðan **Rekstrarsýnileiki** sýnir niðurstöður fyrirspurnar um lagerbirgðir í rauntíma sem byggir á ýmsum víddarsamsetningum. Þegar kveikt er á eiginleikanum *OnHandReservation* er einnig hægt að bóka beiðnir frátekningar á síðunni **Rekstrarsýnileiki**.

### <a name="on-hand-query"></a>Fyrirspurn lagerbirgða

Flipinn **Fyrirspurn lagerbirgða** sýnir niðurstöður fyrirspurnar vegna lagerbirgða í rauntíma.

Þegar flipinn **Fyrirspurn lagerbirgða** er valinn biður kerfið um innskráningarupplýsingarnar þínar svo það geti fengið handhafalykilinn sem þarf til að senda fyrirspurn á þjónustu birgðasýnileika. Þú getur einfaldlega límt handhafalykilinn í reitinn **BearerToken** og lokað svarglugganum. Þú getur síðan birt beiðni lagerfyrirspurnar.

Ef handhafalykillinn er ekki gildur eða hefur runnið út þarftu að líma nýjan í reitinn **BearerToken**. Færðu inn rétt gildi fyrir **Biðlarakenni**, **Leigjandakenni**, **Leynilykill biðlara** og veldu svo **Endurhlaða**. Kerfið mun sjálfkrafa fá nýjan gildan handhafalykil.

Til að birta beiðni lagerfyrirspurnar skal færa inn fyrirspurnina í meginmál beiðninnar. Notaðu mynstrið sem lýst er í [Fyrirspurn með því að nota bókunaraðferðina](inventory-visibility-api.md#query-with-post-method).

![Stillingar lagerfyrirspurnar](media/inventory-visibility-query-settings.png "Stillingar lagerfyrirspurnar")

### <a name="reservation-posting"></a>Bókun frátekningar

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Notaðu flipann **Bókun frátekningar** til að bóka frátekningarbeiðni. Áður en hægt er að bóka frátekningarbeiðni þarf að kveikja á eiginleikanum *OnHandReservation*. Nánari upplýsingar um þennan eiginleika er að finna í [Frátekningar birgðasýnileika](inventory-visibility-reservations.md).

Til að bóka frátekningarbeiðni þarftu að færa inn gildi í meginmál beiðninnar. Notaðu mynstrið sem lýst er í [Búa til eitt tilvik frátekningar](inventory-visibility-api.md#create-one-reservation-event). Veldu síðan **Bóka**. Til að skoða upplýsingar um svar beiðninnar velur þú **Sýna upplýsingar**. Þú getur einnig fengið gildið **reservationID** í upplýsingum um svarið.

## <a name="inventory-summary"></a>Birgðayfirlit

**Birgðasamantekt** er sérstillt yfirlit fyrir *Einingu fyrir samtölu lagerbirgða*. Þar er að finna birgðasamantekt fyrir afurðir ásamt öllum víddum. Með því að nota **Ítarlega sía** sem Dataverse býður upp á getur þú búið til eigið yfirlit sem sýnir línurnar sem skipta þig máli. Ítarlegir síuvalkostir gera þér kleift að búa til margvísleg yfirlit, bæði einföld og flókin. Þeir gera þér einnig kleift að bæta flokkuðum og földuðum skilyrðum við síurnar.

Frekari upplýsingar um hvernig á að nota **Ítarlega sía** er að finna í [Breyta eða búa til eigin yfirlit með ítarlegum síum hnitanets](/powerapps/user/grid-filters-advanced)

Efst á sérsniðnu yfirliti eru gefnir upp þrír reitir: **Sjálfgefin vídd**, **Sérstillt vídd** og **Mæling**. Hægt er að nota þessa reiti til að stjórna því hvaða dálkar eru sýnilegir.

Hægt er að velja dálkhaus til að sía eða raða núverandi niðurstöðu.

Neðst í sérsniðnu yfirliti eru upplýsingar sýndar á borð við „50 færslur (29 valdar)“ eða „50 færslur“. Þessar upplýsingar vísa í núverandi hladdar færslur úr niðurstöðunni **Ítarleg sía**. Textinn „29 valdar“ vísar til fjölda færslna sem hafa verið valdar með því að nota síu dálkhauss fyrir færslurnar sem var hlaðið inn.

Neðst á yfirlitinu er hnappurinn **Hlaða fleiri** sem þú getur notað til að hlaða fleiri færslur úr Dataverse. Sjálfgefinn færslufjöldi sem hlaðið er inn er 50. Þegar þú velur **Hlaða fleiri** verða næstu 1000 tiltækar færslur hlaðnar inn í yfirlitið. Talan á hnappnum **Hlaða fleiri** gefur til kynna núverandi fjölda að færslum sem er hlaðið inn og heildarfjölda af færslum fyrir niðurstöðu **Ítarlegrar síu**.

![Birgðayfirlit](media/inventory-visibility-onhand-list.png "Birgðayfirlit")
