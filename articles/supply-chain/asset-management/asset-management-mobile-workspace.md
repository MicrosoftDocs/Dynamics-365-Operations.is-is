---
title: Nota fartækjavinnusvæði eignastýringar
description: Þessi grein veitir upplýsingar um farsímavinnusvæði eignastýringar.
author: johanhoffmann
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: 8f215d5f6758f222a9dc6b382b172009836547ec
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067002"
---
# <a name="use-the-asset-management-mobile-workspace"></a>Nota fartækjavinnusvæði eignastýringar

[!include [banner](../../includes/banner.md)]
[!include [mobile app deprecated](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Þessi grein veitir upplýsingar um **Eignastýring** færanlegt vinnusvæði. Þetta vinnusvæði gerir notendum kleift að skoða og búa til viðhaldsbeiðnir og verkbeiðnir. Notendur geta einnig skoðað úthlutað verkbeiðnivinnslur í dagatali eða listaskjá. Einnig er hægt að skoða og leita að eignum og hagnýtum stöðum.

## <a name="overview"></a>Yfirlit

Eignastýring er ítarleg eining til að stjórna eignum og verkbeiðnistörfum í Dynamics 365 Supply Chain Management. Fartækjavinnusvæðið **Eignastýring** gerir notendum kleift að skoða fljótt úthlutuð vinnupöntunarstörf í fartæki að eigin vali. Notendur geta einnig búið til og stjórnað viðhaldsbeiðnum, uppfært stöðu lífsferils og skoðað upplýsingar um staðsetningu og eignir með því að nota fartæki sín.

Nánar tiltekið gerir fartækjavinnusvæðið **Eignastýring** notendum kleift að vinna þessi verk:

- Búðu til, skoðaðu og breyttu viðhaldsbeiðnum, taktu mynd eða hengdu fyrirliggjandi mynd við viðhaldsbeiðnina, breyttu líftímastöðu viðhaldsbeiðni. 
- Búðu til, skoðaðu og breyttu verkbeiðnum, taktu mynd eða hengdu fyrirliggjandi mynd við verkbeiðnina, breyttu líftímastöðu verkbeiðni, skoðaðu verkbeiðnaverk.
- Skoða úthlutuð verkbeiðniverk í dagbókaryfirliti.
- Búðu til, skoðaðu og breyttu verkbeiðniverkum, uppfærðu eignateljara, skoðaðu viðhaldsgátlista, skoðaðu og breyttu athugasemdum verkbeiðniverka, skoðaðu verkfærin sem þarf til að vinna í verkbeiðninni.
- Skoðaðu eða leitaðu að tiltekinni eign eða virkri staðsetningu.

## <a name="prerequisites"></a>Forkröfur

Áður en hægt er að nota fartækjavinnusvæðið **Eignastýring** þarf stjórnandinn að setja upp nauðsynlega notendur og reikninga starfskrafta og birta vinnusvæðið. Frekari upplýsingar eru í [Setja upp fartækjavinnusvæði eignastýringar](set-up-asset-management-mobile.md).

## <a name="download-and-install-the-mobile-app"></a>Sæktu og settu upp fartækjaforritið

Sæktu og settu upp fjármála- og rekstrarforritið (Dynamics 365):

- [Fyrir Android síma](https://go.microsoft.com/fwlink/?linkid=850662)
- [Fyrir iPhone síma](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Innskráning í fartækjaforritið

1. Ræstu forritið í fartækinu þínu.

1. Færðu inn vefslóð þína fyrir Dynamics 365.

1. Í fyrsta sinn sem þú skráir þig inn, er beðið um notandanafn og aðgangsorð þitt. Færðu inn skilríki

1. Eftir að þú hefur skráð þig inn, birtast tiltæk vinnusvæði fyrir fyrirtækið. Athugið að ef kerfisstjóri gefur út nýtt vinnusvæði síðar, verður að endurræsa listann yfir fartækjavinnusvæði.

    ![Velja vinnusvæði.](media/am-mobile-01.png "Velja vinnusvæði")

## <a name="view-assigned-work-order-jobs-in-calendar-view"></a>Skoða úthlutuð verkbeiðniverk í dagbókaryfirliti.

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

1. Veldu **Verkbeiðnaverkadagatalið mitt**.

1. Veldu dagsetninguna sem þú vilt skoða verkbeiðniverk fyrir. Á listanum sérðu eignaauðkenni og hagnýtt staðsetningarauðkenni fyrir hvert verk verkbeiðni.

1. Veldu verkbeiðnivinnslu á listanum til að sjá upplýsingar um vinnslu: Upplýsingar um eignir og hagnýtar staðsetningar ásamt öðrum leiðsögutenglum til að skoða **Viðhengi**, **Gátlistar**, **Verkfæri**, **Eignateljarar**, **Athugasemdir**, **Tímarit**.

    ![Skoða úthlutuð verkbeiðniverk í dagbókaryfirliti.](media/am-mobile-02.png "Skoða úthlutuð verkbeiðniverk í dagbókaryfirliti.")

## <a name="create-a-work-order-job"></a>Stofna verkbeiðnivinnslu

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

1. Veldu **Allar verkbeiðnir á viðhaldsvinnu**.

1. Veldu verkbeiðnina sem þú vilt stofna nýja vinnslu verkbeiðni fyrir.

1. Veldu hnappinn **Bæta við línu**.

1. Veldu **Eignina** sem þú vilt stofna vinnslu verkbeiðni fyrir.

1. Veldu **Tegund viðhaldsverks**, **Afbrigði af gerð viðhaldsverka** og **Verslun**.

1. Velja **Ekkert**.

    ![Skjámyndin Bæta við línu.](media/am-mobile-03.png "Skjámyndin Bæta við línu")


## <a name="add-attachment-to-a-work-order-job"></a>Bættu viðhengi við vinnslu verkbeiðni

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

1. Veldu **Allar verkbeiðnir á viðhaldsvinnu**.

1. Veldu verkbeiðnina > vinnslu verkbeiðni sem þú vilt bæta viðhengi við.
    - Einnig er hægt að velja **Verkbeiðnaverkadagatalið mitt** eða **Vinnslulistinn minn fyrir verkbeiðnir** á heimasíðunni til að fletta að síðunni **Upplýsingar um vinnslu verkbeiðni**.

1. Veldu **Viðhengi** á síðunni **Upplýsingar um vinnslu verkbeiðni**.

1. Þú munt sjá fyrirliggjandi viðhengi í vinnslu verkbeiðninnar. Veldu **Bæta við viðhengi**.

1. Skráðu **Heiti** og **Athugasemdir** fyrir viðhengið.

1. Veldu **Veldu mynd** til að velja mynd úr myndasafni farsímans, eða **Taka mynd** til að taka mynd.

1. Velja **Ekkert**.

    ![Skoða og bæta við viðhengjum fyrir verk í verkbeiðni.](media/am-mobile-04.png "Skoða og bæta við viðhengjum fyrir verk í verkbeiðni")

## <a name="view-maintenance-checklist-on-a-work-order-job"></a>Skoða viðhaldsgátlista í vinnslu verkbeiðni

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

1. Veldu **Allar verkbeiðnir á viðhaldsvinnu**.

1. Veldu verkbeiðnina > vinnslu verkbeiðni sem þú vilt skoða gátlista fyrir.
    - Einnig er hægt að velja **Verkbeiðnaverkadagatalið mitt** eða **Vinnslulistinn minn fyrir verkbeiðnir** á heimasíðunni til að fletta að síðunni **Upplýsingar um vinnslu verkbeiðni**.

1. Veldu **Gátlistar** á síðunni **Upplýsingar um vinnslu verkbeiðni**.

1. Þú munt sjá lista yfir gátlistalínur sem tengjast vinnslu verkbeiðninnar. Veldu gátlistalínu til að skoða **Leiðbeiningar** og bæta við **Athugasemdum**.

1. Veldu bakkhnappinn (**<**) til að snúa til baka á fyrri síðuna.

    ![Viðhaldsgátlisti og upplýsingar um línu.](media/am-mobile-05.png "Viðhaldsgátlisti og upplýsingar um línu")

## <a name="view-and-update-asset-counters-on-a-work-order-job"></a>Skoða og uppfæra eignateljara í vinnslu á verkbeiðni

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

1. Veldu **Allar verkbeiðnir á viðhaldsvinnu**.

1. Veldu verkbeiðnina > vinnslu verkbeiðni sem þú vilt skoða eignateljara fyrir.
    - Einnig er hægt að velja **Verkbeiðnaverkadagatalið mitt** eða **Vinnslulistinn minn fyrir verkbeiðnir** á heimasíðunni til að fletta að síðunni **Upplýsingar um vinnslu verkbeiðni**.

1. Veldu **Eignateljara** á síðunni **Upplýsingar um vinnslu verkbeiðni**.

1. Þú munt sjá lista yfir eignateljara sem tengjast vinnslu verkbeiðninnar. Veldu blýantstáknið á línu eignateljara til að uppfæra teljaragildið.

1. Sláðu inn nýtt teljaragildi og veldu **Lokið**.

    ![Skoða og uppfæra eignateljara.](media/am-mobile-06.png "Skoða og uppfæra eignateljara")

## <a name="register-consumption-on-a-work-order-job"></a>Skráðu notkun í vinnslu á verkbeiðni

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

1. Veldu **Allar verkbeiðnir á viðhaldsvinnu**.

1. Veljið Verkbeiðni > verk verkbeiðni sem bæta á við skráningu efnisnotkunar fyrir.
    - Einnig er hægt að velja **Verkbeiðnaverkadagatalið mitt** eða **Vinnslulistinn minn fyrir verkbeiðnir** á heimasíðunni til að fletta að síðunni **Upplýsingar um vinnslu verkbeiðni**.

1. Veldu **Færslubækur** á síðunni **Upplýsingar um vinnslu verkbeiðni**.

1. Veldu **Bæta við vinnustundum** til að búa til vinnutímaskráningar.
    1. Veldu **Flokk** úr leitinni.
    1. Í reitinn **Vinnustundir** skaltu slá inn fjölda vinnutíma sem varið er í vinnslu á verkbeiðni.
    1. Veldu viðeigandi **Línueiginleika**.
    1. Velja **Ekkert**.

1. Veldu **Bæta við vörum** til að búa til vöruskráningar.
    1. Veldu **Vörunúmer** úr uppflettingunni.
    1. Veldu **Svæði** úr uppflettingunni.
    1. Færðu inn **Magn** af notuðum vörum.
    1. Velja **Ekkert**.

1. Veldu **Bæta við kostnaði** til að búa til kostnaðarskráningar.
    1. Veldu **Flokk** úr leitinni.
    1. Færðu inn magn fyrir kostnaðarskráningu.
    1. Veldu **Gjaldmiðill sölu** úr uppflettingunni.
    1. Færðu inn **Kostnaðarverð** fyrir kostnaðarskráningu.
    1. Velja **Ekkert**.

    ![Uppfæra færslubók verkbeiðni.](media/am-mobile-07.png "Uppfæra færslubók verkbeiðni")

## <a name="update-lifecycle-state-on-a-work-order"></a>Uppfærðu líftímastöðu í verkbeiðni

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

1. Veldu **Allar verkbeiðnir á viðhaldsvinnu**.

1. Veldu verkbeiðnina sem þú vilt uppfæra líftímastöðu fyrir.

1. Veldu hnappinn **Uppfæra stöðu** neðst á skjánum.

1. Veldu nýja líftímastöðu af listanum.

1. Velja **Ekkert**.

    ![Uppfæra líftímastöðu í verkbeiðni.](media/am-mobile-08.png "Uppfærðu líftímastöðu í verkbeiðni")

## <a name="create-a-maintenance-request"></a>Stofna viðhaldsbeiðni

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

1. Veljið **Allar viðhaldsbeiðnir**.

1. Veldu **Aðgerðir** neðst á skjánum og veldu **Stofna viðhaldsbeiðni**.

1. Ef númeraröð er virkjuð fyrir viðhaldsbeiðnir í **Eignastýringu** er reiturinn **Viðhaldsbeiðni** falinn vegna þess að hann er sjálfkrafa fylltur út. Ef reiturinn **Viðhaldsbeiðni** er sýnilegur skaltu slá inn auðkenni viðhaldsbeiðni.

1. Veldu **Gerð viðhaldsbeiðni**.

1. Sláðu inn **Lýsingu** fyrir viðhaldsbeiðnina.

1. Veldu **Eign** sem þú vilt stofna beiðnina fyrir.

1. Veldu **Þjónustustig** fyrir viðhaldsbeiðnina.

1. Velja **Ekkert**.

    ![Stofna viðhaldsbeiðni.](media/am-mobile-09.png "Stofna viðhaldsbeiðni")

## <a name="add-attachment-to-a-maintenance-request"></a>Bættu viðhengi við viðhaldsbeiðni

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

1. Veljið **Allar viðhaldsbeiðnir**.

1. Veldu viðhaldsbeiðnina sem þú vilt bæta viðhengi við.

1. Veldu **Viðhengi** neðst á skjánum.

1. Veldu **Bæta við viðhengjum**.

1. Skráðu **Heiti** og **Athugasemdir** fyrir viðhengið.

1. Veljið **Velja mynd** til að velja mynd úr farsímagalleríinu eða **Taka mynd** til að taka mynd.

1. Velja **Ekkert**.

    ![Bæta viðhengi við viðhaldsbeiðni.](media/am-mobile-10.png "Bæta viðhengi við viðhaldsbeiðni")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

