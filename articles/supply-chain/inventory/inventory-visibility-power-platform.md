---
title: Forrit birgðasýnileika
description: Þessi grein lýsir því hvernig á að nota Inventory Visibility appið.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: db158e3b6ae76f69149db04096f99d3dc4251146
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895758"
---
# <a name="use-the-inventory-visibility-app"></a>Nota Inventory Visibility-forritið

[!include [banner](../includes/banner.md)]


Þessi grein lýsir því hvernig á að nota Inventory Visibility appið.

Birgðasýnileiki býður upp á líkanadrifið forrit fyrir myndræna framsetningu. Forritið inniheldur þrjár síður: **Skilgreining**, **Rekstrarsýnileiki** og **Birgðasamantekt**. Það er með eftirfarandi eiginleika:

- Það býður upp á notandaviðmót fyrir lagerskilgreiningu og skilgreiningu mjúkrar frátekningar.
- Það styður fyrirspurnir lagerbirgða í rauntíma í ýmsum víddarsamsetningum.
- Það býður upp á notendaviðmót fyrir bókun frátekningarbeiðna.
- Það býður upp á sérstillt yfirlit yfir lagerbirgðir fyrir afurðir með öllum víddum.

## <a name="prerequisites"></a>Forkröfur

Áður en hafist er handa skal setja upp innbót birgðasýnileika eins og lýst er í [Setja upp sýnileika birgða](inventory-visibility-setup.md).

## <a name="open-the-inventory-visibility-app"></a>Opna forrit birgðasýnileika

Til að opna forrit birgðasýnileika skal skrá sig inn í Power Apps umhverfið og opna **Birgðasýnileika**.

## <a name="configuration"></a><a name="configuration"></a>Grunnstilling

Síðan **Skilgreining** birgðasýnileikaforritsins hjálpar til við að setja upp lagerskilgreiningu og skilgreiningu mjúkrar frátekningar. Eftir að innbót hefur verið sett upp inniheldur sjálfgefna stillingin sjálfgefna uppsetningu frá Microsoft Dynamics 365 Supply Chain Management (`fno` gagnagjafinn). Hægt er að fara yfir sjálfgefnu stillinguna. Byggt á viðskiptaþörfum þínum og þörfum birgðabókunar ytra kerfisins geturðu auk þess breytt skilgreiningunni í til að staðla leiðina sem hægt er að bóka, skipuleggja og senda fyrirspurn á birgðabreytingar í hinum ýmsu kerfum.

