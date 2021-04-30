---
title: Safnvista birgðafærslur
description: Þetta efnisatriði lýsir því hvernig á að safnvista birgðafærslugögn til að hjálpa við að auka afköst kerfisins.
author: sherry-zheng
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: b740da1a8a349f4a1a80b41bf717c388fd3db0c0
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881833"
---
# <a name="archive-inventory-transactions"></a>Safnvista birgðafærslur

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Með tímanum mun birgðafærslutaflan (`InventTrans`) vaxa og nota meira pláss í gagnagrunni. Þess vegna verða fyrirspurnir þar sem sækja þarf upplýsingar úr töflunni smám saman hægari. Þetta efnisatriði lýsir því hvernig hægt er að nota *Safnvistun á birgðafærslum* eiginleikann til að safnvista gögn um birgðafærslur til að aðstoða við að auka afköst kerfisins.

> [!NOTE]
> Aðeins er hægt að safnvista fjárhagslega uppfærðum birgðafærslum á völdu lokuðu fjárhagstímabili. Til að vera safnvistað verða fjárhagslega uppfærðar birgðafærslur að vera með úthreyfingarstöðuna *Selt* og birgðafærslur á innleið verða að vera með nnhreyfingarstöðuna *Keypt*.

Þegar birgðafærslur eru safnvistaðar eru allar tengdar færslur færðar í `InventTransArchive`-töfluna. Úthreyfingarfærslur birgða og færslur á innhreyfingarskjali eru safnvistaðar sérstaklega, samkvæmt samsetningu vörukennisins (`itemId`) og birgðavíddaauðkenninu (`inventDimId`), og þær eru settar í samantektarfærslur og samanteknar innhreyfingarhreyfingar.

Ef `itemId` `inventDimId` samsetningin inniheldur aðeins eina kvittun eða úthreyfingafærslu, verður færslan ekki safnvistuð.

## <a name="turn-on-the-feature-in-your-system"></a>Kveikja á eiginleikanum í kerfinu

Ef kerfið inniheldur ekki eiginleikana sem lýst er í þessu efnisatriði skal fara í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eiginleikanum *Safnvistun á birgðafærslum*. Ekki er hægt að slökkva á þessum eiginleika þegar hann hefur verið gerður virkur.

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>Það sem þarf að hafa í huga áður en birgðafærslur eru safnvistaðar

Áður en birgðafærslur eru safnvistaðar ætti að hafa í huga eftirfarandi viðskiptaaðstæður vegna þess að þær verða fyrir áhrifum af aðgerðinni:

- Við endurskoðun á birgðafærslum úr tengdum skjölum, svo sem innkaupapöntunarlínum, birtast færslurnar sem safnvistaðar. Til að yfirfara safnvistaðar færslur þarf að fara í **Birgðastjórnun \> Reglubundin verk \> Hreinsun \> Safnvistun á birgðafærslum**.
- Ekki er hægt að hætta við birgðalokun fyrir safnvistuð tímabil. Áður en hægt er að hætta við birgðalokun verður að bakfæra birgðafærslusafnið fyrir viðkomandi tímabil.
- Ekki er hægt að umreikna staðalkostnað fyrir safnvistuð tímabil. Áður en hægt er að umreikna staðalkostnað verður að bakfæra birgðafærslusafnið fyrir viðkomandi tímabil.
- Safnvistun hefur áhrif á birgðaskýrslur sem eru færðar úr birgðafærslum. Þessar skýrslur innihalda aldursgreiningarskýrslu birgða og birgðavirðisskýrslur.
- Þetta kann að hafa áhrif á birgðaspár ef þær eru keyrðar meðan hámarkstími safnvistaðar tímabila er í gangi.

## <a name="prerequisites"></a>Forkröfur

Aðeins er hægt að safnvista birgðafærslur á tímabilum þar sem eftirfarandi skilyrði eru uppfyllt:

- Fjárhagstímabilið verður að vera lokað.
- Keyra verður birgðalokun á eða eftir lokatímabils safnsins.
- Tímabilið verður að vera að minnsta kosti einu ári frá upphafsdagsetningu safnsins.
- Engir endurútreikningar birgða mega vera til staðar.

## <a name="archive-inventory-transactions"></a>Safnvista birgðafærslur

Fylgið eftirfarandi skrefum til að halda áfram að safnvista birgðafærslur.

1. Farið í **Birgðastjórnun** \> **Reglubundin verk** \> **Hreinsun** \> **Safnvistun á birgðafærslum**.

    Síðan **Safnvistun á birgðafærslum** birtist og sýnir lista yfir eldri safnferlisfærslur.

    ![Safnvistunarsíða birgðafærslna](media/archive-inventory-empty.png "Safnvistunarsíða birgðafærslna")

