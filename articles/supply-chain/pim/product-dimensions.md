---
title: Afurðarvíddir
description: Það eru fimm afurðarvíddir - litur, skilgreining, stærð, stíll og útgáfa. Afurðavíddir eru sameinaðar í víddaflokka og víddaflokkum er úthlutað á afurðarsniðmát. Samsetning afurðavídda ræður til um það hvernig afurðarafbrigði eru skilgreind.
author: t-benebo
manager: tfehr
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle, EcoResVersionNameLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bdfd9482d30bd65cf84fae032df78e1243e05239
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430106"
---
# <a name="product-dimensions"></a>Afurðarvíddir

[!include [banner](../includes/banner.md)]

Það eru fimm afurðarvíddir: litur, skilgreining, stærð, stíll og útgáfa. Afurðavíddir eru sameinaðar í víddaflokka og víddaflokkum er úthlutað á afurðarsniðmát. Samsetning afurðavídda ræður til um það hvernig afurðarafbrigði eru skilgreind.

Afurðavíddir eru einkenni sem notaður er til að auðkenna afurðarafbrigði. Hægt er að nota samsetningu afurðavídda til að skilgreina afurðarafbrigði. Skilgreina verður minnst eina vídd afurðar fyrir afurðarsniðmát til að stofna afurðarafbrigði.

## <a name="product-variants"></a>Afurðarafbrigði

Afurðarafbrigði eru einnig nefndar vörur. Vara er áþreifanleg afurð sem er ekki það sama og þjónusta. Einnig hægt að skilgreina afurðarsniðmát með þjónustugerðina. Með því að nota þjónustugerð, er hægt að tilgreina afurðarafbrigði sem innihalda þjónustu. Til dæmis er hægt að tilgreina afurðarsniðmát fyrir ráðgjafavinnu og afurða afbrigði fyrir vinnustöð sem er framkvæmd með hjá utanaðkomandi ráðgjöfum bókara og aðalbókara hjá utanaðkomandi ráðgjöfum.

## <a name="product-dimensions"></a>Afurðarvíddir

Hægt er að mynda afurðarafbrigði fyrir á grundvelli afurðarvíddargildi.

Hægt er að stofna afurðavíddargildi fyrir stærðar-, litar- og stílvíddir á eftirfarandi stöðum:

- Síðan **Stærð** (**Afurðaupplýsingastjórnun \> Uppsetning \> Vídda- og afbrigðaflokkar \> Stærðir**)
- Síðan **Litur** (**Afurðaupplýsingastjórnun \> Uppsetning \> Vídda- og afbrigðaflokkar \> Litir**)
- Síðan **Stíll** (**Afurðaupplýsingastjórnun \> Uppsetning \> Vídda- og afbrigðaflokkar \> Stílar**)

Afurðavíddargildi fyrir skilgreiningarvíddina eru yfirleitt stofnaðar með annaðhvort afurðarafbrigðastillinum eða afurðarafbrigðastillinum sem byggir á víddum. 

Afurðarútgáfur eru yfirleitt stofnaðar fyrir tilteknar útgáfur þar sem afurðin þróast á líftíma hennar. Ítarleg umfjöllun um afurðaútgáfur koma síðar í þessu efnisatriði.

Vöruvíddir er einnig hægt að stofnað og þeim viðhaldið í **afurðarvíddir** síðu, sem fæst frá eftirfarandi staðsetningum:

- Opna **upplýsingar um afurðastjórnun \> Afurðir \> Afurðarsniðmát**. Á aðgerðasvæðinu skal velja **Afurðarvíddir**.
- Opnið **Upplýsingastjórnun afurða \> Afurðir \> Allar afurðir og afurðarsniðmát**. Veljið afurðarsniðmát. Á aðgerðasvæðinu skal velja **Afurðarvíddir**.
- Opnið **Upplýsingastjórnun afurðar \> Útgefnar afurðir**. Veljið afurðarsniðmát. Á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Afurðarsniðmát**, skal velja **Afurðarvíddir**.

Númer vöruvíddasamsetningar sem hægt er að stofna fyrir vöru er takmörkuð af fjölda afurð mögulegar samsetningar.

> [!TIP]
> Þegar þú notar afurð á til dæmis pöntunarlínu velurðu afurðarvíddirnar til að tilgreina afurðarafbrigðið sem á að vinna með.

## <a name="example"></a>Dæmi

