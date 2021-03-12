---
title: Stofna reikning með frjálsum texta
description: Í þessu efnisatriði er útskýrt hvernig á að stofna reikninga með frjálsum texta.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 726d4979059417871a00626c55da32fa4286cb53
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991118"
---
# <a name="create-a-free-text-invoice"></a>Stofna reikning með frjálsum texta

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að stofna reikninga með frjálsum texta. Fyrir ferlið skal nota **USMF** sýnifyrirtækið.

## <a name="create-a-free-text-invoice"></a>Stofna textareikning

1. Fara í **Viðskiptakröfur (eða fjárhag) \> Reikningar \> Allir reikningar með frjálsum texta**.
2. Veljið **Nýtt**.
3. Í reitnum **Viðskiptavinalykill** skal velja gildi.

    * Sjálfgefið er að lykill sem valinn er sem viðskiptavinalykill er notaður sem reikningslykill.
    * Ef reikningurinn er ekki bókaður byrjar bókhaldsstaðan á **Í vinnslu**.
    * Númeri reikningsins verður úthlutað þegar reikningurinn er bókaður.
    * Ef verið er að nota umboð fyrir sameiginlegt evrópskt greiðslusvæði (SEPA) er umboðið fyrir beingreiðslu sjálfkrafa fært inn þegar viðskiptavinalykill er valinn.

4. Sláið inn gildi í reitnum **Lýsing**.
5. Í reitnum **Aðallykill** skal tilgreina lykilnúmer sem er ekki með víddir. Víddir verða færðar inn síðar í þessu efnisatriði.

    Einnig er hægt að færa inn einn eða fleiri stafi fyrir aðallykilinn og nota uppflettingu til að finna lykilinn.

6. Veljið flýtiflipann **Línuupplýsingar** til að bæta víddum við aðallykilinn.
7. Veljið flipann **Fjárhagsvíddalína**.

    * Víddirnar eru aðeins ætlaðar fyrir valda línu.
    * VSK-flokkurinn er fylltur út frá viðskiptavininum. Ef viðskiptavinurinn er ekki með VSK-flokk er VSK-flokkur aðallykils notaður.
    * VSK-flokkur vöru er fylltur út frá aðallyklinum. Ef aðallykill er ekki með VSK-flokk vöru, þá er VSK-flokkur vörunnar sem tilgreindur er í færibreytum virðisaukaskatts í fjárhag notaður.

8. Valfrjálst: Sláið inn númer í reitinn **Magn**.
9. Valfrjálst: Sláið inn númer í reitinn **Einingarverð**.

    Upphæðin er reiknuð út sem magnið margfaldað með einingarverðinu. Hins vegar er hægt að hnekkja útreikningnum með því að færa inn upphæð.

10. Veljið **Virðisaukaskattur** til að skoða reiknaðan virðisaukaskatt fyrir reikninginn.

    Hægt er að skoða upphæðir virðisaukaskatts á þessari síðu, eða hnekkja upphæðunum á flipanum **Leiðrétting**.

11. Veldu **Í lagi**.
12. Veljið **Gjöld** til að bæta gjaldi við reikninginn.
13. Sláið inn gildi í reitinn **Gjaldakóði**.
14. Sláið inn númer í reitinn **Virði gjalda**.
15. Lokið síðunni.
16. Veljið **Samtölur** til að skoða samantekt á reikningsupplýsingum og heildarupplýsingum.
17. Veljið **Loka**.
18. Veljið **Bóka** til að bóka reikninginn. Enn er tækifæri til að hætta við áður en bókunin er gerð.

    * Hægt er að breyta tímasetningu á útprentun reiknings. Veljið **Núgildandi** til að prenta hvern reikning þegar hann er uppfærður. Veljið **Á eftir** til að prenta þegar allir reikningar hafa verið uppfærðir.
    * Til að breyta því hvernig lánamark viðskiptavinar er staðfest áður en reikningur er bókaður skal breyta gildinu í reitnum **Gerð lánamarks**.
    * Til að prenta reikninginn skal stilla valkostinn á **Já**.
    * Til að bóka reikninginn skal stilla valkostinn á **Já**. Hægt er að prenta reikninginn án þess að bóka hann.

19. Veldu **Í lagi**.

## <a name="copy-lines"></a>Afrita línur
Til að afrita línur á reikningi með frjálsum texta skal velja eina eða fleiri línur og velja síðan **Afrita valdar línur**. Hægt er að tilgreina fjölda eintaka sem á að gera og einnig er hægt að afrita athugasemdir og viðhengi. Annaðhvort er hægt að afrita dreifingarnar eða leyfa endursköpun þeirra við bókun.

Eftir afritun á línum er hægt að breyta upplýsingum eftir þörfum.

## <a name="create-a-free-text-invoice-from-a-template"></a>Búa til reikning með frjálsum texta út frá sniðmáti
Þú getur búið til reikning með frjálsum texta út frá sniðmáti. Þegar **Nýtt úr sniðmáti** er valið úr flipanum **Reikningur** er hægt að velja sniðmátsheiti og viðskiptavinalykilinn fyrir nýja reikninginn með frjálsum texta. Sjálfgefin gildi, svo sem greiðsluskilmálar og greiðslumáti, geta sjálfkrafa verið fyllt út af viðskiptavininum, eða hægt er að nota gildin sem voru vistuð í sniðmátinu.

Nýr reikningur með frjálsum texta verður búinn til og hægt er að breyta gildunum eftir þörfum.
