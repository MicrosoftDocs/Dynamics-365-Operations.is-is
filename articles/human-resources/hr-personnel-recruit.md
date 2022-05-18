---
title: Ráða umsækjendur
description: Þetta efni lýsir því hvernig á að ráða umsækjendur í Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ef2f2c82708fd48055faa7546e7e0c4da51e7b6c
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/10/2022
ms.locfileid: "8733986"
---
# <a name="recruit-job-candidates"></a>Ráða umsækjendur


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources aðstoðar þig við að stjórna ráðningarbeiðnum. Aðstoðar þig einnig við að breyta umsækjendum í starfsmenn á einfaldan hátt. Þegar fyrirtækið þitt notar annað ráðningarforrit kann ráðningarferlið að fela í sér eftirfarandi skref:<!--note from editor: Should this be a numbered list? These steps do seem to follow a particular order.-->

- Sláðu inn ráðningarbeiðnina þína í Human Resources.
- Taktu á móti tilvísunum frá ráðningarforritinu í Human Resources.
- Ljúktu samþykktarferli umsækjanda í Human Resources.

Þegar þú notar ekki annað ráðningarforrit getur þú einnig haft umsjón með umsækjendum handvirkt í Human Resources.

> [!NOTE]
> Ef þú ert stjórnandi eða þróunaraðili og vilt samþætta mannauð við ráðningarforrit þriðja aðila, farðu á [Stilla Dataverse sameining](hr-admin-integration-common-data-service.md) og [Stilla Dataverse sýndarborðum](hr-admin-integration-common-data-service-virtual-entities.md)
>
> Einnig er hægt að finna samþættingarforrit ráðninga á [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).
>
## <a name="enable-recruiting-requests-on-the-merged-infrastructure"></a>Virkjaðu ráðningarbeiðnir á sameinuðu innviði

Ef þú vilt senda inn ráðningarbeiðnir í mannaráðningum verður þú fyrst að virkja **HR notendaupplifun** og **Stjórnun ráðningarferlis** eiginleikar.

Þegar kveikt hefur verið á eiginleikum skaltu velja virknina með eftirfarandi skrefum: 
1. Fara til **Mannauður** > **Uppsetning** > **Stærðir mannauðs**.
2. Á  **Ráðningar**  flipann, stilltu **Ráðningar óvirkar** sviði til **Nei**.
3. Í **Reynsla af ráðningum** fellivalmynd, veldu **HR ráðningar**.   

> [!Note] 
> Einu sinni **HR ráðningar** er valið, **Ráðningarverkefni** (arfleifð) verður eingöngu lesin. 


## <a name="add-a-recruiting-request-location"></a>Bæta við staðsetningu í ráðningarbeiðni

Ef fyrirtækið er með margar staðsetningar er hægt að bæta þeim við til að beiðendur geti valið staðsetningarnar þar sem nýi starfsmaðurinn á að starfa. Staðsetningin verður höfð með í starfsauglýsingunni.

1. Sláðu inn í leitarstikuna **Staðsetning ráðningarbeiðni**.
2. Veljið **Nýtt**.
3. Sláðu inn heiti staðsetningarinnar í svæðið **Staðsetning ráðningarbeiðni**.

    ![Bæta við staðsetningu í ráðningarbeiðni.](./media/hr-recruit-0a-add-location.png)

