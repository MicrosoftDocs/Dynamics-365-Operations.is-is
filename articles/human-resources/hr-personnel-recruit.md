---
title: Ráða umsækjendur
description: Þetta efnisatriði sýnir hvernig á að ráða umsækjendur í Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dc883606b832dc75b28f6209b05c0e35a51036b8
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359678"
---
# <a name="recruit-job-candidates"></a>Ráða umsækjendur

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources aðstoðar þig við að stjórna ráðningarbeiðnum. Aðstoðar þig einnig við að breyta umsækjendum í starfsmenn á einfaldan hátt. Þegar fyrirtækið þitt notar annað ráðningarforrit kann ráðningarferlið að fela í sér eftirfarandi skref:

- Sláðu inn ráðningarbeiðnina þína í Human Resources.
- Taktu á móti tilvísunum frá ráðningarforritinu í Human Resources.
- Ljúktu samþykktarferli umsækjanda í Human Resources.

Þegar þú notar ekki annað ráðningarforrit getur þú einnig haft umsjón með umsækjendum handvirkt í Human Resources.

>[!NOTE]
>Þegar þú ert stjórnandi eða þróunaraðili og vilt samþætta Human Resources við ráðningarforrit þriðja aðila er frekari upplýsingar að finna í [Grunnstilling Dataverse Samþætting](hr-admin-integration-common-data-service.md) og [Grunnstilling Dataverse sýndartöflur](hr-admin-integration-common-data-service-virtual-entities.md)
>
> Einnig er hægt að finna samþættingarforrit ráðninga á [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).
>
> Til að prófa eiginleikann fyrir samþættingu við LinkedIn Talent Hub skal skoða [Samþætting við LinkedIn Talent Hub](hr-admin-integration-linkedin.md).

## <a name="enable-recruiting-requests"></a>Virkja ráðningarbeiðnir

Ef þú vilt senda ráðningarbeiðnir í Human Resources verður þú fyrst að virkja eiginleikann í **Samnýttar færibreytur fyrir mannauð**.

1. Á vinnusvæðinu **Starfsmannastjórnun** velur þú **Tenglar**.

2. Undir **Uppsetning**, veldu **Samnýttar færibreytur fyrir mannauð**.

3. Á flipanum **Ráðning**, fyrir neðan **RÁÐNINGAR** verður að stilla **Virkja ráðningarbeiðnir** á **Já**.

## <a name="add-a-recruiting-request-location"></a>Bæta við staðsetningu í ráðningarbeiðni

Ef fyrirtækið er með margar staðsetningar er hægt að bæta þeim við til að beiðendur geti valið staðsetningarnar þar sem nýi starfsmaðurinn á að starfa. Staðsetningin verður höfð með í starfsauglýsingunni.

1. Sláðu inn **staðsetning ráðningarbeiðni** í leitarstikuna.

2. Veljið **Nýtt**.

3. Sláðu inn heiti staðsetningarinnar í svæðið **Staðsetning ráðningarbeiðni**.

   ![Bæta við staðsetningu í ráðningarbeiðni.](./media/hr-recruit-0a-add-location.png)

4. Sláðu inn lýsingu á staðsetningunni í svæðið **Lýsing**.

5. Undir **Staðsetning** skal velja **Bæta við**. Sláðu inn heimilisfang staðsetningarinnar ef sprettiglugginn **Nýtt heimilisfang** opnast.

   ![Færa inn aðsetur.](./media/hr-recruit-0b-address.png)

6. Færðu inn upplýsingar um tengilið staðsetningarinnar fyrir neðan **Tengiliðaupplýsingar**.

7. Veljið **Vista**.

## <a name="add-a-recruiting-request"></a>Bæta við ráðningarbeiðni

Stjórnendur geta sent inn ráðningarbeiðnir í mannauði. Þegar annað ráðningarforrit er notað verður ráðningarbeiðni send um leið og þessum skrefum er lokið og ráðningarferlið hefst í áðurnefndu forriti. Ljúktu að öðrum kost við þetta ferli til að hefja verkflæði fyrir eigið innra ráðningarferli.

1. Veljið **Sjálfsafgreiðsla starfsmanna**.

2. Smelltu á flipann **Teymið mitt**.

3. Veljið **Beiðni um að ráða**.

   ![Hefja ráðningarbeiðni.](./media/hr-recruit-1-request-to-recruit.png)

