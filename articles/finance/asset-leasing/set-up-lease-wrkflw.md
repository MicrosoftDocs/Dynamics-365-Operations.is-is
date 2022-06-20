---
title: Setja upp samþykktarverkflæði leigusamnings
description: Greinin útskýrir hvernig á að setja upp samþykkisverkflæði sem mun keyra þegar nýr leigusamningur er stofnaður.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0162e559f8aaec248cfb9042b0152788536c9fc9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870279"
---
# <a name="set-up-lease-approval-workflows"></a>Setja upp samþykktarverkflæði leigusamnings

[!include [banner](../includes/banner.md)]

Greinin útskýrir hvernig á að setja upp samþykkisverkflæði sem mun keyra þegar nýr leigusamningur er stofnaður. Upplýsingar um það hvernig á að nota verkflæðið er að finna í [nota samþykktarverkflæði leigusamninga](use-create-lease-wrkflw.md). 

1. Opnið **Eignarleiga \> Uppsetning \> Verkflæði leigusamnings**.
2. Á síðunni **Verkflæði leigusamnings** skal velja **Nýtt**.
3. Í svarglugganum sem birtist, undir **Verkflæðisgerð**, skal velja tengilinn **Verkflæði leigusamnings**.

    Forritið opnast. Eftir að það er keyrt skal skrá sig inn á Azure Active Directory (Azure AD) til að komast í verkflæðiforritið.

4. Dragið **Verkflæðissamþykki leigusamnings** eininguna inn á verkflæðið.
5. Tengið einn hnút frá **Ræsa** í **Verkflæðissamþykki leigusamnings**. Tengið svo **Verkflæðissamþykki leigusamnings** í **Ljúka**.
6. Tvísmellið á **Verkflæðissamþykki leigusamnings**.
7. Veljið **Eiginleikar** og færi svo inn heiti fyrir verkflæðið undir **Grunnstillingar**.

    Á þessari síðu er einnig hægt að setja upp fleiri færibreytur fyrir verkflæðið. Ef kveikt hefur verið á **sjálfvirkum aðgerðum** mun kerfið sjálfkrafa framkvæma tiltekna aðgerð. Hægt er að senda tilkynningar ef þær eru tilgreindar á flipanum **Tilkynningar**. Á flipanum **Ítarlegar stillingar** er hægt að tilgreina endanlegan samþykktaraðila, stilla tímamörk og tilnefna tilteknar aðgerðir sem þarf að ljúka.

8. Þegar búið er að stilla færibreytur verkflæðis skal velja **Loka**.
9. Veljið **Skref 1** og veljið svo **Eiginleikar**.
10. Undir **Grunnstillingar** skal færa inn heiti fyrir skrefið, stofna efnislínu fyrir samþykkið og tilgreina leiðbeiningar fyrir samþykkið.
11. Á síðunni **Úthlutun** er valin úthlutunargerð.
12. Til að úthluta tilteknum notendum á samþykktina skal velja **Notandi**, velja notendur sem samþykkja leigusamninga og velja svo **Loka**.
13. Veljið **Vista og loka** til að stofna verkflæðið. Síðan, þegar beðið er um það, skal velja **Í lagi**.
14. Á síðunni **Stofna verkflæði** skal velja **Loka**.
14. Veldu nýja verkflæðið og veldu því næst **Útgáfur**. Síðan skal velja **Virkja** til að tryggja að verkflæðið sé virkt.
15. Veljið **Loka**. Nýja virka útgáfan birtist.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
