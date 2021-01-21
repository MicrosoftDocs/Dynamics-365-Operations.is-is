---
title: Reiðufjárstaða (forskoðun)
description: Þetta efnisatriði lýsir því hvernig eiginleikinn fyrir sjóðstreymisspá spáir fyrir um reiðufjárstöðu fyrirtækis á tilteknum tímum. Efnisatriðið lýsir einnig valkostunum sem eru í boði til að sýna spár fyrir mismunandi tímabil.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 64b8dcd43024e5c26d33bf12c5fe198711adde56
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645891"
---
# <a name="cash-position-preview"></a>Reiðufjárstaða (forskoðun)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Staða reiðufjár er vörpun reiðufjárs sem er spá fyrir komandi tíma. Það byggir á vörpun inngreiðslna viðskiptavina sem greiða útistandandi reikninga og pantanir og einnig á vörpuðum útborgunum sem eru greiddar lánardrottnum fyrir innkaupareikninga og pantanir.

Þegar kerfið spáir greiðslum viðskiptavinar notar það greiðsluspár frá eiginleikanum greiðsluspár viðskiptavinar. Án greiðsluspáa er meðaltíminn sem er nauðsynlegur til að umbreyta reikningi viðskiptavinar í greiðslu fyrir hvern viðskiptavin notaður til að reikna út dagsetningu greiðslu. Fyrir opnar pantanir viðskiptavina reiknar kerfið út reikningsdagsetninguna með því að nota meðalfjölda daga fyrir pöntunarlínur á hvern viðskiptavin sem á að reikningsfæra. Það notar síðan reikningsdagsetninguna sem inntak fyrir virkni greiðsluspár. Eiginleikinn greiðsluspá viðskiptavinar reiknar út dagsetningu greiðslu fyrir hverja pöntunarlínu. 

<*Þarf á texta að halda frá Jarek eða Dave varðandi hvernig greiðsluspá er breytt í dagsetningu*> Dagsetning greiðslu fyrir útistandandi reikninga er áætluð [*áætlað*] frá greiðsluspám með því að velja dagsetningu sem samsvarar fimmtugasta prósentuhlutfalli vaxandi dreifingarfalli sem fengið er úr líkum áætlaða rammans.

Svipuð aðferð er notuð til að spá fyrir um greiðslur til lánardrottna. Fyrir hvern lánardrottin reiknar kerfið út meðaltíma sem er nauðsynlegur til að umbreyta reikningi lánardrottins í greiðslu. Sá fjöldi daga er síðan notaður til að reikna út dagsetningu greiðslu. Í opnum pöntunum lánardrottna reiknar kerfið reikningsdagsetninguna með því að taka mið af meðalfjölda daga sem þarf til að umbreyta pöntunarlínum í reikning fyrir hvern lánardrottinn. Kerfið reiknar síðan dagsetningu greiðslu með því að nota meðaltíma til að umbreyta reikningi lánardrottins í greiðslu fyrir hvern lánardrottinn.

Efri hluti á flipanum **Staða reiðufjár** inniheldur sjóðsstöðugraf. Þetta graf sýnir sjóðsinnstreymi og -útstreymi og áhrif þess á stöðu heildargreiðslugetu. Hægt er að skoða upplýsingar í sjóðsstöðugrafinu eftir dögum, vikum, mánuðum eða ársfjórðungum. Þegar **Daglega** er valið er hægt að skoða spár fyrir næsta 21 dag. Þegar **Vikulega** er valið er hægt að skoða spár fyrir næstu 20 vikurnar. Þegar valið er **Mánaðarlega** er hægt að skoða spár fyrir næstu 12 mánuði. Þegar **Ársfjórðungslegt** er valið er hægt að skoða spár fyrir næstu 12 ársfjórðunga. Hægt er að fela myndritið ef viðbótarbil er nauðsynlegt á skjánum til að skoða efni á flipanum **Staða reiðufjár**.

Neðri hluti á flipanum **Staða reiðufjár** sýnir upplýsingar um stöðu, sjóðstreymi, áætlaðar greiðslur og bankareikning.

- Upplýsingar í **Upplýsingar um stöðu** hnitanetinu eru settar fram í þremur hlutum: lista yfir greiðslugetulykla, lista yfir skjöl sem mynda sjóðsinnstreymi og lista yfir skjöl sem mynda ráðstöfun handbærs fjárs. Hnitanetið sýnir einnig reiðufjárstöðu. Fyrir fyrsta tímabilið sem verið að skoða er staðan fyrir greiðslugetulykla opnunarstaðan. Fyrir síðari tímabil eru stöður greiðslugetulykla reiknaðar út frá viðbót sjóðsinnstreymis og frádrætti ráðstöfunar handbærs fjár frá fyrri tímabilum. Til að skoða upplýsingar um færslurnar sem mynda stöðuna skal velja tengilinn **Staða**.
- Hnitanetið **Sjóðstreymi** sýnir uppsafnað sjóðsinnstreymi, ráðstöfun handbærs fjárs á hverju tímabili og áhrif þeirra á stöðu greiðslugetulykla. Fyrir fyrsta tímabilið er staðan fyrir greiðslugetulykla opnunarstaðan. Fyrir síðari tímabil eru stöður greiðslugetulykla reiknaðar út frá viðbót sjóðsinnstreymis og frádrætti ráðstöfunar handbærs fjár frá fyrri tímabilum.
- Hnitanetið **Áætluð staða í banka** sýnir áætlaða ráðstöfun handbærs fjár og áhrif þess á greiðslugetulykla.
- **Bankareikningur** hnitanetið sýnir áhrif áætlaðs sjóðsinnstreymis og ráðstöfun handbærs fjár á stöðu í banka.

Til að vista og breyta sjóðsstöðu skal búa til skyndimynd. Frekari upplýsingar um hvernig á að vinna með skyndimyndir eru í [Yfirlit yfir skyndimyndir](payment-snapshots.md).

#### <a name="privacy-notice"></a>Tilkynning um persónuvernd
Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.