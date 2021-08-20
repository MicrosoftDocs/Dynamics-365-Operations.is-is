---
title: Sveigjanleikaflokkar
description: Í þessu efnisatriði er því lýst hvernig sveigjanleikaflokkar eru notaðir í tíma og viðveru.
author: johanhoffmann
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgFlexGroup, JmgFlexCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 44d8876aac8f8a3439a9a1285780bcc076c95807b950e3640c2a7523beae3f3e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717029"
---
# <a name="flex-groups"></a>Sveigjanleikaflokkar

[!include[banner](../includes/banner.md)]

Sveigjanlegir vinnutímar leyfa fyrirtækjum að lágmarka greiðslur vegna yfirvinnu með því að bjóða starfskröftum meiri tíma frá vinnu á tímabilum þegar vinnuálag er lítið. Þessi eiginleiki er viðeigandi, til dæmis í hlutum sem upplifa árstíðabundnar breytingar á vinnuálagi.

Hægt er að nota sveigjanleikaflokka til að setja eftirfarandi reglur og meginreglur fyrir sveigjanlegar vinnustundir starfskrafts:

- Reglur um sveigjanleikareglur
- Meginregla við útreikning á sveigjanleikastöðu starfskraftsins

## <a name="set-up-flexible-working-hours-in-flex-groups"></a>Setja upp sveigjanlegan vinnutíma í sveigjanleikaflokkum

- Veldu **Tími og viðvera** \> **Uppsetning** \> **Flokkar** \> **Sveigjanleikaflokkar** til að setja upp sveigjanleikaflokka fyrir sveigjanlegar vinnustundir.

## <a name="associate-workers-with-flex-groups"></a>Tengja starfskrafta við sveigjanleikaflokka

- Veldu **Tími og viðvera** \> **Uppsetning** \> **Starfskraftar sem sinna tímaskráningu**.

## <a name="rules-for-flex-regulations"></a>Reglur um sveigjanleikareglur

Hægt er að nota reglur fyrir sveigjanleikareglur til að skilgreina sveigjanleikamörk, eða lágmarks- og hámarksfjölda vinnustunda sem eru leyfðar á sveigjanlegum reikningi starfskrafts. Sveigjanleikamörkin eru sett upp í sveigjanleikaflokknum. Þegar farið er yfir sveigjanleikamörkin er hægt að leiðrétta sveigjanleikastöðu og laun starfskrafts.

Ef farið er undir leyfilegt sveigjanleikalágmark starfskrafts (það er ef fjöldi vinnustunda á sveigjanlegum reikningi er undir tilgreindu lágmarki) er hægt að nota þessar aðferðir til að leiðrétta sveigjanleikastöðu starfskrafts með því að búa til sveigjanleikareglu:

- Hægt er að leiðrétta sveigjanlegan reikning starfskrafts að tilgreindu leyfilegu lágmarki, en án þess að draga af launum starfskrafts sem nemur þeim fjölda klukkustunda sem sveigjanlegi reikningurinn er undir leyfilegu lágmarki.
- Hægt er að draga af launum starfskrafts þann fjölda klukkustunda sem sveigjanlegi reikningurinn er undir leyfilegu lágmarki. Þessi frádráttur er gerður með því að búa til launaliði fyrir ákveðna launagerð sem hefur neikvæða eða jákvæða launaeiningu.

Ef farið er yfir leyfilegt sveigjanleikahámark starfsmanns er hægt að nota þessar aðferðir til að leiðrétta sveigjanleikastöðu starfskrafts með því að búa til sveigjanleikareglu:

- Hægt er að leiðrétta sveigjanlegan reikning starfskrafts að tilgreindu leyfilegu hámarki, en án þess að bæta við laun starfskrafts sem nemur þeim fjölda klukkustunda sem starfskrafturinn vann fram yfir leyfilegt hámark.
- Fjölda klukkustunda sem starfskrafturinn vann fram yfir leyfilegt hámark er hægt að umbreyta í laun. Þessi umbreyting er gerð með því að búa til launalið fyrir tiltekna launagerð.

Hægt er að stilla sveigjanleikastöðu á eftirfarandi tímum:

