---
title: Lagaðu „Ekki nóg af afkastagetu fannst“ í tímasetningarvélarvillu og endanlegri getu
description: Þessi grein veitir upplýsingar um ástæður og úrlausnir fyrir 'Framleiðslupöntun%1 ekki hægt að skipuleggja. Nægileg afköst fundust ekki“ - Villa röðunarvélar.
author: t-benebo
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4f54c06a07b3cdd0b8fe2cc52614189ff31ba7f
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135600"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>Laga villu röðunarvélar: „Nægileg afköst fundust ekki“

[!include [banner](../includes/banner.md)]

Þegar þú keyrir áætlanagerð gætir þú fengið eftirfarandi villuboð:

> Ekki tókst að raða framleiðslupöntun %1. Nægileg afköst fundust ekki.

Nokkrar ástæður geta verið fyrir því að röðunarvél gæti bilað og gefið út þessi villuboð. Þessi grein veitir leiðbeiningar sem hjálpa þér að finna undirrót villunnar og draga úr henni.

## <a name="review-the-applicable-resources"></a>Yfirfara viðeigandi úrræði

Villan getur átt sér stað ef engin viðeigandi úrræði fullnægja kröfum aðgerðarinnar á stað framleiðslupöntunar.

Til að fara yfir viðeigandi úrræði skal fylgja þessum skrefum.

1. Farðu í **Framleiðslustýring \> Framleiðslupantanir \> Allar framleiðslupantanir** og opnaðu eða veldu framleiðslupöntunina sem er ekki hægt að tímasetja.
1. Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Framleiðslupplýsingar**, skal velja **Leið**.
1. Á síðunni **Framleiðsluleið** skal velja aðgerðina og því næst á aðgerðasvæðinu skal velja **Viðeigandi úrræði**.
1. Í svarglugganum **Viðeigandi úrræði** skal stilla reitinn **Nota þarfir fyrir** á *Aðgerðaröðun* eða *Vinnsluröðun* eftir því hvaða gerð áætlanagerðar er notuð.
1. Ganga skal úr skugga um að viðeigandi úrræði séu til staðar á stað framleiðslupöntunar.

## <a name="review-the-calendars-that-are-associated-with-resources"></a>Yfirfara dagatöl sem tengjast úrræðum

Villan getur komið upp ef ekkert dagatal er tengt tilfanginu eða tilfangaflokknum eða ef tengt dagatal er ekki rétt uppsett (til dæmis ef það hefur engan vinnutíma eða ef skilvirkni þess í prósentum er 0 \[núll\]).

Til að staðfesta að dagatal tengist tilfanginu eða tilfangaflokknum skal fylgja þessum skrefum.

1. Farðu í **Framleiðslustýring \> Framleiðslupantanir \> Allar framleiðslupantanir** og opnaðu eða veldu framleiðslupöntunina sem er ekki hægt að tímasetja.
1. Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Framleiðslupplýsingar**, skal velja **Leið**.
1. Á síðunni **Framleiðsluleið** skal velja aðgerðina og því næst á aðgerðasvæðinu skal velja **Viðeigandi úrræði**.
1. Í svarglugganum **Viðeigandi tilföng** skal velja tilfangið og síðan velja **Skoða tilföng**. Einnig er hægt að velja og halda niðri (eða hægrismella) í reitnum **Forðahópur** og velja síðan **Skoða upplýsingar**.
1. Á síðunni **Tilföng** eða síðunni **Tilfangaflokkar**, í flýtiflipanum **Dagatöl**, skal ganga úr skugga um að dagatal tengist tilfanginu eða tilfangaflokknum.

> [!NOTE]
> Ef villan kemur upp við áætlanagerð aðgerðar verður að ganga úr skugga um að dagatal tengist öllum viðeigandi tilfangaflokkum.

Til að yfirfara uppsetningu dagatalsins skal fylgja þessum skrefum.

1. Farðu í **Fyrirtækisstjórnun \> Uppsetning \> Dagatöl \> Dagatöl** og veldu dagatalið sem tengist tilfanginu eða tilfangaflokknum.
1. Á aðgerðasvæðinu skal velja **Vinnutímar**.
1. Á síðunni **Vinnutímar** þarf að ganga úr skugga um að síðan sé ekki auð. Fyrir dagana sem þú hefur áhuga á þarf auk þess að ganga úr skugga um að reiturinn **Stýring** sé ekki stilltur á *Lokaður*, að vinnutímar séu til og að reiturinn **Skilvirkni er prósenta** sé ekki stilltur á *0* (núll).

