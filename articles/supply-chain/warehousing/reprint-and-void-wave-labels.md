---
title: Endurprenta og ógilda bylgjumerki
description: Þetta efnisatriði útskýrir hvernig á að ógilda og endurprenta fyrirliggjandi bylgjumerki.
author: GarmMSFT
manager: PJacobse
ms.date: 07/09/2020
ms.topic: article
ms.service: dynamics-ax-applications
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSWaveTableListPage, WHSWorkException, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelLayout, WHSWaveLabelType, WHSWaveLabelTemplateGroup
audience: Application User
ms.reviewer: PJacobse
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: cc76a3915d6a1e58a71eb997b5af58941905e879
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996049"
---
# <a name="reprint-and-void-wave-labels"></a>Endurprenta og ógilda bylgjumerki

[!include [banner](../includes/banner.md)]

Þetta efni útskýrir hvernig á að stjórna merkjum sem eru búin til með bylgjuvinnslu. (Nánari lýsingu og stillingarleiðbeiningar er að finna í [Skilgreina prentun bylgjumerkis](../warehousing/configure-wave-label-printing.md).)

Hægt er að endurprenta bylgjumerki hvenær sem er. Til dæmis gætirðu þurft að prenta staka merkimiða ef núverandi merkimiði tapaðist eða skemmdist. Að öðrum kosti gæti starfsmaður í vöruhúsi eða yfirmaður þurft að prenta heila merkimiðarúllu aftur ef fjöldi og/eða samsetning heillrar raðar af bylgjumerkjum hefur breyst (til dæmis vegna birgðaskorts eða af öðrum ástæðum). Oft, jafnvel þótt aðeins fjöldi kassa hafi breyst, verður að prenta alla rúlluna aftur til að halda heildarfjöldanum nákvæmum í „Kassi X af Y“ hlutanum fyrir hvern merkimiða.

Endurprentunareiginleiki bylgjumerkja styður eftirfarandi virkni:

- Prenta aftur merkimiða úr bæði vöruhúsaforriti og fjölhæfum biðlara.
- Ógilda merkimiða og prenta þá aftur samtímis. (Möguleikinn til að ógilda merkimiða er til dæmis felld inn í atburðarásir stuttra tiltekta.)
- Hreinsa feril bylgjumerkis.

Þetta efnisatriði kemur með ýmsar atburðarási sem sýna, með dæmum, hvernig á að vinna með endurprentunareiginleika bylgjumerkja.

> [!IMPORTANT]
> Til að fara í gegnum atburðarásirnar sem settar eru fram í þessu efnisatriði þarf fyrst að kveikja á og skilgreina viðeigandi eiginleika bylgjuprentunar, eins og lýst er í [Skilgreina prentun bylgjumerkis](../warehousing/configure-wave-label-printing.md). Nokkrar atburðarásanna í þessu efnisatriði krefjast þess einnig að fyrst sé farið í gegnum atburðarásirnar í þessu efnisatriði til að búa til áskilin sýnigögn.

## <a name="scenario-1-reprint-labels-from-the-web-client"></a>Atburðarás 1: Endurprenta merkimiða úr vefbiðlaranum

Hægt er að skoða og endurprenta bylgjumerki á eftirfarandi síðum. Á aðgerðasvæði hverrar síðu, í flipanum **Sendingar**, í flokknum **Tengdar upplýsingar**, skal velja **Bylgjumerki**.

- Allar sendingar \> Upplýsingar sendingar
- Allar hleðslur \> Upplýsingar um hleðslu
- Allar bylgjur
- Bylgjumerki
- Ferill bylgjumerkis

Til að endurprenta bylgjumerki úr vefbiðlaranum skal fylgja þessum skrefum.

1. Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.
1. Veljið bylgjuna til að endurprenta merkimiða úr.
1. Á aðgerðasvæðinu, í flipanum **Bylgja**, í flokknum **Prenta**, skal velja **Bylgjumerki**.
1. Veljið annað eða bæði eftirfarandi skref:

    - Til að endurprenta merkimiðann skal velja prentara í reitnum **Heiti prentara**. (Skiljið þennan reit eftir auðan ef aðeins á að uppfæra upplýsingar um bylgjumerki, án þess að endurprenta merkimiðann.)
    - Til að uppfæra merkimiðann skal velja gátreitinn **Uppfæra upplýsingar um bylgjumerki**. (Skiljið þennan gátreit eftir auðan ef aðeins á að endurprenta fyrri merkimiða.)

    > [!NOTE]
    > Í hvert skipti sem bylgjumerki er prentað eða endurprentað, er gögnum þess breytt í gegnum viðeigandi útlit bylgjumerkis og öllum staðgenglum er skipt út fyrir raungildi. Viðeigandi strengur er geymdur sem færsla í ferli bylgjumerkis. Ef gátreiturinn **Uppfæra upplýsingar um bylgjumerki** er hreinsaður, eru vistuðu gögn Zebra-forritunarmálsins notuð þegar merkimið er endurprentaður. Ef gátreiturinn **Uppfæra upplýsingar um bylgjumerki** er valinn, er nýr strengur búinn til. Núverandi bylgjumerki eru einnig endurútreiknuð og allir umfram merkimiðar (til dæmis ef hætt hefur verið við tengdar vinnulínur eða þeim breytt) eru merktar sem **Ógildir** og eru ekki endurprentaðir.

