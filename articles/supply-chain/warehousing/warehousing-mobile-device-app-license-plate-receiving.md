---
title: Móttaka númeraplötu í gegnum vöruhúsaforritið
description: Þetta efnisatriði útskýrir hvernig á að setja upp vöruhúsaforrit til að styðja notkun móttökuferlis númeraplötu til að taka á móti efnislegum birgðum.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346377"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a>Móttaka númeraplötu í gegnum vöruhúsaforritið

Þetta efnisatriði útskýrir hvernig á að setja upp vöruhúsaforrit þannig að það styðji notkun móttökuferlis númeraplötu til að taka á móti efnislegum birgðum.

Þú getur notað þessa aðgerð til að skrá fljótt móttöku á birgðum á innleið sem tengjast tilkynningu um sendingu (ASN). Kerfið stofnar sjálfkrafa ASN þegar ferli vöruhússtjórnunar eru notuð til að senda flutningspöntun. Fyrir innkaupapöntunarferlið er hægt að skrá ASN handvirkt eða flytja það sjálfkrafa inn með því að nota ASN gagnaeiningarferli á innleið.

ASN gögnin eru tengd við farm og sendingar um *pakkaskipan*, þar sem bretti (yfirnúmeraplötur) geta innihaldið mál (faldaðar númeraplötur).

> [!NOTE]
> Til að fækka birgðafærslum þegar pakkaskipan sem hefur faldaðar númeraplötur er notuð skráir kerfið efnislegar lagerbirgðir á yfirnúmeraplötuna. Til að kveikja á hreyfingu efnislegrar lagerbirgða frá yfirnúmeraplötunni yfir á faldaðar númeraplötur, byggðar á pakkaskipunargögnum, verður fartækið að bjóða upp á valmyndaratriði sem er byggt á vinnusköpunarferlinu *Pakka á faldaðar númeraplötur*.

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a>Sýna eða sleppa móttökuyfirlitssíðu

Hægt er að nota eiginleikann *Stjórna því hvort á að birta yfirlitssíðu móttöku í fartækjum* til að nýta sér ítarlegra flæði vöruhúsaforrits sem hluta af móttöku númeraplötu.

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Í vinnusvæðinu **Stjórnun eiginleika** er þessi eiginleiki skráður á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Eiginleikaheiti:** *Stjórna því hvort sýna á viðtakandi samantektarsíðu í fartækjum*

Þegar kveikt er á þessari aðgerð munu valmyndaratriðin í fartækinu fyrir móttöku númeraplötu eða móttöku og frágang númeraplötu veita stillinguna **Birta yfirlitssíðu móttöku**. Þessi stilling hefur eftirfarandi valkosti:

- **Birta ítarlegt yfirlit** - Við móttöku númeraplötu munu starfsmenn sjá auka síðu sem sýnir allar ASN upplýsingar.
- **Sleppa yfirlitinu** - Starfsmenn sjá ekki allar ASN upplýsingar. Starfsmenn vörugeymsluhússins ekki heldur sett upp ráðstöfunarkóða eða bætt við undantekningum meðan á móttökuferlinu stendur.

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Komdu í veg fyrir að númeraplötur með flutningspöntunum–sent séu notaðar í vöruhúsum öðrum en ákvörðunarvöruhúsinu

Ekki er hægt að nota móttökuferli númeraplötu ef ASN inniheldur kenni númeraplötu sem þegar eru til og eru með efnisleg gögn á lager í öðru vöruhúsi en vöruhússtaðnum þar sem skráningarmerki skráningar er að gerast.

Fyrir aðstæður flutningspöntunar þar sem flutningsvöruhúsið rekur ekki númeraplöturnar (og rekur þar af leiðandi ekki heldur efnislegar lagerbirgðir á hverja númeraplötu) er hægt að nota eiginleikann *Koma í veg fyrir að númeraplötur með sendum flutningspöntunum séu notaðar í öðrum vöruhúsum en ákvörðunarvöruhúsinu* til að koma í veg fyrir efnislegar birgðauppfærslur á númeraplötum sem eru í flutningi.

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Í vinnusvæðinu **Stjórnun eiginleika** er þessi eiginleiki skráður á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Koma í veg fyrir að númeraplötur með sendum flutningspöntunum séu notaðar í öðrum vöruhúsum en ákvörðunarvöruhúsinu*

Fylgdu þessum skrefum til að stjórna virkni þegar þessi eiginleiki er tiltækur.

1. Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.
1. Á flipanum **Almennt**, á flýtiflipanum **Númeraplötur**, stillirðu reitinn **Reglur um númeraplötu flutningsvöruhúsa** á eitt af eftirfarandi gildum:

    - **Leyfa endurnotkun á óröktum númeraplötum** - Kerfið virkar á sama hátt og það virkar þegar eiginleikinn *Koma í veg fyrir að númeraplötur með sendum flutningspöntunum séu notaðar í öðrum vöruhúsum en ákvörðunarvöruhúsinu* er ekki í boði. Þetta gildi er sjálfgefin stilling þegar þú virkjar eiginleikann fyrst.
    - **Koma í veg fyrir endurnotkun á óröktum númeraplötum** - Aðeins handvirkar uppfærslur sem tengjast sendum númeraplötum verða leyfðar í ákvörðunarvöruhúsinu þar til flutningspöntunin hefur borist.

## <a name="more-information"></a>Meiri upplýsingar

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

Nánari upplýsingar um valmyndaratriði fartækja, sjá [Uppsetning fartækja fyrir vöruhúsavinnu](configure-mobile-devices-warehouse.md).