Ef dagatalið tengist grunndagatalinu þarf einnig að yfirfara uppsetningu grunndagatalsins.

> [!NOTE]
> Í aðgerðaröðun er dagatal tilfangaflokks notað til að ákvarða upphafs- og lokatíma og dagsetningar fyrir hverja aðgerð. Það takmarkar einnig þann tíma sem kerfið getur áætlað fyrir eina tiltekna aðgerð fyrir einn tiltekinn dag í einum tilteknum tilfangaflokki. Ef til dæmis vinnutímar tilfangaflokks á einum ákveðnum degi er frá 8:00 til 16:00, getur álagið sem ein aðgerð setur á tilfangaflokkinn ekki verið meira en álagið sem hægt er að setja á átta klukkustundir, óháð því hve mikla afkastagetu tilfangaflokkurinn hefur þann dag. Tiltæk afkastageta getur hins vegar takmarkað álagið enn frekar.

## <a name="review-the-scheduling-parameters"></a>Fara yfir áætlunarfæribreytur

Til að tryggja góða frammistöðu mun röðunarvélin aðeins leita að tilfangi fyrir tiltekinn tímafjölda og tiltekinn fjölda árekstra í áætlanagerð.

Til að fara yfir áætlunarbreyturnar skal fylgja þessum skrefum.

1. Farðu í **Fyrirtækisstjórnun \> Uppsetning \> Áætlunarfæribreytur**.
1. Fylgið einu af eftirfarandi skrefum:

    - Ef valkosturinn **Tímalok áætlanagerðar virkjuð** er stilltur á *Nei* skal fara yfir í skref 3.
    - Ef valkosturinn **Tímalok áætlanagerðar virkjuð** er stilltur á *Já* skal auka gildið í reitnum **Hámarkstími röðunar á hverja röð** til að gefa úrvinnslunni meiri tíma til að ljúka verkinu.

1. Fylgið einu af eftirfarandi skrefum:

    - Ef valkosturinn **Tímalok fínstillingar áætlanagerðar virkjuð** er stilltur á *Nei* skal fara yfir í skref 4.
    - Ef valkosturinn **Tímalok fínstillingar áætlanagerðar virkjuð** er stilltur á *Já* skal auka gildið í reitnum **Tímalok fyrir tilraunir fínstillingar** til að gefa úrvinnslunni meiri tíma til að ljúka verkinu.

1. Ef þú breyttir einhverjum af stillingunum á síðunni skaltu enduráætla röðina og reyna aftur.

## <a name="review-capacity"></a>Yfirfara afköst

Villan getur komið fram þegar þú framkvæmir takmarkaða tímasetningu, en það er engin laus getu.

Til að framkvæma ótakmarkaða röðun skal fylgja þessum skrefum.

1. Farðu í **Framleiðslustýring \> Framleiðslupantanir \> Allar framleiðslupantanir** og veldu eða opnaðu framleiðslupöntun sem ekki er hægt að áætla.
1. Á aðgerðasvæðinu, í flipanum **Áætlun**, í flokknum **Framleiðslupöntun**, skal velja **Áætla aðgerðir** eða **Áætla verk**.
1. Í svarglugganum **Aðgerðaröðun** eða **Verkröðun** skal stilla valkostinn **Takmörkuð geta** á *Nei*.
1. Veldu **Í lagi** til að áætla pöntunina.

Til að fara yfir tiltæka afkastagetu í tilfanginu skal fylgja þessum skrefum.

1. Farðu í **Fyrirtækisstjórnun \> Tilföng \> Tilföng** og veldu tilfang sem á við um pöntunina sem er ekki hægt að áætla.
1. Á aðgerðarrúðunni, á **Auðlind** flipa, í **Útsýni** hópur, veldu **Afkastagetu álag** eða **Afkastagetu, myndrænt**, og ganga úr skugga um að það sé laus getu.

Til að fara yfir tiltæka afkastagetu í tilfangaflokknum skal fylgja þessum skrefum.

