---
title: Setja upp viðbót rafrænnar reikningsfærslu
description: Í þessu efnisatriði er útskýrt hvernig setja á upp viðbót rafrænnar reikningsfærslu í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 0561a3307f8b990c06dd25c9fc3fd7097254061f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988470"
---
# <a name="set-up-the-electronic-invoicing-add-on"></a>Setja upp viðbót rafrænnar reikningsfærslu

[!include [banner](../includes/banner.md)]


Uppsetning á eiginleika rafrænnar reikningsfærsluviðbótar er ferlið við að stofna nauðsynlega skilgreiningu í gegnum umhverfi Regulatory Configuration Services (RCS) og útgáfu þeirrar skilgreiningar á þjóni rafrænnar reikningsfærsluviðbótar. Uppsetningin leyfir þér að búa til stillanlegar reglur sem gerir viðbót rafrænnar reikningsfærslu kleift að nota örugga samskiptareglu á internetinu til að flytja og skiptast á gögnum við einingu þriðja aðila í gegnum vefþjónustur.

Stillanleikinn reiðir sig á skilgreiningu rafræns skýrslugerðarsniðs sem leið til að búa til efni sem er sent og móttekið í gegnum stafrænar skrár. Hann reiðir sig einnig á útsetningu samskiptaaðgerða til að senda beiðnir til og taka á móti svörum frá vefþjónustum þriðja aðila án þess að þú þurfir að skrifa kóða.

## <a name="overview"></a>Yfirlit

„Eiginleiki rafrænnar reikningsfærsluviðbótar“ er almennt heiti fyrir tilfangið sem er skilgreint og gefið út til að nota þjón rafrænnar reikningsfærsluviðbótar. Uppsetning eiginleikans sameinar meðal annars notkun á sniðum rafrænna skýrslugerðarskilgreininga til að búa til stillanlegar útflutnings- og innflutningsskrá, og notkun á aðgerðum og aðgerðarflæði til að virkja stofnun á stillanlegum reglum til að senda beiðnir, flytja inn svör og þátta innihald svara.

Eftirfarandi mynd sýnir helstu þættina í eiginleika rafrænnar reikningsfærsluviðbótar.

![Yfirlit yfir eiginleika rafrænnar reikningsfærsluviðbótar](media/e-Invoicing-services-feature-setup-Overview-e-Invoicing-feature.png)

Vegna frávika í reikningssniðum og aðgerðarflæði, gæti uppsetning eiginleikans verið breytileg eftir löndum eða svæðum, eða vegna viðskiptakrafa.

## <a name="set-up-the-electronic-invoicing-add-on-feature"></a>Setja upp eiginleika rafrænnar reikningsfærsluviðbótar

Ljúka þarf uppsetningarferlinu í RCS-umhverfinu. Fylgið eftirfarandi skrefum til að stofna nýjan eiginleika rafrænnar reikningsfærsluviðbótar.

1. Skráðu þig inn í RCS-umhverfið þitt.
2. Á vinnusvæðinu **Altækir eiginleikar**, í hlutanum **Eiginleikar**, skal velja reitinn **Viðbót rafrænnar reikningsfærslu**.
3. Á síðunni **Eiginleikar rafrænnar reikningsfærsluviðbótar** skal velja **Flytja inn** til að flytja inn skilgreiningu á gagnalíkani rafrænnar skýrslugerðar úr altæku geymslunni.
4. Veljið **Bæta við** til að stofna eiginleika rafrænnar reikningsfærsluviðbótar. Annaðhvort er hægt að stofna eiginleikann frá grunni eða búa hann til út frá fyrirliggjandi eiginleika rafrænnar reikningsfærsluviðbótar.

    ![Eiginleika rafrænnar reikningsfærsluviðbótar bætt við](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature.png)

> [!NOTE]
> Þegar nýr eiginleiki rafrænnar reikningsfærsluviðbótar er stofnaður fylgir honum nýtt útgáfunúmer og sjálfgefin staða hans er stillt á **Drög**.

### <a name="configurations"></a>Afbrigði

