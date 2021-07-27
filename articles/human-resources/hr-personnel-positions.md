---
title: Stöður
description: Þetta efnisatriði lýsir hugmyndunum á bak við einingar sem staða getur haft. Það sýnir einnig dæmi um hvernig hægt er að nota þessar einingar í fyrirtækinu.
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: anbichse
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 269054
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b44cfaedc4e1286d033bba49b54a12b7e096bf99
ms.sourcegitcommit: 43962e6fedaf55aab2f28f53bc38a69d2ff58403
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2021
ms.locfileid: "6333129"
---
# <a name="positions"></a>Stöður

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir hugmyndunum á bak við einingar sem staða getur haft. Það sýnir einnig dæmi um hvernig hægt er að nota þessar einingar í fyrirtækinu.

Setja þarf upp starf áður en hægt er að stofna stöðu. Ákveðnar upplýsingar um stöðu, eins og launasvæði, verkefni starfskrafts, lengd stöðu og uppgefin tengsl, eru með gildisdagsetningum.

## <a name="general-information"></a>Almennar upplýsingar

Velja þarf starf þegar staða er stofnuð. Fyllt verður út í eftirfarandi upplýsingar sjálfkrafa úr starfinu sem þú velur:

- lýsing
- Titill
- Jafngildi fulls starfs
- Starfasafn

Starfstitill er notaður til að vísa í titil starfsmanns. (Titillinn sem starfsmaður fær er ekki notaður.) Því ættu starfstitlar að vera eins staðlaðir og hægt er.

> [!NOTE]
> Ekki er hægt að úthluta starfsmanni stöðu á dagsetningu sem kemur á undan dagsetningunni „tiltækt fyrir úthlutun“.
>
> Færibreyta í flipanum **Stöður** á síðunni **Samnýttar færibreytur Human Resources** stýrir hegðun á úthlutun starfsmanns. Veljið eitt af eftirfarandi gildum:
>
> - **Alltaf** - Hægt er að tengja starfsmenn við nýjar stöður þegar stöður eru búnar til. Þegar stöður eru stofnaðar í **Tiltækt fyrir úthlutun** eru dagsetning og tími í **Almennt** flipanum á **Stöðu** síðunni sjálfkrafa sett á stofnunardagsetningu og tíma.
> - **Aldrei** - Þú getur ekki úthlutað starfsmönnum á nýjar stöður þegar stöður eru búnar til. Ef þessi valkostur er valinn þarf að opna síðuna **Staða** fyrir hverja nýja stöðu þegar hún verður tiltæk. Síðan í flipanum **Almennt** skal færa inn dagsetninguna **Tiltækt til úthlutunar** til að virkja úthlutun starfsmanns. Ef þessi valkostur er valinn verður dagsetning á úthlutun starfsmanns stillt á **Aldrei** að sjálfgefnu þegar reynt er að úthluta starfsmanninum.

## <a name="position-duration"></a>Tímalengd stöðu

Allar stöður eru í gildi í tiltekinn tíma sem vísað er í sem tímalengd. Sumarstöður gætu til dæmis verið með tímalengdina 1. maí 2021 til 31. ágúst 2021. Virkjunardagsetningin er dagsetningin þegar staðan er virk í kerfinu. Starfslokadagsetningin er þegar staðan er ekki lengur virk í kerfinu.

Athugaðu að hvorki dagsetningin „tiltækt til úthlutunar“ né úthlutunardagsetning starfsmanns geta komið á undan virkjunardagsetningunni. Staða telst ekki virk fyrr en virkjunardagsetningu hefur verið náð. Auk þess getur úthlutun starfsmanns ekki farið yfir starfslokadag stöðunnar.

## <a name="reports-to-position"></a>Staða undir annarri stöðu

Stöður eru mikilvægir þættir á neðri stigum í stigveldi fyrirtækis. Á síðunni **Staða** er hægt að tilgreina stöðuna sem staða heyrir undir. Þegar starfsmanni er úthlutað stöðu sem heyrir undir aðra stöðu stofnarðu til tengsla milli starfsmanna sem er úthlutað þessum tveimur stöðum. Til dæmis heyrir staða 000220 undir stöðu 000300. Kim Akers er úthlutað stöðu 000220 og Sanjay Patel er úthlutað stöðu 000300. Þar af leiðandi er Kim Akers undir Sanjay Patel.

> [!TIP]
> Staða undir annarri stöðu er notuð í gegnum kerfið til að ákvarða hver sé yfirmaður starfsmannsins. Í fyrra dæminu, ef stjórnandahlutverkinu er úthlutað á Sanjay Patel í kerfinu, mun hann líta á Kim Akers sem beinan undirmann í sjálfsafgreiðslu stjórnanda. Tengslin má einnig nota þegar reglur um leiðir verkflæðis og gátlistaverk eru stofnuð.

## <a name="relationships"></a>Vensl

Ef fyrirtækið notar fylkisstigveldi eða annað sérsniðið stigveldi geturðu sett upp stigveldisgerðir stöðu. Þú getur síðan bætt venslum við stöður fyrir hverja gerð stigveldis sem er sett upp. Til dæmis er Lori Penor framkvæmdarstjóri hjá Adventure Works og fær stöðuna **Framkvæmdastjóri** úthlutaða. Lori stjórnar þróun afurðar sem er notuð til að hreinsa búnað. Hún þarf bókara til að aðstoða hana með fjármálin. Því hefur hún ráðið Kim Akers til að vera bókarinn hennar. Kim heyrir beint undir Sanjay Patel, en hún starfar einnig með Lori Penor í vinnu tengdri fjármálum fyrir þróun á hreinsunarbúnaði.

Í fyrra dæminu þarf að ljúka eftirfarandi verkum til að setja upp vinnutengslin milli Kim Akers og Lori Penor:

1. Búðu til sérsniðnar stöðu fyrir gerð stigveldis sem heitir **Búnaður** til að búa til stigveldi sem felur í sér stöður sem bera ábyrgð á vinnu við vöru hreinsunarbúnaðar.
2. Tilgreindu stöðuna **Framkvæmdastjóri** sem stöðuna sem Kim heyrir undir í stigveldinu **Búnaður**.
3. Stigveldi stöðu er notuð til að skoða skýrsluskipan fyrur stöður. Ef þú ert með margar stigveldi stöðu, hægt er að skoða stigveldi fyrir hvert gerð stigveldi í stigveldi stöðunnar. Einnig er hægt að leita að stöðu eftir kenni stöðu eða nafn þess starfsmanns sem er úthlutað á stöðu. Stigveldi stöðunnar er stigveldi fyrirtækis.

## <a name="labor-union"></a>Verkalýðsfélag

Hægt er að skrá hvort krafist er stéttarfélagssamnings fyrir stöðuna og hvaða verkalýðsfélag er notað. Þú getur einnig tengt samninginn við lögaðila.

## <a name="financial-dimensions"></a>Fjárhagsvíddir

Þegar þú býrð til fjárhagslega vídd fyrir stöðu þarftu að tilgreina lögaðila. Þú getur valið sjálfgefnar víddir fyrir hverja vídd fyrir sig. Einnig er hægt að velja dreifingarsniðmát til að fylla sjálfkrafa út sjálfgefnar víddir. Dreifingarsniðmát gefur einnig möguleika á að úthluta upphæðum á margar fjárhagsvíddir.