Fyrirtæki selur denim-gallabuxur. Varan, *gallabuxur*, notar lit og stærð afurðarvíddirnar. Gallabuxurnar eru til í þremur mismunandi litum og sex mismunandi stærðum. Litirnir eru blár, svartur og brúnn. Stærðirnar eru XS, S, M, L, XL og XXL. Ekki eru allar stærðir í boði í öllum þremur litunum. Ef boðið væri upp á allar samsetningar væru til 18 mismunandi gerðir af gallabuxum. Í þessu dæmi eru hinsvegar aðeins eftirfarandi níu samsetningar afurðarafbrigða framleiddar.

| Litur | Stærð |
|-------|------|
| Blátt  | XS   |
| Blátt  | L    |
| Blátt  | M    |
| Svart | M    |
| Svart | L    |
| Svart | XL   |
| Brúnt | L    |
| Brúnt | XL   |
| Brúnt | XXL  |

## <a name="the-version-product-dimension"></a>Afurðarvídd útgáfunnar

Útgáfa er afurðarvídd sem er ætluð til að vinna með og rekja margar útgáfur af afurð í gegnum aðfangakeðjuna. Útgáfurakning er nauðsynleg fyrir velgengni framleiðenda sem starfa í heimi stöðugt minnkandi líftíma afurða, aukinna gæða og kröfur um áreiðanleika og aukinnar áherslu á öryggi afurða.

Sem stöðluð afurðarvídd, mun útgáfa hegða sér á svipaðan hátt og núverandi afurðarvíddir (stærð, stíll, litur og afbrigði). Þess vegna er hægt að nota hana í öðrum tilgangi en að rekja útgáfur afurða.

### <a name="turn-on-the-version-dimension"></a><a name="enable-version-dim"></a>Kveikja á útgáfuvíddinni

#### <a name="before-you-turn-on-the-version-dimension"></a>Áður en kveikt er á vídd útgáfunnar

Þegar kveikt er á útgáfuvíddinni gæti einhver virkni rofnað eða hætt að virka eins og búist er við ef aðrar lausnir hafa verið settar upp sem bæta við sérstillingum á birgðavíddunum. Til að útgáfuvíddin sýni fulla virkni þarf hugsanlega að uppfæra þessar lausnir þannig að þær innihaldi útgáfuvíddina í tilvísunum þeirra í birgðavíddirnar.

Þegar samhæfi lausnanna gagnvart útgáfuvíddinni er prófuð skal leita að eftirfarandi einingum:

1. **Virkni:** Mikilvægast er að leggja þarf mat á allar sérstillingar sem hafa með birgðavíddirnar að gera til að tryggja að þær geti virkað í samhliða útgáfuvíddinni.
1. **Tilvísanir í birgðavíddir:** Leitaðu að tilvísunum í birgðavíddirnar (þ.e. staði þar sem sérstaklega er vísað í víddirnar). Tilvísanir í `InventDimId` ættu að virka strax, en hafðu augun opin fyrir tilvísunum í stíl eða lit. Til dæmis skal gæta þess að skoða eftirfarandi einingar:

    - API-köll í stækkuðum klösum
    - Allar tilvísanir í tilteknar birgðavíddir í viðbótarkóða (þessi kóði verður að fleyta útgáfuvíddina ásamt stíl, lit og stærðarvíddir.)

1. **Tilvísanir í úrelt API-köll:** Í kynningu sinni á útgáfuvíddinni hefur Microsoft reynt að gera sem fæst API-köll úrelt og mögulegt er. Þessi fáu API sem hafa verið úreld senda frá sér aðvörun þegar kveikt er á skilgreiningarlyklinum **Afurðarvídd - útgáfa**. Köll í þessi API verða að vera fest í stækkuðum lausnum áður en kveikt er á útgáfuvíddinni í framleiðslukerfi. Hér eru úrelt útgáfumiðuð API:

    - RetailTransactionServiceInventory::getProductRecordId
    - EcoResProductNumberIdentifiedProductVariantEntity::find
    - EGAISAlcoholProduction_RU::findByItemDim
    - PCVariantConfiguration::findByProductMasterAndDimensions

1. **Varpanir:** Ef einhverjar varpanir nota birgðavíddirnar, þarf að uppfæra samsvarandi tengslavarpanir til þess að þær innihaldi útgáfuvíddina. Í stækkaða líkaninu eða töfluviðbótinni skal leita að töflum þar sem reitirnir innihalda birgðavíddir.
1. **Microsoft Dynamics 365 Commerce virkni:** Þegar kveikt er á henni mun útgáfuvíddin birtast í gegnum Commerce-kóðann í Dynamics 365 Supply Chain Management. Hins vegar er útgáfuvíddin ekki enn studd af gagnagrunnsrás Commerce eða í forritum sölustaðar (POS) eða forritum fyrir rafræn viðskipti. Þessir viðskiptasértæku forrit styðja ekki notendur við að selja/afhenda eða skila/taka á móti birgðum eftir útgáfuvídd. Uppflettingar á birgðum fyrir birgðaframboð munu ekki birta birgðir eftir útgáfuvíddum í Commerce forritum. Þessi hegðun líkist núverandi hegðun skilgreiningarvíddarinnar í gegnum Commerce.

