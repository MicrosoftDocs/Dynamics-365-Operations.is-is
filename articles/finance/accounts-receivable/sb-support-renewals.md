---
title: Þjónusta og endurnýjanir
description: Í þessari grein er útskýrt hvernig á að setja upp og nota stuðnings- og endurnýjunarferli í sölupöntunum til að búa til greiðsluáætlun fyrir endurnýjunarvörur.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: b40e0136883d909755480a3ce101627297bd9ffb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896522"
---
# <a name="support-and-renewals"></a>Þjónusta og endurnýjanir 

Þessi grein útskýrir hvernig á að færa inn stuðningsvörur eða endurnýjunarvörur þegar þú færir inn sölupantanir. Þessar vörur eru notaðar til að reikna út upphæð gjalds fyrir upprunalegan þjónustusamning og/eða endurnýjunarupphæð sem er notað þegar greiðsluáætlun er búin til í áskriftargreiðslu. Fyrirtækið þitt selur til dæmis viðskiptavinum netþjón og þú býður upp á gagnaafritunaráskrift fyrir fyrsta árið og möguleikann á að endurnýja áskriftina á hverju ári. *Þjónustuvaran* er áskriftin fyrir fyrsta árið og *endurnýjunarvaran* er endurnýjunin fyrir hvert ár sem fylgir.

Hægt er að slá inn upplýsingar um stuðningssamninginn, endurnýjunarsamninginn eða hvort tveggja. Þegar upplýsingar um þjónustusamning eru færðar inn er aðeins þjónustuvörunni bætt við sölupöntunina. Þegar upplýsingar um endurnýjunarsamninginn eru færðar inn er endurnýjunarvaran notuð til að búa til greiðsluáætlun.

## <a name="support-and-renewal-setup"></a>Uppsetning þjónustu og endurnýjunar

Á síðunni **Þjónustu- og endurnýjunarstig** er hægt að setja upp þjónustustig fyrir þjónustu- og endurnýjunarvörur. Þjónustan eða endurnýjunin getur verið prósenta af upprunalegri upphæð vöru eða getur verið stöðluð upphæð.

Hægt er að velja sjálfgefin stuðningsstig á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur**.

Til dæmis gæti fyrirtæki boðið eftirfarandi stuðnings- og endurnýjunarstig.

| Stuðningsstig | Þjónustuhlutfall | Prósenta endurnýjunar |
|---|---|---|
| Ótakmarkað | 40% | 30% |
| Gull | 25% | 18% |
| Silfurgrátt | 20% | 14% |
| Brons | 15% | 10% |

Til að stofna stuðnings- eða endurnýjunarstig skal fylgja þessum skrefum.

1. Á síðunni **Stuðnings- og endurnýjunarstig** skal velja **Nýtt**.
2. Í svæðinu **Stuðningsstig** er fært inn einkvæmt heiti.
3. Í reitnum **Lýsing** skal færa inn lýsingu.
4. Í reitnum **Reikningsaðferð fyrir stuðning** skal velja reikningsaðferð fyrir stuðning. Ef valið er **Prósenta**, færið inn stuðningsprósentu í reitinn **Stuðningsprósenta**.
5. Í reitnum **Reikningsaðferð fyrir endurnýjun** skal velja reikningsaðferð fyrir endurnýjun. Ef valið er **Prósenta**, færið inn endurnýjunarprósentu í reitinn **Endurnýjunarprósenta**.
6. Veldu **Vista**.

### <a name="fields"></a>Svæði

Á síðunni **Stuðnings- og endurnýjunarstig** eru eftirfarandi reitir.

| Svæði | Lýsing |
|---|---|
| Stuðningsstig | Einkvæmt auðkenni fyrir stuðnings- eða endurnýjunarstig (t.d. **Gull** eða **Silfur**). |
| Lýsing | Lýsing á stuðnings- eða endurnýjunarstigi. |
| Útreikningsaðferð þjónustu | Velja stuðningsútreikningsaðferð fyrir stigið: **Prósent** eða **Stöðluð upphæð**. |
| Þjónustuhlutfall | Ef **Prósenta** er valið sem útreikningsaðferð þjónustu skal tilgreina prósentuna sem notuð er til að reikna út verðið á þjónustuvörunni. Ef **Stöðluð upphæð** var valið sem útreikningsaðferð er upphæðin tilgreind þegar færslan er stofnuð. |
| Útreikningsaðferð endurnýjunar | Velja endurnýjunarútreikningsaðferð fyrir stigið: **Prósent** eða **Stöðluð upphæð**. |
| Prósenta endurnýjunar | Ef **Prósenta** var valið sem útreikningsaðferð endurnýjunar skal tilgreina prósentuna sem notuð er til að reikna út verð endurnýjunarvörunnar. Ef **Stöðluð upphæð** var valið sem útreikningsaðferð er upphæðin tilgreind þegar færslan er stofnuð. |