1. Veljið **Í lagi** til að staðfesta valið.

## <a name="scenario-2-reprint-labels-from-the-warehousing-app"></a>Atburðarás 2: Endurprenta merkimiða úr vöruhúsaforritinu

Þessi atburðarás á venjulega við ef merkimiðarúlla hefur tapast eða skemmst. Hún býður upp á dæmi sem sýnir hvernig á að setja upp valmyndaratriði fartækis sem gera starfsmönnum kleift að endurprenta einn og marga merkimiða. Hún sýnir síðan hvernig á að nota nýju valmyndaratriðin á meðan unnið er í fartæki.

### <a name="set-up-the-required-menu-items-and-menu-for-the-mobile-device"></a>Setja upp nauðsynleg valmyndaratriði og valmynd fyrir fartæki

Áður en starfsmenn geta endurprentað merkimiða úr fartæki þarf að setja upp valmyndaratriði til að bjóða upp á þessa virkni og bæta þessum hlutum síðan við valmynd vöruhúsaforritsins.

#### <a name="create-new-mobile-device-menu-items"></a>Búa til ný valmyndaratriði fartækis

Fylgið þessum skrefum til að búa til nýtt safn af valmyndaratriðum til að endurprenta merkimiða úr vöruhúsaforritinu.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Búið til valmyndaratriði og stillið eftirfarandi gildi fyrir það:

    - **Heiti valmyndaratriðis:** *Endurprenta eitt bylgjumerki*
    - **Titill:** *Prenta aftur stakt bylgjumerki*
    - **Stilling:** *Óbein*
    - **Kóði verkþáttar:** *Endurprenta eitt bylgjumerki*

1. Búið til annað valmyndaratriði og stillið eftirfarandi gildi fyrir það:

    - **Heiti valmyndaratriðis:** *Endurprenta merkimiða (vara)*
    - **Titill:** *Endurprenta bylgjumerki (vara)*
    - **Stilling:** *Óbein*
    - **Kóði verkþáttar:** *Endurprenta mörg bylgjumerki*
    - **Sýna flokkunarsíu verkefnalista:** *Já*
    - **Reitur kerfisflokkunar:** *ShipmentID*
    - **Merkimiði kerfisflokkunar:** *Auðkenni sendingar*
    - **Prentstilling:** *Vara*

1. Á aðgerðasvæðinu skal velja **Reitalisti** til að opna síðu þar sem hægt er að velja reitina sem starfskraftar fá að sjá til að auðvelda þeim að bera kennsl á rétta miðarúllu.
1. Þú getur sýnt allt að sjö reiti. Notið fellilistana til að velja reitinn sem sýndur er í hverri lausri stöðu. Skildu reitina sem þú þarft ekki eftir auða. 

    Eftirfarandi er dæmi:

    - **Upplýsingasvæði:** *LabelItemId*
    - **Upplýsingasvæði 2:** *LabelItemName*
    - **Upplýsingasvæði 3:** *InventQty*
    - **Upplýsingasvæði 4:** *LabelUnitId*

1. Lokið síðunni.
1. Búið til þriðja valmyndaratriðið og stillið eftirfarandi gildi fyrir það:

    - **Heiti valmyndaratriðis:** *Endurprenta merkimiða (fasttexti)*
    - **Titill:** *Endurprenta bylgjumerki (fasttexti)*
    - **Stilling:** *Óbein**
    - **Kóði verkþáttar:** *Endurprenta mörg bylgjumerki*
    - **Sýna flokkunarsíu verkefnalista:** *Já*
    - **Reitur kerfisflokkunar:** *ShipmentID*
    - **Merkimiði kerfisflokkunar:** *Auðkenni sendingar*
    - **Prentstilling:** *Tölusetning*