#### <a name="turn-on-the-version-dimension"></a>Kveikja á útgáfuvíddinni

Áður en hægt er að nota útgáfuvíddina þarf að vera kveikt á henni í kerfinu. Þetta verk krefst stjórnandaheimildar.

1. Opna skal **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**.
1. Kveikið á eiginleikanum sem kallast *Útgáfa afurðarvíddar*. (Frekari upplýsingar er að finna í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Setja kerfið í [Viðhaldsstillingu](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Opnið **Kerfisstjórnun \> Setja upp \> Skilgreining leyfis**.
1. Í flipanum **Skilgreiningarlyklar** skal útvíkka **Viðskipti** og velja gátreitinn fyrir **Afurðarvídd - útgáfa**.
1. Slökkva skal á [Viðhaldsstillingu](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

### <a name="areas-where-the-version-dimension-isnt-supported"></a>Svæði þar sem útgáfuvíddin er ekki studd

Eftirfarandi svæði styðja ekki útgáfuvíddina vegna þess að kynning á þessari vídd gæti valdið breytingum sem leiða til bilunar:

- Mánaðarlegt yfirlit kostnaðarhluta
- Skyndiminni yfirlits kostnaðarhlutar
- MCR-upplýsingar um sölu á vöru
- Vörulistar lánardrottna
- EcoResProductDimensionGroupEntity

Að auki styðja eiginleikar fyrir stofnun pöntunar og pöntunarúrvinnslu í Commerce (t.d. pantanir á sölustað, í símaveri og rafrænum viðskiptum) ekki útgáfuvíddina. Engin staðfest tímalína er til um hvenær Commerce-pantanir verða stækkaðar til að styðja hana.

### <a name="functional-characteristics-of-the-version-dimension"></a>Hagnýt einkenni útgáfuvíddarinnar

Útgáfuvíddin virkar eins og aðrar afurðavíddir. Hins vegar, vegna sérstakt eðlis hennar, og vegna þess að henni er ætlað að viðhalda og rekja margar útgáfur af afurð, hegðar hún sér örlítið öðruvísi. Hér er dæmi um það sem er líkt og ólíkt:

- **Það er enginn útgáfuflokkur.**

    Þótt hugtök um flokka sé til fyrir stærð, lit og stíl (litaflokkur, stærðarflokkur og stílflokkur), er ekki til neinn útgáfuflokkur. Flokkar gera kleift að skilgreina fyrirfram viðeigandi gildi svo að þegar til dæmis litaflokki er úthlutað á afurð, getur afurðin notað alla litina í þeim litaflokki. Þetta hugtak á ekki við um útgáfuvíddina vegna þess að útgáfurnar sem afurðin tekur eru ekki skilgreindar fyrirfram þegar afurðin er stofnuð. Þess í stað eru útgáfur búnar til á líftíma afurðarinnar, þar sem þær eru nauðsynlegar. Yfirleitt, ef lögun, snið og virkni afurðarinnar helst óbreytt, er stofnuð ný útgáfa í stað nýrrar afurðar.

- **Tillögur um afurðarafbrigði virka eins og þær gera núna.**

    Tillögur um afurðarafbrigði búa til tillögur fyrir öll víddargildi útgáfu, rétt eins og þær gera fyrir aðrar víddir. Ferlið við að búa til og gefa út afurðir með útgáfu er það sama og fyrir afurðir sem nota aðrar víddir. Þegar búin er til útgáfa fyrir afurð, verður fyrsta útgáfan (V1) búin til sem afurðarvídd og afbrigðin verða gefin út. Eftir því sem afurðin breytist og ný útgáfa er nauðsynleg, verður nýja útgáfugildinu (V2) bætt við og nauðsynleg afbrigði verða gefin út. Ekki eru neinar væntingar um að allar útgáfurnar (V1, V2 og V3) verði búnar til fram í tímann fyrir afurðina.

> [!IMPORTANT]
> Ef kveikt er á útgáfuvíddinni og hún notuð, gætu sumar lausnir sem vísa í birgðavíddirnar hætt að virka eins og til er ætlast. Til að staðfesta og laga þessi vandamál skal hafa samband við óháða hugbúnaðarsalann fyrir lausnirnar sem um ræðir. Frekari upplýsingar er að finna í [Virkja útgáfuvíddina](#enable-version-dim).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]