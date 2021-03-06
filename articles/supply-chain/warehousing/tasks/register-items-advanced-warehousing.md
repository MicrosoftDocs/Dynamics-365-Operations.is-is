---
title: Skrá vörur fyrir vöru með ítarlegt vöruhúsakerfi virkt með því að nota komubók
description: Þetta efnisatriði lýsir aðstæðum sem sýnir hvernig á að skrá vörur með komubók þegar ítarleg felri vöruhúsastjórnunar eru notuð.
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830835"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Skrá vörur fyrir vöru með ítarlegt vöruhúsakerfi virkt með því að nota komubók

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir aðstæðum sem sýnir hvernig á að skrá vörur með komubók þegar ítarleg felri vöruhúsastjórnunar eru notuð. Þetta væri yfirleitt gert með af móttöku starfsmaður.

## <a name="enable-sample-data"></a>Virkja gögn sýnishorna

Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind í þessu efnisatriði er nauðsynlegt að nota kerfi þar sem venjuleg sýnigögn eru sett upp og velja þarf lögaðilann *USMF* áður en hafist er handa.

Hægt er að vinna með þessar astæður með því að skipta gildum úr eigin gögnum ef eftirfarandi gögn eru tiltæk:

- Þú þarft að hafa staðfest innkaupapöntun með opna innkaupapöntunarlínu.
- Varan á línunni verðu að vera á lager. Það má ekki nota afurðarafbrigði og má ekki hafa rakningarvíddir.
- Varan verður að vera tengd við geymsluvíddarflokk sem er með virkt vöruhúsakerfisferli.
- Vöruhús sem er notað verður að vera virkt fyrir vöruhúsakerfisferli og staðsetning sem er notað fyrir móttöku verður að vera númeraplötustýrð.

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a>Stofna haus vörukomubókar sem notar vöruhúsakerfi

Eftirfarandi aðstæður sýna hvernig á að stofna síðuhaus í komubók vöru sem notar vöruhúsakerfi:

1. Gangið úr skugga um að kerfið innihaldi staðfesta innkaupapöntun sem uppfyllir kröfurnar sem lýst er í fyrri hlutanum. Þessi atburðarás notar innkaupapöntun fyrir fyrirtæki *USMF*, lánardrottnalykil *1001*, vöruhús *51* með pöntunarlínu fyrir *10 bretti* af vörunúmeri *M9200*.
1. Skráið niður innkaupapöntunarnúmerið sem á að nota.
1. Farið í **Birgðastjórnun \> Færslubókarfærslur \> Vörumóttaka \> Vörumóttaka**.
1. Veljið **Nýtt** á aðgerðasvæðinu.
1. Svarglugginn **Stofna færslubók vöruhúsakerfis** opnast. Veljið færslubókarheiti í svæðinu **Heiti**.
    - Ef *USMF* sýnigögn eru notuð skal velja *WHS*.
    - Ef eigin gögn eru notuð verður færslubókin sem er valin að vera með **Athuga tiltektarstaðsetningu** stillt á *Nei* og **Biðgeymslustjórnun** stillt á *Nei*.
1. Stillið **Tilvísun** á *Innkaupapöntun*.
1. Stillið **Reikningsnúmer** á *1001*.
1. Stillið **Númer** á númer innkaupapöntunarinnar sem var tengd fyrir þessa æfingu.

    ![Vörukomubók](../media/item-arrival-journal-header.png "Vörukomubók")

1. Veldu **Í lagi** til að búa til færslubókarhausinn.
1. Í hlutanum **Færslubókarlínur** skal velja **Bæta við línu** og færa inn eftirfarandi gögn:
    - **Vörunúmer** – Stillið á *M9200*. **Svæðið**, **Vöruhúsið** og **Magnið** verður stillt út frá birgðafærslugögnunum fyrir 10 bretti (1000 ea.).
    - **Staðsetning** – stillt á  *001*. Þessi tiltekna staðsetning rekur ekki númeraplötur.

    ![Lína vörukomubókar](../media/item-arrival-journal-line.png "Lína vörukomubókar")

    > [!NOTE]
    > Reiturinn **Dagsetning** ákvarðar dagsetninguna sem verður að skrá magn á lager fyrir þessa vöru í birgðum.  
    >
    > **Lotukenni** er fyllt út af kerfinu ef hægt er að auðkenna það úr uppgefnum upplýsingum. Annars þarf að slá þetta inn handvirkt. áskilið svæði skyldusvæði sem tengir þessa skráningu við tiltekna upprunaskjalslínu.  

1. Veljið **Villuleita** á aðgerðasvæðinu. Þetta athugar hvort færslubókin sé tilbúin til bókunar. Ef sannvottun bregst verður að lagfæra villurnar áður en hægt er að bóka færslubókina.  
1. Svarglugginn **Villuleita færslubók** opnast. Veljið **Í lagi**.
1. Skoða skilaboðastiku. Skilaboð ættu að birtast sem segja að aðgerðinni sé lokið.  
1. Á aðgerðasvæðinu skal velja **Bóka**.
1. Svarglugginn **Bóka færslubók** opnast. Veljið **Í lagi**.
1. Skoða skilaboðastiku. Skilaboð ættu að birtast um að aðgerðinni sé lokið.
1. Veljið **Aðgerðir > Innhreyfingarskjal afurðar** á aðgerðasvæðinu til að uppfæra innkaupapöntunarlínuna og bóka innhreyfingarskjal afurðar.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
