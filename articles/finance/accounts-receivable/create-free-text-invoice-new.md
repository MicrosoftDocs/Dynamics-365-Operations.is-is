---
title: Stofna reikning með frjálsum texta
description: Í þessu efnisatriði er útskýrt hvernig á að stofna reikninga með frjálsum texta.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 6e9578d9b2d61f241ab5e92fc9740b88b80969f6
ms.sourcegitcommit: 411874545d7c326fc4aa877948a059371f0ccb3c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/07/2022
ms.locfileid: "8392886"
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
    * Þú getur valið að hætta að birta reikninga með frjálsum texta þegar villa kemur upp á **Uppfærslur** flipann á **Færibreytur viðskiptakrafna** síða (**Viðskiptakröfur > Uppsetning > Færibreytur viðskiptakrafna**). Veldu **Já** fyrir **Hættu að bóka ókeypis textareikninga við fyrstu villu** færibreytu til að stöðva bókun reikninga með frjálsum texta þegar villa kemur upp. Ef bókað er í runu mun villa stöðva bókunarferlið og lotustaðan verður stillt á **Villa**. Ef þessi valkostur er ekki valinn mun bókunarferlið sleppa reikningi með bókunarvillu og halda áfram að bóka viðbótarreikninga. Ef bókað er í lotu mun bókunarvilla ekki koma í veg fyrir að aðrir reikningar séu bókaðir. Staða lotunnar verður **Lokað**. Ítarleg skýrsla um birtingarferli verður tiltæk til skoðunar í runuvinnusögu.
    * Til að prenta reikninginn skal stilla valkostinn á **Já**.
    * Til að bóka reikninginn skal stilla valkostinn á **Já**. Hægt er að prenta reikninginn án þess að bóka hann.

19. Veldu **Í lagi**.

## <a name="copy-lines"></a>Afrita línur
Til að afrita línur á reikningi með frjálsum texta skal velja eina eða fleiri línur og velja síðan **Afrita valdar línur**. Hægt er að tilgreina fjölda eintaka sem á að gera og einnig er hægt að afrita athugasemdir og viðhengi. Annaðhvort er hægt að afrita dreifingarnar eða leyfa endursköpun þeirra við bókun.

Eftir afritun á línum er hægt að breyta upplýsingum eftir þörfum.

## <a name="create-a-free-text-invoice-from-a-template"></a>Búa til reikning með frjálsum texta út frá sniðmáti
Þú getur búið til reikning með frjálsum texta út frá sniðmáti. Þegar **Nýtt úr sniðmáti** er valið úr flipanum **Reikningur** er hægt að velja sniðmátsheiti og viðskiptavinalykilinn fyrir nýja reikninginn með frjálsum texta. Sjálfgefin gildi, svo sem greiðsluskilmálar og greiðslumáti, geta sjálfkrafa verið fyllt út af viðskiptavininum, eða hægt er að nota gildin sem voru vistuð í sniðmátinu.

Nýr reikningur með frjálsum texta verður búinn til og hægt er að breyta gildunum eftir þörfum.

## <a name="resetting-the-workflow-status-for-free-text-invoices-from-unrecoverable-to-draft"></a>Endurstillir stöðu verkflæðis fyrir reikninga með frjálsum texta úr óendurheimtanlegum í drög
Verkflæðistilvik sem hefur stöðvast út af óendurkræfri villu verður með stöðu verkflæðis sem **Óendurkræft**. Þegar staða verkflæðis viðskiptaflæðis fyrir ókeypis textareikning er **Óendurheimtanlegt**, þú getur endurstillt það á **Drög** með því að velja **Muna** frá verkflæðisaðgerðum. Þú getur síðan breytt ókeypis textareikningi viðskiptavinarins. Þessi eiginleiki er í boði ef **Endurstilla vinnuflæðisstöðu fyrir reikninga með frjálsum texta úr Óendurheimtanlegur í Drög** breytu á **Eiginleikastjórnun** kveikt er á síðunni.

Hægt er að nota síðuna **Sama verkflæðis** til að endurstilla verkflæðisstöðuna sem **Drög**. Þú getur opnað þessa síðu frá **Ókeypis textareikningur** eða frá **Algengar > Fyrirspurnir > Verkflæði**. Til að núllstilla stöðu flæðis á **Drög**, veldu **afturkalla**. Þú getur líka endurstillt vinnuflæðisstöðuna á **Drög** með því að velja **Muna** aðgerð á **Ókeypis textareikningur** síðu eða **Allir ókeypis textareikningar** síðu. Eftir að verkflæðisstaðan er endurstillt á **Drög**, verður það tiltækt til klippingar á **Ókeypis textareikningur** síðu.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
