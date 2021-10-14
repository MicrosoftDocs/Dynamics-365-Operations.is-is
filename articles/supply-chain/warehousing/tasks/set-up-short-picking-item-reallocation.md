---
title: Setja upp endurúthlutun fyrir stutta vörutiltekt
description: Í þessu efnisatriði er sýnt hvernig á að gera starfsmönnum vöruhúss kleift að finna aðrar staðsetningar á fljótlegan hátt ef ekki eru nægar birgðir á staðsetningunni sem þeim var vísað á.
author: Mirzaab
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7fe17246037a35e44d12476f184af3bd4c806022
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565233"
---
# <a name="set-up-short-picking-item-reallocation"></a>Setja upp endurúthlutun fyrir stutta vörutiltekt

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig starfsmenn vöruhúss geta fundið aðrar staðsetningar fljótt ef það eru ekki nægilegar birgðir á staðsetningunni þangað sem þeim var beint. 

Endurúthlutunarferlinu er stjórnað af **Vinnuundantekningu** og notað af **starfsmanni** vöruhúss.

Mögulegt er að nota sjálfvirka, handvirka eða bæði endurúthlutunarferlin:

- Sjálfvirk endurúthlutun - Staðsetningarleiðbeiningar eru notaðar til að ákvarða hvort vörur eru tiltækar á annarri staðsetningu. Ef það er hægt verður vinnan uppfærð og notanda vöruhúss verður vísað á hina staðsetninguna.
- Handvirk endurúthlutun - Gerir notanda vöruhúss kleift að velja úr einni eða fleiri staðsetningum með ófráteknu magni af vörum. 
- Sjálfvirkt og handvirkt - Ef kerfið getur ekki framkvæmt sjálfvirka endurúthlutun og staðsetningar eru tiltækar fyrir ófrátekið magn, verður notandinn beðinn um að velja staðsetningu.

## <a name="set-up-work-exceptions"></a>Setja upp vinnuundantekningar
Það er hægt að skilgreina margar vinnuundantekningar ásamt mismunandi endurúthlutunarreglum til að gera starfsmaður í vöruhúsi mögulegt að velja eitt á grundvelli þess sem sendingin sem verið er að vinna þarf.

USMF sýniútgáfu fyrirtækis notað til að stofna þetta ferli.

1. Í **Skoðunarrúðu** ferðu í **Vöruhúsakerfi > Uppsetning > Vinna > Undantekningar verks**.
2. Smelltu á **Nýtt** 
3. Í reitinn **Kenni undantekningar verks** skaltu færa inn gildi. Þetta verður titill þessarar undantekningar. Til dæmis, handbók fyrir of litla tiltekt.
4. Í reitinn **Lýsing** skal slá inn gildi. Þetta verður stutt lýsing á notkun þessarar undantekningar. Til dæmis, Of lítil tiltekt - vara ekki í boði.
5. Í reitnum **Undantekning** skal velja **Of lítil tiltekt**.
6. Veldu gátreitinn **Leiðrétta birgðir**. Ef valinn, verða birgðir sjálfvirkt leiðréttar á 0 á staðsetningu þar sem tiltekt er of lítil.
7. Í reitinn **Sjálfgefinn kóði leiðréttingargerðar** skal færa inn eða velja gildi. Til dæmis í USMF er hægt að velja **Fjarlægja leiðrétta frátekt á útleið**. Hver kóði leiðréttingargerðar inniheldur fjóra eiginleika: heiti, lýsing, færslubókarheiti og **Fjarlægja frátekningar**. Ef **Fjarlægja frátekningu** er virkjað verða frátekningar pöntunarlínu of lítillar tiltektar fjarlægðar.  
8. Í reitnum **Endurúthlutun vöru** skal velja gildi, t.d. handvirkt. Ef valið er Handvirkt, eða Sjálfvirkar og Handvirkar, þarf starfsmaður í vöruhúsi að geta notað handvirka endurúthlutun.

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Setja upp starfsmann til að nota handvirka endurúthlutun vöru

USMF sýniútgáfu fyrirtækis notað til að stofna þetta ferli.

1. Lokið síðunni.
2. Í **Skoðunarrúðu** ferðu í **Vöruhúsakerfi > Uppsetning > Vinna > Starfskraftur**.
3. Smellið á **Breyta**.
4. Í listanum skal velja starfskraft. Til dæmis Julia Funderburk.
5. Stækkið flýtiflipann **Notendur**.
6. Í listanum skal velja **Notandakenni**. Til dæmis 24.
7. Stækkið flýtiflipann **Verk**.
8. Velja skal **Já** í svæðinu **Leyfa handvirka endurúthlutun vöru**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]