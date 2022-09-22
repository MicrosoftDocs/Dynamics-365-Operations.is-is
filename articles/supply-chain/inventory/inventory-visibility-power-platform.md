---
title: Forrit birgðasýnileika
description: Þessi grein lýsir því hvernig á að nota Inventory Visibility appið.
author: yufeihuang
ms.date: 09/15/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 674adb70cc4372a8c5ca8c75ed3ef840d8ec7b79
ms.sourcegitcommit: d2046cad5de570e6302a4390b41881a7ecb12e26
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/15/2022
ms.locfileid: "9520865"
---
# <a name="use-the-inventory-visibility-app"></a>Nota Inventory Visibility-forritið

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að nota Inventory Visibility appið.

Birgðasýnileiki býður upp á líkanadrifið forrit fyrir myndræna framsetningu. Forritið inniheldur þrjár síður: **Skilgreining**, **Rekstrarsýnileiki** og **Birgðasamantekt**. Það er með eftirfarandi eiginleika:

- Það býður upp á notandaviðmót fyrir lagerskilgreiningu og skilgreiningu mjúkrar frátekningar.
- Það styður fyrirspurnir lagerbirgða í rauntíma í ýmsum víddarsamsetningum.
- Það býður upp á notendaviðmót fyrir bókun frátekningarbeiðna.
- Það gefur yfirsýn yfir birgðahaldið fyrir vörur ásamt öllum stærðum.
- Það veitir yfirsýn yfir birgðalista fyrir vörur ásamt fyrirfram skilgreindum víddum.


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

Þegar þú opnar **Fyrirspurn** flipi á **Sýnileiki í rekstri** síðu, biður kerfið um skilríki þín svo það geti fengið burðarmerkið sem þarf til að spyrjast fyrir um birgðasýnileikaþjónustuna. Þú getur einfaldlega límt handhafalykilinn í reitinn **BearerToken** og lokað svarglugganum. Þú getur síðan birt beiðni lagerfyrirspurnar.

Ef handhafalykillinn er ekki gildur eða hefur runnið út þarftu að líma nýjan í reitinn **BearerToken**. Færðu inn rétt gildi fyrir **Biðlarakenni**, **Leigjandakenni**, **Leynilykill biðlara** og veldu svo **Endurhlaða**. Kerfið mun sjálfkrafa fá nýjan gildan handhafalykil.