- Þegar greiðsluskrá sem byggist á launagögnum er flutt út með því að nota verkið **Flutningur launa**. Launagögnin eru mynduð þegar skráningar starfskrafts eru fluttar frá síðunni **Samþykkja**.
- Þegar unnið er úr verkinu **Leiðrétta sveigjanleikastöðu**.

> [!NOTE]
> Sveigjanleikareglur eiga sér stað ekki við daglegt samþykki og flutning á skráningum starfskrafts á síðunni **Samþykkja**.

## <a name="principle-for-calculating-a-workers-flex-balance"></a>Meginregla við útreikning á sveigjanleikastöðu starfskrafts

Meginreglan við útreikning á þeim vinnustundum sem nemur leiðréttingunni á sveigjanleikastöðu starfskrafts er sett upp í sveigjanleikaflokknum. Veldu **Tími og viðvera** \> **Uppsetning** \> **Flokkar** \> **Sveigjanleikaflokkar**. 

Hægt er að nota eftirfarandi tvær meginreglur:

- **Tími** - Sveigjanlegar vinnustundir starfskrafts eru aðeins reiknaðar út frá skráðum vinnutíma starfskrafts fyrir daginn. Þegar dagleg skráning starfskrafts er reiknuð, er fjöldi Sveigjanlegra+ og Sveigjanlegra- vinnustunda reiknaður út frá svæðum Sveigjanlegs+ og Sveigjanlegs- sem eru skilgreind í tímaforstillingu starfskrafts.
- **Launagerð** - Sveigjanlegar vinnustundir starfskrafts eru reiknaðar út frá tekjum af launagerðinni fyrir Sveigjanlegan+ og Sveigjanlegan- sem er skilgreind í launasamningi starfskrafts. Launasamningurinn er tengdur við tímaskráningar starfskrafts. Þú gætir viljað nota launagerðir til að stjórna sveigjanlegum reikningum ef þú vilt til dæmis stækka sveigjanlegan reikning starfskrafts með ákveðnum stuðli á einu eða fleiri sveigjanlegum svæðum.

### <a name="scenario-1-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-minimum-is-exceeded"></a>Atburður 1: Leiðrétting á launum og sveigjanlegum reikningi starfskrafts vegna þess að farið er undir leyfilegt lágmark sveigjanleika

Starfskarftur sem getur unnið sveigjanlegan vinnutíma hefur neikvæðan sveigjanlegan reikning.

- **Sveigjanlegur reikningur:** -4

Starfskrafturinn tengist sveigjanleikaflokki sem hefur eftirfarandi grunnstillingu:

- **Lágmark sveigjanleika:** -0,5
- **Lágmarks launagerð:** 1302
- **Stuðull launagerðar:** -1,00

Líkt og munurinn á milli sveigjanlegs reiknings starfskrafts og leyfilegs sveigjanlegs lágmarks bendir til, hefur starfskrafts farið undir leyfilegt lágmark því sem nemur 3,5 klst.

Þegar umsjónarmaður launa flytur launagögn starfskrafts með því að keyra verkið **Flutningur launa** eða **Leiðrétting sveigjanleika** eru eftirfarandi leiðréttingar gerðar:

- Sveigjanlegur reikningur starfskrafts er leiðréttur um 3,5 klst. Þess vegna verður sveigjanleikastaðan -4,0 klst. leiðrétt í leyfilegt sveigjanleikalágmark upp á 0,5 klst.
- Launaliður fyrir launagerðina 1302 er búin til. Þessi launaliður hefur launaeiningu sem nemur -3,5 klst. sem verða dregnar frá launum starfskrafts. Í þessu tilfelli er launaeiningin neikvæð tala vegna þess að jákvæða leiðréttingin sem nemur 3,5 klst. er margfölduð með neikvæða launaliðsstuðlinum -1,0 sem er skilgreindur í sveigjanleikaflokknum. Þessi launaliður verður hluti af launaskránni sem er mynduð af verkinu **Flutningur launa**.

### <a name="scenario-2-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-maximum-is-exceeded"></a>Atburður 2: Leiðrétting á launum og sveigjanlegum reikningi starfskrafts vegna þess að farið er yfir leyfilegt hámark sveigjanleika