Nánari upplýsingar um hvernig á að skilgreina lausnina er að finna í [Stilla sýnileika birgða](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Rekstrarsýnileiki

Síðan **Rekstrarsýnileiki** sýnir niðurstöður fyrirspurnar um lagerbirgðir í rauntíma sem byggir á ýmsum víddarsamsetningum. Þegar kveikt er á eiginleikanum *OnHandReservation* er einnig hægt að bóka beiðnir frátekningar á síðunni **Rekstrarsýnileiki**.

### <a name="on-hand-query"></a>Fyrirspurn lagerbirgða

Flipinn **Fyrirspurn lagerbirgða** sýnir niðurstöður fyrirspurnar vegna lagerbirgða í rauntíma.

Þegar flipinn **Fyrirspurn lagerbirgða** er valinn biður kerfið um innskráningarupplýsingarnar þínar svo það geti fengið handhafalykilinn sem þarf til að senda fyrirspurn á þjónustu birgðasýnileika. Þú getur einfaldlega límt handhafalykilinn í reitinn **BearerToken** og lokað svarglugganum. Þú getur síðan birt beiðni lagerfyrirspurnar.

Ef handhafalykillinn er ekki gildur eða hefur runnið út þarftu að líma nýjan í reitinn **BearerToken**. Færðu inn rétt gildi fyrir **Biðlarakenni**, **Leigjandakenni**, **Leynilykill biðlara** og veldu svo **Endurhlaða**. Kerfið mun sjálfkrafa fá nýjan gildan handhafalykil.

Til að birta beiðni lagerfyrirspurnar skal færa inn fyrirspurnina í meginmál beiðninnar. Notaðu mynstrið sem lýst er í [Fyrirspurn með því að nota bókunaraðferðina](inventory-visibility-api.md#query-with-post-method).

![Stillingar lagerfyrirspurnar](media/inventory-visibility-query-settings.png "Stillingar lagerfyrirspurnar")

### <a name="reservation-posting"></a>Bókun frátekningar

Notaðu flipann **Bókun frátekningar** til að bóka frátekningarbeiðni. Áður en hægt er að bóka frátekningarbeiðni þarf að kveikja á eiginleikanum *OnHandReservation*. Nánari upplýsingar um þennan eiginleika er að finna í [Frátekningar birgðasýnileika](inventory-visibility-reservations.md).

Til að bóka frátekningarbeiðni þarftu að færa inn gildi í meginmál beiðninnar. Notaðu mynstrið sem lýst er í [Búa til eitt tilvik frátekningar](inventory-visibility-api.md#create-one-reservation-event). Veldu síðan **Bóka**. Til að skoða upplýsingar um svar beiðninnar velur þú **Sýna upplýsingar**. Þú getur einnig fengið gildið `reservationId` í upplýsingum um svarið.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Birgðayfirlit

**Birgðasamantekt** er sérstillt yfirlit fyrir Einingu fyrir *samtölu lagerbirgða*. Þar er að finna birgðasamantekt fyrir afurðir ásamt öllum víddum. Birgðayfirlitsgögn eru samstillt reglulega frá Birgðasýnileika á 15 mínútna fresti. Til að sjá gögn um **Birgðayfirlit** flipann verður þú að kveikja á *OnHandMostSpecificBackgroundService* eiginleiki á **Eiginleikastjórnun** flipann og veldu **Uppfærðu stillingar**.

> [!NOTE]
> The *OnHandMostSpecificBackgroundService* eiginleiki fylgist aðeins með vörubreytingum sem áttu sér stað eftir að þú kveiktir á eiginleikanum. Gögn fyrir vörur sem hafa ekki breyst síðan þú kveiktir á eiginleikanum verða ekki samstillt úr skyndiminni birgðaþjónustunnar við Dataverse umhverfi. Ef þín **Birgðayfirlit** síða sýnir ekki allar þær upplýsingar sem þú ert að búast við, farðu á **Birgðastjórnun > Reglubundin verkefni > Samþætting birgðasýnileika**, slökktu á runuvinnslunni og virkjaðu það aftur. Þetta mun gera fyrstu ýtuna og öll gögn verða samstillt við *Inventory OnHand Summa* aðila á næstu 15 mínútum. Ef þú vilt nota þennan eiginleika mælum við með því að þú kveikir á honum áður en þú býrð til breytingar á hendi og virkjar **Samþætting birgðasýnileika** lotuvinna.

Með því að nota **Ítarlega sía** sem Dataverse býður upp á getur þú búið til eigið yfirlit sem sýnir línurnar sem skipta þig máli. Ítarlegir síuvalkostir gera þér kleift að búa til margvísleg yfirlit, bæði einföld og flókin. Þeir gera þér einnig kleift að bæta flokkuðum og földuðum skilyrðum við síurnar. Frekari upplýsingar um hvernig á að nota **Ítarlega sía** er að finna í [Breyta eða búa til eigin yfirlit með ítarlegum síum hnitanets](/powerapps/user/grid-filters-advanced).

Efst á sérsniðnu yfirliti eru gefnir upp þrír reitir: **Sjálfgefin vídd**, **Sérstillt vídd** og **Mæling**. Hægt er að nota þessa reiti til að stjórna því hvaða dálkar eru sýnilegir.

Hægt er að velja dálkhaus til að sía eða raða núverandi niðurstöðu.

Neðst í sérsniðnu yfirliti eru upplýsingar sýndar á borð við „50 færslur (29 valdar)“ eða „50 færslur“. Þessar upplýsingar vísa í núverandi hladdar færslur úr niðurstöðunni **Ítarleg sía**. Textinn „29 valdar“ vísar til fjölda færslna sem hafa verið valdar með því að nota síu dálkhauss fyrir færslurnar sem var hlaðið inn.

Neðst á yfirlitinu er hnappurinn **Hlaða fleiri** sem þú getur notað til að hlaða fleiri færslur úr Dataverse. Sjálfgefinn færslufjöldi sem hlaðið er inn er 50. Þegar þú velur **Hlaða fleiri** verða næstu 1000 tiltækar færslur hlaðnar inn í yfirlitið. Talan á hnappnum **Hlaða fleiri** gefur til kynna núverandi fjölda að færslum sem er hlaðið inn og heildarfjölda af færslum fyrir niðurstöðu **Ítarlegrar síu**.

![Birgðayfirlit](media/inventory-visibility-onhand-list.png "Birgðayfirlit")
