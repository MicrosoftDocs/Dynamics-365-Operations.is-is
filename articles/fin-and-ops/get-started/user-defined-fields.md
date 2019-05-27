---
title: Stofna og vinna með sérstillt svæði
description: Þetta efnisatriði sýnir hvernig Microsoft Dynamics 365 for Finance and Operations gerir sumum notendum kleift að búa til sérsniðin svæði til að laga forritið að sínum viðskiptum.
author: jasongre
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 18402579789c17de7b46dd7a013b3b6327ea5d4f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561761"
---
# <a name="create-and-work-with-custom-fields"></a>Stofna og vinna með sérstillt svæði

[!include [banner](../includes/banner.md)]

Þótt Microsoft Microsoft Dynamics 365 for Finance and Operations veiti víðtækt úrval svæða út fyrir kassann til að stjórna fjölmörgum viðskiptaferlum, er stundum þörf fyrir fyrirtæki til að fylgjast með viðbótarupplýsingum í kerfinu. Til að mæta þessari þörf leyfir Finance and Operations þér að búa til sérsniðin svæði til að laga forritið að þínum viðskiptum, að því tilskildu að þú hafir heimild fyrir eiginleikanum.

Möguleikinn til að bæta við sérstilltum svæðum er í boði í verkvangsuppfærslu 13 og síðar.

Þetta myndband sýnir hversu auðvelt það er að bæta við sérsniðnum reit á síðu: [Bæta við sérsniðnum reitum í Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=gWSGZI9Vtnc).

## <a name="creating-custom-fields"></a>Stofna sérstillt svæði

Eftir að þú hefur auðkennt viðbótarupplýsingar sem þú vilt fylgjast með í forritinu getur þú búið til sérstillta svæðið á viðeigandi töflu og sýna nýja svæðið á síðu.

Eftirfarandi skref lýsa ferlinu við stofnun á sérstilltu svæði og koma þessu svæði fyrir á skjámynd.

1. Farðu á skjámyndina þar sem þörf er á nýja svæðinu.
2. Vegna þess að endamarkið er að sýna sérstillta svæðið á skjámynd, er inngangurinn að því að stofna sérstillt svæði í upplifun sérstillinga. Opnaðu tækastiku sérstillinga með því að velja **Valkostir** og svo **Sérstilla þessa skjámynd**.
3. Smelltu á **Setja inn** og svo **Svæði**.
4. Veldu svæðið á skjámyndinni þar sem þú vilt sýna nýja svæðið. Eftir valið birtir **Setja inn svæði** svarglugginn lista yfir núverandi svæði sem hægt er að setja inn á valda svæðið á skjámyndinni.
5. Gakktu úr skugga um að svæðið sem þú hefur áhuga á sé ekki nú þegar á listanum. Ef svo er, geturðu einfaldlega valið þetta svæði í listanum og smellt á **Setja inn**.
6. Smelltu á **Búa til nýtt svæði** hnappinn fyrir ofan listann til að hefja ferlið við stofnun á sérstilltu svæði. Þetta mun opna **Búa til nýtt svæði** svargluggann.

    Ef þú sérð ekki **Búa til nýtt svæði** hnappinn hefur þú ekki nauðsynlegar heimildir til að nota þennan eiginleika.

7. Sláðu inn eftirfarandi upplýsingar í svargluggann **Búa til nýtt svæði**.

    1. Veldu gagnasafnstöflu þar sem bæta skal við þessari töflu. Athugaðu að aðeins töflur sem styðja sérstillt svæði birtast í fellilistanum. Sjá kaflann hér að neðan til að fá tæknilegar upplýsingar um studdar töflur.
    2. Veldu gagnagerðina fyrir nýja svæðið. Tiltækar gagnagerðir eru gátreitur, dagsetning, dagsetningartími, númer, tínslulisti og texti.

        - Ef þú velur gagngerðina texti getur þú einnig tilgreint hámarkslengd textans sem hægt er að slá inn í þetta svæði.
        - Ef þú velur gagnagerðina tínslulisti getur þú einnig valið sett af gildum sem gilda fyrir svæðið.

    3. Gefðu svæðinu heiti, merkimiða og hjálpartexta. Heitið samsvarar áþreifanlegu heiti svæðis í gagnagrunninum, en merkimiðinn og hjálpartextinn eru textinn sem er notaður til að tákna þetta svæði í notandaviðmótinu.