1. Í aðgerðasvæði skal velja **Safnvistun á birgðafærslum** til að safnvista birgðafærslur.
1. Í svarglugganum **Safnvistun á birgðafærslum** á **Færibreytur** flýtiflipanum, skal stilla eftirfarandi reiti:

    - **Upphafsdagsetning í lokuðu fjárhagstímabili** – Veljið fyrstu dagsetningu færslu sem á að taka með í safninu.
    - **Lokadagsetning í lokuðu fjárhagstímabili** – Veljið síðustu dagsetningu færslu sem á að taka með í safninu.

    ![Svargluggi safnvistunar á birgðafærslum](media/archive-inventory-dates.png "Svargluggi safnvistunar á birgðafærslum")

    > [!NOTE]
    > Aðeins er hægt að velja tímabil sem uppfylla [Skilyrði](#prerequisites).

1. Í flýtiflipanum **Keyra í bakgrunni** skal stilla upplýsingar runuvinnslu eins og þörf er á. Fylgið venjulegum skrefum fyrir runuvinnslur í Microsoft Dynamics 365 Supply Chain Management.
1. Veljið **Í lagi**.
1. Þú færð skilaboð þar sem þú þarft að staðfesta á að þú viljir halda áfram. Lestu skilaboðin vandlega og veldu svo **Já** ef þú vilt halda áfram.

    Þú færð skilaboð sem segja til um að safnvistun birgðafærsla hafi verið bætt við runubiðröðina. Vinnslan hefur nú safnvistun birgðafærsla á völdu tímabili.

## <a name="view-archived-inventory-transactions"></a>Skoða safnvistaðar birgðafærslur

**Safnvistun á birgðafærslum** sýnir allan safnvistunarferil þinn. Hver lína í hnitanetinu sýnir upplýsingar á borð við dagsetninguna þegar safnið var búið til, notandann sem stofnaði það og stöðu þess.

![Safnvistunarferill á síðunni Safnvistun á birgðafærslum](media/archive-inventory-full.png "Safnvistunarferill á síðunni Safnvistun á birgðafærslum")

Í fellilistanum efst á síðunni skal velja eitt af eftirfarandi gildum til að sía safnvistanir sem eru sýndar í hnitanetinu:

- **Virkur** – Sýna aðeins virk söfn, ekki bakfærð söfn.
- **Allt** – Sýna öll söfn, bæði virk og bakfærð.

Fyrir hvert safn í hnitanetinu eru eftirfarandi upplýsingar veittar:

- **Virkt** – Gátmerki sýnir að safnið sé virkt.
- **Dagsetning frá** – Dagsetning elstu færslunnar sem hægt er að taka með í safninu.
- **Til dagsetningar** – Dagsetning nýjustu færslunnar sem hægt er að taka með í safninu.
- **Áætlað af** – Notandareikningurinn sem stofnaði safnið.
- **Keyrt** – Dagsetningin þegar safnið var stofnað.
- **Bakfæra** – Gátmerki gefur til kynna að safnið hafi verið bakfært.
- **Stöðva gildandi uppfærslu** – Gátmerki gefur til kynna að safnið sé í vinnslu en að hlé hafi verið gert á henni.
- **Staða** – Staða safnsins. Möguleg gildi eru *Í bið*, *Í vinnslu* og *Lokið*.

Tækjastikan fyrir ofan hnitanetið býður upp á eftirfarandi hnappa sem hægt er að nota til að vinna með valda safnvistun:

- **Safnvistaðar færslur** – Skoða allar upplýsingar um valið safn. Síðan **Safnvistaðar færslur** sem birtist sýnir allar færslurnar í safninu.

    ![Síða safnvistaðra færslna](media/archive-inventory-transactions.png "Síða safnvistaðra færslna")

    Til að skoða frekari upplýsingar um tiltekna færslu á síðunni **Safnvistaðar færslur** skal velja hana í hnitanetinu og síðan á aðgerðasvæðinu skal velja **Upplýsingar um safnvistaða færslu**. Síðan **Upplýsingar um safnvistaða færslu** sem birtist sýnir upplýsingar á borð við fjárhagsbókun, tengdar tilvísanir undirbókar og fjárhagsvíddir.

- **Gera hlé á safnvistun** – Gera hlé á valdri safnvistun sem er verið að vinna úr. Aðeins er gert hlé eftir að safnvistunarverk hefur verið myndað. Þess vegna gæti liðið stuttur tíma áður en hlé er gert. Þegar búið er að gera hlé birtist gátmerki í reitnum **Stöðva gildandi uppfærslu**.
- **Halda áfram safnvistun** – Halda áfram safnvistun fyrir valda safnvistun sem gert var hlé á.
- **Bakfæra** – Bakfæra valið safn. Aðeins er hægt að bakfæra safn ef **Staða** þess er stillt á *Lokið*. Ef safn hefur verið bakfært birtist gátmerki í reitnum **Bakfæra**.