Starfskraftur sem getur unnið sveigjanlegan vinnutíma hefur jákvæðan sveigjanlegan reikning.

- **Sveigjanlegur reikningur:** 6

Starfskrafturinn tengist sveigjanleikaflokki sem hefur eftirfarandi grunnstillingu:

- **Hámark sveigjanleika:** 2,0
- **Lágmarks launagerð:** 1302
- **Stuðull launagerðar:** -1,0

Líkt og munurinn á milli sveigjanlegs reiknings starfskrafts og leyfilegs sveigjanlegs hámarks bendir til, hefur starfskraftur farið yfir leyfilegt hámark um sem nemur 4,0 klst.

Þegar umsjónarmaður launa flytur launagögn starfskrafts með því að keyra verkið **Flutningur launa** eða **Leiðrétting sveigjanleika** eru eftirfarandi leiðréttingar gerðar:

- Sveigjanlegur reikningur starfskrafts er leiðréttur um -4,0 klst. Þess vegna verður sveigjanleikastaðan 6,0 klst. leiðrétt í leyfilegt sveigjanleikahámark upp á 2,0 klst.
- Launaliður fyrir launagerðina 1302 er búin til. Þessi launaliður hefur launaeiningu sem nemur 4,0 klst. sem verður bætt við laun starfskrafts. Í þessu tilfelli er launaeiningin jákvæð tala vegna þess að jákvæða leiðréttingin sem nemur 4,0 klst. er margfölduð með neikvæða launaliðsstuðlinum -1,0 sem er skilgreindur í sveigjanleikaflokknum. Þessi launaliður verður hluti af launaskránni sem er mynduð af verkinu **Flutningur launa**.

### <a name="scenario-3-managing-a-workers-flex-balance-based-on-pay-types"></a>Atburður 3: Stjórna sveigjanleikastöðu starfskrafts á grundvelli launagerðar

Eins og áður var lýst er hægt að stjórna sveigjanlegum reikningum, annaðhvort með tímanum sem skráður er í Sveigjanlegum+ og Sveigjanlegum- svæðunum sem eru skilgreind í tímaforstillingu starfskrafts eða í launagerðunum sem eru skilgreindar í launasamningi starfskrafts. Ef launagerðir eru notaðar sveigjanlegur reikningur starfskrafts leiðréttur af launaliðunum sem eru myndaðir þegar skráningar starfskrafts eru fluttar frá síðunni **Samþykkja**. Þú gætir viljað nota launagerðir til að stjórna sveigjanlegum reikningum ef þú vilt til dæmis stækka sveigjanlegan reikning starfskrafts með ákveðnum stuðli á einu eða fleiri sveigjanlegum svæðum.

Þessi atburður notar eftirfarandi forstillingu sveigjanlegs sem táknar vinnudag.

| Gerð forstillingar  | Ræsa    | Ljúk.      |
|---------------|----------|----------|
| Sveigjanlegt+         | 12:00 | 08:00 |
| Innstimplun      | 08:00 | 08:00 |
| Sveigjanlegt-         | 08:00 | 09:00 |
| Staðaltími | 09:00 | 11:30 |
| Greitt vinnuhlé    | 11:30 | 12:00 |
| Sveigjanlegt-         | 12:00 | 04:00 |
| Stimpla út     | 04:00 | 04:00 |
| Sveigjanlegt+         | 04:00 | 12:00 |

Í þessu tilfelli viltu geta stjórnað sveigjanleikastöðu starfskrafts á grundvelli launagerðar. Þess vegna þarf að stilla valkostinn **Byggt á launagerð** á **Já** í sveigjanleikaflokki starfskrafts.

Til að taka tillit til sveigjanlegra vinnustunda verður einnig að skilgreina nýja launagerð. Fyrir þennan atburð er launagerðin kölluð **FlexCnt**.

| Launagerð | lýsing  |
|----------|--------------|
| FlexCnt  | Sveigjanlegur teljari |

Næst skaltu fylgja þessum skrefum til að setja upp launagerð og bæta línum af nýju gerðinni við launaforstillingu.