8. Ef þetta er eina svæðið sem þú þarft að stofna fyrir þessa skjámynd, skaltu smella á **Vista**. Ef þú þarft að stofna fleiri svæði skaltu smella á **Vista og nýtt** og fara aftur í skref 7. Athugaðu að það er nú takmarkað við **20 sérstillt svæði á hverja töflu**.
9. Að fara úr **Búa til nýtt svæði** svarglugganum skilar þér aftur í **Setja inn svæði** svargluggann. Sérhvert sérstillt svæði sem var bætt við verður sjálfkrafa merkt í svæðislistanum sem á að setja inn á skjámyndina.
10. Smelltu á **Setja inn** til að setja inn merktu reitina í valda svæðið á forminu.
11. **Valfrjálst:** Virkjaðu **Færa** stillinguna frá tækjastiku sérstillinga til að færa nýju reitina á viðkomandi stað á valda svæðinu. Sjá [Sérsníða notandaupplifun](personalize-user-experience.md) til að fá frekari upplýsingar um hvernig á að nota hinar ýmsu sérstillingar til að hagræða formi til persónulegrar notkunar.

## <a name="sharing-custom-fields-with-other-users"></a>Deiling sérsniðinna reita með öðrum notendum

Eftir að þú hefur búið til sérsniðinn reit og birt hann á sniði gætirðu viljað veita þennan uppfæra síðuskjá sem inniheldur nýja reitinn fyrir aðra notendur í kerfinu. Þetta er hægt að framkvæma á tvenns konar hátt með því að nota sérstillingarvalkosti vörunnar:

- Ráðlögð leið er í gegnum kerfisstjóra, sem getur ýtt sérsniðum til allra notenda eða undirhóps notenda. Sjá [Sérsníða notandaupplifun](personalize-user-experience.md) til að fá frekari upplýsingar.
- Einnig er hægt að flytja út breytingarnar þínar (kallast *sérstillingar*), senda þær á einn eða fleiri notendur og láta hvern notanda flytja inn breytingarnar. **Stjórna** valkosturinn á tækjastiku sérstillinga gerir þér kleift að flytja út og flytja inn sérstillingar.

## <a name="managing-custom-fields"></a>Stjórna sérstilltum svæðum

Stjórnun allra sérstilltra svæði í kerfinu er hægt að gera með **Sérstillt svæði** síðunni í kerfisstjórnunareiningunni. Þessi síða leyfir notendum aðgang að mörgum möguleikum, þar á meðal:

- Skoða lista yfir öll sérstillt svæði í kerfinu.
- Takmarkaðar breytingar á núverandi sérstilltum svæðum.
- Eyða sérstilltum svæðum.
- Birta sérstillt svæði á gagnaeiningum.
- Veita þýðingar á merkimiðum sérstilltra svæða og hjálpartexta.

### <a name="viewing-all-custom-fields"></a>Skoða öll sérstillt svæði

**Sérstillt svæði** síðan veitir sýnileika til allra sérstilltu svæðanna sem hafa verið skilgreind í kerfinu. Veldu einfaldlega töfluna sem þú hefur áhuga á og síðan mun uppfærast og birta lista yfir sérstilltu svæðin sem tengjast þessari töflu. Velja sérstillt svæði úr listanum mun leyfa þér að skoða allar upplýsingar um svæðið.

### <a name="editing-custom-fields"></a>Breyti sérstilltum svæðum

Eftir að sérstillt svæði hefur verið stofnað mun aðeins vera hægt að breyta ákveðnum upplýsingum um sérstilltu svæðin á **Sérstillt svæði** síðunni.

Þú *getur* breytt þessum eiginleikum:

- Merkimiði
- Hjálpartexti
- Lengd, fyrir textasvæði

Þú *getur ekki* breytt eftirfarandi eiginleikum:

- Heiti reits
- Gagnagerð

Að auki, fyrir svæði tínslulista, er hægt að endurskipuleggja gildu gildin fyrir sérstillta svæðið og hægt er að bæta við nýjum gildum; ekki er hægt að fjarlægja núverandi gildi á tínslulistanum. Mundu að smella á **Virkja breytingar** þegar þú ert búinn að breyta svæðum fyrir tiltekna töflu þannig að breytingarnar verði vistaðar.

### <a name="exposing-custom-fields-on-data-entities"></a>Birtu sérstillt svæði í gagnaeiningum

