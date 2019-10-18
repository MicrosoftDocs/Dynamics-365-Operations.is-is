---
title: Fartækjavinnusvæði eignastýringar
description: Í þessu efnisatriði er að finna upplýsingar um fartækjavinnusvæði eignastýringar.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: fd6f45a7dc9d062a3602499e89a6473b3b4aeaee
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2278383"
---
# <a name="asset-management-mobile-workspace"></a>Fartækjavinnusvæði eignastýringar

[!include [banner](../../includes/banner.md)]


Í þessu efnisatriði er að finna upplýsingar um fartækjavinnusvæði eignastýringar. Þetta vinnusvæði gerir notendum kleift að skoða og búa til viðhaldsbeiðnir og verkbeiðnir. Notendur geta einnig skoðað úthlutað verkbeiðnivinnslur í dagatali eða listaskjá. Einnig er hægt að skoða og leita að eignum og hagnýtum stöðum.


## <a name="overview"></a>Yfirlit

Eignastýring er ítarleg eining til að stjórna eignum og verkbeiðnistörfum í Dynamics 365 Supply Chain Management. Fartækjavinnusvæðið **Eignastýring** gerir notendum kleift að skoða fljótt úthlutuð vinnupöntunarstörf í fartæki að eigin vali. Notendur geta einnig búið til og stjórnað viðhaldsbeiðnum, uppfært stöðu lífsferils og skoðað upplýsingar um staðsetningu og eignir með því að nota fartæki sín.

Nánar tiltekið gerir fartækjavinnusvæðið **Eignastýring** notendum kleift að vinna þessi verk:

- Búðu til, skoðaðu og breyttu viðhaldsbeiðnum, taktu mynd eða hengdu fyrirliggjandi mynd við viðhaldsbeiðnina, breyttu líftímastöðu viðhaldsbeiðni. 
- Búðu til, skoðaðu og breyttu verkbeiðnum, taktu mynd eða hengdu fyrirliggjandi mynd við verkbeiðnina, breyttu líftímastöðu verkbeiðni, skoðaðu verkbeiðnaverk.
- Skoða úthlutuð verkbeiðniverk í dagbókaryfirliti.
- Búðu til, skoðaðu og breyttu verkbeiðniverkum, uppfærðu eignateljara, skoðaðu viðhaldsgátlista, skoðaðu og breyttu athugasemdum verkbeiðniverka, skoðaðu verkfærin sem þarf til að vinna í verkbeiðninni.
- Skoðaðu eða leitaðu að tiltekinni eign eða virkri staðsetningu.


## <a name="prerequisites"></a>Forkröfur