## <a name="support-and-renewal-process"></a>Þjónustu- og endurnýjunarferli

Þjónustu- og endurnýjunaraðgerðin getur notað mismunandi þjónustustig á vörur og uppfært upplýsingar um endurnýjun í áskriftargreiðslu.

Áður en þú notar stuðnings- og endurnýjunaraðgerðina verður eftirfarandi verkefnum að vera lokið.

1. Á síðunni **Stuðnings- og endurnýjunarstig** skal búa til að minnsta kosti eitt stuðnings- eða endurnýjunarstig.
2. Á síðunni **Vöruuppsetning** skal tengja vöru við stuðnings- og endurnýjunarvörur. Þetta verk er aðeins nauðsynlegt ef setja á upp sjálfgefin gildi fyrir þjónustu- og/eða endurnýjunarvörur.
3. Á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur** skal tilgreina sjálfgefnar stillingar þjónustu og endurnýjunar fyrir nýjar greiðsluáætlanir.

Til að nota mismunandi stuðningsstig á vörur og uppfæra endurnýjunarupplýsingar skaltu fylgja þessum skrefum.

1. Stofnið sölupöntun á síðunni **Allar sölupantanir**.
2. Í flýtiflipanum **Sölupöntunarlínur** skal velja vöru.
3. Á flipanum **Reikningur** velur þú **Stuðningur og endurnýjun \> Bæta við stuðningi og endurnýjun**.
4. Á síðunni **Þjónustu- og endurnýjunarferli** er haushlutinn uppfærður með stillingunum af síðunni **Færibreytur fyrir endurteknar samningsgreiðslur**. Þessi gildi gilda um öll stuðnings- og endurnýjunaratriði. (Ef greiðslutíðnin er til dæmis stillt á **Árlega**, eru allar sölulínur sem eru búnar til og eru með endurnýjunarvöru með árlega tíðni.) Til að tengja sölupöntunina við fyrirliggjandi greiðsluáætlun skal velja gildi í reitnum **Númer greiðsluáætlunar**.
5. Til að breyta upphafsdegi stuðnings eða endurnýjunar skal stilla valkostinn **Hnekkja upphafsdagsetningu** á **Já**.
6. Til að bæta við eða breyta þjónustuvöru skal velja gátreitinn **Þjónusta** og síðan færa inn þjónustuvöru í reitinn **Þjónustuvara**. Vörunni er bætt við sölupöntunina.
7. Til að bæta við eða breyta endurnýjunarvöru skal velja gátreitinn **Endurnýjun** og síðan færa inn endurnýjunarvöru í reitinn **Endurnýjunarvara**. Þegar sölupöntunin er reikningsfærð verður til greiðsluáætlun sem inniheldur vöruna.
8. Veldu **Í lagi**.
9. Í flipanum **Stofna** skal velja **Reikningur**. Þegar sölupöntunin er bókuð er greiðsluáætlunin stofnuð. Tilkynning með upplýsingum um greiðsluáætlun birtist í skilaboðunum.
10. Á listasíðunni **Allar/virkar greiðsluáætlanir** skal velja númer greiðsluáætlunar til að fara yfir upplýsingarnar um greiðsluáætlunina á síðunni **Greiðsluáætlanir**.
11. Í flýtiflipanum **Greiðsluáætlunarlínur** skal velja **Þjónusta og endurnýjun** til að fara yfir upplýsingarnar um línurnar sem voru búnar til.