1. Farðu í **Fyrirtækisstjórnun \> Tilföng \> Tilfangaflokkar** og veldu tilfangaflokk sem á við um pöntunina sem er ekki hægt að áætla.
1. Á aðgerðarrúðunni, á **Auðlindahópur** flipa, í **Útsýni** hópur, veldu **Afkastagetu álag** eða **Afkastagetu, myndrænt**, og vertu viss um að það sé laus getu.

## <a name="master-planning-books-a-resource-when-the-resource-calendar-is-closed"></a>Aðalskipulag bókar tilfang þegar tilfangadagatalinu er lokað

Þegar aðgerðaáætlun er notuð mun aðaláætlanagerð skipuleggja afkastagetu í samræmi við dagatal aðaltilfangahópsins. Það bókar aukaaðgerðina á sama tíma og aðalaðgerðina og tekur ekki tillit til dagatala eða getu aukaaðgerðarinnar. Þetta getur leitt til þess að framleiðslupöntunin sé tímasett í lokuðu dagatali eða á þeim tíma þegar aukaaðgerðin er ekki tiltæk (dagatalið lokað, engin afkastageta).

Þegar verkáætlun er notuð mun aðalskipulag taka mið af afkastagetu og dagatali bæði aðal- og aukaaðgerðarinnar við tímasetningu pöntunarinnar. Til þess að hægt sé að skipuleggja pöntunina verða dagatöl fyrir tilföng beggja aðgerða að vera opin og hafa tiltæka getu.

## <a name="maximum-job-lead-time-is-too-short"></a>Hámarks afgreiðslutími verks er of stuttur

Tímasetningarvélin mun ekki geta skipulagt pöntun ef **Hámarks afgreiðslutími verks** stillt fyrir síðuna þína er styttri en afgreiðslutíminn sem tilgreindur er fyrir vöru í sjálfgefnum pöntunarstillingum eða þekjustillingum.

Til að skoða eða breyta **Hámarks afgreiðslutími verks** stillingu fyrir síðuna þína, farðu á **Framleiðslueftirlit \> Uppsetning \> Framleiðslustýringarbreytur** og opnaðu **Almennt** flipa.

Til að skoða eða breyta sjálfgefnum pöntunarstillingum fyrir vöru skaltu fylgja þessum skrefum:

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Finndu og veldu viðkomandi vöru á listanum.
1. Á aðgerðarrúðunni, opnaðu **Stjórna birgðum** flipann og veldu **Sjálfgefnar pöntunarstillingar**.
1. Stækkaðu **Birgðir** Flýtiflipa og skoða eða breyta **Leiðslutími birgða** stilla eftir þörfum.

Til að skoða eða breyta þekjustillingum fyrir hlut skaltu fylgja þessum skrefum:

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Finndu og veldu viðkomandi vöru á listanum.
1. Á aðgerðarrúðunni, opnaðu **Áætlun** flipann og veldu **Vöruumfjöllun**.
1. Opnaðu **Leiðslutími** flipann og skoða eða breyta **Framleiðslutími** gildi eftir þörfum.

## <a name="excessive-quantity-of-required-resources"></a>Of mikið magn af nauðsynlegum auðlindum

Meðan á tímasetningu stendur reynir vélin að passa nauðsynlega tilfangamagn sem sett er fyrir leiðaraðgerð við viðeigandi tilföng í samræmi við tilföng aðgerða. Ef auðlindamagnið er stillt of hátt getur það leitt til þess að leið sé óframkvæmanleg, sem veldur áætlunarvillu.

Notaðu eftirfarandi aðferð til að athuga bæði tilgreint magn og viðeigandi tilföng fyrir valda vöru, leið og leiðaraðgerð:

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Finndu og veldu viðkomandi vöru í ristinni.
1. Á aðgerðarrúðunni, opnaðu **Verkfræðingur** flipann og veldu **Leið**.
1. Finndu og veldu viðeigandi leið í töflunni.
1. Opið fyrir **Yfirlit** flipann neðst á síðunni.
1. Veldu aðgerð af listanum yfir valdar leiðaraðgerðir.
1. Veldu **Gildandi auðlindir** til að opna glugga þar sem þú getur skoðað viðeigandi tilföng fyrir valda leiðaraðgerð.
1. Opnaðu **Auðlindaálag** flipa. The **Magn** reiturinn hér sýnir auðlindamagnið sem þarf fyrir valda leiðaraðgerð. Skoðaðu og/eða breyttu því eftir þörfum.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
