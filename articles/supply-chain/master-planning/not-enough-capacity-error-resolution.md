---
title: 'Laga villu röðunarvélar: „Nægileg afköst fundust ekki“'
description: Í þessu efnisatriði er að finna upplýsingar um ástæður og úrlausnir fyrir „Ekki var hægt að tímasetja framleiðslupöntun %1. Nægileg afköst fundust ekki“ - Villa röðunarvélar.
author: crytt
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 37c990067a0c175d93ecf298866041f4d2afc1bc
ms.sourcegitcommit: ab1455c67f6ee6ca36bec148bea0dbb0f7704eda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/26/2021
ms.locfileid: "7428936"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>Laga villu röðunarvélar: „Nægileg afköst fundust ekki“

[!include [banner](../includes/banner.md)]

Þegar þú keyrir áætlanagerð gætir þú fengið eftirfarandi villuboð:

> Ekki tókst að raða framleiðslupöntun %1. Nægileg afköst fundust ekki.

Nokkrar ástæður geta verið fyrir því að röðunarvél gæti bilað og gefið út þessi villuboð. Í þessu efnisatriði er að finna leiðarvísa sem hjálpa þér að finna orsök villunnar og draga síðan úr henni.

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

Villan getur komið upp þegar þú framkvæmir takmarkaða röðun en engin afkastageta er til staðar.

Til að framkvæma ótakmarkaða röðun skal fylgja þessum skrefum.

1. Farðu í **Framleiðslustýring \> Framleiðslupantanir \> Allar framleiðslupantanir** og veldu eða opnaðu framleiðslupöntun sem ekki er hægt að áætla.
1. Á aðgerðasvæðinu, í flipanum **Áætlun**, í flokknum **Framleiðslupöntun**, skal velja **Áætla aðgerðir** eða **Áætla verk**.
1. Í svarglugganum **Aðgerðaröðun** eða **Verkröðun** skal stilla valkostinn **Takmörkuð geta** á *Nei*.
1. Veldu **Í lagi** til að áætla pöntunina.

Til að fara yfir tiltæka afkastagetu í tilfanginu skal fylgja þessum skrefum.

1. Farðu í **Fyrirtækisstjórnun \> Tilföng \> Tilföng** og veldu tilfang sem á við um pöntunina sem er ekki hægt að áætla.
1. Á aðgerðasvæðinu, í flipanum **Tilfang**, í flokknum **Yfirlit**, skal velja **Álag** eða **Álag, myndrænt** og ganga úr skugga um að tiltæk afkastageta sé fyrir hendi.

Til að fara yfir tiltæka afkastagetu í tilfangaflokknum skal fylgja þessum skrefum.

1. Farðu í **Fyrirtækisstjórnun \> Tilföng \> Tilfangaflokkar** og veldu tilfangaflokk sem á við um pöntunina sem er ekki hægt að áætla.
1. Á aðgerðasvæðinu, í flipanum **Tilfangaflokkur**, í flokknum **Yfirlit**, skal velja **Álag** eða **Álag, myndrænt** og ganga úr skugga um að tiltæk afkastageta sé fyrir hendi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]