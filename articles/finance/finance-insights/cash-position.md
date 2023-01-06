---
title: Staða reiðufjár
description: Þessi grein lýsir því hvernig eiginleikinn fyrir sjóðstreymisspá spáir fyrir um reiðufjárstöðu fyrirtækis á tilteknum tímum. Efnisatriðið lýsir einnig valkostunum sem eru í boði til að sýna spár fyrir mismunandi tímabil.
author: ShivamPandey-msft
ms.date: 12/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 7581142348d91b3a37cc75cf801e7bfc098cd604
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870250"
---
# <a name="cash-position"></a>Staða reiðufjár

[!include [banner](../includes/banner.md)]

Staða reiðufjár er vörpun reiðufjárs sem er spá fyrir komandi tíma. Það byggir á vörpun inngreiðslna viðskiptavina sem greiða útistandandi reikninga og pantanir og einnig á vörpuðum útborgunum sem eru greiddar lánardrottnum fyrir innkaupareikninga og pantanir.

Þegar kerfið spáir greiðslum viðskiptavinar notar það greiðsluspár frá eiginleikanum greiðsluspár viðskiptavinar. Án greiðsluspáa er meðaltíminn sem er nauðsynlegur til að umbreyta reikningi viðskiptavinar í greiðslu fyrir hvern viðskiptavin notaður til að reikna út dagsetningu greiðslu. Fyrir opnar pantanir viðskiptavina reiknar kerfið út reikningsdagsetninguna með því að nota meðalfjölda daga fyrir pöntunarlínur á hvern viðskiptavin sem á að reikningsfæra. Það notar síðan reikningsdagsetninguna sem inntak fyrir virkni greiðsluspár. Eiginleikinn greiðsluspá viðskiptavinar reiknar út dagsetningu greiðslu fyrir hverja pöntunarlínu. 

Dagsetning greiðslu fyrir útistandandi reikninga er áætluð út frá greiðsluspám með því að velja dagsetningu sem samsvarar fimmtugasta prósentuhlutfalli vaxandi dreifingarfalli sem fengið er úr líkum áætlaða rammans.

Svipuð aðferð er notuð til að spá fyrir um greiðslur til lánardrottna. Fyrir hvern lánardrottin reiknar kerfið út meðaltíma sem er nauðsynlegur til að umbreyta reikningi lánardrottins í greiðslu. Sá fjöldi daga er síðan notaður til að reikna út dagsetningu greiðslu. Í opnum pöntunum lánardrottna reiknar kerfið reikningsdagsetninguna með því að taka mið af meðalfjölda daga sem þarf til að umbreyta pöntunarlínum í reikning fyrir hvern lánardrottinn. Kerfið reiknar síðan dagsetningu greiðslu með því að nota meðaltíma til að umbreyta reikningi lánardrottins í greiðslu fyrir hvern lánardrottinn.

Efri hluti á flipanum **Staða reiðufjár** inniheldur sjóðsstöðugraf. Þetta graf sýnir sjóðsinnstreymi og -útstreymi og áhrif þess á stöðu heildargreiðslugetu. Hægt er að skoða upplýsingar í sjóðsstöðugrafinu eftir dögum, vikum, mánuðum eða ársfjórðungum. Þegar **Daglega** er valið er hægt að skoða spár fyrir næsta 21 dag. Þegar **Vikulega** er valið er hægt að skoða spár fyrir næstu 20 vikurnar. Þegar valið er **Mánaðarlega** er hægt að skoða spár fyrir næstu 12 mánuði. Þegar **Ársfjórðungslegt** er valið er hægt að skoða spár fyrir næstu 12 ársfjórðunga. Hægt er að fela myndritið ef viðbótarbil er nauðsynlegt á skjánum til að skoða efni á flipanum **Staða reiðufjár**.

Neðri hluti á flipanum **Staða reiðufjár** sýnir upplýsingar um stöðu, sjóðstreymi, áætlaðar greiðslur og bankareikning.

- Upplýsingar í **Upplýsingar um stöðu** hnitanetinu eru settar fram í þremur hlutum: lista yfir greiðslugetulykla, lista yfir skjöl sem mynda sjóðsinnstreymi og lista yfir skjöl sem mynda ráðstöfun handbærs fjárs. Hnitanetið sýnir einnig reiðufjárstöðu. Fyrir fyrsta tímabilið sem verið að skoða er staðan fyrir greiðslugetulykla opnunarstaðan. Fyrir síðari tímabil eru stöður greiðslugetulykla reiknaðar út frá viðbót sjóðsinnstreymis og frádrætti ráðstöfunar handbærs fjár frá fyrri tímabilum. Til að skoða upplýsingar um færslurnar sem mynda stöðuna skal velja tengilinn **Staða**.
- Hnitanetið **Sjóðstreymi** sýnir uppsafnað sjóðsinnstreymi, ráðstöfun handbærs fjárs á hverju tímabili og áhrif þeirra á stöðu greiðslugetulykla. Fyrir fyrsta tímabilið er staðan fyrir greiðslugetulykla opnunarstaðan. Fyrir síðari tímabil eru stöður greiðslugetulykla reiknaðar út frá viðbót sjóðsinnstreymis og frádrætti ráðstöfunar handbærs fjár frá fyrri tímabilum.
- Hnitanetið **Áætluð staða í banka** sýnir áætlaða ráðstöfun handbærs fjár og áhrif þess á greiðslugetulykla.
- **Bankareikningur** hnitanetið sýnir áhrif áætlaðs sjóðsinnstreymis og ráðstöfun handbærs fjár á stöðu í banka.

Til að vista og breyta sjóðsstöðu skal búa til skyndimynd. Frekari upplýsingar um hvernig á að vinna með skyndimyndir eru í [Yfirlit yfir skyndimyndir](payment-snapshots.md).

## <a name="details-of-the-cash-position-capability"></a>Upplýsingar um getu reiðufjárstöðu 

Eiginleiki reiðufjárstöðu inniheldur eftirfarandi virkni. 

- Eiginleiki reiðufjárstöðu sýnir sjóðsstreymi byggt á fyrirliggjandi skjölum í kerfinu og sjóðsinnstreymis- og útstreymislínum sem fluttar eru inn úr ytri kerfum.
- Auðveldar samþættingu sjóðsstreymisgagna úr ytri kerfum í Dynamics 365 Finance. Reiðufjárstöður geta einnig notað inn-útflutningsramma gagna. Þessi rammi auðveldar samþættingu við Excel OData. Einnig er hægt að sameina gögn af ólíkum uppruna til að stofna heildstæða lausn reiðufjárstöðu.
- Kynnir til sögunnar snjalla reiðufjárstöðu. Staða reiðufjár er stofnuð á grundvelli greiðsluhegðunar viðskiptavinar til að spá fyrir um hvenær fyrirtæki getur búist við því að fá greitt reiðufé á reikninga sína.
- Fyrir pantanir og reikninga viðskiptavina er gervigreindarvirkni fyrir greiðsluspá viðskiptavinar notuð til að ákvarða sögulega greiðsluhegðun viðskiptavina þegar pöntun eða reikningur er greiddur.
- Fyrir pantanir og reikninga lánardrottins notum við meðaltíma milli afhendingar og innheimtu og greiðslu reiknings á hvern lánardrottinn þegar pöntun eða reikningur lánardrottins verður greiddur sem gerir ráðstöfun handbærs fjár nákvæmara.

Þetta skapar nákvæmari yfirsýn yfir sjóðstreymi miðað við sögulega greiðsluhegðun hjá fjármálastjóranum. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