1. Veldu **Tími og viðvera** \> **Uppsetning** \> **Flokkar** \> **Sveigjanleikaflokkar** og veldu svo **Nýr**.
2. Bæði í reitnum **Sveigjanlegur+** og reitnum **Sveigjanlegur-** skal tilgreina nýju launagerðina, **FlexCnt**.
3. Veldu **Tími og viðveru** \> **Uppsetning** \> **Launasamningar** og veldu síðan **Samningslínur**.
4. Fyrir **Mánudagur**, fyrir forstillingargerðina **Sveigjanlegur+** skal bæta við eftirfarandi þremur línum.

    | Launagerð | lýsing  | Frá klukkan | Til klukkan  | Lágmark | Hámark | Stuðull |
    |----------|--------------|-----------|----------|---------|---------|--------|
    | FlexCnt  | Sveigjanlegur teljari | 12:00  | 06:00 | 00:00   | 00:00   | 1,00   |
    | FlexCnt  | Sveigjanlegur teljari | 06:00  | 12:00 | 00:00   | 02.00   | 1.50   |
    | FlexCnt  | Sveigjanlegur teljari | 06:00  | 12:00 | 02.00   | 06.00   | 2.00   |

    > [!NOTE]
    > Hver lína er notuð fyrir annað tímabil og hefur annan stuðul. Sveigjanlegar vinnustundir sem starfskrafturinn vinnur á tímabili eru margfaldaður með stuðlinum fyrir þá línu. Til dæmis eru klukkustundirnar sem eru unnar frá kl. 18:00 til 20:00, margfaldaðar með 1,50. Stuðullinn er tilgreindur í reitnum **Stuðull** í flipanum **Almennt** á síðunni **Launasamningslínur**.

Starfskrafturinn færir inn eftirfarandi skráningar fyrir daginn.

| Gerð færslubókarskráningar | Ræsa    | Ljúk.      |
|---------------------------|----------|----------|
| Innstimplun                  | 07:00 | 07:00 |
| Framleiðsluverk            | 07:00 | 09:00 |
| Stimpla út                 | 09:00 | 09:00 |

Fjárhæðin sem þarf að greiða er reiknuð á síðunni **Samþykkja** á grundvelli skráningar starfskrafts. Eftir að skráningin er reiknað er hægt að skoða niðurstöðurnar í flipanum **Vinnustundir**. Fyrir þennan atburð liggur áhuginn á eftirfarandi reitum.

| Sveigjanlegur + | Sveigjanlegur - | Tími  | Launatími |
|--------|--------|-------|----------|
| 6,00   | 0,00   | 13.50 | 08.00    |

Fjöldi vinnustunda Sveigjanlegs+ er sex klukkustundir og útreikningurinn byggist á sveigjanlegu svæðunum í tímaforstillingunni. Þessi fjöldi samanstendur af einni klukkustund af Sveigjanlegum+ tíma frá kl. 07:00 til 08:00 og fimm klukkustundum af Sveigjanlegum+ tíma frá kl. 16:00 til 21:00.

Þegar skráningar eru fluttar tekur þú eftir að fjöldi Sveigjanlegs+ tíma hefur breyst frá 6,0 klst. í 8,0 klst.

| Sveigjanlegur + | Sveigjanlegur - | Tími  | Launatími |
|--------|--------|-------|----------|
| 8,00   | 0,00   | 13.50 | 08.00    |

Þessi breyting gerist eftir flutninginn vegna þess að sveigjanlegar vinnustundir hafa verið reiknaðar út á grundvelli launagerðar í stað tíma. Eftirfarandi tafla sýnir hvernig átta klukkustundir eru reiknaðar.

| Frá     | Að       | Tími | Stuðull    | Sveigjanlegur reikningur |
|----------|----------|------|-----------|--------------|
| 07:00 | 08:00 | 1    | 1         | 1            |
| 04:00 | 06:00 | 2    | 1         | 2            |
| 06:00 | 08:00 | 2    | 1.5       | 3            |
| 08:00 | 09:00 | 1    | 2         | 2            |
|          |          |      | **Samtala** | **8**        |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]