Skilgreiningar geyma skilgreiningar rafræns skýrslugerðarsniðs sem eru nauðsynleg til að umbreyta og búa til skrár sem verður skipst á í samskiptum við vefþjónustur þriðja aðila. Eiginleiki rafrænnar reikningsfærsluviðbótar getur haft eins margar skilgreiningar á skráarsniði rafrænnar skýrslugerðar og þörf er á, sem byggir á tæknilýsingu samþættingar sem vefþjónustan býður upp á.

Fylgið þessum skrefum til að bæta sniðum rafrænnar skýrslugerðar við eiginleika rafrænnar reikningsfærsluviðbótar.

1. Á síðunni **Eiginleikar rafrænnar reikningsfærsluviðbótar**, í flipanum **Skilgreiningar**, skal velja **Bæta við** til að bæta við skilgreiningum á skráarsniði rafrænnar skýrslugerðar fyrir eiginleika rafrænnar reikningsfærsluviðbótar.

    ![Skilgreiningum á eiginleika rafrænnar reikningsfærsluviðbótar bætt við](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Þegar eiginleiki rafrænnar reikningsfærsluviðbótar er búinn til frá grunni, þarf að bæta handvirkt við öllum skilgreiningum á skráarsniði rafrænnar skýrslugerðar. Þegar eiginleiki rafrænnar reikningsfærsluviðbótar er búinn til út frá fyrirliggjandi eiginleika, eru skilgreiningar á skráarsniði rafrænnar skýrslugerðar sjálfkrafa búnar til vegna þess að þær erfast frá upprunalegum eiginleika rafrænnar reikningsfærsluviðbótar.

2. Veljið **Breyta** til að opna síðuna **Sniðshönnuður** þar sem hægt er að breyta skilgreiningu á skráarsniði rafrænnar skýrslugerðar.

    ![Skilgreiningum á eiginleika rafrænnar reikningsfærsluviðbótar breytt](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Þegar sniðinu er breytt breytist staða skilgreiningarinnar í **Drög**.

3. Notið síðuna **Sniðshönnuður** til að breyta skilgreiningu skráarsniðsins. Frekari upplýsingar er að finna í [Stofna skilgreiningar rafræns skjals](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Síða sniðshönnuðar](media/e-Invoicing-services-feature-setup-ER-Format-designer.png)

### <a name="feature-setups"></a>Uppsetning eiginleika

Uppsetningar eiginleika halda utan um reglurnar um samskipti og öryggi gagnvart vefþjónustu þriðja aðila. Eiginleiki rafrænnar reikningsfærsluviðbótar getur haft eins margar uppsetningar á eiginleika og þörf er á, sem byggir á viðskiptareglunni sem á að uppfylla.

Fylgið þessum skrefum til að bæta uppsetningum eiginleika við eiginleika rafrænnar reikningsfærsluviðbótar.

1. Á síðunni **Eiginleikar rafrænnar reikningsfærsluviðbótar**, í flipanum **Uppsetningar**, skal velja **Bæta við** til að bæta uppsetningum eiginleika við eiginleika rafrænnar reikningsfærsluviðbótar.

    ![Uppsetningum á eiginleika rafrænnar reikningsfærsluviðbótar bætt við](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Setups.png)

    > [!NOTE]
    > Þegar eiginleiki rafrænnar reikningsfærsluviðbótar er búinn til frá grunni, þarf að bæta handvirkt við öllum uppsetningum eiginleika sem þörf er á. Þegar eiginleiki rafrænnar reikningsfærsluviðbótar er búinn til út frá fyrirliggjandi eiginleika, eru allar uppsetningar eiginleika sjálfkrafa búnar til vegna þess að þær erfast frá upprunalegum eiginleika rafrænnar reikningsfærsluviðbótar.

2. Veljið **Breyta** til að breyta uppsetningu eiginleikaútgáfu.

    ![Uppsetningum á eiginleika rafrænnar reikningsfærsluviðbótar breytt](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Setups.png)

3. Notið síðuna **Uppsetning eiginleikaútgáfu** til að skilgreina aðgerðir, gildissviðsreglur og breytur.

    ![Aðgerðir, gildissviðsreglur og breytur](media/e-Invoicing-services-feature-setup-View-Actions-Applicability-Rules-Variables.png)

### <a name="actions"></a>Aðgerðir

Aðgerðir eru fyrirframskilgreindur listi yfir aðgerðir sem eru keyrðar í ákveðinni röð. Þessi listi stendur fyrir sundurliðun á nauðsynlegum skrefum fyrir heildarútfærslu á eiginleika rafrænnar reikningsfærsluviðbótar. Aðgerðirnar geta haldið utan um, í sama eiginleika rafrænnar reikningsfærsluviðbótar, samskipti í báðar áttir: senda beiðni um áfangastað og taka á móti svari og þátta innihald þess.

Hver aðgerð inniheldur fyrirframskilgreindan lista yfir færibreytur sem eru nauðsynlegar til að aðgerðin nái settu marki. Einnig er valfrjálst að útvega fleiri færibreytur.

#### <a name="actions-fasttab"></a>Flýtiflipi aðgerða

Á síðunni **Uppsetning eiginleikaútgáfa**, í flipanum **Aðgerðir**, í flýtiflipanum **Aðgerðir**, skal fylgja öðru hvoru eða báðum þessum skrefum til að stjórna aðgerðum:

- Veljið **Ný** eða **Eyða** til að bæta við nýjum aðgerðum eða eyða fyrirliggjandi aðgerðum.
- Veljið **Upp** eða **Niður** til að færa valdar aðgerðir upp eða niður í hnitanetinu og breyta þannig röðinni sem þær eru keyrðar í. Aðgerðir eru keyrðar í þeirri röð sem þær birtast í hnitanetinu, ofan frá og niður.

![Aðgerðum stjórnað](media/e-Invoicing-services-feature-setup-Manage-Actions.png)

Eftirfarandi tafla lýsir svæðunum sem eru tiltæk í flipanum **Aðgerðir**.

| Svæði        | lýsing |
|--------------|-------------|
| Aðgerð       | Til eru átta fyrirframskilgreindar aðgerðir:<ul><li><strong>Skrifa undir skjal</strong></li><li><strong>FileStoreActionName</strong></li><li><strong>Breyta skjali</strong></li><li><strong>Vinna úr svari</strong></li><li><strong>Hringja í REST-vefþjónustu</strong></li><li><strong>Hringja í PAC-þjónustu í Mexíkó</strong></li><li><strong>Hringja í SEFAZ-þjónustu í Brasilíu</strong></li><li><strong>Hringja í SDI-þjónustu á Ítalíu</strong></li></ul> |
| Heiti aðgerðar  | Heiti aðgerðar og keyrsluröð hennar. |
| lýsing  | Færið inn lýsingu á aðgerðinni. |
| Gera kleift að reyna aftur | Valinn gátreitur gefur til kynna að hægt er að reyna aðgerðina aftur ef fyrri tilraun mistókst. |
| Reyna aðgerð aftur | Ef reynt er aftur, þá aðgerðin sem endurtekningin byrjar á. Endurtekningin endar síðan á núverandi aðgerð (innifalin endurtekning). Fyrir aðgerðir sem eru með þær, tilgreina færibreyturnar **Lágmarks biðtími** og **Hámarks biðtími** lágmarks- og hámarksfjölda endurtekinna tilrauna. |

#### <a name="parameters-fasttab"></a>Flýtiflipi færibreyta

Flýtiflipinn **Færibreytur** sýnir færibreyturnar fyrir aðgerðina sem er valin í flýtiflipanum **Aðgerðir**.

![Flýtiflipi færibreyta](media/e-Invoicing-services-feature-setup-View-Actions-Parameters.png)

Eftirfarandi tafla lýsir svæðunum sem eru tiltæk í flipanum **Færibreytur**.

| Svæði       | lýsing |
|-------------|-------------|
| Nafn        | Fyrirframskilgreindur listi yfir færibreytur. Frekari upplýsingar er að finna í hlutanum [Listi yfir færibreytur eftir aðgerð](#list-of-parameters-by-action). |
| lýsing | Lýsing á færibreytunni. |
| Virði       | Gildi færibreytunnar. |

#### <a name="list-of-parameters-by-action"></a>Listi yfir færibreytur eftir aðgerð

Tiltækar færibreytur eru mismunandi eftir aðgerðinni sem er valin í flýtiflipanum **Aðgerðir**.

###### <a name="action-sign-document"></a>Aðgerð: Skrifa undir skjal

| Færibreyta                             | lýsing |
|---------------------------------------|-------------|
| Ílagsskrá                            | Inntaksskrá XML-skjals sem verður að vera undirritað með rafrænni undirskrift. |
| Heiti vottorðs                      | Heiti vottorðs í geymslu. |
| Gerð undirskriftar                        | Gerð undirskriftar sem á að nota. |
| Heiti undirskriftaraðferðar                 | Heiti undirskriftaraðferðar sem er notuð til að mynda rafræna undirskrift. |
| Heiti útdráttaraðferðar                    | Útdráttaraðferðin sem er notuð til að mynda útdráttarstreng í rafrænni undirskrift. |
| Heiti stöðlunaraðferðar          | Stöðlunaraðferðin sem er notuð til að reikna tætigildi undirskriftar. |
| Heiti tilvísunareigindar              | Heiti eigindar sem gefur til kynna hvar eigi að setja tilvísunarkenni inn í undirskriftareininguna. |
| Heiti einingar sem á að undirrita               | Heiti XML-einingarinnar í skjalinu sem verður að undirrita með rafrænni undirskrift. Ef engin eining er tilgreind er rót skjalsins undirrituð. |
| Heiti einingar til að setja inn undirskrift   | Heiti XML-einingarinnar þar sem á að setja inn myndaða stafræna undirskrift. Ef engin eining er tilgreind er undirskriftin sett inn í rót skjalsins. |
| XLST-skrá með útdráttarbreytingu       | XSLT-skráin sem inniheldur reglur um útdráttarbreytingu til að mynda útdráttarstrenginn fyrir rafræna undirskrift. |
| Slóð til að setja inn útdráttarstreng          | Slóðin, á **\<elementName\>.\<Attribute.Path\>** sniði, fyrir staðsetninguna þar sem setja verður inn myndaðan útdráttarstreng. |
| Staðsetning vottorðsnúmers           | Heiti einingar og eigindar þar sem setja á inn vottorðsnúmerið. |
| Staðsetning vottorðsgagna          | Heiti einingar og eigindar þar sem setja verður inn vottorðsgögn (base64). |
| Vottorðsnúmer er á ASCII-sniði | Gildi sem tilgreinir hvort númer vottorðsins er kóðað á ASCII-sniði. |

###### <a name="action-filestoreactionname"></a>Aðgerð: FileStoreActionName

| Færibreyta  | lýsing |
|------------|-------------|
| Ílagsskrá | Inntaksskráin sem á að geyma. |

###### <a name="action-transform-document"></a>Aðgerð: Breyta skjali

| Færibreyta                       | lýsing |
|---------------------------------|-------------|
| Ílagsskrá                      | Upprunaskráin sem veitir gögnin sem þarf að keyra á aðgerðina. |
| Stefna                       | Gildi sem segir til um hvort nota eigi innflutningssnið eða útflutningssnið. |
| Skilgreiningarkenni                | Sniðið sem á að keyra. |
| Útgáfa skilgreiningar           | Ef engin útgáfa skilgreiningar er tilgreind verður nýjasta útgáfan notuð. |
| Samþættingarstaður skilgreiningar | Upprunaskráin sem veitir gögn um tilkynntan keyrslutíma. |

###### <a name="action-process-response"></a>Aðgerð: Vinna úr svari

| Færibreyta                    | lýsing |
|------------------------------|-------------|
| Ílagsskrá                   | Svarið sem á að greina. |
| Listi yfir skilgreiningar skýrslugerðar | Listi yfir skilgreiningar sem notaðar eru til að þátta svör. |

###### <a name="action-call-rest-web-service"></a>Aðgerð: Hringja í REST-vefþjónustu

| Færibreyta                   | lýsing |
|-----------------------------|-------------|
| URL vefþjónustu             | Vefslóðin sem beiðnir eru sendar á. |
| Vefbeiðni útrunnin         | Hámarkstími (í millisekúndum) til að bíða eftir svari vefþjónustu. |
| Gerð beiðniaðgerðar      | Gerð HTTP-beiðniaðgerðar (til dæmis, **SÆKJA**, **BIRTA** eða **EYÐA**). |
| Heiti vottorðs           | Heiti vottorðanna. |
| Kóðun á meginmáli svars      | Væntanleg kóðun á meginmáli HTTP-svars þannig að hægt sé að kóða það á réttan hátt. |
| Efnisgerð HTTP-beiðni   | Innsláttur í haus efnisgerðar HTTP-beiðni. |
| Efni í meginmáli HTTP-beiðni   | Meginmál HTTP-beiðni. (Meginmálið má vera autt.) |
| Fyrirspurnargildi HTTP-færibreyta | Fyrirspurnargildi færibreytu sem eru notuð til að fylla út vefslóðina með færibreytum. |
| Biðja um leið               | Slóð leiðar fyrir HTTP-beiðnina. Færibreytur er hægt að skrifa í táknuninni **\{paramName\}**. Hér er dæmi: **"api/{id}/submit"**. |
| Listi yfir færibreytu leiðar        | Færibreytur leiða, í lyklagildistáknuninni, sem eru notaðar til að setja breytur inn í leiðina. |
| Sérstilltir HTTP-hausar         | Sérstilltir HTTP-hausar til að setja inn í beiðnina. |
| Kökur HTTP-beiðni        | Listi yfir kökur, í lykilgildistáknuninni, til að setja inn í hausabeiðni HTTP-kaka. |
| Öryggissamskiptareglur           | Öryggissamskiptareglur sem nota á fyrir HTTP-beiðnir til að eiga samskipti við þjóninn. (Transport Layer Security \[TLS\] 1.2 er sjálfkrafa notað.) |

###### <a name="action-call-mexican-pac-service"></a>Aðgerð: Hringja í PAC-þjónustu í Mexíkó

| Færibreyta                | lýsing |
|--------------------------|-------------|
| Ílagsskrá               | Skráin sem inniheldur XML-gögn sem verða send til vefþjónustunnar sem innsláttarfæribreyta aðferðar. |
| URL-vistfang              | Vistfang vefþjónustu (endastöð). |
| Heiti vefaðferðar (aðgerðar) | Heiti vefaðferðarinnar (aðgerðarinnar) sem verður að keyra. |
| Skírteini             | Vottorðakeðjan sem krafist er fyrir auðkenningu biðlara af vefþjónustunni. Biðlaravottorðið á að vera síðasta vottorðið í keðjunni. Rótin og millivottorðið eiga að koma fyrst. |
| Vefbeiðni útrunnin      | Hámarkstími (í millisekúndum) til að bíða eftir svari vefþjónustu. |
| Tími milli tilrauna           | Bilið á milli tilrauna til að kalla á og fá svar frá vefþjónustunni. Ef ekkert bil er tilgreint verða engar frekari tilraunir gerðar eftir að fyrsti kallið misheppnast. |
| Fjöldi tilrauna              | Hámarksfjöldi endurtekinna tilrauna til að kalla á og sækja svar frá vefþjónustunni. |
| Reyna aftur þar til               | Hámarkstími (í millisekúndum) sem endurteknar hringingar geta haldið áfram. |
| Lágmarksbiðtími         | Lágmarkshlutfall biðtíma fyrir veldisútreikning á bilum endurtekinna tilrauna. |
| Hámarksbiðtími         | Hámarkshlutfall biðtíma fyrir veldisútreikning á bilum endurtekinna tilrauna. |
| Öryggissamskiptareglur        | Öryggissamskiptareglur sem nota á fyrir HTTP-beiðnir til að eiga samskipti við þjóninn. (TLS 1.2. er sjálfkrafa notað.) |

###### <a name="action-call-brazilian-sefaz-service"></a>Aðgerð: Hringja í SEFAZ-þjónustu í Brasilíu

| Færibreyta                | lýsing |
|--------------------------|-------------|
| Ílagsskrá               | Skráin sem inniheldur XML-gögn sem verða send til vefþjónustunnar sem innsláttarfæribreyta aðferðar. |
| URL-vistfang              | Vistfang vefþjónustu (endastöð). |
| Heiti vefaðferðar (aðgerðar) | Heiti vefaðferðarinnar (aðgerðarinnar) sem verður að keyra. |
| Skírteini             | Vottorðakeðjan sem krafist er fyrir auðkenningu biðlara af vefþjónustunni. Biðlaravottorðið á að vera síðasta vottorðið í keðjunni. Rótin og millivottorðið eiga að koma fyrst. |
| Vefbeiðni útrunnin      | Hámarkstími (í millisekúndum) til að bíða eftir svari vefþjónustu. |
| Tími milli tilrauna           | Bilið á milli tilrauna til að kalla á og fá svar frá vefþjónustunni. Ef ekkert bil er tilgreint verða engar frekari tilraunir gerðar eftir að fyrsti kallið misheppnast. |
| Fjöldi tilrauna              | Hámarksfjöldi endurtekinna tilrauna til að kalla á og sækja svar frá vefþjónustunni. |
| Reyna aftur þar til               | Hámarkstími (í millisekúndum) sem endurteknar hringingar geta haldið áfram. |
| Lágmarksbiðtími         | Lágmarkshlutfall biðtíma fyrir veldisútreikning á bilum endurtekinna tilrauna. |
| Hámarksbiðtími         | Hámarkshlutfall biðtíma fyrir veldisútreikning á bilum endurtekinna tilrauna. |
| Öryggissamskiptareglur        | Öryggissamskiptareglur sem nota á fyrir HTTP-beiðnir til að eiga samskipti við þjóninn. (TLS 1.2. er sjálfkrafa notað.) |

###### <a name="action-call-italian-sdi-service"></a>Aðgerð: Hringja í SDI-þjónustu á Ítalíu

| Færibreyta                | lýsing |
|--------------------------|-------------|
| Ílagsskrá               | Skráin sem inniheldur XML-gögn sem verða send til vefþjónustunnar sem innsláttarfæribreyta aðferðar. |
| URL-vistfang              | Vistfang vefþjónustu (endastöð). |
| Heiti vefaðferðar (aðgerðar) | Heiti vefaðferðarinnar (aðgerðarinnar) sem verður að keyra. |
| Skírteini             | Vottorðakeðjan sem krafist er fyrir auðkenningu biðlara af vefþjónustunni. Biðlaravottorðið á að vera síðasta vottorðið í keðjunni. Rótin og millivottorðið eiga að koma fyrst. |
| Vefbeiðni útrunnin      | Hámarkstími (í millisekúndum) til að bíða eftir svari vefþjónustu. |
| Tími milli tilrauna           | Bilið á milli tilrauna til að kalla á og fá svar frá vefþjónustunni. Ef ekkert bil er tilgreint verða engar frekari tilraunir gerðar eftir að fyrsti kallið misheppnast. |
| Fjöldi tilrauna              | Hámarksfjöldi endurtekinna tilrauna til að kalla á og sækja svar frá vefþjónustunni. |
| Reyna aftur þar til               | Hámarkstími (í millisekúndum) sem endurteknar hringingar geta haldið áfram. |
| Lágmarksbiðtími         | Lágmarkshlutfall biðtíma fyrir veldisútreikning á bilum endurtekinna tilrauna. |
| Hámarksbiðtími         | Hámarkshlutfall biðtíma fyrir veldisútreikning á bilum endurtekinna tilrauna. |
| Öryggissamskiptareglur        | Öryggissamskiptareglur sem nota á fyrir HTTP-beiðnir til að eiga samskipti við þjóninn. (TLS 1.2. er sjálfkrafa notað.) |

### <a name="applicability-rules"></a>Gildissviðsreglur

Gildissviðsreglur gera þér kleift að búa til röklegar reglur sem ákveða samhengið sem uppsetning eiginleikans er notuð í. Þannig að samsvörunin milli samhengisins sem viðskiptaskjalið gefur upp sem er sent til úrvinnslu, ásamt skilyrði gildissviðsreglunnar, ákveða hvaða eiginleiki rafrænnar reikningsfærsluviðbótar er notaður til að vinna úr þeirri innsendingu.

#### <a name="set-up-applicability-rules"></a>Setja upp gildissviðsreglur

1. Á síðunni **Uppsetning á útgáfu eiginleika**, í flipanum **Gildissviðsreglur**, skal velja **Ný** til að bæta við gildissviðsreglu.

    ![Stjórnun gildissviðsreglna](media/e-Invoicing-services-feature-setup-Manage-Actions-Applicability-rules.png)

2. Í hnitanetinu skal velja ákvæðin sem á að flokka saman.
3. Velja **Flokka ákvæði**.

    ![Ákvæði flokkuð](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-clause.png)

    Þegar ákvæði eru flokkuð er nýjum dálki bætt við hnitanetið. Þessi dálkur tilgreinir rökvirkinn fyrir flokkuð ákvæði.

    ![Rökvirkirinn fyrir flokkuð ákvæði](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-criterias.png)

Til að afturkalla flokkun á ákvæðum skal velja flokkuð ákvæði sem á að taka úr flokkun og síðan velja **Afturkalla flokkun ákvæðis**.

![Flokkun ákvæða afturkölluð](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-UnGroup-criterias.png)

> [!NOTE]
> Þegar flokkun ákvæðis er afturkölluð skal alltaf byrja á innsta flokkunarstiginu.

Eftirfarandi tafla lýsir reitunum sem eru í boði í flipanum **Gildissviðsreglur**.

| Svæði         | lýsing |
|---------------|-------------|
| Og/eða        | Rökvirkirinn. |
| Svæði         | Svæðið sem á að nota til að útbúa regluna. |
| Gerð virkja | Gerð virkisins:<ul><li>Jafnt</li><li>Ekki jafnt</li><li>Stærra en/minna en</li><li>Stærra en eða jafnt og/minna en eða jafnt og</li><li>Innheldur</li><li>Byrja á</li></ul> |
| Virði         | Skilyrði reglunnar. |

### <a name="variables"></a>Breytur

Hægt er að búa til breytur og nota þær síðan sem innsláttargildið fyrir færibreytu tiltekinnar aðgerðar. Einnig er hægt að nota þær til að skiptast á upplýsingum, á milli þjónustu rafrænnar reikningsfærsluviðbótar og biðlarans, sem verða til vegna framkvæmdar á tiltekinni aðgerð sem hluti af innsendingarflæðinu.

#### <a name="set-up-variables"></a>Setja upp breytur

- Á síðunni **Uppsetning á útgáfu eiginleika**, í flipanum **Breytur**, skal velja **Ný** eða **Eyða** til að stjórna breytum.

    ![Að stjórna breytum](media/e-Invoicing-services-feature-setup-Manage-Variables.png)

Eftirfarandi tafla lýsir svæðunum sem eru tiltæk í flipanum **Breytur**.

| Svæði       | lýsing |
|-------------|-------------|
| Nafn        | Heiti breytunnar. |
| lýsing | Stutt lýsing á breytunni. |
| Gerð        | Gerð breytunnar:<ul><li><strong>Fasti</strong> - Efni breytunnar er fast.</li><li><strong>Frá biðlara</strong> - Efni breytunnar er fengið úr biðlara Microsoft Dynamics 365 við framkvæmd innsendingarferlisins.</li><li><strong>Til biðlara</strong> - Efni breytunnar er gert aðgengilegt fyrir innflutning af biðlara Microsoft Dynamics 365 við framkvæmd innsendingarferlisins.</li></ul> |
| Gagnagerð   | Gagnagerð breytunnar:<ul><li>Boole</li><li>Dagsetning</li><li>Númer</li><li>UUID</li><li>Strengur</li><li>Skrá</li></ul> |
| Virði       | Gildi breytunnar eða heiti aðgerðarinnar sem stillir gildi breytunnar. |

### <a name="validate-the-feature-setup"></a>Villuleita uppsetningu eiginleikans

- Á síðunni **Uppsetning á útgáfu eiginleika**, á aðgerðasvæðinu, skal velja **Villuleita** til að villuleita uppsetningu á útgáfu eiginleikans.

   ![Villuleitarhnappurinn valinn](media/e-Invoicing-services-feature-setup-Select-Validate-Button.png)

Villuleitin athugar samræmi allrar skilgreiningarinnar. Ef til dæmis tiltekin færibreyta fyrir aðgerð er áskilin en gildi hennar er autt, ber villuleitin kennsl á þetta ósamræmi og upp kemur villa.

## <a name="environments"></a>Umhverfi

Umhverfi rafrænnar reikningsfærsluviðbótar verður að tengjast eiginleika rafrænnar reikningsfærsluviðbótar og vera virkjað fyrir hann. Búa verður til og gefa út umhverfi rafrænnar reikningsfærsluviðbótar fyrirfram í gegnum skilgreiningu altækra eiginleika í RCS-reikningi fyrirtækisins.

Fylgið þessum skrefum til að virkja umhverfi rafrænnar reikningsfærsluviðbótar fyrir eiginleika rafrænnar reikningsfærsluviðbótar.

1. Á síðunni **Eiginleikar rafrænnar reikningsfærsluviðbótar**, í flipanum **Umhverfi**, skal velja **Virkja** til að bæta við umhverfi rafrænnar reikningsfærsluviðbótar.
2. Í reitinn **Gildir frá** skal færa inn dagsetninguna þegar nýja umhverfið tekur gildi.

![Umhverfi rafrænnar reikningsfærsluviðbótar virkjað](media/e-Invoicing-services-feature-setup-Select-Enable-e-Invoicing-feature-Environment.png)

## <a name="organizations"></a>Fyrirtæki

Hægt er að samnýta eiginleika rafrænnar reikningsfærsluviðbótar í mörgum fyrirtækjum.

- Á síðunni **Eiginleikar rafrænnar reikningsfærsluviðbótar**, í flipanum **Fyrirtæki**, skal velja **Samnýta með** til að bæta við fyrirtækinu sem þú vilt samnýta eiginleika rafrænnar reikningsfærsluviðbótar með.

Til að hætta að samnýta eiginleika rafrænnar reikningsfærsluviðbótar með fyrirtækinu skal velja **Stöðva samnýtingu**.

## <a name="versions"></a>Útgáfur

Útgáfur hjálpa til við að stýra stuðningstíma eiginleika rafrænnar reikningsfærsluviðbótar með því að stjórna stöðu hans. Hægt er að búa til nýja útgáfu af fyrirliggjandi eiginleika rafrænnar reikningsfærsluviðbótar, eða þegar öllum skilgreiningum fyrir eiginleika rafrænnar reikningsfærsluviðbótar er lokið, er hægt að breyta stöðu eiginleikans í **Ljúka** og síðan í **Gefa út**.

### <a name="create-a-new-version-of-an-existing-electronic-invoicing-add-on-feature"></a>Búa til nýja útgáfu af fyrirliggjandi eiginleika rafrænnar reikningsfærsluviðbótar

1. Á síðunni **Eiginleikar rafrænnar reikningsfærsluviðbótar**, í hnitanetinu vinstra megin, skal velja eiginleika rafrænnar reikningsfærsluviðbótar.
2. Í flipanum **Útgáfur** skal velja **Ný** til að bæta við nýrri útgáfu af eiginleika rafrænnar reikningsfærsluviðbótar.

### <a name="change-the-status-of-the-electronic-invoicing-add-on-feature"></a>Breyta stöðunni á eiginleika rafrænnar reikningsfærsluviðbótar

Fylgið þessum skrefum til að stjórna stuðningstíma fyrir eiginleika rafrænnar reikningsfærsluviðbótar.

1. Á síðunni **Eiginleikar rafrænnar reikningsfærsluviðbótar**, í hnitanetinu vinstra megin, skal velja eiginleika rafrænnar reikningsfærsluviðbótar.
2. Í flipanum **Útgáfur** skal velja **Breyta stöðu** og síðan breyta stöðunni úr **Drög** í **Ljúka**.
3. Beðið er um staðfestingu á að ætlunin sé að ljúka eiginleika rafrænnar reikningsfærsluviðbótar og öllum þáttum hans. Veljið **Já** til að staðfesta aðgerðina eða **Nei** til að hætta við hana.

    > [!NOTE]
    > Þegar valið er **Já** er staðan á útgáfum skilgreiningar, sem eru þættir í eiginleika rafrænnar reikningsfærsluviðbótar, sjálfkrafa breytt úr **Drög** í **Lokið**.

4. Veljið **Breyta stöðu** og breytið síðan stöðunni úr **Lokið** í **Gefa út**.
5. Beðið er um staðfestingu á að ætlunin sé að gefa út eiginleika rafrænnar reikningsfærsluviðbótar og öllum þáttum hans í altæku geymslunni. Veljið **Já** til að staðfesta aðgerðina eða **Nei** til að hætta við hana.

    > [!NOTE]
    > Þegar valið er **Já** er stöðunni á útgáfum skilgreiningar sjálfkrafa breytt úr **Lokið** í **Samnýtt**.
