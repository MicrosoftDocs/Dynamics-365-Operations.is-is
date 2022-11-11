---
title: Áætlun með vali á tilföngum út frá getu
description: Þessi grein lýsir vali á tilföngum við óendanlega afkastagetu tímasetningu þegar þú tilgreinir getu sem tilfangaþörf fyrir aðgerð.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd, WrkCtrTable, WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 176f40ad8cd1aa1831bbe50c0ebd91ec0cc3bc89
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739899"
---
# <a name="scheduling-with-resource-selection-based-on-capability"></a>Röðun með vali á tilföngum út frá getu

[!include [banner](../../includes/banner.md)]

Með því að tilgreina tilfangaþarfir fyrir aðgerð framleiðsluleiðar skilgreinir þú það sem þarf til að framkvæma aðgerðina. Til dæmis gæti aðgerð þurft tiltekið tilfang eða tilfangaflokk eða samsetningu af hæfni eða getu. Þessi grein lýsir vali á tilföngum við óendanlega afkastagetu tímasetningu þegar þú tilgreinir getu sem tilfangaþörf fyrir aðgerð.

## <a name="turn-the-capability-based-scheduling-feature-on-or-off"></a>Kveiktu eða slökktu á aðgerðinni sem byggir á getu

Til að nota þennan eiginleika verður að vera kveikt á honum fyrir kerfið þitt. Frá og með Supply Chain Management útgáfu 10.0.29 er kveikt á eiginleikanum sjálfgefið. Stjórnendur geta kveikt eða slökkt á þessari virkni með því að leita að *Óendanlega getu tímaáætlun fyrir áætlanagerð hagræðingu* eiginleiki í [Eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými.

Nánari upplýsingar um þennan eiginleika má finna í [Röðun með ótakmarkaða getu](infinite-capacity-planning.md).

## <a name="capability-based-scheduling"></a>Áætlanagerð sem byggir á getu

Geta er hæfni rekstrartilfanga til að framkvæma tiltekinn verkþátt. Hægt er að úthluta fleiri en einum möguleika á stakt tilfang aðgerðar og stakri getu er hægt að úthluta á fleiri en eitt tilfang. Hægt er að úthluta getu á allar gerðir tilfanga, t.d. verkfæri, lánardrottna, vélar, staðsetningar, aðstöðu og mannauð.

Þegar þú tilgreinir getu sem tilfangaþarfir er hægt að fresta úthlutun tilfangs þar til pantanir eru tímasettar. Í stað þess að úthluta ákveðnum tilföngum eða tilfangaflokkum á leiðaraðgerð er hægt að skilgreina getuna sem þarf fyrir hverja leiðaraðgerð. Við áætlanagerð stemmir þá kerfið nauðsynlega getu við getuna sem er skilgreind fyrir tilföngin. Kerfið velur aðeins tilföng sem uppfylla þarfirnar.

Til að úthluta getu á tilfang aðgerðar skal nota flýtiflipann **Geta** á síðunni **Tilföng**. Til að úthluta tilföngum á getu skal nota flýtiflipann **Tilföng** af síðunni **Tilfangageta**. Báðar síðurnar eru aðgengilegar undir **Framleiðslustýring \> Uppsetning \> Tilföng** á yfirlitssvæðinu. Báðir flýtifliparnir innihalda hnitanet sem sýnir tilföngin sem tengjast völdu tilfangi eða getu. Báðir flýtifliparnir innihalda einnig tækjastiku sem hægt er að nota til að bæta við, fjarlægja eða breyta línum í hnitanetinu. Netið inniheldur eftirfarandi dálka:

- **Tilfang** eða **Geta** – Veldu tilfangið eða getuna sem línan er að úthluta.
- **Lýsing** – Færðu inn stutta lýsingu á tilföngunum eða afkastagetunni.
- **Gildistími** – Tilgreindu fyrstu dagsetninguna þegar úthlutun tilfangs eða getu á við. Meðan á áætlanagerð stendur mun kerfið ekki nota tilfang eða getu sem er með útrunna úthlutun á getu, jafnvel þótt þetta tilfang uppfyllir kröfurnar að öðru leyti.
- **Fyrning** – Tilgreindu síðustu dagsetninguna þegar úthlutun tilfangs eða getu á við. Meðan á áætlanagerð stendur mun kerfið ekki nota tilfang eða getu sem er með útrunna úthlutun á getu, jafnvel þótt þetta tilfang uppfyllir kröfurnar að öðru leyti.
- **Stig** – Tilgreindu hversu mikla færni tilfangið verður að vera með fyrir getuna. Ef þú tilgreinir síðan gildi fyrir **Lágmarksstig sem þarf** fyrir kröfu tilfangs eða getu tekur röðunarvélin til greina stig færni við val á tilfangi. Kerfið velur þá aðeins°tilföng°sem hafa nauðsynlega getu á stigi sem er jafnt eða°meira en lágmarksstig sem tilgreint er í tilfangakröfunni.
- **Forgangur** – Þessi reitur er enn ekki studdur af fínstillingu áætlanagerðar. Hins vegar, ef þú ert að nota úreltu aðalskipulagsvélina geturðu notað **Forgangur** reit í auðlindinni eða getuúthlutuninni til að skilgreina auðlindaforganginn. Ef *Forgangur* er valinn á svæðinu **Aðalval tilfanga** á síðunni **Röðunarfæribreytur** velur kerfið fyrst það tilfang sem hefur mestan forgang (það er lægsta tölulegt gildi á reitnum **Forgangur** i) við röðun.

## <a name="example"></a>Dæmi

Þetta dæmi sýnir hvernig röðunarvélin velur tilföng eftir getu.

Framleiðsluleið er með fimm aðgerðir: *10*, *20*, *30*, *40* og *50*. Hver leiðaraðgerð krefst tilfangs sem er með mismunandi getu. Til dæmis krefst leiðaraðgerð *10* tilfangs sem er með getuna til að setja saman hátalara (*0050 Hátalarasamsetning*) og getuna fyrir trésmíði (*1010 Trésmíðisgeta*). Leiðaraðgerð *50* krefst tilfangs sem er með getuna til að pakka framleiðslu (*0070 Pökkunargeta*).

![Geta til áætlunargerðar.](media/capability-based-scheduling.png "Geta til áætlunargerðar.")

Við áætlanagerð leitar vélin að tilföngum sem fullnægja kröfum aðgerðarinnar. Til dæmis velur áætlunarvélin tilfangið *00101* til að framkvæma aðgerð *10* vegna þess að þetta tilfang er fyrsta tilfangið sem finnst sem er með báðar nauðsynlegar getur. Röðunarvélin velur tilfang *00301* til að framkvæma aðgerð *50* vegna þess að þetta tilfang er eina tilfangið sem er með pökkunargetuna.

Því næst skaltu skoða hvaða áhrif það hefur á dæmið þegar hæfnisstig eru notuð:

- Aðgerð *10* krefst lágmarkshæfnisstigs *7* fyrir getuna *0059 Samsetning*.
- Tilfang *00101* er með hæfnisstig *5* fyrir getuna *0059 Samsetning*.
- Tilfang *00102* er með hæfnisstig *10* fyrir getuna *0059 Samsetning*.

Í þessu tilfelli, við áætlanagerð ótakmarkaðrar getu, velur röðunarvélin tilfang *00102* til að framkvæma aðgerð *10* vegna þess að þetta tilfang, ólíkt tilfangi *00101*, er með nauðsynlegt hæfnisstig fyrir getuna.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