4. Fyrir **Lýsing**, sláðu inn lýsingu fyrir staðsetninguna.
5. Undir **Staðsetning** skal velja **Bæta við**. Ef **Nýtt heimilisfang** valmynd birtist, sláðu inn heimilisfangið fyrir staðsetninguna.<!--note from editor: Please make the address in this image less plausible. Via the fictitious guidelines on CELAweb: For street addresses, you should use sequential numbers, common street names, and incorrect zip codes (e.g., 4567 Main St Buffalo, NY 98052). (See https://microsoft.sharepoint.com/sites/CELAWeb-Copyrights-Trademarks-And-Patents/SitePages/trademarks-fictitious-names.aspx)-->

    ![Færa inn aðsetur.](./media/hr-recruit-0b-address.png)

6. Færðu inn upplýsingar um tengilið staðsetningarinnar fyrir neðan **Tengiliðaupplýsingar**.
7. Veljið **Vista**.

## <a name="add-a-recruiting-request"></a>Bæta við ráðningarbeiðni

Stjórnendur geta sent inn ráðningarbeiðnir í mannauði. Þegar annað ráðningarforrit er notað verður ráðningarbeiðni send um leið og þessum skrefum er lokið og ráðningarferlið hefst í áðurnefndu forriti. Ljúktu að öðrum kost við þetta ferli til að hefja verkflæði fyrir eigið innra ráðningarferli.

1. Veljið **Sjálfsafgreiðsla starfsmanna**.
2. Smelltu á flipann **Teymið mitt**.
3. Veldu **Beiðni um ráðningu**.

    ![Hefja ráðningarbeiðni.](./media/hr-recruit-1-request-to-recruit.png)

4. Fylltu út svæðin **Lýsing**, **Starf** og **Áætlaður upphafsdagur**.

    ![Ljúka ráðningarbeiðninni.](./media/hr-recruit-2-request-to-recruit.png)

5. Veldu **Haltu áfram**. Ráðningarbeiðnin fyrir stöðuna þína birtist.
6. Undir **Almennt**, veldu ráðningaraðila frá **Ráðunautur** fellilistanum og veldu síðan staðsetningu úr **Staðsetning ráðningarbeiðni** fellilista.
7. Breyttu öllum upplýsingum eins og þörf krefur í svæðinu **Starf** veldu síðan **Búa til upplýsingar úr starfi**.

    ![Búa til upplýsingar út frá starfi.](./media/hr-recruit-3-create-details-from-job.png)

    Restin af ráðningarbeiðninni verður fyllt út með sjálfgefnum upplýsingum fyrir starfið sem þú slóst inn.

8. Fyrir neðan **Ytri lýsing** skal færa inn ytri starfslýsingu.
9. Fyrir neðan **Stöður** skal velja **Bæta við** og síðan velja staðsetningu fyrir þessa ráðningarbeiðni.<!--note from editor: In all of these images, are they approved fictitious names, or do they come from sample data included with the app?-->

    ![Bæta við stöðu.](./media/hr-recruit-4-select-position.png)

10. Fyrir neðan **Hæfni** skal velja **Bæta við** og síðan bæta við hæfni.
11. Undir **Menntunarkröfur**, veldu **Bæta við**, og veldu síðan gildi úr **Menntun** og **Menntunarstig** fellivalmyndir.

    ![Bæta við menntunarkröfum.](./media/hr-recruit-5-select-educational-requirements.png)

12. Bættu við athugasemdum eftir þörfum fyrir neðan **Athugasemd**.
13. Undir **Bætur**, veldu stig úr **Stig** fellilistanum og stilltu síðan **Lágur þröskuldur**, **·**, og **Hár þröskuldur** eftir þörfum.
14. Þegar ráðningarbeiðninni þinni er lokið og þú er til reiðu til að hefja ráðningarferlið skaltu velja **Virkja** á valmyndarstikunni.

    ![Virkja ráðningarbeiðni.](./media/hr-recruit-6-activate-recruit-request.png)

15. Veldu **Vista**.

## <a name="view-and-edit-your-recruiting-requests"></a>Skoða og breyta ráðningarbeiðnum

Ef þú ert yfirmaður og vilt skoða eigin beiðnir:

1. Veljið **Sjálfsafgreiðsla starfsmanna**.
2. Smelltu á flipann **Teymið mitt**.
3. Fyrir neðan **Upplýsingar um teymi** skal velja flipann **Ráðningarbeiðnir**.

    ![Veldu flipann Ráðningarbeiðnir.](./media/hr-recruit-7-recruiting-requests.png)

4. Veldu ráðningarbeiðni á hnitanetinu til að skoða eða breyta henni.

Ef þú ert HR-Pro og vilt skoða allar ráðningarbeiðnir:

1. Veldu **Starfsmannastjórnun**.
2. Veljið **Ráðningarbeiðnir**.

    ![Skoða ráðningarbeiðnir í Starfsmannastjórnun.](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. Veldu ráðningarbeiðni á hnitanetinu til að skoða eða breyta henni.

## <a name="add-or-edit-a-candidate-profile"></a>Bæta við eða breyta notandaupplýsingum umsækjanda

Þegar fyrirtækið hefur samþætt við annað forrit til að vinna úr ráðningarbeiðnum eru ráðningarbeiðnir áframsendar í umrætt forrit. Ráðningarumsóknin sendir síðan upplýsingar umsækjenda aftur til Human Resources. Að öðrum kosti er hægt að fylgja eigin innri ráðningarferlum og slá inn upplýsingar umsækjenda handvirkt.

1. Veldu **Starfsmannastjórnun**.
2. Veljið **Tenglar**.
3. Undir **Ráðning** skal velja **Umsækjendur**.

    ![Skoða umsækjendur.](./media/hr-recruit-9-candidates.png)

4. Veldu **Nýr** til að bæta við umsækjanda. Þegar breyta á fyrirliggjandi umsækjanda skal velja umsækjanda á listanum og síðan velja **Breyta**. Notandaupplýsingar umsækjanda birtast.
5. Fyrir neðan **Samantekt á umsækjendum** skal færa inn eða breyta upplýsingum umsækjanda eftir þörfum.
6. Veljið ráðningarbeiðni sem á að tengja umsækjanda við undir **Ráðningarbeiðni**. Ljúktu síðan við **Áætlaður upphafsdagur**, **·**, **·**, og **Lýsing** reiti, eftir því sem við á.

    ![Tengill í ráðningarbeiðni.](./media/hr-recruit-10-link-to-recruiting-request.png)

7. Fyllið út allar upplýsingar á eftirfarandi svæðum sem á að hafa með í færslu umsækjanda:

    - **Athugasemdir**
    - **Starfsreynsla**
    - **Tengslaupplýsingar**
    - **Menntun**
    - **Hæfni**
    - **Skírteini**
    - **Skoðanir**

8. Veljið **Vista**.

## <a name="hire-a-candidate"></a>Ráða umsækjanda

Þegar þú ert til reiðu að ráða umsækjanda skaltu fylgja þessu ferli til að breyta umsækjanda í starfsmann.

1. Á **Frambjóðandi** síðu, veldu **Ráða**.

    ![Ráða umsækjanda.](./media/hr-recruit-11-hire.png)

2. Á **Ráða nýjan starfsmann** síða, undir **Upplýsingar**, fylltu út alla reiti.

    ![Slá inn nýjar ráðningarupplýsingar.](./media/hr-recruit-12-hire-new-worker.png)

3. Fyrir neðan **Frekari upplýsingar um stöðu** skaltu staðfesta og breyta upplýsingum eftir þörfum.
4. Í **Gátlisti fyrir nýliða** skal velja viðeigandi gátlista fyrir þennan starfsmann.
5. Veljið **Halda áfram** til að stofna starfsmannafærslu.

    > [!NOTE]
    > Það fer eftir verkflæði fyrirtækisins þíns, umsækjendaskráin gæti farið í gegnum viðbótarsamþykktarskref áður en hún verður starfsmannaskrá.

## <a name="decide-not-to-hire-a-candidate"></a>Ákveðið að ráða ekki umsækjanda

Þegar ákveðið er að ráða ekki umsækjanda skaltu fylgja þessu ferli til að fjarlægja viðkomandi úr greiningarferlinu. 

1. Á **Frambjóðandi** síðu, veldu **Ekki ráða**.

    ![Ekki ráða umsækjanda.](./media/hr-recruit-13-do-not-hire.png)

2. Veljið **Ástæðukóði** og takið með allar athugasemdir.
3. Veldu **Í lagi**.

## <a name="dismiss-a-candidate"></a>Hunsa umsækjanda

Þú getur hunsað umsækjanda eftir ráðningu þeirra, ef þörf krefur. Til dæmis gæti umsækjandi hafnað tilboðinu eða ekki mætt fyrsta daginn.

- Á **Frambjóðandi** síðu, veldu **Segja frambjóðanda upp**.

    ![Hunsa umsækjanda.](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>Sjá einnig

[Skilgreina Dataverse-sýndartöflur](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Skipuleggja starfsfólk](hr-personnel-departments-jobs-positions.md)<br>
[Setja upp íhluti verks](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