> [!NOTE]
> Ef breyta þarf upphafsdagsetningu endurnýjunar fyrir greiðsluáætlunarlínu er hægt að breyta gildinu **Upphafsdagsetning** fyrir línuna á síðunni **Greiðsluáætlanir**. Þegar síðan **Skoða greiðsluupplýsingar** er opnuð fyrir lína er reiturinn **Upphafsdagsetning greiðslu** uppfærður með nýju dagsetningunni. Gildið **Lokadagsetning innheimtu** er endurreiknað miðað við greiðslutíðni. Aðeins er hægt að uppfæra upphafsdagsetningu endurnýjunar ef ekki er búið að búa til og bóka fyrsta reikninginn fyrir greiðsluáætlun endurnýjunar. Ekki er hægt að breyta upphafsdegi eftir að fyrsti reikningurinn er búinn til að og bókaður.

Stuðnings- og endurnýjunarferlið er aðeins í boði fyrir sölupöntunina. Þegar þjónustu- og endurnýjunarvörum er bætt við sölupöntun er hægt að búa til nýja greiðsluáætlun eða bæta endurnýjunarvörunni við fyrirliggjandi greiðsluáætlun.

## <a name="support-and-renewal-audit"></a>Eftirlit með þjónustu og endurnýjun

Á síðunni **Eftirlit með þjónustu og endurnýjun** er hægt að fara yfir upplýsingarnar um greiðsluáætlunarlínurnar sem eru búnar til úr endurnýjunarvörunni í sölupöntun. Þessi valkostur er í boði þegar vara greiðsluáætlunarlínunnar er endurnýjunarvara.

Til að breyta upplýsingum um stuðning og endurnýjun fyrir greiðsluáætlunarlínu skaltu fylgja þessum skrefum.

1. Á síðunni **Allar greiðsluáætlanir** skal velja greiðsluáætlunarnúmerið.
2. Veldu hlutann **Greiðsluáætlunarlínur**, veldu línu og veldu svo **Stuðningur og endurnýjun**.
3. Yfirfarðu allar upplýsingarnar fyrir stuðnings- eða endurnýjunaratriðið.
4. Gerðu allar nauðsynlegar breytingar á þjónustustiginu eða prósentu endurnýjunar eða upphæðar og færðu síðan inn gildi í reitinn **Ástæða breytingar**.
5. Veljið **Ferli**.

### <a name="fields"></a>Svæði

Á síðunni **Stuðningur og endurnýjun endurskoðunar** eru eftirfarandi reitir.

| Svæði | Lýsing |
|-------|-------------|
| Vörunúmer | Vörunúmerið fyrir greiðsluáætlunarlínuna. |
| Afurðarheiti | Afurðarheitið. |
| Stig þjónustuáætlunar | Skoða eða breyta þjónustustigi fyrir endurnýjunarvöru. |
| Prósenta endurnýjunar | Færðu inn endurnýjunarprósentuna sem er notuð þegar einingarverðið er reiknað út fyrir endurnýjunarvöru í greiðsluáætlun. |
| Upphæð endurnýjunar | Færðu inn endurnýjunarupphæðina sem er notuð þegar einingarverðið er reiknað út fyrir endurnýjunarvöru í greiðsluáætlun. |
| Ástæða breytingar | Skráðu ástæðu þess að þú ert að breyta upplýsingum um stuðning og endurnýjun. Færa þarf inn ástæðu þegar gildinu er breytt fyrir **Prósenta endurnýjunar**, **Upphæð endurnýjunar** eða **Stig þjónustuáætlunar**. |
| Upphafleg söluvara | Upprunalegt söluvörunúmer úr sölupöntuninni. |
| Upphafleg nettóupphæð | Upprunaleg nettóupphæð fyrir vöruna. |
| Upphaflegt þjónustustig | Upprunalegt þjónustustig vörunnar. |
| Upphafleg prósenta endurnýjunar | Upprunalegt endurnýjunarhlutfall fyrir vöruna. |
| Upphafleg upphæð endurnýjunar | Upprunaleg endurnýjunarupphæð fyrir vöruna. |
| **Hnitanet** | |
| Upphaflegt þjónustustig | Fyrra stuðningsstigið. |
| Upphafleg prósenta endurnýjunar | Fyrri endurnýjunarprósenta. |
| Upphafleg upphæð endurnýjunar | Fyrri endurnýjunarupphæð. |
| Breytt hefur | Notandanafn notandans sem gerði breytinguna. |
| Breytt dagsetning og tími | Dagsetningin sem breytingin átti sér stað á. |
| Ástæða | Ástæða fyrir breytingunni. |