1. Á aðgerðasvæðinu skal velja **Reitalisti** og síðan nota fellilistana til að velja reitina sem starfskraftar fá að sjá til að auðvelda þeim að bera kennsl á rétta miðarúllu (t.d. *LabelItemId*, *LabelItemName*, *InventQty*, *LabelUnitId*, and *NumberOfLabels*).
1. Lokið síðunni.
1. Búið til fjórða valmyndaratriðið og stillið eftirfarandi gildi fyrir það:

    - **Heiti valmyndaratriðis:** *Endurprenta merkimiða (eftir síðasta)*
    - **Titill:** *Endurprenta bylgjumerki (eftir síðasta)*
    - **Stilling:** *Óbein*
    - **Kóði verkþáttar:** *Endurprenta mörg bylgjumerki*
    - **Sýna flokkunarsíu verkefnalista:** *Já*
    - **Reitur kerfisflokkunar:** *ShipmentID*
    - **Merkimiði kerfisflokkunar:** *Auðkenni sendingar*
    - **Prentstilling:** *Síðasta kenni bylgjumerkis sem var í lagi*

1. Á aðgerðasvæðinu skal velja **Reitalisti** og síðan nota fellilistana til að velja reitina sem starfskraftar fá að sjá til að auðvelda þeim að bera kennsl á rétta miðarúllu (t.d. *LabelItemId*, *LabelItemName*, *InventQty*, *LabelUnitId*, and *NumberOfLabels*).
1. Lokið síðunni.

#### <a name="set-up-the-mobile-device-menu"></a>Uppsetning á valmynd fartækis

Fylgið þessum skrefum til að bæta nýju valmyndaratriðunum við valmynd vöruhúsaforritsins.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.
1. Veljið fyrirliggjandi valmynd **Á útleið**.
1. Í listanum til vinstri skal finna valmyndaratriði endurprentunar sem voru búin til og síðan nota hægri örvarhnappinn til að bæta þeim við listann hægra megin.
1. Lokið síðunni.

### <a name="use-cases"></a>Dæmi um notkun

Notkunartilfellin sem hér er að finna gefa dæmi sem sýna hvernig á að nota hin ýmsu valmyndaratriði fartækis sem sett voru upp til að gera starfsmönnum kleift að endurprenta bylgjumerki.

Áður en farið er í gegnum þessi notkunartilfelli, verða eftirfarandi skilyrði að vera til staðar:

- Setja þarf upp sýnigögn og velja þarf lögaðilann **USMF**.
- Skilgreina þarf prentun bylgjumerkis og búa þarf til suma merkimiða eins og lýst er í [Skilgreina prentun bylgjumerkis](../warehousing/configure-wave-label-printing.md).

#### <a name="use-case-21-a-single-wave-label-is-scratched-and-must-be-reprinted"></a>Notkunartilfelli 2.1: Stakt bylgjumerki er rispað og þarf að endurprenta.

1. Skráðu þig inn í vöruhúsaforritið sem notandi með aðgang að vöruhúsi *62*. (Í venjulegu sýnigögnunum geturðu skráð þig inn með notandakenninu *62* og aðgangsorðinu *1*.)
1. Farið í **Á útleið \> Endurprenta eitt bylgjumerki**.
1. Sláið inn eða skannið auðkenni bylgjumerkis.
1. Veljið prentarann til að endurprenta með.
1. Veljið **Í lagi** til að staðfesta aðgerðina.

#### <a name="use-case-22-several-labels-for-boxes-of-the-same-item-were-damaged-and-must-be-reprinted-each-label-has-a-product-bar-code-but-no-enumeration-or-sscc-number"></a>Notkunartilfelli 2.2: Nokkrir merkimiðar fyrir kassa af sömu vörunni skemmdust og þarf að endurprenta. Hver merkimiði er með strikamerki vöru en enga tölusetningu eða SSCC-númer.

1. Skráðu þig inn í vöruhúsaforritið sem notandi sem hefur aðgang að vöruhúsi *62*. (Í venjulegu sýnigögnunum geturðu skráð þig inn með notandakenninu *62* og aðgangsorðinu *1*.)
1. Farið í **Á útleið \> Endurprenta merkimiða (vara)**.
1. Sláið inn eða skannið auðkenni sendingar.
1. Veljið reitinn sem er með rétta miðarúllu til að endurprenta.
1. Skannið strikamerki vörunnar úr fyrirliggjandi merkimiða til að staðfesta að rétt lína hafi verið valin.
1. Færið inn miðafjöldann sem þarf að endurprenta.
1. Veljið prentarann til að endurprenta með.
1. Veljið **Í lagi** til að staðfesta aðgerðina.

#### <a name="use-case-23-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-because-the-labels-have-enumeration-you-can-define-the-carton-range-to-reprint"></a>Notkunartilfelli 2.3: Nokkrir merkimiðar fyrir kassa prentuðust ekki út af stíflu í prentara. Merkimiðarnir eru tölusettir og þess vegna er hægt að skilgreina kassabilið sem þarf að endurprenta.

