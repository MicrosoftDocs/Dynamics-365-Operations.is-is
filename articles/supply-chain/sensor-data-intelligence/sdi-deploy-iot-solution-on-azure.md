---
title: Uppsetning IoT lausnar á Azure
description: Sensor Data Intelligence notar gögn frá skynjurum sem eru tengdir við Microsoft Azure. Í þessari grein er útskýrt hvernig á að setja internet hlutanna (IoT) lausn inn í Azure-áskriftina þína.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreAzureResourceDeploymentWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5f0f49c0f7daaacb85b75dc11b9f015b6aa4e997
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689722"
---
# <a name="deploy-an-iot-solution-on-azure"></a>Uppsetning IoT lausnar á Azure

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Sensor Data Intelligence notar gögn frá skynjurum sem eru tengdir við Microsoft Azure. Til að gera Azure kleift að ná í gögn úr skynjurum og deila þeim með Dynamics 365 Supply Chain Management þarf að setja upp IoT-lausn í Azure-áskriftinni. Á eftirfarandi skipulagsmynd er boðið upp á yfirlit yfir lausnir og íhluti hennar.

![Skipulagsmynd Sensor Data Intelligence.](media/sdi-architecture.png "Skipulagsmynd Sensor Data Intelligence")

## <a name="video-instructions"></a>Myndbandsleiðbeiningar

Eftirfarandi myndband sýnir hvernig á að [kveikja á eiginleika Sensor Data Intelligence](sdi-enable-feature.md) og setja upp nauðsynleg Azure-tilföng. Í hinum hlutanum í þessari grein er að finna sömu leiðbeiningar á textaformi.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58g3I]

## <a name="procedure"></a>Ferli

Fylgið eftirfarandi skrefum til að nota nauðsynleg tilföng á Azure.

1. Skráðu þig inn í Supply Chain Management sem stjórnandi.
1. Farðu **Kerfisstjórnun \> Uppsetning \> Sensor Data Intelligence \> Setja upp og tengja Azure-tilföng** til að opna uppsetningarleiðsögnina.
1. Á **Upphafssíðunni** skal lesa upplýsingarnar og síðan velja **Áfram**.
1. Á síðunni **Setja upp sýnishorn af IoT-lausninni í Azure** skal lesa upplýsingarnar og síðan í hlutanum **Leiðbeiningar** skal velja **Setja upp**.
1. Nýr vafraflipi er opnaður og farið er í Azure-gáttina svo hægt sé að setja inn Azure tilföngin. Ef þess er óskað skaltu skrá þig inn með því að nota skilríkin þín fyrir Azure-áskriftina.
1. Á síðunni **Sérsniðin uppsetning**, í reitnum **Áskrift**, skal velja áskriftina.
1. Undir reitnum **Tilfangaflokkur** skal velja **Stofna nýjan** til að stofna tilfangaflokk fyrir Azure-íhlutina sem á að setja upp.
1. Í fellilistanum sem birtist skal í reitinn **Heiti** færa inn heiti fyrir nýja tilfangaflokkinn (til dæmis *IoT-sýniútgáfa*). Veljið síðan **Í lagi**.
1. Stilltu eftirfarandi svæði:

    - **Tilfangaflokkur** – Veldu tilfangaflokkinn sem var stofnaður.
    - **Svæði** – Veldu svæði, helst svæðið þar sem Supply Chain Management umhverfi er notað. Hafðu í huga að mismunandi verð er á Azure svæðum. Hægt er að skoða áætlaðan kostnað fyrir svæðið þitt með því að nota [Verðreiknivél Sensor Data Intelligence](https://azure.com/e/c36c4947ebff4215b2e62590c2a24c68).
    - **Vefslóð Supply Chain Management-umhverfisins** – Færðu inn vefslóðina fyrir umhverfi Supply Chain Management.
    - **Endurnýta núverandi Azure IoT Hub** – Skildu þennan gátreit eftir auðan.

1. Veldu **Næst: Yfirfara + Stofna**.
1. Á síðunni **Sérsniðin uppsetning** skal staðfesta að sannprófunin hafi verið í lagi og síðan velja **Stofna**.
1. Síðan **Uppsetning í vinnslu** fylgist með framvindu uppsetningarinnar. Innleiðingarferlið getur tekið allt að 30 mínútur. Þegar síðan **Uppsetning er í vinnslu** tilgreinir að uppsetningu sé lokið skal velja tengilinn fyrir heiti tilfangaflokksins til að opna síðu sem sýnir listann yfir tilföng sem eru sett upp í flokknum.
1. Í tilfangalistanum skal finna færsluna þar sem reiturinn **Gerð** er stilltur á *Stjórnað auðkenni*. Í dálkinum **Heiti** skal velja nafnið til að opna upplýsingasíðu tilfangsins.
1. Afritaðu gildið í reitnum **Biðlarakenni** (til dæmis með því að velja hnappinn **Afrita á klippiborð**).
1. Farðu aftur í vafraflipann þar sem Supply Chain Management er í gangi *en ekki loka flipanum fyrir Azure-gáttina*. Leiðsagnarsíðan **Setja upp sýnishorn af IoT-lausninni í Azure** á enn að vera opin. 
1. Veljið **Næst**.
1. Á síðunni **Tengja Azure-tilföng**, í reitnum **Biðlarakenni Azure AD forrits** skal líma gildið **Biðlarakenni** sem var afritað.
1. Farðu aftur í vafraflipann þar sem Azure gáttin er opin *en ekki loka flipanum fyrir Supply Chain Management*. Upplýsingasíða tilfangsins ætti enn að vera opin.
1. Veldu hnappinn **Til baka** í vafranum til að fara aftur á listann yfir tilföng í nýja tilfangaflokknum.
1. Í tilfangalistanum skal finna færslun þar sem reiturinn **Gerð** er stilltur á *Azure-skyndiminni fyrir Redis*. Í dálkinum **Heiti** skal velja nafnið til að opna upplýsingasíðu tilfangsins.
1. Á vinstri yfirlitssvæði skal velja **Access-lyklar**.
1. Á síðunni **Aðgangslyklar** skal afrita gildið sem er sýnt fyrir **Aðaltengistreng (StackExchange.Redis)** (til dæmis með því að velja hnappinn **Afrita á klippiborð**).
1. Fara aftur í vafraflipann þar sem Supply Chain Management er í gangi. **Connect Azure tilföng** síðan ætti enn að vera opin.
1. Í reitnum **Tengistrengur fyrir mælingageymslu Redis** skal líma gildið **Aðaltengistrengur (StackExchange.Redis)** sem var afritað.
1. Veljið **Ljúka**.

Azure úrræði fyrir Sensor Data Intelligence eru nú útfærðar á Azure áskriftinni þinni.

> [!NOTE]
> Þú getur hvenær sem er skoðað eða breytt upplýsingum tengingar sem eru vistaðar í Supply Chain Management með því að opna síðuna **Færibreytur Sensor Data Intelligence**. Frekari upplýsingar er að finna í [Færibreytur Sensor Data Intelligence](sdi-parameters.md).