Skilyrðin eru mismunandi, byggt á útgáfu Dynamics 365 Supply Chain Management sem hefur verið sett upp fyrir fyrirtækið þitt.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-supply-chain-management"></a>Skilyrði ef þú notar Microsoft Dynamics 365 Supply Chain Management 
Ef Microsoft Dynamics 365 Supply Chain Management hefur verið innleitt í fyrirtækinu verður kerfisstjóri að birta fartækjavinnusvæðið **Eignastýring**. Leiðbeiningar er að finna í [Fartækjavinnusvæði birt](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

## <a name="download-and-install-the-mobile-app"></a>Sæktu og settu upp fartækjaforritið
Sæktu og settu upp fartækjaforritið Dynamics 365 for Unified Operations:

- [Fyrir Android síma](https://go.microsoft.com/fwlink/?linkid=850662)
- [Fyrir iPhone síma](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Innskráning í fartækjaforritið
1. Ræstu forritið í fartækinu þínu.

2. Færðu inn vefslóð þína fyrir Dynamics 365.

3. Í fyrsta sinn sem þú skráir þig inn, er beðið um notandanafn og aðgangsorð þitt. Færðu inn skilríki

4. Eftir að þú hefur skráð þig inn, birtast tiltæk vinnusvæði fyrir fyrirtækið. Athugið að ef kerfisstjóri gefur út nýtt vinnusvæði síðar, verður að endurræsa listann yfir fartækjavinnusvæði.

![Mynd 1](media/am-mobile-01.png)


## <a name="view-assigned-work-order-jobs-in-calendar-view"></a>Skoða úthlutuð verkbeiðniverk í dagbókaryfirliti.

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

2. Veldu **Verkbeiðnaverkadagatalið mitt**.

3. Veldu dagsetninguna sem þú vilt skoða verkbeiðniverk fyrir. Á listanum sérðu eignaauðkenni og hagnýtt staðsetningarauðkenni fyrir hvert verk verkbeiðni.

4. Veldu verkbeiðnivinnslu á listanum til að sjá upplýsingar um vinnslu: Upplýsingar um eignir og hagnýtar staðsetningar ásamt öðrum leiðsögutenglum til að skoða **Viðhengi**, **Gátlistar**, **Verkfæri**, **Eignateljarar**, **Athugasemdir**, **Tímarit**.

![Mynd 2](media/am-mobile-02.png)


## <a name="create-a-work-order-job"></a>Stofna verkbeiðnivinnslu

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

2. Veldu **Allar verkbeiðnir á viðhaldsvinnu**.

3. Veldu verkbeiðnina sem þú vilt stofna nýja vinnslu verkbeiðni fyrir.

4. Veldu hnappinn **Bæta við línu**.

5. Veldu **Eignina** sem þú vilt stofna vinnslu verkbeiðni fyrir.

6. Veldu **Tegund viðhaldsverks**, **Afbrigði af gerð viðhaldsverka** og **Verslun**.

7. Velja **Ekkert**.

![Mynd 3](media/am-mobile-03.png)


## <a name="add-attachment-to-a-work-order-job"></a>Bættu viðhengi við vinnslu verkbeiðni

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

2. Veldu **Allar verkbeiðnir á viðhaldsvinnu**.

3. Veldu verkbeiðnina > vinnslu verkbeiðni sem þú vilt bæta viðhengi við.
    - Einnig er hægt að velja **Verkbeiðnaverkadagatalið mitt** eða **Vinnslulistinn minn fyrir verkbeiðnir** á heimasíðunni til að fletta að síðunni **Upplýsingar um vinnslu verkbeiðni**.

4. Veldu **Viðhengi** á síðunni **Upplýsingar um vinnslu verkbeiðni**.

5. Þú munt sjá fyrirliggjandi viðhengi í vinnslu verkbeiðninnar. Veldu **Bæta við viðhengi**.

6. Skráðu **Heiti** og **Athugasemdir** fyrir viðhengið.

7. Veldu **Veldu mynd** til að velja mynd úr myndasafni farsímans, eða **Taka mynd** til að taka mynd.

8. Velja **Ekkert**.

![Mynd 4](media/am-mobile-04.png)


## <a name="view-maintenance-checklist-on-a-work-order-job"></a>Skoða viðhaldsgátlista í vinnslu verkbeiðni

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

2. Veldu **Allar verkbeiðnir á viðhaldsvinnu**.

3. Veldu verkbeiðnina > vinnslu verkbeiðni sem þú vilt skoða gátlista fyrir.
    - Einnig er hægt að velja **Verkbeiðnaverkadagatalið mitt** eða **Vinnslulistinn minn fyrir verkbeiðnir** á heimasíðunni til að fletta að síðunni **Upplýsingar um vinnslu verkbeiðni**.

4. Veldu **Gátlistar** á síðunni **Upplýsingar um vinnslu verkbeiðni**.

5. Þú munt sjá lista yfir gátlistalínur sem tengjast vinnslu verkbeiðninnar. Veldu gátlistalínu til að skoða **Leiðbeiningar** og bæta við **Athugasemdum**.

6. Veldu bakkhnappinn (**<**) til að snúa til baka á fyrri síðuna.

![Mynd 5](media/am-mobile-05.png)


## <a name="view-and-update-asset-counters-on-a-work-order-job"></a>Skoða og uppfæra eignateljara í vinnslu á verkbeiðni

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

2. Veldu **Allar verkbeiðnir á viðhaldsvinnu**.

3. Veldu verkbeiðnina > vinnslu verkbeiðni sem þú vilt skoða eignateljara fyrir.
    - Einnig er hægt að velja **Verkbeiðnaverkadagatalið mitt** eða **Vinnslulistinn minn fyrir verkbeiðnir** á heimasíðunni til að fletta að síðunni **Upplýsingar um vinnslu verkbeiðni**.

4. Veldu **Eignateljara** á síðunni **Upplýsingar um vinnslu verkbeiðni**.

5. Þú munt sjá lista yfir eignateljara sem tengjast vinnslu verkbeiðninnar. Veldu blýantstáknið á línu eignateljara til að uppfæra teljaragildið.

6. Sláðu inn nýtt teljaragildi og veldu **Lokið**.

![Mynd 6](media/am-mobile-06.png)


## <a name="register-consumption-on-a-work-order-job"></a>Skráðu notkun í vinnslu á verkbeiðni

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

2. Veldu **Allar verkbeiðnir á viðhaldsvinnu**.

3. Veldu verkbeiðnina > vinnslu verkbeiðni sem þú vilt bæta skráningu á notkun við fyrir.
    - Einnig er hægt að velja **Verkbeiðnaverkadagatalið mitt** eða **Vinnslulistinn minn fyrir verkbeiðnir** á heimasíðunni til að fletta að síðunni **Upplýsingar um vinnslu verkbeiðni**.

4. Veldu **Færslubækur** á síðunni **Upplýsingar um vinnslu verkbeiðni**.

5. Veldu **Bæta við vinnustundum** til að búa til vinnutímaskráningar.
    1. Veldu **Flokk** úr leitinni.
    2. Í reitinn **Vinnustundir** skaltu slá inn fjölda vinnutíma sem varið er í vinnslu á verkbeiðni.
    3. Veldu viðeigandi **Línueiginleika**.
    4. Velja **Ekkert**.

6. Veldu **Bæta við vörum** til að búa til vöruskráningar.
    1. Veldu **Vörunúmer** úr uppflettingunni.
    2. Veldu **Svæði** úr uppflettingunni.
    3. Færðu inn **Magn** af notuðum vörum.
    4. Velja **Ekkert**.

7. Veldu **Bæta við kostnaði** til að búa til kostnaðarskráningar.
    1. Veldu **Flokk** úr leitinni.
    2. Færðu inn magn fyrir kostnaðarskráningu.
    3. Veldu **Gjaldmiðill sölu** úr uppflettingunni.
    4. Færðu inn **Kostnaðarverð** fyrir kostnaðarskráningu.
    5. Velja **Ekkert**.

![Mynd 7](media/am-mobile-07.png)


## <a name="update-lifecycle-state-on-a-work-order"></a>Uppfærðu líftímastöðu í verkbeiðni

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

2. Veldu **Allar verkbeiðnir á viðhaldsvinnu**.

3. Veldu verkbeiðnina sem þú vilt uppfæra líftímastöðu fyrir.

4. Veldu hnappinn **Uppfæra stöðu** neðst á skjánum.

5. Veldu nýja líftímastöðu af listanum.

6. Velja **Ekkert**.

![Mynd 8](media/am-mobile-08.png)


## <a name="create-a-maintenance-request"></a>Stofna viðhaldsbeiðni

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

2. Veljið **Allar viðhaldsbeiðnir**.

3. Veldu **Aðgerðir** neðst á skjánum og veldu **Stofna viðhaldsbeiðni**.

4. Ef númeraröð er virkjuð fyrir viðhaldsbeiðnir í **Eignastýringu** er reiturinn **Viðhaldsbeiðni** falinn vegna þess að hann er sjálfkrafa fylltur út. Ef reiturinn **Viðhaldsbeiðni** er sýnilegur skaltu slá inn auðkenni viðhaldsbeiðni.

5. Veldu **Gerð viðhaldsbeiðni**.

6. Sláðu inn **Lýsingu** fyrir viðhaldsbeiðnina.

7. Veldu **Eign** sem þú vilt stofna beiðnina fyrir.

8. Veldu **Þjónustustig** fyrir viðhaldsbeiðnina.

9. Velja **Ekkert**.

![Mynd 9](media/am-mobile-09.png)


## <a name="add-attachment-to-a-maintenance-request"></a>Bættu viðhengi við viðhaldsbeiðni

1. Í fartækinu opnarðu vinnusvæðið **Eignastýring**.

2. Veljið **Allar viðhaldsbeiðnir**.

3. Veldu viðhaldsbeiðnina sem þú vilt bæta viðhengi við.

4. Veldu **Viðhengi** neðst á skjánum.

5. Veldu **Bæta við viðhengjum**.

6. Skráðu **Heiti** og **Athugasemdir** fyrir viðhengið.

7. Veldu **Veldu mynd** til að velja mynd úr myndasafni farsímans, eða **Taka mynd** til að taka mynd.

8. Velja **Ekkert**.

![Mynd 10](media/am-mobile-10.png)