Það kann einnig að vera mikilvægt að leyfa sérstilltum svæðum að vera sýnileg á gagnaeiningum. Gagnaeiningar eru notaðar í [Opna í Office](../../dev-itpro/office-integration/office-integration.md) eiginleikanum, sem og fyrir inn- og útflutning á gögnum framvinduna.

Fylgdu þessum skrefum til að sýna sérstillt svæði á gagnaeiningu:

1. Veldu sérstilltu svæðin **Sérstillt svæði** skjámyndinni.
2. Stækkaðu **Einingar** kaflann til að skoða hóp eininga sem eiga við.
3. Smelltu á hnappinn **Breyta**.
4. Breyttu **Virkjað** svæðinu svo það sé valið fyrir hverja einingu sem ætti að sýna þetta svæði.
5. Smelltu á **Virkja breytingar** til að vista val þitt.

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a>Leyfir sérstilltum svæðum að birtast á öðrum tungumálum

Vegna þess að sérstillt svæði gætu þurft að vera opnuð af notendum á mismunandi tungumálum, **Sérstillt svæði** reiturinn býður upp á þýðingar á merkimiðum og hjálpartextum yfir á önnur tungumál.

Eftirfarandi skref lýsa þýðingaferlinu á sérstilltum svæðum á öðrum tungumálum:

1. Veldu sérstilltu svæðin á **Serstillt svæði** síðunni.
2. Veldu **Þýðingar** hnappinn í aðgerðarglugganum. Þetta mun opna fellilista valmyndar með núverandi þýðingar fyrir þetta svæði.
3. **TUNGUMÁLA** fellilisti valmyndar sýnir tungumálin sem hefur verið þýtt á að svo stöddu.

    Ef þú vilt breyta núverandi þýðingu skaltu velja viðeigandi tungumál úr valmyndinni og breyta inntakinu fyrir merkimiðann og hjálpartextann.

    Annars skaltu smella á **Bæta við tungumáli** hnappinn, veldu viðkomandi tungumál úr valmyndinni og þýddu svo inntakið fyrir merkimiðann og hjálpartextann.

4. Smelltu á **OK** þegar þú ert búin/n.

### <a name="deleting-custom-fields"></a>Eyða sérstilltum svæðum

Í sumum sjaldgæfum tilfellum gætir þú ákveðið að ekki sé lengur þörf á sérstilltum svæðum. Þegar það á við getur kerfisstjóri valið að eyða svæðinu af **Sérstillt svæði** síðunni. Til að gera þetta skaltu tryggja að rétt svæði sé valið, smelltu á **Eyða**, smelltu á **Já** til að staðfesta eyðingu og smelltu loks á **Virkja breytingar**.

> [!NOTE]
> Ekki er hægt að afturkalla þessa aðgerð og hún mun leiða til þess að gögnin sem tengjast svæðinu verði varanlega eytt úr gagnagrunninum.

## <a name="appendix"></a>Viðauki

### <a name="who-can-create-custom-fields"></a>Hver getur búið til sérstillt svæði?

Til að vernda kerfið, getur aðeins kerfisstjóri stofnað sérstillt svæði. Hins vegar geta þessi kraftnotendur, sem fyrirtækið telur nauðsynlega, fengið réttindi til að stofna sérstillt svæði í gegnum kerfisstjóra með því að nota öryggishlutverkið **Sérstillingar keyrslutíma fyrir kraftnotendur**. Notendur án þessa öryggishlutverks geta ekki stofnað sérstillt svæði, en munu samt geta séð og átt við sérstillt svæði sem aðrir notendur í kerfinu hafa bætt við.

### <a name="what-tables-support-custom-fields"></a>Hvað töflur styðja sérstillt svæði?

Út af frammistöðu og tæknilegum ástæðum leyfa aðeins töflur sem uppfylla eftirfarandi núgildandi skilyrði sérstilltum svæðum að vera bætt við.

- Taflan verður að vera merkt sem einn af þessum hópum:

    - Hópur
    - WorksheetHeader
    - Aðal
    - Ýmislegt
    - Færibreyta
    - Tilvísun
    - TransactionHeader

- Taflan getur ekki víkkað út aðra töflu.
- Ekki er hægt að merkja töfluna sem kerfistöflu.
- Taflan getur ekki verið tímabundin tafla.