4. Fylltu út svæðin **Lýsing**, **Starf** og **Áætlaður upphafsdagur**.

   ![Ljúka ráðningarbeiðninni.](./media/hr-recruit-2-request-to-recruit.png)

5. Veldu **Haltu áfram**. Ráðningarbeiðnin fyrir stöðuna þína birtist.

6. Fyrir neðan flipann **Almennt** skal velja ráðningaraðila á fellilistanum **Ráðningaraðili** og síðan velja staðsetningu á fellilistanum **Staðsetning ráðningarbeiðni**.

7. Breyttu öllum upplýsingum eins og þörf krefur í svæðinu **Starf** veldu síðan **Búa til upplýsingar úr starfi**.

   ![Búa til upplýsingar út frá starfi.](./media/hr-recruit-3-create-details-from-job.png)

   Eftirstandandi svæði ráðningarbeiðninnar eru fyllt út með sjálfgefnum upplýsingum um starfið sem þú slóst inn.

8. Fyrir neðan **Ytri lýsing** skal færa inn ytri starfslýsingu.

9. Fyrir neðan **Stöður** skal velja **Bæta við** og síðan velja staðsetningu fyrir þessa ráðningarbeiðni.

   ![Bæta við stöðu.](./media/hr-recruit-4-select-position.png)

10. Fyrir neðan **Hæfni** skal velja **Bæta við** og síðan bæta við hæfni.

11. Fyrir neðan **Menntunarkröfur** skal velja **Bæta við** og síðan velja gildi á fellilistunum **Menntun** og **Menntunarstig**.

   ![Bæta við menntunarkröfum.](./media/hr-recruit-5-select-educational-requirements.png)

12. Bættu við athugasemdum eftir þörfum fyrir neðan **Athugasemd**.

13. Fyrir neðan **Laun** skal velja stig á fellilistanum **Stig** og síðan stilla **Neðri mörk**, **Stýripunkt** og **Efri mörk** eftir þörfum.

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

6. Veljið ráðningarbeiðni sem á að tengja umsækjanda við undir **Ráðningarbeiðni**. Fylltu síðan út svæðin **Áætluð upphafsdagsetning**, **Ráðningarstjóri**, **Staða** og **Lýsing** eftir þörfum.

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

1. Veldu **Ráða** á eyðublaði umsækjandans.

   ![Ráða umsækjanda.](./media/hr-recruit-11-hire.png)

2. Fylltu út öll svæði eyðublaðsins **Ráða nýjan starfsmann** fyrir neðan **Frekari upplýsingar**.

   ![Slá inn nýjar ráðningarupplýsingar.](./media/hr-recruit-12-hire-new-worker.png)

3. Fyrir neðan **Frekari upplýsingar um stöðu** skaltu staðfesta og breyta upplýsingum eftir þörfum.

4. Í **Gátlisti fyrir nýliða** skal velja viðeigandi gátlista fyrir þennan starfsmann.

5. Veljið **Halda áfram** til að stofna starfsmannafærslu.

   >[!NOTE]
   >Færsla umsækjandans kann að fara í gegnum frekari samþykktarskref áður en henni er breytt í starfsmannsfærslu, allt eftir verkflæði fyrirtækisins.

## <a name="decide-not-to-hire-a-candidate"></a>Ákveðið að ráða ekki umsækjanda

Þegar ákveðið er að ráða ekki umsækjanda skaltu fylgja þessu ferli til að fjarlægja viðkomandi úr greiningarferlinu. 

1. Veldu **Ekki ráða** á eyðublaði umsækjandans.

   ![Ekki ráða umsækjanda.](./media/hr-recruit-13-do-not-hire.png)

2. Veljið **Ástæðukóði** og takið með allar athugasemdir.

3. Veldu **Í lagi**.

## <a name="dismiss-a-candidate"></a>Hunsa umsækjanda

Þú getur hunsað umsækjanda eftir ráðningu þeirra, ef þörf krefur. Til dæmis gæti umsækjandi hafnað tilboðinu eða ekki mætt fyrsta daginn.

- Veldu **Hunsa umsækjanda** á eyðublaði umsækjandans.

  ![Hunsa umsækjanda.](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>Sjá einnig

[Skilgreina Dataverse-sýndartöflur](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Skipuleggja starfsfólk](hr-personnel-departments-jobs-positions.md)<br>
[Setja upp íhluti verks](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