Til að birta beiðni lagerfyrirspurnar skal færa inn fyrirspurnina í meginmál beiðninnar. Notaðu mynstrið sem lýst er í [Fyrirspurn með því að nota bókunaraðferðina](inventory-visibility-api.md#query-with-post-method).

![Stillingar lagerfyrirspurnar](media/inventory-visibility-query-settings.png "Stillingar lagerfyrirspurnar")

### <a name="reservation-posting"></a>Bókun frátekningar

Nota **Bókunarfærsla** flipi á **Sýnileiki í rekstri** síðu til að senda inn bókunarbeiðni. Áður en hægt er að bóka frátekningarbeiðni þarf að kveikja á eiginleikanum *OnHandReservation*. Fyrir frekari upplýsingar um þennan eiginleika og hvernig á að kveikja á honum, sjá [Birgðasýnileiki fyrirvaranir](inventory-visibility-reservations.md).

Til að bóka frátekningarbeiðni þarftu að færa inn gildi í meginmál beiðninnar. Notaðu mynstrið sem lýst er í [Búa til eitt tilvik frátekningar](inventory-visibility-api.md#create-one-reservation-event). Veldu síðan **Bóka**. Til að skoða upplýsingar um svar beiðninnar velur þú **Sýna upplýsingar**. Þú getur einnig fengið gildið `reservationId` í upplýsingum um svarið.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Birgðayfirlit

The **Birgðayfirlit** síða veitir birgðayfirlit fyrir vörur ásamt öllum víddum. Það er sérsniðið útsýni fyrir *Inventory OnHand Summa* aðila. Birgðayfirlitsgögn eru samstillt reglulega frá Birgðasýnileika.

Til að virkja **Birgðayfirlit** síðu og stilltu samstillingartíðni, fylgdu þessum skrefum:

1. Opnaðu síðuna **Skilgreining**.
1. Opnaðu **Eiginleikastjórnun og stillingar** flipa.
1. Stilltu rofann fyrir **OnHandMostSpecificBackgroundService** lögun til *Já*.
1. Þegar aðgerðin er virkjuð mun **Þjónustustillingar** hluti verður tiltækur og inniheldur línu til að stilla **OnHandMostSpecificBackgroundService** eiginleiki. Þessi stilling gerir þér kleift að velja tíðni sem birgðayfirlitsgögn eru samstillt á. Nota **Upp** og **Niður** hnappar í **Gildi** dálki til að breyta tímanum á milli samstillinga (sem getur verið allt að 5 mínútur). Veldu síðan **Vista**.

    ![OnHandMostSpecificBackgroundService stillingin](media/inventory-visibility-ohms-freq.png "OnHandMostSpecificBackgroundService stillingin")

1. Veldu **Uppfærðu stillingar** til að vista allar breytingar.


> [!NOTE]
> The *OnHandMostSpecificBackgroundService* eiginleiki fylgist aðeins með birgðabreytingum sem áttu sér stað eftir að þú kveiktir á eiginleikanum. Gögn fyrir vörur sem hafa ekki breyst síðan þú kveiktir á eiginleikanum verða ekki samstillt úr skyndiminni birgðaþjónustunnar við Dataverse umhverfi. Ef þín **Birgðayfirlit** síða sýnir ekki allar fyrirliggjandi upplýsingar sem þú átt von á, opnaðu Supply Chain Management, farðu á **Birgðastjórnun > Reglubundin verkefni > Samþætting birgðasýnileika**, slökktu á runuvinnslunni og virkjaðu það aftur. Þetta mun gera fyrstu ýtuna og öll gögn verða samstillt við *Inventory OnHand Summa* aðila á næstu 15 mínútum. Ef þú vilt nota *OnHandMostSpecificBackgroundService* eiginleika, mælum við með að þú kveikir á honum áður en þú býrð til breytingar á hendi og virkjar **Samþætting birgðasýnileika** lotuvinna.

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-the-inventory-visibility-onhand-query"></a> Forhlaða straumlínulagaða fyrirspurn

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management geymir mikið af upplýsingum um núverandi birgðahald þitt og gerir það aðgengilegt fyrir margvíslegan tilgang. Hins vegar þurfa margar daglegar aðgerðir og samþættingar þriðju aðila aðeins lítið hlutmengi af þessum upplýsingum og að spyrja kerfið um þær allar getur leitt til stórra gagnasetta sem tekur tíma að setja saman og flytja. Þess vegna getur birgðasýnileiki þjónustan reglulega sótt og geymt straumlínulagað safn af birgðagögnum til að gera þessar fínstilltu upplýsingar stöðugt aðgengilegar. Geymdar upplýsingar um birgðahald eru síaðar út frá stillanlegum viðskiptaviðmiðum til að tryggja að aðeins viðeigandi upplýsingar séu innifaldar. Vegna þess að síaðir birgðabirgðalistar eru geymdir á staðnum í birgðasýnileikaþjónustunni og eru uppfærðir reglulega, styðja þeir skjótan aðgang, gagnaútflutning á eftirspurn og straumlínulagaða samþættingu við ytri kerfi.

> [!NOTE]
> Núverandi forskoðunarútgáfa af þessum eiginleika getur aðeins veitt forhlaðnar niðurstöður sem innihalda vefsvæði og staðsetningu. Búist er við að lokaútgáfan af eiginleikanum leyfi þér að velja aðrar víddir til að forhlaða niðurstöðunum.

The **Forhlaða samantekt birgðasýnileika** síða veitir útsýni fyrir *Forhlaða niðurstöður fyrir vísitölufyrirspurn* aðila. Ólíkt *Birgðayfirlit* eining, the *Forhlaða niðurstöður fyrir vísitölufyrirspurn* eining veitir birgðalista fyrir vörur ásamt völdum víddum. Birgðasýnileiki samstillir forhlaðna samantektargögnin á 15 mínútna fresti.

Til að skoða gögn á **Forhlaða samantekt birgðasýnileika** flipann verður þú að kveikja á *OnHandIndexQueryPreloadBackgroundService* eiginleiki á **Eiginleikastjórnun** flipi á **Stillingar** síðu og veldu síðan **Uppfærðu stillingar** (sjá einnig [Stilla birgðasýnileika](inventory-visibility-configuration.md)).

> [!NOTE]
> Eins og með *OnhandMostSpecificBackgroudService* eiginleiki, the *OnHandIndexQueryPreloadBackgroundService* eiginleiki fylgist aðeins með birgðabreytingum sem áttu sér stað eftir að þú kveiktir á eiginleikanum. Gögn fyrir vörur sem hafa ekki breyst síðan þú kveiktir á eiginleikanum verða ekki samstillt úr skyndiminni birgðaþjónustunnar við Dataverse umhverfi. Ef þín **Birgðayfirlit** síða sýnir ekki allar þær upplýsingar sem þú ert að búast við, farðu á **Birgðastjórnun > Reglubundin verkefni > Samþætting birgðasýnileika**, slökktu á runuvinnslunni og virkjaðu það aftur. Þetta mun gera fyrstu ýtuna og öll gögn verða samstillt við *Niðurstöður forhlaða vísitölufyrirspurna fyrir hendi* aðila á næstu 15 mínútum. Ef þú vilt nota þennan eiginleika mælum við með því að þú kveikir á honum áður en þú býrð til breytingar á hendi og virkjar **Samþætting birgðasýnileika** lotuvinna.

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a> Sía og fletta í birgðayfirlitum

Með því að nota **Ítarlega sía** sem Dataverse býður upp á getur þú búið til eigið yfirlit sem sýnir línurnar sem skipta þig máli. Ítarlegir síuvalkostir gera þér kleift að búa til margvísleg yfirlit, bæði einföld og flókin. Þeir gera þér einnig kleift að bæta flokkuðum og földuðum skilyrðum við síurnar. Til að læra meira um hvernig á að nota háþróaða síuna, sjá [Breyttu eða búðu til persónulegar skoðanir með því að nota háþróaða netsíur](/powerapps/user/grid-filters-advanced).

The **Birgðayfirlit** síða gefur upp þrjá reiti fyrir ofan hnitanetið (**Sjálfgefin vídd**, **vídd**, og **Mæla**) sem þú getur notað til að stjórna hvaða dálkar eru sýnilegir. Þú getur líka valið hvaða dálkhaus sem er til að sía eða flokka núverandi niðurstöðu eftir þeim dálki. Eftirfarandi skjámynd dregur fram vídd, síun, niðurstöðutölu og „hlaða meira“ reiti sem eru tiltækir á **Birgðayfirlit** síðu.

![Birgðayfirlit síðan.](media/inventory-visibility-onhand-list.png "Birgðayfirlit síðan")

Vegna þess að þú hefur fyrirfram skilgreint stærðirnar sem notaðar eru til að hlaða yfirlitsgögnum, **Forhlaða samantekt birgðasýnileika** síða sýnir víddartengda dálka. *Stærðirnar eru ekki sérhannaðar&mdash; kerfið styður aðeins svæðis- og staðsetningarvíddir fyrir forhlaðna geymslulista.* The **Forhlaða samantekt birgðasýnileika** síða veitir síur sem eru svipaðar þeim sem eru á **Birgðayfirlit** síðu, nema stærðirnar eru þegar valdar. Eftirfarandi skjámynd undirstrikar síunarreitina sem eru tiltækir á **Forhlaða samantekt birgðasýnileika** síðu.

![Forhlaða yfirlitssíðu birgðasýnileika.](media/inventory-visibility-preload-onhand-list.png "Forhlaða yfirlitssíðu birgðasýnileika")

Neðst á **Forhlaða samantekt birgðasýnileika** og **Birgðayfirlit** síðum, finnur þú upplýsingar eins og "50 færslur (29 valdar)" eða "50 færslur". Þessar upplýsingar vísa í núverandi hladdar færslur úr niðurstöðunni **Ítarleg sía**. Textinn „29 valdar“ vísar til fjölda færslna sem hafa verið valdar með því að nota síu dálkhauss fyrir færslurnar sem var hlaðið inn. Það er líka a **Hlaða meira** hnappinn sem þú getur notað til að hlaða fleiri færslum frá Dataverse. Sjálfgefinn fjöldi hlaðna skráa er 50. Þegar þú velur **Hlaða meira**, næstu 1.000 tiltæku færslur verða hlaðnar inn í yfirlitið. Talan á hnappnum **Hlaða fleiri** gefur til kynna núverandi fjölda að færslum sem er hlaðið inn og heildarfjölda af færslum fyrir niðurstöðu **Ítarlegrar síu**.