1. Skráðu þig inn í vöruhúsaforritið sem notandi sem hefur aðgang að vöruhúsi *62*. (Í venjulegu sýnigögnunum geturðu skráð þig inn með notandakenninu *62* og aðgangsorðinu *1*.)
1. Farið í **Á útleið \> Endurprenta merkimiða (fasttexti)**.
1. Sláið inn eða skannið auðkenni sendingar.
1. Veljið reitinn sem er með rétta miðarúllu til að endurprenta.
1. Færið inn fyrsta kassann sem endurprenta þarf miða fyrir.
1. Færið inn síðasta kassann sem endurprenta þarf miða fyrir. Einnig er hægt að skilja reitinn eftir auðan til að endurprenta merkimiða fyrir alla kassa eftir fyrsta kassann sem var tilgreindur.
1. Veljið prentarann til að endurprenta með.
1. Veljið **Í lagi** til að staðfesta aðgerðina.

#### <a name="use-case-24-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-the-last-good-label-has-a-wave-label-id-that-is-printed-as-a-bar-code"></a>Notkunartilfelli 2.4: Nokkrir merkimiðar fyrir kassa prentuðust ekki út af stíflu í prentara. Síðasti merkimiðinn sem var í lagi er með auðkenni bylgjumerkis sem er prentað sem strikamerki.

1. Skráðu þig inn í vöruhúsaforritið sem notandi sem hefur aðgang að vöruhúsi *62*. (Í venjulegu sýnigögnunum geturðu skráð þig inn með notandakenninu *62* og aðgangsorðinu *1*.)
1. Farið í **Á útleið \> Endurprenta merkimiða (eftir síðasta)**.
1. Sláið inn eða skannið auðkenni sendingar.
1. Veljið reitinn sem er með rétta miðarúllu til að endurprenta.
1. Sláið inn eða skannið auðkenni bylgjumerkis fyrir síðasta bylgjumerkið sem var í lagi. Forritið lítur á næsta merkimiðann í röðinni sem fyrsta kassann sem merkimiði verður prentaður aftur fyrir.
1. Færið inn síðasta kassann sem endurprenta þarf miða fyrir. Einnig er hægt að skilja reitinn eftir auðan til að endurprenta merkimiða fyrir alla kassa eftir fyrsta kassann sem var tilgreindur.
1. Veljið prentarann til að endurprenta með.
1. Veljið **Í lagi** til að staðfesta aðgerðina.

## <a name="scenario-3-short-pick-and-reprint"></a>Atburðarás 3: Stutt tiltekt og endurprentun

Áður en farið er í gegnum þessa atburðarás, verða eftirfarandi skilyrði að vera til staðar:

- Setja þarf upp sýnigögn og velja þarf lögaðilann **USMF**.
- Skilgreina þarf prentun bylgjumerkis og búa þarf til suma merkimiða eins og lýst er í [Skilgreina prentun bylgjumerkis](../warehousing/configure-wave-label-printing.md).

### <a name="set-up-work-exceptions"></a>Setja upp vinnuundantekningar

Undantekningar vinnu stjórna hegðun lítillar tiltektar. Fylgið þessum skrefum til að setja upp undantekningu vinnu.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Undantekningar verks**.
1. Búið til færslu sem er með eftirfarandi stillingum:

    - **Undantekningarkóði vinnu:** *Stutt tiltekt og prentun*
    - **Gerð undantekningar:** *Stutt tiltekt*
    - **Leggja til endurprentun á bylgjumerki:** *Já*

### <a name="void-and-reprint-after-a-short-pick"></a>Ógilda og endurprenta eftir stutta tiltekt

1. Skráðu þig inn í vöruhúsaforritið sem notandi sem hefur aðgang að vöruhúsi *62*. (Í venjulegu sýnigögnunum geturðu skráð þig inn með notandakenninu *62* og aðgangsorðinu *1*.)
1. Opnið verkflæði vinnuferlis fyrir vinnu sölupöntunar sem búin var til þegar bylgjumerki voru upphaflega prentuð.
1. Veljið **Stutt tiltekt**.
1. Veljið undantekningarkóða vinnu sem búinn var til fyrir þessa atburðarás.
1. Ef rétta undantekningin var valin ætti gátreiturinn **Ógilda og prenta aftur** að vera tiltækur. Veldu þennan reit og staðfestu. Þegar staðfest, verður röð miðarúllunnar sem reiturinn **Smíðakenni merkis** ber kennsl á endurreiknuð út frá breyttu magni vinnulínu. Hún er síðan endurprentuð á tilteknum prentara.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]