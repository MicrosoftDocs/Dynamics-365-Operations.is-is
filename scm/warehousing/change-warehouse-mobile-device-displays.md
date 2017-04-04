---
title: "Birtingarstillingar fyrir fartæki vöruhúss"
description: "Þessi grein lýsir hvernig setja á upp útlit skjás fartækisins og hvernig á að varpa flýtilyklum á stýrieiningar, til dæmis hnappar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserSetup, WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: 721b293d1f8c76458ca510732f9bb94f003ac6e3
ms.lasthandoff: 03/31/2017


---

# <a name="warehouse-mobile-device-display-settings"></a>Birtingarstillingar fyrir fartæki vöruhúss

Þessi grein lýsir hvernig setja á upp útlit skjás fartækisins og hvernig á að varpa flýtilyklum á stýrieiningar, til dæmis hnappar. 

Þessi grein á við um aðgerðir „ítarlegs vöruhúss“ í vöruhúsakerfi. Hægt er að nota fartæki fyrir mörg verk sem starfsmenn í vöruhúsi framkvæma.

## <a name="specify-styles-and-map-keyboard-shortcuts"></a>Tilgreina stíla og varpa flýtilykla
Sem hluti af skilgreiningu fartækis er hægt að skilgreina mismunandi útlit fyrir fartæki. Til að gera þetta þarf að vita nafn skrárinnar Stölluð Stílblöð (CSS) og Active Server Síðu Nafnauka (ASPX) skrá. Sjálfgefnar skrár eru settar upp sem hluti af uppsetningu Gátt fyrir Fartæki Vöruhúss. Ef ekki vitað skrárheiti, getur notandi beðið kerfisstjóra. Hægt er að skilgreina nýja stíl á síðunni **Skjástillingar fartækis**:

-    Í reitnum **CSS-skrá** er heiti fyrir skrána fært inn. Hafa .css skráarnafnauka með.
-   Í reitnum **Yfirlit birtingarstillinga fartækis** skal tilgreina ASPX skrána. **Ekki** skal taka fram .aspx skrárendinguna.

CSS og ASPX skrár verða að vera í tilteknu skráasafni svo að Internet Information Services (IIS) umsókninni hægt að sækja þær. Það gæti verið gagnlegt að skilgreina mismunandi CSS skrár ef verið er að keyra fartækjavirkni í mismunandi vöfrum eða á misminandi gerðum vélbúnaður, sem krefjast mismunandi útlitsstýringar. Auðveldlega er hægt að stýra einföldum stillingum eins og bakgrunnslit, letri og leturstærð fyrir texta, og breidd og hegðun hnappa, með notkun mismunandi CSS-skráa. ASPX skráin er notuð til að birta í fartækisvefsvæði þjóni ASP.NET umsókninni. Skráin stjórnar hvernig heildaruppbygging HTML lítur út. Góð hugmynd er að sérsníða þessa virkni aðeins ef alvarleg vandamál koma upp við uppbyggingu á HTML og JavaScript og þú þarft að breyta kóðanum fyrir tiltekin tæki fyrirtækisins. Til að kortleggja HTML-stýringar á síðu fartækja skal úthluta talnakóðum á lyklana á síðunni **Skjástillingar fartækis**, í reitnum **Flýtivísanir**. Hægt er að nota valmyndina **Skoða kóða fyrir flýtilykla** í fartæki til að finna talnakóða. Athugið að vörpununum gæti verið mismunandi eftir vélbúnaðinum sem er notað. Nota eftirfarandi málskipan til að stofna vörpun:

&lt;heiti stýringar&gt;(&lt;lykilheiti&gt;) =&lt;slá kóðann&gt;;

Hér er skýring á hlutum í málskipan:

-   **&lt;heiti stýringar&gt;** – heiti stýringarinnar (til dæmis hnappur) sem er vistuð í HTML.
-   **(&lt;lykilheiti&gt;) ** – Nafn lyklaborð lykillinn sem verið er að stofna flýtivísun fyrir.
-   **&lt;Lykill kóða&gt;** – kóði fyrir lykill sem nota á sem flýtilykill tölustaf.

Eftirfarandi er dæmi:

Hætta við (Esc) = 27; Full (F2) = 113

Á öllum síðum sem innihalda hnappinn **Hætta við** mun hann hafa þennan texta:

**(Esc) Hætta við**

Ef stutt er á Esc-lykilinn á lyklaborði virkjast hnappurinn **Hætta við**. Til að nota stillingar á stíl og flýtileiðum lyklaborðs á tilteknu tæki, verður að stofna vörpun í reitnum **Skilyrði**. Það verður að nota .NET regluleg segð til að stofna vörpun og segðin verður að samanstanda af þremur hlutum sem eru aðskildir með lóðréttum strikum (|), eins og sýnt er hér:

Request.UserHostAddress=&lt;notanda host aðsetur&gt;| HostName =&lt;hýsilheiti notanda&gt;| Request.UserAgent=&lt;gerandi notanda&gt;

Hér er skýring á hlutum segðar:

-   **&lt;heimilisfang notanda host&gt;** – A .NET reglulegu segð sem passar við beiðandinn ip-tala.
-   **&lt;hýsilheiti notanda&gt;** – A .NET regluleg segð sem samsvarar beiðandinn nafn net.
-   **&lt;gerandi notanda&gt;** – A .NET regluleg segð sem samsvarar kenni vafra beiðandinn notar.

Eftirfarandi dæmi auðveldar notkun á Internet Explorer 8:

Request.UserHostAddress=. \*| HostName =. \*| Request.UserAgent=MSIE\\s8\\.0

Hægt er að nota valmyndina **Skoða skilgreiningu þjóns fyrir birtingarstillingar** í fartæki til að finna upplýsingar um uppsetningu.

## <a name="define-text-colors-for-messages"></a>Skilgreina textaliti fyrir skilaboð
Hægt er að nota síðuna **Textalitur fartækis** til að stýra mismunandi litum sem eru notaðir í kerfistölvupóstinn, eins og villuboð. Til dæmis getur textalitur tilgreint tilgang eða villustig skilaboðanna. Eftirfarandi gerðir skilaboða eru sýnd.

| Gerð skilaboða | Lýsing                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sjálfgefinn      | Sjálfgefin skilaboð nota sjálfgefnar litastillingar fyrir öll skilaboð, eins og skilgreint er með css-skrá fyrir Fartækjagátt Vöruhúss.                                                   |
| Villa        | Villuboðin gefa til kynna vandamál sem notandinn verður að leysa áður en hann eða hún getur haldið áfram.                                                                                             |
| Tókst      | Árangursskilaboð staðfesta að aðgerð hafi tekist.                                                                                                                                |
| Viðvörun      | Viðvörunarboð tilkynna starfsmanninum að það sé vandamál eða að vandamál geti komið upp ef starfsmaðurinn heldur áfram. Hins vegar þarf starfsmaðurinn ekki að leysa vandamálið til að halda áfram. |

Til að velja lit á síðunni **Velja lit** skal smella á litaspjald eða sláið inn sextándakerfislitakóði.

## <a name="define-the-date-format-to-use-on-mobile-devices"></a>Skilgreina snið dagsetningar til að nota í fartækjum
Hægt er að útvíkka lista yfir samþykkta dagsetning snið fyrir hverja uppsetningu. Þessi geta getur verið gagnleg til dæmis ef ætlunin er að veita snið sem auðveldar starfsmanni að færa inn dagsetningar í fartæki. Sjálfgefið snið ákvarðast af sjálfgefnu tungumáli notanda, sem er tilgreind í reitnum **Tungumál** á síðunni **Notendastillingar**. (Á sömu síðu er einnig notuð til að tengja starfsmann við tiltekið vöruhús vinnunotanda.) **Athugasemd:** í Gátt fyrir Fartæki Vöruhúss ekki nota stillingin í **Dagsetning tíma- og tölusniði** í í **Tungumáls og svæðis kjörstillingar** síðu. Til að breyta sniði dagsetningar, þarf að þekkja almennar segðir í Microsoft .NET Framework. Nánari upplýsingar, sjá [.NET Framework almennar segðir](http://go.microsoft.com/fwlink/?LinkId=391260). Til að skilgreina snið dagsetningu skal breyta Dates.ini skránni sem er staðsett í Innihald\\Stillingar\\Dates.ini á þjóninum Gátt fyrir Fartæki Vöruhúss. Þessi skrá notar .NET reglulegar segðir til að ákvarða snið dagsetningar. Reglulega segðin verður að innihalda undirsegðir sem stofna nefnda flokka fyrir dag, mánuð og ár (DDMMYY), eins og sýnt er í eftirfarandi dæmi:

^(? &lt;day&gt;\\d{2})(?&lt; month&gt;\\d{2})(?&lt; ár&gt;\\d {2}) $

Hver undirsegð krefst eins til tveggja tölustafa fyrir daginn og mánuðinn og eins til fjögurra tölustafa fyrir árið. Til dæmis skilgreinir eftirfarandi undirsegð nefndan flokk fyrir ár og krefst minnst tveggja tölustafa eða að hámarki fjögurra:

(? &lt;year&gt;\\d{2,4})

Hægt er að tilgreina fleiri en eina segð í sömu skránni. Hver segð verður að vera í aðskilinni línu. Fyrsta segðin sem er jöfnuð er notuð til að þátta dagsetninguna.

<a name="see-also"></a>Sjá einnig
--------

[Configuration of mobile devices for warehouse work](configure-mobile-devices-warehouse.md)


